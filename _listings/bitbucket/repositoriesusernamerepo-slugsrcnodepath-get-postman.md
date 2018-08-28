{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Src Node Path",
    "_postman_id": "a33fb3c6-9db8-482f-8b4c-2611ef2f7359",
    "description": "Get repositories username repo slug src node path",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "69707308-7708-4c4d-9325-bb6a75f73c30",
          "name": "getRepositoriesUsernameRepoSlugSrcNodePath",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/src/:node/:path"
              ],
              "query": [
                {
                  "key": "format",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "username",
                  "value": "username",
                  "type": "string"
                },
                {
                  "id": "repo_slug",
                  "value": "repo_slug",
                  "type": "string"
                },
                {
                  "id": "node",
                  "value": "node",
                  "type": "string"
                },
                {
                  "id": "path",
                  "value": "path",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get repositories username repo slug src node path"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "58c22a28-787c-428e-9ba8-d70dc20878fe"
            }
          ]
        }
      ]
    }
  ]
}