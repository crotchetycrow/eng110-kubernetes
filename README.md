# Kubernetes

- [Creating a K8 cluster for nginx](https://github.com/crotchetycrow/eng110-kubernetes/blob/main/documentation/k8_cluster_nginx.md)
- [Creating a K8 cluster for nodeapp](https://github.com/crotchetycrow/eng110-kubernetes/blob/main/documentation/k8_nodeapp.md)
- [Creating a K8 cluster for mongodb](https://github.com/crotchetycrow/eng110-kubernetes/blob/main/documentation/k8_mongodb.md)
- [Creating a K8 cluster on an EC2](https://github.com/crotchetycrow/eng110-kubernetes/blob/main/documentation/k8_ec2_cluster.md)
- [K8 Commands](https://github.com/crotchetycrow/eng110-kubernetes/blob/main/documentation/k8_cmd.md)

## What is microservice architecture?

Large application divided into separate parts

- SRP

### Benefits?

- Relatively small scale
- Independently managed
- Self-contained and independently deployed
- Supports horizontal scaling
- Can use different technology

### Disadvantages?

- Less secure
- Debugging is difficult (control flow)
- More complex than monolithic applications
- High network usage cost

## What is monolithic architecture?

Application built in one unified model

### Benefits?

- Simple to develop relative to microservice
- Easier to deploy (single)
- Relatively easier and simpler to develop
- Less network and latency problems

### Disadvantages?

- Too large
- Redeploy whole
- The bigger it is, slower it is
- Difficult to understand for new joiners

![](/img/k8_orchestration.png)

## What is Kubernetes?

Open source container orchestration platform that automates many of the manual processes involved in deploying, managing, and scaling containerized applications.

## Why is Kubernetes used?

- Self healing

- Load balancing

- Automated rollout and rollback

- Auto scaling

- Automatic bin packing

- Storage orchestration

## When is Kubernetes used and when shouldn't it be used?

### When?

- If your application uses a microservice architecture
- Slow development and deployment
- To lower infrastructure costs

### When not?

- Simple, lightweight applications
- Short time frame for delivery

## Types of Kubernetes services

![](/img/k8_services.png)

## What is Kubernetes cluster?

K8 cluster is a dynamic system that places and manages containers, grouped together in pods which run on nodes

## What are Kubernetes replica sets?

A process that runs multiple instances of a Pod and keeps the specified number of Pods constant

## LoadBalancer vs NodePort

https://platform9.com/blog/understanding-kubernetes-loadbalancer-vs-nodeport-vs-ingress/

## Why adopt Kubernetes

- 30.8% commercial growth to business - 3-5 years to get ROI
- Faster time to market
- IT cost optimization
- Improved scalability and availability
- Multi-cloud (and hybrid cloud) flexibility
- Effective migration to the cloud
