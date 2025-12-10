# Inventaire Software

## Description
Ce document présente l’inventaire des logiciels gérés dans la CMDB.  
Chaque fiche inclut les informations essentielles : éditeur, version, type de licence, nombre d’utilisateurs et état de conformité.

---

## Systèmes d’exploitation

| Éditeur     | Produit             | Version         | Type de licence | Nb. licences | Conformité | Notes |
|-------------|--------------------|-----------------|-----------------|--------------|------------|-------|
| Microsoft   | Windows Server      | 2019 Datacenter | Licence volume  | 5            | ✅ Conforme | Utilisé sur serveurs HP |
| Canonical   | Ubuntu Server       | 22.04 LTS       | Open source GPL | N/A          | ✅ Conforme | Utilisé sur serveurs Dell |
| VMware      | ESXi                | 7.0             | Licence commerciale | 3        | ⚠️ À renouveler | Serveurs Lenovo |

---

## Applications bureautiques

| Éditeur     | Produit             | Version         | Type de licence | Nb. licences | Conformité | Notes |
|-------------|--------------------|-----------------|-----------------|--------------|------------|-------|
| Microsoft   | Office 365          | E3              | SaaS abonnement | 50           | ✅ Conforme | Comptes synchronisés Azure AD |
| LibreOffice | LibreOffice Suite   | 7.6             | Open source LGPL| N/A          | ✅ Conforme | Alternative open source |

---

## Logiciels créatifs

| Éditeur     | Produit             | Version         | Type de licence | Nb. licences | Conformité | Notes |
|-------------|--------------------|-----------------|-----------------|--------------|------------|-------|
| Adobe       | Creative Cloud      | 2025            | SaaS abonnement | 10           | ✅ Conforme | Utilisé par l’équipe design |
| GIMP        | GIMP                | 2.10            | Open source GPL | N/A          | ✅ Conforme | Alternative open source |

---

## Collaboration et communication

| Éditeur     | Produit             | Version         | Type de licence | Nb. licences | Conformité | Notes |
|-------------|--------------------|-----------------|-----------------|--------------|------------|-------|
| Slack       | Slack Standard      | Cloud SaaS      | Abonnement mensuel | 20        | ✅ Conforme | Utilisé par l’équipe projet |
| Microsoft   | Teams               | Inclus Office 365 | SaaS abonnement | 50        | ✅ Conforme | Intégré à Office 365 |

---

## Notes
- Les données sont fictives et destinées à la démonstration.
- Les fiches sont formatées pour être compatibles avec GLPI et audit‑ready.
- Les informations sensibles (clés de licence, identifiants) sont volontairement exclues.
