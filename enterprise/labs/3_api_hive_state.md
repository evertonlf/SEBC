List Hive Services
[root@cluster1node1 /]# curl -u admin:admin get http://192.168.100.161:7180/api/v2/clusters/evertonlf/services/hive


Stop Hive
[root@cluster1node1 /]# curl -X POST -u admin:admin http://192.168.100.161:7180/api/v2/clusters/evertonlf/services/hive/commands/stop
{
  "id" : 1012,
  "name" : "Stop",
  "startTime" : "2017-04-05T17:43:27.562Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}[root@cluster1node1 /]#




Start Hive
[root@cluster1node1 /]# curl -X POST -u admin:admin http://192.168.100.161:7180/api/v2/clusters/evertonlf/services/hive/commands/start
{
  "id" : 1016,
  "name" : "Start",
  "startTime" : "2017-04-05T17:45:01.547Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}[root@cluster1node1 /]#



Status
[root@cluster1node1 /]# curl -u admin:admin http://192.168.100.161:7180/api/v2/clusters/evertonlf/services/hive
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://cluster1node1.lab.local:7180/cmf/serviceRedirect/hive",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD"
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD"
  } ],
  "configStale" : false,
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive"
}[root@cluster1node1 /]#
