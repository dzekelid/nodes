---
swagger: "2.0"
x-collection-name: Kubernetes
x-complete: 0
info:
  title: Kubernetes Get Proxy Nodes Name
  version: 1.0.0
  description: Proxy get requests to node.
host: /api/v1beta3
basePath: 127.0.0.1:6443
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1beta3/nodes:
    get:
      summary: Get Nodes
      description: List objects of kind node.
      operationId: listNode
      x-api-path-slug: apiv1beta3nodes-get
      responses:
        200:
          description: OK
      tags:
      - Nodes
    post:
      summary: Post Nodes
      description: Create a node.
      operationId: createNode
      x-api-path-slug: apiv1beta3nodes-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Nodes
  /api/v1beta3/nodes/{name}:
    delete:
      summary: Delete Nodes Name
      description: Delete a node.
      operationId: deleteNode
      x-api-path-slug: apiv1beta3nodesname-delete
      parameters:
      - in: path
        name: name
        description: name of the Node
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Name
    get:
      summary: Get Nodes Name
      description: Read the specified node.
      operationId: readNode
      x-api-path-slug: apiv1beta3nodesname-get
      parameters:
      - in: path
        name: name
        description: name of the Node
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Name
    put:
      summary: Put Nodes Name
      description: Update the specified node.
      operationId: updateNode
      x-api-path-slug: apiv1beta3nodesname-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: name of the Node
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Name
  /api/v1beta3/proxy/nodes/{name}:
    delete:
      summary: Delete Proxy Nodes Name
      description: Proxy delete requests to node.
      operationId: proxyDELETENode
      x-api-path-slug: apiv1beta3proxynodesname-delete
      parameters:
      - in: path
        name: name
        description: name of the Node
      responses:
        200:
          description: OK
      tags:
      - Proxy
      - Nodes
      - Name
    get:
      summary: Get Proxy Nodes Name
      description: Proxy get requests to node.
      operationId: proxyGETNode
      x-api-path-slug: apiv1beta3proxynodesname-get
      parameters:
      - in: path
        name: name
        description: name of the Node
      responses:
        200:
          description: OK
      tags:
      - Proxy
      - Nodes
      - Name
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