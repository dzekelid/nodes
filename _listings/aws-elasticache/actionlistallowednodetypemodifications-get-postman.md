{
  "info": {
    "name": "Amazon ElastiCache API List Allowed Node Type Modifications",
    "_postman_id": "bc967634-2707-4a1a-8602-26fb6af4e50a",
    "description": "Lists all available node types that you\n            can scale your Redis cluster's or replication group's current node type up to.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Resource Tags",
      "item": [
        {
          "id": "a38d1d55-9bf4-46ec-8e93-6a62ede06abc",
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
              "id": "940c7acd-aa13-4f1b-85a0-e6b60632771b"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Security Groups",
      "item": [
        {
          "id": "c4355876-eea3-4fd8-9212-7c41b44ab0fa",
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
              "id": "1bab3d37-0874-467a-be50-d9f6015ef9b6"
            }
          ]
        },
        {
          "id": "b97a83e2-3dd6-4dc2-999c-91397a7a8aa3",
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
              "id": "8405f9a4-e631-4d02-bcaa-d6dce71eff3b"
            }
          ]
        },
        {
          "id": "1b558869-23b2-425a-a079-bee91d6bbffa",
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
              "id": "b7cb04a2-7c71-4a9d-803e-39e7e5ed6bad"
            }
          ]
        },
        {
          "id": "724bc3d4-696b-4ef1-8f17-acd5bed432e4",
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
              "id": "fd9433f4-4c33-497b-b3be-4a1c51777841"
            }
          ]
        }
      ]
    },
    {
      "name": "Snapshots",
      "item": [
        {
          "id": "a8578e7b-5df4-4def-9c5a-c628feb6101b",
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
              "id": "27ddd987-5f66-4604-81c4-1cb6f8600adc"
            }
          ]
        },
        {
          "id": "d7fd1cd5-6242-4103-96cb-83614ecc4468",
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
              "id": "72376da8-646f-4e0a-ba2c-3b0e3485d21b"
            }
          ]
        },
        {
          "id": "5a6ce08c-8800-428f-bd27-ca4cfcb6726f",
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
              "id": "8af6aed6-a60a-468d-91bd-a3c8d3f840e1"
            }
          ]
        },
        {
          "id": "0730bea8-d6e7-49ae-88e0-2686a9d6e790",
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
              "id": "18a40c85-5d35-4e7d-920a-a875558b4f7e"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Clusters",
      "item": [
        {
          "id": "e91e4e72-bba4-497c-9b08-ca8b403f5699",
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
              "id": "84bf9e16-844e-4b3e-b667-b9e75d48244b"
            }
          ]
        },
        {
          "id": "2e43c536-697f-429c-9127-883cb2637c18",
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
              "id": "9bdce562-a5f7-4eb4-90da-48e250f48096"
            }
          ]
        },
        {
          "id": "ea7843e6-4f7f-4c58-bf76-29c01d0e27a2",
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
              "id": "26c8363a-9c7f-4990-a72f-3908ba8ac52c"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Parameter Groups",
      "item": [
        {
          "id": "a3f97fc9-563c-46c7-97e4-08dbdd831621",
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
              "id": "8019e4d9-c36c-4fef-ba20-2c70d8565a47"
            }
          ]
        },
        {
          "id": "0354f329-4b83-4488-8a61-d60ba319a93c",
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
              "id": "97074a16-21f3-4e3f-9245-42f5aae09e61"
            }
          ]
        },
        {
          "id": "57c3a945-574a-4bb8-af5d-84e2a35b88eb",
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
              "id": "5f7e4ccd-1c46-44a5-8d2c-ef61fb9c320e"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Subnet Groups",
      "item": [
        {
          "id": "90acd138-c5f8-49a9-b772-ac56da13975e",
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
              "id": "2d50452a-6a1e-4d66-88ad-e4c4052860c2"
            }
          ]
        },
        {
          "id": "cef2e774-ef52-455c-869c-2e4652da87cd",
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
              "id": "f494aec0-0e61-4a2e-9c83-2d70db577990"
            }
          ]
        },
        {
          "id": "cc911f2e-601d-4edb-adab-663b5972e01f",
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
              "id": "419c0077-b00d-47cc-9dc1-f0a9955aee7b"
            }
          ]
        }
      ]
    },
    {
      "name": "Replication Groups",
      "item": [
        {
          "id": "089e840c-faa2-4352-ad00-d9ba411ff1c9",
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
              "id": "093c0beb-8c99-4d4c-bdbf-ffab8dd4500d"
            }
          ]
        },
        {
          "id": "0f7fcc7e-22aa-4ec4-b7f6-2fc103a3e7e0",
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
              "id": "7e4487c2-5aa2-4ddd-abda-89e589bc1e30"
            }
          ]
        },
        {
          "id": "d87ed62e-c2ac-458d-bd58-f33d7cb1c880",
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
              "id": "0046e16f-6f83-46c5-809e-a69a02a1cce5"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Engine Versions",
      "item": [
        {
          "id": "7626b690-61d2-46c8-afd5-c288fbaa14e7",
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
              "id": "a90777d4-f78f-4901-89c4-128b7dfec662"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Parameters",
      "item": [
        {
          "id": "cc5f6d90-ccb6-4be5-9384-d7206609a765",
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
              "id": "47cc407a-3637-4d39-b79d-3bb947ef1649"
            }
          ]
        }
      ]
    },
    {
      "name": "Engine Default Parameters",
      "item": [
        {
          "id": "9d045ae6-3b78-446e-ab60-53ef0cb6e2e7",
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
              "id": "e4b39703-fe5c-46fc-a569-b22b3786e769"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "79a3b340-a590-49f1-9091-8829e4c2f00c",
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
              "id": "b48517c1-b3c0-4741-8794-42762c6d2b16"
            }
          ]
        }
      ]
    },
    {
      "name": "Reserved Cache Nodes",
      "item": [
        {
          "id": "2c2c4892-f1cc-48e8-8ba7-a5fe60aaa145",
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
              "id": "5c7017ce-d0fa-4de9-9da7-d889836f7040"
            }
          ]
        },
        {
          "id": "59227377-0b53-429e-b2ca-ac76062af3b0",
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
              "id": "1a08a67a-0878-459f-be44-86f3eb513943"
            }
          ]
        }
      ]
    },
    {
      "name": "Node Type Modifications",
      "item": [
        {
          "id": "2a054c72-7b0c-41bb-89f2-c0933ae9547d",
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
              "id": "7bc9819f-bdbf-43e1-b3f0-292a3349b046"
            }
          ]
        }
      ]
    }
  ]
}