# Kubernetes

## Why?

- manage hundreds or thousands containers

- HA with no down time

- scalability or high performance

- disaster recovery

## Components

### Node

A simple server

### Pod

- smallest unit of k8s

- abstraction over container

- usually 1 application per pod

- Each pod gets its own IP address

- New IP address on re-creation

### service and ingress

- service functionality
  
  - permanent ip address
  
  - load balancer

- lifecycle of pod and service not connected

- Externel servcie vs Internel service

- Ingress is before the service node to forward the traffice

### ConfigMap and Secrets

- enviroment variables or config maps

- configmap used to store properties

- secrets used to store credentials

### Volumes

- storage on local machine

- or storage on remote, outside of the k8s cluster

- external drive plugged into the k8s cluster

- k8s doesn't manage data persistence

### Deployment

- blueprint fo my-app pods

- you create Deployments

- abstractions of pods

- only for apps with no state

### StatefulSet

- for stateful apps



### Nodes

- each node has multiple pods on it

- 3 processes must be installed on every node
  
  - container runtime
  
  - kubelet
  
  - kubeproxy -> forward request from service to pod

- worker node do the actual work

### Master node

#### Api Server

- cluster gateway

#### Scheduler

- Where to put the pod

#### controller manager

- detect cluster state changes

#### etcd

- cluster brain

- key value store

## Kubelet

- get nodes

- status

- get status
  
  - get nodes
  
  - get pod
  
  - get services
  
  - get replicaset
  
  - get deployement
  
  - get pod --watch

- create deployment
  
  - kubectl create deployment [dname] --image=imagename

- debug
  
  - logs
  
  - describe
  
  - exec

- apply -f file

- delete -f file

## Configuration File

### 3 parts

- metadata

- specification

- status



## Namespaces

- organize

- cluster in cluter

- everything in a namespace

-  conflicate in application names

- resource sharing

- Access limits

- resource quota

- each namespace should create its own configmap and secrets

- you can access service in another namespace

- volumes and nodes can't bind to namespace



## Ingress


