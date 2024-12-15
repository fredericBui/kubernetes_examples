## Répartir les déploiements sur deux machines (nodes) (1h)

Avant de commencer :
- Supprimer le cluster
```bash
minikube delete
```
- Recréer le cluster avec 2 machines
```bash
minikube start --nodes 2
# Vérifier si minikube et les machines sont bien démarré
minikube status
kubectl get nodes
```

Exemple :

```bash
# Créer un déploiement avec 2 réplicas
kubectl create deployment myserver --replicas 2 --image=kicbase/echo-server:1.0
# Voir le déploiement des pods sur les machines
kubectl get pods -o wide
```
### Exercices : 
Déployer et exposer les applications suivantes avec 2 réplicas

1. Image : kicbase/echo-server:1.0 → port 8080
2. Image : httpd → port 80
3. Image : cmintey/wishlist → port 3280

Supprimer les déploiements et services

Note : Il est également possible d'ajouter des nodes à posteriori
```
minikube node add <nomDeMonNode> --worker=true
```

**Notions**
- Qu'est-ce qu'un node ?
- Qu'est-ce qu'un réplica ?
- Que se passe t il si un node tombe ?
- Où sont acheminé les requêtes ?
```
kubectl logs -f <nom_du_pods>
```
- Que se passe t il si un pods est supprimé ?