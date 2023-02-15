# postgrest-cluster-k8s
Cluster K8S généré par chat gpt

# Chat GPT:

## V1:

Ce cluster Kubernetes définit un namespace pour l'application et deux services, l'un pour le serveur PostgreSQL et l'autre pour PostgREST. Il définit également deux déploiements, l'un pour le serveur PostgreSQL et l'autre pour PostgREST.

Le serveur PostgreSQL utilise l'image Docker "postgres:latest" et définit les variables d'environnement POSTGRES_USER, POSTGRES_PASSWORD et POSTGRES_DB pour configurer le serveur.

PostgREST utilise l'image Docker "postgrest/postgrest:latest" et définit les variables d'environnement PGRST_DB_URI, PGRST_DB_SCHEMA, PGRST_SERVER_PROXY_URI, PGRST_SERVER_HOST et PGRST_SERVER_PORT pour se connecter au serveur PostgreSQL et configurer le serveur PostgREST.

## V2:

Ce fichier YAML crée un déploiement (Deployment) pour l'application PostgREST, avec trois réplicas (replicas: 3). Il crée également un service (Service) pour exposer l'application à l'extérieur du cluster.

Dans le déploiement, le conteneur PostgREST utilise l'image postgrest/postgrest:latest. Les variables d'environnement PGRST_DB_URI et PGRST_DB_SCHEMA sont définies pour spécifier l'emplacement de la base de données PostgreSQL utilisée par l'application. Dans cet exemple, l'URL de la base de données est postgres://username:password@postgres-service:5432/postgres.

Le service redirige le trafic vers le port 3000 du conteneur PostgREST en interne, mais écoute sur le port 80 pour les requêtes HTTP externes.

Il est important de noter que ce fichier YAML ne configure pas la base de données PostgreSQL elle-même, qui doit être configurée séparément.
