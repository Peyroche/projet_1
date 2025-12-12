# Inventaire des habilitations (AD ↔ GLPI)

Ce document décrit les groupes Active Directory utilisés pour la gestion des habilitations,
ainsi que leur correspondance avec les profils GLPI. Il inclut également des utilisateurs pour simuler un environnement professionnel.

---

## 👥 Groupes Active Directory

| Groupe AD        | Description                                                   | Mapping GLPI        |
|------------------|---------------------------------------------------------------|---------------------|
| GLPI_Admins      | Administrateurs du parc, droits complets sur GLPI et AD       | Super-Admin         |
| GLPI_Tech_N1     | Techniciens support niveau 1 (tickets simples, comptes, apps) | Technicien          |
| GLPI_Tech_N2     | Techniciens support niveau 2 (réseau, serveurs, escalades)    | Technicien avancé   |
| GLPI_Users       | Utilisateurs finaux, accès au portail GLPI                    | Self-Service        |
| GLPI_Audit       | Auditeurs internes/externes, accès en lecture seule           | Observateur         |
| GLPI_Licences    | Gestionnaires des licences logicielles                        | Gestionnaire        |

---

## 👤 Utilisateurs

| Utilisateur      | Rôle                     | Groupe(s) AD        | usage                                                |
|------------------|--------------------------|---------------------|------------------------------------------------------|
| Alfred Benoit    | Administrateur Systèmes  | GLPI_Admins         | Configure GLPI, gère AD et sauvegardes               |
| Sophie Martin    | Technicien N1            | GLPI_Tech_N1        | Réinitialise mots de passe, installe logiciels       |
| Karim Benali     | Technicien N2            | GLPI_Tech_N2        | Résout incidents réseau, escalade vers N3            |
| Julie Robert     | Utilisatrice métier      | GLPI_Users          | Déclare un ticket via portail GLPI                   |
| Marc Leroy       | Auditeur interne         | GLPI_Audit          | Vérifie conformité inventaire/licences               |
| Claire Dubois    | Responsable licences     | GLPI_Licences       | Suit les licences Adobe, Microsoft, VMware           |


