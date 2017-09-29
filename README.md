```
minikube start
source <(minikube docker-env)
kubectl config use-context minikube
minikube dashboard
kubectl apply -f .
minikube service frontend
```
