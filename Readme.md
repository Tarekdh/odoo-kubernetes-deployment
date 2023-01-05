Running on minikube cluster

* 1- install minikube using docker driver on windows('https://minikube.sigs.k8s.io/docs/drivers/docker/')

set default driver for minikube

````minikube config set driver docker````

````minikube start````

or set options to avoid cluster out of memory errors

````minikube start --cpus=4 --wait=all --wait-timeout=60m0s --memory=max````

* 2- run ````minikube dashboard```` to enable dashboard

* 3- run ````minikube tunnel```` to activate tunnel for loadBalancing

* 4- create deployment 

* ````kubectl apply -f .\odoo-config.yaml -f .\odoo-deployment.yaml -f .\postgres-config.yaml -f .\postgres-deployment.yaml -f .\postgres-pv.yaml````

* 5- delete deployment 

* ````kubectl apply -f .\odoo-config.yaml -f .\odoo-deployment.yaml -f .\postgres-config.yaml -f .\postgres-deployment.yaml -f .\postgres-pv.yaml````

-----
* deploy with helm

* 1- add bitnami repo 

````helm repo add bitnami https://charts.bitnami.com/bitnami````

* 2- run ````helm install odoo-release bitnami-repo/odoo -f .\my-values.yaml````
