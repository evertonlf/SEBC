[neymar@cluster1node5 root]$ time hadoop jar /opt/cloudera/parcels/CDH-5.9.1-1.cdh5.9.1.p0.4/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /user/neymar/tgen640 /user/neymar/tsort640m
17/04/14 15:20:56 INFO terasort.TeraSort: starting
17/04/14 15:20:59 INFO hdfs.DFSClient: Created token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@EVERTONLF.ES, renewer=yarn, realUser=, issueDate=1492209659782, maxDate=1492814459782, sequenceNumber=3, masterKeyId=14 on ha-hdfs:nameservice1
17/04/14 15:20:59 INFO security.TokenCache: Got dt for hdfs://nameservice1; Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:nameservice1, Ident: (token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@EVERTONLF.ES, renewer=yarn, realUser=, issueDate=1492209659782, maxDate=1492814459782, sequenceNumber=3, masterKeyId=14)
17/04/14 15:21:00 INFO input.FileInputFormat: Total input paths to process : 1
Spent 590ms computing base-splits.
Spent 11ms computing TeraScheduler splits.
Computing input splits took 603ms
Sampling 10 splits of 410
Making 4 from 100000 sampled records
Computing parititions took 7379ms
Spent 7986ms computing partitions.
17/04/14 15:21:07 INFO client.RMProxy: Connecting to ResourceManager at cluster1node1.lab.local/192.168.100.161:8032
17/04/14 15:21:08 INFO mapreduce.JobSubmitter: number of splits:410
17/04/14 15:21:09 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1492207720354_0003
17/04/14 15:21:09 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: ha-hdfs:nameservice1, Ident: (token for neymar: HDFS_DELEGATION_TOKEN owner=neymar@EVERTONLF.ES, renewer=yarn, realUser=, issueDate=1492209659782, maxDate=1492814459782, sequenceNumber=3, masterKeyId=14)
17/04/14 15:21:09 INFO impl.YarnClientImpl: Submitted application application_1492207720354_0003
17/04/14 15:21:09 INFO mapreduce.Job: The url to track the job: http://cluster1node1.lab.local:8088/proxy/application_1492207720354_0003/
17/04/14 15:21:09 INFO mapreduce.Job: Running job: job_1492207720354_0003
17/04/14 15:21:26 INFO mapreduce.Job: Job job_1492207720354_0003 running in uber mode : false
17/04/14 15:21:26 INFO mapreduce.Job:  map 0% reduce 0%
17/04/14 15:21:47 INFO mapreduce.Job:  map 1% reduce 0%
17/04/14 15:21:48 INFO mapreduce.Job:  map 2% reduce 0%
17/04/14 15:21:58 INFO mapreduce.Job:  map 3% reduce 0%
17/04/14 15:22:08 INFO mapreduce.Job:  map 4% reduce 0%
17/04/14 15:22:20 INFO mapreduce.Job:  map 5% reduce 0%
17/04/14 15:22:26 INFO mapreduce.Job:  map 6% reduce 0%
17/04/14 15:22:32 INFO mapreduce.Job:  map 7% reduce 0%
17/04/14 15:22:42 INFO mapreduce.Job:  map 8% reduce 0%
17/04/14 15:22:48 INFO mapreduce.Job:  map 9% reduce 0%
17/04/14 15:22:54 INFO mapreduce.Job:  map 10% reduce 0%
17/04/14 15:23:11 INFO mapreduce.Job:  map 11% reduce 0%
17/04/14 15:23:20 INFO mapreduce.Job:  map 12% reduce 0%
17/04/14 15:23:29 INFO mapreduce.Job:  map 13% reduce 0%
17/04/14 15:23:36 INFO mapreduce.Job:  map 14% reduce 0%
17/04/14 15:23:59 INFO mapreduce.Job:  map 15% reduce 0%
17/04/14 15:24:19 INFO mapreduce.Job:  map 16% reduce 0%
17/04/14 15:24:30 INFO mapreduce.Job:  map 17% reduce 0%
17/04/14 15:24:45 INFO mapreduce.Job:  map 18% reduce 0%
17/04/14 15:24:51 INFO mapreduce.Job:  map 19% reduce 0%
17/04/14 15:25:00 INFO mapreduce.Job:  map 20% reduce 0%
17/04/14 15:25:19 INFO mapreduce.Job:  map 21% reduce 0%
17/04/14 15:25:23 INFO mapreduce.Job:  map 22% reduce 0%
17/04/14 15:25:32 INFO mapreduce.Job:  map 23% reduce 0%
17/04/14 15:25:40 INFO mapreduce.Job:  map 24% reduce 0%
17/04/14 15:25:45 INFO mapreduce.Job:  map 25% reduce 0%
17/04/14 15:25:56 INFO mapreduce.Job:  map 26% reduce 0%
17/04/14 15:25:59 INFO mapreduce.Job:  map 27% reduce 0%
17/04/14 15:26:17 INFO mapreduce.Job:  map 28% reduce 0%
17/04/14 15:26:21 INFO mapreduce.Job:  map 29% reduce 0%
17/04/14 15:26:29 INFO mapreduce.Job:  map 30% reduce 0%
17/04/14 15:26:41 INFO mapreduce.Job:  map 31% reduce 0%
17/04/14 15:26:47 INFO mapreduce.Job:  map 32% reduce 0%
17/04/14 15:26:54 INFO mapreduce.Job:  map 33% reduce 0%
17/04/14 15:27:08 INFO mapreduce.Job:  map 34% reduce 0%
17/04/14 15:27:15 INFO mapreduce.Job:  map 35% reduce 0%
17/04/14 15:27:26 INFO mapreduce.Job:  map 36% reduce 0%
17/04/14 15:27:28 INFO mapreduce.Job:  map 37% reduce 0%
17/04/14 15:27:38 INFO mapreduce.Job:  map 38% reduce 0%
17/04/14 15:27:44 INFO mapreduce.Job:  map 39% reduce 0%
17/04/14 15:27:52 INFO mapreduce.Job:  map 40% reduce 0%
17/04/14 15:28:08 INFO mapreduce.Job:  map 41% reduce 0%
17/04/14 15:28:15 INFO mapreduce.Job:  map 42% reduce 0%
17/04/14 15:28:26 INFO mapreduce.Job:  map 43% reduce 0%
17/04/14 15:28:27 INFO mapreduce.Job:  map 44% reduce 0%
17/04/14 15:28:39 INFO mapreduce.Job:  map 45% reduce 0%
17/04/14 15:28:44 INFO mapreduce.Job:  map 46% reduce 0%
17/04/14 15:28:52 INFO mapreduce.Job:  map 47% reduce 0%
17/04/14 15:29:03 INFO mapreduce.Job:  map 48% reduce 0%
17/04/14 15:29:14 INFO mapreduce.Job:  map 49% reduce 0%
17/04/14 15:29:20 INFO mapreduce.Job:  map 50% reduce 0%
17/04/14 15:29:27 INFO mapreduce.Job:  map 51% reduce 0%
17/04/14 15:29:36 INFO mapreduce.Job:  map 52% reduce 0%
17/04/14 15:29:44 INFO mapreduce.Job:  map 53% reduce 0%
17/04/14 15:29:51 INFO mapreduce.Job:  map 54% reduce 0%
17/04/14 15:29:59 INFO mapreduce.Job:  map 55% reduce 0%
17/04/14 15:30:13 INFO mapreduce.Job:  map 56% reduce 0%
17/04/14 15:30:20 INFO mapreduce.Job:  map 57% reduce 0%
17/04/14 15:30:27 INFO mapreduce.Job:  map 58% reduce 0%
17/04/14 15:30:35 INFO mapreduce.Job:  map 59% reduce 0%
17/04/14 15:30:41 INFO mapreduce.Job:  map 60% reduce 0%
17/04/14 15:30:49 INFO mapreduce.Job:  map 61% reduce 0%
17/04/14 15:30:59 INFO mapreduce.Job:  map 62% reduce 0%
17/04/14 15:31:10 INFO mapreduce.Job:  map 63% reduce 0%
17/04/14 15:31:20 INFO mapreduce.Job:  map 64% reduce 0%
17/04/14 15:31:24 INFO mapreduce.Job:  map 65% reduce 0%
17/04/14 15:31:34 INFO mapreduce.Job:  map 66% reduce 0%
17/04/14 15:31:39 INFO mapreduce.Job:  map 67% reduce 0%
17/04/14 15:31:48 INFO mapreduce.Job:  map 68% reduce 0%
17/04/14 15:31:55 INFO mapreduce.Job:  map 69% reduce 0%
17/04/14 15:32:07 INFO mapreduce.Job:  map 70% reduce 0%
17/04/14 15:32:21 INFO mapreduce.Job:  map 71% reduce 0%
17/04/14 15:32:23 INFO mapreduce.Job:  map 72% reduce 0%
17/04/14 15:32:34 INFO mapreduce.Job:  map 73% reduce 0%
17/04/14 15:32:40 INFO mapreduce.Job:  map 74% reduce 0%
17/04/14 15:32:47 INFO mapreduce.Job:  map 75% reduce 0%
17/04/14 15:32:59 INFO mapreduce.Job:  map 77% reduce 0%
17/04/14 15:33:17 INFO mapreduce.Job:  map 78% reduce 0%
17/04/14 15:33:23 INFO mapreduce.Job:  map 79% reduce 0%
17/04/14 15:33:32 INFO mapreduce.Job:  map 80% reduce 0%
17/04/14 15:33:40 INFO mapreduce.Job:  map 81% reduce 0%
17/04/14 15:33:45 INFO mapreduce.Job:  map 82% reduce 0%
17/04/14 15:34:00 INFO mapreduce.Job:  map 83% reduce 0%
17/04/14 15:34:01 INFO mapreduce.Job:  map 83% reduce 4%
17/04/14 15:34:04 INFO mapreduce.Job:  map 83% reduce 9%
17/04/14 15:34:09 INFO mapreduce.Job:  map 83% reduce 12%
17/04/14 15:34:13 INFO mapreduce.Job:  map 83% reduce 13%
17/04/14 15:34:14 INFO mapreduce.Job:  map 83% reduce 15%
17/04/14 15:34:15 INFO mapreduce.Job:  map 83% reduce 17%
17/04/14 15:34:20 INFO mapreduce.Job:  map 83% reduce 18%
17/04/14 15:34:21 INFO mapreduce.Job:  map 84% reduce 20%
17/04/14 15:34:28 INFO mapreduce.Job:  map 84% reduce 21%
17/04/14 15:34:33 INFO mapreduce.Job:  map 85% reduce 21%
17/04/14 15:34:48 INFO mapreduce.Job:  map 86% reduce 21%
17/04/14 15:34:55 INFO mapreduce.Job:  map 86% reduce 22%
17/04/14 15:34:57 INFO mapreduce.Job:  map 87% reduce 22%
17/04/14 15:35:13 INFO mapreduce.Job:  map 88% reduce 22%
17/04/14 15:35:28 INFO mapreduce.Job:  map 89% reduce 22%
17/04/14 15:35:38 INFO mapreduce.Job:  map 90% reduce 22%
17/04/14 15:35:50 INFO mapreduce.Job:  map 90% reduce 23%
17/04/14 15:35:53 INFO mapreduce.Job:  map 91% reduce 23%
17/04/14 15:36:07 INFO mapreduce.Job:  map 92% reduce 23%
17/04/14 15:36:18 INFO mapreduce.Job:  map 93% reduce 23%
17/04/14 15:36:30 INFO mapreduce.Job:  map 94% reduce 23%
17/04/14 15:36:39 INFO mapreduce.Job:  map 94% reduce 24%
17/04/14 15:36:43 INFO mapreduce.Job:  map 95% reduce 24%
17/04/14 15:36:55 INFO mapreduce.Job:  map 96% reduce 24%
17/04/14 15:37:10 INFO mapreduce.Job:  map 97% reduce 24%
17/04/14 15:37:24 INFO mapreduce.Job:  map 98% reduce 24%
17/04/14 15:37:34 INFO mapreduce.Job:  map 99% reduce 25%
17/04/14 15:37:45 INFO mapreduce.Job:  map 100% reduce 25%
17/04/14 15:37:52 INFO mapreduce.Job:  map 100% reduce 28%
17/04/14 15:37:56 INFO mapreduce.Job:  map 100% reduce 36%
17/04/14 15:37:58 INFO mapreduce.Job:  map 100% reduce 51%
17/04/14 15:38:04 INFO mapreduce.Job:  map 100% reduce 53%
17/04/14 15:38:05 INFO mapreduce.Job:  map 100% reduce 54%
17/04/14 15:38:07 INFO mapreduce.Job:  map 100% reduce 58%
17/04/14 15:38:08 INFO mapreduce.Job:  map 100% reduce 60%
17/04/14 15:38:11 INFO mapreduce.Job:  map 100% reduce 62%
17/04/14 15:38:13 INFO mapreduce.Job:  map 100% reduce 64%
17/04/14 15:38:17 INFO mapreduce.Job:  map 100% reduce 68%
17/04/14 15:38:18 INFO mapreduce.Job:  map 100% reduce 70%
17/04/14 15:38:19 INFO mapreduce.Job:  map 100% reduce 72%
17/04/14 15:38:23 INFO mapreduce.Job:  map 100% reduce 76%
17/04/14 15:38:24 INFO mapreduce.Job:  map 100% reduce 78%
17/04/14 15:38:25 INFO mapreduce.Job:  map 100% reduce 80%
17/04/14 15:38:30 INFO mapreduce.Job:  map 100% reduce 82%
17/04/14 15:38:31 INFO mapreduce.Job:  map 100% reduce 91%
17/04/14 15:38:32 INFO mapreduce.Job:  map 100% reduce 92%
17/04/14 15:38:37 INFO mapreduce.Job:  map 100% reduce 93%
17/04/14 15:38:43 INFO mapreduce.Job:  map 100% reduce 95%
17/04/14 15:38:49 INFO mapreduce.Job:  map 100% reduce 96%
17/04/14 15:38:55 INFO mapreduce.Job:  map 100% reduce 97%
17/04/14 15:39:06 INFO mapreduce.Job:  map 100% reduce 98%
17/04/14 15:39:13 INFO mapreduce.Job:  map 100% reduce 99%
17/04/14 15:39:15 INFO mapreduce.Job:  map 100% reduce 100%
17/04/14 15:39:16 INFO mapreduce.Job: Job job_1492207720354_0003 completed successfully
17/04/14 15:39:16 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=2914154841
                FILE: Number of bytes written=5810420773
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=6553647970
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=1242
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=410
                Launched reduce tasks=4
                Data-local map tasks=409
                Rack-local map tasks=1
                Total time spent by all maps in occupied slots (ms)=4235781
                Total time spent by all reduces in occupied slots (ms)=950433
                Total time spent by all map tasks (ms)=4235781
                Total time spent by all reduce tasks (ms)=950433
                Total vcore-seconds taken by all map tasks=4235781
                Total vcore-seconds taken by all reduce tasks=950433
                Total megabyte-seconds taken by all map tasks=4337439744
                Total megabyte-seconds taken by all reduce tasks=973243392
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Map output bytes=6684672000
                Map output materialized bytes=2843032252
                Input split bytes=47970
                Combine input records=0
                Combine output records=0
                Reduce input groups=65536000
                Reduce shuffle bytes=2843032252
                Reduce input records=65536000
                Reduce output records=65536000
                Spilled Records=131072000
                Shuffled Maps =1640
                Failed Shuffles=0
                Merged Map outputs=1640
                GC time elapsed (ms)=47630
                CPU time spent (ms)=1828960
                Physical memory (bytes) snapshot=197248430080
                Virtual memory (bytes) snapshot=654040625152
                Total committed heap usage (bytes)=242083692544
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=6553600000
        File Output Format Counters
                Bytes Written=6553600000
17/04/14 15:39:16 INFO terasort.TeraSort: done

real    18m23.319s
user    0m21.836s
sys     0m1.389s
[neymar@cluster1node5 root]$
