# Choix relié au fichier de Kubernetes

Ce document explique les différents choix reliés à l'implémentation et la création des fichiers de Kubernetes.

## CronJob
Pour le déploiement des CronJob, nous avons créé un fichier. Le fichier "cronjob-deployment.yaml" permet de 
créer et déployer automatiquement l'image avec le tag "latest" se trouvant sur Docker Hub.
