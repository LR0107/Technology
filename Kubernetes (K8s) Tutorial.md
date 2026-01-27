# Kubernetes (K8s) Tutorial

## Install MicroK8s

### Install

`sudo snap install microk8s --classic`

### Check Cluster Status

`microk8s status --wait-ready`

If you see `microk8s is running`, the installation is successful.

---

## Pod

Pod is the smallest running unit in Kubernetes. Applications run inside Pods (not directly inside containers).

### Check Nodes (Cluster Machines & Health)

`kubectl get nodes`

### List Pods (All Namespaces)

`kubectl get pods -A`

### Describe a Pod (Details)

`kubectl describe pod podname`

### View Pod Logs

`kubectl logs podname`

### Enter Pod Container

`kubectl exec -it podname -- bash`

### Delete a Pod

`kubectl delete pod podname`

---

## Deployment

Deployments automatically manage Pods (scaling, upgrading, recovery, rollback).

### List Deployments

`kubectl get deployment`

### Describe a Deployment (Replicas / Update Status / Failures)

`kubectl describe deployment nginx`

### Scale Replicas (Scale Up/Down)

`kubectl scale deployment nginx --replicas=3`

### Update Image

`kubectl set image deployment/nginx nginx=nginx:1.25`

### Rollback

`kubectl rollout undo deployment nginx`

### View Rollout History

`kubectl rollout history deployment nginx`

### Delete a Deployment

`kubectl delete deployment nginx`

---

## YAML

### Create resources using YAML:

`kubectl apply -f app.yaml`

### Delete resources:

`kubectl delete -f app.yaml`

### View a resource YAML config:

`kubectl get pod nginx-xxx -o yaml`

---

## Service

### List Services

`kubectl get svc`

### Describe a Service

`kubectl describe svc nginx`

---

## Troubleshooting Workflow

### 1) Check Status

`kubectl get pods`

### 2) Check Details

`kubectl describe pod xxx`

### 3) Check Logs

`kubectl logs xxx`

### 4) Enter Container

`kubectl exec -it xxx -- sh`
