---
matiere: support-services
type: projet
statut: rendu
tags: [horizon, cahier-des-charges]
---

# Cahier des charges simplifié

## Mise en place du système d'information de l'auto-école Horizon

**Module XSIO306 : Support et mise à disposition de services informatiques**
Adam, BTS SIO option SISR, 2ᵉ année, EFREI
Version 1, septembre 2026

---

## 1. Contexte

Horizon est une auto-école implantée depuis une quinzaine d'années en Île-de-France. Elle propose plusieurs prestations :

- la formation au permis B (conduite traditionnelle et conduite accompagnée) ;
- la préparation à l'examen du code de la route ;
- des stages de récupération de points ;
- des heures de conduite complémentaires et des remises à niveau.

L'entreprise a ouvert une seconde agence il y a trois ans et compte aujourd'hui **14 salariés** répartis sur les deux sites :

| Fonction | Effectif |
|---|---|
| Gérant | 1 |
| Responsable pédagogique | 1 |
| Secrétaires d'agence | 2 |
| Enseignants de la conduite (moniteurs) | 9 |
| Assistant administratif | 1 |

L'auto-école suit environ 300 élèves actifs par an et dispose d'un parc de 7 véhicules.

### Fonctionnement actuel

L'organisation repose encore très largement sur le papier et sur des outils bureautiques non partagés :

- le **planning des leçons** est tenu sur un cahier grand format, un par agence, complété à la main par les secrétaires ;
- les **dossiers élèves** (pièces d'identité, attestations, formulaires d'inscription au permis) sont conservés dans des classeurs physiques, dans l'agence où l'élève s'est inscrit ;
- le **suivi de progression** de chaque élève est noté sur un livret papier que le moniteur remplit après la leçon ;
- les **coordonnées des élèves** sont saisies dans un fichier tableur, dupliqué sur les postes des deux secrétaires ;
- l'auto-école ne dispose d'**aucun site Internet** et communique uniquement par téléphone et par affichage en vitrine.

### Difficultés rencontrées

Ce fonctionnement génère quatre problèmes récurrents que la direction souhaite traiter :

1. **Dispersion et perte de dossiers.** Les dossiers élèves existent en un seul exemplaire papier et restent dans leur agence d'origine. Un élève reçu dans la seconde agence oblige à un déplacement ou à une reconstitution partielle du dossier. Plusieurs dossiers ont été égarés, avec des conséquences directes sur les délais d'inscription à l'examen.

2. **Suivi de progression peu fiable.** Le livret papier est parfois oublié, perdu ou incomplet. Lorsqu'un élève change de moniteur, le nouvel enseignant ne dispose pas d'une vision claire des compétences déjà acquises et doit refaire une évaluation.

3. **Erreurs de planning.** La tenue manuelle du planning provoque des doubles réservations, des créneaux attribués à un moniteur absent et des véhicules affectés simultanément à deux leçons. Chaque erreur se traduit par une heure de formation perdue et un élève mécontent.

4. **Absentéisme aux leçons.** Aucun rappel n'est adressé aux élèves. Le taux d'absence non prévenue est estimé à environ 10 % des créneaux, ce qui représente une perte directe de chiffre d'affaires et une immobilisation inutile des moniteurs et des véhicules.

La direction souhaite moderniser son organisation informatique afin de fiabiliser son activité, de faire communiquer ses deux agences et de gagner en visibilité auprès de sa clientèle.

---

## 2. Besoin / Problématique

Les informations de l'auto-école sont aujourd'hui dispersées entre des supports papier et des fichiers locaux, propres à chaque agence. Aucun système ne permet de partager une information à jour entre les deux sites, ni de garantir la conservation des dossiers.

Le besoin exprimé par la direction est de **disposer d'une information unique, fiable et accessible depuis les deux agences**, de **fiabiliser l'organisation des leçons** et de **réduire les absences**, tout en assurant la **protection et la disponibilité des données** des élèves.

> **Problématique :** comment mettre en place un système d'information permettant à l'auto-école Horizon de centraliser ses données, de fiabiliser l'organisation de ses formations entre ses deux agences et de sécuriser les informations de ses élèves ?

---

## 3. Objectif

Le projet a pour objectif de mettre en place un système d'information permettant à l'auto-école Horizon :

