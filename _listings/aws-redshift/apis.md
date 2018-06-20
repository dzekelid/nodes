---
name: AWS Redshift
x-slug: aws-redshift
description: Amazon Redshift is a fast, fully managed, petabyte-scaledata warehousethat
  makes it simple and cost-effective to analyze all your data using your existing
  business intelligence tools. Start small for $0.25 per hour with no commitments
  and scale to petabytes for $1,000 per terabyte per year, less than a tenth the cost
  of traditional solutions. Customers typically see 3x compression, reducing their
  costs to $333 per uncompressed terabyte per year.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Database_AmazonRedshift.png
x-kinRank: "10"
x-alexaRank: "0"
tags: Nodes
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/aws-redshift/apis.md
specificationVersion: "0.14"
apis:
- name: Amazon Redshift API Describe Reserved Node Offerings
  x-api-slug: amazon-redshift-api
  description: |-
    Returns a list of the available reserved node offerings by Amazon Redshift with their
                descriptions including the node type, the fixed and recurring costs of reserving the
                node and duration the node will be reserved for you.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Database_AmazonRedshift.png
  humanURL: https://aws.amazon.com/redshift/
  baseURL: ://///?Action=DescribeReservedNodeOfferings
  tags: 'Reserved Nodes '
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/aws-redshift/actiondescribereservednodeofferings-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/aws-redshift/actiondescribereservednodeofferings-get-openapi.md
- name: Amazon Redshift API Describe Reserved Nodes
  x-api-slug: amazon-redshift-api
  description: Returns the descriptions of the reserved nodes.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Database_AmazonRedshift.png
  humanURL: https://aws.amazon.com/redshift/
  baseURL: ://///?Action=DescribeReservedNodes
  tags: 'Reserved Nodes '
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/aws-redshift/actiondescribereservednodes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/aws-redshift/actiondescribereservednodes-get-openapi.md
- name: Amazon Redshift API Purchase Reserved Node Offering
  x-api-slug: amazon-redshift-api
  description: Allows you to purchase reserved nodes.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Database_AmazonRedshift.png
  humanURL: https://aws.amazon.com/redshift/
  baseURL: ://///?Action=PurchaseReservedNodeOffering
  tags: Reserved Nodes
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/aws-redshift/actionpurchasereservednodeoffering-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/aws-redshift/actionpurchasereservednodeoffering-get-openapi.md
- name: Amazon Redshift API
  x-api-slug: amazon-redshift-api
  description: Amazon Redshift is a fast, fully managed, petabyte-scaledata warehousethat
    makes it simple and cost-effective to analyze all your data using your existing
    business intelligence tools. Start small for $0.25 per hour with no commitments
    and scale to petabytes for $1,000 per terabyte per year, less than a tenth the
    cost of traditional solutions. Customers typically see 3x compression, reducing
    their costs to $333 per uncompressed terabyte per year.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Database_AmazonRedshift.png
  humanURL: https://aws.amazon.com/redshift/
  baseURL: :///
  tags: Nodes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/aws-redshift/openapi.md
x-common:
- type: x-best-practices
  url: https://aws.amazon.com/redshift/developer-resources/#best-practices
- type: x-command-line-interface
  url: http://docs.aws.amazon.com/cli/latest/reference/redshift/index.html
- type: x-customer-success
  url: https://aws.amazon.com/redshift/customer-success/
- type: x-documentation
  url: http://docs.aws.amazon.com/redshift/latest/APIReference/
- type: x-events
  url: https://aws.amazon.com/redshift/events/
- type: x-faq
  url: https://aws.amazon.com/redshift/faqs/
- type: x-getting-started
  url: https://aws.amazon.com/redshift/getting-started/
- type: x-partners
  url: https://aws.amazon.com/redshift/partners/
- type: x-pricing
  url: https://aws.amazon.com/redshift/pricing/
- type: x-website
  url: https://aws.amazon.com/redshift/
- type: x-whats-new
  url: https://aws.amazon.com/redshift/whats-new/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---