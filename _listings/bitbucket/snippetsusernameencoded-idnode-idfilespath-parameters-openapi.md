---
swagger: "2.0"
x-collection-name: Bitbucket
x-complete: 0
info:
  title: Bitbucket Parameters Snippets Username Encoded  Node  Files Path
  description: Parameters snippets username encoded  node  files path
  termsOfService: https://www.atlassian.com/legal/customer-agreement
  contact:
    name: Bitbucket Support
    url: https://support.atlassian.com/bitbucket
    email: support@bitbucket.org
  version: 1.0.0
host: api.bitbucket.org
basePath: /2.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /repositories/{username}/{repo_slug}/commit/{node}/approve:
    delete:
      summary: Delete Repositories Username Repo Slug Commit Node Approve
      description: |-
        Redact the authenticated user's approval of the specified commit.

        This operation is only available to users that have explicit access to
        the repository. In contrast, just the fact that a repository is
        publicly accessible to users does not give them the ability to approve
        commits.
      operationId: deleteRepositoriesUsernameRepoSlugCommitNodeApprove
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodeapprove-delete
      parameters:
      - in: path
        name: node
        description: The commits SHA1
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Approve
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Node Approve
      description: Parameters repositories username repo slug commit node approve
      operationId: parametersRepositoriesUsernameRepoSlugCommitNodeApprove
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodeapprove-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Approve
    post:
      summary: Add Repositories Username Repo Slug Commit Node Approve
      description: |-
        Approve the specified commit as the authenticated user.

        This operation is only available to users that have explicit access to
        the repository. In contrast, just the fact that a repository is
        publicly accessible to users does not give them the ability to approve
        commits.
      operationId: postRepositoriesUsernameRepoSlugCommitNodeApprove
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodeapprove-post
      parameters:
      - in: path
        name: node
        description: The commits SHA1
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Approve
  /repositories/{username}/{repo_slug}/commit/{node}/statuses:
    get:
      summary: Get Repositories Username Repo Slug Commit Node Statuses
      description: Returns all statuses (e.g. build results) for a specific commit.
      operationId: getRepositoriesUsernameRepoSlugCommitNodeStatuses
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatuses-get
      parameters:
      - in: path
        name: node
        description: The commits SHA1
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Node Statuses
      description: Parameters repositories username repo slug commit node statuses
      operationId: parametersRepositoriesUsernameRepoSlugCommitNodeStatuses
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatuses-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
  /repositories/{username}/{repo_slug}/commit/{node}/statuses/build:
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Node Statuses Build
      description: Parameters repositories username repo slug commit node statuses
        build
      operationId: parametersRepositoriesUsernameRepoSlugCommitNodeStatusesBuild
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatusesbuild-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
      - Build
    post:
      summary: Add Repositories Username Repo Slug Commit Node Statuses Build
      description: |-
        Creates a new build status against the specified commit.

        If the specified key already exists, the existing status object will
        be overwritten.

        When creating a new commit status, you can use a URI template for the URL.
        Templates are URLs that contain variable names that Bitbucket will
        evaluate at runtime whenever the URL is displayed anywhere similar to
        parameter substitution in
        [Bitbucket Connect](https://developer.atlassian.com/bitbucket/concepts/context-parameters.html).
        For example, one could use `https://foo.com/builds/{repository.full_name}`
        which Bitbucket will turn into `https://foo.com/builds/foo/bar` at render time.
        The context variables available are `repository` and `commit`.
      operationId: postRepositoriesUsernameRepoSlugCommitNodeStatusesBuild
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatusesbuild-post
      parameters:
      - in: path
        name: node
        description: The commits SHA1
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
      - Build
  /repositories/{username}/{repo_slug}/commit/{node}/statuses/build/{key}:
    get:
      summary: Get Repositories Username Repo Slug Commit Node Statuses Build Key
      description: Get repositories username repo slug commit node statuses build
        key
      operationId: getRepositoriesUsernameRepoSlugCommitNodeStatusesBuildKey
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatusesbuildkey-get
      parameters:
      - in: path
        name: key
        description: The build status unique key
      - in: path
        name: node
        description: The commits SHA1
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
      - Build
      - Key
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Node Statuses Build
        Key
      description: Parameters repositories username repo slug commit node statuses
        build key
      operationId: parametersRepositoriesUsernameRepoSlugCommitNodeStatusesBuildKey
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatusesbuildkey-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
      - Build
      - Key
    put:
      summary: Update Repositories Username Repo Slug Commit Node Statuses Build Key
      description: |-
        Used to update the current status of a build status object on the
        specific commit.

        This operation can also be used to change other properties of the
        build status:

        * `state`
        * `name`
        * `description`
        * `url`
        * `refname`

        The `key` cannot be changed.
      operationId: putRepositoriesUsernameRepoSlugCommitNodeStatusesBuildKey
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatusesbuildkey-put
      parameters:
      - in: path
        name: key
        description: The commit status unique key
      - in: path
        name: node
        description: The commits SHA1
      - in: body
        name: _body
        description: The updated build status object
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
      - Build
      - Key
  /repositories/{username}/{repo_slug}/src/{node}/{path}:
    get:
      summary: Get Repositories Username Repo Slug Src Node Path
      description: Get repositories username repo slug src node path
      operationId: getRepositoriesUsernameRepoSlugSrcNodePath
      x-api-path-slug: repositoriesusernamerepo-slugsrcnodepath-get
      parameters:
      - in: query
        name: format
        description: Instead of returning the files contents, return the (json) meta
          data for it
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Src
      - Node
      - Path
    parameters:
      summary: Parameters Repositories Username Repo Slug Src Node Path
      description: Parameters repositories username repo slug src node path
      operationId: parametersRepositoriesUsernameRepoSlugSrcNodePath
      x-api-path-slug: repositoriesusernamerepo-slugsrcnodepath-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Src
      - Node
      - Path
  /snippets/{username}/{encoded_id}/{node_id}:
    delete:
      summary: Delete Snippets Username Encoded  Node
      description: |-
        Deletes the snippet.

        Note that this only works for versioned URLs that point to the latest
        commit of the snippet. Pointing to an older commit results in a 405
        status code.

        To delete a snippet, regardless of whether or not concurrent changes
        are being made to it, use `DELETE /snippets/{encoded_id}` instead.
      operationId: deleteSnippetsUsernameEncodedNode
      x-api-path-slug: snippetsusernameencoded-idnode-id-delete
      parameters:
      - in: path
        name: encoded_id
        description: The snippets id
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Node
    get:
      summary: Get Snippets Username Encoded  Node
      description: |-
        Identical to `GET /snippets/encoded_id`, except that this endpoint
        can be used to retrieve the contents of the snippet as it was at an
        older revision, while `/snippets/encoded_id` always returns the
        snippet's current revision.

        Note that only the snippet's file contents are versioned, not its
        meta data properties like the title.

        Other than that, the two endpoints are identical in behavior.
      operationId: getSnippetsUsernameEncodedNode
      x-api-path-slug: snippetsusernameencoded-idnode-id-get
      parameters:
      - in: path
        name: encoded_id
        description: The snippets id
      - in: path
        name: node_id
        description: A commit revision (SHA1)
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Node
    parameters:
      summary: Parameters Snippets Username Encoded  Node
      description: Parameters snippets username encoded  node
      operationId: parametersSnippetsUsernameEncodedNode
      x-api-path-slug: snippetsusernameencoded-idnode-id-parameters
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Node
    put:
      summary: Update Snippets Username Encoded  Node
      description: |-
        Identical to `UPDATE /snippets/encoded_id`, except that this endpoint
        takes an explicit commit revision. Only the snippet's "HEAD"/"tip"
        (most recent) version can be updated and requests on all other,
        older revisions fail by returning a 405 status.

        Usage of this endpoint over the unrestricted `/snippets/encoded_id`
        could be desired if the caller wants to be sure no concurrent
        modifications have taken place between the moment of the UPDATE
        request and the original GET.

        This can be considered a so-called "Compare And Swap", or CAS
        operation.

        Other than that, the two endpoints are identical in behavior.
      operationId: putSnippetsUsernameEncodedNode
      x-api-path-slug: snippetsusernameencoded-idnode-id-put
      parameters:
      - in: path
        name: encoded_id
        description: The snippets id
      - in: path
        name: node_id
        description: A commit revision (SHA1)
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Node
  /snippets/{username}/{encoded_id}/{node_id}/files/{path}:
    get:
      summary: Get Snippets Username Encoded  Node  Files Path
      description: |-
        Retrieves the raw contents of a specific file in the snippet. The
        `Content-Disposition` header will be "attachment" to avoid issues with
        malevolent executable files.

        The file's mime type is derived from its filename and returned in the
        `Content-Type` header.

        Note that for text files, no character encoding is included as part of
        the content type.
      operationId: getSnippetsUsernameEncodedNodeFilesPath
      x-api-path-slug: snippetsusernameencoded-idnode-idfilespath-get
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Node
      - ""
      - Files
      - Path
    parameters:
      summary: Parameters Snippets Username Encoded  Node  Files Path
      description: Parameters snippets username encoded  node  files path
      operationId: parametersSnippetsUsernameEncodedNodeFilesPath
      x-api-path-slug: snippetsusernameencoded-idnode-idfilespath-parameters
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Node
      - ""
      - Files
      - Path
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---