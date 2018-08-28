{
  "info": {
    "name": "Azure Automation API Node Reports List By Node",
    "_postman_id": "0148db51-6040-4278-b76b-24c55109791a",
    "description": "Retrieve the Dsc node report list by node id.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "node",
      "item": [
        {
          "id": "63384203-cf08-41b8-ae7f-4a8e9c3e9b1b",
          "name": "NodeReports_ListByNode",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/nodes/:nodeId/reports"
              ],
              "query": [
                {
                  "key": "$filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
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
            "description": "Retrieve the Dsc node report list by node id"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c3e78dc5-1b3d-49d0-a56f-7c786d03d246"
            }
          ]
        }
      ]
    }
  ]
}