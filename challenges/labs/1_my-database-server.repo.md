{\rtf1\ansi\ansicpg1252\cocoartf1504\cocoasubrtf820
{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\fnil\fcharset0 Menlo-Regular;\f2\fnil\fcharset0 Menlo-Bold;
}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;\red255\green255\blue255;}
{\*\expandedcolortbl;;\csgray\c0;\csgray\c100000;}
\paperw11900\paperh16840\margl1440\margr1440\vieww10800\viewh8400\viewkind0
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0\fs24 \cf0 \
\
\
\
\pard\tx560\tx1120\tx1680\tx2240\tx2800\tx3360\tx3920\tx4480\tx5040\tx5600\tx6160\tx6720\pardirnatural\partightenfactor0

\f1\fs22 \cf2 \cb3 \CocoaLigature0 [root@cluster1node1 ~]# yum install mariadb-server\
Loaded plugins: fastestmirror\
base                                                                                                                                                                                                                                              | 3.6 kB  00:00:00     \
extras                                                                                                                                                                                                                                            | 3.4 kB  00:00:00     \
Loading mirror speeds from cached hostfile\
 * base: centos.xpg.com.br\
 * extras: centos.xpg.com.br\
 * updates: centos.xpg.com.br\
Resolving Dependencies\
There are unfinished transactions remaining. You might consider running yum-complete-transaction, or "yum-complete-transaction --cleanup-only" and "yum history redo last", first to finish them. If those don't work you'll have to try removing/installing packages by hand (maybe package-cleanup can help).\
The program 
\f2\b yum-complete-transaction
\f1\b0  is found in the yum-utils package.\
--> Running transaction check\
---> Package mariadb-server.x86_64 1:5.5.52-1.el7 will be installed\
--> Processing Dependency: mariadb(x86-64) = 1:5.5.52-1.el7 for package: 1:mariadb-server-5.5.52-1.el7.x86_64\
--> Processing Dependency: perl-DBI for package: 1:mariadb-server-5.5.52-1.el7.x86_64\
--> Processing Dependency: perl-DBD-MySQL for package: 1:mariadb-server-5.5.52-1.el7.x86_64\
--> Processing Dependency: perl(Data::Dumper) for package: 1:mariadb-server-5.5.52-1.el7.x86_64\
--> Processing Dependency: perl(DBI) for package: 1:mariadb-server-5.5.52-1.el7.x86_64\
--> Running transaction check\
---> Package mariadb.x86_64 1:5.5.52-1.el7 will be installed\
---> Package perl-DBD-MySQL.x86_64 0:4.023-5.el7 will be installed\
---> Package perl-DBI.x86_64 0:1.627-4.el7 will be installed\
--> Processing Dependency: perl(RPC::PlServer) >= 0.2001 for package: perl-DBI-1.627-4.el7.x86_64\
--> Processing Dependency: perl(RPC::PlClient) >= 0.2000 for package: perl-DBI-1.627-4.el7.x86_64\
---> Package perl-Data-Dumper.x86_64 0:2.145-3.el7 will be installed\
--> Running transaction check\
---> Package perl-PlRPC.noarch 0:0.2020-14.el7 will be installed\
--> Processing Dependency: perl(Net::Daemon) >= 0.13 for package: perl-PlRPC-0.2020-14.el7.noarch\
--> Processing Dependency: perl(Net::Daemon::Test) for package: perl-PlRPC-0.2020-14.el7.noarch\
--> Processing Dependency: perl(Net::Daemon::Log) for package: perl-PlRPC-0.2020-14.el7.noarch\
--> Processing Dependency: perl(Compress::Zlib) for package: perl-PlRPC-0.2020-14.el7.noarch\
--> Running transaction check\
---> Package perl-IO-Compress.noarch 0:2.061-2.el7 will be installed\
--> Processing Dependency: perl(Compress::Raw::Zlib) >= 2.061 for package: perl-IO-Compress-2.061-2.el7.noarch\
--> Processing Dependency: perl(Compress::Raw::Bzip2) >= 2.061 for package: perl-IO-Compress-2.061-2.el7.noarch\
---> Package perl-Net-Daemon.noarch 0:0.48-5.el7 will be installed\
--> Running transaction check\
---> Package perl-Compress-Raw-Bzip2.x86_64 0:2.061-3.el7 will be installed\
---> Package perl-Compress-Raw-Zlib.x86_64 1:2.061-4.el7 will be installed\
--> Finished Dependency Resolution\
\
Dependencies Resolved\
\
=========================================================================================================================================================================================================================================================================\
 Package                                                                    Arch                                                      Version                                                              Repository                                               Size\
=========================================================================================================================================================================================================================================================================\
Installing:\
 mariadb-server                                                             x86_64                                                    1:5.5.52-1.el7                                                       base                                                     11 M\
Installing for dependencies:\
 mariadb                                                                    x86_64                                                    1:5.5.52-1.el7                                                       base                                                    8.7 M\
 perl-Compress-Raw-Bzip2                                                    x86_64                                                    2.061-3.el7                                                          base                                                     32 k\
 perl-Compress-Raw-Zlib                                                     x86_64                                                    1:2.061-4.el7                                                        base                                                     57 k\
 perl-DBD-MySQL                                                             x86_64                                                    4.023-5.el7                                                          base                                                    140 k\
 perl-DBI                                                                   x86_64                                                    1.627-4.el7                                                          base                                                    802 k\
 perl-Data-Dumper                                                           x86_64                                                    2.145-3.el7                                                          base                                                     47 k\
 perl-IO-Compress                                                           noarch                                                    2.061-2.el7                                                          base                                                    260 k\
 perl-Net-Daemon                                                            noarch                                                    0.48-5.el7                                                           base                                                     51 k\
 perl-PlRPC                                                                 noarch                                                    0.2020-14.el7                                                        base                                                     36 k\
