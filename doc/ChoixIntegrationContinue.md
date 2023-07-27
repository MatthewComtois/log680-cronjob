# Choix pipeline d'intégration continue

Ce document explique les différents choix reliés à l'implémentation du pipeline d'intégration continue


## Github Action
Nous avons décidé d'exécuter notre Github Actions à chaque fois qu'un push est exécuté sur la branch "main".
C'est à ce moment que nous considérons qu'il est approprié de "build" et "push" notre image sur Docker Hub.

Pour ce qui est du Github actions en tant que telles, seulement si l'événement qui à déclencher l'action est 
un push dans la branche "main", on build l'image Docker et on pousse ensuite l'image sur Docker Hub avec deux
tags, soit "latest" et le numéro de build de Github.