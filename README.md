# server

[To Do List](/todo.md)

## Creating containers

For building any individual deployment, or a large number of deployments. Enter directory with kustomization.yaml file and run the following command:

```bash
kustomize build --enable-helm | kubectl apply -f
```

To build deployments and remove any unnecesssary previous deployment files, use the following command:

```bash
kustomize build --enable-helm | kubectl apply -f - --prune -l prune=true
```

Creating sealed secrets for safe upload to the cloud can be done with the following:

```bash
kubeseal <secret.yaml >sealed-secret.yaml -o yaml
```

## Status checks

Getting a list of all pods on system can be done with either of the following: 

```bash
kubectl get pods --all-namespaces
kubectl get pods -A
```

Getting specific details about a pod can be done with the following:

```bash
kubectl describe pods <name> -n <namespace>
```

## Maintancence

Restarting a deployment for any reason can be done with the following:

```bash
kubectl -n service rollout restart deployment <name> -n server
```

## Record keeping

Uploading configuration files to a git repository require the following:

```bash
git pull 
git add .
git commit
git push
```
