---
matiere: support-services
type: projet
statut: en cours
date: 2026-09-08
tags: [horizon, reseau, adressage]
---

# Plan d'adressage · auto-école Horizon

Source des schémas réseau et d'infrastructure du livrable 2. Établi le 08/09/2026.

## Sous-réseaux

| Zone                | Réseau          | Masque          | Passerelle     | Interface                 |
| ------------------- | --------------- | --------------- | -------------- | ------------------------- |
| Postes agence 1     | 192.168.10.0/24 | 255.255.255.0   | 192.168.10.254 | R-Agence1 G0/0            |
| Serveurs            | 192.168.30.0/24 | 255.255.255.0   | 192.168.30.254 | R-Agence1 G0/1            |
| DMZ                 | 192.168.40.0/24 | 255.255.255.0   | 192.168.40.254 | R-Agence1 G0/2            |
| Postes agence 2     | 192.168.20.0/24 | 255.255.255.0   | 192.168.20.254 | R-Agence2 G0/0            |
| Liaison inter-sites | 10.0.0.0/30     | 255.255.255.252 | sans           | Se0/3/0 des deux routeurs |
| Accès Internet      | 203.0.113.0/30  | 255.255.255.252 | sans           | R-Agence1 Se0/3/1         |

## Équipements

| Hôte | Adresse | Rôle |
|---|---|---|
| R-Agence1 | 192.168.10.254, 192.168.30.254, 192.168.40.254, 10.0.0.1, 203.0.113.2 | Routeur du siège, sortie Internet |
| R-Agence2 | 192.168.20.254, 10.0.0.2 | Routeur de l'agence 2 |
| SW-Postes-A1 | sans | Commutateur des postes du siège |
| SW-Serveurs | sans | Commutateur des serveurs |
| SW-Postes-A2 | sans | Commutateur des postes de l'agence 2 |
| SRV-APP | 192.168.30.1 | Application métier et base de données |
| SRV-TICKETS | 192.168.30.2 | Gestion des demandes et incidents |
| SRV-SUPERVISION | 192.168.30.3 | Supervision des serveurs et du réseau |
| SRV-FICHIERS | 192.168.30.4 | Partage de documents et sauvegarde |
| SRV-WEB | 192.168.40.1 | Site vitrine, en DMZ |
| PC-Gerant | 192.168.10.1 | Poste du gérant |
| PC-RespPeda | 192.168.10.2 | Poste du responsable pédagogique |
| PC-Secretaire-A1 | 192.168.10.3 | Poste secrétariat agence 1 |
| PC-Secretaire-A2 | 192.168.20.1 | Poste secrétariat agence 2 |
| PC-Moniteurs-A2 | 192.168.20.2 | Poste partagé des moniteurs |

## Routage

- R-Agence1 : route statique `192.168.20.0/24` via `10.0.0.2`
- R-Agence2 : route par défaut `0.0.0.0/0` via `10.0.0.1`

## Choix à justifier à l'oral

- **Trois sous-réseaux au siège** : les postes, les serveurs et la DMZ sont séparés pour pouvoir filtrer les flux entre eux, comme l'exige la partie 6.5 du cahier des charges.
- **Site vitrine en DMZ** : c'est le seul service exposé sur Internet, il ne doit pas se trouver sur le même réseau que les données des élèves.
- **Liaison série entre les deux agences** : liaison dédiée fournie par un opérateur, avec le siège comme côté DCE.
- **Route par défaut à l'agence 2** : le siège est sa seule sortie, une seule route suffit au lieu de trois.
- **Adressage privé en /24** : très au-delà des 25 utilisateurs prévus en 6.1, pour absorber l'ouverture d'une troisième agence sans renumérotation.
- **203.0.113.0/24** est un préfixe réservé à la documentation (RFC 5737), il ne peut pas entrer en conflit avec une adresse réelle.

## Limite connue

Le nuage INTERNET symbolise l'accès opérateur. Packet Tracer ne fait pas monter ce lien sans configuration Frame Relay, il apparaît donc en rouge sur la topologie. Aucun flux vers Internet n'est simulé à ce stade.
