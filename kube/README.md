# first-k8s-deployment

## Enabling ingress
1) First, you need to start minikube cluster as:
```
$ minikube start --vm=true --driver=hyperv
```

2) Then, you need to enable:
```
$ minikube addons enable ingress
```