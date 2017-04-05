What is ubertask optimization?
Is the option to enable small-jobs run sequentially within a single JVM, default value is disabled.


Where in CM is the Kerberos Security Realm value displayed?
In the menu Admnistration option configration category Kerberos.


Which CDH service(s) host a property for enabling Kerberos authentication?
Hue


How do you upgrade the CM agents?
By wizard in the cloudera manager\hosts or by command line manually stopping the agent in the hosts executing the
upgrade command and restart agent in the host.


Give the tsquery statement used to chart Hue's CPU utilization?
select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName=$SERVICENAME


Name all the roles that make up the Hive service.
Gateway, Hive Metastore Server and HiveServe2, hive-webhcat-server


What steps must be completed before integrating Cloudera Manager with Kerberos?
Create a Kerberos administrator principal for the Cloudera Manager, set up a working KDC, 
Configure the KDC to allow renewable tickets with non-zero ticket lifetimes, If you are using Active Directory, make sure LDAP over TLS/SSL (LDAPS) is enabled for the Domain Controllers,
install the packages open-ldap and krb5-libs (in this case for red hat or centos) depending of the OS in use.  