---
doc_type: hypothesis-highlights
url: >-
  https://stackoverflow.com/questions/51762679/what-is-the-difference-between-google-kubernetes-engine-gke-and-google-compute
---
https://medium.com/@use.abhiram/gke-vs-compute-engine-a-detailed-showdown-in-the-cloud-coliseum-73a828ebb5a2


## Page Notes
## Highlights
- A big difference between the two is that a normal GCE VM instance is completely unmanaged. Once you've used the GCP-provided image, all updates are up to you. Whereas with GKE, the Master and node versions can be set to upgrade automatically and you only choose which OS you want, not the specific OS version. This means that if there are security patches or updates to a node OS, it will get pushed to your cluster. When there are improvements or patches to GKE (as long as you enable automatic upgrades) your nodes will receive the new versions. GKE may cost you a little more than a stand-alone GCE VM, but it comes with more automation and management baked in. — [Updated on 2025-01-19 15:34:09](https://hyp.is/uacD0tZMEe-muzMHgM8ZJg/stackoverflow.com/questions/51762679/what-is-the-difference-between-google-kubernetes-engine-gke-and-google-compute) — Group: #me-only

both of gce and gke are parts of gcp : services provided by it.
gke is more expensive but has features like autoscaling, auto-updates, all these are manually handled by gce components, however gke requires knowledge of containers, and generally microservices benefit more with gke , gce is good for legacy code bases which do not require frequent updates or if the code base has a constant traffic, 
if there is frequent up and down in traffic in that scenario then gke is better. in terms of cost optimization.



