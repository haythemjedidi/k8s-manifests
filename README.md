# k8s-manifests

Reference Kubernetes manifests and a Docker Compose stack for a typical
microservice application - the same kind of resources I operate day to day
(Deployments, Services, and Ingress).

## Contents

- `docker-compose.yml` - a Spring Boot + PostgreSQL + Keycloak stack for
  local development.
- `deployment.yaml` - a Deployment with resource requests/limits and
  readiness/liveness probes.
- `service.yaml` - a ClusterIP Service in front of the pods.
- `ingress.yaml` - an Ingress exposing the Service externally.

## Usage

```bash
# local
docker compose up

# cluster
kubectl apply -f deployment.yaml -f service.yaml -f ingress.yaml
```
