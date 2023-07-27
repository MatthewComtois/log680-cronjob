# Création de l’application

Ce document explique les différents choix technologiques faits lors de ce projet

## Choix technologiques pour la conteneurisation de l'application

### Docker
Docker est le standard dans l'industrie pour ce qui est de la conteneurisation 
d'application. C'était donc un choix assez facile à faire. De plus, il est indiqué
dans le laboratoire d'utiliser Docker. En utilisant Docker, nous pouvons aussi
déployé nos images sur Docker hub, ce qui est nécessaire pour la partie d'intégration
continue. 

## Choix technologiques pour le déploiement des container de l'application

### Kubernetes
Kubernetes permet de facilement déployer des conteneurs Docker. Il permet aussi de 
facilement faire la gestion et de gérer la gestion de mise en échelle de ces conteneurs.
Nous l'avons choisi primordialement, car c'est la technologie qui est demandée lors du 
laboratoire. Cependant, même si ce choix ne nous était pas imposé, nous aurions quand
même choisi d'utiliser Kubernetes. Nous utilisons un fichier de type "yaml" pour faire
le déploiement automatique de l'application. L'avantage de cela est que nous pouvons 
réutiliser ce fichier pour faire du déploiement en continu à l'aide de Github Actions.

## Choix technologiques pour l'intégration continue

### Github Action
Nous utilisons les Github Action pour construire l'image Docker et la "push" sur DockerHub 
lorsque nous poussons du code sur notre repo Github ou même quand on créer un pull-request. 
Les Github Action sont un aussi un standard dans l'industrie. C'est une bonne manière 
pour s'assurer la qualité du code présent dans le repo. Aussi, les Github Action 
permettent d'exécuter des actions de manière conditionnelle, ce qui est parfait pour
l'implémentation que nous devions faire.

### Docker Hub
Docker Hub permet de facilement faire la gestion et le partage d'image Docker. C'est 
semblable à github. Étant donné que nous utilisons déjà Docker et que nous devions 
déployer nos images sur Docker hub, nous n'avions pas vraiment le choix de l'utiliser.

## Choix technologiques pour le déploiement continu

### Github Action
Étant donné que nous ont utilisait déjà des Github Action pour l'intégration en
continu, nous avons décidé de continué à l'utiliser pour le déploiement en continu.
Il est aussi pratique de voir à un seul endroit, github, si notre intégration et 
notre déploiement à fonctionner. 