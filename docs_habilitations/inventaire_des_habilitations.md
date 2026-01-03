# Inventaire des habilitations

## Description
Ce document décrit les groupes utilisés pour la gestion des habilitations.

---

## Groupes GLPI
Un groupe GLPI sert à : affecter des tickets, organiser les équipes, filtrer la visibilité, appliquer des règles GLPI.

| Groupes GLPI       | Employés MDF                                                  | Droits attribués sur GLPI  |
|------------------- |---------------------------------------------------------------|----------------------------|
| Groupe RH          | Chef de projet                                                | Super-Admin                |
| Groupe Direction   | Administrateur système                                        | Super-Admin                |
| Groupe Techniciens | Technicien niveau 1 & 2                                       | Technician                 |
| Groupe users       | Commercial, Responsable marketing, Customer Success, Stagaire | Self-Service               |
| Groupe Licences    | Responsable licences                                          | Observer                   |

---

## Groupes Domaine Local (DLG)
Un groupe Domaine local (Domain Local Group) sert à : attribuer des droits NTFS sur un dossier partagé, attribuer des droits sur une imprimante, attribuer des droits sur une ressource du domaine, gérer les autorisations locales sur un serveur membre.

| Groupes Domaine Local  |  Groupe Global          | Employés MDF                                                  | Droit attribués sur AD  |
|------------------------|-------------------------|---------------------------------------------------------------|-------------------------|
| DLG_RH                 |  GG_RH                  | Chef de projet                                                | Full                    |
| DLG_Admins             |  GG_Admins              | Administrateur système                                        | Full                    |
| DLG_Tech               |  GG_Tech                | Technicien niveau 1 & 2                                       | RW (Lecture + Ecriture) |
| DLG_Licences           |  GG_Users               | Commercial, Responsable marketing, Customer Success, Stagaire | RO (Lecture seule)      |
| DLG_Users              |  GG_Licences            | Accès portail utilisateur                                     | RW (Lecture + Ecriture) |


---

[Fiche 2 : Création des groupes dans Active Directory](Fiche_002.pdf)

---

## Notes
- Les données sont fictives et destinées à la démonstration.
- Les fiches sont formatées pour être compatibles avec GLPI.
- Les informations sensibles (nom, prénom, téléphone, ...) sont volontairement exclues.