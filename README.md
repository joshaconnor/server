# server

```bash
kustomize build --enable-helm | kubectl apply -f - --prune -l prune=true
```

```bash
kubectl get pods --all-namespaces
```
