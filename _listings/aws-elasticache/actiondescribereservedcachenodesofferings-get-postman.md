{
  "info": {
    "name": "Amazon ElastiCache API Describe Reserved Cache Nodes Offerings",
    "_postman_id": "47e066d0-605e-4800-b0af-8df46de398df",
    "description": "Lists available reserved cache\n            node offerings.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Resource Tags",
      "item": [
        {
          "id": "c405d607-4310-4abc-82b8-63b3c804d8f2",
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
              "id": "7685c2e4-1064-4b67-b8f2-3f164a5bd188"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Security Groups",
      "item": [
        {
          "id": "d531294c-28d0-4509-bddd-7297476a8663",
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
              "id": "6f0a9541-3af2-4bdc-a24a-6c7fc5de0b2d"
            }
          ]
        },
        {
          "id": "bdbdde2d-a617-4dfb-8fb4-76316f5fdd3f",
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
              "id": "5be87484-6b18-4cae-9838-db5eac7367af"
            }
          ]
        },
        {
          "id": "66f52d28-7a08-46ef-90ef-197600618e95",
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
              "id": "47cfe877-4fde-4549-b0e1-c06ffd26d1ad"
            }
          ]
        },
        {
          "id": "06e00f76-547c-469b-812f-00951022f1f7",
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
              "id": "6f0d42b4-4fab-4709-92dd-c774da714d97"
            }
          ]
        }
      ]
    },
    {
      "name": "Snapshots",
      "item": [
        {
          "id": "6d1e262c-44f8-4427-b4f2-749ed2fc758b",
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
              "id": "36f1f4f0-6961-45f8-ab32-6e764b521f8e"
            }
          ]
        },
        {
          "id": "cf19b27f-6232-4d9f-8e77-d42710210cd0",
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
              "id": "76114d4e-bfcb-4daf-9dea-ab6d3ad9add3"
            }
          ]
        },
        {
          "id": "2dc91b80-e9ac-4cec-8ae4-1055a7b213a1",
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
              "id": "4d2ae75d-a083-4914-bf81-a6195579d4e1"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Clusters",
      "item": [
        {
          "id": "6033c3a9-db23-47d2-841b-9de75ec65eb1",
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
              "id": "af636a0a-6999-4f92-9035-6a255e68a647"
            }
          ]
        },
        {
          "id": "90611ade-cbb0-46c4-a602-440f5ebb9776",
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
              "id": "61913958-071f-4de9-90cd-1d4ee87d7306"
            }
          ]
        },
        {
          "id": "ba20337f-48a8-4853-9713-e05a11bcda95",
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
              "id": "8f4ffb68-cf32-42e9-b1c6-6a873789a744"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Parameter Groups",
      "item": [
        {
          "id": "1e519f13-6e93-4740-b1f5-0ff9463a2a97",
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
              "id": "dd373d9c-e572-4730-abab-e8458ec44c6d"
            }
          ]
        },
        {
          "id": "c40aa6a6-e0a9-470e-9b4e-218ebdd74fd7",
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
              "id": "c64516ac-af00-4026-a718-50b4f10dfeb1"
            }
          ]
        },
        {
          "id": "8fbc9000-2b6c-4fa4-9c55-01a18dc1dfdf",
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
              "id": "c3a209c6-9bc0-4eaf-81d4-b21b7c0713d5"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Subnet Groups",
      "item": [
        {
          "id": "ee059d7e-d730-4108-9e2e-2d3cc93708ea",
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
              "id": "a6e7a353-250f-4c08-b9cd-4b82211dd526"
            }
          ]
        },
        {
          "id": "95506315-b429-4aa8-9ffd-affb5b75b9c3",
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
              "id": "4263adbf-5fc0-4381-847e-34d2d99d091a"
            }
          ]
        },
        {
          "id": "e57e9882-f336-4330-8206-6b8a8c0526ab",
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
              "id": "bd3c90ad-327c-450e-aaab-f4194e305b02"
            }
          ]
        }
      ]
    },
    {
      "name": "Replication Groups",
      "item": [
        {
          "id": "49e42672-029a-4e9a-8f88-967f49f44c90",
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
              "id": "c5b8113c-3027-4eb2-8bbc-efd8af59f3d5"
            }
          ]
        },
        {
          "id": "6621bc3e-d80d-42b9-a161-241b498c3751",
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
              "id": "ef4a4821-712b-42bf-bdaa-23f18f3d2dc0"
            }
          ]
        },
        {
          "id": "00674bc7-716a-4d3c-a9d0-fc37d14fade8",
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
              "id": "20f8831e-ca7b-4fe3-acca-742c68c892f8"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Engine Versions",
      "item": [
        {
          "id": "a8784b6f-9cbe-4fb1-aa65-8c6d6713f62b",
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
              "id": "070bc353-7a23-4405-94a7-85e303b910d6"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Parameters",
      "item": [
        {
          "id": "3d905259-910b-4ee2-ae1b-e2ece0230475",
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
              "id": "6b52a428-c132-44a4-ba86-e3e239f80112"
            }
          ]
        }
      ]
    },
    {
      "name": "Engine Default Parameters",
      "item": [
        {
          "id": "cc1daf2a-4725-49af-9abf-da0d3c52957c",
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
              "id": "376889ef-48b3-43ae-8622-5447606d4fd1"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "f9cc143e-dc34-400a-a4a5-846411975d2e",
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
              "id": "593bf7c3-fdd4-430f-baf1-a2654b08616c"
            }
          ]
        }
      ]
    },
    {
      "name": "Reserved Cache Nodes",
      "item": [
        {
          "id": "4bbb942d-e5ac-4f0f-a0cf-061198c138da",
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
              "id": "756bd7d5-f196-430e-9408-70e16e053eb2"
            }
          ]
        },
        {
          "id": "b8b0c58a-e31f-4f93-a56e-aa4e8e5354da",
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
              "id": "60dab0ee-988f-4838-9c1c-ce8589345481"
            }
          ]
        }
      ]
    }
  ]
}