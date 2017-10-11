```
# Set sufficient resources for Cassandra
minikube config set memory 5120
minikube config set cpus 4

minikube start

minikube ssh
   sudo sed -i '/^ExecStart/s/$/ --insecure-registry registry.zing.zenoss.eng/' /lib/systemd/system/docker.service
   sudo systemctl daemon-reload
   sudo systemctl restart docker

source <(minikube docker-env)
kubectl config use-context minikube
minikube dashboard
kubectl apply -f .
minikube service frontend
```
