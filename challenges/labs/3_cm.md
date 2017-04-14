{\rtf1\ansi\ansicpg1252\cocoartf1504\cocoasubrtf820
{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\fnil\fcharset0 Menlo-Regular;}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;\red255\green255\blue255;}
{\*\expandedcolortbl;;\csgray\c0;\csgray\c100000;}
\paperw11900\paperh16840\margl1440\margr1440\vieww10800\viewh8400\viewkind0
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0\fs24 \cf0 Output Users\
\pard\tx560\tx1120\tx1680\tx2240\tx2800\tx3360\tx3920\tx4480\tx5040\tx5600\tx6160\tx6720\pardirnatural\partightenfactor0

\f1\fs22 \cf2 \cb3 \CocoaLigature0 [root@cluster1node2 cloudera-scm-server]# sudo -u hdfs hdfs dfs -ls /user\
Found 7 items\
drwx------   - hdfs    supergroup          0 2017-04-14 13:32 /user/hdfs\
drwxrwxrwx   - mapred  hadoop              0 2017-04-14 13:24 /user/history\
drwxrwxr-t   - hive    hive                0 2017-04-14 13:25 /user/hive\
drwxrwxr-x   - hue     hue                 0 2017-04-14 13:25 /user/hue\
drwxr-xr-x   - neymar  supergroup          0 2017-04-14 13:30 /user/neymar\
drwxrwxr-x   - oozie   oozie               0 2017-04-14 13:26 /user/oozie\
drwxr-xr-x   - ronaldo supergroup          0 2017-04-14 13:31 /user/ronaldo\
[root@cluster1node2 cloudera-scm-server]# \
\
\
Output curl\
[root@cluster1node2 cloudera-scm-server]# curl -u admin:admin http://localhost:7180/api/v14/hosts\
\{\
  "items" : [ \{\
    "hostId" : "a6a3d370-8bcc-43b1-a154-a9f9cf4a0bb5",\
    "ipAddress" : "192.168.100.161",\
    "hostname" : "cluster1node1.lab.local",\
    "rackId" : "/default",\
    "hostUrl" : "http://cluster1node2.lab.local:7180/cmf/hostRedirect/a6a3d370-8bcc-43b1-a154-a9f9cf4a0bb5",\
    "maintenanceMode" : false,\
    "maintenanceOwners" : [ ],\
    "commissionState" : "COMMISSIONED",\
    "numCores" : 2,\
    "numPhysicalCores" : 2,\
    "totalPhysMemBytes" : 16659066880\
  \}, \{\
    "hostId" : "8df46f13-8a01-441b-8583-a592242331fc",\
    "ipAddress" : "192.168.100.162",\
    "hostname" : "cluster1node2.lab.local",\
    "rackId" : "/default",\
    "hostUrl" : "http://cluster1node2.lab.local:7180/cmf/hostRedirect/8df46f13-8a01-441b-8583-a592242331fc",\
    "maintenanceMode" : false,\
    "maintenanceOwners" : [ ],\
    "commissionState" : "COMMISSIONED",\
    "numCores" : 2,\
    "numPhysicalCores" : 2,\
    "totalPhysMemBytes" : 16659066880\
  \}, \{\
    "hostId" : "05d6ebd8-2051-43b1-8886-520cbf9a3e7d",\
    "ipAddress" : "192.168.100.163",\
    "hostname" : "cluster1node3.lab.local",\
    "rackId" : "/default",\
    "hostUrl" : "http://cluster1node2.lab.local:7180/cmf/hostRedirect/05d6ebd8-2051-43b1-8886-520cbf9a3e7d",\
    "maintenanceMode" : false,\
    "maintenanceOwners" : [ ],\
    "commissionState" : "COMMISSIONED",\
    "numCores" : 2,\
    "numPhysicalCores" : 2,\
    "totalPhysMemBytes" : 16659066880\
  \}, \{\
    "hostId" : "dfc83895-c320-4e61-a74c-6d6d526836fb",\
    "ipAddress" : "192.168.100.164",\
    "hostname" : "cluster1node4.lab.local",\
    "rackId" : "/default",\
    "hostUrl" : "http://cluster1node2.lab.local:7180/cmf/hostRedirect/dfc83895-c320-4e61-a74c-6d6d526836fb",\
    "maintenanceMode" : false,\
    "maintenanceOwners" : [ ],\
    "commissionState" : "COMMISSIONED",\
    "numCores" : 2,\
    "numPhysicalCores" : 2,\
    "totalPhysMemBytes" : 16659066880\
  \}, \{\
    "hostId" : "1fdd523e-fb7b-4d49-a985-183098e84e18",\
    "ipAddress" : "192.168.100.165",\
    "hostname" : "cluster1node5.lab.local",\
    "rackId" : "/default",\
    "hostUrl" : "http://cluster1node2.lab.local:7180/cmf/hostRedirect/1fdd523e-fb7b-4d49-a985-183098e84e18",\
    "maintenanceMode" : false,\
    "maintenanceOwners" : [ ],\
    "commissionState" : "COMMISSIONED",\
    "numCores" : 2,\
    "numPhysicalCores" : 2,\
    "totalPhysMemBytes" : 16659066880\
  \} ]\
\}[root@cluster1node2 cloudera-scm-server]# }