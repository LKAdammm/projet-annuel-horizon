# Projet annuel · système d'information de l'auto-école Horizon

Projet fil rouge du module **XSIO306, Support et mise à disposition de services
informatiques**. BTS SIO option SISR, 2e année, EFREI.

Adam Cohen · groupe BTS2-SIO1 · année 2026-2027

Ce dépôt trace l'avancement du projet, livrable par livrable.

---

## Le contexte

Horizon est une auto-école fictive d'Île-de-France : deux agences, 14 salariés,
environ 300 élèves actifs par an, 7 véhicules. Elle fonctionne encore au papier
et au tableur, ce qui produit quatre difficultés récurrentes : dossiers élèves
perdus ou bloqués dans une seule agence, suivi de progression peu fiable,
doubles réservations de moniteurs et de véhicules, et environ 10 % d'absences
non prévenues.

Le projet consiste à concevoir et mettre en œuvre son système d'information.

---

## Les livrables

### 01 · Cahier des charges

Cahier des charges simplifié en six parties, selon la méthode du cours, avec
priorisation MoSCoW des fonctionnalités (8 Must, 3 Should, 1 Could, 1 Won't).
Les 18 contraintes obligatoires du sujet y sont traduites en besoins métier.

| Fichier | Contenu |
|---|---|
| `01-cahier-des-charges/cahier-des-charges.md` | le document source |
| `01-cahier-des-charges/cahier-des-charges.pdf` | la version rendue |

### 02 · Conception et planification

Architecture du système d'information, schéma réseau maquetté et testé,
planification du projet.

| Fichier | Contenu |
|---|---|
| `02-conception-planification/plan-adressage.md` | sous-réseaux, équipements, routage et justifications |
| `02-conception-planification/schema-infrastructure.drawio` | schéma d'infrastructure, source draw.io |
| `02-conception-planification/schema-infrastructure.png` | le même, exporté |
| `02-conception-planification/schema-reseau.pkt` | maquette Cisco Packet Tracer 9.0.1 |
| `02-conception-planification/captures/` | topologie et tests de connectivité |

L'architecture retenue : deux sites reliés par une liaison série opérateur, et
au siège trois réseaux séparés, les postes, les serveurs et une DMZ qui porte le
site vitrine.

| Zone | Réseau |
|---|---|
| Postes agence 1 | 192.168.10.0/24 |
| Serveurs | 192.168.30.0/24 |
| DMZ | 192.168.40.0/24 |
| Postes agence 2 | 192.168.20.0/24 |
| Liaison inter-sites | 10.0.0.0/30 |
| Accès Internet | 203.0.113.0/30 |

Connectivité validée dans les deux sens, captures à l'appui.

---

## Suite prévue

Application web reliée à une base de données et à un service externe, site
vitrine, gestion de tickets selon ITIL, sauvegarde avec test de restauration,
supervision, documentation.
