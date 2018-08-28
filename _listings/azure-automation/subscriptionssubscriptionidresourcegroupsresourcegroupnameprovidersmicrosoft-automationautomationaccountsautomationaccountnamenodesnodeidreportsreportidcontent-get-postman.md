{
  "info": {
    "name": "Azure Automation API Node Reports Get Content",
    "_postman_id": "fb7d5b85-0d73-40c1-a952-b5a809461f0b",
    "description": "Retrieve the Dsc node reports by node id and report id.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "node",
      "item": [
        {
          "id": "18818086-9cfa-4c21-b2b5-4a5ba6926ab8",
          "name": "NodeReports_GetContent",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/nodes/:nodeId/reports/:reportId/content"
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
            "description": "Retrieve the Dsc node reports by node id and report id"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9c5dfbf1-92e2-4fd6-95e4-4d3d7adb7945"
            }
          ]
        }
      ]
    }
  ]
}