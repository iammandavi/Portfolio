Each time your PC restarts or minikube stops:

make sure to run docker desktop in background

1. check minikube status 
    minikube status
if stoped then start minikube
    minikube start

2. Start docker driver
minikube start --driver=docker

3. Load Your Docker Image into Minikube
docker build -t portfolio:1.0 . 

OR

minikube image build -t portfolio:1.0 .

4. Apply ReplicaSet/pod any file if alreday then ignore

5. check pods - kubectl get pods -n kuma-system

6. port forwrd it
kubectl port-forward pod/<one-of-your-pods> -n kuma-system 8080:80

7. Then open: http://127.0.0.1:8080


If code changes

1. Rebuild image
minikube image build -t portfolio:1.0 .

2. delete old pods

3. check new pods

4. port forwad



