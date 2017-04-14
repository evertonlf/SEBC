{\rtf1\ansi\ansicpg1252\cocoartf1504\cocoasubrtf820
{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\fnil\fcharset0 Menlo-Regular;}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;\red255\green255\blue255;}
{\*\expandedcolortbl;;\csgray\c0;\csgray\c100000;}
\paperw11900\paperh16840\margl1440\margr1440\vieww13260\viewh8080\viewkind0
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0\fs24 \cf0 Output teragen Command\
\pard\tx560\tx1120\tx1680\tx2240\tx2800\tx3360\tx3920\tx4480\tx5040\tx5600\tx6160\tx6720\pardirnatural\partightenfactor0

\f1\fs22 \cf2 \cb3 \CocoaLigature0 time hadoop jar /opt/cloudera/parcels/CDH-5.9.1-1.cdh5.9.1.p0.4/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -D mapreduce.job.maps=8 -D dfs.blocksize=16000000 65536000 /user/neymar/tgen640
\f0\fs24 \cf0 \cb1 \CocoaLigature1 \
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 \
\
\
Job Output\
\pard\tx560\tx1120\tx1680\tx2240\tx2800\tx3360\tx3920\tx4480\tx5040\tx5600\tx6160\tx6720\pardirnatural\partightenfactor0

