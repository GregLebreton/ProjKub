# ProjKub
```
dockeriser un site PHP et le deployer sur Kubernetes
```
## Dockerisation de l'application
```
docker build -t phpapp .
```
## Création des composants kubernetes(deployment et service)
```
cd ../manifestesKub
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```
## exposer le service et afficher le résultat dans le navigateur par défault
```
minikube service frontend
```
### Accés au service 
```

```
