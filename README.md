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

- Deny all ingress and egress per namespace
- Add fine granular ingress and egress access per Pod

## Kubernetes Policies

- OPA Gatekeeper
- Kyverno

## Google Kubernetes Engine (GKE)

- Private API server endpoint
- De-privilege default node service accounts
- Private nodes
- Shielded nodes
- Confidential nodes
- COS-containerd nodes image
- Nodes auto-update
- Workload Identity to bridge Kubernetes IAM with Google Cloud IAM
- [Encrypt etcd](https://cloud.google.com/kubernetes-engine/docs/how-to/encrypting-secrets)
- Dataplane V2 with NetworPolicies logging
- Protect public ingress with Cloud Armor (DDOS and WAF) and Managed Certificates
- Managed Controlplane and Dataplane for Anthos Service Mesh
- Security Posture dashboard (container configurations and images scanning)
- Anthos Security Insights dashboard

## Resources

- [Threat Matrix for Kubernetes](http://aka.ms/KubernetesThreatMatrix)
- [OWASP Kubernetes Top Ten](https://owasp.org/www-project-kubernetes-top-ten/)
- [CIS Benchmark for Kubernetes](https://www.cisecurity.org/benchmark/kubernetes)
