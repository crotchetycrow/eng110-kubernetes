`sudo apt-get install docker.io`

`docker --version`

https://phoenixnap.com/kb/install-kubernetes-on-ubuntu
https://phoenixnap.com/kb/install-minikube-on-ubuntu
https://www.techrepublic.com/article/how-to-quickly-install-kubernetes-on-ubuntu/

`sudo nano /run/flannel/subnet.env`

```
FLANNEL_NETWORK=10.244.0.0/16
FLANNEL_SUBNET=10.244.0.1/24
FLANNEL_MTU=1450
FLANNEL_IPMASQ=true
```

ec2 security group - allow custom tcp (whatever port used) any ipv4

```
      tolerations:
      - key: "node-role.kubernetes.io/control-plane"
        operator: "Exists"
        effect: "NoSchedule"
```
