{
  "info": {
    "name": "Bitbucket Add Repositories Username Repo Slug Commit Node Approve",
    "_postman_id": "2893e34f-bc32-442d-8439-bbc7e4057871",
    "description": "Approve the specified commit as the authenticated user.\n\nThis operation is only available to users that have explicit access to\nthe repository. In contrast, just the fact that a repository is\npublicly accessible to users does not give them the ability to approve\ncommits.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "cce45bb9-8ec2-448c-98ea-debca895eeff",
          "name": "postRepositoriesUsernameRepoSlugCommitNodeApprove",
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
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Approve the specified commit as the authenticated user"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e2c02cbd-4596-4b06-b5f5-9719a643810b"
            }
          ]
        }
      ]
    }
  ]
}