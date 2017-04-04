
Change vm.swappiness=1 in all hosts

nano /usr/lib/tuned/virtual-guest/tuned.conf 

vm.swappiness=1




Show volumes

[root@cluster1node1 /]# clear
[root@cluster1node1 /]# df -h
Filesystem               Size  Used Avail Use% Mounted on
/dev/mapper/centos-root   36G  2.7G   33G   8% /
devtmpfs                 7.8G     0  7.8G   0% /dev
tmpfs                    7.8G     0  7.8G   0% /dev/shm
tmpfs                    7.8G  8.5M  7.8G   1% /run
tmpfs                    7.8G     0  7.8G   0% /sys/fs/cgroup
/dev/sda1                497M  169M  329M  34% /boot
tmpfs                    1.6G     0  1.6G   0% /run/user/0
[root@cluster1node1 /]# fdisk -l

Disk /dev/sda: 42.9 GB, 42949672960 bytes, 83886080 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disk label type: dos
Disk identifier: 0x0005a7d3

   Device Boot      Start         End      Blocks   Id  System
/dev/sda1   *        2048     1026047      512000   83  Linux
/dev/sda2         1026048    83886079    41430016   8e  Linux LVM

Disk /dev/sdb: 42.9 GB, 42949672960 bytes, 83886080 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/mapper/centos-root: 38.1 GB, 38084280320 bytes, 74383360 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/mapper/centos-swap: 4294 MB, 4294967296 bytes, 8388608 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes

[root@cluster1node1 /]#




Disable Huge Pages in all hosts

create file 

nano /etc/init.d/disable-transparent-hugepages

copy parameters

#!/bin/bash
### BEGIN INIT INFO
# Provides:          disable-transparent-hugepages
# Required-Start:    $local_fs
# Required-Stop:
# X-Start-Before:    mongod mongodb-mms-automation-agent
# Default-Start:     2 3 4 5
# Default-Stop:      0 1 6
# Short-Description: Disable Linux transparent huge pages
# Description:       Disable Linux transparent huge pages, to improve
#                    database performance.
### END INIT INFO

case $1 in
  start)
    if [ -d /sys/kernel/mm/transparent_hugepage ]; then
      thp_path=/sys/kernel/mm/transparent_hugepage
    elif [ -d /sys/kernel/mm/redhat_transparent_hugepage ]; then
      thp_path=/sys/kernel/mm/redhat_transparent_hugepage
    else
      return 0
    fi

    echo 'never' > ${thp_path}/enabled
    echo 'never' > ${thp_path}/defrag

    re='^[0-1]+$'
    if [[ $(cat ${thp_path}/khugepaged/defrag) =~ $re ]]
    then
      # RHEL 7
      echo 0  > ${thp_path}/khugepaged/defrag
    else
      # RHEL 6
      echo 'no' > ${thp_path}/khugepaged/defrag
    fi

    unset re
    unset thp_path
    ;;
esac



Give permission

chmod 755 /etc/init.d/disable-transparent-hugepage



Put on boot
chkconfig --add disable-transparent-hugepages


New Profile to THP to never
mkdir /etc/tuned/no-thp

nano /etc/tuned/no-thp/tuned.conf

[main]
include=virtual-guest

[vm]
transparent_hugepages=never	




Test
cat /sys/kernel/mm/transparent_hugepage/enabled
cat /sys/kernel/mm/transparent_hugepage/defrag


always madvise [never]




List Network Interface

