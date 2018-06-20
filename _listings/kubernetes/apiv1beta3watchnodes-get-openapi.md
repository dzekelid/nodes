---
swagger: "2.0"
x-collection-name: Kubernetes
x-complete: 0
info:
  title: Kubernetes Get Watch Nodes
  version: 1.0.0
  description: Watch a list of node.
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
    post:
      summary: Post Proxy Nodes Name
      description: Proxy post requests to node.
      operationId: proxyPOSTNode
      x-api-path-slug: apiv1beta3proxynodesname-post
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
    put:
      summary: Put Proxy Nodes Name
      description: Proxy put requests to node.
      operationId: proxyPUTNode
      x-api-path-slug: apiv1beta3proxynodesname-put
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
  /api/v1beta3/proxy/nodes/{name}/{path:*}:
    delete:
      summary: Delete Proxy Nodes Name Path *
      description: Proxy delete requests to node.
      operationId: proxyDELETENode
      x-api-path-slug: apiv1beta3proxynodesnamepath-delete
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
      - Path
      - '*'
    get:
      summary: Get Proxy Nodes Name Path *
      description: Proxy get requests to node.
      operationId: proxyGETNode
      x-api-path-slug: apiv1beta3proxynodesnamepath-get
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
      - Path
      - '*'
    post:
      summary: Post Proxy Nodes Name Path *
      description: Proxy post requests to node.
      operationId: proxyPOSTNode
      x-api-path-slug: apiv1beta3proxynodesnamepath-post
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
      - Path
      - '*'
    put:
      summary: Put Proxy Nodes Name Path *
      description: Proxy put requests to node.
      operationId: proxyPUTNode
      x-api-path-slug: apiv1beta3proxynodesnamepath-put
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
      - Path
      - '*'
  /api/v1beta3/redirect/nodes/{name}:
    get:
      summary: Get Redirect Nodes Name
      description: Redirect get request to node.
      operationId: redirectNode
      x-api-path-slug: apiv1beta3redirectnodesname-get
      parameters:
      - in: path
        name: name
        description: name of the Node
      responses:
        200:
          description: OK
      tags:
      - Redirect
      - Nodes
      - Name
  /api/v1beta3/watch/nodes:
    get:
      summary: Get Watch Nodes
      description: Watch a list of node.
      operationId: watchNodelist
      x-api-path-slug: apiv1beta3watchnodes-get
      responses:
        200:
          description: OK
      tags:
      - Watch
      - Nodes
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