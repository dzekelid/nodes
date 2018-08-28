swagger: "2.0"
x-collection-name: Neblio
x-complete: 1
info:
  title: Neblio REST API Suite
  description: apis-for-interacting-with-ntp1-tokens--the-neblio-blockchain
  version: 1.0.0
host: ntp1node.nebl.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /ins/sync:
    get:
      summary: Get node sync status
      description: Returns information on the node's sync progress
      operationId: getSync
      x-api-path-slug: inssync-get
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Node
      - Sync
      - Status
  /ins/status:
    get:
      summary: Utility API for calling several blockchain node functions
      description: Utility API for calling several blockchain node functions - getInfo,
        getDifficulty, getBestBlockHash, getLastBlockHash
      operationId: getStatus
      x-api-path-slug: insstatus-get
      parameters:
      - in: query
        name: q
        description: Function to call, getInfo, getDifficulty, getBestBlockHash, or
          getLastBlockHash
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Utility
      - APIcalling
      - Several
      - Blockchain
      - Node
      - Functions
  /testnet/ins/sync:
    get:
      summary: Get node sync status
      description: Returns information on the node's sync progress
      operationId: testnet_getSync
      x-api-path-slug: testnetinssync-get
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Node
      - Sync
      - Status
  /testnet/ins/status:
    get:
      summary: Utility API for calling several blockchain node functions
      description: Utility API for calling several blockchain node functions - getInfo,
        getDifficulty, getBestBlockHash, getLastBlockHash
      operationId: testnet_getStatus
      x-api-path-slug: testnetinsstatus-get
      parameters:
      - in: query
        name: q
        description: Function to call, getInfo, getDifficulty, getBestBlockHash, or
          getLastBlockHash
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Utility
      - APIcalling
      - Several
      - Blockchain
      - Node
      - Functions