[root@cluster1node1 ~]# ifconfig
eno16777984: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.100.161  netmask 255.255.255.0  broadcast 192.168.100.255
        inet6 fe80::250:56ff:fe86:50f9  prefixlen 64  scopeid 0x20<link>
        ether 00:50:56:86:50:f9  txqueuelen 1000  (Ethernet)
        RX packets 1838  bytes 119097 (116.3 KiB)
        RX errors 0  dropped 48  overruns 0  frame 0
        TX packets 71  bytes 10722 (10.4 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1  (Local Loopback)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 0  bytes 0 (0.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

[root@cluster1node1 ~]#


getent Hosts

127.0.0.1   localhost
192.168.100.161 cluster1node1.lab.local cluster1node1
192.168.100.162 cluster1node2.lab.local cluster1node2
192.168.100.163 cluster1node3.lab.local cluster1node3
192.168.100.164 cluster1node4.lab.local cluster1node4
192.168.100.165 cluster1node5.lab.local cluster1node5


nscd status

[root@cluster1node1 /]# service nscd status
Redirecting to /bin/systemctl status  nscd.service
? nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-04-03 15:59:53 -03; 1min 33s ago
  Process: 2641 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 2642 (nscd)
   CGroup: /system.slice/nscd.service
           +-2642 /usr/sbin/nscd

Apr 03 15:59:53 cluster1node1.compwire.local nscd[2642]: 2642 monitoring directory...
Apr 03 15:59:53 cluster1node1.compwire.local nscd[2642]: 2642 monitoring file `/et...
Apr 03 15:59:53 cluster1node1.compwire.local nscd[2642]: 2642 monitoring directory...
Apr 03 15:59:53 cluster1node1.compwire.local nscd[2642]: 2642 monitoring file `/et...
Apr 03 15:59:53 cluster1node1.compwire.local nscd[2642]: 2642 monitoring directory...
Apr 03 15:59:53 cluster1node1.compwire.local nscd[2642]: 2642 disabled inotify-bas...
Apr 03 15:59:53 cluster1node1.compwire.local nscd[2642]: 2642 stat failed for file...
Apr 03 15:59:53 cluster1node1.compwire.local nscd[2642]: 2642 Access Vector Cache ...
Apr 03 15:59:53 cluster1node1.compwire.local systemd[1]: Started Name Service Cach...
Apr 03 16:00:12 cluster1node1.compwire.local nscd[2642]: 2642 checking for monitor...
Hint: Some lines were ellipsized, use -l to show in full.




ntpd status

[root@cluster1node1 /]# service ntpd status
Redirecting to /bin/systemctl status  ntpd.service
? ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-04-03 16:10:14 -03; 3s ago
  Process: 2839 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 2840 (ntpd)
   CGroup: /system.slice/ntpd.service
           +-2840 /usr/sbin/ntpd -u ntp:ntp -g

Apr 03 16:10:14 cluster1node1.compwire.local ntpd[2840]: Listen and drop on 1 v6wi...
Apr 03 16:10:14 cluster1node1.compwire.local ntpd[2840]: Listen normally on 2 lo 1...
Apr 03 16:10:14 cluster1node1.compwire.local ntpd[2840]: Listen normally on 3 eno1...
Apr 03 16:10:14 cluster1node1.compwire.local ntpd[2840]: Listen normally on 4 lo :...
Apr 03 16:10:14 cluster1node1.compwire.local systemd[1]: Started Network Time Serv...
Apr 03 16:10:14 cluster1node1.compwire.local ntpd[2840]: Listen normally on 5 eno1...
Apr 03 16:10:14 cluster1node1.compwire.local ntpd[2840]: Listening on routing sock...
Apr 03 16:10:14 cluster1node1.compwire.local ntpd[2840]: 0.0.0.0 c016 06 restart
Apr 03 16:10:14 cluster1node1.compwire.local ntpd[2840]: 0.0.0.0 c012 02 freq_set ...
Apr 03 16:10:14 cluster1node1.compwire.local ntpd[2840]: 0.0.0.0 c011 01 freq_not_set
Hint: Some lines were ellipsized, use -l to show in full.
[root@cluster1node1 /]#



Install MariaDB


yum install mariadb-server


Check if Service is stop

service mariadb stop


Configure my.cnf


[mysqld]
transaction-isolation = READ-COMMITTED
# Disabling symbolic-links is recommended to prevent assorted security risks;
# to do so, uncomment this line:
# symbolic-links = 0

key_buffer = 16M
key_buffer_size = 32M
max_allowed_packet = 32M
thread_stack = 256K
thread_cache_size = 64
query_cache_limit = 8M
query_cache_size = 64M
query_cache_type = 1

max_connections = 550
#expire_logs_days = 10
#max_binlog_size = 100M

#log_bin should be on a disk with enough free space. Replace '/var/lib/mysql/mysql_b$
#and chown the specified folder to the mysql user.
log_bin=/var/lib/mysql/mysql_binary_log

binlog_format = mixed

read_buffer_size = 2M
read_rnd_buffer_size = 16M
sort_buffer_size = 8M
join_buffer_size = 8M

# InnoDB settings
innodb_file_per_table = 1
innodb_flush_log_at_trx_commit  = 2
innodb_log_buffer_size = 64M
innodb_buffer_pool_size = 4G
innodb_thread_concurrency = 8
innodb_flush_method = O_DIRECT
innodb_log_file_size = 512M

[mysqld_safe]
log-error=/var/log/mariadb/mariadb.log
pid-file=/var/run/mariadb/mariadb.pid


Put to Start MariaDB
systemctl enable mariadb.service


Start MariaDB
service mariadb start

Setup MariaDB

[root@cluster1node2 /]# /usr/bin/mysql_secure_installation

NOTE: RUNNING ALL PARTS OF THIS SCRIPT IS RECOMMENDED FOR ALL MariaDB
      SERVERS IN PRODUCTION USE!  PLEASE READ EACH STEP CAREFULLY!

In order to log into MariaDB to secure it, we'll need the current
password for the root user.  If you've just installed MariaDB, and
you haven't set the root password yet, the password will be blank,
so you should just press enter here.

Enter current password for root (enter for none):
OK, successfully used password, moving on...

Setting the root password ensures that nobody can log into the MariaDB
root user without the proper authorisation.

Set root password? [Y/n] y
New password:
Re-enter new password:
Password updated successfully!
Reloading privilege tables..
 ... Success!


By default, a MariaDB installation has an anonymous user, allowing anyone
to log into MariaDB without having to have a user account created for
them.  This is intended only for testing, and to make the installation
go a bit smoother.  You should remove them before moving into a
production environment.

Remove anonymous users? [Y/n] y
 ... Success!

Normally, root should only be allowed to connect from 'localhost'.  This
ensures that someone cannot guess at the root password from the network.

Disallow root login remotely? [Y/n] n
 ... skipping.

By default, MariaDB comes with a database named 'test' that anyone can
access.  This is also intended only for testing, and should be removed
before moving into a production environment.

Remove test database and access to it? [Y/n] y
 - Dropping test database...
 ... Success!
 - Removing privileges on test database...
 ... Success!

Reloading the privilege tables will ensure that all changes made so far
will take effect immediately.

Reload privilege tables now? [Y/n] y
 ... Success!

Cleaning up...

All done!  If you've completed all of the above steps, your MariaDB
installation should now be secure.

Thanks for using MariaDB!
[root@cluster1node2 /]#
[root@cluster1node2 /]#


Create Directory to Java conector
[root@cluster1node2 /]# mkdir -p /usr/share/java/



Extract file of the Java conector
tar zxvf mysql-connector-java-5.1.41.tar.gz



Copy the *.jar conector to directory 
/usr/share/java/mysql-connector-java.jar



Configuring High Availability in MAriaDB

Put this parameter int my.cnf on Master

[mariadb]
log-bin
server_id=1
log-basename=master1

Configure User 
MariaDB [(none)]> GRANT REPLICATION SLAVE ON *.* TO root@cluster1node2.lab.local identified by 'password';




Put this parameter int my.cnf on Slave

[mariadb]
log-bin
server_id=2
log-basename=master1



On Master Flush Databses

MariaDB [(none)]> FLUSH TABLES WITH READ LOCK
  
Query OK, 0 rows affected (0.00 sec)


Optional
FLUSH LOCAL HOSTS, QUERY CACHE, TABLE_STATISTICS, INDEX_STATISTICS, USER_STATISTICS;



MariaDB [(none)]> show master status;
+--------------------+----------+--------------+------------------+
| File               | Position | Binlog_Do_DB | Binlog_Ignore_DB |
+--------------------+----------+--------------+------------------+
| master1-bin.000008 |     2246 |              |                  |
+--------------------+----------+--------------+------------------+
1 row in set (0.01 sec)

MariaDB [(none)]>



On Slave


Stop Slave

CHANGE MASTER TO
  MASTER_HOST='cluster1node1.lab.local',
  MASTER_USER='root',
  MASTER_PASSWORD='password',
  MASTER_PORT=3306,
  MASTER_LOG_FILE='master1-bin.000008',
  MASTER_LOG_POS=407,
  MASTER_CONNECT_RETRY=10;


Start Slave

show slave status \G;



MariaDB [(none)]> show slave status \G;
*************************** 1. row ***************************
               Slave_IO_State: Waiting for master to send event
                  Master_Host: cluster1node1.lab.local
                  Master_User: root
                  Master_Port: 3306
                Connect_Retry: 10
              Master_Log_File: master1-bin.000011
          Read_Master_Log_Pos: 24025103
               Relay_Log_File: mariadb-relay-bin.000012
                Relay_Log_Pos: 24025389
        Relay_Master_Log_File: master1-bin.000011
             Slave_IO_Running: Yes
            Slave_SQL_Running: Yes
              Replicate_Do_DB:
          Replicate_Ignore_DB:
           Replicate_Do_Table:
       Replicate_Ignore_Table:
      Replicate_Wild_Do_Table:
  Replicate_Wild_Ignore_Table:
                   Last_Errno: 0
                   Last_Error:
                 Skip_Counter: 0
          Exec_Master_Log_Pos: 24025103
              Relay_Log_Space: 24025971
              Until_Condition: None
               Until_Log_File:
                Until_Log_Pos: 0
           Master_SSL_Allowed: No
           Master_SSL_CA_File:
           Master_SSL_CA_Path:
              Master_SSL_Cert:
            Master_SSL_Cipher:
               Master_SSL_Key:
        Seconds_Behind_Master: 0
Master_SSL_Verify_Server_Cert: No
                Last_IO_Errno: 0
                Last_IO_Error:
               Last_SQL_Errno: 0
               Last_SQL_Error:
  Replicate_Ignore_Server_Ids:
             Master_Server_Id: 1
1 row in set (0.00 sec)

ERROR: No query specified

MariaDB [(none)]>


Show databases;


Create databases for Activity Monitor, Reports Manager, Hive Metastore Server, Sentry Server, Cloudera Navigator Audit Server, and Cloudera Navigator Metadata Server

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> create database amon DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> create database rman DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> create database metastore DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> create database sentry DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> create database nav DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> create database navms DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> grant all on amon.* TO 'user'@'%' IDENTIFIED BY 'amon_password';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> grant all on rman.* TO 'user'@'%' IDENTIFIED BY 'rman_password';
Query OK, 0 rows affected (0.01 sec)

MariaDB [(none)]> grant all on metastore.* TO 'user'@'%' IDENTIFIED BY 'hive_password';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> grant all on sentry.* TO 'user'@'%' IDENTIFIED BY 'sentry_password';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> grant all on nav.* TO 'user'@'%' IDENTIFIED BY 'nav_password';     Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> grant all on navms.* TO 'user'@'%' IDENTIFIED BY 'navms_password';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]>


Create database for oozie

MariaDB [(none)]> create database oozie;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> grant all privileges on oozie.* to 'oozie'@'localhost' identified by 'oozie';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]>
MariaDB [(none)]>
MariaDB [(none)]> grant all privileges on oozie.* to 'oozie'@'%' identified by 'oozie';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]>



