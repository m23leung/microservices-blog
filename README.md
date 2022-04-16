# microservices-blog

# Modules

|  Module    | Port
---------------------
  comments   | 4001
  event-bus  | 4005
  posts      | 4000
  moderation | 4003
  query      | 4002
  client     | --

services
------------
query  - called by front-end to retrieve the required back-end data
event bus - receives events and forwards them to the subscribers (including the one who sent it - stateless )
moderation - determines whether comment has been approved/rejected, which will push a status update


# infra/k8s

Ingress is used to...

Skaffold is utilized in order to:
 - Automate many tasks in a Kubernetes dev environment
 - Make it really easy to update code in a running pod
 - Make it really easy to create/delete all objects tied to a project at once
 Site: skaffold.dev
