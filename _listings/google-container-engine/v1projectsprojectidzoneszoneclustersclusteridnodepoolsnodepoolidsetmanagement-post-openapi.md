---
swagger: "2.0"
x-collection-name: Google Container Engine
x-complete: 0
info:
  title: Google Container Engine API Set Cluster Node Management
  description: Sets the NodeManagement options for a node pool.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: container.googleapis.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/projects/{projectId}/zones/{zone}/clusters/{clusterId}/nodePools:
    get:
      summary: Get Cluster Node Pools
      description: Lists the node pools for a cluster.
      operationId: container.projects.zones.clusters.nodePools.list
      x-api-path-slug: v1projectsprojectidzoneszoneclustersclusteridnodepools-get
      parameters:
      - in: path
        name: clusterId
        description: The name of the cluster
      - in: path
        name: projectId
        description: The Google Developers Console [project ID or project number](https://developers
      - in: path
        name: zone
        description: The name of the Google Compute Engine [zone](/compute/docs/zones#available)
          in which the cluster resides
      responses:
        200:
          description: OK
      tags:
      - Node Pool
    post:
      summary: Create Cluster Node Pool
      description: Creates a node pool for a cluster.
      operationId: container.projects.zones.clusters.nodePools.create
      x-api-path-slug: v1projectsprojectidzoneszoneclustersclusteridnodepools-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: clusterId
        description: The name of the cluster
      - in: path
        name: projectId
        description: The Google Developers Console [project ID or project number](https://developers
      - in: path
        name: zone
        description: The name of the Google Compute Engine [zone](/compute/docs/zones#available)
          in which the cluster resides
      responses:
        200:
          description: OK
      tags:
      - Node Pool
  /v1/projects/{projectId}/zones/{zone}/clusters/{clusterId}/nodePools/{nodePoolId}:
    delete:
      summary: Delete Cluster Node Pool
      description: Deletes a node pool from a cluster.
      operationId: container.projects.zones.clusters.nodePools.delete
      x-api-path-slug: v1projectsprojectidzoneszoneclustersclusteridnodepoolsnodepoolid-delete
      parameters:
      - in: path
        name: clusterId
        description: The name of the cluster
      - in: path
        name: nodePoolId
        description: The name of the node pool to delete
      - in: path
        name: projectId
        description: The Google Developers Console [project ID or project number](https://developers
      - in: path
        name: zone
        description: The name of the Google Compute Engine [zone](/compute/docs/zones#available)
          in which the cluster resides
      responses:
        200:
          description: OK
      tags:
      - Node Pool
    get:
      summary: Get Cluster Node Pool
      description: Retrieves the node pool requested.
      operationId: container.projects.zones.clusters.nodePools.get
      x-api-path-slug: v1projectsprojectidzoneszoneclustersclusteridnodepoolsnodepoolid-get
      parameters:
      - in: path
        name: clusterId
        description: The name of the cluster
      - in: path
        name: nodePoolId
        description: The name of the node pool
      - in: path
        name: projectId
        description: The Google Developers Console [project ID or project number](https://developers
      - in: path
        name: zone
        description: The name of the Google Compute Engine [zone](/compute/docs/zones#available)
          in which the cluster resides
      responses:
        200:
          description: OK
      tags:
      - Node Pool
  /v1/projects/{projectId}/zones/{zone}/clusters/{clusterId}/nodePools/{nodePoolId}/setManagement:
    post:
      summary: Set Cluster Node Management
      description: Sets the NodeManagement options for a node pool.
      operationId: container.projects.zones.clusters.nodePools.setManagement
      x-api-path-slug: v1projectsprojectidzoneszoneclustersclusteridnodepoolsnodepoolidsetmanagement-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: clusterId
        description: The name of the cluster to update
      - in: path
        name: nodePoolId
        description: The name of the node pool to update
      - in: path
        name: projectId
        description: The Google Developers Console [project ID or project number](https://support
      - in: path
        name: zone
        description: The name of the Google Compute Engine [zone](/compute/docs/zones#available)
          in which the cluster resides
      responses:
        200:
          description: OK
      tags:
      - Node Pool
  /v1/projects/{projectId}/zones/{zone}/clusters/{clusterId}/nodePools/{nodePoolId}:rollback:
    post:
      summary: Rollback Node
      description: Roll back the previously Aborted or Failed NodePool upgrade. This
        will be an no-op if the last upgrade successfully completed.
      operationId: container.projects.zones.clusters.nodePools.rollback
      x-api-path-slug: v1projectsprojectidzoneszoneclustersclusteridnodepoolsnodepoolidrollback-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: clusterId
        description: The name of the cluster to rollback
      - in: path
        name: nodePoolId
        description: The name of the node pool to rollback
      - in: path
        name: projectId
        description: The Google Developers Console [project ID or project number](https://support
      - in: path
        name: zone
        description: The name of the Google Compute Engine [zone](/compute/docs/zones#available)
          in which the cluster resides
      responses:
        200:
          description: OK
      tags:
      - Node Pool
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