create user
add user evertonlf
passwd *********




Give pemission o user on hdfs


[root@cluster1node1 /]# sudo -u hdfs hadoop fs -chown -R evertonlf:evertonlf /user/evertonlf



[root@cluster1node1 /]# sudo -u evertonlf time hadoop jar /opt/cloudera/parcels/CDH-5.10.1-1.cdh5.10.1.p0.10/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -D mapreduce.job.maps=4 -D dfs.block.size=33554432 100000000 /user/evertonlf/terageninput
17/04/04 19:31:31 INFO client.RMProxy: Connecting to ResourceManager at cluster1node3.lab.local/192.168.100.163:8032
17/04/04 19:31:32 INFO terasort.TeraGen: Generating 100000000 using 4
17/04/04 19:31:32 INFO mapreduce.JobSubmitter: number of splits:4
17/04/04 19:31:32 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/04/04 19:31:33 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1491340415902_0001
17/04/04 19:31:34 INFO impl.YarnClientImpl: Submitted application application_1491340415902_0001
17/04/04 19:31:34 INFO mapreduce.Job: The url to track the job: http://cluster1node3.lab.local:8088/proxy/application_1491340415902_0001/
17/04/04 19:31:34 INFO mapreduce.Job: Running job: job_1491340415902_0001
17/04/04 19:31:44 INFO mapreduce.Job: Job job_1491340415902_0001 running in uber mode : false
17/04/04 19:31:44 INFO mapreduce.Job:  map 0% reduce 0%
17/04/04 19:32:11 INFO mapreduce.Job:  map 2% reduce 0%
17/04/04 19:32:12 INFO mapreduce.Job:  map 3% reduce 0%
17/04/04 19:32:17 INFO mapreduce.Job:  map 8% reduce 0%
17/04/04 19:32:23 INFO mapreduce.Job:  map 13% reduce 0%
17/04/04 19:32:36 INFO mapreduce.Job:  map 17% reduce 0%
17/04/04 19:32:42 INFO mapreduce.Job:  map 21% reduce 0%
17/04/04 19:32:48 INFO mapreduce.Job:  map 28% reduce 0%
17/04/04 19:32:54 INFO mapreduce.Job:  map 29% reduce 0%
17/04/04 19:32:59 INFO mapreduce.Job:  map 30% reduce 0%
17/04/04 19:33:00 INFO mapreduce.Job:  map 31% reduce 0%
17/04/04 19:33:12 INFO mapreduce.Job:  map 32% reduce 0%
17/04/04 19:33:18 INFO mapreduce.Job:  map 37% reduce 0%
17/04/04 19:33:25 INFO mapreduce.Job:  map 38% reduce 0%
17/04/04 19:33:31 INFO mapreduce.Job:  map 43% reduce 0%
17/04/04 19:33:37 INFO mapreduce.Job:  map 50% reduce 0%
17/04/04 19:33:42 INFO mapreduce.Job:  map 51% reduce 0%
17/04/04 19:33:43 INFO mapreduce.Job:  map 52% reduce 0%
17/04/04 19:33:49 INFO mapreduce.Job:  map 53% reduce 0%
17/04/04 19:34:00 INFO mapreduce.Job:  map 56% reduce 0%
17/04/04 19:34:02 INFO mapreduce.Job:  map 57% reduce 0%
17/04/04 19:34:04 INFO mapreduce.Job:  map 58% reduce 0%
17/04/04 19:34:08 INFO mapreduce.Job:  map 59% reduce 0%
17/04/04 19:34:13 INFO mapreduce.Job:  map 60% reduce 0%
17/04/04 19:34:14 INFO mapreduce.Job:  map 61% reduce 0%
17/04/04 19:34:15 INFO mapreduce.Job:  map 62% reduce 0%
17/04/04 19:34:19 INFO mapreduce.Job:  map 64% reduce 0%
17/04/04 19:34:20 INFO mapreduce.Job:  map 65% reduce 0%
17/04/04 19:34:21 INFO mapreduce.Job:  map 66% reduce 0%
17/04/04 19:34:25 INFO mapreduce.Job:  map 69% reduce 0%
17/04/04 19:34:26 INFO mapreduce.Job:  map 70% reduce 0%
17/04/04 19:34:27 INFO mapreduce.Job:  map 72% reduce 0%
17/04/04 19:34:31 INFO mapreduce.Job:  map 73% reduce 0%
17/04/04 19:34:32 INFO mapreduce.Job:  map 74% reduce 0%
17/04/04 19:34:37 INFO mapreduce.Job:  map 75% reduce 0%
17/04/04 19:34:44 INFO mapreduce.Job:  map 77% reduce 0%
17/04/04 19:34:45 INFO mapreduce.Job:  map 78% reduce 0%
17/04/04 19:34:49 INFO mapreduce.Job:  map 79% reduce 0%
17/04/04 19:34:50 INFO mapreduce.Job:  map 81% reduce 0%
17/04/04 19:34:51 INFO mapreduce.Job:  map 82% reduce 0%
17/04/04 19:34:55 INFO mapreduce.Job:  map 84% reduce 0%
17/04/04 19:34:56 INFO mapreduce.Job:  map 86% reduce 0%
17/04/04 19:34:57 INFO mapreduce.Job:  map 87% reduce 0%
17/04/04 19:35:01 INFO mapreduce.Job:  map 88% reduce 0%
17/04/04 19:35:02 INFO mapreduce.Job:  map 89% reduce 0%
17/04/04 19:35:10 INFO mapreduce.Job:  map 90% reduce 0%
17/04/04 19:35:20 INFO mapreduce.Job:  map 91% reduce 0%
17/04/04 19:35:21 INFO mapreduce.Job:  map 92% reduce 0%
17/04/04 19:35:27 INFO mapreduce.Job:  map 93% reduce 0%
17/04/04 19:35:33 INFO mapreduce.Job:  map 95% reduce 0%
17/04/04 19:35:38 INFO mapreduce.Job:  map 96% reduce 0%
17/04/04 19:35:39 INFO mapreduce.Job:  map 99% reduce 0%
17/04/04 19:35:41 INFO mapreduce.Job:  map 100% reduce 0%
17/04/04 19:35:41 INFO mapreduce.Job: Job job_1491340415902_0001 completed successfully
17/04/04 19:35:41 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=498516
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=929936
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=929936
                Total vcore-seconds taken by all map tasks=929936
                Total megabyte-seconds taken by all map tasks=952254464
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=3831
                CPU time spent (ms)=259190
                Physical memory (bytes) snapshot=820408320
                Virtual memory (bytes) snapshot=6292459520
                Total committed heap usage (bytes)=982515712
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=214760662691937609
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10000000000
10.77user 0.62system 4:14.98elapsed 4%CPU (0avgtext+0avgdata 180512maxresident)k
40inputs+2120outputs (0major+61698minor)pagefaults 0swaps
[root@cluster1node1 /]#








