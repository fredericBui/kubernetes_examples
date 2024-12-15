## Attacher des volumes aux déploiements

Exemple : https://github.com/fredericBui/kubernetes_examples/tree/main/multi-deployment-volume
Templates : https://github.com/fredericBui/kubernetes_examples/tree/main/multi-deployment-volume/templates

```bash
# Pour éxécuté un fichier
kubectl apply -f <mon_fichier>
# Pour accéder au service via Minikube
minikube service <mon_service>
# Pour supprimer les objets créés
kubectl delete -f <mon_fichier>
```

### Exercices 

Ajouter des volumes aux fichiers de déploiements précédemment (wordpress+MySQL | odoo + PostGres | metabase + postgres) créés

MySQL :
- volume : /var/lib/mysql

Wordpress :
- volume : /var/www/html

Postgress :
- volume : /var/lib/postgresql/data

Supprimer les pvc, services et déploiements

**Notion**
PVC