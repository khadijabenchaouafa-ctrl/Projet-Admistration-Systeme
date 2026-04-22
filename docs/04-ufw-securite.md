####  Sécurisation du serveur avec UFW

## Introduction

Dans le cadre de ce projet, nous avons mis en place un mécanisme de sécurité
pour protéger le serveur web Apache.
Pour cela, nous avons utilisés UFW(Uncomplicated Firewall), un outil simple 
de gestion de par-feu sous Linux.

# Qu'est-ce qu'un pare-feu ?

Un pare-feu est un système de sécurité qui permet de controler les connexions
réseau entrantes et sortantes.
Il permet de:
  - Bloquer les accès non autorisés
  - Autoriser uniquement les services nécessaires
  - Protéger le serveur contre les attaques

# Commandes urilisées

1. Autoriser Apache
sudo ufw allow 'Apache'

-> Cette commande permet d'ouvrir:
  - le port 80(HTTP)
  - le port 443(HTTPS)

2. Autoriser OpenSSH(IMPORTANT)
sudo ufw allow OpenSSH

-> Permet de garder l'accès au serveur à distance.

3. Activer la pare-feu
sudo ufw enable

-> Activre le protection du serveur.

4. Vérifier le status
sudo ufw status verbose

-> Permet de voir les règles actives.

# Pourquoi autorisre OpenSSH avant d'ctiver UFW ?

Il est très important d'autoriser OpenSSH avant d'activer le firewall, car:
  - Sinon, l'accès SSH sera bloqué
  - Le srveur deviendra inaccessible à distance
  - On risque de perdre le controle du serveur 

## Conclusion
La configuration de UFW permet de sécuriser efficacement le serveur en 
limitant les accès aux services essentiels.
Cela renforce le protection du système tout en garantissant le bon 
fonctionnement du serveur web.
