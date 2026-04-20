INSTALLATION D'APACHE2 SUR UBUNTU 

pour installer et demarer le serveur web apache sur ubuntu j'ai suivi les étapes suivantes: 

1. sudo apt update 
     pour garantir que le systeme est a jour , stable et sécurisé. cela évite 
     les conflits de dépendances et assure que les paquets que vous installez fonctionneront 
     correctemment avec les versions déja présentes.
2. sudo apt install apache2
     installe les binaires pour gérer le serveur , les fichiers de configuration 
     pour personnaliser son comportement , et un  
     répertoire web (/var/www/html/) par défaut pour héberger vos pages .
3. systemctl status apache2
     rôle: vérifier l'état du service Apache2 géré par systemd
     il affiche les informations comme :
        . le loaded : indique que le service apache2 est  bien installé et reconnu par systemd
        . active : montre si le service est en cours d'exécution(running),arrêté(inactive)ou 
                   en erreur (failed)

        . docs: lien vers la documentation officielle du service apache 

        . mains pid : identifiant du processus principal apache en cours 
 
        . tasks : nombre de processus ou threads utilisés par apache 

        . memory: quantité de memoire consommée par le service 

        . cpu : temps processeur utilisé par apache  depuis son lancement

        .cgroup: chemin du groupe de contrôle systemd auquel appartient le service
 
        . dates and journaux : affichent quand le service a démaré et les évènements (logs)
