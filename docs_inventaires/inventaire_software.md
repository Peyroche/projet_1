# Inventaire Software

## Description
Ce document présente l’inventaire des logiciels gérés sur GLPI.  

---

## Systèmes d’exploitation

| NOM           | EDITEUR          | VERSION        | TYPES DE LICENCE    | NOMBRES DE LICENCE | CONFORMITE      | Notes                            |
|-------------  |------------------|----------------|---------------------|--------------------|-----------------|----------------------------------|
| Windows Server| Microsoft        | 2019 Datacenter| Licence volume      | 1                  | ✅ Conforme     | Utilisé sur serveur HP           |
| ESXi          | VMware           | 7.0            | Licence commerciale | 2                  | ✅ Conforme     | Utilisé sur serveur HP           |
| Windows pro   | Microsoft        | 11             | Licence volume      | 6                  | ✅ Conforme     | Utilisé sur ordinateurs          |                

---

## Applications bureautiques

| NOM         | EDITEUR            | VERSION        | TYPES DE LICENCE | NOMBRES DE LICENCE | CONFORMITE      | 
|-------------|--------------------|----------------|----------------- |--------------------|-----------------|
| Office 365  | Microsoft          | E3             | SaaS abonnement  | 6                  | ✅ Conforme    | 

---

## Tableau comparatif des licences

| TYPE DE LICENCE       | MODE DE DISTRIBUTION | DUREE / RENOUVELLEMENT            | AVANTAGES                   | INCONVENIENTS                          |
|-----------------------|----------------------|-----------------------------------|-----------------------------|----------------------------------------|
| Licence volume        | On-premise           | Achat unique + Software Assurance | Support officiel, stabilité | Coût élevé, dépendance éditeur         |
| Licence commerciale   | On-premise           | Abonnement annuel                 | Virtualisation robuste      | Coût élevé, renouvellement obligatoire |
| Licence volume        | On-premise           | Abonnement mensuel ou annuel      | Accès instantané            | Coût élevé, renouvellement obligatoire |

---

## Notes
- Les données sont fictives et destinées à la démonstration.
- Les fiches sont formatées pour être compatibles avec GLPI et audit‑ready.
- Les informations sensibles (clés de licence, identifiants) sont volontairement exclues.
