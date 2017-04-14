Cloud Provider
I am using our own Private Cloud Compwire


List of the Nodes
cluster1node1.lab.local 192.168.100.161
cluster1node2.lab.local 192.168.100.162
cluster1node3.lab.local 192.168.100.163
cluster1node4.lab.local 192.168.100.164
cluster1node5.lab.local 192.168.100.165


Linux realease
CentOS Linux release 7.3.1611 (Core)


Disk Capacity
[root@cluster1node1 ~]# df -h
Filesystem               Size  Used Avail Use% Mounted on
/dev/mapper/centos-root   36G  1.2G   35G   4% /
devtmpfs                 7.8G     0  7.8G   0% /dev
tmpfs                    7.8G     0  7.8G   0% /dev/shm
tmpfs                    7.8G  8.5M  7.8G   1% /run
tmpfs                    7.8G     0  7.8G   0% /sys/fs/cgroup
/dev/sda1                497M  169M  329M  34% /boot
tmpfs                    1.6G     0  1.6G   0% /run/user/0
[root@cluster1node1 ~]# fdisk -l

Disk /dev/sda: 42.9 GB, 42949672960 bytes, 83886080 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disk label type: dos
Disk identifier: 0x00004b55

   Device Boot      Start         End      Blocks   Id  System
/dev/sda1   *        2048     1026047      512000   83  Linux
/dev/sda2         1026048    83886079    41430016   8e  Linux LVM

Disk /dev/mapper/centos-root: 38.1 GB, 38084280320 bytes, 74383360 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/mapper/centos-swap: 4294 MB, 4294967296 bytes, 8388608 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes

[root@cluster1node1 ~]#


[root@cluster1node2 ~]# df -h
Filesystem               Size  Used Avail Use% Mounted on
/dev/mapper/centos-root   36G  1.2G   35G   4% /
devtmpfs                 7.8G     0  7.8G   0% /dev
tmpfs                    7.8G     0  7.8G   0% /dev/shm
tmpfs                    7.8G  8.5M  7.8G   1% /run
tmpfs                    7.8G     0  7.8G   0% /sys/fs/cgroup
/dev/sda1                497M  169M  329M  34% /boot
tmpfs                    1.6G     0  1.6G   0% /run/user/0
[root@cluster1node2 ~]#
[root@cluster1node2 ~]#
[root@cluster1node2 ~]# fdisk -l

Disk /dev/sda: 42.9 GB, 42949672960 bytes, 83886080 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disk label type: dos
Disk identifier: 0x00004b55

   Device Boot      Start         End      Blocks   Id  System
/dev/sda1   *        2048     1026047      512000   83  Linux
/dev/sda2         1026048    83886079    41430016   8e  Linux LVM

Disk /dev/mapper/centos-root: 38.1 GB, 38084280320 bytes, 74383360 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/mapper/centos-swap: 4294 MB, 4294967296 bytes, 8388608 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes

[root@cluster1node2 ~]#



[root@cluster1node3 ~]# df -h
Filesystem               Size  Used Avail Use% Mounted on
/dev/mapper/centos-root   36G  1.2G   35G   4% /
devtmpfs                 7.8G     0  7.8G   0% /dev
tmpfs                    7.8G     0  7.8G   0% /dev/shm
tmpfs                    7.8G  8.5M  7.8G   1% /run
tmpfs                    7.8G     0  7.8G   0% /sys/fs/cgroup
/dev/sda1                497M  169M  329M  34% /boot
tmpfs                    1.6G     0  1.6G   0% /run/user/0
[root@cluster1node3 ~]#
[root@cluster1node3 ~]#
[root@cluster1node3 ~]# fdisk -l

Disk /dev/sda: 42.9 GB, 42949672960 bytes, 83886080 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disk label type: dos
Disk identifier: 0x00004b55

   Device Boot      Start         End      Blocks   Id  System
/dev/sda1   *        2048     1026047      512000   83  Linux
/dev/sda2         1026048    83886079    41430016   8e  Linux LVM

Disk /dev/mapper/centos-root: 38.1 GB, 38084280320 bytes, 74383360 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/mapper/centos-swap: 4294 MB, 4294967296 bytes, 8388608 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes

[root@cluster1node3 ~]#

[root@cluster1node4 ~]# df -h
Filesystem               Size  Used Avail Use% Mounted on
/dev/mapper/centos-root   36G  1.2G   35G   4% /
devtmpfs                 7.8G     0  7.8G   0% /dev
tmpfs                    7.8G     0  7.8G   0% /dev/shm
tmpfs                    7.8G  8.5M  7.8G   1% /run
tmpfs                    7.8G     0  7.8G   0% /sys/fs/cgroup
/dev/sda1                497M  169M  329M  34% /boot
tmpfs                    1.6G     0  1.6G   0% /run/user/0
[root@cluster1node4 ~]#
[root@cluster1node4 ~]#
[root@cluster1node4 ~]# fdisk -l

Disk /dev/sda: 42.9 GB, 42949672960 bytes, 83886080 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disk label type: dos
Disk identifier: 0x00004b55

   Device Boot      Start         End      Blocks   Id  System
