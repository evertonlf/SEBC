[root@cluster1node1 /]# beeline
Beeline version 1.1.0-cdh5.10.1 by Apache Hive
beeline> !connect jdbc:hive2://192.168.100.162:10000/default;principal=hive/cluster1node2.lab.local@LAB.LOCAL
scan complete in 3ms
Connecting to jdbc:hive2://192.168.100.162:10000/default;principal=hive/cluster1node2.lab.local@LAB.LOCAL
Connected to: Apache Hive (version 1.1.0-cdh5.10.1)
Driver: Hive JDBC (version 1.1.0-cdh5.10.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://192.168.100.162:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20170408213232_3435aa3a-f3b6-42a5-9fe2-984b19f2477a): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170408213232_3435aa3a-f3b6-42a5-9fe2-984b19f2477a); Time taken: 0.116 seconds
INFO  : Executing command(queryId=hive_20170408213232_3435aa3a-f3b6-42a5-9fe2-984b19f2477a): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170408213232_3435aa3a-f3b6-42a5-9fe2-984b19f2477a); Time taken: 0.243 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (0.527 seconds)
0: jdbc:hive2://192.168.100.162:10000/default>



[root@cluster1node1 /]# kinit george@LAB.LOCAL
Password for george@LAB.LOCAL:
[root@cluster1node1 /]#
[root@cluster1node1 /]#
[root@cluster1node1 /]#
[root@cluster1node1 /]# beeline
Beeline version 1.1.0-cdh5.10.1 by Apache Hive
beeline> !connect jdbc:hive2://192.168.100.162:10000/default;principal=hive/cluster1node2.lab.local@LAB.LOCAL
scan complete in 4ms
Connecting to jdbc:hive2://192.168.100.162:10000/default;principal=hive/cluster1node2.lab.local@LAB.LOCAL
Connected to: Apache Hive (version 1.1.0-cdh5.10.1)
Driver: Hive JDBC (version 1.1.0-cdh5.10.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://192.168.100.162:10000/default>
0: jdbc:hive2://192.168.100.162:10000/default>
0: jdbc:hive2://192.168.100.162:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20170408215151_f82019b1-af3d-4998-b9b1-5e54b4b501a4): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170408215151_f82019b1-af3d-4998-b9b1-5e54b4b501a4); Time taken: 0.17 seconds
INFO  : Executing command(queryId=hive_20170408215151_f82019b1-af3d-4998-b9b1-5e54b4b501a4): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170408215151_f82019b1-af3d-4998-b9b1-5e54b4b501a4); Time taken: 0.383 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.877 seconds)
0: jdbc:hive2://192.168.100.162:10000/default>



[root@cluster1node1 /]# kinit ferdinand@LAB.LOCAL
Password for ferdinand@LAB.LOCAL:
[root@cluster1node1 /]#
[root@cluster1node1 /]#
[root@cluster1node1 /]#
[root@cluster1node1 /]# beeline
Beeline version 1.1.0-cdh5.10.1 by Apache Hive
beeline>
beeline>
beeline> !connect jdbc:hive2://192.168.100.162:10000/default;principal=hive/cluster1node2.lab.local@LAB.LOCAL
scan complete in 3ms
Connecting to jdbc:hive2://192.168.100.162:10000/default;principal=hive/cluster1node2.lab.local@LAB.LOCAL
Connected to: Apache Hive (version 1.1.0-cdh5.10.1)
Driver: Hive JDBC (version 1.1.0-cdh5.10.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://192.168.100.162:10000/default>
0: jdbc:hive2://192.168.100.162:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20170408215454_72724c6b-f822-42a3-ab82-e7838c4d497a): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170408215454_72724c6b-f822-42a3-ab82-e7838c4d497a); Time taken: 0.13 seconds
INFO  : Executing command(queryId=hive_20170408215454_72724c6b-f822-42a3-ab82-e7838c4d497a): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170408215454_72724c6b-f822-42a3-ab82-e7838c4d497a); Time taken: 0.241 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.556 seconds)
0: jdbc:hive2://192.168.100.162:10000/default>








