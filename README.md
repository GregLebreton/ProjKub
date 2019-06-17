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
## création du jar et dockerisation de l'application
```
cd ../spring-boot-couchbase-example-master
mvn package
docker build -t springcouchbase .
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

