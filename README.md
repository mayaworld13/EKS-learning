# EKS-learning

# Deploying Applications on EKS using eksctl and kubectl

This guide provides step-by-step instructions to create an Amazon EKS cluster and deploy applications using `eksctl` and `kubectl`.

## Prerequisites

1. **AWS CLI** installed and configured with appropriate permissions.
2. **eksctl** installed.
3. **kubectl** installed.

## Steps

### 1. Create an EKS Cluster

To create an EKS cluster named `mymaya`:

```sh
eksctl create cluster --name=mymaya --region=us-east-1 --version=1.29
```

### 2. Verify Cluster Nodes

After the cluster is created, verify the nodes:
```sh
kubectl get nodes
```

### 3. Deploy Your Application

Deploy your Django application using the following command:
```sh
kubectl create deployment myweb --image=mayaworld13/django-todo-app --port=8000
```

4. Expose the Deployment
Expose the deployment to create a LoadBalancer service with same port in which your pod is running:

```sh
kubectl expose deployment myweb --type=LoadBalancer --port=8000
```

5. Get Service Details
Retrieve the external IP address of the LoadBalancer:
```sh
kubectl get svc
```
