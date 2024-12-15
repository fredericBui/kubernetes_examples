## Déployer des applications avec des fichiers YAML

Exemple : https://github.com/fredericBui/kubernetes_examples/blob/main/echo-server-deployment.yaml
Template vierge : https://github.com/fredericBui/kubernetes_examples/blob/main/template-deployment.yaml

```bash
# Pour éxécuté un fichier
kubectl apply -f <mon_fichier>
# Pour accéder au service via Minikube
minikube service <mon_service>
# Pour supprimer les objets créés
kubectl delete -f <mon_fichier>
```

### Exercices

Déployer et exposer les services suivants via des fichiers YAML

1. Image : kicbase/echo-server:1.0 → port 8080
2. Image : nginx → port 80
3. Image : cmintey/wishlist → port 3280    

**Notions**
- Qu'est-ce que YAML ?
- Quel avantage ?