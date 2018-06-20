{
  "info": {
    "name": "Amazon Redshift API Describe Reserved Nodes",
    "_postman_id": "7bc437f2-24cb-4783-bc8f-ab7292eea410",
    "description": "Returns the descriptions of the reserved nodes.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Cluster Security Group",
      "item": [
        {
          "id": "e9098252-0583-40f3-a2a7-440d8c8c992f",
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
              "id": "4ce0e496-4853-4764-b230-df7444cfceaa"
            }
          ]
        },
        {
          "id": "33155db7-682f-4fd9-86d5-a617b2f5ef83",
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
              "id": "d11639d3-ff14-4284-8771-595207369f8e"
            }
          ]
        },
        {
          "id": "f2ccec11-3adf-4314-9f4f-f66dda38a41f",
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
              "id": "a3fe0502-d541-4c85-ba15-3b573ccd558d"
            }
          ]
        },
        {
          "id": "cbc7aa1c-544e-4099-9f1d-b95e613ea8b8",
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
              "id": "92fc925d-dd73-4b1d-b06f-6e4cd15cdaa9"
            }
          ]
        }
      ]
    },
    {
      "name": "Snapshots",
      "item": [
        {
          "id": "46d90a13-90d5-421b-8be5-7aa6da000830",
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
              "id": "fb1d6cb3-4d93-4592-99b6-6d299fb7707e"
            }
          ]
        },
        {
          "id": "4409ffda-ab1a-4846-9c6c-1ae8252a815f",
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
              "id": "1ec6f0b0-0f3f-4b04-8db1-a8b83ecb815f"
            }
          ]
        },
        {
          "id": "85e59ebc-2fbe-4b6b-8ef5-a109afa7ad87",
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
              "id": "6be43734-a9f9-435e-853f-25123e4af5b8"
            }
          ]
        },
        {
          "id": "3c767276-6315-4fa5-b613-898f74f92869",
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
              "id": "0a7edaf5-eb31-4c8a-9c35-f09dd72de729"
            }
          ]
        },
        {
          "id": "7ad0c63d-c774-4736-8f2a-0584d175a8d3",
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
              "id": "2dce9067-5e9e-432b-806c-ba4e2dfc2902"
            }
          ]
        },
        {
          "id": "61e7b935-de83-4096-b427-a3335d834a0f",
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
              "id": "3ba3d80a-6019-430a-b52d-c2e758dc95e1"
            }
          ]
        },
        {
          "id": "003fa8b4-ebea-4497-9951-42e292a9a065",
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
              "id": "4f678e0f-52a2-4c8e-8f41-7f249ad651df"
            }
          ]
        }
      ]
    },
    {
      "name": "Clusters",
      "item": [
        {
          "id": "691a1558-4222-484e-a799-4fd6bd9a72aa",
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
              "id": "e17839bc-c279-47bf-97c6-2a390189b124"
            }
          ]
        },
        {
          "id": "6ca7ef3a-1583-4f47-ada6-9f4c600d950a",
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
              "id": "770e429d-db26-4781-88a5-28313a386920"
            }
          ]
        },
        {
          "id": "d71189fe-0d42-476d-b37a-16886d65f92d",
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
              "id": "20e3da8e-b84b-4411-962f-ca1d87bc216b"
            }
          ]
        },
        {
          "id": "6dc2f3a0-7d0f-43b4-8520-81a35eb68ba1",
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
              "id": "ae2085b5-a0f9-4c2a-9e58-8b96da8a30ad"
            }
          ]
        }
      ]
    },
    {
      "name": "Cluster Parameter Groups",
      "item": [
        {
          "id": "fa447fc5-1dc0-44df-88dd-c4063d78bfce",
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
              "id": "5ab47e9a-5930-49e2-890c-36fe5c7e245d"
            }
          ]
        },
        {
          "id": "7e5290cb-9fa6-416e-a2b2-92bcf243ca57",
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
              "id": "431d8de3-4663-4e34-906d-5494400abb10"
            }
          ]
        },
        {
          "id": "44d20d26-55b2-4ea3-93ba-766b3cd8113f",
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
              "id": "6ee1bead-f1cc-4ecd-90f3-defb8363986b"
            }
          ]
        }
      ]
    },
    {
      "name": "Cluster Subnet Groups",
      "item": [
        {
          "id": "7cedd947-62d7-4b7c-bf92-74cf44f1fbd8",
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
              "id": "c5e0b193-9f8b-4f21-a632-ee55ac66885a"
            }
          ]
        },
        {
          "id": "8f7e22c4-80ba-40f9-b1db-70af5d3a9ac4",
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
              "id": "0ebdfdcb-cd66-4c20-a30a-d7f114fcc3ab"
            }
          ]
        },
        {
          "id": "687d0cd7-dc76-4325-a3c5-7618f159ccb8",
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
              "id": "5651c48a-ede9-4aeb-92bd-98563f2f4a50"
            }
          ]
        }
      ]
    },
    {
      "name": "Event Subscriptions",
      "item": [
        {
          "id": "a8b7720c-62de-41df-9178-10997ded8738",
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
              "id": "f6e201ac-c1e8-471c-a054-b79496794a0f"
            }
          ]
        },
        {
          "id": "39de11bd-4adc-40c7-bd44-f8f6be12c42a",
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
              "id": "69890b1c-4a25-44e9-b192-ebc02e0b8455"
            }
          ]
        },
        {
          "id": "04b311a1-305d-46b3-a8de-607b3cabba50",
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
              "id": "9f4c4289-867e-4aea-8453-f9ef42b1941d"
            }
          ]
        }
      ]
    },
    {
      "name": "HSM Client Certificates",
      "item": [
        {
          "id": "15fff25e-7d7c-4021-b7f8-f97722f4478c",
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
              "id": "59ac6283-d971-4141-83ab-daf84165a6bd"
            }
          ]
        },
        {
          "id": "2b4e5c5c-6958-47cc-988b-f4178f193280",
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
              "id": "cbf12953-34ed-40de-baaa-fb9098073c65"
            }
          ]
        },
        {
          "id": "694acc06-4f54-4004-a994-b11bf173a4c9",
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
              "id": "c6753de7-dc0c-431c-804c-3e1c100403ab"
            }
          ]
        }
      ]
    },
    {
      "name": "HSM Configurations",
      "item": [
        {
          "id": "b83a285e-9b14-4a9c-84d6-ae852b3ed1f9",
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
              "id": "2f7bf56c-38a0-4ffe-baf4-11d5b70c46cf"
            }
          ]
        },
        {
          "id": "a3a7d566-7069-46e9-9a10-94c7867fd4ba",
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
              "id": "8f6baf17-5388-44d1-92c0-532996ce3529"
            }
          ]
        },
        {
          "id": "9ff1a311-d51e-493b-acbf-53de574398fc",
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
              "id": "19e22b80-2ceb-4ff7-903e-2e702c5484f1"
            }
          ]
        }
      ]
    },
    {
      "name": "Tags",
      "item": [
        {
          "id": "fbbfc8a2-80c4-450c-ab99-4b3eac6ac54d",
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
              "id": "4290391a-1de9-484d-a6f3-4623b425d604"
            }
          ]
        },
        {
          "id": "a11f6a81-c47c-4772-aaff-d44fe54af101",
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
              "id": "632cd9b7-733f-4927-9510-4765b61120d8"
            }
          ]
        }
      ]
    },
    {
      "name": "Cluster Parameters",
      "item": [
        {
          "id": "5992c74b-2802-4446-9d9d-338cb4a7d409",
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
              "id": "051700c0-c97e-425e-8c7b-b581ceae15ef"
            }
          ]
        },
        {
          "id": "7158d51f-ffd0-4d4a-8ab1-bb4cf9447287",
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
              "id": "7f30f7f4-8c7c-4300-8016-c0fb1e2378c1"
            }
          ]
        }
      ]
    },
    {
      "name": "Event Categories",
      "item": [
        {
          "id": "0c26a6c6-5647-4180-8e7d-d8a9068084ce",
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
              "id": "9d08bb85-9c00-4033-b88b-0c8a95bfeb10"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "985aabe6-72cc-46b8-81c9-a2e04dbdaddd",
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
              "id": "5bbfbe8c-56a8-401d-a239-3aa062e801cb"
            }
          ]
        }
      ]
    },
    {
      "name": "Logging",
      "item": [
        {
          "id": "77dc49f4-5b07-4a2d-b0d1-e72f1950c626",
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
              "id": "8b58a5f1-8263-4710-8807-f92e8b872c2f"
            }
          ]
        }
      ]
    },
    {
      "name": "Cluster Options",
      "item": [
        {
          "id": "428b7036-51a9-46e9-b3a3-4b2f8b84e40f",
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
              "id": "e4c7695e-152e-4ae4-bfb2-251930034209"
            }
          ]
        }
      ]
    },
    {
      "name": "Reserved Nodes",
      "item": [
        {
          "id": "ef57414b-5ef2-4e8e-922f-6133f7873c8e",
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
              "id": "af57d43b-9fa4-4f7c-b0ab-a4b9a2ec115b"
            }
          ]
        },
        {
          "id": "d316b339-a40b-4ca6-9b5d-2c647422df19",
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
              "id": "69bc12dd-433f-4895-826d-af25d3e7cbeb"
            }
          ]
        }
      ]
    }
  ]
}