\
Transaction Summary\
=========================================================================================================================================================================================================================================================================\
Install  1 Package (+9 Dependent packages)\
\
Total download size: 21 M\
Installed size: 107 M\
Is this ok [y/d/N]: y\
Downloading packages:\
(1/10): mariadb-5.5.52-1.el7.x86_64.rpm                                                                                                                                                                                                           | 8.7 MB  00:00:01     \
(2/10): perl-Compress-Raw-Bzip2-2.061-3.el7.x86_64.rpm                                                                                                                                                                                            |  32 kB  00:00:00     \
(3/10): perl-Compress-Raw-Zlib-2.061-4.el7.x86_64.rpm                                                                                                                                                                                             |  57 kB  00:00:00     \
(4/10): perl-DBD-MySQL-4.023-5.el7.x86_64.rpm                                                                                                                                                                                                     | 140 kB  00:00:00     \
(5/10): perl-DBI-1.627-4.el7.x86_64.rpm                                                                                                                                                                                                           | 802 kB  00:00:00     \
(6/10): mariadb-server-5.5.52-1.el7.x86_64.rpm                                                                                                                                                                                                    |  11 MB  00:00:02     \
(7/10): perl-Data-Dumper-2.145-3.el7.x86_64.rpm                                                                                                                                                                                                   |  47 kB  00:00:00     \
(8/10): perl-Net-Daemon-0.48-5.el7.noarch.rpm                                                                                                                                                                                                     |  51 kB  00:00:00     \
(9/10): perl-IO-Compress-2.061-2.el7.noarch.rpm                                                                                                                                                                                                   | 260 kB  00:00:00     \
(10/10): perl-PlRPC-0.2020-14.el7.noarch.rpm                                                                                                                                                                                                      |  36 kB  00:00:00     \
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------\
Total                                                                                                                                                                                                                                    8.7 MB/s |  21 MB  00:00:02     \
Running transaction check\
Running transaction test\
Transaction test succeeded\
Running transaction\
  Installing : perl-Data-Dumper-2.145-3.el7.x86_64                                                                                                                                                                                                                  1/10 \
  Installing : perl-Net-Daemon-0.48-5.el7.noarch                                                                                                                                                                                                                    2/10 \
  Installing : 1:perl-Compress-Raw-Zlib-2.061-4.el7.x86_64                                                                                                                                                                                                          3/10 \
  Installing : 1:mariadb-5.5.52-1.el7.x86_64                                                                                                                                                                                                                        4/10 \
  Installing : perl-Compress-Raw-Bzip2-2.061-3.el7.x86_64                                                                                                                                                                                                           5/10 \
  Installing : perl-IO-Compress-2.061-2.el7.noarch                                                                                                                                                                                                                  6/10 \
  Installing : perl-PlRPC-0.2020-14.el7.noarch                                                                                                                                                                                                                      7/10 \
  Installing : perl-DBI-1.627-4.el7.x86_64                                                                                                                                                                                                                          8/10 \
  Installing : perl-DBD-MySQL-4.023-5.el7.x86_64                                                                                                                                                                                                                    9/10 \
  Installing : 1:mariadb-server-5.5.52-1.el7.x86_64                                                                                                                                                                                                                10/10 \
  Verifying  : perl-Compress-Raw-Bzip2-2.061-3.el7.x86_64                                                                                                                                                                                                           1/10 \
  Verifying  : 1:mariadb-5.5.52-1.el7.x86_64                                                                                                                                                                                                                        2/10 \
  Verifying  : perl-Data-Dumper-2.145-3.el7.x86_64                                                                                                                                                                                                                  3/10 \
  Verifying  : 1:mariadb-server-5.5.52-1.el7.x86_64                                                                                                                                                                                                                 4/10 \
  Verifying  : perl-PlRPC-0.2020-14.el7.noarch                                                                                                                                                                                                                      5/10 \
  Verifying  : 1:perl-Compress-Raw-Zlib-2.061-4.el7.x86_64                                                                                                                                                                                                          6/10 \
  Verifying  : perl-Net-Daemon-0.48-5.el7.noarch                                                                                                                                                                                                                    7/10 \
  Verifying  : perl-DBI-1.627-4.el7.x86_64                                                                                                                                                                                                                          8/10 \
  Verifying  : perl-IO-Compress-2.061-2.el7.noarch                                                                                                                                                                                                                  9/10 \
  Verifying  : perl-DBD-MySQL-4.023-5.el7.x86_64                                                                                                                                                                                                                   10/10 \
\
Installed:\
  mariadb-server.x86_64 1:5.5.52-1.el7                                                                                                                                                                                                                                   \
\
Dependency Installed:\
  mariadb.x86_64 1:5.5.52-1.el7              perl-Compress-Raw-Bzip2.x86_64 0:2.061-3.el7      perl-Compress-Raw-Zlib.x86_64 1:2.061-4.el7      perl-DBD-MySQL.x86_64 0:4.023-5.el7      perl-DBI.x86_64 0:1.627-4.el7      perl-Data-Dumper.x86_64 0:2.145-3.el7     \
  perl-IO-Compress.noarch 0:2.061-2.el7      perl-Net-Daemon.noarch 0:0.48-5.el7               perl-PlRPC.noarch 0:0.2020-14.el7               \
\
Complete!\
[root@cluster1node1 ~]# }