# Installation de GLPI

## Description
Ce document décrit les étapes utiliser pour l'installation de GLPI.

---

## Outils utilisés
- Windows 64 bit
- WampServer (PHP version 7.4.33)
- GLPI version 10.0.6

---

## Téléchargements
- Télécharger WampServer : https://www.wampserver.com
- Installer WampServer sur Windows et choix du répertoire par défaut c:\wamp64 
- Télécharger les packages Microsoft Visual C++ : https://wampserver.aviatechno.net
- Télécharger GLPI : https://www.glpi-project.org/en/new-version-glpi-10-0-6/
- Décompresser et importer les fichiers GLPI dans `/wamp64/www/glpi`.

---

## Configurations
- Démarrer WampServer puis accéder à `http://localhost/Phpmyadmin`.

![Ajout](images/base_1.png)

- Créer une base de données `glpi`.

![Ajout](images/base_2.png)

- Accéder ensuite à `http://localhost/glpi`.
- Connexion à glpi entant que super-admin avec pour `identifiant : glpi` et `mot de passe : glpi`.

![Ajout](images/glpi_1.png)

- Affichage du tableau de bord glpi.

![Ajout](images/glpi.png)

---

## Post installation
Voici les actions urgentes à effectuer pour sécuriser glpi :
- Modifier le mot de passe par défaut : GLPI crée automatiquement des comptes (administrateur, technicien, utilisateur standard, utilisateur limité) avec des mots de passes standards (glpi, tech, normal, post-only).
- Supprimer le fichier install/install.php dans le répertoire glpi.
