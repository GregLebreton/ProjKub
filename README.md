# ProjKub
## Création du cluster couchbase
```
cd vagranteansible 
1- creation des machines vagrant (2 machines centos)
vagrant up
2- partage des clés ssh de l'utilisateur courant avec les 2 machines
./ssh.sh 
3- installation et configuration d'un cluster couchbase (master+noeud)
ansible-playbook -i inventory.env -u vagrant install.yml
ansible-playbook -i inventory.env -u vagrant config.yml 
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
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```
## Exposition du service et afficher le résultat dans le navigateur par défault
```
minikube service frontend
```
### Accés au service 
```
docker exec aspnetcore_sample ipconfig
Copy the container IP address and paste into your browser (for example, 172.29.245.43)
```
