This is a sample project which will deploy 2 springboot services in Kubernetes cluster irrespective of Cloud or In-house infrastructure.
It also deploys HPA and scales both services if CPU utilization goes above 70% for the pods

## Prerequisites:
* Kubernetes Cluster and kubectl client >= v1.22.2 pointing to cluster
* Metrics server deployed in cluster
* Helm3


## Steps to deploy:
* Clone this repository
* Navigate to exercise folder on terminal
* Default values are set in values.yaml
* run `helm install RELEASE-NAME .`
* run `kubectl get all -n staging` to see all deployed resources
* It deploys 2 services i.e. users service on node port 30165 and shifts service on node port 30166
* You should be able to access both services at http://NODE-IP:30165 and http://NODE-IP:30166 (30165 & 30166 should be open)
