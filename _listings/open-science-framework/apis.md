---
name: Open Science Framework
x-slug: open-science-framework
description: OSF provides free and open source project management support for researchers
  across the entire research lifecycle. As a collaboration tool, OSF helps researchers
  work on projects privately with a limited number of collaborators and make parts
  of their projects public, or make all the project publicly accessible for broader
  dissemination. As a workflow system, OSF enables connections to the many services
  researchers already use to streamline their process and increase efficiency. As
  a flexible repository, it can store and archive research data, protocols, and materials.
image: ""
x-kinRank: "7"
x-alexaRank: "0"
tags: Nodes
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/apis.md
specificationVersion: "0.14"
apis:
- name: Open Science Framework List all affiliated nodes
  x-api-slug: open-science-framework
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
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//institutions/{institution_id}/nodes/
  tags: Institutions,Institution,Nodes
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/institutionsinstitution-idnodes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/institutionsinstitution-idnodes-get-openapi.md
- name: Open Science Framework List all nodes
  x-api-slug: open-science-framework
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
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/
  tags: Nodes
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodes-get-openapi.md
- name: Open Science Framework Create a node
  x-api-slug: open-science-framework
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
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/
  tags: Nodes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodes-post-openapi.md
- name: Open Science Framework Delete a node
  x-api-slug: open-science-framework
  description: |-
    Permanently deletes a node. This action cannot be undone.
    #### Permissions
    Only project administrators may delete a node. Attempting to delete a node for which you are not an administrator will result in a **403 Forbidden** response.
    #### Returns
    If the request is successful, no content is returned.

    If the request is unsuccessful, a JSON object with an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/
  tags: Nodes,Node
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-id-delete-openapi.md
- name: Open Science Framework Retrieve a node
  x-api-slug: open-science-framework
  description: |-
    Retrieves the details of a given node (project or component).
    #### Permissions
    Only project contributors may retrieve the details of a private node. Attempting to retreive a private node for which you are not a contributor will result in a **403 Forbidden** response.

    Authentication is not required to view the details of a public node, as public nodes give read-only access to everyone.
    #### Returns
    Returns a JSON object with a `data` key containing the representation of the requested node, if the request is successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/
  tags: Nodes,Node
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-id-get-openapi.md
- name: Open Science Framework Update a node
  x-api-slug: open-science-framework
  description: |-
    Updates a node by setting the values of the attributes specified in the request body. Any unspecified attributes will be left unchanged.

    Nodes can be updated with either a **PUT** or **PATCH** request. The `title` and `category` fields are mandatory in a **PUT** request, and optional in a **PATCH**.
    #### Permissions
    Only write contributors may update a node. Attempting to update a node for which you do not have write access will result in a **403 Forbidden** response.
    #### Returns
    Returns a JSON object with a `data` key containing the new representation of the updated node, if the request is successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/
  tags: Nodes,Node
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-id-patch-openapi.md
- name: Open Science Framework List all addons
  x-api-slug: open-science-framework
  description: |-
    A paginated list of addons connected to the given node or project.
    #### Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of at most 10 addon objects. Each resource in the array is a separate addon object and contains the full representation of the addon, meaning additional requests to a addon's detail view are not necessary.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/addons/
  tags: Nodes,Node,Addons
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idaddons-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idaddons-get-openapi.md
- name: Open Science Framework Retrieve an addon
  x-api-slug: open-science-framework
  description: |-
    Retrieve details of an individual addon connected to this node.
    #### Permissions
    NodeSettings that are attached to public nodes will give read-only access to everyone. Private nodes require explicit read permission. Write and admin access are the same for public and private nodes. Administrators on a parent node have implicit read permissions for all child nodes.
    Any users with write or admin access to the node are able to deauthorize an enabled addon, but only the addon authorizer is able to change the configuration (i.e. selected folder) of an already-configured NodeSettings entity.
    #### Returns
    Returns a JSON object with a `data` key containing the details of the requested addon, if the request is successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/addons/{provider}/
  tags: Nodes,Node,Addons,Provider
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idaddonsprovider-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idaddonsprovider-get-openapi.md
- name: Open Science Framework Update an addon
  x-api-slug: open-science-framework
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
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/addons/{provider}/
  tags: Nodes,Node,Addons,Provider
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idaddonsprovider-patch-openapi.md
- name: Open Science Framework List all addon folders
  x-api-slug: open-science-framework
  description: |-
    A paginated list of folders retrieved from the associated third-party (provider) service.
    #### Permissions
    Folders are visible only to the user that authorized the addon.
    #### Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of addon folder objects. Each resource in the array is a separate addon folder object and contains the full representation of the addon folder, meaning additional requests to a addon folder's detail view are not necessary.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/addons/{provider}/folders/
  tags: Nodes,Node,Addons,Provider,Folders
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idaddonsproviderfolders-get-openapi.md
- name: Open Science Framework List all child nodes
  x-api-slug: open-science-framework
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
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/children/
  tags: Nodes,Node,Children
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idchildren-get-openapi.md
- name: Open Science Framework Create a child node
  x-api-slug: open-science-framework
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
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/children/
  tags: Nodes,Node,Children
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idchildren-post-openapi.md
- name: Open Science Framework Retrieve citation details
  x-api-slug: open-science-framework
  description: |-
    The citation details for a node, in CSL format.
    #### Returns
    Returns a JSON object with a `data` key that contains the representation of the details necessary for the node citation.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/citation/
  tags: Nodes,Node,Citation
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idcitation-get-openapi.md
- name: Open Science Framework Retrieve a styled citation
  x-api-slug: open-science-framework
  description: |-
    The citation for a node in a specific style.
    #### Returns
    Returns a JSON object with a `data` key that contains the representation of the node citation, in the requested style.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/citation/{style_id}/
  tags: Nodes,Node,Citation,Style
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idcitationstyle-id-get-openapi.md
- name: Open Science Framework List all comments
  x-api-slug: open-science-framework
  description: |-
    A paginated list of comments related to a given node.

    The returned comments are sorted by their creation date, with the most recent comments appearing first.
    ####Permissions
    Comments on public nodes are given read-only access to everyone.

    If the node comment-level is `private`, only contributors have permission to comment.

    If the comment-level is `public`, any logged-in OSF user can comment.

    Comments on private nodes are only visible to contributors and administrators on the parent node.
    ####Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of comment objects. Each resource in the array is a separate comment object.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
    #### Filtering
    You can optionally request that the response only include comments that match your filters by utilizing the `filter` query parameter, e.g. https://api.osf.io/v2/nodes/ezcuj/comments/?filter[target_id]=jg7sezmdnt93

    Nodes may be filtered by their `deleted`, `target_id`, `date_created`, `date_modified`.

    Most fields are string fields and will be filtered using simple substring matching. Public and preprint are boolean fields, and can be filtered using truthy values, such as **true**, **false**, **0** or **1**. Note that quoting `true` or `false` in the query will cause the match to fail.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/comments/
  tags: Nodes,Node,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idcomments-get-openapi.md
