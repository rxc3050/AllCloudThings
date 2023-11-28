# K8s-App-Manifest-Code

- Sample code for frontend app manifest file 

```YAML

apiVersion: apps/v1
kind: Deployment
metadata:
  name: frontend-app
spec:
  replicas: 3
  selector:
    matchLabels:
      app: frontend-app
  template:
    metadata:
      labels:
        app: frontend-app
    spec:
      containers:
        - name: nodejs-app
          image: your-frontend-app-image:tag
          ports:
            - containerPort: 3000  # Replace with the port your Node.js app listens on

---
apiVersion: v1
kind: Service
metadata:
  name: frontend-service
spec:
  selector:
    app: frontend-app
  ports:
    - protocol: TCP
      port: 80  # The port your service listens on
      targetPort: 3000  # The port your Node.js app container exposes
  type: ClusterIP  # Use 'ClusterIP' for internal access within the cluster

```

- Deploy Command 
    - ```yaml 
        kubectl apply -f frontend-app.yaml

- Steps to consider before deploy:
  -  Make sure to have your Node.js application Docker image pushed to a container registry and specify the correct image name and tag in the manifest.   
  
        