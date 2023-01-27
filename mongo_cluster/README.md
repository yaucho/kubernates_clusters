# Mongo cluster
Simple k8s cluster with mongo db and mongo express Depoyments, internal service for mongo db, external service for mongo express, secret and configMap entities.

## Setup
To create cluster:
1) Create secret which contains mongo db username and password
```kubectl apply -f mongo_db_secret.yaml```
2) Create configMap which contains mongo db URL
```kubectl apply -f config_map.yaml```
3) Create mongo db and mongo express Deployments. Files already contains Services for those Deployments
```
kubectl apply -f mongo_db_deployment.yaml
kubectl apply -f mongo_express_deployment.yaml
```
To enter to the mongo express from browser using minikube:
`minikube service mongo-express-service`

## Request path from browser to mongo db:
[[https://github.com/username/repository/mongo_cluster/doc/request_path.png|alt=octocat]]
