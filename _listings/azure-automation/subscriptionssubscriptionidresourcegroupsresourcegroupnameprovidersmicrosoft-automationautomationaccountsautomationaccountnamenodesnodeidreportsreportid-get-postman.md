{
  "info": {
    "name": "Azure Automation API Node Reports Get",
    "_postman_id": "44078579-4bdd-448f-befc-8336a55af518",
    "description": "Retrieve the Dsc node report data by node id and report id.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "node",
      "item": [
        {
          "id": "e44c2bda-dbb0-4712-b7a8-67cfaf2def72",
          "name": "NodeReports_Get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/nodes/:nodeId/reports/:reportId"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "automationAccountName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "nodeId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "reportId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "subscriptionId",
                  "value": "subscriptionId",
                  "type": "string"
                },
                {
                  "id": "resourceGroupName",
                  "value": "resourceGroupName",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve the Dsc node report data by node id and report id"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "135aa844-41da-4f20-9079-34aafac24122"
            }
          ]
        }
      ]
    }
  ]
}