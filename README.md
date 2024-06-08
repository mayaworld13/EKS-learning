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
