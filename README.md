# Solution for Anastrat Assignment

1. A Dockerfile to build docker image and container for main.go application with mentioned requirements. 
minimal base image requirement to run the go application, 
multi-stage build and built from scratch i.e FROM scratch,
an executable to run by default when starting the container,
SENDER_EMAIL, PASSWORD & RECEIVER_EMAIL passed environment variable)

2. A README.md file with instructions on how to build and run the image.
 
3. A Kubernetes object file (deployment.yaml) having two replicas (pods) of the above application, 
Load balance the pods using a service. 
Expose service at port 31000.
 
4. Complete helm chart with instructions to run on kubernetes cluster.

5. A README.md file with instructions to run application on kubernetes and helm chart.
