{
  "info": {
    "name": "Bitbucket Delete Repositories Username Repo Slug Commit Node Approve",
    "_postman_id": "fa3d5641-882c-4ddc-b10e-692fee3eb72a",
    "description": "Redact the authenticated user's approval of the specified commit.\n\nThis operation is only available to users that have explicit access to\nthe repository. In contrast, just the fact that a repository is\npublicly accessible to users does not give them the ability to approve\ncommits.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "fc15911f-4b23-4339-9a3a-c6ab56393987",
          "name": "deleteRepositoriesUsernameRepoSlugCommitNodeApprove",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/commit/:node/approve"
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Redact the authenticated user's approval of the specified commit"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b0db44d6-47a6-4ff9-a48b-e16bc8f02172"
            }
          ]
        }
      ]
    }
  ]
}