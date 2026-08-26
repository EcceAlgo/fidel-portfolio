# Analyse des besoins du projet

| Élément | Valeur |
|---------|--------|
| Projet | Fidel Portfolio |
| Document | Analyse des besoins |
| Version | 1.1 |
| Auteur | Fidel Nziengui Ateba |
| Statut | Validé |
| Dernière mise à jour | 26/08/2026 |

---

← [Vision du projet](01-vision-projet.md) | [Cahier des charges →](02-cahier-des-charges.md)

## Sommaire

1. [Introduction](#1-introduction)
2. [Parties prenantes](#2-parties-prenantes)
3. [Besoins métier](#3-besoins-métier)
4. [Besoins utilisateurs](#4-besoins-utilisateurs)
5. [Besoins techniques](#5-besoins-techniques)
6. [Synthèse des besoins](#6-synthèse-des-besoins)
7. [Priorisation](#7-priorisation)
8. [Traçabilité](#8-traçabilité)
9. [Documents liés](#9-documents-liés)


---

## 1. Introduction

Ce document formalise les besoins identifiés lors de la phase de cadrage du projet **Fidel Portfolio**.

Il constitue le lien entre la Vision du projet et le Cahier des charges en recensant les besoins métier, les besoins des utilisateurs ainsi que les besoins techniques qui devront être pris en compte lors de la conception de l'application.

Les besoins présentés dans ce document serviront de base à la rédaction des exigences fonctionnelles et non fonctionnelles du projet.

> **Évolution du périmètre — version 1.1 :** l'analyse intègre l'administration sécurisée et la persistance des projets dans la V1, conformément à l'affinement réalisé avant validation du cahier des charges. Les références de traçabilité ont également été alignées sur la numérotation consolidée des User Stories.

---

## 2. Parties prenantes

| Partie prenante | Catégorie | Rôle |
|-----------------|-----------|------|
| Porteur du projet | Interne | Conçoit, développe et maintient l'application. |
| Recruteur | Externe | Évalue les compétences et les réalisations du développeur. |
| Responsable technique | Externe | Analyse la qualité technique, l'architecture et les choix d'ingénierie. |
| Client potentiel | Externe | Évalue les réalisations avant une éventuelle collaboration. |
| Visiteur | Externe | Consulte le portfolio afin de découvrir le parcours et les projets. |
| Testeur | Interne | Vérifie le bon fonctionnement et la qualité de l'application. |
| Administrateur | Interne | Gère les projets publiés dans le portfolio via un espace d'administration sécurisé. |

Les besoins identifiés ont été regroupés en trois catégories :

- Les **besoins métier**, qui répondent aux objectifs du projet.
- Les **besoins utilisateurs**, qui expriment les attentes des visiteurs et de l'administrateur du portfolio.
- Les **besoins techniques**, qui garantissent la qualité, la maintenabilité et la pérennité de la solution.

---

## 3. Besoins métier

| ID | Besoin | Justification | Priorité |
|----|---------|---------------|----------|
| BM-001 | Valoriser le profil professionnel du développeur. | Faciliter le recrutement. | Haute |
| BM-002 | Mettre en avant les réalisations du développeur. | Démontrer concrètement les compétences. | Haute |
| BM-003 | Renforcer la crédibilité du développeur. | Rassurer les recruteurs et les clients potentiels. | Moyenne |
| BM-004 | Démontrer la capacité à conduire un projet de bout en bout. | Montrer la maîtrise de l'ensemble du cycle de vie d'une application, depuis l'analyse jusqu'au déploiement et à la maintenance. | Haute |

---

## 4. Besoins utilisateurs

| ID | Besoin | Justification | Priorité |
|----|---------|---------------|----------|
| BU-001 | Consulter le profil du développeur. | Comprendre rapidement son parcours. | Haute |
| BU-002 | Consulter les projets réalisés. | Évaluer les compétences à partir de réalisations concrètes. | Haute |
| BU-003 | Identifier les compétences techniques. | Vérifier l'adéquation avec le poste ou la mission. | Haute |
| BU-004 | Comprendre la démarche d'ingénierie mise en œuvre. | Évaluer la méthode de travail et la rigueur. | Haute |
| BU-005 | Contacter facilement le développeur. | Faciliter la prise de contact. | Haute |
| BU-006 | Accéder rapidement aux informations essentielles. | Réduire le temps nécessaire à l'évaluation du profil. | Haute |
| BU-007 | Gérer les projets depuis un espace d'administration sécurisé. | Permettre au propriétaire du portfolio d'ajouter, modifier et supprimer les projets sans modifier directement le code source. | Haute |

---

## 5. Besoins techniques

| ID | Besoin | Justification | Priorité |
|----|---------|---------------|----------|
| BT-001 | Offrir une navigation fluide et intuitive. | Améliorer l'expérience utilisateur. | Haute |
| BT-002 | Garantir une bonne maintenabilité. | Faciliter les évolutions futures. | Haute |
| BT-003 | Assurer la sécurité des données sensibles. | Respecter les bonnes pratiques de sécurité. | Haute |
| BT-004 | Faciliter le déploiement de l'application. | Simplifier la mise en production. | Haute |
| BT-005 | Produire une documentation complète et cohérente. | Faciliter la compréhension, la maintenance et la transmission du projet. | Haute |
| BT-006 | Permettre des évolutions futures sans remise en cause de l'architecture. | Garantir la pérennité et l'évolutivité de la solution. | Moyenne |
| BT-007 | Assurer la persistance et l'intégrité des données des projets. | Garantir la conservation, la cohérence et la disponibilité des projets gérés depuis l'administration. | Haute |
| BT-008 | Protéger l'accès aux fonctionnalités d'administration. | Empêcher tout accès ou toute modification non autorisée des projets. | Haute |

---

## 6. Synthèse des besoins

Cette section regroupe l'ensemble des besoins identifiés lors de l'analyse. Elle constitue une vue d'ensemble des besoins métier, utilisateurs et techniques qui serviront de référence pour la rédaction du cahier des charges.

| ID | Catégorie | Besoin | Priorité |
|----|-----------|---------|----------|
| BM-001 | Métier | Valoriser le profil professionnel du développeur. | Haute |
| BM-002 | Métier | Mettre en avant les réalisations du développeur. | Haute |
| BM-003 | Métier | Renforcer la crédibilité du développeur. | Moyenne |
| BM-004 | Métier | Démontrer la capacité à conduire un projet de bout en bout. | Haute |
| BU-001 | Utilisateur | Consulter le profil du développeur. | Haute |
| BU-002 | Utilisateur | Consulter les projets réalisés. | Haute |
| BU-003 | Utilisateur | Identifier les compétences techniques. | Haute |
| BU-004 | Utilisateur | Comprendre la démarche d'ingénierie mise en œuvre. | Haute |
| BU-005 | Utilisateur | Contacter facilement le développeur. | Haute |
| BU-006 | Utilisateur | Accéder rapidement aux informations essentielles. | Haute |
| BU-007 | Utilisateur | Gérer les projets depuis un espace d'administration sécurisé. | Haute |
| BT-001 | Technique | Offrir une navigation fluide et intuitive. | Haute |
| BT-002 | Technique | Garantir une bonne maintenabilité. | Haute |
| BT-003 | Technique | Assurer la sécurité des données sensibles. | Haute |
| BT-004 | Technique | Faciliter le déploiement de l'application. | Haute |
| BT-005 | Technique | Produire une documentation complète et cohérente. | Haute |
| BT-006 | Technique | Permettre des évolutions futures sans remise en cause de l'architecture. | Moyenne |
| BT-007 | Technique | Assurer la persistance et l'intégrité des données des projets. | Haute |
| BT-008 | Technique | Protéger l'accès aux fonctionnalités d'administration. | Haute |

---

## 7. Priorisation

### 7.1 Priorité haute

Les besoins de priorité haute sont indispensables à la réussite du projet. Ils devront être pris en compte dès la première version de l'application.

- Besoins métier (BM-001, BM-002 et BM-004)
- Besoins utilisateurs (BU-001 à BU-007)
- Besoins techniques (BT-001 à BT-005, BT-007 et BT-008)

### 7.2 Priorité moyenne

- BM-003 — Renforcer la crédibilité du développeur.
- BT-006 — Permettre des évolutions futures sans remise en cause de l'architecture.

### 7.3 Priorité faible

Aucun besoin de priorité faible n'a été identifié lors de cette phase d'analyse.

---

## 8. Traçabilité

Cette matrice permettra d'assurer le suivi de chaque besoin tout au long du projet, depuis son identification jusqu'à sa validation.

| Besoin | Exigence | User Story | Test | Statut |
|--------|----------|------------|------|--------|
| BM-001 | EF-002 | US-001 | À définir | En cours |
| BM-002 | EF-004, EF-005, EF-006, EF-007, EF-010, EF-011, EF-012, EF-021 | US-003, US-004, US-005, US-006, US-008, US-009, US-010 | À définir | En cours |
| BM-003 | EF-002, EF-003, EF-010 | US-001, US-003, US-004 | À définir | En cours |
| BM-004 | EF-005, EF-010, ENF-005, ENF-006 | US-004 | À définir | En cours |
| BU-001 | EF-002, EF-003 | US-001 | À définir | En cours |
| BU-002 | EF-004, EF-005, EF-006, EF-007, EF-010, EF-021 | US-002, US-003, US-004, US-008, US-009, US-010 | À définir | En cours |
| BU-003 | EF-003, EF-006 | US-001, US-003, US-004 | À définir | En cours |
| BU-004 | EF-010 | US-004 | À définir | En cours |
| BU-005 | EF-009 | US-012 | À définir | En cours |
| BU-006 | EF-001, EF-004, EF-011, EF-012, EF-013 | US-001, US-002, US-003, US-005, US-006, US-007, US-013, US-015 | À définir | En cours |
| BU-007 | EF-014, EF-015, EF-016, EF-017, EF-018, EF-019, EF-020 | US-016, US-017, US-018, US-019, US-020, US-021 | À définir | En cours |
| BT-001 | ENF-001, ENF-003, ENF-004, ENF-017 | US-015 | À définir | En cours |
| BT-002 | ENF-005 | À définir | À définir | En cours |
| BT-003 | ENF-007, ENF-008 | À définir | À définir | En cours |
| BT-004 | ENF-010, ENF-012 | À définir | À définir | En cours |
| BT-005 | ENF-009 | À définir | À définir | En cours |
| BT-006 | ENF-006 | À définir | À définir | En cours |
| BT-007 | EF-019, EF-020, ENF-015, ENF-016 | US-017, US-018, US-019, US-020 | À définir | En cours |
| BT-008 | EF-014, EF-015, ENF-013, ENF-014 | US-016, US-021 | À définir | En cours |

---

## 9. Documents liés

- [Glossaire](00-glossaire.md)
- [Vision du projet](01-vision-projet.md)
- [Cahier des charges](02-cahier-des-charges.md)

---

**Document précédent :**
➡️ [Vision du projet](01-vision-projet.md)

**Document suivant :**
➡️ [Cahier des charges](02-cahier-des-charges.md)