\f1\fs22 \cf2 \cb3 \CocoaLigature0 [neymar@cluster1node2 cloudera-scm-server]$ time hadoop jar /opt/cloudera/parcels/CDH-5.9.1-1.cdh5.9.1.p0.4/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -D mapreduce.job.maps=8 -D dfs.blocksize=16000000 65536000 /user/neymar/tgen640\
17/04/14 13:45:17 INFO Configuration.deprecation: session.id is deprecated. Instead, use dfs.metrics.session-id\
17/04/14 13:45:17 INFO jvm.JvmMetrics: Initializing JVM Metrics with processName=JobTracker, sessionId=\
17/04/14 13:45:17 INFO terasort.TeraSort: Generating 65536000 using 1\
17/04/14 13:45:17 INFO mapreduce.JobSubmitter: number of splits:1\
17/04/14 13:45:17 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_local1625289168_0001\
17/04/14 13:45:18 INFO mapreduce.Job: The url to track the job: http://localhost:8080/\
17/04/14 13:45:18 INFO mapreduce.Job: Running job: job_local1625289168_0001\
17/04/14 13:45:18 INFO mapred.LocalJobRunner: OutputCommitter set in config null\
17/04/14 13:45:18 INFO output.FileOutputCommitter: File Output Committer Algorithm version is 1\
17/04/14 13:45:18 INFO mapred.LocalJobRunner: OutputCommitter is org.apache.hadoop.mapreduce.lib.output.FileOutputCommitter\
17/04/14 13:45:18 INFO mapred.LocalJobRunner: Waiting for map tasks\
17/04/14 13:45:18 INFO mapred.LocalJobRunner: Starting task: attempt_local1625289168_0001_m_000000_0\
17/04/14 13:45:18 INFO output.FileOutputCommitter: File Output Committer Algorithm version is 1\
17/04/14 13:45:18 INFO mapred.Task:  Using ResourceCalculatorProcessTree : [ ]\
17/04/14 13:45:18 INFO mapred.MapTask: Processing split: org.apache.hadoop.examples.terasort.TeraGen$RangeInputFormat$RangeInputSplit@4c4d2a8\
17/04/14 13:45:19 INFO mapreduce.Job: Job job_local1625289168_0001 running in uber mode : false\
17/04/14 13:45:19 INFO mapreduce.Job:  map 0% reduce 0%\
17/04/14 13:45:24 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:45:25 INFO mapreduce.Job:  map 4% reduce 0%\
17/04/14 13:45:27 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:45:28 INFO mapreduce.Job:  map 6% reduce 0%\
17/04/14 13:45:30 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:45:31 INFO mapreduce.Job:  map 8% reduce 0%\
17/04/14 13:45:33 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:45:34 INFO mapreduce.Job:  map 10% reduce 0%\
17/04/14 13:45:36 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:45:37 INFO mapreduce.Job:  map 13% reduce 0%\
17/04/14 13:45:39 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:45:40 INFO mapreduce.Job:  map 15% reduce 0%\
17/04/14 13:45:42 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:45:43 INFO mapreduce.Job:  map 17% reduce 0%\
17/04/14 13:45:45 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:45:46 INFO mapreduce.Job:  map 19% reduce 0%\
17/04/14 13:45:48 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:45:49 INFO mapreduce.Job:  map 21% reduce 0%\
17/04/14 13:45:51 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:45:52 INFO mapreduce.Job:  map 23% reduce 0%\
17/04/14 13:45:54 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:45:55 INFO mapreduce.Job:  map 26% reduce 0%\
17/04/14 13:45:57 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:45:58 INFO mapreduce.Job:  map 28% reduce 0%\
17/04/14 13:46:00 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:01 INFO mapreduce.Job:  map 30% reduce 0%\
17/04/14 13:46:03 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:06 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:09 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:09 INFO mapreduce.Job:  map 31% reduce 0%\
17/04/14 13:46:12 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:12 INFO mapreduce.Job:  map 33% reduce 0%\
17/04/14 13:46:15 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:15 INFO mapreduce.Job:  map 36% reduce 0%\
17/04/14 13:46:18 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:18 INFO mapreduce.Job:  map 38% reduce 0%\
17/04/14 13:46:21 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:21 INFO mapreduce.Job:  map 40% reduce 0%\
17/04/14 13:46:24 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:24 INFO mapreduce.Job:  map 42% reduce 0%\
17/04/14 13:46:27 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:27 INFO mapreduce.Job:  map 45% reduce 0%\
17/04/14 13:46:30 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:30 INFO mapreduce.Job:  map 47% reduce 0%\
17/04/14 13:46:33 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:33 INFO mapreduce.Job:  map 50% reduce 0%\
17/04/14 13:46:36 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:36 INFO mapreduce.Job:  map 52% reduce 0%\
17/04/14 13:46:39 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:39 INFO mapreduce.Job:  map 54% reduce 0%\
17/04/14 13:46:42 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:42 INFO mapreduce.Job:  map 56% reduce 0%\
17/04/14 13:46:45 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:45 INFO mapreduce.Job:  map 58% reduce 0%\
17/04/14 13:46:48 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:48 INFO mapreduce.Job:  map 61% reduce 0%\
17/04/14 13:46:51 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:51 INFO mapreduce.Job:  map 63% reduce 0%\
17/04/14 13:46:54 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:54 INFO mapreduce.Job:  map 65% reduce 0%\
17/04/14 13:46:57 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:46:57 INFO mapreduce.Job:  map 68% reduce 0%\
17/04/14 13:47:00 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:00 INFO mapreduce.Job:  map 70% reduce 0%\
17/04/14 13:47:03 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:09 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:12 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:12 INFO mapreduce.Job:  map 72% reduce 0%\
17/04/14 13:47:15 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:15 INFO mapreduce.Job:  map 74% reduce 0%\
17/04/14 13:47:18 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:18 INFO mapreduce.Job:  map 76% reduce 0%\
17/04/14 13:47:21 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:21 INFO mapreduce.Job:  map 78% reduce 0%\
17/04/14 13:47:24 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:24 INFO mapreduce.Job:  map 81% reduce 0%\
17/04/14 13:47:27 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:27 INFO mapreduce.Job:  map 83% reduce 0%\
17/04/14 13:47:30 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:30 INFO mapreduce.Job:  map 85% reduce 0%\
17/04/14 13:47:33 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:33 INFO mapreduce.Job:  map 87% reduce 0%\
17/04/14 13:47:36 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:36 INFO mapreduce.Job:  map 89% reduce 0%\
17/04/14 13:47:39 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:39 INFO mapreduce.Job:  map 91% reduce 0%\
17/04/14 13:47:42 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:42 INFO mapreduce.Job:  map 93% reduce 0%\
17/04/14 13:47:45 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:45 INFO mapreduce.Job:  map 95% reduce 0%\
17/04/14 13:47:48 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:48 INFO mapreduce.Job:  map 97% reduce 0%\
17/04/14 13:47:51 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:51 INFO mapreduce.Job:  map 99% reduce 0%\
17/04/14 13:47:53 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:53 INFO mapred.Task: Task:attempt_local1625289168_0001_m_000000_0 is done. And is in the process of committing\
17/04/14 13:47:53 INFO mapred.LocalJobRunner: map > map\
17/04/14 13:47:53 INFO mapred.Task: Task attempt_local1625289168_0001_m_000000_0 is allowed to commit now\
17/04/14 13:47:53 INFO output.FileOutputCommitter: Saved output of task 'attempt_local1625289168_0001_m_000000_0' to hdfs://cluster1node2.lab.local:8020/user/neymar/tgen640/_temporary/0/task_local1625289168_0001_m_000000\
17/04/14 13:47:53 INFO mapred.LocalJobRunner: map\
17/04/14 13:47:53 INFO mapred.Task: Task 'attempt_local1625289168_0001_m_000000_0' done.\
17/04/14 13:47:53 INFO mapred.LocalJobRunner: Finishing task: attempt_local1625289168_0001_m_000000_0\
17/04/14 13:47:53 INFO mapred.LocalJobRunner: map task executor complete.\
17/04/14 13:47:53 INFO mapreduce.Job:  map 100% reduce 0%\
17/04/14 13:47:53 INFO mapreduce.Job: Job job_local1625289168_0001 completed successfully\
17/04/14 13:47:53 INFO mapreduce.Job: Counters: 21\
	File System Counters\
		FILE: Number of bytes read=276327\
		FILE: Number of bytes written=566725\
		FILE: Number of read operations=0\
		FILE: Number of large read operations=0\
		FILE: Number of write operations=0\
		HDFS: Number of bytes read=0\
		HDFS: Number of bytes written=6553600000\
		HDFS: Number of read operations=4\
		HDFS: Number of large read operations=0\
		HDFS: Number of write operations=3\
	Map-Reduce Framework\
		Map input records=65536000\
		Map output records=65536000\
		Input split bytes=83\
		Spilled Records=0\
		Failed Shuffles=0\
		Merged Map outputs=0\
		GC time elapsed (ms)=1447\
		Total committed heap usage (bytes)=249036800\
	org.apache.hadoop.examples.terasort.TeraGen$Counters\
		CHECKSUM=140750829423462787\
	File Input Format Counters \
		Bytes Read=0\
	File Output Format Counters \
		Bytes Written=6553600000\
