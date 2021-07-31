# server

```bash
kustomize build --enable-helm | kubectl apply -f - --prune -l prune=true
```

```bash
kubectl get pods --all-namespaces
```

```bash
kubeseal <secret.yaml >sealed-secret.yaml -o yaml
```

```bash
git pull 
git add .
git commit
git push
```
