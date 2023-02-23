There is not that much security best practices in place by default with your Kubernetes clusters and your containers, let’s see what you need to do by yourself to mitigate this.

## Containers

- Multistage container build
- Minimal base image (alpine, distroless)
- Vulnerabilities scanning
- Non-root user

## Kubernetes

- PSA
- SecComp profile
- Restrict privilege Security Context
- Set Pod resources limits

## Istio

- Istio CNI
- Sidecar proxy image distroless
- mTLS STRICT
- AuthorizationPolicies
- Ingress Gateway

## Kubernetes NetworkPolicies

## Kubernetes Policies

## Google Kubernetes Engine (GKE)

- Private API server endpoint
- De-privilege default node service accounts
- Private nodes
- Shielded nodes
- Confidential nodes
- COS-containerd nodes image
- Nodes auto-update
- Workload Identity to bridge Kubernetes IAM with Google Cloud IAM

## Resources

- [Threat Matrix for Kubernetes](http://aka.ms/KubernetesThreatMatrix)
- [OWASP Kubernetes Top Ten](https://owasp.org/www-project-kubernetes-top-ten/)
