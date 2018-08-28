---
swagger: "2.0"
x-collection-name: AWS Elastic MapReduce
x-complete: 0
info:
  title: AWS Elastic MapReduce API Modify Instance Groups
  version: 1.0.0
  description: ModifyInstanceGroups modifies the number of nodes and configuration
    settings of an instance group.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=ModifyInstanceGroups:
    get:
      summary: Modify Instance Groups
      description: ModifyInstanceGroups modifies the number of nodes and configuration
        settings of an instance group.
      operationId: modifyInstanceGroups
      x-api-path-slug: actionmodifyinstancegroups-get
      parameters:
      - in: query
        name: ClusterId
        description: The ID of the cluster to which the instance group belongs
        type: string
      - in: query
        name: InstanceGroups
        description: Instance groups to change
        type: string
      responses:
        200:
          description: OK
      tags:
      - Instance Groups
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