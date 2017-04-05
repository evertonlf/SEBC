{
  "timestamp" : "2017-04-05T16:18:12.403Z",
  "clusters" : [ {
    "name" : "evertonlf",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "1101004800"
          }, {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "110100480"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "2025848832"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "2238028185"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "376"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "cluster1node1.lab.local"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "password"
        }, {
          "name" : "hive_metastore_database_user",
          "value" : "user"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-128924fa5686f7395dbba64fdf9352a8",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "81cf6822-9023-4bb6-aeae-baa8f0db9800"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-9257b14dd0bed4e0b211bcea0f25e74e",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "ff7f072e-e935-40bc-bdd6-e6e04cb24a41"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-d223a4be4b4362573659760ff024cb7f",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "3d5ba5c5-95dc-43e3-ac43-a8cc8a3b74b0"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-d5c4884915b78fb0e97147bbb61597a4",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "d374d06e-9076-4042-8a85-29bb53cf7a3f"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-f674365dc3ff1608310b49d8a7ac7c4b",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "27ad1803-6aae-4e79-b92d-fb7208f40cb5"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-d5c4884915b78fb0e97147bbb61597a4",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "d374d06e-9076-4042-8a85-29bb53cf7a3f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8tenic9s8snvof37f6gt0mk8z"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-128924fa5686f7395dbba64fdf9352a8",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "81cf6822-9023-4bb6-aeae-baa8f0db9800"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6x0znhrl84gnhb8jzpuewox7z"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "service_health_suppression_zookeeper_canary_health",
          "value" : "true"
        } ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-9257b14dd0bed4e0b211bcea0f25e74e",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "ff7f072e-e935-40bc-bdd6-e6e04cb24a41"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ezcorqdhjk2obr3r8ydptvzj4"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-d223a4be4b4362573659760ff024cb7f",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "3d5ba5c5-95dc-43e3-ac43-a8cc8a3b74b0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "abfj6myofvwnz560nsbf6p4ct"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-f674365dc3ff1608310b49d8a7ac7c4b",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "27ad1803-6aae-4e79-b92d-fb7208f40cb5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1ldvooox1ft92w9d29j66nx99"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "cluster1node1.lab.local"
        }, {
          "name" : "database_password",
          "value" : "password"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "database_user",
          "value" : "user"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-d5c4884915b78fb0e97147bbb61597a4"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-d5c4884915b78fb0e97147bbb61597a4",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "d374d06e-9076-4042-8a85-29bb53cf7a3f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3pxnmu6vzilv79j7ug8oqu4nj"
          }, {
            "name" : "secret_key",
            "value" : "dQZhmlUolutFQjWWMROjyQhzf5fNNB"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "cluster1node1.lab.local"
          }, {
            "name" : "oozie_database_password",
            "value" : "password"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "user"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-d5c4884915b78fb0e97147bbb61597a4",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "d374d06e-9076-4042-8a85-29bb53cf7a3f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1coukqt5zwkt6c0eqem92dd0o"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "4"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "2"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "2"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "3026"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "4620"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "2"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "bYesNpkECmwWDLYhyR689fI7c7KoiB"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-GATEWAY-d5c4884915b78fb0e97147bbb61597a4",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "d374d06e-9076-4042-8a85-29bb53cf7a3f"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-JOBHISTORY-9257b14dd0bed4e0b211bcea0f25e74e",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "ff7f072e-e935-40bc-bdd6-e6e04cb24a41"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c9dyp28aibudqfn8egpwuev1m"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-128924fa5686f7395dbba64fdf9352a8",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "81cf6822-9023-4bb6-aeae-baa8f0db9800"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "787znm9kom2fn5dczquln3u7a"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-9257b14dd0bed4e0b211bcea0f25e74e",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "ff7f072e-e935-40bc-bdd6-e6e04cb24a41"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d1guk2xu4x16arnww3kxjuy6k"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-d223a4be4b4362573659760ff024cb7f",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "3d5ba5c5-95dc-43e3-ac43-a8cc8a3b74b0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "eieankv6kd6qs8xpdyjtvyj1q"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-f674365dc3ff1608310b49d8a7ac7c4b",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "27ad1803-6aae-4e79-b92d-fb7208f40cb5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "izwdmq6ugprag9n992vveg6n"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-d223a4be4b4362573659760ff024cb7f",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "3d5ba5c5-95dc-43e3-ac43-a8cc8a3b74b0"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "173"
          }, {
            "name" : "role_jceks_password",
            "value" : "3yk0uaypvwwr1qdutzg04el8l"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3806568448"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "3172990976"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "1101004800"
          }, {
            "name" : "role_config_suppression_namenode_java_heapsize_minimum_validator",
            "value" : "true"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "1101004800"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "A1g5vuOWhOaECDuHdUDfhXbSr0Z6Jx"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "Glv4IftqpZAsJe74fPX68NJ08AYlgI"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "k5zp7aSNoOOPXEk4KDbRf3sxQktzle"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-d223a4be4b4362573659760ff024cb7f",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "3d5ba5c5-95dc-43e3-ac43-a8cc8a3b74b0"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-128924fa5686f7395dbba64fdf9352a8",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "81cf6822-9023-4bb6-aeae-baa8f0db9800"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6uhkzhba18pcdyrak4oo1qnol"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-9257b14dd0bed4e0b211bcea0f25e74e",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "ff7f072e-e935-40bc-bdd6-e6e04cb24a41"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6ig1fmfpkgcphzh9f4mb10fho"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-d223a4be4b4362573659760ff024cb7f",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "3d5ba5c5-95dc-43e3-ac43-a8cc8a3b74b0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ervsg56m42b7no9dxacwq4528"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-f674365dc3ff1608310b49d8a7ac7c4b",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "27ad1803-6aae-4e79-b92d-fb7208f40cb5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c1lcndyaoz6sbcqa51uzwny1q"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-128924fa5686f7395dbba64fdf9352a8",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "81cf6822-9023-4bb6-aeae-baa8f0db9800"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ebvebhgasiw3vb3bppyj7nix7"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-d5c4884915b78fb0e97147bbb61597a4",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "d374d06e-9076-4042-8a85-29bb53cf7a3f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d1wnyvxesg8jkog2zxy3ym64k"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-9257b14dd0bed4e0b211bcea0f25e74e",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "ff7f072e-e935-40bc-bdd6-e6e04cb24a41"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "l1di2c77ipr3yqoiotl0gr0j"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-d223a4be4b4362573659760ff024cb7f",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "3d5ba5c5-95dc-43e3-ac43-a8cc8a3b74b0"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "11skoi341fzynthhg5c0xevep"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-f674365dc3ff1608310b49d8a7ac7c4b",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "27ad1803-6aae-4e79-b92d-fb7208f40cb5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "93zwdmfefrzxbxg9n6p2c4vgq"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-128924fa5686f7395dbba64fdf9352a8",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "81cf6822-9023-4bb6-aeae-baa8f0db9800"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "197"
          }, {
            "name" : "role_jceks_password",
            "value" : "f1ewmy6s4856xp8ejjr800wrm"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-d5c4884915b78fb0e97147bbb61597a4",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "d374d06e-9076-4042-8a85-29bb53cf7a3f"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "195"
          }, {
            "name" : "role_jceks_password",
            "value" : "12gfytkg7b08osa6viaji4xha"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "d374d06e-9076-4042-8a85-29bb53cf7a3f",
    "ipAddress" : "192.168.100.161",
    "hostname" : "cluster1node1.lab.local",
    "rackId" : "/default",
    "config" : {
      "items" : [ {
        "name" : "host_config_suppression_memory_overcommitted_validator",
        "value" : "true"
      } ]
    }
  }, {
    "hostId" : "81cf6822-9023-4bb6-aeae-baa8f0db9800",
    "ipAddress" : "192.168.100.162",
    "hostname" : "cluster1node2.lab.local",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "3d5ba5c5-95dc-43e3-ac43-a8cc8a3b74b0",
    "ipAddress" : "192.168.100.163",
    "hostname" : "cluster1node3.lab.local",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "ff7f072e-e935-40bc-bdd6-e6e04cb24a41",
    "ipAddress" : "192.168.100.164",
    "hostname" : "cluster1node4.lab.local",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "27ad1803-6aae-4e79-b92d-fb7208f40cb5",
    "ipAddress" : "192.168.100.165",
    "hostname" : "cluster1node5.lab.local",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-d5c4884915b78fb0e97147bbb61597a4",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "c746e9981f1398a5b5ace44bf1a804245133def45053da867d338f9a615fc3ba",
    "pwSalt" : 6522078188711666728,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-d5c4884915b78fb0e97147bbb61597a4",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "075711cc2e3a01e515d40fc9fdfc60b2c3431debc6a14e6f73150cf585d7ed58",
    "pwSalt" : 6753700964151102484,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-d5c4884915b78fb0e97147bbb61597a4",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "4851aa95e1de0d89dc1269f4ed7e8a5e5b45586bf02a8d9e13303e08a4738ba7",
    "pwSalt" : -6894841834178993326,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-d5c4884915b78fb0e97147bbb61597a4",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "afe0d46539a0ace12a3f1799a08393916180e5a4b7bb3a9bd4cdc6490877b9de",
    "pwSalt" : -5432837255423163393,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "cc0e550ed30495ecc27730b38ef9817eb332602f43cd725d938ecc791fa04c63",
    "pwSalt" : 2906667041831912110,
    "pwLogin" : true
  }, {
    "name" : "evertonlf",
    "roles" : [ "ROLE_OPERATOR" ],
    "pwHash" : "80da18cb15ec0d91c1fc724e12c06e627e756eb98b31b9887c11332bb3cdc31b",
    "pwSalt" : -7201451136583309193,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "dc2723c9ed8376f84d0a4ba035bc960e862d171ebf9b20a0f6aac6950dcba868",
    "pwSalt" : 2127169449077195423,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.10.1",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170319-2001",
    "gitHash" : "f226435f6fa5f545543c00245900ae43bea7a29c",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736000"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "cluster1node1.lab.local"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "password"
        }, {
          "name" : "headlamp_database_user",
          "value" : "user"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736000"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-d5c4884915b78fb0e97147bbb61597a4",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "d374d06e-9076-4042-8a85-29bb53cf7a3f"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "dxwsho8bss8fp8vajb5o3ob4r"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-d5c4884915b78fb0e97147bbb61597a4",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "d374d06e-9076-4042-8a85-29bb53cf7a3f"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "4wxayi572xefngts4q7c1qy62"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-d5c4884915b78fb0e97147bbb61597a4",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "d374d06e-9076-4042-8a85-29bb53cf7a3f"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "7zjqy5g4jb3l4e6iw2pri150f"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-d5c4884915b78fb0e97147bbb61597a4",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "d374d06e-9076-4042-8a85-29bb53cf7a3f"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "cbiwp55adx9m4ri8s6ahe2mtx"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-d5c4884915b78fb0e97147bbb61597a4",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "d374d06e-9076-4042-8a85-29bb53cf7a3f"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "6wrk94sx46vnbuurao74c1mey"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/25/2012 2:20"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "NOT_ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}