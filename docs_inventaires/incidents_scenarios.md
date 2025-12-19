# Scénarios d'incidents - CMDB MDF

## Description
Ce document présente des scénarios d’incidents simulés et documentés dans la CMDB.  
Chaque scénario suit les étapes ITIL : détection, diagnostic, résolution et post‑mortem.

---

## Scénario 1 : Panne réseau dans le Datacenter A

### Chronologie
| Heure       | Étape                  | Description                                                                 |
|-------------|------------------------|-----------------------------------------------------------------------------|
| 09:00       | Détection              | Les utilisateurs signalent une perte de connexion au serveur Dell R740.     |
| 09:10       | Diagnostic             | Vérification des switchs Cisco Catalyst : un module est en panne.           |
| 09:20       | Escalade               | Incident transmis à l’équipe réseau.                                        |
| 09:40       | Résolution             | Remplacement du module défectueux et redémarrage du switch.                 |
| 10:00       | Rétablissement         | Connexion rétablie pour tous les utilisateurs.                              |
| 10:30       | Post‑mortem            | Rapport d’incident rédigé, recommandation : ajouter un switch de secours.   |

---

## Scénario 2 : Défaillance du NAS Synology

### Chronologie
| Heure       | Étape                  | Description                                                                 |
|-------------|------------------------|-----------------------------------------------------------------------------|
| 14:00       | Détection              | Alertes GLPI : espace disque critique sur NAS DS920+.                       |
| 14:15       | Diagnostic             | Vérification : un disque dur montre des erreurs SMART.                      |
| 14:30       | Escalade               | Incident transmis à l’équipe stockage.                                      |
| 15:00       | Résolution             | Remplacement du disque et reconstruction du RAID.                           |
| 16:00       | Rétablissement         | Volume restauré, aucune perte de données.                                   |
| 16:30       | Post‑mortem            | Rapport : prévoir une surveillance proactive des disques via DSM.           |

---

## Scénario 3 : Incident logiciel - Licence expirée

### Chronologie
| Heure       | Étape                  | Description                                                                 |
|-------------|------------------------|-----------------------------------------------------------------------------|
| 11:00       | Détection              | Utilisateurs ne peuvent plus accéder à VMware ESXi (licence expirée).       |
| 11:15       | Diagnostic             | Vérification : licence commerciale non renouvelée.                          |
| 11:30       | Escalade               | Incident transmis à l’équipe systèmes.                                      |
| 12:00       | Résolution             | Renouvellement de la licence et activation immédiate.                       |
| 12:30       | Rétablissement         | Accès rétabli aux machines virtuelles.                                      |
| 13:00       | Post‑mortem            | Rapport : mettre en place un suivi proactif des licences dans GLPI.         |

---

## Notes
- Les scénarios sont fictifs et destinés à la démonstration.
- Chaque incident est documenté pour être compatible avec GLPI et audit‑ready.
- Les recommandations post‑mortem permettent d’améliorer la continuité de service.