Install Cloudera Manager

Configuring repos

[root@cluster1node1 ~]# nano cloudera-manager.repo
[root@cluster1node1 ~]#
[root@cluster1node1 ~]#
[root@cluster1node1 ~]#
[root@cluster1node1 ~]#
[root@cluster1node1 ~]# cat cloudera-manager.repo
[cloudera-manager]
# Packages for Cloudera Manager, Version 5, on RedHat or CentOS 7 x86_64             
name=Cloudera Manager
baseurl=https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/5/
gpgkey =https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/RPM-GPG-KEY-cloudera
gpgcheck = 1
[root@cluster1node1 ~]#
[root@cluster1node1 ~]#
[root@cluster1node1 ~]#
[root@cluster1node1 ~]# mv cloudera-manager.repo /etc/yum.repos.d/



Installing Oracle JDK


[root@cluster1node1 ~]# yum install oracle-j2sdk1.7
Loaded plugins: fastestmirror
cloudera-manager                                              |  951 B  00:00:00
cloudera-manager/primary                                      | 4.3 kB  00:00:00
Loading mirror speeds from cached hostfile
 * base: mirror.globo.com
 * extras: mirror.globo.com
 * updates: mirror.globo.com
cloudera-manager                                                                 7/7
Resolving Dependencies
--> Running transaction check
---> Package oracle-j2sdk1.7.x86_64 0:1.7.0+update67-1 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

