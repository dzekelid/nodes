{
  "info": {
    "name": "Amazon ElastiCache API Describe Reserved Cache Nodes",
    "_postman_id": "fe154b02-eaf9-49d0-9b50-c46a9abdfe35",
    "description": "Returns information about reserved cache\n            nodes for this account, or about a specified reserved cache node.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Resource Tags",
      "item": [
        {
          "id": "2bce4d08-43c8-4ab2-b04f-69f02d717c57",
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
              "id": "f6f2f7b9-748b-461f-88d6-3e241ae2f51b"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Security Groups",
      "item": [
        {
          "id": "57a05804-bc96-47f0-ab88-c75dc67ab255",
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
              "id": "7df64828-999c-4ce2-b448-0bdafea2fab3"
            }
          ]
        },
        {
          "id": "adf4b352-ad09-45bd-ad02-e9235aa60e10",
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
              "id": "830225fe-9aa3-4708-8900-7dfd94ff9a42"
            }
          ]
        },
        {
          "id": "d1bff28b-8924-40ef-b887-49d5bfc34e65",
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
              "id": "c5368e2e-ff6a-4b18-8394-8f9d041c4f61"
            }
          ]
        },
        {
          "id": "80a50dbd-b926-4019-bd38-16cddf28db33",
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
              "id": "622ed09a-a572-45fa-b9a2-aa2d8b0e04f9"
            }
          ]
        }
      ]
    },
    {
      "name": "Snapshots",
      "item": [
        {
          "id": "ca80e40c-758d-4919-a974-92f61b7ad849",
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
              "id": "825d98f1-6303-44cf-8ca2-5c825ed997e7"
            }
          ]
        },
        {
          "id": "97b80b83-959d-4ccb-8de1-bf50c31a2d5f",
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
              "id": "bee8783b-4617-42e0-827e-b344d55ab0a7"
            }
          ]
        },
        {
          "id": "d24eb161-5e59-4dbb-9195-984f4143822f",
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
              "id": "3c5c8c29-27c9-41f2-b485-e0482d454ca2"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Clusters",
      "item": [
        {
          "id": "ff74057e-17b9-4bdb-ac98-782b369b5b50",
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
              "id": "c5435112-0afd-4919-8bbe-aa93928fff26"
            }
          ]
        },
        {
          "id": "8a029fb7-43a4-44e1-954d-1e905f2c0802",
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
              "id": "f9497c7b-7038-4bca-8ae2-9bd2477fe65f"
            }
          ]
        },
        {
          "id": "ea2f0828-8a27-4c4a-8e65-06490faa4550",
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
              "id": "99564cef-a9b8-4b4a-9df3-30c69504f462"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Parameter Groups",
      "item": [
        {
          "id": "f43779c9-3397-496a-b98e-237f80e5112a",
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
              "id": "c861e35e-d85e-456a-9575-e47464daa10e"
            }
          ]
        },
        {
          "id": "09e37d89-b3fc-4a36-8cdf-ae3db6274135",
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
              "id": "068016f7-27d2-4d8b-a4f9-019e0c1a2a79"
            }
          ]
        },
        {
          "id": "5ca3c44e-2c3d-4cc6-bb0c-b591175a304f",
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
              "id": "9325dd57-9335-46ca-a758-d7d400d1a099"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Subnet Groups",
      "item": [
        {
          "id": "ddb11ad6-bf21-4f1f-954a-348aa0b33a9c",
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
              "id": "a6121ce6-00e9-4e76-95d5-54203d893ca0"
            }
          ]
        },
        {
          "id": "b6568e61-2cad-49de-a0f9-d3781d025bf0",
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
              "id": "c0fcdb6a-1b76-432d-8934-38a3a2ec1597"
            }
          ]
        },
        {
          "id": "82d96e25-0957-42af-a79d-55e005f5977f",
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
              "id": "7932b3f9-93b2-4867-910e-d9b673714e4a"
            }
          ]
        }
      ]
    },
    {
      "name": "Replication Groups",
      "item": [
        {
          "id": "46448427-97c5-40a7-939a-0f23b29e3e68",
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
              "id": "48b5d9f0-2866-4d2d-a670-b9e2478cb378"
            }
          ]
        },
        {
          "id": "672ed07e-21e6-4ca9-93e6-db7f28c4d4e9",
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
              "id": "fd34ee0f-74e3-4c8f-989e-1766f66dd39b"
            }
          ]
        },
        {
          "id": "ac948dae-1e93-4957-aeab-e6a612eab567",
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
              "id": "fca07fff-fad1-4da9-99f4-ace5b4ba6d46"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Engine Versions",
      "item": [
        {
          "id": "7812b41e-7f06-4ccf-9b3d-90f317d2ebf0",
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
              "id": "d0c7ba4e-4bbd-46d2-90ef-242eee007163"
            }
          ]
        }
      ]
    },
    {
      "name": "Cache Parameters",
      "item": [
        {
          "id": "52dffc51-66f2-432f-b778-666adaa1d9d5",
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
              "id": "bfd13f71-e44d-4030-8e16-3b277b2109cf"
            }
          ]
        }
      ]
    },
    {
      "name": "Engine Default Parameters",
      "item": [
        {
          "id": "33ade27d-5bf0-4712-878e-d3a9fa782dc6",
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
              "id": "5ff64c97-4743-475c-b8e4-b9f98dc79623"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "74172f4a-f848-42f6-83b6-95ca9d739aca",
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
              "id": "0ffd29b4-0284-4046-b9b1-b647a8f01455"
            }
          ]
        }
      ]
    },
    {
      "name": "Reserved Cache Nodes",
      "item": [
        {
          "id": "a7984fd6-efb0-4ea1-ba5f-d20d58793179",
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
              "id": "2a720923-495b-48e4-b8f7-458162c21d8a"
            }
          ]
        }
      ]
    }
  ]
}