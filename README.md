==== Pre-requisite:

1. minikube must be installed  [ code is tested on Minikube v1.23.2 running ubuntu(20.04.3) ]
   command to verify the version: minikube version
   command to start/status minikube: minikube start | minikube status
   
2. Ingress addon must be enabled.
   command to enable ingress : minikube addons enable ingress
   
3. check the status of ingress controller.
   command: kubectl get pods -n ingress-nginx

==== Deployment steps:

1. git clone git@github.com:thiru1102/devops-task1.git 

2. files as part of repo[2 files]

devops-task1
├── manifest.yml
├── README.md


3. Execute the below commands.
Command to deploy app : kubectl apply -f manifest.yml
** manifest file creates the following resources svc account, pdb, deployment, svc , ingress, hba.

4. Reqd - minkube ip
command : minikube ip

5. open the browser and hit http://<ip> [ Refresh will reflect the change in pod hostname,as LB is performed ]