=====================================================================================
 Package              Arch        Version                Repository             Size
=====================================================================================
Installing:
 oracle-j2sdk1.7      x86_64      1.7.0+update67-1       cloudera-manager      135 M

Transaction Summary
=====================================================================================
Install  1 Package

Total download size: 135 M
Installed size: 279 M
Is this ok [y/d/N]:


Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
  Installing : oracle-j2sdk1.7-1.7.0+update67-1.x86_64                           1/1
  Verifying  : oracle-j2sdk1.7-1.7.0+update67-1.x86_64                           1/1

Installed:
  oracle-j2sdk1.7.x86_64 0:1.7.0+update67-1

Complete!
[root@cluster1node1 ~]#




Install Cloudera Manager


[root@cluster1node1 ~]# yum install cloudera-manager-daemons cloudera-manager-server
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: mirror.globo.com
 * extras: mirror.globo.com
 * updates: mirror.globo.com
Resolving Dependencies
--> Running transaction check
---> Package cloudera-manager-daemons.x86_64 0:5.10.1-1.cm5101.p0.6.el7 will be installed
---> Package cloudera-manager-server.x86_64 0:5.10.1-1.cm5101.p0.6.el7 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

=====================================================================================
 Package                   Arch    Version                   Repository         Size
=====================================================================================
Installing:
 cloudera-manager-daemons  x86_64  5.10.1-1.cm5101.p0.6.el7  cloudera-manager  571 M
 cloudera-manager-server   x86_64  5.10.1-1.cm5101.p0.6.el7  cloudera-manager  8.4 k

