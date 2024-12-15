## Scalling & Auto-scalling

Exemple: 

```bash
kubectl create deployment nginx --image=nginx
kubectl expose deployment nginx --type=NodePort --port=80
kubectl get pods
## Scale manualy
kubectl scale deployments/nginx --replicas=2
kubectl get pods -o wide
## Unscale manualy
kubectl scale deployments/nginx --replicas=1
kubectl get pods -o wide
```

Lire la documentation jusqu'à "Autoscaling on multiple metrics and custom metrics" :
https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale-walkthrough/

Repartir d'une base simple avec un déploiement d'un server web sans base de donnée

### Exercices

Redéployer avec des fichiers YAML ces images et les autoscales

1. Image : kicbase/echo-server:1.0 → port 8080
2. Image : nginx → port 80
3. Image : cmintey/wishlist → port 3280

Supprimer les hpa, services et déploiements.

C'est possible que votre ordinateur soit paralysé par la boucle infini