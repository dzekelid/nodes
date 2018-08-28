---
swagger: "2.0"
x-collection-name: AWS ElastiCache
x-complete: 0
info:
  title: Amazon ElastiCache API List Allowed Node Type Modifications
  version: 1.0.0
  description: |-
    Lists all available node types that you
                can scale your Redis cluster's or replication group's current node type up to.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=ListAllowedNodeTypeModifications:
    get:
      summary: List Allowed Node Type Modifications
      description: |-
        Lists all available node types that you
                    can scale your Redis cluster's or replication group's current node type up to.
      operationId: listAllowedNodeTypeModifications
      x-api-path-slug: actionlistallowednodetypemodifications-get
      parameters:
      - in: query
        name: CacheClusterId
        description: The name of the cache cluster you want to scale up to a larger
          node instanced type
        type: string
      - in: query
        name: ReplicationGroupId
        description: The name of the replication group want to scale up to a larger
          node type
        type: string
      responses:
        200:
          description: OK
      tags:
      - Node Type Modifications
  /?Action=ListAvailableNodeTypes:
    get:
      summary: List Available Node Types
      description: .
      operationId: listAvailableNodeTypes
      x-api-path-slug: actionlistavailablenodetypes-get
      parameters:
      - in: query
        name: AvailableNodeTypes.member.N
        description: 'Type: array of AvailableNodeType objects'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Node Types
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
  /?Action=PurchaseReservedCacheNodesOffering:
    get:
      summary: Purchase Reserved Cache Nodes Offering
      description: |-
        Allows you to purchase a reserved
                    cache node offering.
      operationId: purchaseReservedCacheNodesOffering
      x-api-path-slug: actionpurchasereservedcachenodesoffering-get
      parameters:
      - in: query
        name: CacheNodeCount
        description: The number of cache node instances to reserve
        type: string
      - in: query
        name: ReservedCacheNodeId
        description: A customer-specified identifier to track this reservation
        type: string
      - in: query
        name: ReservedCacheNodesOfferingId
        description: The ID of the reserved cache node offering to purchase
        type: string
      responses:
        200:
          description: OK
      tags:
      - Reserved Cache Nodes
  /?Action=RebootCacheCluster:
    get:
      summary: Reboot Cache Cluster
      description: |-
        Reboots some, or all, of the cache nodes
                    within a provisioned cache cluster.
      operationId: rebootCacheCluster
      x-api-path-slug: actionrebootcachecluster-get
      parameters:
      - in: query
        name: CacheClusterId
        description: The cache cluster identifier
        type: string
      - in: query
        name: CacheNodeIdsToReboot.CacheNodeId.N
        description: A list of cache node IDs to reboot
        type: string
      responses:
        200:
          description: OK
      tags:
      - Cache Clusters
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