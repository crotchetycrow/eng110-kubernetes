`nano nginx.yml`

```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx
spec:
  selector:
    matchLabels:
      app: nginx
  replicas: 3
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
        - name: nginx
          image: ahskhan/sre_nginx_test
          ports:
            - containerPort: 80
          imagePullPolicy: Always
```

`kubectl create -f nginx.yml`

`nano nginx_service.yml`

```
apiVersion: v1
kind: Service
metadata:
  name: nginx-service
spec:
  selector:
    app: nginx
  type: NodePort
  ports:
    - nodePort: 30442
      port: 80
      protocol: TCP
      targetPort: 80
```

`kubectl create -f nginx_service.yml`

`kubectl edit deploy nginx` - edits the image's configuration

`kubectl delete deploy nginx` - deletes the deployed image named nginx

`kubectl delete svc nginx-service` - deletes the service named nginx-service
