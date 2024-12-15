## Utiliser Kubectl pour interagir avec le cluster (1h)

Exemple : 

```bash
# Déployer une application
kubectl create deployment hello-minikube --image=kicbase/echo-server:1.0

# Voir les déploiements et pods
kubectl get deployment
kubectl get pods

# Exposer l'application
kubectl expose deployment hello-minikube --type=NodePort --port=8080

# Voir les services
kubectl get services

# Accéder au service via Minikube
minikube service hello-minikube

# Supprimer le service et le déploiement
kubectl delete service hello-minikube
kubectl delete deployment hello-minikube
```

### Exercices :

Déployer et exposer les images suivantes

1. Image : kicbase/echo-server:1.0 → port 8080
2. Image : nginx → port 80
3. Image : cmintey/wishlist → port 3280

Supprimer les déploiements et services.

**Notions**

- comment fonctionne deployment, pods et services ?