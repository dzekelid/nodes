---
swagger: "2.0"
x-collection-name: Azure Automation
x-complete: 0
info:
  title: Azure Automation API Node Reports Get Content
  version: 1.0.0
  description: Retrieve the Dsc node reports by node id and report id.
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/nodes/{nodeId}
  : delete:
      summary: Dsc Node Delete
      description: Delete the dsc node identified by node id.
      operationId: DscNode_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-automationautomationaccountsautomationaccountnamenodesnodeid-delete
      parameters:
      - in: path
        name: automationAccountName
        description: Automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeId
        description: The node id
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Node
    get:
      summary: Dsc Node Get
      description: Retrieve the dsc node identified by node id.
      operationId: DscNode_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-automationautomationaccountsautomationaccountnamenodesnodeid-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeId
        description: The node id
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Node
    patch:
      summary: Dsc Node Update
      description: Update the dsc node.
      operationId: DscNode_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-automationautomationaccountsautomationaccountnamenodesnodeid-patch
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeId
        description: Parameters supplied to the update dsc node
      - in: body
        name: parameters
        description: Parameters supplied to the update dsc node
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Node
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/nodes
  : get:
      summary: Dsc Node List By Automation Account
      description: Retrieve a list of dsc nodes.
      operationId: DscNode_ListByAutomationAccount
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-automationautomationaccountsautomationaccountnamenodes-get
      parameters:
      - in: query
        name: $filter
        description: The filter to apply on the operation
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Node
      - List
      - Automation
      - Account
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/nodes/{nodeId}/reports
  : get:
      summary: Node Reports List By Node
      description: Retrieve the Dsc node report list by node id.
      operationId: NodeReports_ListByNode
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-automationautomationaccountsautomationaccountnamenodesnodeidreports-get
      parameters:
      - in: query
        name: $filter
        description: The filter to apply on the operation
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeId
        description: The parameters supplied to the list operation
      responses:
        200:
          description: OK
      tags:
      - Node
      - Reports
      - ListNode
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/nodes/{nodeId}/reports/{reportId}
  : get:
      summary: Node Reports Get
      description: Retrieve the Dsc node report data by node id and report id.
      operationId: NodeReports_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-automationautomationaccountsautomationaccountnamenodesnodeidreportsreportid-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeId
        description: The Dsc node id
      - in: path
        name: reportId
        description: The report id
      responses:
        200:
          description: OK
      tags:
      - Node
      - Reports
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/nodes/{nodeId}/reports/{reportId}/content
  : get:
      summary: Node Reports Get Content
      description: Retrieve the Dsc node reports by node id and report id.
      operationId: NodeReports_GetContent
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-automationautomationaccountsautomationaccountnamenodesnodeidreportsreportidcontent-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeId
        description: The Dsc node id
      - in: path
        name: reportId
        description: The report id
      responses:
        200:
          description: OK
      tags:
      - Node
      - Reports
      - ""
      - Content
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/nodeConfigurations/{nodeConfigurationName}
  : delete:
      summary: Dsc Node Configuration Delete
      description: Delete the Dsc node configurations by node configuration.
      operationId: DscNodeConfiguration_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-automationautomationaccountsautomationaccountnamenodeconfigurationsnodeconfigurationname-delete
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeConfigurationName
        description: The Dsc node configuration name
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Node
      - Configuration
    get:
      summary: Dsc Node Configuration Get
      description: Retrieve the Dsc node configurations by node configuration.
      operationId: DscNodeConfiguration_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-automationautomationaccountsautomationaccountnamenodeconfigurationsnodeconfigurationname-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeConfigurationName
        description: The Dsc node configuration name
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Node
      - Configuration
    put:
      summary: Dsc Node Configuration Create Or Update
      description: Create the node configuration identified by node configuration
        name.
      operationId: DscNodeConfiguration_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-automationautomationaccountsautomationaccountnamenodeconfigurationsnodeconfigurationname-put
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeConfigurationName
        description: The create or update parameters for configuration
      - in: body
        name: parameters
        description: The create or update parameters for configuration
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Node
      - Configuration
      - Or
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/nodeConfigurations
  : get:
      summary: Dsc Node Configuration List By Automation Account
      description: Retrieve a list of dsc node configurations.
      operationId: DscNodeConfiguration_ListByAutomationAccount
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-automationautomationaccountsautomationaccountnamenodeconfigurations-get
      parameters:
      - in: query
        name: $filter
        description: The filter to apply on the operation
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Node
      - Configuration
      - List
      - Automation
      - Account
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