# Python HTTP Server on Kubernetes

## Initializing minikube
First, on Windows, you need to initalize the minikube like this:
```
$ minikube start --vm=true --driver=hyperv
```

## Enabling ingress
Then, you need to enable ingress with the command:
```
$ minikube addons enable ingress
```

## Deploying the app
Finally, you need to deploy the app:
```
$ kubectl apply -f app.yaml -n python-http-server
```

## Checking with ingress worked
You can use the port-forward to check with the deployment worked:
```
$ kubectl port-forward <pod-name> 8080:8000
```
Then, you check on localhost:8080 and see what happens!

You can see if the service is working, too:
```
$ kubectl port-forward service/<service-name> 8081:80
```
Then, check on localhost:8081