\
real	2m40.974s\
user	2m0.598s\
sys	0m9.857s\
[neymar@cluster1node2 cloudera-scm-server]$ \
\
\
\
\
Time command Output\
real	2m40.974s\
user	2m0.598s\
sys	0m9.857s\
\
\
tgen640 Directory Output \
[neymar@cluster1node2 cloudera-scm-server]$ hdfs dfs -ls /user/neymar/tgen640\
Found 2 items\
-rw-r--r--   3 neymar supergroup          0 2017-04-14 13:47 /user/neymar/tgen640/_SUCCESS\
-rw-r--r--   3 neymar supergroup 6553600000 2017-04-14 13:47 /user/neymar/tgen640/part-m-00000\
[neymar@cluster1node2 cloudera-scm-server]$ \
\
\
Blocks of the Directory Output \
[neymar@cluster1node2 cloudera-scm-server]$ hdfs fsck /user/neymar/tgen640\
Connecting to namenode via http://cluster1node2.lab.local:50070\
FSCK started by neymar (auth:SIMPLE) from /192.168.100.162 for path /user/neymar/tgen640 at Fri Apr 14 13:50:36 BRT 2017\
..Status: HEALTHY\
 Total size:	6553600000 B\
 Total dirs:	1\
 Total files:	2\
 Total symlinks:		0\
 Total blocks (validated):	410 (avg. block size 15984390 B)\
 Minimally replicated blocks:	410 (100.0 %)\
 Over-replicated blocks:	0 (0.0 %)\
 Under-replicated blocks:	0 (0.0 %)\
 Mis-replicated blocks:		0 (0.0 %)\
 Default replication factor:	3\
 Average block replication:	3.0\
 Corrupt blocks:		0\
 Missing replicas:		0 (0.0 %)\
 Number of data-nodes:		4\
 Number of racks:		1\
FSCK ended at Fri Apr 14 13:50:36 BRT 2017 in 34 milliseconds\
\
\
The filesystem under path '/user/neymar/tgen640' is HEALTHY\
[neymar@cluster1node2 cloudera-scm-server]$ }