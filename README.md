# postgrest-cluster-k8s
Cluster K8S généré par chat gpt

# Chat GPT:

Ce cluster Kubernetes définit un namespace pour l'application et deux services, l'un pour le serveur PostgreSQL et l'autre pour PostgREST. Il définit également deux déploiements, l'un pour le serveur PostgreSQL et l'autre pour PostgREST.

Le serveur PostgreSQL utilise l'image Docker "postgres:latest" et définit les variables d'environnement POSTGRES_USER, POSTGRES_PASSWORD et POSTGRES_DB pour configurer le serveur.

PostgREST utilise l'image Docker "postgrest/postgrest:latest" et définit les variables d'environnement PGRST_DB_URI, PGRST_DB_SCHEMA, PGRST_SERVER_PROXY_URI, PGRST_SERVER_HOST et PGRST_SERVER_PORT pour se connecter au serveur PostgreSQL et configurer le serveur PostgREST.
