# Commands

`kubectl` - tests if Kubernetes is running

`kubectl cluster-info` - display addresses of the master and services

`kubectl get services` - lists all services in the namespace

`kubectl get namespace` - lists all namespaces available

`kubectl describe svc kubernetes` - More information on specific service

`kubectl taint nodes --all node-role.kubernetes.io/master-` - untaints nodes

`kubectl exec --stdin --tty 'pod-name -- /bin/bash` - ssh into pod
