# 🔍 Auditabilité des habilitations AD ↔ GLPI

## 🎯 Objectif
Garantir la traçabilité des accès utilisateurs entre Active Directory (AD) et GLPI, en répondant aux questions :
- Qui a accès à quoi ?
- Pourquoi cette personne a-t-elle ces droits ?
- Comment ces droits sont-ils attribués, modifiés et contrôlés ?

---

## 🧩 Principes de traçabilité

- **Source unique d’identité** : Active Directory centralise les comptes utilisateurs.
- **Synchronisation LDAP** : GLPI récupère les informations d’AD via un connecteur LDAP.
- **Attribution des droits** : Les groupes AD sont mappés vers des profils GLPI.
- **Justification des accès** : Chaque habilitation est liée à une fonction métier ou un rôle technique.

---

## 📑 Registre des habilitations

Un fichier d’inventaire (CSV ou Markdown) est maintenu pour documenter :

| Utilisateur       | Groupe AD        | Profil GLPI    | Rôle métier         | Justification d’accès             |
|-------------------|------------------|----------------|----------------------|-----------------------------------|
| jdupont           | Support_IT       | Technicien     | Support niveau 1     | Traitement des tickets            |
| mleroy            | Admin_GLPI       | Super-Admin    | Responsable IT       | Administration de la plateforme   |
| afournier         | Finance_Users    | Utilisateur    | Comptabilité         | Déclaration d’incidents matériels |

---

## 🛠️ Mécanismes de contrôle

- **Journalisation GLPI** : toutes les connexions, modifications de tickets et changements de profil sont enregistrés.
- **Logs LDAP** : les synchronisations entre AD et GLPI sont tracées (horodatage, utilisateurs importés).
- **Historique des groupes AD** : les ajouts/suppressions de groupes sont visibles dans les attributs AD.
- **Revue périodique des accès** : audit mensuel des profils GLPI et comparaison avec les rôles métier.

---

## ✅ Exemple de scénario d’audit

> 🔎 Cas : L’auditeur demande pourquoi l’utilisateur `jdupont` a accès à l’inventaire GLPI.

**Réponse documentée :**
- `jdupont` appartient au groupe AD `Support_IT`.
- Ce groupe est mappé vers le profil GLPI `Technicien`.
- Le rôle métier associé est "Support niveau 1".
- La justification est : "Traitement des tickets et gestion de l’inventaire".
- La dernière synchronisation LDAP a eu lieu le `2025-12-10` à `03:00`.

---

## 📌 Bonnes pratiques

- Utiliser des **groupes AD explicites** (`Support_IT`, `Admin_GLPI`) pour faciliter la lecture.
- Documenter chaque **profil GLPI** avec ses droits et sa finalité.
- Archiver les **exports d’habilitations** à chaque revue mensuelle.
- Intégrer cette documentation dans le **référentiel sécurité** ou le **plan de continuité**.

---

## 📂 Références

- [Documentation GLPI - LDAP & Authentification](https://glpi-project.org)
- [Microsoft AD - Gestion des groupes et utilisateurs](https://learn.microsoft.com)
- [ISO/IEC 27001 - Contrôle des accès](https://www.iso.org/isoiec-27001-information-security.html)
