---
swagger: "2.0"
x-collection-name: AWS Redshift
x-complete: 1
info:
  title: AWS Redshift API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeReservedNodeOfferings:
    get:
      summary: Describe Reserved Node Offerings
      description: |-
        Returns a list of the available reserved node offerings by Amazon Redshift with their
                    descriptions including the node type, the fixed and recurring costs of reserving the
                    node and duration the node will be reserved for you.
      operationId: describeReservedNodeOfferings
      x-api-path-slug: actiondescribereservednodeofferings-get
      parameters:
      - in: query
        name: Marker
        description: An optional parameter that specifies the starting point to return
          a set of response            records
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of response records to return in each call
        type: string
      - in: query
        name: ReservedNodeOfferingId
        description: The unique identifier for the offering
        type: string
      responses:
        200:
          description: OK
      tags:
      - Reserved Nodes
  /?Action=DescribeReservedNodes:
    get:
      summary: Describe Reserved Nodes
      description: Returns the descriptions of the reserved nodes.
      operationId: describeReservedNodes
      x-api-path-slug: actiondescribereservednodes-get
      parameters:
      - in: query
        name: Marker
        description: An optional parameter that specifies the starting point to return
          a set of response            records
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of response records to return in each call
        type: string
      - in: query
        name: ReservedNodeId
        description: Identifier for the node reservation
        type: string
      responses:
        200:
          description: OK
      tags:
      - Reserved Nodes
  /?Action=PurchaseReservedNodeOffering:
    get:
      summary: Purchase Reserved Node Offering
      description: Allows you to purchase reserved nodes.
      operationId: purchaseReservedNodeOffering
      x-api-path-slug: actionpurchasereservednodeoffering-get
      parameters:
      - in: query
        name: NodeCount
        description: The number of reserved nodes that you want to purchase
        type: string
      - in: query
        name: ReservedNodeOfferingId
        description: The unique identifier of the reserved node offering you want
          to purchase
        type: string
      responses:
        200:
          description: OK
      tags:
      - Reserved Nodes
---