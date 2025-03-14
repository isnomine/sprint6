minikube start --addons=metrics-server --vm-driver=docker
kubectl apply -f ./deployment.yaml
kubectl apply -f ./service.yaml
kubectl apply -f ./hpa.yaml

kubectl get services


kubectl expose deployment scaleapp-deployment --type=NodePort 

