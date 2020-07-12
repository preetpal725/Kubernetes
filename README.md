# Kubernetes
Python application on Kubernetes

This is a 'Hello World!' Python application running in a docker container on Kubernetes. I have used light weight python alpine image to run the application.

Attached below are the commands needed to run the whole application from start to end:
Install Docker first, go to your kubernetes(main) folder in terminal and run the below command:
$ docker

Once you build server.py, requirements.txt, dockerfile and docker-compose.yaml as shown in the repository, run these commands: 
$ docker-compose build python
$ docker-compose up python
Now, your application is hosted on localhost:5000. You can check it.

Stop the container using the stop button in Docker dashboard and initialte Kubernetes.
$ kubectl --help 
$ kubectl get nodes
$ docker-compose push python

After this, create deployment.yaml and service.yaml files as shown in the repository and run these commands:
$ kubectl apply -f ./kubernetes/deployments/deployment.yaml
$ kubectl apply -f ./kubernetes/services/service.yaml
$ kubectl get svc
Now, your application is hosted on localhost. You can check it.
