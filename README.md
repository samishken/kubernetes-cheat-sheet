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
