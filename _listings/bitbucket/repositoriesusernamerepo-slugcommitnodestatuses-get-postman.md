{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Commit Node Statuses",
    "_postman_id": "3d3a6d6d-2ccc-4f34-a7a1-cb4c54609219",
    "description": "Returns all statuses (e.g. build results) for a specific commit.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "b71bbf45-8f75-469e-abcc-06938048c8e5",
          "name": "getRepositoriesUsernameRepoSlugCommitNodeStatuses",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/commit/:node/statuses"
              ],
              "variable": [
                {
                  "id": "node",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "username",
                  "value": "username",
                  "type": "string"
                },
                {
                  "id": "repo_slug",
                  "value": "repo_slug",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all statuses (e"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "45ac5ca8-c6df-4791-a134-bb0ce7dd0345"
            }
          ]
        }
      ]
    }
  ]
}