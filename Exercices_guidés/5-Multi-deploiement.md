## Déployer des applications qui doivent fonctionner ensemble

Exemple : https://github.com/fredericBui/kubernetes_examples/tree/main/multi-deployment
Templates vierge : https://github.com/fredericBui/kubernetes_examples/tree/main/multi-deployment/templates

```bash
kubectl apply -f mysql-deployment.yaml
kubectl apply -f wordpress-deployment.yaml
minikube service wordpress
```

### Exercices

Déployer les applications suivantes

1. MySQL & Wordpress

MySQL :
- image : mysql
- port: 3306
- env :
    - MYSQL_ROOT_PASSWORD
    - MYSQL_DATABASE
    - MYSQL_USER
    - MYSQL_PASSWORD

Wordpress :
- image: wordpress
- port: 80
- env :
    - WORDPRESS_DB_HOST (nom du service)
    - WORDPRESS_DB_PASSWORD
    - WORDPRESS_DB_USER 

2. Postgress & Metadatabase

Postgress :
- image: postgres
- port: 5432
- env:
    - POSTGRES_USER
    - POSTGRES_DB
    - POSTGRES_PASSWORD

Metadabase :
- image: metabase/metabase
- port: 3000
- env:
    - MB_DB_TYPE (postgres)
    - MB_DB_DBNAME
    - MB_DB_PORT
    - MB_DB_USER
    - MB_DB_PASS
    - MB_DB_HOST

3. Odoo & postgres

Postgress :
- image: postgres:15
- port: 5432
- env:
    - POSTGRES_USER
    - POSTGRES_DB
    - POSTGRES_PASSWORD

Odoo :
- image: odoo:17.0
- port: 8069
- env:
    - HOST
    - USER
    - PASSWORD

**Notion**
- tiers ?