- name: Open Science Framework Create a comment
  x-api-slug: open-science-framework
  description: |-
    Create a comment on a given node overview page or a reply to a comment on that node.

    To create a comment on the node overview page, the target `type` would be "nodes" and the target `id` would be the node `id`.

    To reply to a comment on this node, the target `type` would be "comments" and the target `id` would be the `id` of the comment to reply to.
    ####Required
    A relationship object with a `data` key, containing the target (`comments` or `nodes`) type and a target `id` is required.
    In addition, the `content` attribute describing the relationship between the node and the comment is required.
    ####Returns
    Returns a JSON object with a data key containing the representation of the new comment, if the request is successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/comments/
  tags: Nodes,Node,Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idcomments-post-openapi.md
- name: Open Science Framework List all contributors
  x-api-slug: open-science-framework
  description: |-
    A paginated list of the node's contributors, sorted by their index.

    Contributors are users who can make changes to the node or, in the case of private nodes, have read access to the node.

    Contributors are categorized as either "bibliographic" or "non-bibliographic". From a permissions standpoint, both are the same, but bibliographic contributors are included in citations and are listed on the project overview page on the OSF, while non-bibliographic contributors are not.

    Note that if an anonymous view_only key is being used to view the list of contributors, the user relationship will not be exposed and the contributor ID will be an empty string.

    #### Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of 10 contributors. Each resource in the array contains the full representation of the contributor, meaning additional requests to a contributor's detail view are not necessary. Additionally, the full representation of the user this contributor represents is automatically embedded within the `data` key of the response.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
    #### Filtering
    You can optionally request that the response only include contributors that match your filters by utilizing the `filter` query parameter, e.g. https://api.osf.io/v2/nodes/y9jdt/contributors/?filter[bibliographic]=true.

    Contributors may be filtered by their `bibliographic` and `permission` attributes.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/contributors/
  tags: Nodes,Node,Contributors
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idcontributors-get-openapi.md
- name: Open Science Framework Create a contributor
  x-api-slug: open-science-framework
  description: |-
    Adds a contributor to a node, effectively creating a relationship between the node and a user.

    Contributors are users who can make changes to the node or, in the case of private nodes, have read access to the node.

    Contributors are categorized as either "bibliographic" or "non-bibliographic" contributors. From a permissions standpoint, both are the same, but bibliographic contributors are included in citations and are listed on the project overview page on the OSF, while non-bibliographic contributors are not.
    #### Permissions
    Only project administrators can add contributors to a node.
    #### Required
    A relationship object with a `data` key, containing the `users` type and valid user ID is required.

    All attributes describing the relationship between the node and the user are optional.
    #### Returns
    Returns a JSON object with a `data` key containing the representation of the new contributor, if the request is successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/contributors/
  tags: Nodes,Node,Contributors
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idcontributors-post-openapi.md
- name: Open Science Framework Delete a contributor
  x-api-slug: open-science-framework
  description: |-
    Removes a contributor from a node. This request only removes the relationship between the node and the user, it does not delete the user itself.

    A node must always have at least one admin, and attempting to remove the only admin from a node will result in a **400 Bad Request** response.
    #### Permissions
    A user can remove themselves as a node contributor. Otherwise, only project administrators can remove contributors.
    #### Returns
    If the request is successful, no content is returned.

    If the request is unsuccessful, a JSON object with an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/contributors/{user_id}/
  tags: Nodes,Node,Contributors,User
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idcontributorsuser-id-delete-openapi.md
- name: Open Science Framework Retrieve a contributor
  x-api-slug: open-science-framework
  description: |-
    Retrieves the details of a given contributor.

    Contributors are users who can make changes to the node or, in the case of private nodes, have read access to the node.

    Contributors are categorized as either "bibliographic" or "non-bibliographic". From a permissions standpoint, both are the same, but bibliographic contributors are included in citations and are listed on the project overview page on the OSF, while non-bibliographic contributors are not.
    #### Returns
    Returns a JSON object with a `data` key containing the representation of the requested contributor, if the request is successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/contributors/{user_id}/
  tags: Nodes,Node,Contributors,User
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idcontributorsuser-id-get-openapi.md
- name: Open Science Framework Update a contributor
  x-api-slug: open-science-framework
  description: |-
    Updates a contributor by setting the values of the attributes specified in the request body. Any unspecified attributes will be left unchanged.

    Contributors can be updated with either a **PUT** or **PATCH** request. Since this endpoint has no mandatory attributes, PUT and PATCH are functionally the same.
    #### Permissions
    Only project administrators can update the contributors on a node.
    #### Returns
    Returns a JSON object with a `data` key containing the new representation of the updated contributor, if the request is successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.

    If the given user is not already in the contributor list, a 404 Not Found error will be returned. A node must always have at least one admin, and any attempt to downgrade the permissions of a sole admin will result in a 400 Bad Request error.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/contributors/{user_id}/
  tags: Nodes,Node,Contributors,User
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idcontributorsuser-id-patch-openapi.md
- name: Open Science Framework List all draft registrations
  x-api-slug: open-science-framework
  description: |-
    A paginated list of all of the draft registrations of a given node.

    Draft registrations contain the supplemental registration questions that accompany a registration. A registration is a frozen version of the project that can never be edited or deleted, but can be withdrawn.

    Your original project remains editable but will now have the draft registration linked to it.
    #### Permissions
    Only project administrators may view draft registrations.
    #### Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of 10 draft registrations. Each resource in the array is a separate draft registration object and contains the full representation of the draft registration, meaning additional requests to a draft registration's detail view are not necessary.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/draft_registrations/
  tags: Nodes,Node,Draft,Registrations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-iddraft-registrations-get-openapi.md
