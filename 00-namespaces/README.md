# 0. Set up a namespace

## Everyone 

* Run `apply-your-name.sh` and provide unique string for placeholders
* Download kubeconfig
* Copy kubeconfig to `~/.kube/config`
* Install kubectl: https://kubernetes.io/docs/tasks/tools/install-kubectl/
* Try connection
```
kubectl version
```
* List Namespaces
```
kubectl get namespaces
```
* Create Namespace
```
kubectl create namespace <YOURNAME>
```
* Set default namespace to context
```
kubectl config set-context admin@k8s-workshop2/phpbenelux-workshop --namespace=<YOURNAME>
```
* See change in kubeconfig
```
cat ~/.kube/config
```
