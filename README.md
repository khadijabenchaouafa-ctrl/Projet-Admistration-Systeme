# Projet-Administration-Systeme

##   Déploiement d'un site statique web avec Apache
 

#Objectif
 Ce projet a pour objectif de mettre en place un serveur web Apache permettant d'héberger un site 
statique(HTML/CSS), tout en assurant la configuration réseau et la sécurisation du serveur.

#Membres du groupe
- Nana idrissa Aicha : Installation d'apache
- Meryem chalh :Configuration du serveur (VirtualHost, réseau)
- Noura ajarra: Développement du site web(HTML/CSS)
- Khadija benchouafa: Sécurisation(UFW) + Documentation

#Technologies utilisées

- Apache2
- HTML/CSS
- Git / Github
- Ubuntu
- UFWW(Firewall)

# Structure du projet
 Projet-Administration-Systeme/
|
|___ html/             # Fichiers du site web
|    |___ index.html
|    |___ style.css
|
|___ scripts/          # Scripts d'installation
|
|___ config/           # Docummentation (sécurité, réseau...)
|
|___ README.md         # Description du projet

# Installation du prpjet

1. Cloner le dépot

git clone https://github.com/khadijabenchaouafa-ctrl/Projet-Admistration-Systeme
cd Projet-Admistration-Systeme

2. Installer Apache

sudo apt update
sudo apt install apache2 -y

3. Copier le site dans apache

sudo cp -r html/* /var/www/html/

4. Démarrer Apache

sudo systemctl start apache2
sudo systemctl enable apache2

# Accès au site 

Ouvrir dans le navigateur:
http://monsite.local/

# Configuration du serveur(VirtualHost)

Créer un fichier:
sudo nano /etc/apache2/sites-available/monsite.conf
Activer:
sudo a2ensite monsite.conf
sudo systemctl reload apache2

# Sécurisation du serveur(UFW)

Autoriser Apahe:

sudo ufw allow 'Apache'

Activer le firewall:

sudo ufw enable

Vérifier:

sudo ufw status

# Travail collaboratif avec Git

Chaque étudiant travaille sur une brache
git checkout -b nom-branche
git add .
git commit -m "message"
git push origin nom-brache

Puis fusion via Pull Request sur Github.

## Conclusion:

Ce projet nous permis de comprendre:

  - le déploiement d'un serveur web Apache
  - le travail collaboratif avec Github
  - la configuration réseau et la sécuristaion d'un serveur