- de centraliser les dossiers et les informations des élèves sur un support unique ;
- de rendre ces informations accessibles depuis les deux agences ;
- de fiabiliser la gestion des plannings et des réservations de leçons ;
- d'assurer un suivi de progression pédagogique continu et partagé entre moniteurs ;
- de réduire l'absentéisme aux leçons ;
- de gérer le parc de véhicules et son affectation ;
- de faire connaître l'entreprise et ses prestations auprès du public ;
- de permettre aux salariés de signaler et de suivre leurs problèmes informatiques ;
- de protéger les données personnelles des élèves conformément à la réglementation ;
- d'assurer la disponibilité des services indispensables à l'activité quotidienne ;
- d'accompagner l'ouverture éventuelle d'une troisième agence.

---

## 4. Utilisateurs

Le système sera utilisé par les salariés des deux agences, ainsi que par les élèves et les visiteurs du site Internet.

| Utilisateur | Besoins principaux |
|---|---|
| **Gérant** | Suivre l'activité des deux agences, consulter les indicateurs, accéder à l'ensemble des informations |
| **Responsable pédagogique** | Organiser les plannings, affecter les moniteurs et les véhicules, suivre la progression des élèves |
| **Secrétaires d'agence** | Inscrire les élèves, constituer et consulter les dossiers, planifier et modifier les leçons, encaisser et suivre les règlements |
| **Enseignants de la conduite** | Consulter leur planning, renseigner la progression après chaque leçon, consulter le dossier de l'élève, signaler un problème sur un véhicule |
| **Assistant administratif** | Gérer les documents administratifs, préparer les dossiers d'inscription à l'examen, suivre les échéances |
| **Prestataire informatique** | Administrer et superviser le système d'information, gérer les comptes et les droits, traiter les demandes et les incidents |
| **Élèves** | Consulter leur planning et leur progression, recevoir les rappels de leçon |
| **Visiteurs du site** | Consulter les prestations et les tarifs, contacter l'auto-école |

---

## 5. Fonctionnalités