/dev/sda1   *        2048     1026047      512000   83  Linux
/dev/sda2         1026048    83886079    41430016   8e  Linux LVM

Disk /dev/mapper/centos-root: 38.1 GB, 38084280320 bytes, 74383360 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/mapper/centos-swap: 4294 MB, 4294967296 bytes, 8388608 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes

[root@cluster1node4 ~]#
[root@cluster1node4 ~]#


[root@cluster1node5 ~]# df -h
Filesystem               Size  Used Avail Use% Mounted on
/dev/mapper/centos-root   36G  1.2G   35G   4% /
devtmpfs                 7.8G     0  7.8G   0% /dev
tmpfs                    7.8G     0  7.8G   0% /dev/shm
tmpfs                    7.8G  8.5M  7.8G   1% /run
tmpfs                    7.8G     0  7.8G   0% /sys/fs/cgroup
/dev/sda1                497M  169M  329M  34% /boot
tmpfs                    1.6G     0  1.6G   0% /run/user/0
[root@cluster1node5 ~]#
[root@cluster1node5 ~]#
[root@cluster1node5 ~]# fdisk -l

Disk /dev/sda: 42.9 GB, 42949672960 bytes, 83886080 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disk label type: dos
Disk identifier: 0x00004b55

   Device Boot      Start         End      Blocks   Id  System
/dev/sda1   *        2048     1026047      512000   83  Linux
/dev/sda2         1026048    83886079    41430016   8e  Linux LVM

Disk /dev/mapper/centos-root: 38.1 GB, 38084280320 bytes, 74383360 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/mapper/centos-swap: 4294 MB, 4294967296 bytes, 8388608 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes

[root@cluster1node5 ~]#



Yum repolist

[root@cluster1node1 ~]# yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
Could not retrieve mirrorlist http://mirrorlist.centos.org/?release=7&arch=x86_64&repo=os&infra=stock error was
14: curl#6 - "Could not resolve host: mirrorlist.centos.org; Unknown error"
Could not retrieve mirrorlist http://mirrorlist.centos.org/?release=7&arch=x86_64&repo=extras&infra=stock error was
14: curl#6 - "Could not resolve host: mirrorlist.centos.org; Unknown error"
Could not retrieve mirrorlist http://mirrorlist.centos.org/?release=7&arch=x86_64&repo=updates&infra=stock error was
14: curl#6 - "Could not resolve host: mirrorlist.centos.org; Unknown error"
 * base: centos.brisanet.com.br
 * extras: centos.brisanet.com.br
 * updates: centos.brisanet.com.br
repo id                                                                           repo name                                                                           status
!base/7/x86_64                                                                    CentOS-7 - Base                                                                     9,363
!extras/7/x86_64                                                                  CentOS-7 - Extras                                                                     311
!updates/7/x86_64                                                                 CentOS-7 - Updates                                                                  1,126
repolist: 10,800
[root@cluster1node1 ~]#

List User and Groups

[root@cluster1node1 ~]# ls -l /etc/passwd
-rw-r--r-- 1 root root 1164 Apr 14 10:40 /etc/passwd
[root@cluster1node1 ~]# ls -l /etc/group
-rw-r--r-- 1 root root 543 Apr 14 10:40 /etc/group
[root@cluster1node1 ~]#


List Users and Groups

[root@cluster1node1 etc]# cat /etc/passwd
ronaldo:x:2016:1000::/home/ronaldo:/bin/bash
neymar:x:2010:1001::/home/neymar:/bin/bash

[root@cluster1node1 etc]# cat /etc/group
barca:x:1000:
merengues:x:1001:
[root@cluster1node1 etc]#


[root@cluster1node2 ~]# cat /etc/passwd
ronaldo:x:2016:1000::/home/ronaldo:/bin/bash
neymar:x:2010:1001::/home/neymar:/bin/bash
[root@cluster1node2 ~]#

[root@cluster1node2 ~]# cat /etc/group
barca:x:1000:
merengues:x:1001:
[root@cluster1node2 ~]#


[root@cluster1node3 ~]# cat /etc/passwd
ronaldo:x:2016:1000::/home/ronaldo:/bin/bash
neymar:x:2010:1001::/home/neymar:/bin/bash
[root@cluster1node3 ~]#

[root@cluster1node3 ~]# cat /etc/group
barca:x:1000:
merengues:x:1001:
[root@cluster1node3 ~]#


[root@cluster1node4 ~]# cat /etc/passwd
ronaldo:x:2016:1000::/home/ronaldo:/bin/bash
neymar:x:2010:1001::/home/neymar:/bin/bash
[root@cluster1node4 ~]#
[root@cluster1node4 ~]#

[root@cluster1node4 ~]# cat /etc/group
barca:x:1000:
merengues:x:1001:
[root@cluster1node4 ~]#


[root@cluster1node5 ~]# cat /etc/passwd
ronaldo:x:2016:1000::/home/ronaldo:/bin/bash
neymar:x:2010:1001::/home/neymar:/bin/bash
[root@cluster1node5 ~]#


[root@cluster1node5 ~]# cat /etc/group
barca:x:1000:
merengues:x:1001:
[root@cluster1node5 ~]#






