# Deploying-MongoDB-and-Mongo-Express
  
## Installation

### Platform & tools

You need to install minikube, kubectl and docker as a driver for minikube .
* [Install minikube](https://minikube.sigs.k8s.io/docs/start/)
* [Install docker engine](https://docs.docker.com/engine/install/)
* [Install kubectl](https://kubernetes.io/docs/tasks/tools/)


## Running
### Start the minikube

```
minikube start
```
    
### Create Config and Secret for MongoDB Credentials
 ```
    kubectl apply -f configMap.yaml
    kubectl apply -f secret.yml
 ```
 ### Create MongoDB Deployment
  ```
    kubectl apply -f mongoDB.yml
  ```
    
 ### Create mongo-express Deployment 
  ```
    kubectl apply -f mongo-express.yml
  ```
  
  ### Get minikube node's ip address
```
minikube ip
```
### To directly access service
```
minikube service webapp-service
```

### To stop cluster 
```
minikue stop
```




