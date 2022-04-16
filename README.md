# microservices-blog

# Modules

| Module     | Port |
| ---      | ---       |
| comments  | 4001  |
| event-bus  | 4005  |
| posts  | 4000  |
| moderation  | 4003  |
| query  | 4002  |
| client  | ----  |

services
------------
client - react front end
query  - called by front-end to retrieve the required back-end data <br />
event bus - receives events and forwards them to the subscribers (including the one who sent it - stateless ) <br />
moderation - determines whether comment has been approved/rejected, which will push a status update <br />

# infra/k8s

1. Docker

2. Kubernetes

3. Ingress is used to...

4. Skaffold is utilized in order to:
 - Automate many tasks in a Kubernetes dev environment
 - Make it really easy to update code in a running pod
 - Make it really easy to create/delete all objects tied to a project at once
 Site: skaffold.dev
