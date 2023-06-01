Create files and add data in both files .
{sudo vim wordpress.yaml & sudo vim mysql.yaml}

````
kubectl apply -f <mysql-file-name>
kubectl apply -f <wordpress-file-name>
kubectl expose pod mysql --port=3306 --name=mysql 
kubectl expose pod wordpress --port=80 --target-port=80 --name=wordpress --type=NodePort
minikube service wordpress --url
kubectl describe po mysql
`````


``````````
kubectl delete svc wordpress
kubectl delete svc mysql
kubectl delete po wordpress
kubectl delete po mysql
```````````````