- name: Open Science Framework Create a draft registration
  x-api-slug: open-science-framework
  description: |-
    Initiate a draft registration of the current node.
    Draft registrations contain the supplemental registration questions that accompany a registration. A registration is a frozen version of the project that can never be edited or deleted, but can be withdrawn.

    Your original project remains editable but will now have the draft registration linked to it.
    #### Permissions
    Only project administrators may view create registrations.
    #### Required
    Required fields for creating a draft registration include:

    &nbsp;&nbsp;&nbsp;&nbsp`registration_supplement`
    #### Returns
    Returns a JSON object with a `data` key containing the representation of the created draft registration, if the request is successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/draft_registrations/
  tags: Nodes,Node,Draft,Registrations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-iddraft-registrations-post-openapi.md
- name: Open Science Framework Delete a draft registration
  x-api-slug: open-science-framework
  description: |-
    Permanently deletes a draft registration. A draft that has already been registered cannot be deleted.
    #### Permissions
    Only project administrators may delete draft registrations.
    #### Returns
    If the request is successful, no content is returned.

    If the request is unsuccessful, a JSON object with an `errors` key containing information about the failure will be returned. Refer to the [list of error codes]() to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/draft_registrations/{draft_id}/
  tags: Nodes,Node,Draft,Registrations,Draft
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-iddraft-registrationsdraft-id-delete-openapi.md
- name: Open Science Framework Retrieve a draft registration
  x-api-slug: open-science-framework
  description: |-
    Retrieve the details of a given draft registration.
    Draft registrations contain the supplemental registration questions that accompany a registration. A registration is a frozen version of the project that can never be edited or deleted, but can be withdrawn.

    Your original project remains editable but will now have the draft registration linked to it.
    #### Permissions
    Only project administrators may view draft registrations.
    #### Returns
    Returns a JSON object with a `data` key containing the representation of the requested draft registration, if the request is successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/draft_registrations/{draft_id}/
  tags: Nodes,Node,Draft,Registrations,Draft
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-iddraft-registrationsdraft-id-get-openapi.md
- name: Open Science Framework Update a draft registration
  x-api-slug: open-science-framework
  description: |-
    Updates a draft registration by setting the values of the attributes specified in the request body. Any unspecified attributes will be left unchanged.

    Draft registrations contain the supplemental registration questions that accompany a registration. Answer the questions in the draft registration supplement by sending update requests until you are ready to submit the draft.

    The registration supplement of a draft registration cannot be updated after the draft has been created.

    When updating a draft registration, `registration_metadata` is required. It must be a dictionary with keys as question ids in the registration form, and values as nested dictionaries matching the specific format in the [registration schema](TODO: link me pls).

    If a question is multiple-choice, the question response must exactly match one of the possible choices.
    #### Permissions
    Only project administrators may update draft registrations.
    #### Returns
    Returns a JSON object with a `data` key containing the new representation of the updated draft registration, if the request is successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/draft_registrations/{draft_id}/
  tags: Nodes,Node,Draft,Registrations,Draft
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-iddraft-registrationsdraft-id-patch-openapi.md
- name: Open Science Framework List all storage providers
  x-api-slug: open-science-framework
  description: |-
    List of all storage providers that are configured for this node

    Users of the OSF may access their data on a [number of cloud-storage services](https://api.osf.io/v2/#storage-providers) that have integrations with the OSF. We call these **providers**. By default, every node has access to the OSF-provided storage but may use as many of the supported providers as desired.


    ####Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of files. Each resource in the array is a separate file object.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).

    Note: In the OSF filesystem model, providers are treated as folders, but with special properties that distinguish them from regular folders. Every provider folder is considered a root folder, and may not be deleted through the regular file API.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/files/
  tags: Nodes,Node,Files
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idfiles-get-openapi.md
- name: Open Science Framework Retrieve a storage provider
  x-api-slug: open-science-framework
  description: |-
    Retrieves the details of a storage provider enabled on this node.
    ####Returns
    Returns a JSON object with a `data` key containing the representation of the requested file object, if the request is successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/files/providers/{provider}/
  tags: Nodes,Node,Files,Providers,Provider
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idfilesprovidersprovider-get-openapi.md
- name: Open Science Framework List all node files
  x-api-slug: open-science-framework
  description: |-
    List of all the files/folders that are attached to your project for a given storage provider.
    ####Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of files. Each resource in the array is a separate file object and contains the full representation of the file.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).

    ####Filtering

    You can optionally request that the response only include files that match your filters by utilizing the `filter` query parameter, e.g. https://api.osf.io/v2/nodes/ezcuj/files/osfstorage/?filter[kind]=file

    Node files may be filtered by `id`, `name`, `node`, `kind`, `path`, `provider`, `size`, and `last_touched`.

    ###Waterbutler API actions

    Files can be modified through the Waterbutler API routes found in `links` (`new_folder`, `move`, `upload`, `download`, and `delete`).

    #### Download (files)

    To download a file, issue a GET request against the download link. The response will have the Content-Disposition header set, which will will trigger a download in a browser.

    #### Create Subfolder (folders)

    You can create a subfolder of an existing folder by issuing a PUT request against the new_folder link. The ?kind=folder portion of the query parameter is already included in the new_folder link. The name of the new subfolder should be provided in the name query parameter. The response will contain a WaterButler folder entity. If a folder with that name already exists in the parent directory, the server will return a 409 Conflict error response.

    #### Upload New File (folders)

    To upload a file to a folder, issue a PUT request to the folder's upload link with the raw file data in the request body, and the kind and name query parameters set to 'file' and the desired name of the file. The response will contain a WaterButler file entity that describes the new file. If a file with the same name already exists in the folder, the server will return a 409 Conflict error response.

    #### Update Existing File (file)

    To update an existing file, issue a PUT request to the file's upload link with the raw file data in the request body and the kind query parameter set to "file". The update action will create a new version of the file. The response will contain a WaterButler file entity that describes the updated file.

    #### Rename (files, folders)

    To rename a file or folder, issue a POST request to the move link with the action body parameter set to "rename" and the rename body parameter set to the desired name. The response will contain either a folder entity or file entity with the new name.

    #### Move & Copy (files, folders)

    Move and copy actions both use the same request structure, a POST to the move url, but with different values for the action body parameters. The path parameter is also required and should be the OSF path attribute of the folder being written to. The rename and conflict parameters are optional. If you wish to change the name of the file or folder at its destination, set the rename parameter to the new name. The conflict param governs how name clashes are resolved. Possible values are replace and keep. replace is the default and will overwrite the file that already exists in the target folder. keep will attempt to keep both by adding a suffix to the new file's name until it no longer conflicts. The suffix will be ' (x)' where x is a increasing integer starting from 1. This behavior is intended to mimic that of the OS X Finder. The response will contain either a folder entity or file entity with the new name.
    Files and folders can also be moved between nodes and providers. The resource parameter is the id of the node under which the file/folder should be moved. It must agree with the path parameter, that is the path must identify a valid folder under the node identified by resource. Likewise, the provider parameter may be used to move the file/folder to another storage provider, but both the resource and path parameters must belong to a node and folder already extant on that provider. Both resource and provider default to the current node and providers.
    If a moved/copied file is overwriting an existing file, a 200 OK response will be returned. Otherwise, a 201 Created will be returned.

    #### Delete (file, folders)

    To delete a file or folder send a DELETE request to the delete link. Nothing will be returned in the response body.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/files/{provider}/
  tags: Nodes,Node,Files,Provider
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idfilesprovider-get-openapi.md
- name: Open Science Framework Retrieve a file
  x-api-slug: open-science-framework
  description: |-
    Retrieves the details of a file attached to given node (project or component) for the given storage provider.
    ####Returns
    Returns a JSON object with a `data` key containing the representation of the requested file object, if the request is successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/files/{provider}/{path}/
  tags: Nodes,Node,Files,Provider,Path
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idfilesproviderpath-get-openapi.md
- name: Open Science Framework List all forks of this node
  x-api-slug: open-science-framework
  description: |-
    A paginated list of the current node's forks. The returned fork nodes are sorted by their `forked_date`, with the most recently forked nodes appearing first.

    Forking a project creates a copy of an existing node and all of its contents. The fork always points back to the original node, forming a network of nodes.
    #### Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of up to 10 forked nodes. If the current node has zero forked nodes, the `data` key will contain an empty array. Each resource in the array is a separate node object and contains the full representation of the forked node, meaning additional requests to the forked node's detail view are not necessary.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).

    This request should never return an error.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/forks/
  tags: Nodes,Node,Forks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idforks-get-openapi.md
- name: Open Science Framework Create a fork of this node
  x-api-slug: open-science-framework
  description: |-
    Creates a fork of the given node.

    Forking a project creates a copy of an existing node and all of its contents. The fork always points back to the original node, forming a network of nodes.

    You might use a fork to copy another's work to build on and extend. For example, a professor may create an OSF project of materials for individual student use. Each student forks the project to have his or her own copy of the materials to start his/her own work.

    When creating a fork, your fork will only contain public components of the current node and components for which you are a contributor. Private components that you do not have access to will not be forked.
    #### Required
    There are no required attributes when creating a fork, as all of the forked node's attributes will be copied from the current node.

    The `title` field is optional, with the default title being "Fork of " prepended to the current node's title.
    #### Returns
    Returns a JSON object with a `data` key containing the complete srepresentation of the forked node, if the request is successful.
    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/forks/
  tags: Nodes,Node,Forks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idforks-post-openapi.md
- name: Open Science Framework List all identifiers
  x-api-slug: open-science-framework
  description: |-
    List all identifiers associated with a given node.
    ####Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of identifiers. Each resource in the array is a separate identifier object.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
    ####Filtering

    You can optionally request that the response only include nodes that match your filters by utilizing the `filter` query parameter, e.g. https://api.osf.io/v2/nodes/ezcuj/identifiers/?filter[category]=ark

    Identifiers may be filtered by their `category` e.g `ark` or `doi`.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/identifiers/
  tags: Nodes,Nodeentifiers
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-ididentifiers-get-openapi.md
- name: Open Science Framework List all institutions
  x-api-slug: open-science-framework
  description: |-
    List of all institutions affiliated with this node.
    ####Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of up to 10 affilited institutions. Each resource in the array is a separate institution object.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/institutions/
  tags: Nodes,Node,Institutions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idinstitutions-get-openapi.md
- name: Open Science Framework List all linked nodes
  x-api-slug: open-science-framework
  description: |-
    List of all nodes linked to the given node.
    ####Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of up to 10 nodes. Each resource in the array is a separate node object.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
    ####Filtering
    You can optionally request that the response only include nodes that match your filters by utilizing the `filter` query parameter, e.g. https://api.osf.io/v2/nodes/?filter[title]=reproducibility.

    Nodes may be filtered by their `title`, `category`, `description`, `public`, `registration`, or `tags`. `title`, `description`, and `category` are string fields and will be filteres using simple substring matching. `public`, `registration` are boolean and can be filtered using truthy values, such as `true`, `false`, `0`, `1`. `tags` is an array of simple strings.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/linked_nodes/
  tags: Nodes,Node,Linked,Nodes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idlinked-nodes-get-openapi.md
- name: Open Science Framework List all logs
  x-api-slug: open-science-framework
  description: |-
    A paginated list of all logs associated with a given node.

    The returned logs are sorted by their `date`, with the most recents logs appearing first.

    This list includes the logs of the specified node as well as the logs of that node's children to which the current user has read-only access.

    ####Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of up to 10 logs. Each resource in the array is a separate logs object.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
    ####Filtering
    You can optionally request that the response only include logs that match your filters by utilizing the `filter` query parameter, e.g. https://api.osf.io/v2/nodes/ezcuj/logs/?filter[action]=made_private.

    Nodes may be filtered by their `action`, and `date`.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/logs/
  tags: Nodes,Node,Logs
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idlogs-get-openapi.md
- name: Open Science Framework List all preprints
  x-api-slug: open-science-framework
  description: |-
    A paginated list of preprints related to a given node. The returned preprints are sorted by their creation date, with the most recent preprints appearing first.

    **Note: This API endpoint is under active development, and is subject to change in the future.**
    #### Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of up to 10 preprints. Each resource in the array is a separate preprint object.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/preprints/
  tags: Nodes,Node,Preprints
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idpreprints-get-openapi.md
- name: Open Science Framework List all registrations
  x-api-slug: open-science-framework
  description: |-
    List of all registrations of the given node.
    ####Returns

    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of up to 10 registrations. Each resource in the array is a separate registrations object.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
    ####Filtering

    You can optionally request that the response only include registrations that match your filters by utilizing the filter query parameter, e.g. https://api.osf.io/v2/registrations/?filter[title]=open.

    Registrations may be filtered by their `id`, `title`, `category`, `description`, `public`, `tags`, `date_created`, `date_modified`, `root`, `parent`, and `contributors`.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/registrations/
  tags: Nodes,Node,Registrations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idregistrations-get-openapi.md
- name: Open Science Framework List all view only links
  x-api-slug: open-science-framework
  description: |-
    List of view only links on a node.
    ####Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of up to 10 view only links. Each resource in the array is a view only link object.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).

    ####Permissions

    View only links on a node, public or private, are readable and writeable only by users that are administrators on the node.

    ####Filtering

    You can optionally request that the response only include view only links that match your filters by utilizing the `filter` query parameter, e.g. https://api.osf.io/v2/nodes/ezcuj/view_only_links/?filter[anonymous]=true.

    View Only Links may be filtered based on their `name`, `anonymous` and `date_created` fields. Possible comparison operators include 'gt' (greater than), 'gte'(greater than or equal to), 'lt' (less than) and 'lte' (less than or equal to). The date must be in the format YYYY-MM-DD and the time is optional.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/view_only_links/
  tags: Nodes,Node,View,Only,Links
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idview-only-links-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idview-only-links-get-openapi.md
- name: Open Science Framework Retrieve a view only link
  x-api-slug: open-science-framework
  description: |-
    Retrieves the details of a view only link on a node.
    ####Returns
    Returns a JSON object with a `data` key containing the representation of the requested view only link, if the request is successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
    ####Permissions

    View only links on a node, public or private, are readable and writeable only by users that are administrators on the node.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/view_only_links/{link_id}/
  tags: Nodes,Node,View,Only,Links,Link
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idview-only-linkslink-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idview-only-linkslink-id-get-openapi.md
- name: Open Science Framework List all wikis
  x-api-slug: open-science-framework
  description: |-
    List of wiki pages on a node.
    ####Returns
    Paginated list of the node's current wiki page versions ordered by their date_modified. Each resource contains the full representation of the wiki, meaning additional requests to an individual wiki's detail view are not necessary.

    Note that if an anonymous view_only key is being used, the user relationship will not be exposed.

    If the request is unsuccessful, a JSON object with an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
    #### Filtering
    Wiki pages can be filtered based on their `name` and `date_modified` fields.
    + `filter[name]=<Str>` -- filter wiki pages by name
    + `filter[date_modified][comparison_operator]=YYYY-MM-DDTH:M:S` -- filter wiki pages based on date modified.

    Possible comparison operators include 'gt' (greater than), 'gte'(greater than or equal to), 'lt' (less than) and 'lte' (less than or equal to). The date must be in the format YYYY-MM-DD and the time is optional.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//nodes/{node_id}/wikis/
  tags: Nodes,Node,Wikis
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/nodesnode-idwikis-get-openapi.md
- name: Open Science Framework List all linked nodes
  x-api-slug: open-science-framework
  description: |-
    List of all nodes linked to the registration.
    ####Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of up to 10 nodes. Each resource in the array is a separate node object.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
    ####Filtering
    You can optionally request that the response only include nodes that match your filters by utilizing the `filter` query parameter, e.g. https://api.osf.io/v2/registrations/wucr8/linked_nodes/?filter[title]=reproducibility/?filter[title]=reproducibility.

    Nodes may be filtered by their `title`, `category`, `description`, `public`, `registration`, or `tags`. `title`, `description`, and `category` are string fields and will be filteres using simple substring matching. `public`, `registration` are boolean and can be filtered using truthy values, such as `true`, `false`, `0`, `1`. `tags` is an array of simple strings.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//registrations/{registration_id}/linked_nodes/
  tags: Registrations,Registration,Linked,Nodes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/registrationsregistration-idlinked-nodes-get-openapi.md
- name: Open Science Framework List all nodes
  x-api-slug: open-science-framework
  description: |-
    A paginated list of nodes that the user is a contributor to. The returned nodes are sorted by their `date_modified`, with the most recently updated nodes appearing first.

    If the user ID in the path is the same as the logged-in user, all nodes will be returned. Otherwise, only the user's public nodes will be returned.

    User registrations are not available at this endpoint.
    #### Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of 10 nodes. Each resource in the array is a separate node object and contains the full representation of the node, meaning additional requests to a node's detail view are not necessary.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).
    #### Filtering
    You can optionally request that the response only include nodes that match your filters by utilizing the `filter` query parameter, e.g. https://api.osf.io/v2/users/cdi38/nodes/?filter[title]=open.

    Nodes may be filtered by their `id`, `title`, `category`, `description`, `public`, `tags`, `date_created`, `date_modified`, `root`, `parent`, `preprint`, and `contributors`.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//users/{user_id}/nodes/
  tags: Users,User,Nodes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/usersuser-idnodes-get-openapi.md
- name: Open Science Framework List all nodes
  x-api-slug: open-science-framework
  description: |-
    The list of nodes which this view only link gives read-only access to.
    #### Permissions
    Only project administrators may retrieve the nodes of a view only link. Attempting to retrieve a view only link without appropriate permissions will result in a 403 Forbidden response.
    #### Returns
    Returns a JSON object containing `data` and `links` keys.
    The `data` key contains an array of up to 10 nodes. Each resource in the array is a separate node object and contains the full representation of the node, meaning additional requests to a node's detail view are not necessary.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//view_only_links/{link_id}/nodes/
  tags: View,Only,Links,Link,Nodes
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/view-only-linkslink-idnodes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/view-only-linkslink-idnodes-get-openapi.md
- name: Open Science Framework
  x-api-slug: open-science-framework
  description: OSF provides free and open source project management support for researchers
    across the entire research lifecycle. As a collaboration tool, OSF helps researchers
    work on projects privately with a limited number of collaborators and make parts
    of their projects public, or make all the project publicly accessible for broader
    dissemination. As a workflow system, OSF enables connections to the many services
    researchers already use to streamline their process and increase efficiency. As
    a flexible repository, it can store and archive research data, protocols, and
    materials.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2
  tags: Nodes
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/open-science-framework/openapi.md
x-common:
- type: x-website
  url: https://cos.io
- type: x-github
  url: https://github.com/OSFramework
- type: x-twitter
  url: https://twitter.com/OSFramework
- type: x-website
  url: http://osf.io
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---