---
layout: page
title:   Accès ScienceFS
permalink: /AccesSFS/
---

ATTENTION : Cette page est en cours de révision, certaines informations peuvent être périmées. En cas de difficulté, prendre contact.


## ACCÈS DEPUIS CLOUD@VD
Votre répertoire personnel est disponible sous forme de point de montage via la technologie SSHFS. Pour y accéder depuis une machine virtuelle utilisant CentOS, utilisez les commandes suivantes :

yum -y install fuse-sshfs

mkdir /mesdocuments

sshfs -o Ciphers=arcfour256 <prenom.nom>@sciencefs.di.u-psud.fr:/sciencefs/homes/<prenom.nom> /mesdocuments

Pour une machine virtuelle utilisant Ubuntu, remplacez yum -y install fuse-sshfs par apt-get install sshfs

L'option -o Ciphers=arcfour256 permet d'augmenter les performances en diminuant légèrement la sécurité des flux de données, ce qui ne pose pas de problème entre le réseau de l'université et Cloud@VD.

## ACCÈS DEPUIS LE GROUPE DE MACHINES PLUTON
Depuis les machines du groupe Pluton, l'accès est immédiat et transparent.
Votre "home directory" (répertoire par défaut) est de la forme /sciencefs/homes/<prenom.nom>

Pour des raisons historiques, un chemin de la forme /netapp_nix/homes/<login court Adonis> est également maintenu.

## ACCÈS DEPUIS VOTRE MACHINE DE BUREAU WINDOWS
Il est possible d'accéder à votre espace en HTTP et WebDav via l'adresse https://sciencefs.di.u-psud.fr/mesdocuments/. Cette adresse n'est disponible que depuis le réseau de l'université (VPN inclus).
Ce moyen d'accès permet par exemple de voir vos fichiers depuis un navigateur web ou depuis une machine Windows en tant que lecteur externe (voir la section documentation pour plus d'informations). Pour des raisons de performances, vous pouvez utiliser "http" à la place de de "https".
Il est également possible de vous connecter via SFTP (FTP par SSH) à l'aide d'un outil comme Filezilla ou Cyberduck. Pour cela, utilisez sciencefs.di.u-psud.fr comme nom de serveur et vos identifiants Adonis habituels.

## ACCÈS DEPUIS VOTRE MACHINE DE BUREAU MACOS

Sous macOSX, pour se connecter à l'espace de stockage, dans un premier temps, dans Safari allez à cette adresse: https://sciencefs.di.u-psud.fr/mesdocuments/
Identifiez-vous avec vos login (prenom.nom) et mot de passe Adonis.
A partir du Finder, allez dans le menu "Aller -> Se connecter au serveur" et entrez : https://sciencefs.di.u-psud.fr/mesdocuments/
Cliquez sur le signe (+) pour ajouter cette adresse de façon pérenne à la liste des serveurs.
Une boîte de dialogue vous demande l'autorisation d'utiliser le mot de passe que vous aurez précédemment indiqué avec Safari. Cliquez sur "Toujours autoriser". L'espace de stockage apparait comme un dossier sur le bureau.
Vous pouvez en faire un alias pour y accéder plus rapidement ensuite :
Cliquez sur le disque mesdocuments et allez dans le menu "Fichier -> Créer un alias".
En double-cliquant sur l'alias, cela montera automatiquement l'espace de stockage.
Mettez l'alias à un endroit qui ne vous gêne pas ; vous pouvez aussi en mettre une copie dans le Dock.
Si vous voulez que l'espace de stockage soit accessible dès l'ouverture de la session sur l'ordinateur, allez dans le menu "Pomme->Préférence Système" et choisir l'élément "Utilisateurs et Groupes", puis l'onglet "Ouverture".
Cliquez sur le signe (+) et choissez l'alias que vous venez de créer. A l'ouverture de session, l'espace de stockage sera directement accessible.

## ACCÈS DEPUIS L'EXTÉRIEUR DE L'UNIVERSITÉ
L'accès au stockage est disponible depuis l'extérieur de l'université. Vous pouvez donc utiliser les procédures de connexion via SSH et HTTPS décrites ci-dessus.
## DOCUMENTATION
Accès WebDav via Windows : Tout d'abord, la valeur de la clé de registre "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\WebClient\Parameters\BasicAuthLevel" doit être "2".
Ensuite, ajoutez un nouveau lecteur réseau et entrez comme URL https://sciencefs.di.u-psud.fr/mesdocuments/
