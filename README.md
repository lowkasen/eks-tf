# eks-tf

To update kubeconfig, run:

```
aws eks update-kubeconfig --name test-cluster --profile eks1
```

To install AgroCD, run:

```
kubectl create namespace argocd
kubectl apply -n argocd -f agrocd_install.yaml
```
