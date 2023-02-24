# k8s playground
This project aims to deploy a simple project (which is visitor counter) on kubernetes.

### Deploy steps
#### all one 

`cd deployment/k8s && kubectl apply -f .`

#### one by one

`kubectl apply -f secret.yaml`

`kubectl apply -f redis-deployment.yaml`

`kubectl apply -f redis-service.yaml`

`kubectl apply -f config-map.yaml`

`kubectl apply -f visitors-deployment.yaml`

`kubectl apply -f visitors-service.yaml`

### Test 
 
#### using port-forward
`kubectl port-forward service/visitors-service 8888:80`

`curl localhost:8888/api`
