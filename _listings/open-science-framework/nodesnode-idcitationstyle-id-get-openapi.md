---
swagger: "2.0"
x-collection-name: Open Science Framework
x-complete: 0
info:
  title: Open Science Framework Retrieve a styled citation
  description: |-
    The citation for a node in a specific style.
    #### Returns
    Returns a JSON object with a `data` key that contains the representation of the node citation, in the requested style.
  contact:
    name: OSF
    url: https://osf.io/support
    email: support@osf.io
  version: "2.0"
host: test-api.osf.io
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /institutions/{institution_id}/nodes/:
    get:
      summary: List all affiliated nodes
      description: |-
        A paginated list of all nodes affiliated with an institution.
        #### Versioning
        As of version `2.2`, affiliated components (in addition to affiliated top-level projects) are returned from this endpoint.
        #### Returns
        Returns a JSON object containing `data` and `links` keys.

        The `data` key contains an array of 10 nodes. Each resource in the array is a separate nodes object.

        The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).

        If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
        #### Filtering
        You can optionally request that the response only include nodes that match your filters by utilizing the `filter` query parameter, e.g. https://api.osf.io/v2/institutions/cos/nodes?filter[title]=science.

        Nodes may be filtered by their `id`, `title`, `description`, `public`, `tags`, `category`, `date_created`, `date_modified`, `root`, `parent`, `contributors`, and `preprint`
      operationId: institutions_node_list
      x-api-path-slug: institutionsinstitution-idnodes-get
      parameters:
      - in: path
        name: institution_id
        description: The unique identifier of the institution you wish to retrieve
      responses:
        200:
          description: OK
      tags:
      - Institutions
      - Institution
      - Nodes
  /nodes/:
    get:
      summary: List all nodes
      description: |-
        A paginated list of nodes, representing projects and components, on the OSF.

        The returned nodes are those which are public or which the user has access to view.

        The returned nodes are sorted by their `date_modified`, with the most recently updated nodes appearing first.

        Registrations cannot be accessed through this endpoint (use the [registrations](#Registrations_registrations_list) endpoints instead).
        #### Returns
        Returns a JSON object containing `data` and `links` keys.

        The `data` key contains an array of 10 nodes. Each resource in the array is a separate node object and contains the full representation of the node, meaning additional requests to a node's detail view are not necessary.

        The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).

        This request should never return an error.
        #### Filtering
        You can optionally request that the response only include nodes that match your filters by utilizing the `filter` query parameter, e.g. https://api.osf.io/v2/nodes/?filter[title]=reproducibility.

        Nodes may be filtered by their `id`, `title`, `category`, `description`, `public`, `tags`, `date_created`, `date_modified`, `root`, `parent`, `preprint`, and `contributors`.

        Most fields are string fields and will be filtered using simple substring matching. Public and preprint are boolean fields, and can be filtered using truthy values, such as **true**, **false**, **0** or **1**. Note that quoting true or false in the query will cause the match to fail.
      operationId: nodes_list
      x-api-path-slug: nodes-get
      responses:
        200:
          description: OK
      tags:
      - Nodes
    post:
      summary: Create a node
      description: |-
        Creates a new node.

        On the OSF, nodes are considered **projects** or **components**. The difference between a project and a component is that a project is a top-level node, and a component is a child of a project.

        Additionally, nodes have a `category` field that includes **project** as an option. The categorization determines what icon is displayed with the node on the OSF, and helps with search organization. Projects (top-level nodes) may have a category other than project, and components (children) may have a category of **project**.
        #### Required
        Required fields for creating a node include:

        &nbsp;&nbsp;&nbsp;&nbsp`title`

        &nbsp;&nbsp;&nbsp;&nbsp`category`

        Note: Nodes default to **private** unless the `public` field is explicitly set to **true** in the request payload.
        #### Returns
        Returns a JSON object with a `data` key containing the representation of the created node, if the request is successful.

        If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
      operationId: nodes_create
      x-api-path-slug: nodes-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Nodes
  /nodes/{node_id}/:
    delete:
      summary: Delete a node
      description: |-
        Permanently deletes a node. This action cannot be undone.
        #### Permissions
        Only project administrators may delete a node. Attempting to delete a node for which you are not an administrator will result in a **403 Forbidden** response.
        #### Returns
        If the request is successful, no content is returned.

        If the request is unsuccessful, a JSON object with an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
      operationId: nodes_delete
      x-api-path-slug: nodesnode-id-delete
      parameters:
      - in: path
        name: node_id
        description: The unique identifier of the node
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Node
    get:
      summary: Retrieve a node
      description: |-
        Retrieves the details of a given node (project or component).
        #### Permissions
        Only project contributors may retrieve the details of a private node. Attempting to retreive a private node for which you are not a contributor will result in a **403 Forbidden** response.

        Authentication is not required to view the details of a public node, as public nodes give read-only access to everyone.
        #### Returns
        Returns a JSON object with a `data` key containing the representation of the requested node, if the request is successful.

        If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
      operationId: nodes_read
      x-api-path-slug: nodesnode-id-get
      parameters:
      - in: path
        name: node_id
        description: The unique identifier of the node
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Node
    patch:
      summary: Update a node
      description: |-
        Updates a node by setting the values of the attributes specified in the request body. Any unspecified attributes will be left unchanged.

        Nodes can be updated with either a **PUT** or **PATCH** request. The `title` and `category` fields are mandatory in a **PUT** request, and optional in a **PATCH**.
        #### Permissions
        Only write contributors may update a node. Attempting to update a node for which you do not have write access will result in a **403 Forbidden** response.
        #### Returns
        Returns a JSON object with a `data` key containing the new representation of the updated node, if the request is successful.

        If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
      operationId: nodes_partial_update
      x-api-path-slug: nodesnode-id-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: node_id
        description: The unique identifier of the node
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Node
  /nodes/{node_id}/addons/:
    get:
      summary: List all addons
      description: |-
        A paginated list of addons connected to the given node or project.
        #### Returns
        Returns a JSON object containing `data` and `links` keys.

        The `data` key contains an array of at most 10 addon objects. Each resource in the array is a separate addon object and contains the full representation of the addon, meaning additional requests to a addon's detail view are not necessary.

        The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
      operationId: nodes_addons_list
      x-api-path-slug: nodesnode-idaddons-get
      parameters:
      - in: path
        name: node_id
        description: The unique identifier of the node
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Node
      - Addons
  /nodes/{node_id}/addons/{provider}/:
    get:
      summary: Retrieve an addon
      description: |-
        Retrieve details of an individual addon connected to this node.
        #### Permissions
        NodeSettings that are attached to public nodes will give read-only access to everyone. Private nodes require explicit read permission. Write and admin access are the same for public and private nodes. Administrators on a parent node have implicit read permissions for all child nodes.
        Any users with write or admin access to the node are able to deauthorize an enabled addon, but only the addon authorizer is able to change the configuration (i.e. selected folder) of an already-configured NodeSettings entity.
        #### Returns
        Returns a JSON object with a `data` key containing the details of the requested addon, if the request is successful.

        If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
      operationId: nodes_addon_read
      x-api-path-slug: nodesnode-idaddonsprovider-get
      parameters:
      - in: path
        name: node_id
        description: The unique identifier of the node
      - in: path
        name: provider
        description: The unique identifier of the addon
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Node
      - Addons
      - Provider
    patch:
      summary: Update an addon
      description: |-
        Updates a node addon by setting the values of the attributes specified in the request body. Any unspecified attributes will be left unchanged.

        Node addon can be updated with either a **PUT** or **PATCH** request. The `external_account_id`, `enabled`, and `folder_id` fields are mandatory in a **PUT**, and optional in **PATCH**. Non-string values will be accepted and stringified, however we make no promises about the stringification output.

        To delete or deauthorize a node addon, issue a **PUT** with all fields set to `null` or `False`, or a **PATCH** with enabled set `False`.
        #### Permissions
        NodeSettings that are attached to public nodes will give read-only access to everyone. Private nodes require explicit read permission. Write and admin access are the same for public and private nodes. Administrators on a parent node have implicit read permissions for all child nodes.
        Any users with write or admin access to the node are able to deauthorize an enabled addon, but only the addon authorizer is able to change the configuration (i.e. selected folder) of an already-configured NodeSettings entity.

        #### Returns
        Returns a JSON object with a `data` key containing the new representation of the updated node addon, if the request is successful.

        If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
      operationId: nodes_node_addon_update
      x-api-path-slug: nodesnode-idaddonsprovider-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: node_id
        description: The unique identifier of the node
      - in: path
        name: provider
        description: The unique identifier of the addon
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Node
      - Addons
      - Provider
  /nodes/{node_id}/addons/{provider}/folders/:
    get:
      summary: List all addon folders
      description: |-
        A paginated list of folders retrieved from the associated third-party (provider) service.
        #### Permissions
        Folders are visible only to the user that authorized the addon.
        #### Returns
        Returns a JSON object containing `data` and `links` keys.

        The `data` key contains an array of addon folder objects. Each resource in the array is a separate addon folder object and contains the full representation of the addon folder, meaning additional requests to a addon folder's detail view are not necessary.

        The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
      operationId: nodes_addons_folders_list
      x-api-path-slug: nodesnode-idaddonsproviderfolders-get
      parameters:
      - in: path
        name: node_id
        description: The unique identifier of the node
      - in: path
        name: provider
        description: The unique identifier of the provider
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Node
      - Addons
      - Provider
      - Folders
  /nodes/{node_id}/children/:
    get:
      summary: List all child nodes
      description: |-
        A paginated list of the next level child nodes for the given node. The returned nodes are sorted by their `date_modified`, with the most recently updated child nodes appearing first.

        The list will include child nodes that are public, as well as child nodes that are private, if the authenticated user has permission to view them.
        #### Returns
        Returns a JSON object containing `data` and `links` keys.

        The `data` key contains an array of up to 10 child nodes. If the given node has zero child nodes, the `data` key will contain an empty array. Each resource in the array is a separate node object and contains the full representation of the child node, meaning additional requests to the child node's detail view are not necessary.

        The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).

        This request should never return an error.
        #### Filtering
        You can optionally request that the response only include nodes that match your filters by utilizing the `filter` query parameter, e.g. https://api.osf.io/v2/nodes/ezcuj/children/?filter[title]=reproducibility.

        Nodes may be filtered by their `id`, `title`, `category`, `description`, `public`, `tags`, `date_created`, `date_modified`, `root`, `parent`, `preprint`, and `contributors`.

        Most fields are string fields and will be filtered using simple substring matching. Public and preprint are boolean fields, and can be filtered using truthy values, such as **true**, **false**, **0** or **1**. Note that quoting true or false in the query will cause the match to fail.
      operationId: nodes_children_list
      x-api-path-slug: nodesnode-idchildren-get
      parameters:
      - in: path
        name: node_id
        description: The unique identifier of the node
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Node
      - Children
    post:
      summary: Create a child node
      description: |-
        Creates a new child node.

        Note: Creating a child node via this endpoint will function the same as creating a node via the node list endpoint, but the child node will have the given node set as its parent.
        #### Permissions
        Only write contributors may create children nodes.
        #### Required
        Required fields for creating a node include:

        &nbsp;&nbsp;&nbsp;&nbsp`title`

        &nbsp;&nbsp;&nbsp;&nbsp`category`

        Note: nodes default to **private** unless the `public` field is explicitly set to **true** in the request payload.
        #### Returns
        Returns a JSON object with a `data` key containing the representation of the created node, if the request is successful.

        If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
      operationId: nodes_children_create
      x-api-path-slug: nodesnode-idchildren-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: node_id
        description: The unique identifier of the node
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Node
      - Children
  /nodes/{node_id}/citation/:
    get:
      summary: Retrieve citation details
      description: |-
        The citation details for a node, in CSL format.
        #### Returns
        Returns a JSON object with a `data` key that contains the representation of the details necessary for the node citation.
      operationId: nodes_citation_list
      x-api-path-slug: nodesnode-idcitation-get
      parameters:
      - in: path
        name: node_id
        description: The unique identifier of the node
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Node
      - Citation
  /nodes/{node_id}/citation/{style_id}/:
    get:
      summary: Retrieve a styled citation
      description: |-
        The citation for a node in a specific style.
        #### Returns
        Returns a JSON object with a `data` key that contains the representation of the node citation, in the requested style.
      operationId: nodes_citation_read
      x-api-path-slug: nodesnode-idcitationstyle-id-get
      parameters:
      - in: path
        name: node_id
        description: The unique identifier of the node
      - in: path
        name: style_id
        description: The unique identifier of the citation style
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Node
      - Citation
      - Style
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