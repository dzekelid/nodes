{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Commit Node Statuses Build Key",
    "_postman_id": "bfa80d8b-1ca4-49f3-8061-33b2bcc66de1",
    "description": "Get repositories username repo slug commit node statuses build key",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "805310e5-8b62-47b1-9532-0aa7ba39e45f",
          "name": "getRepositoriesUsernameRepoSlugCommitNodeStatusesBuildKey",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/commit/:node/statuses/build/:key"
              ],
              "variable": [
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                },
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
            "description": "Get repositories username repo slug commit node statuses build key"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3673d62e-23ef-4d3f-8ce9-7d54c5465d61"
            }
          ]
        }
      ]
    }
  ]
}