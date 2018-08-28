swagger: "2.0"
x-collection-name: Azure Blockchain Workbench
x-complete: 1
info:
  title: Azure Blockchain Workbench REST API
  description: the-azure-blockchain-workbench-rest-api-is-a-workbench-extensibility-point-which-allows-developers-to-create-and-manage-blockchain-applications-manage-users-and-organizations-within-a-consortium-integrate-blockchain-applications-into-services-and-platforms-perform-transactions-on-a-blockchain-and-retrieve-transactional-and-contract-data-from-a-blockchain-
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/checkers/checkContractCode:
    post:
      summary: Post Checkers Check Contract Node
      description: Check if the application smart contract implementation file is
        valid for Workbench.
      operationId: CheckContractCodePost
      x-api-path-slug: apiv1checkerscheckcontractcode-post
      parameters:
      - in: formData
        name: appFile
        description: Upload Application File
      - in: formData
        name: contractFile
        description: Upload Contract Code File
      - in: query
        name: ledgerId
        description: The index of the chain type
      responses:
        200:
          description: OK
      tags:
      - Checkers
      - Check
      - Contract
      - Node