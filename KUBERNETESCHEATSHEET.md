### MINIKUBE!!!!

```sh
minikube start

##Errors?
minikube delete
#https://github.com/kubernetes/minikube/issues/2765
rm -rf ~/.minikube
```

### KUBERNETES!!

```sh
kubectl get nodes

kubectl create -f node-client.yml

kubectl get pods
kubectl get pods --watch #Wait for the container to create

#Register changes
kubectl apply -f node-client.yaml


#Get pods with certain labels (How to check many?)
kubectl get pod -l app=sa-frontend

#Quick - hackish test
kubectl port-forward node-client 80:8080 #local computer:container

#ROLLBACK?!
kubectl rollout history deployment sa-frontend

kubectl rollout undo deployment $DEPLOYMENT_NAME --to-revision=$REVISION_NUM
```
