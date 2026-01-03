# Inventaires Hardware & Software

## Description
Ce document présente l’inventaire matériels et logiciels géré sur GLPI.  

---

## Inventaire Hardware

## Ordinateurs

| Nom        | Statut       | Fabricant |  Type       | Modèle          | Lieu        | Système d'exploitation      | Processeur    | RAM    | Stockage   | 
|------------|--------------|-----------|-------------|-----------------|-------------|-----------------------------|---------------|--------|------------|
| Ordinateur | En service   | Dell      | Portable    | OptiPlex 7090   | Bureau 02   | Windows 11 Pro              | i5-11400      | 16 Go  | 512 Go SSD |  
| Ordinateur | En service   | Lenovo    | Bureau      | ThinkPad T14    | Bureau 02   | Windows 11 Pro              | Ryzen 5 Pro   | 16 Go  | 512 Go SSD |
| Serveur    | En service   | HP        | Virtuel     | ProLiant DL380  | Bureau 02   | Windows Server 2019 et ESXi | 2x Xeon Gold  | 128 Go | 4x 2 To    |

## Imprimante

| Nom        | Statut       | Fabricant | Lieu          |   Type       | Modèle          |
|------------|--------------|-----------|---------------|--------------|-----------------|
| Ordinateur | En service   |    HP     | Bureau 01     | Portable     | LaserJet Pro    |

## Matériels réseau

| Nom     |  Statut       | Fabricant  | Lieu       | Modèle        |
|---------|---------------|------------|------------|---------------|
| Switch  | En service    | Cisco      | Bureau 01  | Catalyst 2960 | 
| Routeur | En service    | Cisco      | Bureau 01  | ISR 4331      |  

---

## Inventaire Software

## Systèmes d’exploitation

| Nom           | Editeur          | Version        | Type de Licences    | Nb. Licences | Notes                   |
|-------------  |------------------|----------------|---------------------|--------------|-------------------------|
| Windows Server| Microsoft        | 2019 Datacenter| Licence volume      | 1            | Utilisé sur serveur HP  |
| ESXi          | VMware           | 7.0            | Licence commerciale | 2            | Utilisé sur serveur HP  |
| Windows pro   | Microsoft        | 11             | Licence volume      | 6            | Utilisé sur ordinateurs |                

## Applications bureautiques

| Nom         | Editeur            | Version        | Types de Licences | Nb. Licences | 
|-------------|--------------------|----------------|-------------------|--------------|
| Office 365  | Microsoft          | E3             | SaaS abonnement   | 6            | 

## Tableau comparatif des licences

| Types de Licences     | Mode de distribution | Durée / Renouvellement            | Avantages                   | Inconvénients                          |
|-----------------------|----------------------|-----------------------------------|-----------------------------|----------------------------------------|
| Licence volume        | On-premise           | Achat unique + Software Assurance | Support officiel, stabilité | Coût élevé, dépendance éditeur         |
| Licence commerciale   | On-premise           | Abonnement annuel                 | Virtualisation robuste      | Coût élevé, renouvellement obligatoire |
| Licence volume        | On-premise           | Abonnement mensuel ou annuel      | Accès instantané            | Coût élevé, renouvellement obligatoire |
 
---

[Fiche 1 : Installation et configuration de GLPI](Fiche_001.pdf)

---

## Notes
- Les données sont fictives et destinées à la démonstration.
- Les fiches sont formatées pour être compatibles avec GLPI.
- Les informations sensibles (IP, mots de passe, numéros de série) sont volontairement exclues.
