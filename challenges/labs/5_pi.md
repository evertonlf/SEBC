[ronaldo@cluster1node4 /]$ hadoop jar /opt/cloudera/parcels/CDH-5.9.1-1.cdh5.9.1.p0.4/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar pi 16 1000
Number of Maps  = 16
Samples per Map = 1000
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Wrote input for Map #4
Wrote input for Map #5
Wrote input for Map #6
Wrote input for Map #7
Wrote input for Map #8
Wrote input for Map #9
Wrote input for Map #10
Wrote input for Map #11
Wrote input for Map #12
Wrote input for Map #13
Wrote input for Map #14
Wrote input for Map #15
Starting Job
17/04/14 15:18:44 INFO client.RMProxy: Connecting to ResourceManager at cluster1node1.lab.local/192.168.100.161:8032
17/04/14 15:18:44 INFO hdfs.DFSClient: Created token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@EVERTONLF.ES, renewer=yarn, realUser=, issueDate=1492209764748, maxDate=1492814564748, sequenceNumber=4, masterKeyId=14 on ha-hdfs:nameservice1
17/04/14 15:18:44 INFO security.TokenCache: Got dt for hdfs://nameservice1; Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:nameservice1, Ident: (token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@EVERTONLF.ES, renewer=yarn, realUser=, issueDate=1492209764748, maxDate=1492814564748, sequenceNumber=4, masterKeyId=14)
17/04/14 15:18:45 INFO input.FileInputFormat: Total input paths to process : 16
17/04/14 15:18:45 INFO mapreduce.JobSubmitter: number of splits:16
17/04/14 15:18:46 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1492207720354_0004
17/04/14 15:18:46 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:nameservice1, Ident: (token for ronaldo: HDFS_DELEGATION_TOKEN owner=ronaldo@EVERTONLF.ES, renewer=yarn, realUser=, issueDate=1492209764748, maxDate=1492814564748, sequenceNumber=4, masterKeyId=14)
17/04/14 15:18:47 INFO impl.YarnClientImpl: Submitted application application_1492207720354_0004
17/04/14 15:18:47 INFO mapreduce.Job: The url to track the job: http://cluster1node1.lab.local:8088/proxy/application_1492207720354_0004/
17/04/14 15:18:47 INFO mapreduce.Job: Running job: job_1492207720354_0004
17/04/14 15:19:23 INFO mapreduce.Job: Job job_1492207720354_0004 running in uber mode : false
17/04/14 15:19:23 INFO mapreduce.Job:  map 0% reduce 0%
17/04/14 15:19:44 INFO mapreduce.Job:  map 6% reduce 0%
17/04/14 15:19:47 INFO mapreduce.Job:  map 13% reduce 0%
17/04/14 15:19:50 INFO mapreduce.Job:  map 31% reduce 0%
17/04/14 15:19:51 INFO mapreduce.Job:  map 38% reduce 0%
17/04/14 15:20:00 INFO mapreduce.Job:  map 44% reduce 0%
17/04/14 15:20:13 INFO mapreduce.Job:  map 50% reduce 0%
17/04/14 15:20:14 INFO mapreduce.Job:  map 56% reduce 0%
17/04/14 15:20:15 INFO mapreduce.Job:  map 63% reduce 0%
17/04/14 15:20:21 INFO mapreduce.Job:  map 75% reduce 0%
17/04/14 15:20:31 INFO mapreduce.Job:  map 81% reduce 0%
17/04/14 15:20:35 INFO mapreduce.Job:  map 88% reduce 0%
17/04/14 15:20:37 INFO mapreduce.Job:  map 94% reduce 0%
17/04/14 15:20:38 INFO mapreduce.Job:  map 100% reduce 0%
17/04/14 15:20:57 INFO mapreduce.Job:  map 100% reduce 100%
17/04/14 15:20:59 INFO mapreduce.Job: Job job_1492207720354_0004 completed successfully
17/04/14 15:20:59 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=132
                FILE: Number of bytes written=2173584
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=4230
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=67
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=16
                Launched reduce tasks=1
                Data-local map tasks=15
                Rack-local map tasks=1
                Total time spent by all maps in occupied slots (ms)=138308
                Total time spent by all reduces in occupied slots (ms)=10714
                Total time spent by all map tasks (ms)=138308
                Total time spent by all reduce tasks (ms)=10714
                Total vcore-seconds taken by all map tasks=138308
                Total vcore-seconds taken by all reduce tasks=10714
                Total megabyte-seconds taken by all map tasks=141627392
                Total megabyte-seconds taken by all reduce tasks=10971136
        Map-Reduce Framework
                Map input records=16
                Map output records=32
                Map output bytes=288
                Map output materialized bytes=544
                Input split bytes=2342
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=544
                Reduce input records=32
                Reduce output records=0
                Spilled Records=64
                Shuffled Maps =16
                Failed Shuffles=0
                Merged Map outputs=16
                GC time elapsed (ms)=967
                CPU time spent (ms)=14010
                Physical memory (bytes) snapshot=7532093440
                Virtual memory (bytes) snapshot=26896355328
                Total committed heap usage (bytes)=8752988160
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=1888
        File Output Format Counters
                Bytes Written=97
Job Finished in 135.706 seconds
Estimated value of Pi is 3.14250000000000000000
[ronaldo@cluster1node4 /]$
