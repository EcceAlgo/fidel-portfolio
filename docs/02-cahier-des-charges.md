# Cahier des charges du projet

| Élément | Valeur |
|---------|--------|
| Projet | Fidel Portfolio |
| Document | Cahier des charges |
| Version | 1.0 |
| Auteur | Fidel Nziengui Ateba |
| Statut | En cours de rédaction |
| Dernière mise à jour | 04/07/2026 |

---

← [Analyse des besoins](01a-analyse-des-besoins.md) | [Spécifications fonctionnelles →](03-specifications-fonctionnelles.md)

## Sommaire

1. [Introduction](#1-introduction)
2. [Présentation du projet](#2-présentation-du-projet)
3. [Contexte](#3-contexte)
4. [Objectifs](#4-objectifs)
5. [Périmètre du projet](#5-périmètre-du-projet)
6. [Parties prenantes](#6-parties-prenantes)
7. [Exigences fonctionnelles](#7-exigences-fonctionnelles)
8. [Exigences non fonctionnelles](#8-exigences-non-fonctionnelles)
9. [Livrables](#9-livrables)
10. [Planning prévisionnel](#10-planning-prévisionnel)
11. [Critères d'acceptation](#11-critères-dacceptation)
12. [Risques](#12-risques)
13. [Documents liés](#13-documents-liés)

---

## 1. Introduction

Le présent cahier des charges définit les exigences fonctionnelles et non fonctionnelles du projet **Fidel Portfolio**.

Il traduit les besoins identifiés lors de la phase d'analyse en un ensemble d'exigences précises qui serviront de référence tout au long de la conception, du développement, des tests et du déploiement de l'application.

Ce document précise également le périmètre du projet, les objectifs, les parties prenantes, les livrables attendus ainsi que les contraintes et les critères d'acceptation de la première version du portfolio.

Il constitue le document de référence permettant de s'assurer que la solution développée répond aux besoins exprimés tout en respectant les objectifs fixés.

---

## 2. Présentation du projet

**Fidel Portfolio** est une application web de type portfolio professionnel destinée à présenter mon profil, mes compétences, mes réalisations et ma démarche d’ingénierie logicielle.

Le projet vise à fournir un support de présentation clair, accessible et structuré pour les recruteurs, responsables techniques et clients potentiels.

Ce cahier des charges encadre la première version du projet, en définissant son périmètre, ses exigences fonctionnelles, ses exigences non fonctionnelles, ses livrables et ses critères d’acceptation.

---

## 3. Contexte

Le projet **Fidel Portfolio** s'inscrit dans une démarche de développement d'un portfolio technique destiné à valoriser un profil de développeur Full Stack orienté DevOps et DevSecOps.

Dans un contexte où les recruteurs et les responsables techniques recherchent des preuves concrètes des compétences d'un candidat, le projet a pour objectif de proposer une application permettant de présenter non seulement les réalisations effectuées, mais également la démarche de conception, les choix d'architecture, les pratiques de sécurité et les méthodes de développement mises en œuvre.

Le projet est développé dans un cadre personnel avec une approche professionnelle. Il constitue à la fois un support de présentation auprès des recruteurs et un terrain d'expérimentation permettant d'appliquer les bonnes pratiques d'ingénierie logicielle, de qualité logicielle et de DevSecOps.

Le présent cahier des charges définit le périmètre de la première version de l'application ainsi que les exigences auxquelles elle devra répondre afin de satisfaire les besoins identifiés lors de la phase d'analyse.

---

## 4. Objectifs

Cette section présente les principaux objectifs que devra atteindre la première version du projet **Fidel Portfolio**. Ils sont regroupés selon leur nature : métier, fonctionnelle et technique.

### 4.1 Objectifs métier

La première version de l'application devra permettre de :

- valoriser le profil professionnel du développeur ;
- mettre en avant les réalisations et les compétences techniques ;
- renforcer la crédibilité du développeur auprès des recruteurs et des clients potentiels ;
- faciliter la prise de contact dans le cadre d'un recrutement ou d'une collaboration.

### 4.2 Objectifs fonctionnels

La première version de l'application devra permettre aux visiteurs de :

- consulter le profil du développeur ;
- consulter les projets réalisés ;
- accéder au détail de chaque projet ;
- identifier rapidement les compétences techniques mobilisées ;
- accéder aux liens vers GitHub et LinkedIn ;
- contacter facilement le développeur.

### 4.3 Objectifs techniques

Le projet devra permettre de :

- démontrer une démarche d'ingénierie logicielle complète ;
- produire une architecture claire, maintenable et évolutive ;
- appliquer les bonnes pratiques de développement et de sécurité ;
- documenter l'ensemble du projet ;
- préparer l'intégration d'une chaîne CI/CD et d'un déploiement automatisé ;
- faciliter les évolutions futures de l'application.

---

## 5. Périmètre du projet

Cette section définit les fonctionnalités couvertes par la première version de **Fidel Portfolio** ainsi que celles qui ne sont pas incluses dans son périmètre.

### 5.1 Fonctionnalités incluses

La première version de l'application comprendra notamment les fonctionnalités suivantes :

- présentation du profil professionnel du développeur ;
- consultation des compétences techniques ;
- consultation de la liste des projets réalisés ;
- consultation du détail d'un projet ;
- accès aux liens vers GitHub et LinkedIn ;
- prise de contact via un lien de type *mailto* ;
- consultation du site sur ordinateur, tablette et smartphone (responsive design).

### 5.2 Fonctionnalités exclues

Les fonctionnalités suivantes ne font pas partie du périmètre de la première version :

- authentification des visiteurs ;
- espace d'administration ;
- système de gestion dynamique des projets ;
- commentaires publics sur les projets ;
- messagerie interne ;
- forum de discussion ;
- système de notation ou d'avis ;
- formulaire de contact avec stockage des messages ;
- gestion multilingue du site ;
- tableau de bord de supervision (Grafana, Prometheus, etc.).

---

## 6. Parties prenantes

Le projet **Fidel Portfolio** implique plusieurs parties prenantes intervenant à différents niveaux du cycle de vie de l'application.

| Partie prenante | Rôle |
|-----------------|------|
| Porteur du projet | Analyse le besoin, conçoit, développe, teste, déploie et maintient l'application. |
| Recruteur | Consulte le portfolio afin d'évaluer les compétences et les réalisations du développeur. |
| Responsable technique | Analyse la qualité technique du projet, l'architecture et les choix d'ingénierie. |
| Client potentiel | Évalue les réalisations avant une éventuelle collaboration professionnelle. |
| Visiteur | Consulte le portfolio afin de découvrir le profil et les projets présentés. |

---

## 7. Exigences fonctionnelles

Les exigences fonctionnelles décrivent les fonctionnalités que devra offrir la première version de l'application.

| ID | Exigence |
|----|----------|
| EF-001 | Le système doit permettre au visiteur de consulter la page d'accueil du portfolio. |
| EF-002 | Le système doit permettre au visiteur de consulter le profil professionnel du développeur. |
| EF-003 | Le système doit permettre au visiteur de consulter les compétences techniques du développeur. |
| EF-004 | Le système doit permettre au visiteur de consulter la liste des projets réalisés. |
| EF-005 | Le système doit permettre au visiteur de consulter la fiche détaillée d'un projet. |
| EF-006 | Le système doit afficher les technologies utilisées pour chaque projet. |
| EF-007 | Le système doit permettre d'accéder au dépôt GitHub associé lorsqu'il est public. |
| EF-008 | Le système doit permettre d'accéder au profil LinkedIn du développeur. |
| EF-009 | Le système doit permettre au visiteur de contacter le développeur via un lien de type *mailto*. |
| EF-010 | Le système doit permettre la consultation du portfolio depuis un ordinateur, une tablette et un smartphone. |

---

## 8. Exigences non fonctionnelles

Les exigences non fonctionnelles définissent les caractéristiques de qualité que devra respecter l'application.

| ID | Exigence |
|----|----------|
| ENF-001 | L'application doit proposer une interface claire, ergonomique et intuitive. |
| ENF-002 | L'application doit être compatible avec les principaux navigateurs web modernes. |
| ENF-003 | L'application doit être responsive et s'adapter aux différentes tailles d'écran. |
| ENF-004 | Les pages principales doivent se charger rapidement dans des conditions normales d'utilisation. |
| ENF-005 | Le code source doit être structuré, lisible et maintenable. |
| ENF-006 | L'architecture du projet doit faciliter les évolutions futures. |
| ENF-007 | Les bonnes pratiques de sécurité applicative doivent être respectées. |
| ENF-008 | Aucune donnée sensible (clés API, mots de passe, secrets, variables d'environnement) ne doit être exposée dans le dépôt Git. |
| ENF-009 | Le projet doit être entièrement documenté afin de faciliter sa compréhension, sa maintenance et son évolution. |
| ENF-010 | Le projet doit pouvoir être déployé de manière reproductible. |
| ENF-011 | Les principales fonctionnalités doivent être testées avant leur mise en production. |
| ENF-012 | L'application doit être conçue de manière à pouvoir intégrer ultérieurement une chaîne CI/CD complète et des outils de supervision. |

---

## 9. Livrables

À l'issue du projet, les livrables suivants devront être disponibles.

| Livrable | Description |
|----------|-------------|
| Code source | Dépôt GitHub contenant l'ensemble du code source de l'application. |
| Application web | Portfolio déployé et accessible publiquement. |
| Documentation projet | Ensemble des documents de conception, d'analyse et de spécification. |
| Documentation technique | Documentation relative à l'architecture, à la sécurité, aux tests et au déploiement. |
| Pipeline CI/CD | Pipeline d'intégration et de déploiement automatisé (selon l'avancement du projet). |
| Décisions d'architecture | Historique des principales décisions techniques prises durant le projet (ADR). |

---

## 10. Planning prévisionnel

Le développement du projet **Fidel Portfolio** est organisé en plusieurs phases successives couvrant l'ensemble de son cycle de vie.

### 10.1 Cadrage

- Définition de la vision du projet
- Analyse des besoins
- Rédaction du cahier des charges

### 10.2 Conception

- Rédaction des spécifications fonctionnelles
- Rédaction des spécifications techniques
- Définition de l'architecture
- Élaboration des décisions d'architecture (ADR)

### 10.3 Développement

- Développement des fonctionnalités prévues dans le périmètre de la V1
- Mise en œuvre des bonnes pratiques de développement
- Documentation du code

### 10.4 Tests

- Vérification des fonctionnalités
- Correction des anomalies
- Validation des exigences

### 10.5 Déploiement

- Préparation de l'environnement
- Déploiement de l'application
- Vérification du bon fonctionnement en production

### 10.6 Maintenance et évolutions

- Correction des anomalies
- Amélioration des fonctionnalités
- Ajout de nouvelles fonctionnalités dans les versions futures
- Mise à jour de la documentation

---

## 11. Critères d'acceptation

La première version de **Fidel Portfolio** sera considérée comme conforme au présent cahier des charges si les critères suivants sont respectés.

| ID | Critère d'acceptation |
|----|-----------------------|
| CA-001 | Toutes les exigences fonctionnelles définies dans ce document sont implémentées. |
| CA-002 | Les principales exigences non fonctionnelles sont respectées. |
| CA-003 | L'application est accessible publiquement et consultable depuis un navigateur web moderne. |
| CA-004 | Le portfolio est utilisable sur ordinateur, tablette et smartphone. |
| CA-005 | Les liens vers GitHub, LinkedIn et le contact fonctionnent correctement. |
| CA-006 | La documentation du projet est complète et cohérente. |
| CA-007 | Les principaux scénarios de test sont validés avant la mise en production. |
| CA-008 | Le code source est versionné sur GitHub et respecte l'organisation définie pour le projet. |
| CA-009 | Le projet peut être déployé conformément à la procédure documentée. |

---

## 12. Risques

Les principaux risques identifiés pour la réalisation du projet sont présentés ci-dessous.

| ID | Risque | Impact | Probabilité | Mesure envisagée |
|----|---------|--------|-------------|------------------|
| R-001 | Dépassement du planning prévisionnel | Moyen | Moyenne | Prioriser le MVP et planifier les tâches. |
| R-002 | Difficultés techniques liées à certaines technologies | Moyen | Moyenne | Réaliser des phases de veille, de prototypage et documenter les solutions retenues. |
| R-003 | Budget limité pour l'hébergement | Faible | Élevée | Privilégier les offres gratuites ou à faible coût pour la première version. |
| R-004 | Régression lors de l'ajout de nouvelles fonctionnalités | Moyen | Moyenne | Effectuer des tests avant chaque mise en production. |
| R-005 | Exposition accidentelle de données sensibles | Élevé | Faible | Utiliser des variables d'environnement, ne jamais versionner les secrets et appliquer les bonnes pratiques de sécurité. |
| R-006 | Documentation incomplète ou obsolète | Moyen | Moyenne | Mettre à jour la documentation au fur et à mesure de l'avancement du projet. |
| R-007 | Complexification excessive de la première version | Moyen | Moyenne | Respecter strictement le périmètre défini pour le MVP. |

---

## 13. Documents liés

- [Glossaire](00-glossaire.md)
- [Vision du projet](01-vision-projet.md)
- [Analyse des besoins](01a-analyse-des-besoins.md)
- [Spécifications fonctionnelles](03-specifications-fonctionnelles.md)

---

**Document précédent :**
➡️ [Analyse des besoins](01a-analyse-des-besoins.md)

**Document suivant :**
➡️ [Spécifications fonctionnelles](03-specifications-fonctionnelles.md)