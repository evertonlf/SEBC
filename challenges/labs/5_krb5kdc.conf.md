[root@cluster1node2 krb5kdc]# cat /etc/krb5.conf
# Configuration snippets may be placed in this directory as well
includedir /etc/krb5.conf.d/

[logging]
 default = FILE:/var/log/krb5libs.log
 kdc = FILE:/var/log/krb5kdc.log
 admin_server = FILE:/var/log/kadmind.log

[libdefaults]
 dns_lookup_realm = false
 ticket_lifetime = 24h
 renew_lifetime = 7d
 forwardable = true
 rdns = false
 default_realm = EVERTONLF.ES
 udp_preference_limit = 1
 default_tgs_enctypes = arcfour-hmac
 default_tkt_enctypes = arcfour-hmac

[realms]
 EVERTONLF.ES = {
 kdc = cluster1node2.lab.local
 admin_server = cluster1node2.lab.local
 }

[domain_realm]
 .lab.local = EVERTONLF.ES
 lab.local = EVERTONLF.ES
[root@cluster1node2 krb5kdc]#
