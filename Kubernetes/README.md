Using deployment.yaml containing Kubernetes object-

1. Create the deployment using below-
sudo kubectl apply -f deployment.yaml

2. Check if the Deployment was created-
kubectl get deployments

3. Check if the Service was created-
kubectl get services

4. To see the Deployment rollout status-
kubectl rollout status deployment/docker-main-go


To run helm chart-

1. helm lint maingo (to check syntax errors)

2. helm install maingohelm maingo

after executing helm install, follow the instruction given in notes to run on a Kubernetes cluster.
