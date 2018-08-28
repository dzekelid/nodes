{
  "info": {
    "name": "Bitbucket Add Repositories Username Repo Slug Commit Node Statuses Build",
    "_postman_id": "3897c78d-65ac-4cf1-afb7-6649ed42aa76",
    "description": "Creates a new build status against the specified commit.\n\nIf the specified key already exists, the existing status object will\nbe overwritten.\n\nWhen creating a new commit status, you can use a URI template for the URL.\nTemplates are URLs that contain variable names that Bitbucket will\nevaluate at runtime whenever the URL is displayed anywhere similar to\nparameter substitution in\n[Bitbucket Connect](https://developer.atlassian.com/bitbucket/concepts/context-parameters.html).\nFor example, one could use `https://foo.com/builds/{repository.full_name}`\nwhich Bitbucket will turn into `https://foo.com/builds/foo/bar` at render time.\nThe context variables available are `repository` and `commit`.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "dcf50e87-1643-4c72-9017-64bae6c1e1f3",
          "name": "postRepositoriesUsernameRepoSlugCommitNodeStatusesBuild",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/commit/:node/statuses/build"
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
            "description": "Creates a new build status against the specified commit"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b20a50d8-a322-4695-b758-04ad1f8823b4"
            }
          ]
        }
      ]
    }
  ]
}