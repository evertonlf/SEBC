{\rtf1\ansi\ansicpg1252\cocoartf1504\cocoasubrtf820
{\fonttbl\f0\fnil\fcharset0 Menlo-Regular;\f1\fnil\fcharset0 Menlo-Bold;}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;\red255\green255\blue255;}
{\*\expandedcolortbl;;\csgray\c0;\csgray\c100000;}
\paperw11900\paperh16840\margl1440\margr1440\vieww22920\viewh9620\viewkind0
\pard\tx560\tx1120\tx1680\tx2240\tx2800\tx3360\tx3920\tx4480\tx5040\tx5600\tx6160\tx6720\pardirnatural\partightenfactor0

\f0\fs22 \cf2 \cb3 \CocoaLigature0 Hostname Database\
[root@cluster1node1 java]# cat /etc/hostname\
cluster1node1.lab.local\
[root@cluster1node1 java]# \
\
\
\
MariaDB Version\
[root@cluster1node1 java]# mysql -V\
mysql  Ver 15.1 Distrib 5.5.52-MariaDB, for Linux (x86_64) using readline 5.1\
[root@cluster1node1 java]#\
\
\
List Databases\
MariaDB [(none)]> show databases;\
+--------------------+\
| Database           |\
+--------------------+\
| information_schema |\
| hive               |\
| hue                |\
| mysql              |\
| oozie              |\
| performance_schema |\
| rman               |\
| sentry             |\
+--------------------+\
\pard\tx560\tx1120\tx1680\tx2240\tx2800\tx3360\tx3920\tx4480\tx5040\tx5600\tx6160\tx6720\pardirnatural\partightenfactor0

\f1\b \cf2 \cb3 8 rows in set (0.00 sec)
\f0\b0 \cf2 \cb3 \
\
MariaDB [(none)]> }