# Projet annuel · système d'information de l'auto-école Horizon

Projet fil rouge du module **XSIO306, Support et mise à disposition de services
informatiques**. BTS SIO option SISR, 2e année, EFREI.

Adam Cohen · groupe BTS2-SIO1 · année 2026-2027

Ce dépôt trace l'avancement du projet, mission par mission.

Planning : [GitHub Projects](https://github.com/users/LKAdammm/projects/1).

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

Les dossiers suivent le Monde 1 du parcours : Idéation, Conception et
planification, Maquettage.

### 01 · Cahier des charges

Cahier des charges simplifié en six parties, selon la méthode du cours, avec
priorisation MoSCoW des fonctionnalités (8 Must, 3 Should, 1 Could, 1 Won't),
besoins non fonctionnels vérifiables, méthode projet et grandes étapes.
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
| `02-conception-planification/schema-architecture.drawio` | schéma d'architecture : composants logiciels et flux, source draw.io |
| `02-conception-planification/schema-architecture.png` | le même, exporté |
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

### 03 · Maquettage

Fichier Figma : [Horizon · Maquettage](https://www.figma.com/design/rmD2VxxiW7KICzMycwAr11).

Démarche centrée utilisateur pour le site vitrine et l'application métier :
personas, benchmark, arborescence, parcours utilisateur, moodboard, charte
graphique, 9 wireframes, 9 maquettes graphiques et un prototype interactif.

Prototype : [site vitrine](https://www.figma.com/proto/rmD2VxxiW7KICzMycwAr11?node-id=15-40&starting-point-node-id=15%3A40),
[application métier](https://www.figma.com/proto/rmD2VxxiW7KICzMycwAr11?node-id=14-371&starting-point-node-id=14%3A371).

Reste à faire : le test du prototype par un autre étudiant.

---

## Suite prévue

| Monde | Contenu |
|---|---|
| 2 | Modèle de données et API REST, développement, tests, infrastructure d'hébergement |
| 3 | Premier oral blanc, projet professionnel et veille |
| 4 | Inventaire, habilitations, charte utilisateur, GLPI et ITIL, pannes simulées |
| 5 | Deuxième oral blanc, portfolio |
| 6 | Audit de sécurité, continuité et sauvegarde, mise en production, mesure d'audience, troisième oral blanc |
