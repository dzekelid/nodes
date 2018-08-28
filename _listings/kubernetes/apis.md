---
name: Kubernetes
x-slug: kubernetes
description: Manage a cluster of Linux containers as a single system to accelerate
  Dev and simplify Ops. Kubernetes is an open source orchestration system for Docker
  containers. It handles scheduling onto nodes in a compute cluster and actively manages
  workloads to ensure that their state matches the users declared intentions. Using
  the concepts of labels and pods, it groups the containers which make up an application
  into logical units for easy management and discovery.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
x-kinRank: "8"
x-alexaRank: "0"
tags: Nodes
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apis.md
specificationVersion: "0.14"
apis:
- name: Kubernetes - Get Nodes
  x-api-slug: apiv1beta3nodes-get
  description: List objects of kind node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3nodes-get-openapi.md
- name: Kubernetes - Post Nodes
  x-api-slug: apiv1beta3nodes-post
  description: Create a node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3nodes-post-openapi.md
- name: Kubernetes - Delete Nodes Name
  x-api-slug: apiv1beta3nodesname-delete
  description: Delete a node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3nodesname-delete-openapi.md
- name: Kubernetes - Get Nodes Name
  x-api-slug: apiv1beta3nodesname-get
  description: Read the specified node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3nodesname-get-openapi.md
- name: Kubernetes - Put Nodes Name
  x-api-slug: apiv1beta3nodesname-put
  description: Update the specified node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3nodesname-put-openapi.md
- name: Kubernetes - Delete Proxy Nodes Name
  x-api-slug: apiv1beta3proxynodesname-delete
  description: Proxy delete requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3proxynodesname-delete-openapi.md
- name: Kubernetes - Get Proxy Nodes Name
  x-api-slug: apiv1beta3proxynodesname-get
  description: Proxy get requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3proxynodesname-get-openapi.md
- name: Kubernetes - Post Proxy Nodes Name
  x-api-slug: apiv1beta3proxynodesname-post
  description: Proxy post requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3proxynodesname-post-openapi.md
- name: Kubernetes - Put Proxy Nodes Name
  x-api-slug: apiv1beta3proxynodesname-put
  description: Proxy put requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3proxynodesname-put-openapi.md
- name: Kubernetes - Delete Proxy Nodes Name Path *
  x-api-slug: apiv1beta3proxynodesnamepath-delete
  description: Proxy delete requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3proxynodesnamepath-delete-openapi.md
- name: Kubernetes - Get Proxy Nodes Name Path *
  x-api-slug: apiv1beta3proxynodesnamepath-get
  description: Proxy get requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3proxynodesnamepath-get-openapi.md
- name: Kubernetes - Post Proxy Nodes Name Path *
  x-api-slug: apiv1beta3proxynodesnamepath-post
  description: Proxy post requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3proxynodesnamepath-post-openapi.md
- name: Kubernetes - Put Proxy Nodes Name Path *
  x-api-slug: apiv1beta3proxynodesnamepath-put
  description: Proxy put requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3proxynodesnamepath-put-openapi.md
- name: Kubernetes - Get Redirect Nodes Name
  x-api-slug: apiv1beta3redirectnodesname-get
  description: Redirect get request to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3redirectnodesname-get-openapi.md
- name: Kubernetes - Get Watch Nodes
  x-api-slug: apiv1beta3watchnodes-get
  description: Watch a list of node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3watchnodes-get-openapi.md
- name: Kubernetes - Get Watch Nodes Name
  x-api-slug: apiv1beta3watchnodesname-get
  description: Watch a particular node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3watchnodesname-get-openapi.md
- name: Kubernetes - Get Nodes
  x-api-slug: apiv1beta3nodes-get
  description: List objects of kind node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3nodes-get-openapi.md
- name: Kubernetes - Post Nodes
  x-api-slug: apiv1beta3nodes-post
  description: Create a node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3nodes-post-openapi.md
- name: Kubernetes - Delete Nodes Name
  x-api-slug: apiv1beta3nodesname-delete
  description: Delete a node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3nodesname-delete-openapi.md
- name: Kubernetes - Get Nodes Name
  x-api-slug: apiv1beta3nodesname-get
  description: Read the specified node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3nodesname-get-openapi.md
- name: Kubernetes - Put Nodes Name
  x-api-slug: apiv1beta3nodesname-put
  description: Update the specified node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3nodesname-put-openapi.md
- name: Kubernetes - Delete Proxy Nodes Name
  x-api-slug: apiv1beta3proxynodesname-delete
  description: Proxy delete requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3proxynodesname-delete-openapi.md
- name: Kubernetes - Get Proxy Nodes Name
  x-api-slug: apiv1beta3proxynodesname-get
  description: Proxy get requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3proxynodesname-get-openapi.md
- name: Kubernetes - Post Proxy Nodes Name
  x-api-slug: apiv1beta3proxynodesname-post
  description: Proxy post requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3proxynodesname-post-openapi.md
- name: Kubernetes - Put Proxy Nodes Name
  x-api-slug: apiv1beta3proxynodesname-put
  description: Proxy put requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3proxynodesname-put-openapi.md
- name: Kubernetes - Delete Proxy Nodes Name Path *
  x-api-slug: apiv1beta3proxynodesnamepath-delete
  description: Proxy delete requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3proxynodesnamepath-delete-openapi.md
- name: Kubernetes - Get Proxy Nodes Name Path *
  x-api-slug: apiv1beta3proxynodesnamepath-get
  description: Proxy get requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3proxynodesnamepath-get-openapi.md
- name: Kubernetes - Post Proxy Nodes Name Path *
  x-api-slug: apiv1beta3proxynodesnamepath-post
  description: Proxy post requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3proxynodesnamepath-post-openapi.md
- name: Kubernetes - Put Proxy Nodes Name Path *
  x-api-slug: apiv1beta3proxynodesnamepath-put
  description: Proxy put requests to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3proxynodesnamepath-put-openapi.md
- name: Kubernetes - Get Redirect Nodes Name
  x-api-slug: apiv1beta3redirectnodesname-get
  description: Redirect get request to node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3redirectnodesname-get-openapi.md
- name: Kubernetes - Get Watch Nodes
  x-api-slug: apiv1beta3watchnodes-get
  description: Watch a list of node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3watchnodes-get-openapi.md
- name: Kubernetes - Get Watch Nodes Name
  x-api-slug: apiv1beta3watchnodesname-get
  description: Watch a particular node.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/kubernetes-logo.png
  humanURL: http://kubernetes.io/
  baseURL: :///api/v1beta3/127.0.0.1:6443
  tags: Containers, Google, Stack Network, API Service Provider, Containers, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/nodes/master/_listings/kubernetes/apiv1beta3watchnodesname-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://knoema.api.gallery.streamdata.io
- type: x-api-stack
  url: http://kubernetes.stack.network
- type: x-blog
  url: http://blog.kubernetes.io/
- type: x-blog-rss
  url: http://blog.kubernetes.io/feeds/posts/default
- type: x-github
  url: https://github.com/kubernetes
- type: x-twitter
  url: https://twitter.com/kubernetesio
- type: x-website
  url: http://kubernetes.io/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---