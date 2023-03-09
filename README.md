You are asked to create or deploy the following services and tools:

* your own Helm chart for each microservice; charts must be reusable and customizable in case we need it in the future (different Docker images, environment variables...)
* an internal load balancer setup to be the single entrypoint of your infrastructure
* a monitoring stack based on Prometheus and Grafana
* a log aggregation
* databases, internal load balancer, log aggregation, monitoring must be deployed with Helm
public packages
* docker images, stored on a private Docker registry (such as Github).
High-quality and secured services are required:
* the resource consumption must be limited
* databases must be secured with password; some custom settings may be set, for better
performance
* passwords must be stored in Kubernetes secrets
* kubernetes resources must have coherent labels, in order to filter resources easily
* 2 roles (sysadmin and developer) must be configured with suitable permissions (at least
one user per role).

The infra must also respect a high-availability standard:
* your infrastructure must be resilient: services should be replicated when possible
* auto-scaling rules must allow your platform to accept a growing number of requests
* a node failure must not make any downtime; a delay in indexation is permitted
* propose a zero-downtime deployment strategy; a demonstration must be prepared.

Tout en HELM chart:
loadbalancer
monitoring: prometheus & grafana
log aggregation: ELK
docker images in private registry
une queue: RAbbitMQ