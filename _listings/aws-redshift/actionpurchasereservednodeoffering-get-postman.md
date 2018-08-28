{
  "info": {
    "name": "Amazon Redshift API Purchase Reserved Node Offering",
    "_postman_id": "3ebe931a-6219-4f18-afdc-216f7c8501e0",
    "description": "Allows you to purchase reserved nodes.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Cluster Security Group",
      "item": [
        {
          "id": "faa57366-f06a-4bd3-ae73-74bca22406f4",
          "name": "authorizeClusterSecurityGroupIngress",
          "request": {
            "url": "http://example.com/api/?Action=AuthorizeClusterSecurityGroupIngress?CIDRIP=CIDRIP&ClusterSecurityGroupName=ClusterSecurityGroupName&EC2SecurityGroupName=EC2SecurityGroupName&EC2SecurityGroupOwnerId=EC2SecurityGroupOwnerId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Adds an inbound (ingress) rule to an Amazon Redshift security group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "722cdac9-840e-4962-84ef-86b5f0d6ae96"
            }
          ]
        },
        {
          "id": "cff9c37f-d655-45cc-9195-92fa8ebb5365",
          "name": "createClusterSecurityGroup",
          "request": {
            "url": "http://example.com/api/?Action=CreateClusterSecurityGroup?ClusterSecurityGroupName=ClusterSecurityGroupName&Description=Description&Tags.Tag.N=Tags.Tag.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new Amazon Redshift security group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "373db0b6-1dc4-452c-bbba-4ab05a6fdc1a"
            }
          ]
        },
        {
          "id": "768ed32c-18b1-4714-844b-8a557b918029",
          "name": "deleteClusterSecurityGroup",
          "request": {
            "url": "http://example.com/api/?Action=DeleteClusterSecurityGroup?ClusterSecurityGroupName=ClusterSecurityGroupName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes an Amazon Redshift security group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "13f948ae-12c0-430a-8c37-3c8ad8569256"
            }
          ]
        },
        {
          "id": "ca4817f3-b82d-40e5-b316-a3ff5db70275",
          "name": "describeClusterSecurityGroups",
          "request": {
            "url": "http://example.com/api/?Action=DescribeClusterSecurityGroups?ClusterSecurityGroupName=ClusterSecurityGroupName&Marker=Marker&MaxRecords=MaxRecords&TagKeys.TagKey.N=TagKeys.TagKey.N&TagValues.TagValue.N=TagValues.TagValue.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns information about Amazon Redshift security groups."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cb1f5fc2-0352-465a-85d0-772c1ec8dc8c"
            }
          ]
        }
      ]
    },
    {
      "name": "Snapshots",
      "item": [
        {
          "id": "172c27f9-b1e3-41b4-84d6-e3031c1257ad",
          "name": "authorizeSnapshotAccess",
          "request": {
            "url": "http://example.com/api/?Action=AuthorizeSnapshotAccess?AccountWithRestoreAccess=AccountWithRestoreAccess&SnapshotClusterIdentifier=SnapshotClusterIdentifier&SnapshotIdentifier=SnapshotIdentifier",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Authorizes the specified AWS customer account to restore the specified\n            snapshot."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c55f79a0-12a1-443c-bd15-df5d6778de81"
            }
          ]
        },
        {
          "id": "cd87218c-6ffe-44dd-a8c0-5fdbaa7a4ad9",
          "name": "copyClusterSnapshot",
          "request": {
            "url": "http://example.com/api/?Action=CopyClusterSnapshot?SourceSnapshotClusterIdentifier=SourceSnapshotClusterIdentifier&SourceSnapshotIdentifier=SourceSnapshotIdentifier&TargetSnapshotIdentifier=TargetSnapshotIdentifier",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Copies the specified automated cluster snapshot to a new manual cluster snapshot."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d84a7a1c-21bf-4ed7-a27e-049b82b8e228"
            }
          ]
        },
        {
          "id": "d14ba487-59a9-429c-ad26-6362b318a83d",
          "name": "createClusterSnapshot",
          "request": {
            "url": "http://example.com/api/?Action=CreateClusterSnapshot?ClusterIdentifier=ClusterIdentifier&SnapshotIdentifier=SnapshotIdentifier&Tags.Tag.N=Tags.Tag.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a manual snapshot of the specified cluster."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8823ce21-ea1c-4491-a2a1-656777aed3b8"
            }
          ]
        },
        {
          "id": "0c7ac355-91b5-4709-bc3c-06346a3c3054",
          "name": "createSnapshotCopyGrant",
          "request": {
            "url": "http://example.com/api/?Action=CreateSnapshotCopyGrant?KmsKeyId=KmsKeyId&SnapshotCopyGrantName=SnapshotCopyGrantName&Tags.Tag.N=Tags.Tag.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a snapshot copy grant that permits Amazon Redshift to use a customer master key\n            (CMK) from AWS Key Management Service (AWS KMS) to encrypt copied snapshots in a\n            destination region."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "848d48b0-56e4-4c86-98f4-2ce68ca3b48c"
            }
          ]
        },
        {
          "id": "3783ad9d-b51e-4ed2-9984-3837f3660900",
          "name": "deleteClusterSnapshot",
          "request": {
            "url": "http://example.com/api/?Action=DeleteClusterSnapshot?SnapshotClusterIdentifier=SnapshotClusterIdentifier&SnapshotIdentifier=SnapshotIdentifier",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes the specified manual snapshot."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7d9d1f80-7e39-4d90-81c6-da61aa059935"
            }
          ]
        },
        {
          "id": "d8973d99-be50-4ce4-833c-a5893c946d59",
          "name": "deleteSnapshotCopyGrant",
          "request": {
            "url": "http://example.com/api/?Action=DeleteSnapshotCopyGrant?SnapshotCopyGrantName=SnapshotCopyGrantName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes the specified snapshot copy grant."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "08283742-e4a5-4b5c-8d94-e0d77a39c97c"
            }
          ]
        },
        {
          "id": "d37d3113-964d-4cc9-b274-6801dd222e46",
          "name": "describeClusterSnapshots",
          "request": {
            "url": "http://example.com/api/?Action=DescribeClusterSnapshots?ClusterIdentifier=ClusterIdentifier&EndTime=EndTime&Marker=Marker&MaxRecords=MaxRecords&OwnerAccount=OwnerAccount&SnapshotIdentifier=SnapshotIdentifier&SnapshotType=SnapshotType&StartTime=StartTime&TagKeys.TagKey.N=TagKeys.TagKey.N&TagValues.TagValue.N=TagValues.TagValue.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns one or more snapshot objects, which contain metadata about your cluster\n            snapshots."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "095ed93e-5409-41ab-8008-81f5887ee6cf"
            }
          ]
        },
        {
          "id": "a37e95a5-4a65-4bf3-83b7-b9606a4c7362",
          "name": "describeSnapshotCopyGrants",
          "request": {
            "url": "http://example.com/api/?Action=DescribeSnapshotCopyGrants?Marker=Marker&MaxRecords=MaxRecords&SnapshotCopyGrantName=SnapshotCopyGrantName&TagKeys.TagKey.N=TagKeys.TagKey.N&TagValues.TagValue.N=TagValues.TagValue.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of snapshot copy grants owned by the AWS account in the destination\n            region."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "02f0b351-2a54-4d22-ac3b-ba1b5467a96b"
            }
          ]
        },
        {
          "id": "43c16770-3772-4b86-8e25-93741eb948b4",
          "name": "disableSnapshotCopy",
          "request": {
            "url": "http://example.com/api/?Action=DisableSnapshotCopy?ClusterIdentifier=ClusterIdentifier",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Disables the automatic copying of snapshots from one region to another region for a\n            specified cluster."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "58e5dcc4-cf26-46b7-8ebf-04c71cd1cd96"
            }
          ]
        },
        {
          "id": "50ba92c4-f643-4f13-a6fe-17b81d61cf1d",
          "name": "enableSnapshotCopy",
          "request": {
            "url": "http://example.com/api/?Action=EnableSnapshotCopy?ClusterIdentifier=ClusterIdentifier&DestinationRegion=DestinationRegion&RetentionPeriod=RetentionPeriod&SnapshotCopyGrantName=SnapshotCopyGrantName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Enables the automatic copy of snapshots from one region to another region for a\n            specified cluster."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "602c6257-2c84-42a0-bad7-46f7a3be02a3"
            }
          ]
        },
        {
          "id": "dd110f2c-79fe-491d-8f69-256fd7cc5d3b",
          "name": "modifySnapshotCopyRetentionPeriod",
          "request": {
            "url": "http://example.com/api/?Action=ModifySnapshotCopyRetentionPeriod?ClusterIdentifier=ClusterIdentifier&RetentionPeriod=RetentionPeriod",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Modifies the number of days to retain automated snapshots in the destination region\n            after they are copied from the source region."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c25e6a0d-01a8-4b17-9e5d-4e540a0799e8"
            }
          ]
        }
      ]
    },
    {
      "name": "Clusters",
      "item": [
        {
          "id": "5a4ace38-9222-457e-b240-c2b62d8bdd54",
          "name": "createCluster",
          "request": {
            "url": "http://example.com/api/?Action=CreateCluster?AdditionalInfo=AdditionalInfo&AllowVersionUpgrade=AllowVersionUpgrade&AutomatedSnapshotRetentionPeriod=AutomatedSnapshotRetentionPeriod&AvailabilityZone=AvailabilityZone&ClusterIdentifier=ClusterIdentifier&ClusterParameterGroupName=ClusterParameterGroupName&ClusterSecurityGroups.ClusterSecurityGroupName.N=ClusterSecurityGroups.ClusterSecurityGroupName.N&ClusterSubnetGroupName=ClusterSubnetGroupName&ClusterType=ClusterType&ClusterVersion=ClusterVersion&DBName=DBName&ElasticIp=ElasticIp&Encrypted=Encrypted&EnhancedVpcRouting=EnhancedVpcRouting&HsmClientCertificateIdentifier=HsmClientCertificateIdentifier&HsmConfigurationIdentifier=HsmConfigurationIdentifier&IamRoles.IamRoleArn.N=IamRoles.IamRoleArn.N&KmsKeyId=KmsKeyId&MasterUsername=MasterUsername&MasterUserPassword=MasterUserPassword&NodeType=NodeType&NumberOfNodes=NumberOfNodes&Port=Port&PreferredMaintenanceWindow=PreferredMaintenanceWindow&PubliclyAccessible=PubliclyAccessible&Tags.Tag.N=Tags.Tag.N&VpcSecurityGroupIds.VpcSecurityGroupId.N=VpcSecurityGroupIds.VpcSecurityGroupId.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new cluster."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "496bb9e5-a266-4326-88cf-f4c0ccb6e015"
            }
          ]
        },
        {
          "id": "cad9e887-fb17-4cb3-aad2-8f5ab4dea25b",
          "name": "deleteCluster",
          "request": {
            "url": "http://example.com/api/?Action=DeleteCluster?ClusterIdentifier=ClusterIdentifier&FinalClusterSnapshotIdentifier=FinalClusterSnapshotIdentifier&SkipFinalClusterSnapshot=SkipFinalClusterSnapshot",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a previously provisioned cluster."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "00386375-45ce-44a9-9eb3-01b91583aac8"
            }
          ]
        },
        {
          "id": "e0b173a3-3c3b-4f72-8a99-1a1dc51e2cea",
          "name": "describeClusters",
          "request": {
            "url": "http://example.com/api/?Action=DescribeClusters?ClusterIdentifier=ClusterIdentifier&Marker=Marker&MaxRecords=MaxRecords&TagKeys.TagKey.N=TagKeys.TagKey.N&TagValues.TagValue.N=TagValues.TagValue.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns properties of provisioned clusters including general cluster properties,\n            cluster database properties, maintenance and backup properties, and security and access\n            properties."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7187400a-47e5-4e19-a2fc-b2dc9f3e718c"
            }
          ]
        },
        {
          "id": "7754688b-66b2-4365-a56f-fd50c87a3d4d",
          "name": "describeClusterVersions",
          "request": {
            "url": "http://example.com/api/?Action=DescribeClusterVersions?ClusterParameterGroupFamily=ClusterParameterGroupFamily&ClusterVersion=ClusterVersion&Marker=Marker&MaxRecords=MaxRecords",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns descriptions of the available Amazon Redshift cluster versions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1f7ed32c-2737-4d12-b7df-646f83687561"
            }
          ]
        },
        {
          "id": "ea3425f2-fd9d-43b3-82a0-f79399c2d9ad",
          "name": "modifyCluster",
          "request": {
            "url": "http://example.com/api/?Action=ModifyCluster?AllowVersionUpgrade=AllowVersionUpgrade&AutomatedSnapshotRetentionPeriod=AutomatedSnapshotRetentionPeriod&ClusterIdentifier=ClusterIdentifier&ClusterParameterGroupName=ClusterParameterGroupName&ClusterSecurityGroups.ClusterSecurityGroupName.N=ClusterSecurityGroups.ClusterSecurityGroupName.N&ClusterType=ClusterType&ClusterVersion=ClusterVersion&ElasticIp=ElasticIp&EnhancedVpcRouting=EnhancedVpcRouting&HsmClientCertificateIdentifier=HsmClientCertificateIdentifier&HsmConfigurationIdentifier=HsmConfigurationIdentifier&MasterUserPassword=MasterUserPassword&NewClusterIdentifier=NewClusterIdentifier&NodeType=NodeType&NumberOfNodes=NumberOfNodes&PreferredMaintenanceWindow=PreferredMaintenanceWindow&PubliclyAccessible=PubliclyAccessible&VpcSecurityGroupIds.VpcSecurityGroupId.N=VpcSecurityGroupIds.VpcSecurityGroupId.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Modifies the settings for a cluster."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "358d2e12-7f96-4a7f-8566-668fd27a4b35"
            }
          ]
        }
      ]
    },
    {
      "name": "Cluster Parameter Groups",
      "item": [
        {
          "id": "cdc554c9-f84b-4eb0-8204-9fe585f1fe8e",
          "name": "createClusterParameterGroup",
          "request": {
            "url": "http://example.com/api/?Action=CreateClusterParameterGroup?Description=Description&ParameterGroupFamily=ParameterGroupFamily&ParameterGroupName=ParameterGroupName&Tags.Tag.N=Tags.Tag.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates an Amazon Redshift parameter group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "347a70e0-4541-4d4f-820b-0b7f66eb74de"
            }
          ]
        },
        {
          "id": "5f5b63da-f77c-4cc5-b165-f2855f49ad0b",
          "name": "deleteClusterParameterGroup",
          "request": {
            "url": "http://example.com/api/?Action=DeleteClusterParameterGroup?ParameterGroupName=ParameterGroupName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a specified Amazon Redshift parameter group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "745a1cfe-e513-449d-be36-cfdc8ff63d1c"
            }
          ]
        },
        {
          "id": "a64efbc8-b925-474d-9299-57dd676f239d",
          "name": "describeClusterParameterGroups",
          "request": {
            "url": "http://example.com/api/?Action=DescribeClusterParameterGroups?Marker=Marker&MaxRecords=MaxRecords&ParameterGroupName=ParameterGroupName&TagKeys.TagKey.N=TagKeys.TagKey.N&TagValues.TagValue.N=TagValues.TagValue.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of Amazon Redshift parameter groups, including parameter groups you\n            created and the default parameter group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "875080dd-ef38-48f4-8b3c-87c91a164d89"
            }
          ]
        },
        {
          "id": "92db42ab-6fb4-4f15-a56a-dc1427e9a1a3",
          "name": "modifyClusterParameterGroup",
          "request": {
            "url": "http://example.com/api/?Action=ModifyClusterParameterGroup?ParameterGroupName=ParameterGroupName&Parameters.Parameter.N=Parameters.Parameter.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Modifies the parameters of a parameter group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a44a60ad-c24a-4eaf-8a48-d479da96abc5"
            }
          ]
        }
      ]
    },
    {
      "name": "Cluster Subnet Groups",
      "item": [
        {
          "id": "2d0244f5-5fb0-48d0-aba5-3f39b852489b",
          "name": "createClusterSubnetGroup",
          "request": {
            "url": "http://example.com/api/?Action=CreateClusterSubnetGroup?ClusterSubnetGroupName=ClusterSubnetGroupName&Description=Description&SubnetIds.SubnetIdentifier.N=SubnetIds.SubnetIdentifier.N&Tags.Tag.N=Tags.Tag.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new Amazon Redshift subnet group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "67dcd26e-5691-4a67-965d-26cb60062812"
            }
          ]
        },
        {
          "id": "79380eec-3b6f-40c2-8a92-3acd2a1b3612",
          "name": "deleteClusterSubnetGroup",
          "request": {
            "url": "http://example.com/api/?Action=DeleteClusterSubnetGroup?ClusterSubnetGroupName=ClusterSubnetGroupName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes the specified cluster subnet group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ea022696-fd62-472b-9dad-d34b890a2b35"
            }
          ]
        },
        {
          "id": "0c03ed0a-28b3-4486-b17d-6445d0b1092b",
          "name": "describeClusterSubnetGroups",
          "request": {
            "url": "http://example.com/api/?Action=DescribeClusterSubnetGroups?ClusterSubnetGroupName=ClusterSubnetGroupName&Marker=Marker&MaxRecords=MaxRecords&TagKeys.TagKey.N=TagKeys.TagKey.N&TagValues.TagValue.N=TagValues.TagValue.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns one or more cluster subnet group objects, which contain metadata about your\n            cluster subnet groups."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "25986590-b68e-4404-ba61-dc91485b3315"
            }
          ]
        },
        {
          "id": "5e9128f1-6af1-4f38-878a-ada09d189c14",
          "name": "modifyClusterSubnetGroup",
          "request": {
            "url": "http://example.com/api/?Action=ModifyClusterSubnetGroup?ClusterSubnetGroupName=ClusterSubnetGroupName&Description=Description&SubnetIds.SubnetIdentifier.N=SubnetIds.SubnetIdentifier.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Modifies a cluster subnet group to include the specified list of VPC subnets."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ffaf3c5b-a57a-48f7-8eda-dd561c9173be"
            }
          ]
        }
      ]
    },
    {
      "name": "Event Subscriptions",
      "item": [
        {
          "id": "45176245-6935-4573-9495-51c31b0075dc",
          "name": "createEventSubscription",
          "request": {
            "url": "http://example.com/api/?Action=CreateEventSubscription?Enabled=Enabled&EventCategories.EventCategory.N=EventCategories.EventCategory.N&Severity=Severity&SnsTopicArn=SnsTopicArn&SourceIds.SourceId.N=SourceIds.SourceId.N&SourceType=SourceType&SubscriptionName=SubscriptionName&Tags.Tag.N=Tags.Tag.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates an Amazon Redshift event notification subscription."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "59cdf7b6-909c-4438-a5c7-47f173e70f0b"
            }
          ]
        },
        {
          "id": "0bc26f97-d58b-42f8-8aa2-beb107a69037",
          "name": "deleteEventSubscription",
          "request": {
            "url": "http://example.com/api/?Action=DeleteEventSubscription?SubscriptionName=SubscriptionName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes an Amazon Redshift event notification subscription."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "13ec9255-65da-489e-98f7-5d7360953d9f"
            }
          ]
        },
        {
          "id": "2b2e0e2c-8d94-45a2-b663-151c506fb335",
          "name": "describeEventSubscriptions",
          "request": {
            "url": "http://example.com/api/?Action=DescribeEventSubscriptions?Marker=Marker&MaxRecords=MaxRecords&SubscriptionName=SubscriptionName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists descriptions of all the Amazon Redshift event notifications subscription for a\n            customer account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1b048ce3-77a6-4587-be99-65a1f5f193c3"
            }
          ]
        },
        {
          "id": "de877991-b54d-4fe9-9d21-e33bfc426935",
          "name": "modifyEventSubscription",
          "request": {
            "url": "http://example.com/api/?Action=ModifyEventSubscription?Enabled=Enabled&EventCategories.EventCategory.N=EventCategories.EventCategory.N&Severity=Severity&SnsTopicArn=SnsTopicArn&SourceIds.SourceId.N=SourceIds.SourceId.N&SourceType=SourceType&SubscriptionName=SubscriptionName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Modifies an existing Amazon Redshift event notification subscription."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "28f310a7-aa22-497e-8390-d0ca6f36b60f"
            }
          ]
        }
      ]
    },
    {
      "name": "HSM Client Certificates",
      "item": [
        {
          "id": "5e979f79-fe5a-4004-9a85-7cd6854fd426",
          "name": "createHsmClientCertificate",
          "request": {
            "url": "http://example.com/api/?Action=CreateHsmClientCertificate?HsmClientCertificateIdentifier=HsmClientCertificateIdentifier&Tags.Tag.N=Tags.Tag.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates an HSM client certificate that an Amazon Redshift cluster will use to connect to\n            the client's HSM in order to store and retrieve the keys used to encrypt the cluster\n            databases."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f35c485c-901b-4165-b2e7-ab929b56c18d"
            }
          ]
        },
        {
          "id": "1ba3eab2-1399-44a7-854e-80b73d26069d",
          "name": "deleteHsmClientCertificate",
          "request": {
            "url": "http://example.com/api/?Action=DeleteHsmClientCertificate?HsmClientCertificateIdentifier=HsmClientCertificateIdentifier",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes the specified HSM client certificate."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1cd6779f-7b69-4b4b-82a1-df25158537d8"
            }
          ]
        },
        {
          "id": "fc79b0cd-85a7-4434-94af-adf001ddc927",
          "name": "describeHsmClientCertificates",
          "request": {
            "url": "http://example.com/api/?Action=DescribeHsmClientCertificates?HsmClientCertificateIdentifier=HsmClientCertificateIdentifier&Marker=Marker&MaxRecords=MaxRecords&TagKeys.TagKey.N=TagKeys.TagKey.N&TagValues.TagValue.N=TagValues.TagValue.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns information about the specified HSM client certificate."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "456c364b-9370-4c5c-9476-915a9eafde1c"
            }
          ]
        }
      ]
    },
    {
      "name": "HSM Configurations",
      "item": [
        {
          "id": "ae7c2a04-be7a-4013-957d-f5dfca982f7a",
          "name": "createHsmConfiguration",
          "request": {
            "url": "http://example.com/api/?Action=CreateHsmConfiguration?Description=Description&HsmConfigurationIdentifier=HsmConfigurationIdentifier&HsmIpAddress=HsmIpAddress&HsmPartitionName=HsmPartitionName&HsmPartitionPassword=HsmPartitionPassword&HsmServerPublicCertificate=HsmServerPublicCertificate&Tags.Tag.N=Tags.Tag.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates an HSM configuration that contains the information required by an Amazon Redshift\n            cluster to store and use database encryption keys in a Hardware Security Module (HSM)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f23cf44a-bbf9-4cfc-ad02-c4ccf726f383"
            }
          ]
        },
        {
          "id": "6fabb459-d3b7-4a4e-b629-39b4a4c61eb2",
          "name": "deleteHsmConfiguration",
          "request": {
            "url": "http://example.com/api/?Action=DeleteHsmConfiguration?HsmConfigurationIdentifier=HsmConfigurationIdentifier",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes the specified Amazon Redshift HSM configuration."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bfe014d6-6b65-49a3-900f-4aeef2f42bde"
            }
          ]
        },
        {
          "id": "031b135d-9921-4426-91c7-e3b60e3f217a",
          "name": "describeHsmConfigurations",
          "request": {
            "url": "http://example.com/api/?Action=DescribeHsmConfigurations?HsmConfigurationIdentifier=HsmConfigurationIdentifier&Marker=Marker&MaxRecords=MaxRecords&TagKeys.TagKey.N=TagKeys.TagKey.N&TagValues.TagValue.N=TagValues.TagValue.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns information about the specified Amazon Redshift HSM configuration."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8b20aa51-cb2a-4583-8223-3bec29b8d9f6"
            }
          ]
        }
      ]
    },
    {
      "name": "Tags",
      "item": [
        {
          "id": "b0d6a13f-c727-4286-9f96-f859731e32df",
          "name": "createTags",
          "request": {
            "url": "http://example.com/api/?Action=CreateTags?ResourceName=ResourceName&Tags.Tag.N=Tags.Tag.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Adds one or more tags to a specified resource."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f1e94bba-9f12-4102-85ab-0035fc88ead0"
            }
          ]
        },
        {
          "id": "d8de85c4-cb79-439d-a521-8604735e7872",
          "name": "deleteTags",
          "request": {
            "url": "http://example.com/api/?Action=DeleteTags?ResourceName=ResourceName&TagKeys.TagKey.N=TagKeys.TagKey.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a tag or tags from a resource."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fe16d959-a157-44ae-a687-d22081fdea80"
            }
          ]
        },
        {
          "id": "67bfbc7b-426c-4cbc-b2e6-cf63331e23a1",
          "name": "describeTags",
          "request": {
            "url": "http://example.com/api/?Action=DescribeTags?Marker=Marker&MaxRecords=MaxRecords&ResourceName=ResourceName&ResourceType=ResourceType&TagKeys.TagKey.N=TagKeys.TagKey.N&TagValues.TagValue.N=TagValues.TagValue.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of tags."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "48832751-94b4-48f8-818f-9178b08ff19b"
            }
          ]
        }
      ]
    },
    {
      "name": "Cluster Parameters",
      "item": [
        {
          "id": "7d7b513d-f13a-4b58-b95b-52e112271574",
          "name": "describeClusterParameters",
          "request": {
            "url": "http://example.com/api/?Action=DescribeClusterParameters?Marker=Marker&MaxRecords=MaxRecords&ParameterGroupName=ParameterGroupName&Source=Source",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a detailed list of parameters contained within the specified Amazon Redshift\n            parameter group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3125a90b-3b6a-4aed-9d06-ba1a7da94e5e"
            }
          ]
        },
        {
          "id": "35b87f36-62f1-4985-aff6-133cc3c9dabe",
          "name": "describeDefaultClusterParameters",
          "request": {
            "url": "http://example.com/api/?Action=DescribeDefaultClusterParameters?Marker=Marker&MaxRecords=MaxRecords&ParameterGroupFamily=ParameterGroupFamily",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of parameter settings for the specified parameter group\n            family."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "db5b776d-5953-415a-bbac-b29d7a7f6ec5"
            }
          ]
        }
      ]
    },
    {
      "name": "Event Categories",
      "item": [
        {
          "id": "3c002b34-91c5-4b9f-959e-4bee9484a2bb",
          "name": "describeEventCategories",
          "request": {
            "url": "http://example.com/api/?Action=DescribeEventCategories?SourceType=SourceType",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Displays a list of event categories for all event source types, or for a specified\n            source type."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bc08f3dd-f481-4640-a273-e7ab6a7c6eef"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "7235969d-d54c-4c5a-85dc-20931ec0cf76",
          "name": "describeEvents",
          "request": {
            "url": "http://example.com/api/?Action=DescribeEvents?Duration=Duration&EndTime=EndTime&Marker=Marker&MaxRecords=MaxRecords&SourceIdentifier=SourceIdentifier&SourceType=SourceType&StartTime=StartTime",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns events related to clusters, security groups, snapshots, and parameter\n            groups for the past 14 days."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8aafe4bd-8e6b-4c27-acd3-44e7f95dd8ea"
            }
          ]
        }
      ]
    },
    {
      "name": "Logging",
      "item": [
        {
          "id": "e3441265-920a-43f1-8a03-a37c2403df35",
          "name": "describeLoggingStatus",
          "request": {
            "url": "http://example.com/api/?Action=DescribeLoggingStatus?ClusterIdentifier=ClusterIdentifier",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Describes whether information, such as queries and connection attempts, is being\n            logged for the specified Amazon Redshift cluster."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1847d71f-3fab-4b47-99ce-4a592c7bff1d"
            }
          ]
        },
        {
          "id": "d454fdc7-d555-4fe7-88fc-dfa034fb95b5",
          "name": "disableLogging",
          "request": {
            "url": "http://example.com/api/?Action=DisableLogging?ClusterIdentifier=ClusterIdentifier",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Stops logging information, such as queries and connection attempts, for the\n            specified Amazon Redshift cluster."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0ebc1845-04b3-442b-9c22-b0cec06e8f25"
            }
          ]
        },
        {
          "id": "5ca3ea7d-b54e-4fab-bac1-fb649960ee91",
          "name": "enableLogging",
          "request": {
            "url": "http://example.com/api/?Action=EnableLogging?BucketName=BucketName&ClusterIdentifier=ClusterIdentifier&S3KeyPrefix=S3KeyPrefix",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Starts logging information, such as queries and connection attempts, for the\n            specified Amazon Redshift cluster."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f0cbd712-a380-4129-a0e6-9c51c9395913"
            }
          ]
        }
      ]
    },
    {
      "name": "Cluster Options",
      "item": [
        {
          "id": "b4ec590a-9e8e-48fd-a2c5-5b664ed214ed",
          "name": "describeOrderableClusterOptions",
          "request": {
            "url": "http://example.com/api/?Action=DescribeOrderableClusterOptions?ClusterVersion=ClusterVersion&Marker=Marker&MaxRecords=MaxRecords&NodeType=NodeType",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of orderable cluster options."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b41b3754-71f7-4104-9cf9-9b5c74f99779"
            }
          ]
        }
      ]
    },
    {
      "name": "Reserved Nodes",
      "item": [
        {
          "id": "5f8fb1e2-d00d-4dc5-acb6-2f61a00ab8c8",
          "name": "describeReservedNodeOfferings",
          "request": {
            "url": "http://example.com/api/?Action=DescribeReservedNodeOfferings?Marker=Marker&MaxRecords=MaxRecords&ReservedNodeOfferingId=ReservedNodeOfferingId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of the available reserved node offerings by Amazon Redshift with their\n            descriptions including the node type, the fixed and recurring costs of reserving the\n            node and duration the node will be reserved for you."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7646fd22-5dcb-482d-bc81-a361909ab0c6"
            }
          ]
        },
        {
          "id": "ff386594-bee4-4ac3-b9eb-adc289e323c7",
          "name": "describeReservedNodes",
          "request": {
            "url": "http://example.com/api/?Action=DescribeReservedNodes?Marker=Marker&MaxRecords=MaxRecords&ReservedNodeId=ReservedNodeId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the descriptions of the reserved nodes."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dfdcba18-69b9-4958-bf86-84fe8470db77"
            }
          ]
        },
        {
          "id": "ab8f5dcd-b234-4938-8606-3819f1741482",
          "name": "purchaseReservedNodeOffering",
          "request": {
            "url": "http://example.com/api/?Action=PurchaseReservedNodeOffering?NodeCount=NodeCount&ReservedNodeOfferingId=ReservedNodeOfferingId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Allows you to purchase reserved nodes."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f2faa917-aa53-4354-b6d0-8bdd5f530278"
            }
          ]
        }
      ]
    },
    {
      "name": "Resize",
      "item": [
        {
          "id": "b1d4adeb-5aa6-451b-af90-cc9509864d08",
          "name": "describeResize",
          "request": {
            "url": "http://example.com/api/?Action=DescribeResize?ClusterIdentifier=ClusterIdentifier",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns information about the last resize operation for the specified cluster."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3a2ef2b2-e5ef-4357-ad36-eaa7fae53ef8"
            }
          ]
        }
      ]
    },
    {
      "name": "Tables",
      "item": [
        {
          "id": "1b5d4b06-4750-431e-ae77-e829d6e2669f",
          "name": "describeTableRestoreStatus",
          "request": {
            "url": "http://example.com/api/?Action=DescribeTableRestoreStatus?ClusterIdentifier=ClusterIdentifier&Marker=Marker&MaxRecords=MaxRecords&TableRestoreRequestId=TableRestoreRequestId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists the status of one or more table restore requests made using the."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5f44976b-8158-4c02-ae17-314362aeff62"
            }
          ]
        }
      ]
    },
    {
      "name": "Cluster IAM Roles",
      "item": [
        {
          "id": "2c9b8f8d-2e99-4c68-9998-c24935051a27",
          "name": "modifyClusterIamRoles",
          "request": {
            "url": "http://example.com/api/?Action=ModifyClusterIamRoles?AddIamRoles.IamRoleArn.N=AddIamRoles.IamRoleArn.N&ClusterIdentifier=ClusterIdentifier&RemoveIamRoles.IamRoleArn.N=RemoveIamRoles.IamRoleArn.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Modifies the list of AWS Identity and Access Management (IAM) roles that can be\n            used by the cluster to access other AWS services."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c376496c-c0ed-476a-bc6c-e6f085609a77"
            }
          ]
        }
      ]
    }
  ]
}