Les fonctionnalités attendues sont regroupées par domaine. Chacune est priorisée selon la méthode **MoSCoW** (*Must* : indispensable, *Should* : important, *Could* : optionnel, *Won't* : non prévu pour cette version).

Le critère de priorisation retenu est le suivant :

- sont classées en **Must** les fonctionnalités sans lesquelles l'auto-école ne peut pas assurer son activité quotidienne, ainsi que celles dont l'absence laisserait subsister les difficultés identifiées en partie 1 ;
- sont classées en **Should** les fonctionnalités qui apportent un gain d'organisation ou de pilotage réel, mais dont le report ne bloque pas le fonctionnement de l'entreprise ;
- sont classées en **Could** les améliorations de confort, mises en œuvre si le temps le permet ;
- sont classées en **Won't** les fonctionnalités volontairement exclues du périmètre de cette version.

### 5.1 Gestion des dossiers élèves (*Must*)

Le système devra permettre :

- de créer et de modifier la fiche d'un élève ;
- d'enregistrer les pièces justificatives sous forme numérique ;
- de consulter un dossier depuis l'une ou l'autre des deux agences ;
- de suivre l'état d'avancement administratif du dossier (inscription, examen du code, examen de conduite) ;
- de conserver l'historique des formations suivies ;
- de retrouver un élève par une recherche.

### 5.2 Gestion des plannings et des réservations (*Must*)

Le système devra permettre :

- de consulter le planning des leçons par agence, par moniteur ou par véhicule ;
- de réserver un créneau pour un élève ;
- d'affecter un moniteur et un véhicule à une leçon ;
- d'empêcher toute double réservation d'un moniteur ou d'un véhicule ;
- de modifier ou d'annuler une leçon ;
- d'enregistrer les absences et les annulations ;
- de gérer les indisponibilités des moniteurs (congés, formations).

### 5.3 Suivi de la progression pédagogique (*Must*)

Le système devra permettre :

- de renseigner les compétences travaillées à l'issue de chaque leçon ;
- de consulter le niveau atteint par un élève ;
- de conserver l'historique des évaluations ;
- de permettre à tout moniteur de reprendre le suivi d'un élève ;
- d'identifier les élèves prêts à se présenter à l'examen.

### 5.4 Rappels automatiques des leçons (*Must*)

Le système devra permettre :

- d'envoyer automatiquement à l'élève un rappel avant sa leçon ;
- de notifier l'élève en cas de modification ou d'annulation de son créneau ;
- de conserver la trace des rappels envoyés.

> Cette fonctionnalité s'appuiera sur un service de notification externe à l'entreprise.

### 5.5 Gestion des comptes et des droits d'accès (*Must*)

Le système devra permettre :

- de créer et de gérer les comptes des salariés ;
- d'authentifier les utilisateurs avant tout accès aux données ;
- d'organiser les utilisateurs par agence et par fonction ;
- d'attribuer des droits différents selon le profil ;
- de désactiver un compte lors d'un départ.

### 5.6 Stockage et partage des documents (*Should*)

Le système devra permettre :

- de stocker les documents de l'entreprise sur un espace commun ;
- de partager des documents entre les deux agences ;
- d'organiser les documents par nature et par agence ;
- de restreindre l'accès aux documents sensibles.

### 5.7 Support informatique (*Must*)

Le système devra permettre :

- à un salarié de signaler un problème informatique ou une demande ;
- de suivre l'état d'avancement de sa demande ;
- d'affecter la demande à un intervenant ;
- de distinguer une demande de service d'un incident ;
- d'ajouter des commentaires et des pièces jointes ;
- de conserver l'historique des demandes traitées.

### 5.8 Site Internet (*Must*)

L'auto-école devra disposer d'un site Internet accessible au public permettant :

- de présenter l'entreprise et ses deux agences ;
- de présenter les formations proposées ;
- de présenter les tarifs et les modalités d'inscription ;
- d'afficher les résultats et les taux de réussite ;
- de fournir les coordonnées et les horaires d'ouverture ;
- de permettre à un visiteur de demander un rendez-vous ou des informations.

### 5.9 Administration et supervision du système (*Must*)

Le prestataire informatique devra pouvoir :

- administrer les différents services ;
- surveiller la disponibilité des serveurs et des équipements réseau ;
- surveiller les ressources système ;
- être alerté en cas de dysfonctionnement ;
- consulter l'utilisation des services.

### 5.10 Gestion du parc de véhicules (*Should*)

Le système devra permettre :

- d'identifier chaque véhicule ;
- de connaître sa disponibilité ;
- d'enregistrer les entretiens et les contrôles techniques ;
- de signaler une anomalie constatée par un moniteur ;
- de consulter l'historique des interventions.

### 5.11 Suivi de l'activité (*Should*)

Le système devra permettre à la direction :

- de consulter le nombre d'heures réalisées par agence et par moniteur ;
- de suivre le taux d'absentéisme aux leçons ;
- de suivre le taux de réussite aux examens ;
- de consulter le nombre d'élèves inscrits et en cours de formation.

### 5.12 Espace élève en ligne (*Could*)

Le système pourrait permettre à un élève :

- de consulter ses prochaines leçons ;
- de consulter sa progression ;
- de consulter les documents de son dossier.

### 5.13 Fonctionnalités non retenues pour cette version (*Won't*)

Les fonctionnalités suivantes ne sont pas prévues dans le périmètre actuel du projet :

- le paiement en ligne des heures de conduite ;
- la réservation de leçons directement par l'élève, sans validation du secrétariat ;
- une application mobile dédiée aux moniteurs ;
- la gestion de la paie et de la comptabilité, qui reste confiée au cabinet comptable externe.

### Récapitulatif de la priorisation

| Priorité | Fonctionnalités |
|---|---|
| **Must** | Dossiers élèves · Plannings et réservations · Progression pédagogique · Rappels automatiques · Comptes et droits d'accès · Support informatique · Site Internet · Administration et supervision |
| **Should** | Stockage et partage de documents · Gestion du parc de véhicules · Suivi de l'activité |
| **Could** | Espace élève en ligne |
| **Won't** | Paiement en ligne · Réservation autonome par l'élève · Application mobile moniteurs · Paie et comptabilité |

---

## 6. Contraintes

### 6.1 Infrastructure

L'infrastructure devra être composée de plusieurs machines permettant d'héberger les différents services de l'entreprise. Elle devra :

- desservir les deux agences ;
- être dimensionnée pour les besoins actuels et pouvoir accueillir jusqu'à 25 utilisateurs ;
- reposer sur un réseau permettant la communication entre les services et entre les deux sites ;
- permettre l'ajout d'une troisième agence sans refonte complète ;
- être documentée.

### 6.2 Ressources numériques

L'ensemble des ressources numériques nécessaires au fonctionnement du système d'information devra être recensé, identifié et documenté : postes de travail, serveurs, équipements réseau, périphériques, licences et services utilisés.

### 6.3 Continuité de service

Les services indispensables à l'activité quotidienne devront disposer de mesures permettant leur maintien ou leur rétablissement en cas d'incident. Sont considérés comme critiques :

- l'accès au planning des leçons ;
- l'accès aux dossiers élèves.

L'indisponibilité de ces services interrompt directement l'activité de formation. Les mesures retenues et les procédures de reprise devront être documentées.

### 6.4 Sauvegarde et restauration

Une solution de sauvegarde devra être mise en place et couvrir les données des élèves, les plannings et les documents de l'entreprise. Un **test de restauration devra être réalisé et ses résultats documentés**. La stratégie de sauvegarde devra préciser la fréquence, le périmètre et le lieu de conservation des sauvegardes.

### 6.5 Sécurité et gestion des accès

Le système d'information devra intégrer des mesures permettant :

- de contrôler les accès aux ressources et aux services ;
- de gérer les droits selon le profil et l'agence de rattachement ;
- de sécuriser les comptes utilisateurs ;
- de protéger les serveurs et les équipements ;
- de filtrer les communications ;
- de sécuriser les services accessibles depuis Internet ;
- de limiter les accès administrateurs.

### 6.6 Règles d'utilisation

Des règles d'utilisation et de sécurité des ressources numériques devront être définies, formalisées et communiquées à l'ensemble des salariés.

### 6.7 Conformité réglementaire

L'auto-école traite des données personnelles d'élèves, dont une partie sont mineurs, ainsi que des pièces d'identité. Le système devra respecter le RGPD, notamment :

- la limitation de l'accès aux données aux personnes habilitées ;
- la définition d'une durée de conservation des dossiers ;
- l'information des élèves sur le traitement de leurs données.

### 6.8 Gestion des services

La gestion des demandes et des incidents devra s'appuyer sur les principes **ITIL**. Elle devra permettre de collecter, suivre, affecter et traiter :

- les demandes des utilisateurs ;
- les incidents système et réseau ;
- les incidents applicatifs.

### 6.9 Mesure et supervision

L'utilisation des services numériques devra faire l'objet d'une analyse à l'aide d'indicateurs adaptés, portant notamment sur la fréquentation du site Internet, la charge des services aux heures de pointe et la disponibilité des équipements.

### 6.10 Conduite du projet

- Les activités du projet devront être planifiées et suivies à l'aide d'un outil de gestion de projet.
- Des indicateurs devront permettre de mesurer l'avancement du projet et les résultats obtenus.
- Les services devront être testés et validés avant leur mise en production, et les résultats des tests documentés.
- La mise en production devra être préparée, réalisée et documentée.
- Les utilisateurs devront être accompagnés dans la prise en main des services par des supports, des procédures ou des formations adaptés.

### 6.11 Documentation

L'ensemble du système devra être documenté. La documentation devra présenter :

- l'architecture du système d'information et l'architecture réseau ;
- les équipements, serveurs et services ;
- les utilisateurs et leurs droits ;
- les mesures de sécurité ;
- la stratégie de sauvegarde ;
- les procédures d'administration et de reprise après incident.

### 6.12 Choix techniques

Aucune technologie n'est imposée. Les choix devront être justifiés au regard :

- des besoins de l'entreprise ;
- du budget disponible, limité pour une structure de cette taille ;
- de la sécurité ;
- de la facilité de maintenance, l'entreprise ne disposant pas de service informatique interne ;
- de l'évolutivité du système.

### 6.13 Budget et délais

Le budget est contraint par la taille de l'entreprise : les solutions open source ou déjà disponibles seront privilégiées lorsqu'elles répondent au besoin. Le projet devra être déployé sans interrompre l'activité de formation des deux agences.
