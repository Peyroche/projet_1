# Installation de GLPI

## Description
Ce document décrit les étapes d’installation de GLPI pour le projet MDF (Sales and Marketing).

## Installation de WampServer
Téléchargement de la dernière version WampServer : https://www.wampserver.com
![Wampserver](Wampserver.png)























- OS : Ubuntu 22.04
- Serveur : Apache2
- Base de données : MySQL/MariaDB
- PHP : 8.1

## Téléchargement
Télécharger GLPI depuis le site officiel : https://glpi-project.org  
Version utilisée : GLPI 10.0.x

## Configuration
1. Créer une base de données `glpi_db`.
2. Créer un utilisateur `glpi_user` avec mot de passe.
3. Importer les fichiers GLPI dans `/var/www/html/glpi`.

## Installation via navigateur
- Accéder à `http://localhost/glpi`.
- Suivre l’assistant d’installation.
- Configurer la base de données.
- Créer les comptes par défaut.

## Post-installation
- Modifier le mot de passe admin.
- Créer les entités et catégories.
- Vérifier les modules PHP.

