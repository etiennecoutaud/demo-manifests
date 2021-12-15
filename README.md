# Demo manifests

## Discover the kubernetes CLI
```
kubectl help
```

```
kubectl get -h
```

### Questions
- How many pods are running on the cluster ? (`wc` command can help)
- What is the `podIp` of the pod named `argocd-server-XXXX-XXXX`
- Can you find the cloud region where the cluster is running ? (`kubectl api-resources` can help

## Create a new namespace

```
kubectl create ns <MY SECRET CODE>
```
### Questions
- What are the default kubernetes namespaces ? Which usage ?
- How many namespaces are currently on the cluster ?
- Try to delete and recreate your namespace
- Add the following labels to your namespace `artifakt.io/owner=<lastname>.<name>`
- Try to identify namespace owner with labels


## TP 1 First resource

Create resource on the cluster
```
kubectl apply -f tp1 -n <MY PREVIOUS NS NAME>
```

### Questions
- What is your `podIP` ? Your container digest ?
- Time to scale, scale up your app with your manifest with 3 instances (Add more if you want ;)
- With the dockerhub, update your manifest to deploy another nginx version, during the update observe with `kubectl watch get pods -n <MY SECRET_CODE> -w` (-w for watch)
- What happened during update ?