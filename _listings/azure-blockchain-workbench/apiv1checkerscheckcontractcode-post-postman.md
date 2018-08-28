{
  "info": {
    "name": "Azure Blockchain Workbench Post Checkers Check Contract Node",
    "_postman_id": "81d0718a-e4ef-4980-99fe-a62545cd1ab1",
    "description": "Check if the application smart contract implementation file is valid for Workbench.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Checkers",
      "item": [
        {
          "id": "8f1c52d1-3ceb-48c1-ad89-b5d74c791c75",
          "name": "CheckApplicationPost",
          "request": {
            "url": "{{default}}/api/v1/checkers/checkApplication",
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "appFile",
                  "value": "{}",
                  "disabled": false,
                  "description": "Upload Application File"
                }
              ]
            },
            "description": "Checks if the supplied application configuration file is valid for Workbench."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b2bbd75f-6c77-47e6-b521-e17e173395b5"
            }
          ]
        },
        {
          "id": "fd913056-8fb9-494e-9bf9-42ad84fa0ee7",
          "name": "CheckContractCodePost",
          "request": {
            "url": "{{default}}/api/v1/checkers/checkContractCode?ledgerId=%7B%7D",
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "appFile",
                  "value": "{}",
                  "disabled": false,
                  "description": "Upload Application File"
                },
                {
                  "key": "contractFile",
                  "value": "{}",
                  "disabled": false,
                  "description": "Upload Contract Code File"
                }
              ]
            },
            "description": "Check if the application smart contract implementation file is valid for Workbench."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "66725531-66ee-4731-867c-ea0e57eb037a"
            }
          ]
        }
      ]
    }
  ],
  "variable": [
    {
      "key": "default",
      "value": "http://www.example.com/"
    }
  ]
}