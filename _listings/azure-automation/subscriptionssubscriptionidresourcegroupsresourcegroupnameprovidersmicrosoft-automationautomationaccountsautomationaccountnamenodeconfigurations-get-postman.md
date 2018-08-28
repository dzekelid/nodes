{
  "info": {
    "name": "Azure Automation API Dsc Node Configuration List By Automation Account",
    "_postman_id": "d879bdb6-3557-488f-acf8-e6b3f1d2b79d",
    "description": "Retrieve a list of dsc node configurations.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "dsc",
      "item": [
        {
          "id": "ea634a06-a662-46d2-aec0-2b73c9bef254",
          "name": "DscNodeConfiguration_ListByAutomationAccount",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/nodeConfigurations"
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
            "description": "Retrieve a list of dsc node configurations"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2ff25978-f3ba-4e1d-a910-6e0d29a4a9c7"
            }
          ]
        }
      ]
    }
  ]
}