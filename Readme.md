Running on minikube cluster

* 1- install minikube using docker driver on windows('https://minikube.sigs.k8s.io/docs/drivers/docker/')

minikube config set driver docker

minikube start

* 2- run minikube dashboard to enable dashboard

* 3- run minikube tunnel to activate tunnel for loadBalancing

* 4- create deployment 

* kubectl apply -f .\odoo-config.yaml -f .\odoo-deployment.yaml -f .\postgres-config.yaml -f .\postgres-deployment.yaml -f .\postgres-pv.yaml

* 5- delete deployment 

* kubectl apply -f .\odoo-config.yaml -f .\odoo-deployment.yaml -f .\postgres-config.yaml -f .\postgres-deployment.yaml -f .\postgres-pv.yaml