# Procédure d’intégration des utilisateurs AD ↔ GLPI

## 🎯 Objectif
Cette procédure décrit les étapes permettant :
- d’ajouter un nouvel utilisateur dans Active Directory (AD) et de l’intégrer automatiquement dans GLPI ;
- de modifier les droits d’un utilisateur existant via les groupes AD et leur correspondance avec les profils GLPI.

---

## ⚙️ Pré-requis
- Active Directory opérationnel avec une organisation des **OU (Organizational Units)** claire.
- GLPI configuré avec un **connecteur LDAP** pointant vers l’AD.
- Mapping défini entre **Groupes AD** et **Profils GLPI** (ex. : `AD_Groupe_Tech` → `Profil Technicien`).

---

## 📝 Étapes d’ajout d’un nouvel utilisateur

1. **Création dans Active Directory**
   - Ouvrir la console **Active Directory Users and Computers**.
   - Créer un nouvel utilisateur dans l’OU appropriée (ex. : `OU=Users,DC=entreprise,DC=fr`).
   - Renseigner les champs obligatoires :  
     - `Nom`  
     - `Prénom`  
     - `Identifiant de connexion (sAMAccountName)`  
     - `Adresse e-mail`  

2. **Attribution aux groupes AD**
   - Ajouter l’utilisateur aux groupes correspondant à ses habilitations (ex. : `Support_IT`, `Finance_Users`).
   - Vérifier que les groupes choisis ont une correspondance dans GLPI.

3. **Synchronisation LDAP dans GLPI**
   - Accéder à **Configuration → Authentification → LDAP directories**.
   - Lancer une **synchronisation manuelle** ou attendre la synchronisation planifiée.
   - Vérifier que l’utilisateur apparaît dans GLPI avec le bon profil.

4. **Validation**
   - Se connecter à GLPI avec le compte nouvellement créé.
   - Vérifier l’accès aux menus et fonctionnalités correspondant au profil attribué.

---

## 🔧 Étapes de modification des droits d’un utilisateur

1. **Modification des groupes AD**
   - Dans AD, ouvrir la fiche de l’utilisateur.
   - Ajouter ou retirer des groupes selon les nouvelles habilitations.

2. **Propagation vers GLPI**
   - Attendre la synchronisation LDAP ou la déclencher manuellement.
   - Vérifier que le profil GLPI a été mis à jour automatiquement.

3. **Contrôle**
   - Demander à l’utilisateur de se reconnecter à GLPI.
   - Vérifier que les droits correspondent aux nouvelles habilitations.

---

## 📑 Bonnes pratiques
- Toujours documenter les changements d’habilitation dans un **registre des accès**.  
- Utiliser des **groupes AD normalisés** (nommage clair, sans accents ni espaces).  
- Tester la synchronisation LDAP après toute modification de configuration.  
- Prévoir un **compte de test** pour valider les flux AD ↔ GLPI avant mise en production.  

---

## ✅ Exemple de mapping
| Groupe AD        | Profil GLPI    | Description des droits            |
|------------------|----------------|-----------------------------------|
| `Support_IT`     | Technicien     | Accès aux tickets et inventaire   |
| `Finance_Users`  | Utilisateur    | Déclaration de tickets            |
| `Admins_GLPI`    | Super-Admin    | Administration complète de GLPI   |

---

## 📌 Références
- Documentation officielle GLPI : [https://glpi-project.org](https://glpi-project.org)  
- Documentation Microsoft Active Directory : [https://learn.microsoft.com](https://learn.microsoft.com)  