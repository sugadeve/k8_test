install kubectl
===============
sudo apt-get update && sudo apt-get install -y apt-transport-https gnupg2
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee -a /etc/apt/sources.list.d/kubernetes.list
sudo apt-get update
sudo apt-get install -y kubectl




Install Minikube
=================
1. download the minikube binary

curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 \
  && chmod +x minikube
  
  
2. Install minikube

sudo mkdir -p /usr/local/bin/

sudo install minikube /usr/local/bin/

3. starti minikube using driver virtualbox

   minikube start --driver=<driver_name>
   
   driver_name=virtualbox
   
4. check the minikube status

   minikube status

apply the k8 configs
====================

1. kubectl create -f nginx-hello-world-deployment.yaml

2. kubectl create -f nginx-hello-world-service.yaml

