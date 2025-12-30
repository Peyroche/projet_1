# Inventaire des habilitations

## Description
Ce document décrit les groupes et utilisateurs utilisés pour la gestion des habilitations sur GLPI.

---

## Groupes Globaux (GG) sur AD
Ce sont les groupes qui représentent qui sont les utilisateurs.

| Groupe Global    | Rôles                                                         |
|------------------|---------------------------------------------------------------|
| GG_GLPI_Admins   | Administrateurs du parc, droits complets sur GLPI             | 
| GG_GLPI_Tech_N1  | Techniciens support niveau 1 (tickets simples, comptes, apps) | 
| GG_GLPI_Tech_N2  | Techniciens support niveau 2 (réseau, serveurs, escalades)    | 
| GG_GLPI_Users    | Utilisateurs finaux, accès au portail GLPI                    | 
| GG_GLPI_Audit    | Auditeurs internes/externes, accès en lecture seule           | 
| GG_GLPI_Licences | Gestionnaires des licences logicielles                        | 

---

## Groupes Domaine Local (DLG) sur AD
Ce sont les groupes qui représentent ce à quoi les utilisateurs ont accès. 

|  Groupes Domaine Local  | Droit attribué                          |
|-------------------------|-----------------------------------------|
| DLG_GLPI_Admins_Full    | Accès complet à GLPI                    |
| DLG_GLPI_Tech_N1_RW     | Accès technicien N1 (tickets simples)   |
| DLG_GLPI_Tech_N2_RW     | Accès technicien N2 (réseau, serveurs)  |
| DLG_GLPI_Audit_RO       | Accès lecture seule                     |  
| DLG_GLPI_Licences_RW    | Gestion des licences                    |
| DLG_GLPI_Users_Portal   | Accès portail utilisateur               |

---

## Attribution des droits dans GLPI

|  Groupe Domaine Local   | Groupes Domaine Local    | Profils
|-------------------------|--------------------------|------------------------------|
| Administrateur Systèmes | DLG_GLPI_Admins_Full     | Super-Admin                  |
| Technicien N2           | DLG_GLPI_Tech_N2_RW      | Technician                   |
| Responsable licences    | DLG_GLPI_Licences_RW     | Observer                     |
| Technicien N1           | DLG_GLPI_Tech_N1_RW      | Technician                   |  
| Commercial              | DLG_GLPI_Users_Portal    | Self-Service                 |
| Responsable marketing   | DLG_GLPI_Users_Portal    | Self-Service                 |
| Customer Success        | DLG_GLPI_Users_Portal    | Self-Service                 |
| Stagiaire               | DLG_GLPI_Users_Portal    | Self-Service                 |

---

## Notes
- Les données sont fictives et destinées à la démonstration.
- Les fiches sont formatées pour être compatibles avec GLPI.
- Les informations sensibles (nom, prénom, téléphone, ...) sont volontairement exclues.
