{
  "info": {
    "name": "Amazon Redshift API Describe Reserved Node Offerings",
    "_postman_id": "9fc122e5-fe9b-424a-a7f0-e2891444d2fb",
    "description": "Returns a list of the available reserved node offerings by Amazon Redshift with their\n            descriptions including the node type, the fixed and recurring costs of reserving the\n            node and duration the node will be reserved for you.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Cluster Security Group",
      "item": [
        {
          "id": "f5253e06-e7c8-4970-91a6-c68abafb736d",
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
              "id": "ca241a69-1943-41e6-a91d-1b53c3953622"
            }
          ]
        },
        {
          "id": "4d971a56-3ae1-4995-b9f9-d23807743b65",
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
              "id": "dafd4e70-63cd-4eb5-ae07-2eb4d88fb5b6"
            }
          ]
        },
        {
          "id": "e2a953b4-35a3-40a3-820c-a97741ba556d",
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
              "id": "231e1447-e010-4da1-b30e-eeeb173a73e3"
            }
          ]
        },
        {
          "id": "2b3e5d26-2051-41e7-890f-71600b73eb3d",
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
              "id": "3c74e86f-8109-49d6-b04d-fb3e58995d02"
            }
          ]
        }
      ]
    },
    {
      "name": "Snapshots",
      "item": [
        {
          "id": "09a296bc-dd11-4d3f-99c3-09c515f3cb02",
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
              "id": "ea40f6f5-e75d-4fba-aa19-edd151ec5453"
            }
          ]
        },
        {
          "id": "3de9dbc4-89af-4cfd-b088-422754ad40b5",
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
              "id": "a4f8ca98-0f53-451d-8061-715f124f5ee2"
            }
          ]
        },
        {
          "id": "3a1a07b8-1ab5-41da-aef3-27c6d06fdae5",
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
              "id": "e1f65abb-dc32-4f54-9d79-e30a7b68b451"
            }
          ]
        },
        {
          "id": "082f5897-756e-4cfd-9202-218f1d89517e",
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
              "id": "785e9c2f-7679-4a83-87cc-23c7f19173a1"
            }
          ]
        },
        {
          "id": "59b65a4a-5ef6-4d7b-a859-9556339d71a6",
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
              "id": "076224b5-9457-458f-b162-51bfc0535dfe"
            }
          ]
        },
        {
          "id": "98119f02-a95d-4c34-9792-cc87e67a3a9f",
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
              "id": "388a1bc7-02d6-4a6d-9458-f29418b3c843"
            }
          ]
        },
        {
          "id": "87056e3b-c6ac-4a35-a0e2-49740bfd195e",
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
              "id": "208fe083-a188-42ff-9fa5-4f29b8d49f7c"
            }
          ]
        }
      ]
    },
    {
      "name": "Clusters",
      "item": [
        {
          "id": "28fd492a-6b69-484a-9027-e3d5ab76ef2c",
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
              "id": "4131ec30-0198-4ce6-8e5a-544fe3bcedaa"
            }
          ]
        },
        {
          "id": "597b376c-9269-4d7a-94e1-aee2caa6e27e",
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
              "id": "225dbfa5-12ed-41c7-a2e5-0a6174f9df6f"
            }
          ]
        },
        {
          "id": "651ee90c-8964-4f1d-858c-8746b0594e53",
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
              "id": "692f9297-02fc-4fc4-a269-769e0aa5a993"
            }
          ]
        },
        {
          "id": "fe5a8409-ced0-4977-b0d4-01a5c5f873f2",
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
              "id": "d7c3da5c-c6ad-4f20-8b63-4d3a439e6318"
            }
          ]
        }
      ]
    },
    {
      "name": "Cluster Parameter Groups",
      "item": [
        {
          "id": "04d8e13e-35a6-4786-a5fe-7974d5b9341c",
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
              "id": "7ca7495b-ae15-4aa2-bbba-09813e654404"
            }
          ]
        },
        {
          "id": "62fd9ed1-b7dc-426d-894b-b32dfeb7fb00",
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
              "id": "05f0512d-5877-4290-81da-26b9997bc72b"
            }
          ]
        },
        {
          "id": "773c8c41-1252-4e3b-bb77-d7f2b1c992e4",
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
              "id": "f1d34e38-a6d6-43ea-a8fd-3ee17aaf73f8"
            }
          ]
        }
      ]
    },
    {
      "name": "Cluster Subnet Groups",
      "item": [
        {
          "id": "b604a175-5408-4893-8cc7-6305aa487d8c",
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
              "id": "4db10ef8-4fb3-49ab-a004-17391b60540f"
            }
          ]
        },
        {
          "id": "be4a6fdc-9620-45d7-8b91-703541ee5dec",
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
              "id": "69c93b69-c7e0-472b-b899-09e8f89b24e8"
            }
          ]
        },
        {
          "id": "a49d3f96-1f8c-45d8-9aad-81e5fb532360",
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
              "id": "c48238ab-64d6-48af-85c7-ebde47220174"
            }
          ]
        }
      ]
    },
    {
      "name": "Event Subscriptions",
      "item": [
        {
          "id": "af3e0c60-a53d-4307-9a22-6ae0eba76fc2",
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
              "id": "eb1082ba-3144-4863-9d16-2b661cd75cda"
            }
          ]
        },
        {
          "id": "17524495-f83f-4af4-b9a2-4bb24d316c80",
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
              "id": "1001f5a5-0ffb-4159-a68c-902d2b0650fd"
            }
          ]
        },
        {
          "id": "7f387ab3-6b3d-49fd-aeb1-630fa8b001f1",
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
              "id": "eead659a-f4b8-44f1-9441-830d68268d92"
            }
          ]
        }
      ]
    },
    {
      "name": "HSM Client Certificates",
      "item": [
        {
          "id": "e9587386-ccda-4211-b170-c96b6b1c5d68",
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
              "id": "a9ba97fb-a1b9-4c11-b652-f1b4ad4aa994"
            }
          ]
        },
        {
          "id": "7158637b-3558-4ce1-8526-bfa325aef034",
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
              "id": "665c0361-5b37-4c1e-926a-b0d749becd74"
            }
          ]
        },
        {
          "id": "bbcdf187-ad6f-4e1a-85a6-9455204afe61",
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
              "id": "14157308-0942-41ac-b3c2-40e7ac2428a1"
            }
          ]
        }
      ]
    },
    {
      "name": "HSM Configurations",
      "item": [
        {
          "id": "5fa24062-20fe-4443-b296-cfd39d815758",
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
              "id": "6f135ef1-fa8d-4ab1-8acc-d9beef7edf0c"
            }
          ]
        },
        {
          "id": "34194806-36d2-4a03-9196-efa149fdd7b8",
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
              "id": "7c244cf5-a781-4e42-81a0-51eb3ed219da"
            }
          ]
        },
        {
          "id": "f11d09bc-383d-4356-8b2f-d5e974ba34b2",
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
              "id": "17dfbeb5-c6b5-49a4-92be-744390ac0098"
            }
          ]
        }
      ]
    },
    {
      "name": "Tags",
      "item": [
        {
          "id": "e8ee933d-08aa-448c-a7da-666bb34851e3",
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
              "id": "d6ed5f35-2f84-440a-b5db-fd5e7e1a19ab"
            }
          ]
        },
        {
          "id": "0ba8b5ac-50fa-4fc9-89d3-656b91c00666",
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
              "id": "23012e53-0554-4b88-a13e-5b04a5df2723"
            }
          ]
        }
      ]
    },
    {
      "name": "Cluster Parameters",
      "item": [
        {
          "id": "5d9722d2-33ef-410a-a191-d9ac10f460bf",
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
              "id": "9cffcc05-ffe8-42ca-b7b1-e14662e2ac2a"
            }
          ]
        },
        {
          "id": "860dc3ff-ff73-47dc-bfa1-825fd5959182",
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
              "id": "eb5b3b52-4b46-42a1-ae85-b7935b813bb6"
            }
          ]
        }
      ]
    },
    {
      "name": "Event Categories",
      "item": [
        {
          "id": "24c9a076-b51a-4d7a-828d-54c23f7d7e6d",
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
              "id": "ef7f0ecf-4dc4-4239-9ec7-1b1a33da67c8"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "2e96cac6-d871-443f-b902-ffa963a6c208",
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
              "id": "9a34d24c-058e-4bf5-ad4b-c8207e64c4e7"
            }
          ]
        }
      ]
    },
    {
      "name": "Logging",
      "item": [
        {
          "id": "07dfdaa2-1d07-4d22-8042-ae8ae6fe29c1",
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
              "id": "6abc5583-d50d-40cd-8b6d-3290fddacb8b"
            }
          ]
        }
      ]
    },
    {
      "name": "Cluster Options",
      "item": [
        {
          "id": "833e08ab-cf62-433e-bc2c-a84ace40960c",
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
              "id": "04c3aa28-cf4b-437a-b9b2-b787c17b786a"
            }
          ]
        }
      ]
    },
    {
      "name": "Reserved Nodes",
      "item": [
        {
          "id": "1a2a44e3-30f1-4b0a-9005-4eb1ee704b5b",
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
              "id": "48951aeb-81b9-4c38-8e27-6ee6336b5642"
            }
          ]
        }
      ]
    }
  ]
}