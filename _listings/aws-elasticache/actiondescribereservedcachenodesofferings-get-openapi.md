---
swagger: "2.0"
x-collection-name: AWS ElastiCache
x-complete: 0
info:
  title: Amazon ElastiCache API Describe Reserved Cache Nodes Offerings
  version: 1.0.0
  description: |-
    Lists available reserved cache
                node offerings.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeReservedCacheNodes:
    get:
      summary: Describe Reserved Cache Nodes
      description: |-
        Returns information about reserved cache
                    nodes for this account, or about a specified reserved cache node.
      operationId: describeReservedCacheNodes
      x-api-path-slug: actiondescribereservedcachenodes-get
      parameters:
      - in: query
        name: CacheNodeType
        description: The cache node type filter value
        type: string
      - in: query
        name: Duration
        description: The duration filter value, specified in years or seconds
        type: string
      - in: query
        name: Marker
        description: An optional marker returned from a prior request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      - in: query
        name: OfferingType
        description: The offering type filter value
        type: string
      - in: query
        name: ProductDescription
        description: The product description filter value
        type: string
      - in: query
        name: ReservedCacheNodeId
        description: The reserved cache node identifier filter value
        type: string
      - in: query
        name: ReservedCacheNodesOfferingId
        description: The offering identifier filter value
        type: string
      responses:
        200:
          description: OK
      tags:
      - Reserved Cache Nodes
  /?Action=DescribeReservedCacheNodesOfferings:
    get:
      summary: Describe Reserved Cache Nodes Offerings
      description: |-
        Lists available reserved cache
                    node offerings.
      operationId: describeReservedCacheNodesOfferings
      x-api-path-slug: actiondescribereservedcachenodesofferings-get
      parameters:
      - in: query
        name: CacheNodeType
        description: The cache node type filter value
        type: string
      - in: query
        name: Duration
        description: Duration filter value, specified in years or seconds
        type: string
      - in: query
        name: Marker
        description: An optional marker returned from a prior request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      - in: query
        name: OfferingType
        description: The offering type filter value
        type: string
      - in: query
        name: ProductDescription
        description: The product description filter value
        type: string
      - in: query
        name: ReservedCacheNodesOfferingId
        description: The offering identifier filter value
        type: string
      responses:
        200:
          description: OK
      tags:
      - Reserved Cache Nodes
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---