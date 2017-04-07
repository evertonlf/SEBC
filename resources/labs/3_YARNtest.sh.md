[root@cluster1node1 results]# cat script_yarn.sh
#!/bin/sh
# Confirm the path values given below correspond to your installation

MR=/opt/cloudera/parcels/CDH-5.10.1-1.cdh5.10.1.p0.10/lib/hadoop-mapreduce/
HADOOP=/usr/bin

# Mark start of the loop
echo Testing loop started on `date`

# Mapper containers
for i in $(seq 1 16)
do
   # Reducer containers
   for j in $(seq 1 16)
   do
      # Container memory
      for k in 512 1024
      do
         # Set mapper JVM heap
         MAP_MB=`echo "($k*0.8)/1" | bc`

         # Set reducer JVM heap
         RED_MB=`echo "($k*0.8)/1" | bc`

                echo Mappers $i
                echo Reducers $j
                echo Memory $k
                echo MAP_MB $MAP_MB
                echo RED_MB $RED_MB

                time ${HADOOP}/hadoop jar ${MR}/hadoop-mapreduce-examples.jar teragen \
                     -Dmapreduce.job.maps=$i \
                     -Dmapreduce.map.memory.mb=$k \
                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
                     51200 /yarn/tg-10GB-${i}-${j}-${k} 1>times/tera_${i}_${j}_${k}.out 2>times/tera_${i}_${j}_${k}.err

                time ${HADOOP}/hadoop jar $MR/hadoop-mapreduce-examples.jar terasort \
                     -Dmapreduce.job.maps=$i \
                     -Dmapreduce.job.reduces=$j \
                     -Dmapreduce.map.memory.mb=$k \
                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
                     -Dmapreduce.reduce.memory.mb=$k \
                     -Dmapreduce.reduce.java.opts.max.heap=$RED_MB \
                     /yarn/tg-10GB-${i}-${j}-${k}  \
                     /yarn/ts-10GB-${i}-${j}-${k} 1>>times/tera_${i}_${j}_${k}.out 2>>times/tera_${i}_${j}_${k}.err

       $HADOOP/hadoop fs -rm -r -skipTrash /yarn/tg-10GB-${i}-${j}-${k}
       $HADOOP/hadoop fs -rm -r -skipTrash /yarn/ts-10GB-${i}-${j}-${k}
      done
   done
done

echo Testing loop ended on `date`
[root@cluster1node1 results]#
