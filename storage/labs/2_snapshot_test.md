[root@cluster1node1 tmp]# sudo -u hdfs hdfs dfs -mkdir /user/evertonlf/precious


[root@cluster1node1 tmp]# sudo -u hdfs hdfs dfs -ls /user/evertonlf/precious
Found 1 items
-rw-r--r--   3 hdfs evertonlf     473950 2017-04-04 21:01 /user/evertonlf/precious/SEBC-master.zip
[root@cluster1node1 tmp]#


[root@cluster1node1 tmp]# sudo -u hdfs hdfs dfsadmin -allowSnapshot /user/evertonlf/precious
Allowing snaphot on /user/evertonlf/precious succeeded
[root@cluster1node1 tmp]#


[root@cluster1node1 tmp]# sudo -u hdfs hdfs dfs -createSnapshot /user/evertonlf/precious sebc-hdfs-test
Created snapshot /user/evertonlf/precious/.snapshot/sebc-hdfs-test
[root@cluster1node1 tmp]#


[root@cluster1node1 tmp]# sudo -u hdfs hdfs dfs -ls /user/evertonlf/precious
Found 1 items
-rw-r--r--   3 hdfs evertonlf     473950 2017-04-04 21:01 /user/evertonlf/precious/SEBC-master.zip
[root@cluster1node1 tmp]#



[root@cluster1node1 tmp]# sudo -u hdfs hdfs dfs -rm /user/evertonlf/precious/SEBC-master.zip
17/04/04 23:34:02 INFO fs.TrashPolicyDefault: Moved: 'hdfs://nameservice1/user/evertonlf/precious/SEBC-master.zip' to trash at: hdfs://nameservice1/user/hdfs/.Trash/Current/user/evertonlf/precious/SEBC-master.zip
[root@cluster1node1 tmp]#


[root@cluster1node1 tmp]# sudo -u hdfs hdfs dfs -ls /user/evertonlf/precious
[root@cluster1node1 tmp]#



[root@cluster1node1 tmp]# sudo -u hdfs hdfs dfs -ls /user/evertonlf/precious/.snapshot/sebc-hdfs-test
Found 1 items
-rw-r--r--   3 hdfs evertonlf     473950 2017-04-04 21:01 /user/evertonlf/precious/.snapshot/sebc-hdfs-test/SEBC-master.zip
[root@cluster1node1 tmp]#



[root@cluster1node1 tmp]# sudo -u hdfs hdfs dfs -cp /user/evertonlf/precious/.snapshot/sebc-hdfs-test/SEBC-master.zip /user/evertonlf/precious
[root@cluster1node1 tmp]#



[root@cluster1node1 tmp]# sudo -u hdfs hdfs dfs -ls /user/evertonlf/precious
Found 1 items
-rw-r--r--   3 hdfs evertonlf     473950 2017-04-04 23:39 /user/evertonlf/precious/SEBC-master.zip
[root@cluster1node1 tmp]#








