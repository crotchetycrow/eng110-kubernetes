`nano nodeapp.yml`

```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nodeapp
spec:
  selector:
    matchLabels:
      app: nodeapp
  replicas: 3
  template:
    metadata:
      labels:
        app: nodeapp
    spec:
      containers:
        - name: nodeapp
          image: jackhooper/eng110-docker-test:eng110_node_prod
          ports:
            - containerPort: 3000
          imagePullPolicy: Always
```

`kubectl create -f nodeapp.yml`

`nano node_svc.yml`

```
apiVersion: v1
kind: Service
metadata:
  name: nodeapp-service
spec:
  selector:
    app: nodeapp
  type: LoadBalancer
  ports:
    - port: 3000
      protocol: TCP
      targetPort: 3000
```

`kubectl create -f node_svc.yml`

`kubectl edit deploy nodeapp` - edits the image's configuration

`kubectl delete deploy nodeapp` - deletes the deployed image named nodeapp

`kubectl delete svc nodeapp-service` - deletes the service named nodeapp-service
