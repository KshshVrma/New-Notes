---
doc_type: hypothesis-highlights
url: 'https://devopedia.org/google-kubernetes-engine'
---

# Google Kubernetes Engine

## Metadata
- Author: [devopedia.org]()
- Title: Google Kubernetes Engine
- Reference: https://devopedia.org/google-kubernetes-engine
- Category: #article

## Page Notes
## Highlights




- if you were to build an online retail application with user sign-in, inventory management, billing and shipping, you could break up your application into smaller modules called microservices. — [Updated on 2025-01-19 15:19:49](https://hyp.is/uTuw3tZKEe-oSTuAlhCRBw/devopedia.org/google-kubernetes-engine) — Group: #me-only

- Containers provided the environment to deploy microservices. You can run them on the same or even different machines, start and stop them quickly, but you can't specify how many machines or containers to keep running. What to do if containers fail? How to connect a container to other containers and enable persistent storage? — [Updated on 2025-01-19 15:20:17](https://hyp.is/yh29ytZKEe-Fdfc5Yt7e_w/devopedia.org/google-kubernetes-engine) — Group: #me-only

- For these aspects, you need a container orchestration system like Kubernetes. — [Updated on 2025-01-19 15:20:25](https://hyp.is/zsXohNZKEe-vE-_bmqMMyQ/devopedia.org/google-kubernetes-engine) — Group: #me-only

- Kubernetes is an open source orchestrator for a container environment. It provides the ability to define how many machines to use, how many containers to deploy, how to scale them, where the persistent disks reside, and how to deploy a group of containers as a single unit. — [Updated on 2025-01-19 15:20:39](https://hyp.is/1yQ90tZKEe-V4MfuHys7fA/devopedia.org/google-kubernetes-engine) — Group: #me-only

- features that Google Cloud Platform provides. These include: Leverage CI/CD tools in GCP to help you build and serve application containers Use Google Cloud Build to build container images from various source code repositories Use Google Container Registry to store and serve your container images Load balancing for Google Compute Engine instances Node pools to designate subsets of nodes within a cluster for additional flexibility Automatic scaling of your cluster's node instance count Automatic upgrades for your cluster's node software Node auto-repair to maintain node health and availability — [Updated on 2025-01-19 15:21:16](https://hyp.is/7VPLuNZKEe-an38XNTP6zg/devopedia.org/google-kubernetes-engine) — Group: #me-only

- Logging and monitoring with Operations (formerly Stackdriver) for visibility into your cluster — [Updated on 2025-01-19 15:21:32](https://hyp.is/9uQY4NZKEe-2t6ubXP-92g/devopedia.org/google-kubernetes-engine) — Group: #me-only

- A cluster is the foundation of GKE. The Kubernetes objects that represent containerized applications all run within the cluster. A cluster consists of at least one cluster master and multiple worker machines called nodes, which are the worker machines that run containerized applications and other workloads. The worker machines are Google Compute Engine (GCE) instances that GKE creates on your behalf when you create a cluster. — [Updated on 2025-01-19 15:22:36](https://hyp.is/HNiypNZLEe-_6Deb5EhrsQ/devopedia.org/google-kubernetes-engine) — Group: #me-only

- It's now possible to do container-native load balancing for GKE-based applications. Previously, load balancers worked at the granularity of VMs. These VMs then used IPTable rules to route workloads to the right pods. This was suboptimal and resulted in traffic hops between nodes. With Network Endpoint Groups (NEGs), load balancing can now be done based on the availability and health of pods rather than nodes. — [Updated on 2025-01-19 15:25:11](https://hyp.is/eTZLLtZLEe-c4V9R7DTgZA/devopedia.org/google-kubernetes-engine) — Group: #me-only



[[What is the difference between Google Kubernetes Engine (GKE) and Google Compute Engine (GCE)]]