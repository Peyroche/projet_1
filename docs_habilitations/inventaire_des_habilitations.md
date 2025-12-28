# Inventaire des habilitations

## Description
Ce document décrit les groupes et utilisateurs utilisés pour la gestion des habilitations sur GLPI.

---

## Groupes employés MDF

| GROUPES          | DESCRIPTIONS                                                  |
|------------------|---------------------------------------------------------------|
| GLPI_Admins      | Administrateurs du parc, droits complets sur GLPI             | 
| GLPI_Tech_N1     | Techniciens support niveau 1 (tickets simples, comptes, apps) | 
| GLPI_Tech_N2     | Techniciens support niveau 2 (réseau, serveurs, escalades)    | 
| GLPI_Users       | Utilisateurs finaux, accès au portail GLPI                    | 
| GLPI_Audit       | Auditeurs internes/externes, accès en lecture seule           | 
| GLPI_Licences    | Gestionnaires des licences logicielles                        | 

---

## Employés MDF
 
| IDENTIFIANTS            | GROUPE(S)                | PROFILS                      |
|-------------------------|--------------------------|------------------------------|
| Administrateur Systèmes | GLPI_Admins              | Super-Admin                  |
| Technicien N2           | GLPI_Tech_N2             | Technician                   |
| Responsable licences    | GLPI_Licences            | Observer                     |
| Technicien N1           | GLPI_Tech_N1             | Technician                   |  
| Commercial              | GLPI_Users               | Self-Service                 |
| Responsable marketing   | GLPI_Users               | Self-Service                 |
| Customer Success        | GLPI_Users               | Self-Service                 |
| Stagiaire               | GLPI_Users               | Self-Service                 |

---

## Notes
- Les données sont fictives et destinées à la démonstration.
- Les fiches sont formatées pour être compatibles avec GLPI.
- Les informations sensibles (nom, prénom, téléphone, ...) sont volontairement exclues.