[root@cluster1node1 /]# sudo -u evertonlf time hadoop jar /opt/cloudera/parcels/CDH-5.10.1-1.cdh5.10.1.p0.10/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /user/evertonlf/terageninput /user/evertonlf/terasortoutput
17/04/04 19:44:54 INFO terasort.TeraSort: starting
17/04/04 19:44:57 INFO input.FileInputFormat: Total input paths to process : 4
Spent 522ms computing base-splits.
Spent 13ms computing TeraScheduler splits.
Computing input splits took 536ms
Sampling 10 splits of 300
Making 4 from 100000 sampled records
Computing parititions took 2076ms
Spent 2616ms computing partitions.
17/04/04 19:44:59 INFO client.RMProxy: Connecting to ResourceManager at cluster1node3.lab.local/192.168.100.163:8032
17/04/04 19:45:00 INFO mapreduce.JobSubmitter: number of splits:300
17/04/04 19:45:00 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1491340415902_0002
17/04/04 19:45:00 INFO impl.YarnClientImpl: Submitted application application_1491340415902_0002
17/04/04 19:45:00 INFO mapreduce.Job: The url to track the job: http://cluster1node3.lab.local:8088/proxy/application_1491340415902_0002/
17/04/04 19:45:00 INFO mapreduce.Job: Running job: job_1491340415902_0002
17/04/04 19:45:12 INFO mapreduce.Job: Job job_1491340415902_0002 running in uber mode : false
17/04/04 19:45:12 INFO mapreduce.Job:  map 0% reduce 0%
17/04/04 19:45:30 INFO mapreduce.Job:  map 2% reduce 0%
17/04/04 19:45:36 INFO mapreduce.Job:  map 3% reduce 0%
17/04/04 19:45:45 INFO mapreduce.Job:  map 4% reduce 0%
17/04/04 19:45:46 INFO mapreduce.Job:  map 5% reduce 0%
17/04/04 19:45:58 INFO mapreduce.Job:  map 6% reduce 0%
17/04/04 19:45:59 INFO mapreduce.Job:  map 7% reduce 0%
17/04/04 19:46:12 INFO mapreduce.Job:  map 8% reduce 0%
17/04/04 19:46:19 INFO mapreduce.Job:  map 9% reduce 0%
17/04/04 19:46:22 INFO mapreduce.Job:  map 10% reduce 0%
17/04/04 19:46:32 INFO mapreduce.Job:  map 11% reduce 0%
17/04/04 19:46:35 INFO mapreduce.Job:  map 12% reduce 0%
17/04/04 19:46:43 INFO mapreduce.Job:  map 13% reduce 0%
17/04/04 19:46:47 INFO mapreduce.Job:  map 14% reduce 0%
17/04/04 19:46:53 INFO mapreduce.Job:  map 15% reduce 0%
17/04/04 19:46:59 INFO mapreduce.Job:  map 16% reduce 0%
17/04/04 19:47:11 INFO mapreduce.Job:  map 17% reduce 0%
17/04/04 19:47:16 INFO mapreduce.Job:  map 18% reduce 0%
17/04/04 19:47:20 INFO mapreduce.Job:  map 19% reduce 0%
17/04/04 19:47:30 INFO mapreduce.Job:  map 20% reduce 0%
17/04/04 19:47:33 INFO mapreduce.Job:  map 21% reduce 0%
17/04/04 19:47:44 INFO mapreduce.Job:  map 22% reduce 0%
17/04/04 19:47:47 INFO mapreduce.Job:  map 23% reduce 0%
17/04/04 19:47:52 INFO mapreduce.Job:  map 24% reduce 0%
17/04/04 19:48:01 INFO mapreduce.Job:  map 25% reduce 0%
17/04/04 19:48:07 INFO mapreduce.Job:  map 26% reduce 0%
17/04/04 19:48:19 INFO mapreduce.Job:  map 27% reduce 0%
17/04/04 19:48:21 INFO mapreduce.Job:  map 28% reduce 0%
17/04/04 19:48:27 INFO mapreduce.Job:  map 29% reduce 0%
17/04/04 19:48:34 INFO mapreduce.Job:  map 30% reduce 0%
17/04/04 19:48:38 INFO mapreduce.Job:  map 31% reduce 0%
17/04/04 19:48:47 INFO mapreduce.Job:  map 32% reduce 0%
17/04/04 19:48:51 INFO mapreduce.Job:  map 33% reduce 0%
17/04/04 19:48:56 INFO mapreduce.Job:  map 34% reduce 0%
17/04/04 19:49:08 INFO mapreduce.Job:  map 35% reduce 0%
17/04/04 19:49:15 INFO mapreduce.Job:  map 36% reduce 0%
17/04/04 19:49:23 INFO mapreduce.Job:  map 37% reduce 0%
17/04/04 19:49:26 INFO mapreduce.Job:  map 38% reduce 0%
17/04/04 19:49:32 INFO mapreduce.Job:  map 39% reduce 0%
17/04/04 19:49:39 INFO mapreduce.Job:  map 40% reduce 0%
17/04/04 19:49:46 INFO mapreduce.Job:  map 41% reduce 0%
17/04/04 19:49:51 INFO mapreduce.Job:  map 42% reduce 0%
17/04/04 19:49:55 INFO mapreduce.Job:  map 43% reduce 0%
17/04/04 19:50:00 INFO mapreduce.Job:  map 44% reduce 0%
17/04/04 19:50:11 INFO mapreduce.Job:  map 45% reduce 0%
17/04/04 19:50:20 INFO mapreduce.Job:  map 46% reduce 0%
17/04/04 19:50:25 INFO mapreduce.Job:  map 47% reduce 0%
17/04/04 19:50:31 INFO mapreduce.Job:  map 48% reduce 0%
17/04/04 19:50:35 INFO mapreduce.Job:  map 49% reduce 0%
17/04/04 19:50:40 INFO mapreduce.Job:  map 50% reduce 0%
17/04/04 19:50:47 INFO mapreduce.Job:  map 51% reduce 0%
17/04/04 19:50:50 INFO mapreduce.Job:  map 52% reduce 0%
17/04/04 19:51:00 INFO mapreduce.Job:  map 53% reduce 0%
17/04/04 19:51:10 INFO mapreduce.Job:  map 54% reduce 0%
17/04/04 19:51:19 INFO mapreduce.Job:  map 55% reduce 0%
17/04/04 19:51:22 INFO mapreduce.Job:  map 56% reduce 0%
17/04/04 19:51:29 INFO mapreduce.Job:  map 57% reduce 0%
17/04/04 19:51:36 INFO mapreduce.Job:  map 58% reduce 0%
17/04/04 19:51:39 INFO mapreduce.Job:  map 59% reduce 0%
17/04/04 19:51:50 INFO mapreduce.Job:  map 60% reduce 0%
17/04/04 19:51:51 INFO mapreduce.Job:  map 61% reduce 0%
17/04/04 19:52:00 INFO mapreduce.Job:  map 62% reduce 0%
17/04/04 19:52:11 INFO mapreduce.Job:  map 63% reduce 0%
17/04/04 19:52:19 INFO mapreduce.Job:  map 64% reduce 0%
17/04/04 19:52:24 INFO mapreduce.Job:  map 65% reduce 0%
17/04/04 19:52:27 INFO mapreduce.Job:  map 66% reduce 0%
17/04/04 19:52:32 INFO mapreduce.Job:  map 67% reduce 0%
17/04/04 19:52:39 INFO mapreduce.Job:  map 68% reduce 0%
17/04/04 19:52:46 INFO mapreduce.Job:  map 69% reduce 0%
17/04/04 19:52:50 INFO mapreduce.Job:  map 70% reduce 0%
17/04/04 19:52:58 INFO mapreduce.Job:  map 71% reduce 0%
17/04/04 19:53:04 INFO mapreduce.Job:  map 72% reduce 0%
17/04/04 19:53:10 INFO mapreduce.Job:  map 73% reduce 0%
17/04/04 19:53:21 INFO mapreduce.Job:  map 74% reduce 0%
17/04/04 19:53:23 INFO mapreduce.Job:  map 75% reduce 0%
17/04/04 19:53:33 INFO mapreduce.Job:  map 76% reduce 0%
17/04/04 19:53:36 INFO mapreduce.Job:  map 77% reduce 0%
17/04/04 19:53:37 INFO mapreduce.Job:  map 78% reduce 0%
17/04/04 19:53:49 INFO mapreduce.Job:  map 79% reduce 0%
17/04/04 19:53:51 INFO mapreduce.Job:  map 80% reduce 0%
17/04/04 19:54:09 INFO mapreduce.Job:  map 81% reduce 0%
17/04/04 19:54:13 INFO mapreduce.Job:  map 82% reduce 0%
17/04/04 19:54:19 INFO mapreduce.Job:  map 83% reduce 0%
17/04/04 19:54:32 INFO mapreduce.Job:  map 84% reduce 3%
17/04/04 19:54:36 INFO mapreduce.Job:  map 84% reduce 8%
17/04/04 19:54:38 INFO mapreduce.Job:  map 84% reduce 9%
17/04/04 19:54:42 INFO mapreduce.Job:  map 84% reduce 10%
17/04/04 19:54:44 INFO mapreduce.Job:  map 84% reduce 11%
17/04/04 19:54:46 INFO mapreduce.Job:  map 85% reduce 11%
17/04/04 19:54:48 INFO mapreduce.Job:  map 85% reduce 13%
17/04/04 19:54:50 INFO mapreduce.Job:  map 85% reduce 14%
17/04/04 19:54:54 INFO mapreduce.Job:  map 85% reduce 17%
17/04/04 19:55:00 INFO mapreduce.Job:  map 86% reduce 20%
17/04/04 19:55:07 INFO mapreduce.Job:  map 86% reduce 21%
17/04/04 19:55:12 INFO mapreduce.Job:  map 87% reduce 21%
17/04/04 19:55:13 INFO mapreduce.Job:  map 87% reduce 22%
17/04/04 19:55:20 INFO mapreduce.Job:  map 88% reduce 22%
17/04/04 19:55:33 INFO mapreduce.Job:  map 89% reduce 22%
17/04/04 19:55:36 INFO mapreduce.Job:  map 90% reduce 22%
17/04/04 19:55:47 INFO mapreduce.Job:  map 91% reduce 22%
17/04/04 19:55:49 INFO mapreduce.Job:  map 91% reduce 23%
17/04/04 19:55:55 INFO mapreduce.Job:  map 92% reduce 23%
17/04/04 19:56:08 INFO mapreduce.Job:  map 93% reduce 23%
17/04/04 19:56:20 INFO mapreduce.Job:  map 94% reduce 23%
17/04/04 19:56:29 INFO mapreduce.Job:  map 95% reduce 23%
17/04/04 19:56:31 INFO mapreduce.Job:  map 95% reduce 24%
17/04/04 19:56:39 INFO mapreduce.Job:  map 96% reduce 24%
17/04/04 19:56:51 INFO mapreduce.Job:  map 97% reduce 24%
17/04/04 19:57:00 INFO mapreduce.Job:  map 98% reduce 24%
17/04/04 19:57:08 INFO mapreduce.Job:  map 98% reduce 25%
17/04/04 19:57:14 INFO mapreduce.Job:  map 99% reduce 25%
17/04/04 19:57:20 INFO mapreduce.Job:  map 100% reduce 25%
17/04/04 19:57:26 INFO mapreduce.Job:  map 100% reduce 42%
17/04/04 19:57:27 INFO mapreduce.Job:  map 100% reduce 51%
17/04/04 19:57:32 INFO mapreduce.Job:  map 100% reduce 53%
17/04/04 19:57:33 INFO mapreduce.Job:  map 100% reduce 54%
17/04/04 19:57:34 INFO mapreduce.Job:  map 100% reduce 57%
17/04/04 19:57:38 INFO mapreduce.Job:  map 100% reduce 59%
17/04/04 19:57:39 INFO mapreduce.Job:  map 100% reduce 60%
17/04/04 19:57:40 INFO mapreduce.Job:  map 100% reduce 61%
17/04/04 19:57:44 INFO mapreduce.Job:  map 100% reduce 63%
17/04/04 19:57:45 INFO mapreduce.Job:  map 100% reduce 64%
17/04/04 19:57:46 INFO mapreduce.Job:  map 100% reduce 65%
17/04/04 19:57:50 INFO mapreduce.Job:  map 100% reduce 67%
17/04/04 19:57:51 INFO mapreduce.Job:  map 100% reduce 68%
17/04/04 19:57:52 INFO mapreduce.Job:  map 100% reduce 69%
17/04/04 19:57:56 INFO mapreduce.Job:  map 100% reduce 71%
17/04/04 19:57:57 INFO mapreduce.Job:  map 100% reduce 72%
17/04/04 19:57:58 INFO mapreduce.Job:  map 100% reduce 73%
17/04/04 19:58:03 INFO mapreduce.Job:  map 100% reduce 74%
17/04/04 19:58:04 INFO mapreduce.Job:  map 100% reduce 76%
17/04/04 19:58:05 INFO mapreduce.Job:  map 100% reduce 77%
17/04/04 19:58:08 INFO mapreduce.Job:  map 100% reduce 78%
17/04/04 19:58:10 INFO mapreduce.Job:  map 100% reduce 79%
17/04/04 19:58:11 INFO mapreduce.Job:  map 100% reduce 80%
17/04/04 19:58:16 INFO mapreduce.Job:  map 100% reduce 81%
17/04/04 19:58:21 INFO mapreduce.Job:  map 100% reduce 82%
17/04/04 19:58:23 INFO mapreduce.Job:  map 100% reduce 90%
17/04/04 19:58:27 INFO mapreduce.Job:  map 100% reduce 91%
17/04/04 19:58:29 INFO mapreduce.Job:  map 100% reduce 92%
17/04/04 19:58:35 INFO mapreduce.Job:  map 100% reduce 94%
17/04/04 19:58:41 INFO mapreduce.Job:  map 100% reduce 95%
17/04/04 19:58:47 INFO mapreduce.Job:  map 100% reduce 96%
17/04/04 19:58:53 INFO mapreduce.Job:  map 100% reduce 97%
17/04/04 19:58:59 INFO mapreduce.Job:  map 100% reduce 98%
17/04/04 19:59:05 INFO mapreduce.Job:  map 100% reduce 100%
17/04/04 19:59:09 INFO mapreduce.Job: Job job_1491340415902_0002 completed successfully
17/04/04 19:59:09 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=4457909859
                FILE: Number of bytes written=8839042460
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10000042300
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=912
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=300
                Launched reduce tasks=4
                Data-local map tasks=300
                Total time spent by all maps in occupied slots (ms)=4070629
                Total time spent by all reduces in occupied slots (ms)=845256
                Total time spent by all map tasks (ms)=4070629
                Total time spent by all reduce tasks (ms)=845256
                Total vcore-seconds taken by all map tasks=4070629
                Total vcore-seconds taken by all reduce tasks=845256
                Total megabyte-seconds taken by all map tasks=4168324096
                Total megabyte-seconds taken by all reduce tasks=865542144
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Map output bytes=10200000000
                Map output materialized bytes=4342801127
                Input split bytes=42300
                Combine input records=0
                Combine output records=0
                Reduce input groups=100000000
                Reduce shuffle bytes=4342801127
                Reduce input records=100000000
                Reduce output records=100000000
                Spilled Records=200000000
                Shuffled Maps =1200
                Failed Shuffles=0
                Merged Map outputs=1200
                GC time elapsed (ms)=47950
                CPU time spent (ms)=1936580
                Physical memory (bytes) snapshot=143930126336
                Virtual memory (bytes) snapshot=478701699072
                Total committed heap usage (bytes)=177275404288
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=10000000000
        File Output Format Counters
                Bytes Written=10000000000
17/04/04 19:59:09 INFO terasort.TeraSort: done
16.36user 1.17system 14:16.92elapsed 2%CPU (0avgtext+0avgdata 251256maxresident)k
0inputs+2936outputs (0major+77948minor)pagefaults 0swaps
[root@cluster1node1 /]#






















