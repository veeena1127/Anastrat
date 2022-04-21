Using deployment.yaml containing Kubernetes object-

Create the deployment using below-
sudo kubectl apply -f deployment.yaml

Check if the Deployment was created-
kubectl get deployments

Check if the Service was created-
kubectl get services

To see the Deployment rollout status-
kubectl rollout status deployment/docker-main-go
