{\rtf1\ansi\ansicpg1252\cocoartf1504\cocoasubrtf820
{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\fnil\fcharset0 Menlo-Regular;}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;\red255\green255\blue255;\red60\green95\blue255;
}
{\*\expandedcolortbl;;\csgray\c0;\csgray\c100000;\cssrgb\c29814\c47883\c100000;
}
\paperw11900\paperh16840\margl1440\margr1440\vieww19360\viewh5760\viewkind0
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0\fs24 \cf0 List Repos\
\pard\tx560\tx1120\tx1680\tx2240\tx2800\tx3360\tx3920\tx4480\tx5040\tx5600\tx6160\tx6720\pardirnatural\partightenfactor0

\f1\fs22 \cf2 \cb3 \CocoaLigature0 [root@cluster1node2 yum.repos.d]# ls -l\
total 32\
drwxr-xr-x  2 root root    6 Apr 11 18:39 \cf4 \cb3 bkp\cf2 \cb3 \
-rw-r--r--. 1 root root 1664 Nov 29 16:12 CentOS-Base.repo\
-rw-r--r--. 1 root root 1309 Nov 29 16:12 CentOS-CR.repo\
-rw-r--r--. 1 root root  649 Nov 29 16:12 CentOS-Debuginfo.repo\
-rw-r--r--. 1 root root  314 Nov 29 16:12 CentOS-fasttrack.repo\
-rw-r--r--. 1 root root  630 Nov 29 16:12 CentOS-Media.repo\
-rw-r--r--. 1 root root 1331 Nov 29 16:12 CentOS-Sources.repo\
-rw-r--r--. 1 root root 2893 Nov 29 16:12 CentOS-Vault.repo\
-rw-r--r--  1 root root  275 Apr 14 12:24 cloudera-manager-repo\
[root@cluster1node2 yum.repos.d]# \
[root@cluster1node2 yum.repos.d]# \
\
\
[root@cluster1node2 yum.repos.d]# cat cloudera-manager.repo \
[cloudera-manager]\
# Packages for Cloudera Manager, Version 5, on RedHat or CentOS 7 x86_64           	  \
name=Cloudera Manager\
baseurl=https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/5.9.1\
gpgkey =https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/RPM-GPG-KEY-cloudera    \
gpgcheck = 1\
[root@cluster1node2 yum.repos.d]# 
\f0\fs24 \cf0 \cb1 \CocoaLigature1 \
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0
\cf0 \
\
Command scm_prepare_database.sh\
\pard\tx560\tx1120\tx1680\tx2240\tx2800\tx3360\tx3920\tx4480\tx5040\tx5600\tx6160\tx6720\pardirnatural\partightenfactor0

\f1\fs22 \cf2 \cb3 \CocoaLigature0 [root@cluster1node2 /]# /usr/share/cmf/schema/scm_prepare_database.sh \\mysql -h cluster1node1.lab.local -uroot -p \\--scm-host cluster1node2.lab.local scm scm scm\
Enter database password: \
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera\
Verifying that we can write to /etc/cloudera-scm-server\
Creating SCM configuration file in /etc/cloudera-scm-server\
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.\
[                          main] DbCommandExecutor              INFO  Successfully connected to database.\
All done, your SCM database is configured correctly!\
[root@cluster1node2 /]# 
\f0\fs24 \cf0 \cb1 \CocoaLigature1 \
}