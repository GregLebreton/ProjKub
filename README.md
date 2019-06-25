# ProjKub

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
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```
## Exposition du service et afficher le résultat dans le navigateur par défault
```
// TODO
```
### Accés au service 
```
docker exec aspnetcore_sample ipconfig
Copy the container IP address and paste into your browser (for example, 172.29.245.43)
```
