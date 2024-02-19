# argocd-test-repo


```shell
kind create cluster

kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/v2.10.1/manifests/install.yaml

argocd admin initial-password -n argocd
kubectl port-forward svc/argocd-server -n argocd 8080:443

# patch image tag
kubectl set image deployment/nginx-deployment nginx=nginx:1.25.4-alpine3.18
```