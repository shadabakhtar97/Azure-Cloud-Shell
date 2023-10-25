# Azure-Cloud-Shell
Learn Azure Cloud Shell Deep Dive

Connect to your cluster using command line tooling to interact directly with cluster using kubectl, the command line tool for Kubernetes. Kubectl is available within the Azure Cloud Shell by default and can also be installed locally

### Set cluster context

1. Open Cloud Shell
   
2. Run the following commands

Set the cluster subscription
```
az account set --subscription xxxxx-xxxxx-xxxxx-xxxxx-xxxxx
```
Download cluster credentials
```
az aks get-credentials --resource-group shadab-RG --name shadab-k8s-cluster
```

### Sample commands
Once you have run the command above to connect to the cluster, you can run any kubectl commands. Here are a few examples of useful commands you can try.
List all deployments in all namespaces
```
kubectl get deployments --all-namespaces=true
```
List all deployments in a specific namespace
```
kubectl get deployments --namespace <namespace-name>
```
List details about a specific deployment
```
kubectl describe deployment <deployment-name> --namespace <namespace-name>
```
Get logs for all pods with a specific label
```
kubectl logs -l <label-key>=<label-value>
```

### Useful links
Overview of kubectl
Getting started with kubectl
Kubectl cheat sheet
Kubectl reference
