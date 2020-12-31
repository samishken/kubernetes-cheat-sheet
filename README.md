# kubernetes-cheat-sheet

## The Kubernetes command-line tool, kubectl, allows you to run commands against Kubernetes clusters. You can use kubectl to deploy applications, inspect and manage cluster resources, and view logs. 

1) kubectl get pod
2) kubectl get services (at the beginning there will be one default service)
3) kubectl delete pod <pod>
4) kubectl delete services <service>
5) kubectl create deployment NAME --image=image [--dry-run][options]
    >>- kubectl create deployment nginx-depl --image=nginx
6) kubectl get deployment
7) kubectl get replicaset (Replicaset manages the replicas of a Pod)
8) kubectl edit deployment <deployment-name>
9) kubectl logs <pod name>
10) kubectl exec -it <pod name> -- bin/bash
11) kubectl apply -f <name of config file .yaml>
12) To get detail information about a Pods - ex. ip addr
     run "kubectl get pod -o wide"
13) 


## kubectl commands
kubectl get nodes
kubectl get pod
kubectl get services
kubectl create deployment nginx-depl --image=nginx
kubectl get deployment
kubectl get replicaset
kubectl edit deployment nginx-depl

## debugging
kubectl logs {pod-name}
kubectl exec -it {pod-name} -- bin/bash

## create mongo deployment
kubectl create deployment mongo-depl --image=mongo
kubectl logs mongo-depl-{pod-name}
kubectl describe pod mongo-depl-{pod-name}

## delete deplyoment
kubectl delete deployment mongo-depl
kubectl delete deployment nginx-depl

## create or edit config file
vim nginx-deployment.yaml
kubectl apply -f nginx-deployment.yaml
kubectl get pod
kubectl get deployment

## delete with config
kubectl delete -f nginx-deployment.yaml

## Metrics
kubectl top The kubectl top command returns current CPU and memory usage for a cluster’s pods or nodes, or for a particular pod or node if specified.
