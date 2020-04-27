## Instructions
* For Running pods having nginx container:
   1. Run the minikube
   1. Run this command - ```kubectl create -f pod_configuration.yml```
   1. New pod will be created, run - ```kubectl get pods```

* For running replication controller:
   1. run a minikube.
   1. Run this command - ```kubectl create -f rc-defination.yml```
   1. New controller has been created, run following commands to see them
		* ```kubectl get replicationcontroller```
  		* ```kubectl get pods```

* For running replica set:
   1. run an minikube
   1. Run this command: kubeclt create -f replicaset-definition.yml
   1. New replicaset has been created. Some useful commands:
		* **Get**: 
			* ```kubeclt get replicaset```
			* ```kubeclt decribe replicaset <replicaset-name>```
		* **Delete**:
			* ```kubectl delete replicaset <replicaset-name>```

* For running deployemnt:
  1. run a minikube.
  2. Run this command: kubectl create -f deployemnt-definition.yml
  3. New deployment has been created. Some useful commands:
		* **Get**: 
			* ```kubeclt get deployment```
			* ```kubectl get all```
		* **Update**:
			* ```kubectl apply -f deployment-difinition.yml```
			* ```kubectl set image deployment/<deployment-name> nginx=nginx:1.9.1```
		* **Status**:
			* ```kubectl rollout status deployment/<deployment-name>```
			* ```kubectl rollout  history deployment/<deployment-name>```
 		* **Rollback**:
			* ```kubectl rollout undo deployment/<deployment-name>```

* For running service:
  1. run a minikibe.
  2. Run a deployment.
  3. Run a service: ```kubectl create -f service-configuration.yml```
  4. New Service will be created of type NodePort
  5. For accessing api endpoint through your broswer:
		* find out node ip address: ```kubectl describe node <node-name>``` {ex - minikube }
		* hit the - url:targetPort 
