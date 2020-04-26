Instructions:
For Running pods having nginx container:
   1. Run the minikube
   2. Run this command - kubectl create -f pod_configuration.yml
   3. New pod will be created, run - kubectl get pods

For running replication controller:
   1. run a minikube.
   2. Run this command - kubectl create -f rc-defination
   3. New controller has been created, run following commands to see them
	a. kubectl get replicationcontroller
  	b. kubectl get pods
