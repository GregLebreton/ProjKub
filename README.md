# ProjKub
```
Dockeriser une application asp.net
```
## Dockerisation de l'application
```
cd ../aspnetapp
docker build -t aspnetapp .
docker run -d -p 8080:80 --name myapp aspnetapp
```
## Visualisation de l'application dans le container
```
http://localhost:8080
```
## Création des composants kubernetes(deployment et service)
```
cd ../manifestesKub
kubectl apply -f deployment.yaml --> deploy greglebreton/aspnetapp:1.0
```
## Exposition du service et afficher le résultat dans le navigateur par défault
```
kubectl expose deployment aspnetapp --type=NodePort --name=myappservice
minikube service myappservice
```