Transaction Summary
=====================================================================================
Install  2 Packages

Total download size: 571 M
Installed size: 734 M
Is this ok [y/d/N]: y
Downloading packages:
(1/2): cloudera-manager-server-5.10.1-1.cm5101.p0.6.el7.x86_6 | 8.4 kB  00:00:05
(2/2): cloudera-manager-daemons-5.10.1-1.cm5101.p0.6.el7.x86_ | 571 MB  00:00:54
-------------------------------------------------------------------------------------
Total                                                    11 MB/s | 571 MB  00:54
Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
  Installing : cloudera-manager-daemons-5.10.1-1.cm5101.p0.6.el7.x86_64          1/2
  Installing : cloudera-manager-server-5.10.1-1.cm5101.p0.6.el7.x86_64           2/2
  Verifying  : cloudera-manager-daemons-5.10.1-1.cm5101.p0.6.el7.x86_64          1/2
  Verifying  : cloudera-manager-server-5.10.1-1.cm5101.p0.6.el7.x86_64           2/2

Installed:
  cloudera-manager-daemons.x86_64 0:5.10.1-1.cm5101.p0.6.el7
  cloudera-manager-server.x86_64 0:5.10.1-1.cm5101.p0.6.el7

Complete!
[root@cluster1node1 ~]#



Setup Cloudera Database


[root@cluster1node1 cdh5.10.1]# /usr/share/cmf/schema/scm_prepare_database.sh \mysql -h localhost -uroot -p \--scm-host localhost scm scm scm
Enter database password:
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Successfully connected to database.
All done, your SCM database is configured correctly!
[root@cluster1node1 cdh5.10.1]#
[root@cluster1node1 cdh5.10.1]#



Start Cloudera Manager Server

[root@cluster1node1 cdh5.10.1]# service cloudera-scm-server start
Starting cloudera-scm-server (via systemctl):              [  OK  ]
[root@cluster1node1 cdh5.10.1]#


















