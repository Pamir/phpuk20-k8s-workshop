# 15. LinkerD Service Mesh

## Presenter only

* Download linkerd CLI: https://linkerd.io/2/getting-started/#step-1-install-the-cli
* Check if everything is correct for LinkerD
```
linkerd check --pre
```
* Install LinkerD
```
linkerd install --ha | kubectl apply -f -
```

## Everyone

* Start LinkerD dashboard
```
linkerd dashboard
```

* Inject LinkerD proxy into existing deployments

Add this anntation to pods
```
linkerd.io/inject: enabled
```

Or run

```
kubectl get deployments -o yaml | linkerd inject - | kubectl apply -f -
```
* Check LinkerD dashboard
