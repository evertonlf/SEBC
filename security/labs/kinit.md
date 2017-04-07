KINIT

[root@cluster1node1 krb5kdc]# kinit evertonlf/admin@LAB.LOCAL
Password for evertonlf/admin@LAB.LOCAL:
[root@cluster1node1 krb5kdc]#


KLIST

[root@cluster1node1 krb5kdc]# klist
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: evertonlf/admin@LAB.LOCAL

Valid starting       Expires              Service principal
04/07/2017 01:55:45  04/08/2017 01:55:45  krbtgt/LAB.LOCAL@LAB.LOCAL
        renew until 04/14/2017 01:55:45
[root@cluster1node1 krb5kdc]#
[root@cluster1node1 krb5kdc]#


