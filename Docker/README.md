Prerequisite:
Check if golang installed in your system and Copy go.mod and go.sum in directory.

Else,
Install golang in your system (ie. ubuntu) using below-
sudo apt install golang-go
go get github.com/sirupsen/logrus
Copy go.mod and go.sum in directory.

Build the application with DOckerfile using below command-
docker build -t docker-main-go:latest -f Dockerfile .

Run the application using below command-
docker run docker-main-go:latest
