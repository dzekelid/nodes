{
  "info": {
    "name": "Amazon ElastiCache API Purchase Reserved Cache Nodes Offering",
    "_postman_id": "7563d4aa-6fa9-41bf-b157-ce6909b171da",
    "description": "Allows you to purchase a reserved\n            cache node offering.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Resource Tags",
      "item": [
        {
          "id": "403d9b78-2e1f-4d77-8eea-0524b9b7f3c1",
          "name": "addTagsToResource",
          "request": {
            "url": "http://example.com/api/?Action=AddTagsToResource?ResourceName=ResourceName&Tags.Tag.N=Tags.Tag.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Adds up to 10 cost allocation tags to the named resource."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "26ddc75c-0aa5-4c3f-a23a-c2d93b5148b7"
            }
          ]
        },
        {
          "id": "5b952cb3-8a6e-4014-99e7-c310ceed6943",
          "name": "listTagsForResource",
          "request": {
            "url": "http://example.com/api/?Action=ListTagsForResource?ResourceName=ResourceName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists all cost allocation tags currently on the named resource."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f99f1c5e-b0c0-42d3-b906-7b78fd507f63"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Security Groups",
      "item": [
        {
          "id": "f90141d4-e285-4d13-a09d-02f88eebda19",
          "name": "authorizeCacheSecurityGroupIngress",
          "request": {
            "url": "http://example.com/api/?Action=AuthorizeCacheSecurityGroupIngress?CacheSecurityGroupName=CacheSecurityGroupName&EC2SecurityGroupName=EC2SecurityGroupName&EC2SecurityGroupOwnerId=EC2SecurityGroupOwnerId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Allows network ingress to a cache\n            security group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5d01cabc-2886-4154-9d07-0b5a5001cd3e"
            }
          ]
        },
        {
          "id": "34e2b00f-5480-465b-950f-8e4d47204423",
          "name": "createCacheSecurityGroup",
          "request": {
            "url": "http://example.com/api/?Action=CreateCacheSecurityGroup?CacheSecurityGroupName=CacheSecurityGroupName&Description=Description",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new cache security group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e425fd2f-ad57-4e8b-8c8f-cba93247ba8f"
            }
          ]
        },
        {
          "id": "31ee024f-76e3-46a3-bc4e-d6911395010b",
          "name": "deleteCacheSecurityGroup",
          "request": {
            "url": "http://example.com/api/?Action=DeleteCacheSecurityGroup?CacheSecurityGroupName=CacheSecurityGroupName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a cache security group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7ab59534-8076-4985-9718-85ea48284a44"
            }
          ]
        },
        {
          "id": "072d07ca-e8ec-42e7-998a-4d5702ac7c3f",
          "name": "describeCacheSecurityGroups",
          "request": {
            "url": "http://example.com/api/?Action=DescribeCacheSecurityGroups?CacheSecurityGroupName=CacheSecurityGroupName&Marker=Marker&MaxRecords=MaxRecords",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of cache security group\n            descriptions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "25c2cc3d-5e16-44db-94c7-d97a772390c4"
            }
          ]
        }
      ]
    },
    {
      "name": "Snapshots",
      "item": [
        {
          "id": "c7703aee-378f-47a0-b85d-619cb9243597",
          "name": "copySnapshot",
          "request": {
            "url": "http://example.com/api/?Action=CopySnapshot?SourceSnapshotName=SourceSnapshotName&TargetBucket=TargetBucket&TargetSnapshotName=TargetSnapshotName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Makes a copy of an existing snapshot."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a933c8ae-761c-46a0-9011-d86d40d60ee0"
            }
          ]
        },
        {
          "id": "52cff653-467c-49f5-89fe-c80a5079985e",
          "name": "createSnapshot",
          "request": {
            "url": "http://example.com/api/?Action=CreateSnapshot?CacheClusterId=CacheClusterId&ReplicationGroupId=ReplicationGroupId&SnapshotName=SnapshotName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a copy of an entire cache cluster or replication group at a\n            specific moment in time."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ad9513cb-3c42-4645-a586-5dafca1a67e3"
            }
          ]
        },
        {
          "id": "110fe83e-4d74-491b-80ac-11f111425725",
          "name": "deleteSnapshot",
          "request": {
            "url": "http://example.com/api/?Action=DeleteSnapshot?SnapshotName=SnapshotName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes an existing snapshot."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1b614007-5ce0-4dd5-a909-dc4a411f3033"
            }
          ]
        },
        {
          "id": "506e2f87-b3b7-4681-b493-eab4b76f830e",
          "name": "describeSnapshots",
          "request": {
            "url": "http://example.com/api/?Action=DescribeSnapshots?CacheClusterId=CacheClusterId&Marker=Marker&MaxRecords=MaxRecords&ReplicationGroupId=ReplicationGroupId&ShowNodeGroupConfig=ShowNodeGroupConfig&SnapshotName=SnapshotName&SnapshotSource=SnapshotSource",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns information about cache cluster or replication group snapshots."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "49eef4fc-663f-4bca-8dec-b8e44ab46f38"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Clusters",
      "item": [
        {
          "id": "2be56697-d6c5-436d-9cb9-3efeeb646fab",
          "name": "createCacheCluster",
          "request": {
            "url": "http://example.com/api/?Action=CreateCacheCluster?AuthToken=AuthToken&AutoMinorVersionUpgrade=AutoMinorVersionUpgrade&AZMode=AZMode&CacheClusterId=CacheClusterId&CacheNodeType=CacheNodeType&CacheParameterGroupName=CacheParameterGroupName&CacheSecurityGroupNames.CacheSecurityGroupName.N=CacheSecurityGroupNames.CacheSecurityGroupName.N&CacheSubnetGroupName=CacheSubnetGroupName&Engine=Engine&EngineVersion=EngineVersion&NotificationTopicArn=NotificationTopicArn&NumCacheNodes=NumCacheNodes&Port=Port&PreferredAvailabilityZone=PreferredAvailabilityZone&PreferredAvailabilityZones.PreferredAvailabilityZone.N=PreferredAvailabilityZones.PreferredAvailabilityZone.N&PreferredMaintenanceWindow=PreferredMaintenanceWindow&ReplicationGroupId=ReplicationGroupId&SecurityGroupIds.SecurityGroupId.N=SecurityGroupIds.SecurityGroupId.N&SnapshotArns.SnapshotArn.N=SnapshotArns.SnapshotArn.N&SnapshotName=SnapshotName&SnapshotRetentionLimit=SnapshotRetentionLimit&SnapshotWindow=SnapshotWindow&Tags.Tag.N=Tags.Tag.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a cache cluster."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f8a04710-a0e9-43ef-958c-9950bdf22af9"
            }
          ]
        },
        {
          "id": "288686d9-5376-424c-bdd9-f2922198c90e",
          "name": "deleteCacheCluster",
          "request": {
            "url": "http://example.com/api/?Action=DeleteCacheCluster?CacheClusterId=CacheClusterId&FinalSnapshotIdentifier=FinalSnapshotIdentifier",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a previously provisioned cache cluster."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b9373e3e-277e-45c6-a1dd-28095bf4af16"
            }
          ]
        },
        {
          "id": "89eb4e71-426f-4984-8595-2b1eb1683ba1",
          "name": "describeCacheClusters",
          "request": {
            "url": "http://example.com/api/?Action=DescribeCacheClusters?CacheClusterId=CacheClusterId&Marker=Marker&MaxRecords=MaxRecords&ShowCacheNodeInfo=ShowCacheNodeInfo",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns information about all provisioned\n            cache clusters if no cache cluster identifier is specified, or about a specific cache\n            cluster if a cache cluster identifier is supplied."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1c0d5558-2c5e-43f9-9655-00f04182e030"
            }
          ]
        },
        {
          "id": "6cff5695-b87c-41e6-a01f-b6c29c5eba97",
          "name": "modifyCacheCluster",
          "request": {
            "url": "http://example.com/api/?Action=ModifyCacheCluster?ApplyImmediately=ApplyImmediately&AutoMinorVersionUpgrade=AutoMinorVersionUpgrade&AZMode=AZMode&CacheClusterId=CacheClusterId&CacheNodeIdsToRemove.CacheNodeId.N=CacheNodeIdsToRemove.CacheNodeId.N&CacheNodeType=CacheNodeType&CacheParameterGroupName=CacheParameterGroupName&CacheSecurityGroupNames.CacheSecurityGroupName.N=CacheSecurityGroupNames.CacheSecurityGroupName.N&EngineVersion=EngineVersion&NewAvailabilityZones.PreferredAvailabilityZone.N=NewAvailabilityZones.PreferredAvailabilityZone.N&NotificationTopicArn=NotificationTopicArn&NotificationTopicStatus=NotificationTopicStatus&NumCacheNodes=NumCacheNodes&PreferredMaintenanceWindow=PreferredMaintenanceWindow&SecurityGroupIds.SecurityGroupId.N=SecurityGroupIds.SecurityGroupId.N&SnapshotRetentionLimit=SnapshotRetentionLimit&SnapshotWindow=SnapshotWindow",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Modifies the settings for a cache cluster."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "14cc9e8f-da95-4ca2-9815-99cf8e235675"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Parameter Groups",
      "item": [
        {
          "id": "37c08e87-c545-4398-98ac-8bc2041d1998",
          "name": "createCacheParameterGroup",
          "request": {
            "url": "http://example.com/api/?Action=CreateCacheParameterGroup?CacheParameterGroupFamily=CacheParameterGroupFamily&CacheParameterGroupName=CacheParameterGroupName&Description=Description",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new cache parameter group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "78954254-b3ba-4ff7-8689-99a2bed72ad3"
            }
          ]
        },
        {
          "id": "4c9a602c-b114-4737-8e42-f296669722ed",
          "name": "deleteCacheParameterGroup",
          "request": {
            "url": "http://example.com/api/?Action=DeleteCacheParameterGroup?CacheParameterGroupName=CacheParameterGroupName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes the specified cache parameter\n            group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8591efc7-40b0-4018-b4da-d2105cbe1277"
            }
          ]
        },
        {
          "id": "4f5e7cef-2af1-4dce-8f4f-65ac837ba543",
          "name": "describeCacheParameterGroups",
          "request": {
            "url": "http://example.com/api/?Action=DescribeCacheParameterGroups?CacheParameterGroupName=CacheParameterGroupName&Marker=Marker&MaxRecords=MaxRecords",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of cache parameter group\n            descriptions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "64442c87-60fc-4207-a6a2-02892aafc2dc"
            }
          ]
        },
        {
          "id": "a72c6c73-b409-46ce-92e7-0f2f81006bf1",
          "name": "modifyCacheParameterGroup",
          "request": {
            "url": "http://example.com/api/?Action=ModifyCacheParameterGroup?CacheParameterGroupName=CacheParameterGroupName&ParameterNameValues.ParameterNameValue.N=ParameterNameValues.ParameterNameValue.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Modifies the parameters of a cache\n            parameter group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6c206d8d-6726-4670-a4bf-b8213f667917"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Subnet Groups",
      "item": [
        {
          "id": "c5765d65-c069-4f2a-bac4-90194c70dcf1",
          "name": "createCacheSubnetGroup",
          "request": {
            "url": "http://example.com/api/?Action=CreateCacheSubnetGroup?CacheSubnetGroupDescription=CacheSubnetGroupDescription&CacheSubnetGroupName=CacheSubnetGroupName&SubnetIds.SubnetIdentifier.N=SubnetIds.SubnetIdentifier.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new cache subnet group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "958edb3a-009c-4b31-a148-2fbdcaa9babb"
            }
          ]
        },
        {
          "id": "77ba1c8b-af0f-4043-bc21-4a7322f7056c",
          "name": "deleteCacheSubnetGroup",
          "request": {
            "url": "http://example.com/api/?Action=DeleteCacheSubnetGroup?CacheSubnetGroupName=CacheSubnetGroupName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a cache subnet group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ebca084a-b823-4d46-8690-63879ba07c44"
            }
          ]
        },
        {
          "id": "bc5f8f1b-077c-45ab-9cf4-1a5cb73eea98",
          "name": "describeCacheSubnetGroups",
          "request": {
            "url": "http://example.com/api/?Action=DescribeCacheSubnetGroups?CacheSubnetGroupName=CacheSubnetGroupName&Marker=Marker&MaxRecords=MaxRecords",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of cache subnet group\n            descriptions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "77418b81-229a-4889-8f5c-c37f080b2301"
            }
          ]
        },
        {
          "id": "71e0b219-1b88-46ba-a445-0aee736f7c4a",
          "name": "modifyCacheSubnetGroup",
          "request": {
            "url": "http://example.com/api/?Action=ModifyCacheSubnetGroup?CacheSubnetGroupDescription=CacheSubnetGroupDescription&CacheSubnetGroupName=CacheSubnetGroupName&SubnetIds.SubnetIdentifier.N=SubnetIds.SubnetIdentifier.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Modifies an existing cache subnet group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "94b5c10f-5f0f-4c33-8da7-219855458f6f"
            }
          ]
        }
      ]
    },
    {
      "name": "Replication Groups",
      "item": [
        {
          "id": "9d945eb6-3865-4c05-8cee-d888c88544fa",
          "name": "createReplicationGroup",
          "request": {
            "url": "http://example.com/api/?Action=CreateReplicationGroup?AuthToken=AuthToken&AutomaticFailoverEnabled=AutomaticFailoverEnabled&AutoMinorVersionUpgrade=AutoMinorVersionUpgrade&CacheNodeType=CacheNodeType&CacheParameterGroupName=CacheParameterGroupName&CacheSecurityGroupNames.CacheSecurityGroupName.N=CacheSecurityGroupNames.CacheSecurityGroupName.N&CacheSubnetGroupName=CacheSubnetGroupName&Engine=Engine&EngineVersion=EngineVersion&NodeGroupConfiguration.NodeGroupConfiguration.N=NodeGroupConfiguration.NodeGroupConfiguration.N&NotificationTopicArn=NotificationTopicArn&NumCacheClusters=NumCacheClusters&NumNodeGroups=NumNodeGroups&Port=Port&PreferredCacheClusterAZs.AvailabilityZone.N=PreferredCacheClusterAZs.AvailabilityZone.N&PreferredMaintenanceWindow=PreferredMaintenanceWindow&PrimaryClusterId=PrimaryClusterId&ReplicasPerNodeGroup=ReplicasPerNodeGroup&ReplicationGroupDescription=ReplicationGroupDescription&ReplicationGroupId=ReplicationGroupId&SecurityGroupIds.SecurityGroupId.N=SecurityGroupIds.SecurityGroupId.N&SnapshotArns.SnapshotArn.N=SnapshotArns.SnapshotArn.N&SnapshotName=SnapshotName&SnapshotRetentionLimit=SnapshotRetentionLimit&SnapshotWindow=SnapshotWindow&Tags.Tag.N=Tags.Tag.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a Redis (cluster mode disabled) or a Redis (cluster mode enabled) replication group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3733a5fb-8fb9-4bc3-921a-d199053482fe"
            }
          ]
        },
        {
          "id": "7b2ab2c9-e56e-40b4-a4b6-d18ca246fef7",
          "name": "deleteReplicationGroup",
          "request": {
            "url": "http://example.com/api/?Action=DeleteReplicationGroup?FinalSnapshotIdentifier=FinalSnapshotIdentifier&ReplicationGroupId=ReplicationGroupId&RetainPrimaryCluster=RetainPrimaryCluster",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes an existing replication group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fccffc57-3d1d-48a6-9875-880b3f65bcee"
            }
          ]
        },
        {
          "id": "460ac883-683e-4827-a6c7-114cffa74528",
          "name": "describeReplicationGroups",
          "request": {
            "url": "http://example.com/api/?Action=DescribeReplicationGroups?Marker=Marker&MaxRecords=MaxRecords&ReplicationGroupId=ReplicationGroupId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns information about a particular\n            replication group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f414be4e-45cd-46a7-80a3-5b0ece5f0dbb"
            }
          ]
        },
        {
          "id": "8e02b4e8-b95a-47cf-bd92-002e4e502951",
          "name": "modifyReplicationGroup",
          "request": {
            "url": "http://example.com/api/?Action=ModifyReplicationGroup?ApplyImmediately=ApplyImmediately&AutomaticFailoverEnabled=AutomaticFailoverEnabled&AutoMinorVersionUpgrade=AutoMinorVersionUpgrade&CacheNodeType=CacheNodeType&CacheParameterGroupName=CacheParameterGroupName&CacheSecurityGroupNames.CacheSecurityGroupName.N=CacheSecurityGroupNames.CacheSecurityGroupName.N&EngineVersion=EngineVersion&NotificationTopicArn=NotificationTopicArn&NotificationTopicStatus=NotificationTopicStatus&PreferredMaintenanceWindow=PreferredMaintenanceWindow&PrimaryClusterId=PrimaryClusterId&ReplicationGroupDescription=ReplicationGroupDescription&ReplicationGroupId=ReplicationGroupId&SecurityGroupIds.SecurityGroupId.N=SecurityGroupIds.SecurityGroupId.N&SnapshotRetentionLimit=SnapshotRetentionLimit&SnapshottingClusterId=SnapshottingClusterId&SnapshotWindow=SnapshotWindow",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Modifies the settings for a replication group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5dc46213-613c-4316-95b8-92b7e8697edf"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Engine Versions",
      "item": [
        {
          "id": "50b51c2f-8d60-42ef-a007-7581d5bcd0dc",
          "name": "describeCacheEngineVersions",
          "request": {
            "url": "http://example.com/api/?Action=DescribeCacheEngineVersions?CacheParameterGroupFamily=CacheParameterGroupFamily&DefaultOnly=DefaultOnly&Engine=Engine&EngineVersion=EngineVersion&Marker=Marker&MaxRecords=MaxRecords",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of the available cache\n            engines and their versions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0238e02d-06c8-4916-b186-b9b4e5b81afa"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Parameters",
      "item": [
        {
          "id": "6027c142-cc18-4650-ab05-5994c45fc0c2",
          "name": "describeCacheParameters",
          "request": {
            "url": "http://example.com/api/?Action=DescribeCacheParameters?CacheParameterGroupName=CacheParameterGroupName&Marker=Marker&MaxRecords=MaxRecords&Source=Source",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the detailed parameter list for a\n            particular cache parameter group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2d40c359-643a-40a2-88f4-26e64d12caf8"
            }
          ]
        }
      ]
    },
    {
      "name": "Engine Default Parameters",
      "item": [
        {
          "id": "af3382f3-0f98-49c4-99a8-c372cac3a042",
          "name": "describeEngineDefaultParameters",
          "request": {
            "url": "http://example.com/api/?Action=DescribeEngineDefaultParameters?CacheParameterGroupFamily=CacheParameterGroupFamily&Marker=Marker&MaxRecords=MaxRecords",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the default engine and\n            system parameter information for the specified cache engine."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "88dfe79a-3df4-45cb-bd91-c40aeb0e652d"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "8b916304-2e15-4d46-88b5-cc8c3e92c379",
          "name": "describeEvents",
          "request": {
            "url": "http://example.com/api/?Action=DescribeEvents?Duration=Duration&EndTime=EndTime&Marker=Marker&MaxRecords=MaxRecords&SourceIdentifier=SourceIdentifier&SourceType=SourceType&StartTime=StartTime",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns events related to cache clusters, cache\n            security groups, and cache parameter groups."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7000cbd5-7990-4af4-8dd7-51ed834b1b89"
            }
          ]
        }
      ]
    },
    {
      "name": "Reserved Cache Nodes",
      "item": [
        {
          "id": "6f7b96a1-9d41-41c4-8494-9473f6c92f3f",
          "name": "describeReservedCacheNodes",
          "request": {
            "url": "http://example.com/api/?Action=DescribeReservedCacheNodes?CacheNodeType=CacheNodeType&Duration=Duration&Marker=Marker&MaxRecords=MaxRecords&OfferingType=OfferingType&ProductDescription=ProductDescription&ReservedCacheNodeId=ReservedCacheNodeId&ReservedCacheNodesOfferingId=ReservedCacheNodesOfferingId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns information about reserved cache\n            nodes for this account, or about a specified reserved cache node."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f40a4774-26e2-4ad9-98ed-f360b3518a08"
            }
          ]
        },
        {
          "id": "14b84eb7-5511-4217-b497-7aca8b164d3e",
          "name": "describeReservedCacheNodesOfferings",
          "request": {
            "url": "http://example.com/api/?Action=DescribeReservedCacheNodesOfferings?CacheNodeType=CacheNodeType&Duration=Duration&Marker=Marker&MaxRecords=MaxRecords&OfferingType=OfferingType&ProductDescription=ProductDescription&ReservedCacheNodesOfferingId=ReservedCacheNodesOfferingId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists available reserved cache\n            node offerings."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7d9c0477-e2e0-42c1-8069-b5d1def131a9"
            }
          ]
        },
        {
          "id": "84fed21a-6c3a-4995-8488-12ff4ff86a73",
          "name": "purchaseReservedCacheNodesOffering",
          "request": {
            "url": "http://example.com/api/?Action=PurchaseReservedCacheNodesOffering?CacheNodeCount=CacheNodeCount&ReservedCacheNodeId=ReservedCacheNodeId&ReservedCacheNodesOfferingId=ReservedCacheNodesOfferingId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Allows you to purchase a reserved\n            cache node offering."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "43db931b-cb0e-4582-bda1-296d80c70798"
            }
          ]
        }
      ]
    },
    {
      "name": "Node Type Modifications",
      "item": [
        {
          "id": "969337f0-431a-4191-a48c-ed4befc1efcb",
          "name": "listAllowedNodeTypeModifications",
          "request": {
            "url": "http://example.com/api/?Action=ListAllowedNodeTypeModifications?CacheClusterId=CacheClusterId&ReplicationGroupId=ReplicationGroupId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists all available node types that you\n            can scale your Redis cluster's or replication group's current node type up to."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c93cb0a2-1815-4bd4-8207-f0654a35f27c"
            }
          ]
        }
      ]
    },
    {
      "name": "Node Types",
      "item": [
        {
          "id": "44a1c965-4216-4e70-83a8-42002be63433",
          "name": "listAvailableNodeTypes",
          "request": {
            "url": "http://example.com/api/?Action=ListAvailableNodeTypes?AvailableNodeTypes.member.N=AvailableNodeTypes.member.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "502ead42-fcc6-4fbc-9239-dddec6055a54"
            }
          ]
        }
      ]
    }
  ]
}