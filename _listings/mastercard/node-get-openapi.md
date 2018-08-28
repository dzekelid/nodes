---
swagger: "2.0"
x-collection-name: MasterCard
x-complete: 0
info:
  title: Mastercard Get Node
  description: |-
    By default, this call gets information about your local node and its
    connections. The `scope` parameter enabled this query to be extended
    to get further information about nodes that are visible to your node.
  version: 1.0.0
host: eas5stl0.mastercard.int:13046
basePath: /z0/core/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /node:
    get:
      summary: Get Node
      description: |-
        By default, this call gets information about your local node and its
        connections. The `scope` parameter enabled this query to be extended
        to get further information about nodes that are visible to your node.
      operationId: getNode
      x-api-path-slug: node-get
      parameters:
      - in: header
        name: MCWSSAML
        description: SAML Authorization
      - in: query
        name: scope
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Node
  /node/{address}:
    get:
      summary: Get Node Address
      description: |-
        Information about a specific node may be retrieved by its address.
        This is useful when navigating the network.
      operationId: getNodeAddress
      x-api-path-slug: nodeaddress-get
      parameters:
      - in: path
        name: address
      - in: header
        name: MCWSSAML
        description: SAML Authorization
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Node
      - Address
  /address/{address}:
    get:
      summary: Get Address Address
      description: |-
        Information about a particular address on the network. Note that this
        call may return information about a blockchain node or a signing entity.
        Also, the level of detail returned will vary depending on your permissions
        for the query target.
      operationId: getAddressAddress
      x-api-path-slug: addressaddress-get
      parameters:
      - in: path
        name: address
      - in: header
        name: MCWSSAML
        description: SAML Authorization
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Address
      - Address
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