# Kubernetes

A scalable, stateless application

## Run on your computer

Start your minikube cluster

$ minikube start

First of all, deploy your application to your Minikube cluster and wait until all the Pods are ready:

`kubectl apply -f kube`

Kubernetes makes it very easy to increase the number of replicas to 2

`kubectl scale --replicas=2 deployment/knote`

You can watch how a new Pod is created with:

`kubectl get pods -l app=knote --watch`

The -l flag restricts the output to only those Pods with a app=knote label.

Access your app:

`minikube service knote --url`

Open the url given in the output