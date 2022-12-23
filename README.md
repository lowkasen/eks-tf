# eks-tf

To update kubeconfig, run:

```
aws eks update-kubeconfig --name test-cluster --profile eks1
```

To install ArgoCD, run:

```
kubectl create namespace argocd
kubectl apply -n argocd -f agrocd_install.yaml
```

To connect to ArgoCD UI, run:

```
kubectl port-forward svc/argocd-server -n argocd 8080:443
```

Use the following credentials to login to UI:

```
Username: admin
Password: kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
```
