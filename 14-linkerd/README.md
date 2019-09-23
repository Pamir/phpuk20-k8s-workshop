# 15. LinkerD Service Mesh

## Presenter only

* Download linkerd CLI: https://linkerd.io/2/getting-started/#step-1-install-the-cli
* Check if everything is correct for LinkerD
```
linkerd check --pre
```
* Install LinkerD
```
linkerd install | kubectl apply -f -
```
* Add Ingress for LinkerD dashboard
```
kubectl apply -f basic-auth.yaml
kubectl apply -f linkerd-ingress.yaml
```

## Everyone

* Inject LinkerD proxy into existing deployments
```
kubectl get deployments -o yaml | linkerd inject - | kubectl apply -f -
```
* Check LinkerD dashboard
