# Helm Demo
This repository is about application deployment on Kubernetes using Helm. 

## Deployment Workflow

### Deploy MongoDB
```python
kubectl apply -f helm-mongodb.yaml
Verify deployment:
kubectl get pods
kubectl get svc
```

### Deploy Mongo Express
```python
kubectl apply -f helm-mongo-express.yaml
Verify:
kubectl get deployments
kubectl get services
kubectl get pod
kubectl logs <pod-name>
```

### Deploy Ingress
```python
kubectl apply -f helm-ingress.yaml
Verify:
kubectl get ingress
```

## Verification

### Check Pods
```python
kubectl get pods
```

### Check Services
```python
kubectl get svc
```

### Check Secrets
```python
kubectl get secrets
```

## Access Mongo Express

If Ingress is configured:
```python
http://<hostname>
```
Or via port-forwarding:
```python
kubectl port-forward service/mongo-express-service 8081:8081
Access:
http://localhost:8081
```
