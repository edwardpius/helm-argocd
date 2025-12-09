# helm-argocd

## Creating the ArgoCD Helm Chart App
```bash
argocd app create helm-argo-app \
    --repo git@github.com:edwardpius/helm-argocd.git \
    --path helm-argo-app \
    --dest-server https://kubernetes.default.svc \
    --dest-namespace helm-argo-app \
    --sync-option CreateNamespace=true \
    --parameter namespace=helm-argo-app
```
