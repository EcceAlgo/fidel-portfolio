# Spécifications techniques

| Élément | Valeur |
|---------|--------|
| Projet | Fidel Portfolio |
| Document | Spécifications techniques |
| Version | 1.0 |
| Auteur | Fidel Nziengui Ateba |
| Statut | En cours de rédaction |
| Dernière mise à jour | 17/08/2026 |

---

← [Spécifications fonctionnelles](03-specifications-fonctionnelles.md) | [Architecture →](05-architecture.md)

## Sommaire

1. [Introduction](#1-introduction)
2. [Contraintes techniques](#2-contraintes-techniques)
3. [Environnement technique](#3-environnement-technique)
4. [Spécifications de l'application](#4-spécifications-de-lapplication)
5. [Gestion des données](#5-gestion-des-données)
6. [Sécurité technique](#6-sécurité-technique)
7. [Performance et compatibilité](#7-performance-et-compatibilité)
8. [Qualité du code](#8-qualité-du-code)
9. [Tests et validation technique](#9-tests-et-validation-technique)
10. [Intégration et déploiement](#10-intégration-et-déploiement)
11. [Observabilité et maintenance](#11-observabilité-et-maintenance)
12. [Traçabilité](#12-traçabilité)
13. [Documents liés](#13-documents-liés)

## 1. Introduction

### 1.1 Objet du document

Ce document définit les spécifications techniques du projet **Fidel Portfolio**.

Il traduit les exigences fonctionnelles et non fonctionnelles définies lors des phases de cadrage en contraintes et exigences techniques nécessaires à la conception, au développement, aux tests, au déploiement et à la maintenance de l'application.

Il précise notamment l'environnement technique du projet, les contraintes applicables à l'application, la gestion des données, les exigences de sécurité, de performance, de compatibilité et de qualité ainsi que les principes liés à l'intégration et au déploiement.

Les choix d'architecture détaillés et leur organisation seront décrits dans le document dédié à l'architecture.

### 1.2 Objectifs

Les spécifications techniques ont pour objectifs de :

- définir les exigences techniques auxquelles l'application devra répondre ;
- encadrer les choix technologiques et leur mise en œuvre ;
- garantir la cohérence entre les besoins fonctionnels et leur réalisation technique ;
- définir les contraintes de qualité, de sécurité, de performance et de compatibilité ;
- favoriser la maintenabilité et l'évolutivité de l'application ;
- servir de référence lors du développement, des tests et du déploiement ;
- assurer la traçabilité entre les exigences du cahier des charges et leur prise en compte technique.

### 1.3 Périmètre

Ce document couvre les spécifications techniques nécessaires à la réalisation de la **version 1 (V1)** de **Fidel Portfolio**.

Il porte notamment sur :

- l'environnement de développement et d'exécution ;
- les technologies et outils nécessaires à la réalisation de l'application ;
- les contraintes techniques liées à l'interface et aux fonctionnalités de la V1 ;
- la gestion et le stockage des données ;
- les exigences techniques de sécurité ;
- les exigences de performance et de compatibilité ;
- les règles relatives à la qualité et à l'organisation du code ;
- les mécanismes de validation technique et de tests ;
- les principes d'intégration, de déploiement et de maintenance.

Ce document ne détaille pas :

- les besoins et parcours utilisateurs, décrits dans les spécifications fonctionnelles ;
- l'organisation détaillée des composants, décrite dans la documentation d'architecture ;
- la stratégie de sécurisation complète, décrite dans la documentation de sécurité ;
- les scénarios et procédures de test détaillés, décrits dans la documentation de tests ;
- les procédures opérationnelles de mise en production, décrites dans la documentation de déploiement.

## 2. Contraintes techniques

Cette section définit les principales contraintes techniques à respecter pour la réalisation de la V1 de **Fidel Portfolio**.

Ces contraintes encadrent les choix technologiques et l'implémentation de l'application afin de garantir sa compatibilité avec les exigences définies dans le cahier des charges et les spécifications fonctionnelles.

### 2.1 Application web

**Fidel Portfolio** doit être réalisé sous la forme d'une application web accessible depuis un navigateur.

L'application doit :

- être accessible sans installation préalable sur l'appareil du visiteur ;
- être accessible publiquement après son déploiement ;
- permettre l'accès aux fonctionnalités publiques de la V1 sans authentification ;
- restreindre les fonctionnalités d'administration aux utilisateurs autorisés ;
- utiliser des technologies compatibles avec les navigateurs web modernes.

### 2.2 Compatibilité et responsive design

L'application doit être utilisable sur différentes tailles d'écran conformément aux exigences fonctionnelles de la V1.

L'interface doit notamment s'adapter :

- aux ordinateurs ;
- aux tablettes ;
- aux smartphones.

L'adaptation de l'interface ne doit pas entraîner la perte d'une fonctionnalité essentielle.

Les navigateurs et versions faisant partie du périmètre de compatibilité seront précisés dans la section dédiée à la compatibilité.

### 2.3 Maintenabilité et évolutivité

La solution doit être conçue de manière à faciliter sa maintenance et ses évolutions futures.

Le code source doit notamment :

- être organisé de manière cohérente ;
- favoriser la séparation des responsabilités ;
- limiter les duplications inutiles ;
- permettre l'ajout ou la modification de fonctionnalités sans remise en cause globale de l'application ;
- respecter les conventions et règles de qualité définies pour le projet.

Les choix d'architecture permettant de répondre à ces contraintes seront détaillés dans la documentation d'architecture.

### 2.4 Gestion des données

Les données nécessaires au fonctionnement du portfolio doivent pouvoir être maintenues sans nécessiter de modification importante de la structure de l'application.

Cela concerne notamment :

- les informations relatives au profil ;
- les compétences ;
- les projets ;
- les catégories ;
- les technologies associées aux projets ;
- les liens vers les ressources externes.

Le mécanisme de stockage retenu devra être adapté aux besoins réels de la V1.

L'utilisation éventuelle d'une base de données devra être justifiée par les besoins fonctionnels et techniques du projet.

### 2.5 Sécurité

L'application et son processus de développement doivent respecter les bonnes pratiques de sécurité adaptées au périmètre de la V1.

En particulier :

- aucun secret ne doit être stocké directement dans le code source ;
- aucun mot de passe, jeton, clé API ou autre donnée sensible ne doit être versionné dans le dépôt Git ;
- les dépendances utilisées par le projet doivent pouvoir faire l'objet de contrôles de sécurité ;
- les ressources privées associées aux projets ne doivent pas être exposées publiquement ;
- les données provenant de sources externes ou saisies par un utilisateur doivent être traitées de manière appropriée avant leur utilisation.

La stratégie de sécurisation complète du projet sera détaillée dans la documentation dédiée à la sécurité.

### 2.6 Gestion du code source

Le code source et la documentation du projet doivent être versionnés avec Git et hébergés dans le dépôt GitHub du projet.

Le développement doit suivre le workflow de branches défini pour le projet :

`feature/*` / `docs/*` → `develop` → `main`

Les branches protégées ne doivent pas recevoir directement les modifications lorsqu'une Pull Request est imposée par les règles du dépôt.

Les modifications doivent être intégrées conformément aux règles de validation et de revue définies pour le projet.

### 2.7 Automatisation

Les opérations répétitives pouvant être automatisées doivent pouvoir être intégrées progressivement au cycle de développement.

Cela concerne notamment :

- les contrôles de qualité du code ;
- l'exécution des tests ;
- les contrôles de sécurité ;
- la construction de l'application ;
- le déploiement.

Les mécanismes précis d'intégration et de déploiement continus seront définis en fonction de l'environnement technique retenu.

### 2.8 Déploiement

L'application doit pouvoir être déployée de manière reproductible.

Le processus de déploiement doit limiter les opérations manuelles nécessaires à la mise en production et permettre, à terme, leur automatisation.

L'environnement d'hébergement devra être compatible avec les technologies retenues pour l'application et avec les contraintes budgétaires du projet.

### 2.9 Contraintes budgétaires

Le projet étant réalisé dans un cadre personnel, les coûts d'infrastructure et de services externes doivent être maîtrisés.

Pour la V1 :

- les solutions gratuites ou disposant d'un niveau gratuit adapté doivent être privilégiées lorsqu'elles répondent aux exigences du projet ;
- l'ajout d'un service payant doit être justifié par un besoin technique ou fonctionnel ;
- l'architecture ne doit pas introduire une infrastructure disproportionnée par rapport aux besoins du portfolio.

### 2.10 Portabilité

La solution doit limiter autant que possible sa dépendance à un environnement de développement local spécifique.

Le projet doit pouvoir être récupéré depuis le dépôt Git et exécuté dans un environnement compatible à partir d'une procédure documentée.

Les dépendances et prérequis nécessaires à son exécution doivent être explicitement déclarés et documentés.

## 3. Environnement technique

Cette section définit l'environnement technique utilisé pour développer, versionner, exécuter et maintenir la V1 de **Fidel Portfolio**.

Les technologies retenues doivent répondre aux besoins fonctionnels du projet tout en respectant les contraintes de maintenabilité, de sécurité, de coût et d'évolutivité définies précédemment.

### 3.1 Environnement de développement

Le développement de l'application est réalisé dans un environnement local avant l'intégration des modifications dans le dépôt distant.

L'environnement de développement doit permettre :

- l'exécution locale de l'application ;
- la gestion des dépendances ;
- l'exécution des outils de qualité et de validation ;
- l'exécution des tests ;
- l'utilisation de Git ;
- la reproduction de l'environnement à partir des fichiers de configuration versionnés.

Les versions des principaux outils nécessaires au projet doivent être définies ou documentées afin de limiter les différences de comportement entre les environnements.

### 3.2 Gestion du code source

Git est utilisé comme système de gestion de versions.

GitHub est utilisé pour l'hébergement du dépôt distant et la gestion du cycle d'intégration des modifications.

Le workflow principal repose sur les branches suivantes :

- `main` : branche contenant la version stable du projet ;
- `develop` : branche d'intégration des développements ;
- `feature/*` : branches dédiées au développement de fonctionnalités ;
- `docs/*` : branches dédiées aux évolutions de la documentation ;
- `fix/*` : branches pouvant être utilisées pour les corrections.

Les modifications sont intégrées dans les branches protégées par l'intermédiaire de Pull Requests conformément aux règles configurées sur le dépôt.

### 3.3 Interface utilisateur

La V1 nécessite une interface web permettant notamment :

- l'affichage du profil ;
- l'affichage dynamique des projets ;
- la recherche et le filtrage ;
- la navigation vers les pages détaillées ;
- la gestion du thème clair et sombre ;
- la mémorisation de certaines préférences d'affichage ;
- l'adaptation de l'interface aux différentes tailles d'écran ;
- la gestion d'animations et de transitions ;
- l'accès aux fonctionnalités d'administration prévues pour la V1.

La solution retenue devra permettre de construire ces interfaces tout en garantissant leur maintenabilité, leur accessibilité et leur évolutivité.

La technologie utilisée pour réaliser l'interface ainsi que son intégration dans l'architecture globale seront déterminées après étude des solutions adaptées au projet.

### 3.4 Traitements applicatifs

La V1 nécessite des traitements applicatifs permettant notamment :

- l'authentification de l'administrateur ;
- le contrôle des autorisations ;
- la consultation des projets ;
- la création de projets ;
- la modification de projets ;
- la suppression de projets ;
- la validation des données ;
- l'accès aux données persistantes ;
- la mise à disposition des données nécessaires à la partie publique du portfolio.

Les fonctionnalités publiques et les fonctionnalités protégées d'administration doivent être distinguées afin d'appliquer les contrôles d'accès appropriés.

La manière dont ces traitements seront organisés, exécutés et répartis entre les différents composants de la solution dépendra de l'architecture retenue.

Aucune architecture applicative particulière n'est imposée à ce stade.

### 3.5 Persistance des données

La V1 nécessite un mécanisme de persistance permettant de conserver durablement les données nécessaires au fonctionnement du portfolio.

Les données concernées comprennent notamment :

- les informations relatives aux projets ;
- les catégories ;
- les technologies associées ;
- les mots-clés ;
- les ressources et liens associés aux projets ;
- les données nécessaires au fonctionnement des fonctionnalités d'administration.

Le mécanisme de persistance retenu devra permettre :

- la création des données ;
- leur consultation ;
- leur modification ;
- leur suppression ;
- le maintien de leur cohérence ;
- leur conservation entre les sessions ;
- leur exploitation par les fonctionnalités publiques et administratives de l'application.

Le modèle de données sera défini lors de la phase de conception.

Le type de stockage, son organisation et les technologies associées seront sélectionnés après analyse du modèle de données, des contraintes techniques et de l'architecture retenue.

### 3.6 Gestion des dépendances

Les dépendances nécessaires au fonctionnement et au développement de l'application doivent être déclarées explicitement par le projet.

Le gestionnaire de dépendances retenu doit permettre :

- l'installation reproductible des dépendances ;
- le verrouillage des versions lorsque cela est nécessaire ;
- l'identification des dépendances directes et transitives ;
- l'analyse des vulnérabilités connues ;
- la mise à jour contrôlée des dépendances.

Les fichiers nécessaires à la reproduction de l'environnement doivent être versionnés dans le dépôt.

### 3.7 Conteneurisation

La conteneurisation pourra être utilisée si elle apporte une valeur réelle au développement, aux tests, à la reproductibilité des environnements ou au déploiement.

L'utilisation de conteneurs ne constitue pas une exigence fonctionnelle de la V1.

Si une technologie de conteneurisation est retenue, son utilisation devra notamment permettre :

- de reproduire l'environnement d'exécution ;
- de limiter les différences entre les environnements ;
- de faciliter l'exécution, les tests et éventuellement le déploiement de l'application.

La pertinence de la conteneurisation sera évaluée en fonction de l'architecture, des technologies et du mode de déploiement finalement retenus.

### 3.8 Intégration continue

GitHub Actions pourra être utilisé pour automatiser les contrôles réalisés lors de l'intégration des modifications.

Le pipeline d'intégration continue devra pouvoir intégrer progressivement :

- l'installation des dépendances ;
- les contrôles de formatage ;
- l'analyse statique du code ;
- l'exécution des tests ;
- la construction de l'application ;
- les contrôles de sécurité pertinents.

Les contrôles obligatoires avant fusion seront définis en fonction de la maturité du projet et pourront être associés aux règles de protection des branches.

### 3.9 Environnements d'exécution

Le projet distingue au minimum :

- l'environnement local de développement ;
- l'environnement de production.

Un environnement intermédiaire de préproduction pourra être introduit ultérieurement si les besoins du projet le justifient.

Les différences entre les environnements doivent être limitées et documentées.

Les paramètres spécifiques à un environnement ne doivent pas être codés en dur lorsqu'ils contiennent des informations sensibles ou sont susceptibles de varier.

### 3.10 Hébergement

La solution d'hébergement devra être sélectionnée en fonction de l'architecture finalement retenue.

Elle devra notamment être compatible avec :

- la technologie utilisée par l'application ;
- le mode de construction et de déploiement ;
- les besoins de disponibilité de la V1 ;
- l'utilisation d'un accès HTTPS ;
- l'automatisation du déploiement ;
- les contraintes budgétaires du projet.

Le choix du fournisseur et du service d'hébergement sera documenté lorsqu'il aura été arrêté.

### 3.11 Synthèse de l'environnement technique

| Élément | Solution / statut |
|---------|-------------------|
| Gestion de versions | Git |
| Hébergement du dépôt | GitHub |
| Workflow Git | `feature/*` / `docs/*` / `fix/*` → `develop` → `main` |
| Interface utilisateur | Nécessaire — technologie et organisation à déterminer |
| Traitements applicatifs | Nécessaires — organisation et technologies à déterminer |
| Persistance des données | Nécessaire — mécanisme et technologie à déterminer |
| Architecture applicative | À étudier et à sélectionner |
| Gestionnaire de dépendances | À déterminer selon les technologies retenues |
| Conteneurisation | À évaluer |
| CI | GitHub Actions envisagé |
| Hébergement | À sélectionner |
| Environnement local | Développement |
| Environnement distant | Production |

### 3.12 Critères de sélection technologique

Les technologies retenues pour la V1 de **Fidel Portfolio** doivent être sélectionnées en fonction des besoins fonctionnels, des contraintes techniques et des objectifs de maintenabilité, de sécurité, de performance et de déploiement du projet.

Les principaux critères de sélection sont les suivants :

- compatibilité avec les fonctionnalités définies pour la V1 ;
- capacité à fournir une interface web responsive et maintenable ;
- capacité à mettre en œuvre les traitements applicatifs nécessaires ;
- capacité à sécuriser les fonctionnalités d'administration ;
- capacité à assurer la persistance et la cohérence des données ;
- facilité de mise en œuvre de la gestion des projets ;
- qualité de l'écosystème et de la documentation ;
- facilité de test et d'automatisation ;
- compatibilité avec les outils CI/CD ;
- possibilité d'effectuer des contrôles de sécurité sur les dépendances et le code ;
- facilité de déploiement ;
- compatibilité avec les contraintes budgétaires du projet ;
- maintenabilité et évolutivité de la solution ;
- adéquation avec le délai prévu pour la réalisation de la V1.

Les technologies ne doivent pas être retenues uniquement en fonction de leur popularité ou de leur maîtrise préalable.

Le choix des technologies devra également tenir compte de l'architecture applicative retenue.

Les choix structurants devront être justifiés et, lorsque cela est pertinent, consignés dans les décisions d'architecture du projet.

---

## 4. Spécifications de l'application

Cette section définit les capacités techniques nécessaires au fonctionnement de la V1 de **Fidel Portfolio** sans imposer à ce stade une architecture applicative particulière.

Ces capacités constituent les exigences auxquelles devra répondre la solution retenue.

La répartition de ces responsabilités entre les différents composants sera définie dans la documentation d'architecture après étude et comparaison des solutions envisageables.

### 4.1 Capacités techniques attendues

La solution retenue devra permettre :

- de fournir une interface publique accessible depuis un navigateur ;
- de fournir un espace d'administration protégé ;
- d'authentifier l'administrateur ;
- de contrôler les autorisations d'accès ;
- de consulter les projets ;
- de créer, modifier et supprimer les projets ;
- de conserver les données de manière persistante ;
- de rechercher et filtrer les projets ;
- de valider les données avant leur traitement ou leur enregistrement ;
- de mettre à disposition les données nécessaires aux fonctionnalités publiques ;
- de gérer les erreurs de manière appropriée ;
- de protéger les opérations réservées à l'administration ;
- de permettre les tests automatisés ;
- de permettre l'intégration dans une chaîne CI/CD ;
- de permettre un déploiement reproductible.

### 4.2 Organisation des responsabilités

La solution devra assurer une séparation suffisamment claire des différentes responsabilités fonctionnelles et techniques afin de favoriser :

- la maintenabilité ;
- la testabilité ;
- la sécurité ;
- l'évolutivité ;
- la compréhension du code ;
- la limitation du couplage entre les différentes responsabilités.

La manière dont ces responsabilités seront regroupées ou réparties n'est pas imposée par les présentes spécifications.

Elle dépendra de l'architecture retenue après analyse des besoins et contraintes du projet.

### 4.3 Accès public et administration

La solution devra distinguer les fonctionnalités accessibles publiquement des fonctionnalités réservées à l'administration.

Les opérations publiques doivent permettre notamment la consultation et la recherche des projets sans authentification.

Les opérations permettant de créer, modifier ou supprimer des données doivent être protégées et accessibles uniquement à un administrateur authentifié et autorisé.

La solution doit empêcher qu'une opération réservée à l'administration puisse être exécutée uniquement en contournant l'interface utilisateur.

### 4.4 Gestion des données

La solution devra permettre aux fonctionnalités de l'application d'accéder aux données nécessaires à leur fonctionnement tout en préservant leur cohérence.

Elle devra notamment permettre :

- la consultation des projets ;
- la création de nouveaux projets ;
- la modification des projets existants ;
- la suppression des projets ;
- la gestion de leurs catégories, technologies et autres informations associées ;
- la conservation durable des modifications réalisées depuis l'administration.

L'organisation détaillée des données et leurs relations seront définies lors de la modélisation des données.

### 4.5 Communication entre les composants

Si l'architecture retenue nécessite des échanges entre plusieurs composants, services ou systèmes, leurs interfaces de communication devront être clairement définies.

Ces échanges devront notamment préciser :

- les responsabilités de chaque composant ;
- les données échangées ;
- les opérations disponibles ;
- les mécanismes de validation ;
- les règles d'authentification et d'autorisation lorsqu'elles sont nécessaires ;
- les comportements attendus en cas d'erreur.

Les protocoles, formats d'échange et mécanismes de communication dépendront de l'architecture et des technologies finalement retenues.

## 5. Gestion des données

Cette section définit les exigences techniques relatives aux données nécessaires au fonctionnement de la V1 de **Fidel Portfolio**.

Elle précise les données à gérer ainsi que les contraintes relatives à leur persistance, leur cohérence, leur validation et leur cycle de vie.

Le modèle de données détaillé, les relations entre les différentes entités et le mécanisme de stockage seront définis lors de la phase de conception.

### 5.1 Données relatives aux projets

Les projets constituent les principales données administrables de la V1.

Chaque projet doit disposer des informations nécessaires à sa présentation publique et à sa gestion depuis l'espace d'administration.

Les données associées à un projet peuvent notamment comprendre :

- un identifiant unique ;
- un titre ;
- un résumé ;
- une description ;
- un contexte ;
- un objectif ;
- une ou plusieurs catégories ;
- les technologies et outils utilisés ;
- des mots-clés ;
- la méthodologie suivie ;
- les principales étapes de réalisation ;
- les difficultés rencontrées ;
- les solutions apportées ;
- les résultats obtenus ;
- des ressources visuelles ;
- un lien éventuel vers une démonstration publique ;
- un lien éventuel vers un dépôt public ;
- une information indiquant qu'un dépôt ou un code source n'est pas public.

Les données obligatoires et facultatives devront être cohérentes avec les règles définies dans les spécifications fonctionnelles.

---

### 5.2 Données liées aux catégories et technologies

Un projet peut être associé à une ou plusieurs catégories ainsi qu'à plusieurs technologies ou outils.

La solution devra permettre de représenter ces associations sans introduire de duplication inutile des données.

Les catégories prévues pour la V1 comprennent notamment :

- Développement ;
- DevOps ;
- DevSecOps ;
- Cloud ;
- Autres.

L'organisation détaillée de ces données et de leurs relations avec les projets sera déterminée lors de la modélisation des données.

---

### 5.3 Données d'administration

La V1 nécessite les données permettant d'authentifier l'administrateur et de contrôler son accès aux fonctionnalités protégées.

Les informations d'authentification doivent être gérées de manière sécurisée.

En particulier :

- les mots de passe ne doivent jamais être stockés en clair ;
- les informations sensibles ne doivent pas être exposées dans le code source ou dans les interfaces publiques ;
- seules les données nécessaires au fonctionnement de l'authentification doivent être conservées.

Le mécanisme précis d'authentification et de gestion des informations associées sera défini lors de la conception de l'architecture et de la stratégie de sécurisation.

---

### 5.4 Persistance

Les données administrables doivent être conservées de manière persistante.

Une modification validée depuis l'espace d'administration doit rester disponible après :

- le rechargement de l'application ;
- la fermeture d'une session ;
- le redémarrage de l'application ;
- un nouveau déploiement, lorsque le mécanisme de déploiement utilisé implique le remplacement de l'instance applicative.

Le cycle de déploiement de l'application ne doit pas provoquer la perte des données persistantes.

Le mécanisme permettant d'assurer cette persistance sera déterminé en fonction de l'architecture et de la technologie de stockage retenues.

---

### 5.5 Validation des données

Les données reçues par l'application doivent être validées avant leur utilisation ou leur enregistrement.

La validation doit notamment permettre de vérifier :

- la présence des données obligatoires ;
- le respect du format attendu ;
- la validité des valeurs ;
- la cohérence entre les données associées ;
- la validité des liens lorsqu'un format particulier est attendu.

Une donnée invalide ne doit pas être enregistrée comme une donnée valide.

La validation ne doit pas reposer uniquement sur les contrôles réalisés dans l'interface utilisateur lorsqu'une opération peut être exécutée autrement.

---

### 5.6 Intégrité et cohérence des données

La solution doit préserver la cohérence des données pendant les opérations de création, de modification et de suppression.

Elle doit notamment éviter :

- la création de données dans un état incohérent ;
- les associations invalides entre les différentes données ;
- les références vers des données inexistantes ;
- les duplications non souhaitées lorsque celles-ci peuvent être évitées par le modèle retenu.

Les contraintes d'intégrité précises seront définies lors de la modélisation des données.

---

### 5.7 Suppression des données

La suppression d'un projet depuis l'administration doit entraîner son retrait des contenus accessibles publiquement.

La suppression doit également prendre en compte les données ou associations dépendantes du projet afin d'éviter la conservation de références devenues invalides.

Le comportement précis des données associées lors d'une suppression sera défini dans le modèle de données.

La stratégie de suppression retenue, notamment suppression définitive ou conservation logique, sera déterminée lors de la conception en fonction des besoins du projet.

---

### 5.8 Ressources visuelles

Les projets peuvent comporter des ressources visuelles telles que des captures d'écran, illustrations ou schémas.

La solution devra permettre d'associer ces ressources aux projets concernés.

Le mécanisme de stockage des fichiers ne doit pas être confondu avec le stockage des informations permettant de les référencer.

Le mode de stockage, d'accès et de gestion de ces ressources sera défini en fonction de l'architecture et de la solution d'hébergement retenues.

---

### 5.9 Sauvegarde et récupération

Les données nécessaires au fonctionnement du portfolio ne doivent pas dépendre uniquement d'une instance temporaire de l'application.

La solution retenue devra permettre de prévoir un mécanisme adapté de sauvegarde ou de récupération des données en cas de perte, de corruption ou d'erreur de manipulation.

Les modalités précises de sauvegarde, leur fréquence et leur éventuelle automatisation seront définies en fonction du mécanisme de persistance et de l'environnement d'hébergement retenus.

---

### 5.10 Évolution du modèle de données

Le modèle de données doit pouvoir évoluer avec les futures versions de l'application.

Les évolutions devront pouvoir être réalisées de manière contrôlée afin de limiter :

- la perte de données existantes ;
- les incompatibilités entre différentes versions de l'application ;
- les modifications manuelles difficiles à reproduire.

Si la technologie retenue utilise un mécanisme de migration de données ou de schéma, celui-ci devra pouvoir être versionné et intégré au processus de développement.

## 6. Sécurité technique

Cette section définit les principales exigences techniques de sécurité applicables à la V1 de **Fidel Portfolio**.

Elle ne remplace pas la stratégie de sécurisation détaillée du projet, qui sera décrite dans la documentation dédiée à la sécurité.

### 6.1 Authentification de l'administrateur

L'accès aux fonctionnalités d'administration doit être protégé par un mécanisme d'authentification.

Le mécanisme retenu devra notamment permettre :

- de vérifier l'identité de l'administrateur ;
- de refuser l'accès lorsque les informations fournies sont invalides ;
- de protéger les fonctionnalités réservées à l'administration ;
- de mettre fin à la session d'administration lors de la déconnexion.

Les informations d'authentification ne doivent pas être stockées en clair.

Le mécanisme technique retenu sera défini lors de la conception de l'architecture et de la stratégie de sécurisation.

---

### 6.2 Autorisation et contrôle d'accès

L'authentification seule ne doit pas suffire à garantir la sécurité des opérations d'administration.

La solution doit également vérifier que l'utilisateur authentifié est autorisé à exécuter les opérations protégées.

Les opérations de création, modification et suppression des projets doivent être accessibles uniquement à un administrateur autorisé.

Le contrôle d'accès ne doit pas reposer uniquement sur le masquage des fonctionnalités dans l'interface utilisateur.

Les contrôles nécessaires doivent être appliqués au niveau où les opérations protégées sont réellement exécutées.

---

### 6.3 Gestion des secrets

Aucun secret nécessaire au fonctionnement de l'application ne doit être stocké directement dans le code source.

Cela concerne notamment :

- les mots de passe ;
- les jetons d'accès ;
- les clés API ;
- les secrets cryptographiques ;
- les identifiants d'accès à des services externes ;
- les paramètres sensibles liés au stockage des données.

Les secrets ne doivent pas être versionnés dans le dépôt Git.

Le mécanisme de gestion des secrets devra être adapté aux environnements de développement, d'intégration et de production.

---

### 6.4 Protection des données d'authentification

Les données utilisées pour l'authentification doivent être protégées pendant leur stockage et leur transmission.

Les mots de passe ne doivent jamais être conservés sous leur forme originale.

Le mécanisme retenu devra utiliser des pratiques adaptées au stockage sécurisé des informations d'authentification.

Les échanges contenant des informations sensibles doivent être protégés contre leur interception lors des communications réseau.

---

### 6.5 Validation des entrées

Les données provenant des utilisateurs ou de sources externes doivent être considérées comme non fiables jusqu'à leur validation.

La solution doit notamment :

- vérifier le format des données reçues ;
- vérifier les valeurs attendues ;
- limiter les données acceptées aux besoins de l'application ;
- rejeter les données invalides ;
- empêcher qu'une donnée malformée puisse compromettre le fonctionnement de l'application ou l'intégrité des données.

La validation réalisée dans l'interface utilisateur ne doit pas constituer l'unique contrôle lorsque les données peuvent être reçues ou traitées par d'autres mécanismes.

---

### 6.6 Protection contre les injections

Les mécanismes utilisés pour accéder aux données ou exécuter des traitements ne doivent pas construire directement des commandes à partir de données non validées provenant des utilisateurs.

La solution retenue devra permettre de réduire les risques d'injection liés aux technologies utilisées.

Les mesures précises dépendront du mécanisme de persistance, des bibliothèques et de l'architecture finalement retenus.

---

### 6.7 Protection des contenus affichés

Les données affichées dans l'interface doivent être traitées de manière à limiter les risques liés à l'injection de contenu malveillant.

Les contenus saisis depuis l'administration ne doivent pas permettre l'exécution involontaire de code dans le navigateur des visiteurs.

Les mécanismes précis de protection seront adaptés à la technologie utilisée pour l'interface.

---

### 6.8 Communications réseau

Les communications de l'application en production doivent utiliser un canal sécurisé.

L'accès public à l'application devra être réalisé via HTTPS.

Les échanges entre composants de l'application devront également être protégés lorsqu'ils transitent sur un réseau non considéré comme sûr.

La configuration précise des communications dépendra de l'architecture retenue.

---

### 6.9 Dépendances

Les dépendances utilisées par le projet doivent pouvoir faire l'objet de contrôles réguliers.

Le projet devra permettre :

- l'identification des dépendances utilisées ;
- la détection de vulnérabilités connues ;
- la mise à jour contrôlée des dépendances ;
- le retrait des dépendances inutilisées lorsque cela est possible.

Les contrôles de dépendances pourront être intégrés au pipeline d'intégration continue.

---

### 6.10 Journalisation des événements de sécurité

Les événements techniques pertinents pour la sécurité doivent pouvoir être journalisés.

Cela peut notamment concerner :

- les échecs d'authentification ;
- les erreurs lors d'opérations protégées ;
- les actions d'administration importantes ;
- les erreurs applicatives susceptibles d'avoir un impact sur la sécurité.

Les journaux ne doivent pas contenir inutilement de secrets, mots de passe ou autres données sensibles.

Le niveau de journalisation et la conservation des événements seront définis en fonction de l'architecture et de l'environnement d'exécution retenus.

---

### 6.11 Principe du moindre privilège

Les composants, comptes techniques et utilisateurs doivent disposer uniquement des permissions nécessaires à leur fonctionnement.

Les permissions excessives doivent être évitées.

Ce principe devra notamment être pris en compte pour :

- l'administration de l'application ;
- l'accès aux données ;
- les outils CI/CD ;
- les environnements de déploiement ;
- les services externes éventuellement utilisés.

---

### 6.12 Sécurité du dépôt et du processus de développement

Le dépôt Git doit être configuré afin de réduire les risques de modification non contrôlée du code.

Les mécanismes utilisés pourront notamment comprendre :

- la protection des branches importantes ;
- l'utilisation de Pull Requests ;
- les contrôles automatisés avant fusion ;
- l'analyse du code ;
- l'analyse des dépendances ;
- la détection de secrets ;
- la restriction des droits d'accès au dépôt lorsque cela est nécessaire.

Les règles précises seront détaillées dans la stratégie de sécurisation du projet.

## 7. Performance et compatibilité

Cette section définit les exigences techniques relatives aux performances, à la compatibilité et à l'adaptation de l'application aux différents environnements d'utilisation.

Les outils et mécanismes permettant de mesurer et d'optimiser ces performances seront déterminés lors de la conception et de l'implémentation.

### 7.1 Performance de chargement

L'application doit offrir des temps de chargement permettant une consultation fluide du portfolio dans des conditions normales d'utilisation.

Une attention particulière doit être portée aux ressources susceptibles d'affecter les performances, notamment :

- les images ;
- les polices ;
- les feuilles de style ;
- les scripts ;
- les animations ;
- les ressources provenant de services externes.

Les ressources devront être optimisées afin de limiter leur poids et le volume de données transférées.

Les ressources qui ne sont pas immédiatement nécessaires à l'affichage initial pourront être chargées de manière différée lorsque cela est pertinent.

---

### 7.2 Performance des interactions

Les interactions principales de l'application doivent fournir un retour suffisamment rapide pour ne pas donner au visiteur l'impression que l'interface est bloquée.

Cela concerne notamment :

- la navigation ;
- la recherche de projets ;
- le filtrage des projets ;
- le changement de thème ;
- l'affichage du détail d'un projet ;
- les opérations réalisées depuis l'espace d'administration.

Lorsqu'une opération nécessite un traitement perceptible, l'interface doit pouvoir informer l'utilisateur qu'un traitement est en cours.

---

### 7.3 Performance de la recherche et du filtrage

La recherche et le filtrage doivent permettre d'actualiser la liste des projets sans dégradation perceptible de l'expérience utilisateur dans le volume de données prévu pour la V1.

La conception devra éviter :

- les traitements inutilement répétés ;
- le chargement de données inutiles ;
- les requêtes redondantes ;
- les transferts de données disproportionnés par rapport au besoin.

Les mécanismes d'optimisation précis dépendront de l'architecture et du mode de stockage retenus.

---

### 7.4 Optimisation des médias

Les médias utilisés dans le portfolio doivent être adaptés à leur contexte d'affichage.

Les images et autres ressources visuelles devront notamment être optimisées afin de limiter leur impact sur :

- le temps de chargement ;
- la consommation de bande passante ;
- les performances sur appareil mobile.

Lorsque cela est pertinent, différentes dimensions ou formats pourront être utilisés selon le contexte d'affichage.

---

### 7.5 Animations

Les animations et transitions prévues dans l'interface ne doivent pas dégrader significativement les performances de l'application.

Elles doivent rester secondaires par rapport à l'accès au contenu et aux fonctionnalités.

Une animation ne doit pas :

- bloquer une interaction essentielle ;
- provoquer un ralentissement important de l'interface ;
- être nécessaire à la compréhension d'une information ;
- empêcher l'utilisation de l'application lorsqu'elle ne peut pas être exécutée.

Les préférences utilisateur relatives à la réduction des animations devront être prises en compte lorsque l'environnement permet de les détecter.

---

### 7.6 Compatibilité avec les navigateurs

La V1 doit être utilisable avec les versions récentes des principaux navigateurs web modernes.

La compatibilité devra notamment être vérifiée avec des navigateurs représentatifs utilisant différents moteurs de rendu.

Les fonctionnalités essentielles ne doivent pas dépendre d'une fonctionnalité expérimentale disponible uniquement sur un navigateur particulier.

La liste précise des navigateurs et versions faisant partie du périmètre de test sera définie dans la documentation de test.

---

### 7.7 Compatibilité avec les différents écrans

L'interface doit s'adapter aux différentes tailles d'écran prévues dans le périmètre de la V1.

L'application doit notamment rester utilisable sur :

- ordinateur ;
- tablette ;
- smartphone.

L'adaptation de l'interface doit préserver :

- la lisibilité du contenu ;
- la navigation ;
- la consultation des projets ;
- la recherche et le filtrage ;
- les actions principales ;
- l'accès aux fonctionnalités d'administration sur les formats pour lesquels celles-ci sont prises en charge.

Les seuils d'adaptation de l'interface seront déterminés lors de la conception de l'interface et pourront évoluer en fonction des besoins réels du contenu.

---

### 7.8 Critères de mesure

Les performances de l'application devront être évaluées à l'aide de mesures reproductibles.

Les contrôles pourront notamment porter sur :

- le temps nécessaire à l'affichage du contenu principal ;
- la stabilité visuelle lors du chargement ;
- la réactivité de l'interface ;
- le poids des ressources transférées ;
- le nombre de ressources nécessaires au chargement ;
- les performances sur appareil mobile.

Les valeurs cibles précises devront être définies avant la phase de validation afin de disposer de critères d'acceptation mesurables.

Les outils utilisés pour réaliser ces mesures seront définis dans la documentation de test et dans la chaîne d'intégration continue lorsque ces contrôles seront automatisés.

---

## 8. Journalisation et observabilité

Cette section définit les exigences techniques relatives à la journalisation, au suivi du fonctionnement de l'application et à sa capacité à être supervisée.

L'objectif est de permettre l'identification des erreurs, le diagnostic des incidents et le suivi du comportement de l'application sans imposer à ce stade une solution particulière de supervision.

### 8.1 Journalisation applicative

L'application doit permettre de journaliser les événements techniques nécessaires à son exploitation et à son diagnostic.

Les journaux peuvent notamment concerner :

- le démarrage et l'arrêt des composants applicatifs ;
- les erreurs applicatives ;
- les erreurs d'accès aux données ;
- les échecs d'opérations importantes ;
- les événements liés à l'authentification de l'administrateur ;
- les opérations d'administration pertinentes ;
- les interactions avec des services externes lorsqu'elles nécessitent un suivi.

Les événements enregistrés doivent fournir suffisamment d'informations pour permettre leur analyse sans exposer inutilement de données sensibles.

---

### 8.2 Niveaux de journalisation

Le mécanisme de journalisation doit permettre de distinguer différents niveaux de gravité.

Les niveaux pourront notamment permettre d'identifier :

- les informations utiles au suivi normal de l'application ;
- les avertissements correspondant à une situation inhabituelle mais non bloquante ;
- les erreurs ayant empêché l'exécution normale d'une opération ;
- les erreurs critiques susceptibles d'affecter fortement le fonctionnement de l'application.

Le niveau de détail des journaux doit pouvoir être adapté selon l'environnement d'exécution.

La production ne doit pas exposer inutilement les informations techniques détaillées destinées au développement ou au diagnostic interne.

---

### 8.3 Protection des journaux

Les journaux ne doivent pas contenir inutilement d'informations sensibles.

Ne doivent notamment pas être enregistrés en clair :

- les mots de passe ;
- les secrets ;
- les clés API ;
- les jetons d'authentification ;
- les informations permettant de contourner les mécanismes de sécurité.

Lorsque certaines informations doivent être journalisées pour permettre le diagnostic, leur contenu doit être limité au strict nécessaire.

L'accès aux journaux de production doit être réservé aux personnes ou systèmes autorisés.

---

### 8.4 Traçabilité des opérations d'administration

Les opérations d'administration présentant un intérêt pour le diagnostic ou la sécurité doivent pouvoir être tracées.

Cela concerne notamment :

- les tentatives d'authentification ;
- les créations de projets ;
- les modifications de projets ;
- les suppressions de projets ;
- les erreurs rencontrées lors de ces opérations.

La journalisation doit permettre d'identifier la nature de l'événement et le moment auquel il s'est produit.

Les informations enregistrées devront rester proportionnées aux besoins du projet et respecter les règles de protection des données.

---

### 8.5 Gestion des erreurs

Les erreurs techniques doivent être traitées de manière à distinguer les informations destinées à l'utilisateur des informations nécessaires au diagnostic technique.

Une erreur ne doit pas exposer publiquement :

- une trace d'exécution détaillée ;
- des informations sur la configuration interne ;
- des informations d'authentification ;
- des secrets ;
- des informations techniques susceptibles de faciliter une attaque.

Les informations techniques nécessaires au diagnostic pourront être enregistrées dans les journaux appropriés.

L'utilisateur doit recevoir un message compréhensible lui permettant, lorsque cela est possible, de poursuivre son utilisation de l'application.

---

### 8.6 Métriques

L'architecture doit permettre l'ajout de métriques permettant de suivre le fonctionnement de l'application.

Selon les besoins d'exploitation, les métriques pourront notamment concerner :

- la disponibilité de l'application ;
- les temps de réponse ;
- le nombre de requêtes ;
- le taux d'erreurs ;
- l'utilisation des ressources techniques ;
- le comportement des composants nécessaires au fonctionnement de l'application.

Les métriques effectivement collectées dépendront de l'architecture et de l'environnement d'hébergement retenus.

---

### 8.7 Supervision

La solution doit pouvoir être supervisée afin de vérifier son bon fonctionnement après son déploiement.

La supervision pourra notamment permettre de détecter :

- une indisponibilité de l'application ;
- une augmentation anormale du nombre d'erreurs ;
- une dégradation des performances ;
- un dysfonctionnement d'un composant nécessaire à l'application.

La mise en place d'une plateforme complète de supervision n'est pas une exigence obligatoire de la V1.

L'architecture devra toutefois éviter de rendre difficile son intégration ultérieure.

---

### 8.8 Alertes

Lorsque des mécanismes de supervision sont mis en place, ils doivent pouvoir évoluer vers la génération d'alertes en cas d'événement nécessitant une intervention.

Une alerte pourra notamment être déclenchée en cas :

- d'indisponibilité prolongée ;
- de taux d'erreurs anormal ;
- de dégradation importante des performances ;
- d'événement de sécurité nécessitant une attention particulière.

Les seuils, canaux de notification et mécanismes techniques d'alerte seront définis en fonction de l'environnement de déploiement retenu.

---

### 8.9 Observabilité et évolutivité

Les choix techniques réalisés pour la V1 doivent permettre de faire évoluer progressivement les capacités d'observabilité du projet.

L'architecture devra notamment permettre l'intégration future, lorsque cela est pertinent, de mécanismes de :

- centralisation des journaux ;
- collecte de métriques ;
- visualisation ;
- supervision ;
- alerting ;
- traçage distribué si l'architecture future le justifie.

Les technologies permettant de mettre en œuvre ces mécanismes seront choisies en fonction de l'architecture, des besoins réels du projet et des contraintes d'exploitation.

---

## 9. Tests et qualité logicielle

## 9. Tests et qualité logicielle

Cette section définit les exigences techniques relatives aux tests, à la validation du code et au maintien de la qualité logicielle du projet.

L'objectif est de réduire les risques de régression, de détecter les anomalies avant leur mise en production et de garantir que les fonctionnalités développées restent conformes aux exigences définies.

Les outils, bibliothèques et seuils précis seront déterminés en fonction des technologies et de l'architecture retenues.

### 9.1 Stratégie générale de test

Le projet doit intégrer des tests adaptés aux différents niveaux de l'application.

La stratégie de test pourra notamment comprendre :

- des tests unitaires ;
- des tests d'intégration ;
- des tests fonctionnels ;
- des tests de bout en bout ;
- des tests de sécurité ;
- des tests de performance lorsque cela est pertinent.

Le choix et la répartition des différents types de tests devront être proportionnés aux risques et à la complexité des fonctionnalités concernées.

Les fonctionnalités critiques, notamment l'authentification et la gestion des projets, devront faire l'objet d'une attention particulière.

---

### 9.2 Tests unitaires

Les composants contenant une logique pouvant être testée de manière isolée doivent pouvoir faire l'objet de tests unitaires.

Ces tests devront notamment permettre de vérifier :

- les traitements métier ;
- les règles de validation ;
- les transformations de données ;
- les comportements attendus dans les cas nominaux ;
- les principaux cas d'erreur.

Les tests unitaires doivent pouvoir être exécutés automatiquement et de manière reproductible.

---

### 9.3 Tests d'intégration

Des tests d'intégration doivent permettre de vérifier le bon fonctionnement des interactions entre les composants concernés.

Selon l'architecture retenue, ils pourront notamment vérifier :

- les interactions avec le mécanisme de persistance ;
- les échanges entre différentes couches de l'application ;
- les mécanismes d'authentification et d'autorisation ;
- les opérations de création, lecture, modification et suppression des projets ;
- les échanges avec des services externes lorsqu'ils interviennent dans le fonctionnement de l'application.

Les tests d'intégration doivent permettre d'identifier les anomalies qui ne peuvent pas être détectées par les seuls tests unitaires.

---

### 9.4 Tests fonctionnels

Les fonctionnalités définies dans les spécifications fonctionnelles doivent pouvoir être vérifiées à partir de scénarios de test.

Ces tests devront notamment couvrir les fonctionnalités principales de la V1 :

- consultation du profil ;
- consultation de la liste des projets ;
- consultation détaillée d'un projet ;
- recherche ;
- filtrage ;
- changement et conservation du thème ;
- accès aux ressources externes ;
- prise de contact ;
- authentification de l'administrateur ;
- gestion des projets ;
- déconnexion de l'administrateur.

Les cas nominaux ainsi que les principaux cas particuliers définis dans les spécifications fonctionnelles devront être pris en compte.

---

### 9.5 Tests de bout en bout

Des tests de bout en bout pourront être utilisés afin de vérifier les parcours utilisateurs les plus importants dans un environnement représentatif de l'application.

Ils pourront notamment couvrir :

- la navigation depuis l'accueil jusqu'au détail d'un projet ;
- la recherche et le filtrage des projets ;
- l'authentification de l'administrateur ;
- la création d'un projet ;
- la modification d'un projet ;
- la suppression d'un projet ;
- la déconnexion.

Le nombre de tests de bout en bout devra rester proportionné aux besoins du projet afin de limiter leur coût de maintenance et leur temps d'exécution.

---

### 9.6 Tests de sécurité

Les fonctionnalités présentant des enjeux de sécurité doivent faire l'objet de contrôles spécifiques.

Les tests pourront notamment vérifier :

- le refus d'une authentification invalide ;
- l'impossibilité pour un utilisateur non authentifié d'accéder aux opérations d'administration protégées ;
- le contrôle des autorisations ;
- la validation des données reçues ;
- l'absence d'exposition de secrets ;
- le comportement de l'application face à des entrées invalides ou malformées.

Des outils automatisés d'analyse de sécurité pourront compléter ces tests.

La stratégie détaillée des contrôles de sécurité sera définie dans la documentation dédiée à la sécurité.

---

### 9.7 Analyse statique et qualité du code

Le code source doit pouvoir faire l'objet de contrôles automatisés indépendamment de son exécution.

Ces contrôles pourront notamment permettre de détecter :

- les erreurs de syntaxe ;
- les problèmes de formatage ;
- certaines erreurs de programmation ;
- les violations des conventions définies pour le projet ;
- certaines vulnérabilités ou mauvaises pratiques ;
- le code inutilisé ou problématique lorsque les outils retenus permettent de l'identifier.

Les règles appliquées doivent être cohérentes et reproductibles entre les environnements de développement et d'intégration continue.

---

### 9.8 Couverture des tests

La couverture du code peut être mesurée afin d'identifier les parties de l'application qui ne sont pas exercées par les tests automatisés.

La couverture ne doit toutefois pas constituer à elle seule un indicateur de qualité des tests.

La priorité doit être donnée à la couverture des comportements importants et des zones présentant le plus de risques.

Un seuil minimal pourra être défini lorsque la stratégie de test et les technologies du projet auront été déterminées.

Ce seuil devra être utilisé comme un indicateur complémentaire et non comme une garantie de qualité du logiciel.

---

### 9.9 Automatisation des contrôles

Les contrôles pouvant être automatisés doivent pouvoir être intégrés au processus d'intégration continue.

Selon les outils retenus, le pipeline pourra notamment exécuter :

- les contrôles de formatage ;
- l'analyse statique ;
- les tests unitaires ;
- les tests d'intégration ;
- certains tests fonctionnels ;
- les analyses de dépendances ;
- les contrôles de sécurité ;
- la construction de l'application.

L'échec d'un contrôle considéré comme obligatoire doit pouvoir empêcher la validation ou la livraison d'une version non conforme.

Les règles précises de blocage seront définies lors de la conception du pipeline CI/CD.

---

### 9.10 Reproductibilité des tests

Les tests automatisés doivent produire des résultats reproductibles dans des conditions équivalentes.

Le projet doit éviter autant que possible que les résultats dépendent :

- de l'environnement local d'un développeur ;
- de données non maîtrisées ;
- de l'ordre d'exécution des tests ;
- d'un état résiduel provenant d'une exécution précédente.

Les données et environnements nécessaires aux tests devront être préparés de manière contrôlée lorsque cela est nécessaire.

---

### 9.11 Traçabilité des tests

Les tests fonctionnels devront pouvoir être rattachés aux exigences et spécifications qu'ils permettent de vérifier.

La documentation de test devra conserver, lorsque cela est pertinent, la relation :

**Besoin → Exigence → User Story → Spécification fonctionnelle → Règle métier → Cas de test**

Les identifiants déjà définis dans les documents fonctionnels devront être réutilisés afin d'éviter la création de références incompatibles entre les différents documents.

---

### 9.12 Critères de validation

Une modification ne doit pas être considérée comme techniquement validée uniquement parce qu'elle fonctionne dans l'environnement local du développeur.

Avant son intégration ou sa livraison, les contrôles obligatoires définis pour le projet doivent être satisfaits.

Selon la nature de la modification, la validation pourra notamment nécessiter :

- la réussite des tests automatisés applicables ;
- l'absence d'erreur bloquante détectée par l'analyse statique ;
- la réussite des contrôles de sécurité obligatoires ;
- la construction correcte de l'application ;
- la validation des fonctionnalités concernées ;
- la revue des modifications avant leur intégration.

Les critères précis utilisés comme barrières de qualité seront définis dans le processus CI/CD et dans la stratégie de test.

## 10. CI/CD et déploiement

Cette section définit les exigences techniques relatives à l'intégration continue, à la livraison de l'application et à son déploiement.

L'objectif est de disposer d'un processus reproductible permettant de vérifier les modifications, de préparer les versions de l'application et de réduire les risques liés aux opérations manuelles de mise en production.

Les technologies et services utilisés pour mettre en œuvre cette chaîne seront sélectionnés en fonction de l'architecture, des besoins du projet et de l'environnement d'hébergement retenus.

### 10.1 Intégration continue

Le projet doit disposer d'un processus d'intégration continue permettant d'exécuter automatiquement les contrôles nécessaires lors des modifications du code source.

Selon la nature des modifications et les technologies retenues, ce processus pourra notamment exécuter :

- l'installation des dépendances ;
- les contrôles de formatage ;
- l'analyse statique du code ;
- les tests automatisés ;
- les contrôles de sécurité ;
- l'analyse des dépendances ;
- la détection de secrets ;
- la construction de l'application.

L'intégration continue doit permettre de détecter les anomalies avant l'intégration des modifications dans les branches protégées du projet.

---

### 10.2 Déclenchement des contrôles

Les contrôles automatisés doivent pouvoir être déclenchés lors des événements pertinents du cycle de développement.

Ils pourront notamment être exécutés :

- lors de l'ouverture ou de la mise à jour d'une Pull Request ;
- lors de l'intégration de modifications dans une branche de référence ;
- lors de la préparation d'une version ;
- manuellement lorsqu'une nouvelle exécution est nécessaire.

Les événements précis déclenchant chaque étape seront définis lors de la conception du pipeline.

---

### 10.3 Validation avant intégration

Les modifications destinées à rejoindre une branche protégée doivent satisfaire les contrôles obligatoires définis pour le projet.

Une modification présentant un échec sur un contrôle bloquant ne doit pas pouvoir être considérée comme validée.

Les contrôles bloquants pourront notamment concerner :

- les tests ;
- la construction de l'application ;
- l'analyse statique ;
- les contrôles de sécurité ;
- la détection de secrets ;
- la conformité aux règles définies pour le dépôt.

Les règles précises seront adaptées au niveau de maturité du projet et pourront évoluer progressivement.

---

### 10.4 Construction de l'application

Le processus de construction de l'application doit être reproductible.

À partir d'une même version du code source et d'une configuration équivalente, le processus doit permettre de produire une version déployable de l'application de manière cohérente.

Les dépendances nécessaires à la construction doivent être explicitement déclarées et leur gestion doit limiter les différences entre les environnements.

Les artefacts produits devront pouvoir être identifiés et rattachés à la version du code source dont ils proviennent.

---

### 10.5 Artefacts

Lorsqu'un processus de construction produit des artefacts destinés au déploiement, ceux-ci doivent pouvoir être identifiés et versionnés.

Un artefact peut notamment correspondre, selon l'architecture retenue, à :

- une application compilée ;
- un ensemble de fichiers statiques ;
- un paquet applicatif ;
- une image de conteneur ;
- tout autre élément nécessaire au déploiement.

Le format des artefacts dépendra des technologies finalement retenues.

Dans la mesure du possible, un artefact validé doit pouvoir être promu entre les environnements sans être reconstruit différemment pour chaque environnement.

---

### 10.6 Environnements

Le projet doit permettre de distinguer les configurations nécessaires aux différents contextes d'exécution.

Selon les besoins retenus, ces contextes pourront notamment comprendre :

- le développement local ;
- un environnement de validation ou de préproduction ;
- la production.

Les différences de configuration entre les environnements ne doivent pas nécessiter de modifier directement le code source de l'application.

Les secrets et paramètres propres à chaque environnement doivent être gérés séparément du code source.

---

### 10.7 Déploiement

Le déploiement de l'application doit pouvoir être réalisé selon une procédure documentée et reproductible.

Le processus doit permettre d'identifier :

- la version déployée ;
- l'environnement cible ;
- le résultat du déploiement ;
- les éventuelles erreurs rencontrées.

Les opérations pouvant être automatisées devront l'être lorsque leur automatisation apporte un gain de fiabilité, de reproductibilité ou de sécurité.

Le niveau d'automatisation retenu pour la V1 dépendra de l'environnement d'hébergement et des contraintes du projet.

---

### 10.8 Validation après déploiement

Un déploiement réussi techniquement ne suffit pas à garantir que l'application fonctionne correctement.

Des vérifications doivent pouvoir être réalisées après le déploiement afin de confirmer que l'application est utilisable.

Ces vérifications pourront notamment porter sur :

- l'accessibilité de l'application ;
- le fonctionnement des fonctionnalités essentielles ;
- la disponibilité des composants nécessaires ;
- l'absence d'erreurs critiques immédiatement détectables ;
- la version effectivement déployée.

Certaines de ces vérifications pourront être automatisées.

---

### 10.9 Gestion des échecs de déploiement

Un échec de déploiement ne doit pas conduire à laisser volontairement l'application dans un état incohérent sans possibilité de récupération.

La procédure de déploiement doit prévoir les actions permettant de diagnostiquer l'échec et de restaurer un état fonctionnel.

Selon l'architecture et l'environnement retenus, cela pourra notamment nécessiter :

- l'arrêt du déploiement ;
- la conservation de la version précédemment fonctionnelle ;
- la correction puis la réexécution du déploiement ;
- le retour vers une version antérieure.

---

### 10.10 Retour à une version antérieure

La stratégie de déploiement doit prévoir la possibilité de revenir à une version antérieure lorsque la nouvelle version provoque une anomalie importante en production.

La méthode utilisée dépendra :

- du type d'application ;
- du mécanisme de déploiement ;
- de la gestion des données ;
- de l'infrastructure retenue.

La procédure de retour arrière devra être documentée avant la mise en production.

Lorsque des modifications de données sont impliquées, leur compatibilité avec un retour à une version précédente devra être prise en compte.

---

### 10.11 Gestion des secrets dans la chaîne CI/CD

Les secrets nécessaires aux opérations d'intégration, de construction ou de déploiement ne doivent pas être directement inscrits dans :

- le code source ;
- les scripts versionnés ;
- les fichiers de configuration publics ;
- les journaux du pipeline.

La chaîne CI/CD doit utiliser un mécanisme permettant de fournir les secrets uniquement aux opérations qui en ont besoin.

Les droits accordés aux identités techniques utilisées par le pipeline doivent respecter le principe du moindre privilège.

---

### 10.12 Traçabilité des déploiements

Les déploiements doivent pouvoir être rattachés à une version identifiable du projet.

Il doit être possible de déterminer, dans la mesure permise par l'environnement retenu :

- quelle version a été déployée ;
- quand elle a été déployée ;
- dans quel environnement ;
- si le déploiement a réussi ou échoué.

Cette traçabilité doit faciliter le diagnostic des incidents et le retour vers une version antérieure lorsque cela est nécessaire.

---

### 10.13 Évolution de la chaîne CI/CD

La chaîne CI/CD doit pouvoir évoluer avec le projet.

De nouveaux contrôles pourront être intégrés progressivement, notamment :

- des analyses de sécurité supplémentaires ;
- des tests plus complets ;
- des contrôles de performance ;
- des vérifications de conformité ;
- des contrôles sur l'infrastructure ;
- des mécanismes de déploiement plus avancés.

Cette évolution devra rester cohérente avec les besoins réels du projet et éviter l'ajout de mécanismes inutilement complexes.

## 11. Gestion de la configuration et des environnements

Cette section définit les exigences techniques relatives à la configuration de l'application et à la gestion de ses différents environnements d'exécution.

L'objectif est de permettre à l'application de fonctionner dans plusieurs environnements sans nécessiter de modification du code source et de garantir une configuration maîtrisée, reproductible et sécurisée.

Les mécanismes et outils utilisés seront déterminés en fonction de l'architecture et de l'infrastructure retenues.

### 11.1 Séparation de la configuration et du code

Les paramètres susceptibles de varier selon l'environnement ne doivent pas être directement intégrés au code source lorsqu'ils nécessitent une configuration spécifique.

Cela peut notamment concerner :

- les paramètres de connexion aux services de persistance ;
- les adresses des services utilisés par l'application ;
- les paramètres liés à l'authentification ;
- les paramètres propres à l'environnement d'exécution ;
- les secrets nécessaires au fonctionnement de l'application.

Le code source doit pouvoir être utilisé dans différents environnements en adaptant sa configuration sans nécessiter de modification de sa logique applicative.

---

### 11.2 Environnement de développement

Un environnement de développement doit permettre de développer et de tester l'application localement.

Il doit permettre au développeur :

- d'exécuter les composants nécessaires au développement ;
- d'utiliser une configuration adaptée au contexte local ;
- d'exécuter les tests ;
- de diagnostiquer les erreurs ;
- de travailler sans dépendre directement de l'environnement de production.

Les données et secrets de production ne doivent pas être nécessaires au fonctionnement normal de l'environnement de développement.

---

### 11.3 Environnement de validation

Un environnement distinct de la production pourra être utilisé afin de valider l'application avant sa mise en production.

Cet environnement pourra notamment permettre :

- de vérifier une version candidate ;
- d'exécuter certains tests dans des conditions proches de la production ;
- de vérifier le processus de déploiement ;
- de valider les interactions entre les différents composants ;
- de détecter des anomalies avant la mise en production.

La nécessité de disposer d'un environnement de validation permanent ou temporaire sera déterminée en fonction des contraintes d'hébergement et du niveau d'automatisation retenu.

---

### 11.4 Environnement de production

L'environnement de production correspond à l'environnement dans lequel la version publique du portfolio est exécutée.

Sa configuration doit être adaptée à un usage réel de l'application.

Une attention particulière doit être portée :

- à la sécurité ;
- à la disponibilité ;
- aux performances ;
- à la gestion des secrets ;
- à la journalisation ;
- aux mécanismes de déploiement ;
- à la possibilité de diagnostiquer un incident.

Les fonctionnalités ou informations exclusivement destinées au développement ne doivent pas être exposées publiquement en production.

---

### 11.5 Variables de configuration

Les paramètres variables doivent pouvoir être fournis à l'application par un mécanisme de configuration approprié.

Selon les technologies retenues, ce mécanisme pourra notamment reposer sur :

- des variables d'environnement ;
- des fichiers de configuration ;
- un service de configuration ;
- un mécanisme fourni par la plateforme d'hébergement.

Les valeurs de configuration doivent être clairement distinguées du code source.

Les paramètres obligatoires au fonctionnement de l'application doivent être documentés.

---

### 11.6 Gestion des secrets

Les secrets constituent une catégorie particulière de configuration et doivent bénéficier de protections supplémentaires.

Ils ne doivent pas être :

- intégrés directement au code source ;
- versionnés dans le dépôt Git ;
- exposés dans la partie publique de l'application ;
- enregistrés inutilement dans les journaux ;
- copiés sans nécessité entre les environnements.

Chaque environnement doit pouvoir disposer de ses propres secrets.

Le mécanisme de stockage et de distribution des secrets sera défini en fonction de l'environnement d'hébergement et de la chaîne CI/CD retenus.

---

### 11.7 Fichiers de configuration locaux

Lorsqu'un fichier local est utilisé pour fournir des paramètres propres à un environnement de développement, les fichiers contenant des valeurs sensibles ne doivent pas être versionnés.

Un fichier d'exemple dépourvu de secrets pourra être fourni afin de documenter les paramètres nécessaires.

Ce fichier d'exemple devra permettre d'identifier :

- les paramètres attendus ;
- leur rôle ;
- les éventuelles valeurs non sensibles utilisables par défaut.

---

### 11.8 Validation de la configuration

L'application doit pouvoir détecter une configuration obligatoire absente ou invalide.

Lorsqu'une configuration indispensable au démarrage n'est pas disponible, l'application doit éviter de poursuivre son exécution dans un état incohérent.

Les erreurs de configuration doivent permettre un diagnostic technique tout en évitant l'exposition publique de secrets ou d'informations sensibles.

---

### 11.9 Cohérence entre les environnements

Les environnements doivent être suffisamment cohérents pour limiter les anomalies apparaissant uniquement lors du passage en production.

Les différences nécessaires entre les environnements doivent principalement relever de leur configuration et non de versions différentes du code source.

Lorsque cela est possible, les mêmes mécanismes de construction et de déploiement doivent être réutilisés entre les différents environnements.

---

### 11.10 Reproductibilité des environnements

La mise en place d'un environnement nécessaire au projet doit être documentée et reproductible dans une mesure adaptée aux besoins de la V1.

La documentation doit permettre d'identifier :

- les dépendances nécessaires ;
- les paramètres de configuration ;
- les services requis ;
- les étapes nécessaires au démarrage de l'application.

Lorsque la complexité de l'infrastructure le justifie, l'automatisation de sa création et de sa configuration pourra être envisagée.

Les technologies permettant cette automatisation seront choisies après définition de l'architecture et de l'infrastructure cibles.

---

### 11.11 Configuration de l'infrastructure

Lorsque le fonctionnement de l'application nécessite des ressources d'infrastructure configurables, leur configuration doit pouvoir être documentée et reproduite.

Selon l'infrastructure finalement retenue, une approche d'Infrastructure as Code pourra être utilisée afin notamment de :

- versionner la définition de l'infrastructure ;
- rendre sa création reproductible ;
- limiter les opérations manuelles ;
- faciliter la revue des modifications ;
- intégrer certains contrôles dans le processus CI/CD.

Le recours à l'Infrastructure as Code dépendra de la complexité et des besoins réels de l'infrastructure du projet.

---

### 11.12 Documentation de la configuration

Les éléments nécessaires à la configuration et à l'exécution du projet doivent être documentés.

La documentation doit permettre à une personne disposant des autorisations nécessaires de comprendre :

- les environnements existants ;
- les paramètres nécessaires ;
- les dépendances externes ;
- la procédure de configuration ;
- les mécanismes de gestion des secrets ;
- les principales différences entre les environnements.

Aucune valeur secrète réelle ne doit être incluse dans cette documentation.

---

## 12. Gestion des données et persistance

Cette section définit les exigences techniques relatives à la gestion, à la persistance et à l'intégrité des données utilisées par l'application.

La V1 nécessitant la gestion dynamique des projets depuis un espace d'administration, les données associées aux projets doivent pouvoir être conservées indépendamment du cycle d'exécution de l'application.

Le modèle de données et la technologie de persistance seront définis lors de la conception en fonction de la structure des données, des relations identifiées, des besoins fonctionnels et des contraintes techniques du projet.

### 12.1 Données persistantes

Les informations nécessaires à la présentation et à la gestion des projets doivent être persistées.

Un projet doit notamment pouvoir comporter les informations définies dans les spécifications fonctionnelles, telles que :

- un titre ;
- un résumé ;
- une description ;
- un contexte ;
- un objectif ;
- une ou plusieurs catégories ;
- les technologies ou outils utilisés ;
- la méthodologie suivie ;
- les principales étapes de réalisation ;
- les difficultés rencontrées ;
- les solutions apportées ;
- les résultats obtenus ;
- des mots-clés ;
- un éventuel lien vers une démonstration ;
- un éventuel lien vers un dépôt public ;
- les informations nécessaires à la gestion des contenus visuels associés.

Certaines informations sont obligatoires tandis que d'autres peuvent être facultatives conformément aux règles fonctionnelles définies pour les projets.

---

### 12.2 Identification des projets

Chaque projet doit disposer d'un identifiant permettant de le distinguer de manière non ambiguë des autres projets.

Cet identifiant doit permettre de retrouver le projet concerné lors des opérations de :

- consultation ;
- modification ;
- suppression ;
- association avec d'autres données.

Le mécanisme technique utilisé pour produire cet identifiant sera déterminé lors de la conception du modèle de données.

---

### 12.3 Relations entre les données

Le modèle de données doit permettre de représenter les relations nécessaires au fonctionnement de l'application.

Il doit notamment prendre en compte qu'un projet peut être associé à plusieurs catégories et à plusieurs technologies ou outils.

Une même catégorie ou technologie peut également être associée à plusieurs projets.

Les autres relations nécessaires seront identifiées lors de la modélisation détaillée des données.

Le modèle retenu devra limiter les incohérences et les duplications inutiles de données.

---

### 12.4 Création des données

Lorsqu'un administrateur crée un projet, les données validées doivent pouvoir être enregistrées de manière persistante.

L'enregistrement ne doit être effectué que lorsque les données obligatoires respectent les règles définies pour le projet.

Après une création réussie, le projet doit pouvoir être retrouvé depuis les fonctionnalités concernées de l'application.

---

### 12.5 Lecture des données

L'application doit permettre de récupérer les données nécessaires à la consultation publique et à l'administration des projets.

Les données retournées doivent être adaptées au contexte dans lequel elles sont utilisées.

La partie publique de l'application ne doit pas recevoir inutilement des informations réservées à l'administration ou des données sensibles.

---

### 12.6 Modification des données

L'administrateur doit pouvoir modifier les informations d'un projet existant.

Les nouvelles valeurs doivent être validées avant leur persistance.

Une modification réussie doit remplacer ou compléter les données concernées sans compromettre l'intégrité des autres informations du projet.

Les modifications persistées doivent être prises en compte lors des consultations ultérieures.

---

### 12.7 Suppression des données

L'administrateur doit pouvoir supprimer un projet conformément aux règles fonctionnelles définies.

La suppression doit prendre en compte les éventuelles relations du projet avec d'autres données afin d'éviter de laisser des références incohérentes.

Le comportement précis des données associées lors de la suppression d'un projet sera défini dans le modèle de données.

La stratégie de suppression retenue devra également déterminer si une suppression doit être définitive ou si certaines données doivent pouvoir être conservées ou restaurées.

---

### 12.8 Validation et intégrité des données

Les données doivent être validées avant leur persistance.

Les contrôles doivent permettre notamment de vérifier :

- la présence des données obligatoires ;
- leur type ;
- leur format ;
- les contraintes de longueur lorsque cela est pertinent ;
- la validité des valeurs attendues ;
- la cohérence des relations entre les données.

Les mécanismes de persistance doivent également contribuer au maintien de l'intégrité des données lorsque la technologie retenue le permet.

La validation réalisée dans l'interface utilisateur ne doit pas constituer l'unique mécanisme de protection de l'intégrité des données.

---

### 12.9 Cohérence des opérations

Les opérations modifiant plusieurs données liées doivent éviter de laisser le système dans un état partiellement modifié ou incohérent lorsqu'une erreur intervient.

Lorsque plusieurs modifications constituent une même opération logique, la solution de persistance retenue devra permettre de garantir un niveau de cohérence adapté au besoin.

Les mécanismes précis dépendront de la technologie de persistance sélectionnée.

---

### 12.10 Accès aux données

L'accès en écriture aux données administrables doit être réservé aux opérations autorisées.

Un visiteur non authentifié ne doit pas pouvoir :

- créer un projet ;
- modifier un projet ;
- supprimer un projet ;
- modifier directement les données utilisées par l'application.

Les mécanismes de contrôle d'accès doivent être appliqués indépendamment des restrictions présentes dans l'interface utilisateur.

---

### 12.11 Protection des données sensibles

Les données sensibles éventuellement nécessaires au fonctionnement de l'application ne doivent pas être stockées ou exposées sans protection adaptée.

Les données d'authentification doivent notamment respecter les exigences définies dans la section relative à la sécurité.

Les secrets de configuration ne doivent pas être stockés dans les mêmes données applicatives simplement pour faciliter leur utilisation.

---

### 12.12 Sauvegarde et restauration

Les données nécessaires au fonctionnement du portfolio doivent pouvoir être sauvegardées lorsqu'une perte de ces données aurait un impact significatif sur l'application.

La stratégie retenue devra prendre en compte :

- les données à sauvegarder ;
- la fréquence adaptée au besoin ;
- le lieu de conservation des sauvegardes ;
- leur durée de conservation ;
- leur protection ;
- la possibilité de restaurer les données.

Une sauvegarde ne doit pas être considérée comme fiable uniquement parce qu'elle a été créée.

La possibilité de restaurer les données devra pouvoir être vérifiée.

---

### 12.13 Évolution du modèle de données

Le modèle de données doit pouvoir évoluer avec les futures versions de l'application.

Les modifications de structure devront pouvoir être identifiées, versionnées et appliquées de manière contrôlée lorsque la technologie retenue le nécessite.

Une évolution du modèle de données ne doit pas entraîner volontairement une perte de données existantes sans qu'une procédure adaptée ait été prévue.

Les modifications du modèle devront également être prises en compte dans les procédures de déploiement et de retour arrière lorsqu'elles affectent la compatibilité entre différentes versions de l'application.

---

### 12.14 Données de développement et de test

Les environnements de développement et de test doivent pouvoir utiliser des données adaptées à leur usage sans nécessiter l'utilisation des données réelles de production.

Lorsque des jeux de données de test sont nécessaires, ils doivent pouvoir être créés ou réinitialisés de manière contrôlée.

Les tests automatisés ne doivent pas modifier les données de production.

---

### 12.15 Choix du mécanisme de persistance

La technologie de persistance ne doit pas être sélectionnée uniquement en fonction de sa popularité ou de sa maîtrise préalable.

Le choix devra notamment prendre en compte :

- la structure des données ;
- les relations entre les données ;
- les contraintes d'intégrité ;
- les opérations de lecture et d'écriture nécessaires ;
- les besoins de recherche et de filtrage ;
- les besoins de sauvegarde et de restauration ;
- les besoins d'évolution du modèle ;
- les contraintes d'exploitation et de déploiement ;
- la complexité introduite par la solution.

La décision retenue devra être justifiée dans la documentation d'architecture et pourra faire l'objet d'un ADR.

---

## 13. API et échanges entre composants

Cette section définit les exigences techniques relatives aux échanges de données entre les différents composants de l'application et, lorsque cela est nécessaire, à l'exposition d'interfaces applicatives.

L'objectif est de garantir des échanges cohérents, sécurisés et maintenables sans imposer prématurément un style d'API, un protocole ou une architecture particulière.

Les mécanismes de communication seront déterminés lors de la conception de l'architecture en fonction des composants identifiés et de leurs besoins d'interaction.

### 13.1 Identification des échanges

L'architecture devra identifier les échanges nécessaires entre les différents composants participant au fonctionnement de l'application.

Ces échanges pourront notamment concerner :

- la récupération des projets destinés à la partie publique ;
- la récupération du détail d'un projet ;
- la recherche et le filtrage des projets ;
- l'authentification de l'administrateur ;
- la consultation des projets depuis l'administration ;
- la création d'un projet ;
- la modification d'un projet ;
- la suppression d'un projet ;
- l'accès aux données persistées ;
- les éventuelles interactions avec des services externes.

La nature de ces échanges dépendra de la séparation retenue entre les différents composants de l'application.

---

### 13.2 Interface entre la présentation et la logique applicative

Les fonctionnalités de présentation ne doivent pas dépendre directement de la manière dont les données sont physiquement stockées.

Les échanges entre l'interface utilisateur et la logique chargée de traiter les données doivent reposer sur des contrats clairement définis.

Ces contrats doivent notamment préciser :

- les données attendues ;
- les données retournées ;
- les opérations disponibles ;
- les conditions de réussite ;
- les principaux cas d'erreur.

Cette séparation doit permettre de faire évoluer le mécanisme de persistance sans imposer inutilement sa structure interne à l'interface utilisateur.

---

### 13.3 Consultation des projets

Le mécanisme d'échange retenu doit permettre à la partie publique de récupérer les informations nécessaires à l'affichage des projets.

Il doit notamment permettre :

- d'obtenir la liste des projets publiés ;
- d'obtenir les informations nécessaires aux cartes de présentation ;
- d'obtenir le détail d'un projet ;
- d'obtenir les catégories et technologies associées lorsque cela est nécessaire.

Les données retournées doivent être limitées aux informations utiles au contexte de consultation.

---

### 13.4 Recherche et filtrage

Les mécanismes d'échange doivent permettre de répondre aux besoins de recherche et de filtrage définis dans les spécifications fonctionnelles.

Selon l'architecture et le volume de données retenus, la recherche et le filtrage pourront être réalisés :

- dans l'interface utilisateur ;
- par un composant applicatif ;
- par le mécanisme de persistance ;
- par une combinaison de ces mécanismes.

Le choix devra notamment prendre en compte :

- le volume de données ;
- les performances ;
- la maintenabilité ;
- la complexité de la recherche ;
- les possibilités d'évolution du projet.

---

### 13.5 Opérations d'administration

Les échanges permettant de modifier les données doivent être protégés.

Les opérations suivantes doivent être réservées à l'administrateur autorisé :

- création d'un projet ;
- modification d'un projet ;
- suppression d'un projet.

La réception d'une demande de modification ne doit pas entraîner automatiquement son exécution.

Avant toute modification persistante, le système doit notamment vérifier :

- l'authentification lorsque celle-ci est requise ;
- l'autorisation de réaliser l'opération ;
- la validité des données reçues ;
- l'existence des ressources concernées lorsque cela est nécessaire.

---

### 13.6 Format des données échangées

Les données échangées entre composants doivent utiliser une représentation clairement définie et adaptée aux technologies retenues.

La structure des données doit être suffisamment stable et documentée pour éviter une dépendance implicite entre les composants.

Lorsque des données sont facultatives, absentes ou invalides, leur comportement doit être défini de manière cohérente.

Le format technique utilisé pour représenter les échanges sera déterminé lors de la conception de l'architecture.

---

### 13.7 Validation des données reçues

Toute donnée reçue depuis une interface externe au composant qui la traite doit être considérée comme non fiable jusqu'à sa validation.

Les contrôles doivent notamment pouvoir porter sur :

- la présence des données obligatoires ;
- leur type ;
- leur format ;
- les valeurs autorisées ;
- les longueurs ou limites définies ;
- la cohérence entre plusieurs données.

Une donnée refusée ne doit pas être persistée comme si l'opération avait réussi.

La validation réalisée dans l'interface utilisateur ne doit pas remplacer la validation réalisée au niveau chargé d'exécuter l'opération.

---

### 13.8 Gestion des réponses et des erreurs

Les composants doivent communiquer de manière suffisamment explicite le résultat des opérations demandées.

Il doit être possible de distinguer notamment :

- une opération réussie ;
- une donnée invalide ;
- une authentification nécessaire ou invalide ;
- une opération non autorisée ;
- une ressource inexistante ;
- une erreur interne.

Les informations retournées à l'utilisateur ne doivent pas exposer de détails techniques sensibles.

Les informations nécessaires au diagnostic peuvent être enregistrées dans les mécanismes de journalisation prévus à cet effet.

---

### 13.9 Authentification des échanges protégés

Lorsqu'un échange permet d'accéder à une fonctionnalité réservée à l'administration, le système doit pouvoir vérifier l'identité de l'administrateur.

Les informations permettant de maintenir ou de prouver cette authentification doivent être protégées contre :

- leur exposition inutile ;
- leur modification non autorisée ;
- leur réutilisation abusive lorsque des mécanismes permettent de limiter ce risque.

Le mécanisme précis d'authentification sera déterminé lors de la conception de la sécurité et de l'architecture.

---

### 13.10 Autorisation

L'identification d'un utilisateur ne suffit pas à autoriser automatiquement une opération.

Le composant responsable d'une opération protégée doit vérifier que l'utilisateur dispose des droits nécessaires pour l'exécuter.

Les contrôles d'autorisation doivent être réalisés du côté où l'opération protégée est effectivement traitée et ne doivent pas reposer uniquement sur l'interface utilisateur.

---

### 13.11 Sécurisation des échanges

Les échanges contenant des informations sensibles ou permettant des opérations protégées doivent utiliser des mécanismes de communication adaptés au niveau de risque.

En production, les communications exposées sur un réseau non considéré comme sûr doivent être protégées contre leur interception ou leur modification.

Les interfaces exposées ne doivent fournir que les opérations nécessaires au fonctionnement de l'application.

---

### 13.12 Évolution des contrats d'échange

Les contrats utilisés pour les échanges entre composants doivent pouvoir évoluer sans provoquer inutilement de rupture dans l'ensemble de l'application.

Une modification susceptible d'affecter plusieurs composants devra être identifiée et prise en compte dans les composants concernés.

Si une interface doit ultérieurement être consommée indépendamment par plusieurs clients ou services, une stratégie de gestion de ses évolutions pourra être mise en place.

Le besoin de versionner explicitement une API sera évalué en fonction de l'architecture retenue et de son exposition.

---

### 13.13 Documentation des interfaces

Les interfaces techniques nécessaires aux échanges entre composants doivent être documentées lorsque leur complexité ou leur exposition le justifie.

La documentation pourra notamment préciser :

- les opérations disponibles ;
- les données attendues ;
- les données retournées ;
- les règles de validation ;
- les mécanismes d'authentification nécessaires ;
- les erreurs pouvant être retournées.

Le format et les outils de documentation seront déterminés en fonction du type d'interface retenu.

---

### 13.14 Choix du mécanisme de communication

Le mécanisme de communication entre les composants sera sélectionné après définition de l'architecture de l'application.

Le choix devra notamment prendre en compte :

- le nombre et la nature des composants ;
- leur niveau de couplage ;
- leur emplacement d'exécution ;
- les besoins de sécurité ;
- les besoins de performance ;
- les besoins d'évolution ;
- la simplicité de développement et d'exploitation ;
- la nécessité éventuelle d'exposer une interface à d'autres consommateurs.

Une API réseau indépendante ne doit pas être introduite lorsqu'une communication interne plus simple répond suffisamment aux besoins.

Inversement, lorsqu'une séparation entre composants nécessite une interface réseau clairement définie, le style d'API et le protocole devront être sélectionnés en fonction de ces contraintes.

La décision retenue devra être documentée dans l'architecture et pourra faire l'objet d'un ADR.

---

## 14. Contraintes techniques et critères de choix technologiques

Cette section définit les contraintes techniques connues du projet ainsi que les critères qui devront être utilisés pour sélectionner les technologies, outils et solutions d'infrastructure de **Fidel Portfolio**.

L'objectif est d'éviter que les choix techniques reposent uniquement sur les habitudes du développeur, la popularité d'une technologie ou une préférence personnelle.

Les solutions retenues devront répondre aux besoins fonctionnels et non fonctionnels du projet tout en restant cohérentes avec son périmètre, ses contraintes et ses perspectives d'évolution.

---

### 14.1 Principes de sélection

Les choix technologiques devront être réalisés à partir des besoins du projet.

Une technologie ne devra pas être retenue uniquement parce qu'elle :

- est populaire ;
- est récente ;
- est déjà connue du développeur ;
- est fréquemment utilisée dans d'autres projets ;
- permet d'ajouter des fonctionnalités qui ne répondent à aucun besoin identifié.

À l'inverse, une technologie déjà maîtrisée pourra constituer un avantage lorsqu'elle répond correctement aux besoins et permet de réduire la complexité, le temps de développement ou les risques du projet.

Les décisions importantes devront pouvoir être justifiées à partir de critères explicites.

---

### 14.2 Contraintes liées au périmètre du projet

La solution retenue doit être proportionnée au périmètre de la V1.

La V1 comprend notamment :

- une partie publique permettant de présenter le profil et les projets ;
- une recherche et un filtrage des projets ;
- une consultation détaillée des projets ;
- un espace d'administration protégé ;
- une authentification de l'administrateur ;
- la création, la consultation, la modification et la suppression des projets ;
- la persistance des données nécessaires au fonctionnement de l'application ;
- une interface responsive ;
- la gestion d'un thème clair et sombre.

L'architecture et les technologies retenues ne doivent pas introduire une complexité disproportionnée par rapport à ces besoins.

---

### 14.3 Maintenabilité

Les technologies retenues doivent permettre de construire une application compréhensible et maintenable.

L'évaluation de la maintenabilité devra notamment prendre en compte :

- la lisibilité du code ;
- la séparation des responsabilités ;
- la possibilité de tester les composants ;
- la facilité de correction des anomalies ;
- la facilité d'ajout ou de modification de fonctionnalités ;
- la qualité de la documentation disponible ;
- la stabilité des technologies utilisées.

Une solution techniquement performante mais difficile à maintenir ne devra pas être privilégiée sans justification suffisante.

---

### 14.4 Sécurité

Les technologies et composants sélectionnés doivent permettre de mettre en œuvre les mesures de sécurité nécessaires au projet.

Ils doivent notamment permettre de traiter correctement :

- l'authentification de l'administrateur ;
- l'autorisation des opérations protégées ;
- la validation des données ;
- la protection des secrets ;
- la sécurisation des communications ;
- la gestion des dépendances ;
- la journalisation des événements pertinents ;
- la limitation de l'exposition des composants internes.

Une technologie présentant des vulnérabilités connues non corrigées ou n'étant plus maintenue ne doit pas être utilisée en production.

Les mesures détaillées seront définies dans la documentation de sécurité.

---

### 14.5 Performance

Les technologies retenues doivent permettre d'atteindre les objectifs de performance définis pour le projet.

L'évaluation pourra notamment prendre en compte :

- le temps nécessaire à l'affichage des pages ;
- le volume de ressources transférées ;
- le traitement des données ;
- les échanges entre composants ;
- les opérations de lecture et d'écriture ;
- le comportement de l'application sur les appareils et connexions ciblés.

L'optimisation ne doit toutefois pas entraîner une complexité disproportionnée lorsqu'aucun besoin mesurable ne la justifie.

---

### 14.6 Évolutivité

La solution doit permettre les évolutions raisonnablement prévisibles du portfolio.

Elle devra notamment faciliter :

- l'ajout de nouveaux projets ;
- l'évolution des informations associées aux projets ;
- l'ajout de nouvelles catégories ou technologies ;
- l'évolution de l'espace d'administration ;
- l'ajout de nouvelles fonctionnalités ;
- l'évolution des mécanismes de déploiement.

L'évolutivité ne signifie pas que l'architecture doit anticiper toutes les évolutions possibles.

Les mécanismes complexes destinés à répondre à des besoins hypothétiques ne devront pas être introduits sans justification.

---

### 14.7 Testabilité

Les technologies et l'architecture retenues doivent permettre de vérifier automatiquement les comportements importants de l'application.

La solution devra permettre la mise en place, selon les besoins, de différents niveaux de tests, notamment :

- tests unitaires ;
- tests d'intégration ;
- tests fonctionnels ;
- tests de bout en bout ;
- contrôles de sécurité ;
- contrôles intégrés au processus d'intégration continue.

Les outils précis seront sélectionnés en fonction des technologies finalement retenues.

---

### 14.8 Automatisation et CI/CD

La solution doit être compatible avec l'automatisation des principales étapes du cycle de développement.

Il doit notamment être possible d'automatiser tout ou partie des opérations suivantes :

- installation des dépendances ;
- vérification de la qualité du code ;
- exécution des tests ;
- analyse des dépendances ;
- construction de l'application ;
- création des artefacts nécessaires au déploiement ;
- déploiement selon l'environnement concerné.

Les technologies retenues doivent pouvoir être intégrées dans une chaîne CI/CD adaptée au projet.

---

### 14.9 Déploiement et portabilité

Les choix techniques doivent prendre en compte les conditions dans lesquelles l'application sera exécutée et déployée.

L'évaluation devra notamment considérer :

- les prérequis nécessaires à l'exécution ;
- la reproductibilité du déploiement ;
- la gestion de la configuration ;
- la gestion des environnements ;
- la compatibilité avec les solutions d'hébergement envisagées ;
- la possibilité de migrer vers une autre solution lorsque cela est raisonnablement nécessaire.

Une dépendance forte à une plateforme ou à un fournisseur devra être identifiée lorsqu'elle peut avoir un impact significatif sur l'évolution du projet.

---

### 14.10 Coût

Le coût constitue un critère de sélection des solutions techniques et d'infrastructure.

L'évaluation doit prendre en compte, lorsque cela est applicable :

- le coût de l'hébergement ;
- le coût du stockage ;
- le coût des bases de données ou services managés ;
- le coût du trafic réseau ;
- le coût des outils utilisés ;
- les éventuelles licences ;
- l'évolution du coût avec l'utilisation de l'application.

Pour la V1, les solutions gratuites ou à faible coût pourront être privilégiées lorsqu'elles répondent correctement aux autres exigences du projet.

Le coût ne doit toutefois pas être le seul critère de décision.

---

### 14.11 Maturité et pérennité

Les technologies retenues doivent présenter un niveau de maturité compatible avec l'utilisation prévue.

L'évaluation pourra notamment prendre en compte :

- l'activité du projet ou de l'éditeur ;
- la fréquence et la qualité des mises à jour ;
- la disponibilité des correctifs de sécurité ;
- la documentation officielle ;
- la communauté ou l'écosystème ;
- la politique de support ;
- la stabilité des interfaces proposées.

L'utilisation d'une technologie récente ou expérimentale devra être justifiée lorsque son niveau de maturité augmente significativement le risque du projet.

---

### 14.12 Compétences et apprentissage

Le niveau de maîtrise des technologies constitue un critère à prendre en compte, mais ne doit pas déterminer seul les choix techniques.

Pour chaque solution envisagée, il pourra être nécessaire d'évaluer :

- les connaissances déjà acquises ;
- le temps nécessaire à l'apprentissage ;
- la difficulté de mise en œuvre ;
- la capacité à maintenir la solution dans le temps ;
- l'intérêt pédagogique ou professionnel de la technologie.

Dans le cadre du portfolio, l'utilisation d'une technologie nouvelle peut être pertinente lorsqu'elle permet de développer une compétence recherchée tout en restant cohérente avec les besoins réels du projet.

---

### 14.13 Complexité opérationnelle

Les technologies et architectures envisagées doivent également être évaluées selon leur coût opérationnel.

L'analyse devra notamment prendre en compte :

- le nombre de composants à exploiter ;
- le nombre de services à configurer ;
- la gestion des déploiements ;
- la supervision nécessaire ;
- la gestion des incidents ;
- la gestion des sauvegardes ;
- la gestion des mises à jour ;
- la difficulté de diagnostic en cas de panne.

Une architecture distribuée ne doit pas être retenue uniquement pour démontrer la maîtrise de technologies associées aux systèmes distribués.

Elle doit apporter un bénéfice identifiable au regard des besoins ou des objectifs du projet.

---

### 14.14 Dépendance technologique

Les choix devront prendre en compte le niveau de dépendance créé envers :

- un framework ;
- une bibliothèque ;
- un fournisseur Cloud ;
- un service managé ;
- une plateforme de déploiement ;
- un format propriétaire ;
- une API externe.

Une dépendance n'est pas nécessairement problématique.

Elle doit cependant être identifiée lorsque son remplacement pourrait entraîner un coût important ou une modification significative de l'application.

---

### 14.15 Critères de comparaison des solutions

Les principales solutions envisagées pourront être comparées à l'aide d'une grille commune.

| Critère | Question principale |
|---------|---------------------|
| Adéquation fonctionnelle | La solution permet-elle de répondre aux fonctionnalités attendues ? |
| Adéquation technique | Répond-elle aux contraintes techniques identifiées ? |
| Sécurité | Permet-elle d'appliquer correctement les mesures de sécurité nécessaires ? |
| Maintenabilité | La solution restera-t-elle compréhensible et modifiable ? |
| Testabilité | Permet-elle de mettre en place les tests nécessaires ? |
| Performance | Permet-elle d'atteindre les objectifs de performance ? |
| Évolutivité | Peut-elle accompagner les évolutions raisonnablement prévues ? |
| Déploiement | Peut-elle être déployée et exploitée simplement ? |
| Automatisation | S'intègre-t-elle correctement dans une chaîne CI/CD ? |
| Coût | Son coût initial et récurrent est-il acceptable ? |
| Maturité | Dispose-t-elle d'un niveau de stabilité et de support suffisant ? |
| Documentation | Existe-t-il une documentation officielle suffisante ? |
| Compétences | Quel effort d'apprentissage et de maintenance nécessite-t-elle ? |
| Complexité | La complexité introduite est-elle proportionnée aux bénéfices ? |
| Portabilité | Quel serait l'effort nécessaire pour changer de solution ? |

---

### 14.16 Méthode de décision

Lorsqu'un choix technologique important doit être effectué, plusieurs solutions pertinentes devront être identifiées lorsque des alternatives réalistes existent.

La décision pourra suivre les étapes suivantes :

1. identifier le besoin ou le problème à résoudre ;
2. identifier les contraintes associées ;
3. sélectionner les solutions techniquement envisageables ;
4. éliminer les solutions incompatibles avec les exigences obligatoires ;
5. comparer les solutions restantes à partir des critères pertinents ;
6. identifier les avantages, inconvénients et compromis de chaque solution ;
7. sélectionner la solution présentant le meilleur compromis pour le projet ;
8. documenter la décision lorsqu'elle possède un impact architectural significatif.

Tous les critères ne doivent pas nécessairement avoir la même importance.

Leur pondération dépendra du problème étudié.

---

### 14.17 Traçabilité des choix technologiques

Les choix techniques structurants devront pouvoir être reliés aux besoins ou contraintes qui les justifient.

La chaîne de décision recherchée est la suivante :

**Besoin → Exigence → Contrainte → Alternatives → Critères → Décision → Justification**

Les décisions ayant un impact significatif sur l'architecture pourront être documentées à l'aide d'**Architecture Decision Records (ADR)**.

Un ADR devra notamment permettre de retrouver :

- le contexte de la décision ;
- le problème à résoudre ;
- les contraintes importantes ;
- les principales solutions envisagées ;
- la solution retenue ;
- les raisons du choix ;
- les principales conséquences de la décision.

---

### 14.18 Choix restant à effectuer

À ce stade des spécifications techniques, les technologies ne sont pas considérées comme définitivement sélectionnées.

Les décisions à formaliser ultérieurement concernent notamment :

- l'architecture applicative ;
- les technologies utilisées pour construire l'interface ;
- les technologies utilisées pour la logique applicative ;
- le mécanisme de persistance ;
- le système de gestion des données ;
- le mécanisme d'authentification ;
- le mécanisme de communication entre composants ;
- la stratégie de conteneurisation éventuelle ;
- la solution d'hébergement ;
- la chaîne CI/CD ;
- les outils de test ;
- les outils de sécurité ;
- les mécanismes d'observabilité.

Ces décisions devront être prises à partir des exigences et des critères définis dans la documentation du projet.

---

## 15. Étude et choix de l'architecture applicative

Cette section analyse les principales architectures applicatives envisageables pour **Fidel Portfolio** afin d'identifier celle qui répond le mieux aux besoins et aux contraintes du projet.

Le choix de l'architecture ne doit pas être déterminé uniquement par les technologies envisagées. Il doit découler des besoins fonctionnels, des exigences non fonctionnelles, du niveau de complexité du projet et de ses perspectives d'évolution.

---

### 15.1 Besoins ayant un impact sur l'architecture

Plusieurs caractéristiques de la V1 influencent directement le choix de l'architecture.

L'application doit notamment permettre :

- la consultation publique du portfolio ;
- la consultation dynamique des projets ;
- la recherche et le filtrage des projets ;
- la consultation détaillée d'un projet ;
- l'authentification d'un administrateur ;
- la création, la consultation, la modification et la suppression des projets ;
- la persistance des données ;
- la séparation entre les fonctionnalités publiques et les fonctionnalités d'administration ;
- le déploiement reproductible de l'application ;
- l'intégration future d'une chaîne CI/CD ;
- la mise en œuvre de mesures de sécurité adaptées.

L'architecture doit également rester suffisamment simple pour être développée, testée, déployée et maintenue dans le cadre d'un projet individuel.

---

### 15.2 Architectures envisagées

Plusieurs modèles d'architecture peuvent répondre aux besoins du projet.

Les principales solutions étudiées sont :

1. application monolithique ;
2. application monolithique modulaire ;
3. architecture client-serveur avec séparation de l'interface et de la logique applicative ;
4. architecture en microservices.

Ces architectures ne constituent pas les seules architectures existantes, mais représentent les alternatives les plus pertinentes à étudier au regard du périmètre actuel du projet.

---

### 15.3 Application monolithique

Dans une architecture monolithique, les principales fonctionnalités de l'application sont regroupées au sein d'une même application déployable.

La présentation, la logique métier, l'accès aux données et les fonctionnalités d'administration peuvent appartenir au même ensemble applicatif.

#### Avantages

- architecture relativement simple ;
- nombre limité de composants à exploiter ;
- déploiement simplifié ;
- communication interne directe ;
- environnement de développement relativement facile à reproduire ;
- coût opérationnel limité.

#### Inconvénients

- couplage potentiellement important entre les différentes parties de l'application ;
- risque de dégradation de la maintenabilité si la structure interne n'est pas correctement organisée ;
- évolution indépendante des différentes parties plus difficile ;
- déploiement généralement réalisé pour l'ensemble de l'application.

Cette architecture peut répondre au périmètre de la V1 à condition de maintenir une séparation claire des responsabilités dans le code.

---

### 15.4 Monolithe modulaire

Le monolithe modulaire conserve une seule unité principale de déploiement tout en organisant l'application en modules disposant de responsabilités clairement définies.

Des modules peuvent par exemple être définis autour de domaines fonctionnels tels que :

- gestion des projets ;
- authentification ;
- administration ;
- présentation publique.

Les frontières exactes des modules seront déterminées lors de la conception détaillée.

#### Avantages

- complexité opérationnelle relativement faible ;
- séparation plus claire des responsabilités qu'un monolithe peu structuré ;
- facilité de développement et de déploiement ;
- possibilité de faire évoluer indépendamment la structure interne des modules ;
- préparation éventuelle à une séparation future de certains composants si un besoin réel apparaît.

#### Inconvénients

- les modules restent généralement déployés ensemble ;
- une mauvaise définition des frontières peut recréer un couplage important ;
- nécessite une discipline d'architecture afin de préserver les responsabilités de chaque module.

Cette approche constitue une évolution structurée du modèle monolithique sans introduire immédiatement la complexité d'un système distribué.

---

### 15.5 Architecture client-serveur avec séparation de l'interface et de la logique applicative

Une autre possibilité consiste à séparer l'interface utilisateur de la partie chargée de la logique applicative et de l'accès aux données.

L'application comporte alors au minimum :

- une application cliente chargée de l'interface utilisateur ;
- une application serveur exposant les fonctionnalités nécessaires à la manipulation des données et à l'administration.

Les deux parties communiquent à travers une interface définie entre elles.

#### Avantages

- séparation claire entre présentation et logique applicative ;
- possibilité de faire évoluer séparément les deux parties ;
- réutilisation potentielle des fonctionnalités serveur par d'autres clients ;
- séparation explicite des responsabilités ;
- possibilité de déployer indépendamment certaines parties.

#### Inconvénients

- plusieurs composants doivent être développés et exploités ;
- communication réseau à gérer ;
- configuration supplémentaire pour les environnements ;
- gestion de la sécurité des échanges ;
- déploiement potentiellement plus complexe qu'une application unique.

Cette solution peut être pertinente si les bénéfices liés à la séparation de l'interface et de la logique applicative justifient cette complexité supplémentaire.

---

### 15.6 Architecture en microservices

Une architecture en microservices consiste à répartir les responsabilités de l'application entre plusieurs services pouvant être développés, déployés et exploités de manière relativement indépendante.

Dans le contexte du portfolio, une telle architecture pourrait théoriquement séparer certains domaines fonctionnels.

Cependant, la définition de services ne doit pas être effectuée artificiellement uniquement pour appliquer une architecture microservices.

#### Avantages

- déploiement indépendant des services ;
- isolation de certaines responsabilités ;
- possibilité de faire évoluer certains composants indépendamment ;
- possibilité d'adapter les ressources selon les besoins propres à chaque service ;
- autonomie technologique possible entre certains services.

#### Inconvénients

- augmentation importante de la complexité opérationnelle ;
- multiplication des déploiements ;
- communications réseau supplémentaires ;
- gestion plus complexe des erreurs distribuées ;
- observabilité plus exigeante ;
- gestion des données potentiellement plus complexe ;
- sécurité interservices à prendre en compte ;
- tests d'intégration plus complexes ;
- coût d'infrastructure potentiellement supérieur.

Pour la V1, aucun besoin identifié ne nécessite actuellement le déploiement indépendant ou la mise à l'échelle indépendante de plusieurs domaines fonctionnels.

L'utilisation de microservices introduirait donc une complexité importante qui devrait être justifiée par d'autres objectifs mesurables avant d'être retenue.

---

### 15.7 Comparaison des architectures

Les architectures envisagées peuvent être comparées selon les critères définis précédemment.

| Critère | Monolithe | Monolithe modulaire | Client-serveur séparé | Microservices |
|---------|-----------|---------------------|-----------------------|---------------|
| Adéquation avec la V1 | Bonne | Très bonne | Très bonne | Possible |
| Complexité de développement | Faible | Faible à moyenne | Moyenne | Élevée |
| Complexité de déploiement | Faible | Faible | Moyenne | Élevée |
| Maintenabilité | Moyenne à bonne | Bonne | Bonne | Bonne si correctement maîtrisée |
| Séparation des responsabilités | Moyenne | Bonne | Très bonne | Très bonne |
| Testabilité | Bonne | Bonne | Bonne | Plus complexe |
| Coût opérationnel | Faible | Faible | Faible à moyen | Moyen à élevé |
| Besoin en observabilité | Faible | Faible | Moyen | Élevé |
| Gestion des communications réseau | Faible | Faible | Nécessaire | Importante |
| Adaptation au périmètre actuel | Bonne | Très bonne | Très bonne | Faible |
| Facilité d'évolution | Moyenne | Bonne | Bonne | Très bonne pour certains scénarios |
| Risque de surarchitecture | Faible | Faible | Moyen | Élevé |

Cette comparaison ne signifie pas qu'une architecture est intrinsèquement meilleure qu'une autre.

Elle évalue leur adéquation avec les besoins actuellement identifiés pour **Fidel Portfolio**.

---

### 15.8 Architecture retenue

Pour la V1, une architecture **client-serveur avec séparation de l'interface utilisateur et de la logique applicative**, organisée de manière modulaire, est retenue.

L'application sera donc structurée autour de deux ensembles applicatifs principaux :

- une partie cliente chargée de l'interface et des interactions avec l'utilisateur ;
- une partie serveur chargée de la logique applicative, de l'authentification, de la gestion des projets et de l'accès aux données.

La partie serveur devra elle-même être organisée selon une séparation claire des responsabilités afin d'éviter la création d'un bloc applicatif difficile à maintenir.

Le choix d'une architecture en microservices n'est pas retenu pour la V1.

Aucun besoin actuel ne justifie notamment :

- une mise à l'échelle indépendante de plusieurs services ;
- des cycles de déploiement indépendants pour plusieurs domaines ;
- une forte distribution des traitements ;
- une organisation composée de plusieurs équipes autonomes.

La complexité supplémentaire introduite par les microservices serait donc disproportionnée par rapport au périmètre actuel.

---

### 15.9 Justification du choix

L'architecture retenue répond notamment aux besoins suivants :

| Besoin / exigence | Contribution de l'architecture |
|-------------------|--------------------------------|
| Gestion dynamique des projets | La partie serveur centralise la logique de gestion et la persistance. |
| Administration sécurisée | Les opérations d'administration peuvent être contrôlées côté serveur. |
| Maintenabilité | Les responsabilités entre interface, logique applicative et données peuvent être séparées. |
| Évolutivité | Les différentes parties peuvent évoluer sans imposer immédiatement une architecture distribuée complexe. |
| Testabilité | Les responsabilités peuvent être testées à différents niveaux. |
| Sécurité | Les opérations sensibles et l'accès aux données ne reposent pas uniquement sur l'application cliente. |
| Déploiement | Le nombre de composants reste limité et compatible avec le périmètre du projet. |
| Coût | L'architecture ne nécessite pas la multiplication de services d'infrastructure. |

Le choix cherche ainsi un compromis entre **séparation des responsabilités, maintenabilité, sécurité, évolutivité et simplicité opérationnelle**.

---

### 15.10 Conséquences du choix

L'adoption de cette architecture implique notamment :

- la définition d'une interface de communication entre la partie cliente et la partie serveur ;
- la définition d'un modèle de données persistant ;
- la mise en place d'un mécanisme d'authentification pour l'administration ;
- la sécurisation des opérations de création, modification et suppression ;
- la gestion des erreurs de communication entre les composants ;
- la configuration des différents environnements ;
- la définition d'une stratégie de déploiement adaptée aux deux parties.

Elle implique également que les technologies utilisées pour chaque partie devront être sélectionnées séparément selon leurs propres contraintes.

---

### 15.11 Évolution éventuelle de l'architecture

L'architecture retenue pour la V1 ne constitue pas une contrainte définitive pour les versions futures.

Une évolution pourra être étudiée si de nouveaux besoins apparaissent, par exemple :

- augmentation importante de la charge ;
- apparition de domaines métier indépendants ;
- besoin de déploiements indépendants ;
- intégration de nouveaux consommateurs des services ;
- traitements nécessitant une mise à l'échelle spécifique ;
- évolution importante de l'organisation du projet.

Une migration vers une architecture plus distribuée devra être motivée par des besoins identifiés et non par la seule volonté d'utiliser une architecture particulière.

---

## 16. Décomposition des composants et responsabilités

Cette section précise la répartition des responsabilités entre les principaux composants de l'architecture retenue pour la V1 de **Fidel Portfolio**.

L'objectif est de garantir une séparation claire des rôles afin de favoriser la maintenabilité, la testabilité, la sécurité et l'évolutivité de l'application.

La décomposition présentée dans cette section reste indépendante des technologies qui seront utilisées pour implémenter chaque composant.

---

### 16.1 Composants principaux

L'architecture retenue repose sur plusieurs responsabilités principales :

- interface utilisateur publique ;
- interface d'administration ;
- logique applicative ;
- authentification et autorisation ;
- gestion des projets ;
- accès aux données persistantes ;
- mécanismes de validation ;
- gestion des ressources associées aux projets ;
- journalisation et gestion des erreurs.

Ces responsabilités pourront être regroupées dans un nombre limité de composants déployables tout en conservant une séparation logique claire.

---

### 16.2 Interface publique

L'interface publique est responsable de la présentation du portfolio aux visiteurs.

Elle doit notamment permettre :

- l'affichage de la page d'accueil ;
- la présentation du profil professionnel ;
- l'affichage de la liste des projets ;
- l'affichage détaillé d'un projet ;
- la recherche des projets ;
- le filtrage des projets ;
- l'accès aux liens et ressources externes ;
- la prise de contact ;
- le changement de thème ;
- l'adaptation de l'affichage aux différentes tailles d'écran.

L'interface publique ne doit pas permettre directement l'exécution d'opérations réservées à l'administration.

---

### 16.3 Interface d'administration

L'interface d'administration permet au propriétaire du portfolio de gérer les projets.

Elle doit notamment permettre :

- l'authentification de l'administrateur ;
- la consultation des projets administrables ;
- la création d'un projet ;
- la modification d'un projet ;
- la suppression d'un projet ;
- la gestion des informations associées aux projets ;
- la déconnexion.

L'interface d'administration ne doit pas constituer à elle seule le mécanisme de protection des opérations sensibles.

Les contrôles d'authentification, d'autorisation et de validation doivent également être appliqués par les composants responsables de l'exécution de ces opérations.

---

### 16.4 Logique applicative

La logique applicative regroupe les traitements nécessaires au fonctionnement de l'application indépendamment de leur représentation dans l'interface utilisateur.

Elle doit notamment permettre :

- de traiter les demandes provenant des interfaces ;
- d'appliquer les règles fonctionnelles ;
- de valider les opérations demandées ;
- de coordonner l'accès aux données ;
- de gérer les principaux cas d'erreur ;
- de retourner les résultats nécessaires aux interfaces.

La logique applicative ne doit pas dépendre inutilement des détails de présentation de l'interface utilisateur.

---

### 16.5 Module de gestion des projets

La gestion des projets constitue l'un des domaines fonctionnels principaux de la V1.

Le composant ou module concerné doit notamment gérer :

- la récupération de la liste des projets ;
- la récupération d'un projet ;
- la création d'un projet ;
- la modification d'un projet ;
- la suppression d'un projet ;
- la validation des informations associées ;
- la gestion des relations avec les catégories et technologies ;
- la mise à disposition des informations nécessaires à la partie publique.

Les règles métier associées aux projets doivent être appliquées indépendamment de l'interface depuis laquelle l'opération est déclenchée.

---

### 16.6 Authentification

Le mécanisme d'authentification est responsable de la vérification de l'identité de l'administrateur.

Il doit notamment permettre :

- de recevoir les informations nécessaires à l'authentification ;
- de vérifier leur validité ;
- de refuser une authentification invalide ;
- d'établir un contexte d'authentification après une authentification réussie ;
- de permettre la fin de ce contexte lors de la déconnexion.

Les modalités précises de gestion de l'authentification dépendront du mécanisme retenu lors de la conception de la sécurité.

---

### 16.7 Autorisation

Le contrôle d'autorisation doit permettre de déterminer si une opération peut être exécutée par l'utilisateur concerné.

Pour la V1 :

- les fonctionnalités publiques sont accessibles sans authentification ;
- les opérations d'administration sont réservées à l'administrateur autorisé.

Les contrôles d'autorisation doivent être réalisés au niveau du composant responsable de l'opération protégée.

L'absence d'un bouton ou d'un écran dans l'interface ne doit jamais être considérée comme un mécanisme suffisant d'autorisation.

---

### 16.8 Validation des données

Un composant ou mécanisme clairement identifié doit assurer la validation des données reçues avant leur traitement ou leur persistance.

La validation doit notamment prendre en compte :

- les données obligatoires ;
- les types attendus ;
- les formats ;
- les valeurs autorisées ;
- les relations entre les données ;
- les règles métier applicables.

Les données invalides doivent être rejetées avant toute modification persistante.

---

### 16.9 Accès aux données

L'accès au mécanisme de persistance doit être isolé des interfaces utilisateur.

Le composant responsable de l'accès aux données doit permettre aux autres parties de l'application d'effectuer les opérations nécessaires sans dépendre directement des détails du stockage.

Il doit notamment prendre en charge :

- la lecture ;
- la création ;
- la modification ;
- la suppression ;
- la récupération des relations nécessaires ;
- l'application des contraintes de persistance lorsque cela relève de sa responsabilité.

Cette séparation doit faciliter une éventuelle évolution du mécanisme de stockage.

---

### 16.10 Gestion des catégories et technologies

Les catégories et technologies constituent des données réutilisées par plusieurs projets.

Le système doit permettre :

- d'associer plusieurs catégories à un projet ;
- d'associer plusieurs technologies à un projet ;
- de réutiliser une même catégorie ou technologie pour plusieurs projets ;
- d'éviter les duplications inutiles lorsque le modèle de données retenu permet de les prévenir.

Les responsabilités exactes liées à leur création, modification ou suppression seront précisées lors de la conception fonctionnelle et du modèle de données si leur gestion dynamique est intégrée à la V1.

---

### 16.11 Gestion des ressources visuelles

Les ressources visuelles associées aux projets doivent être gérées séparément des données descriptives lorsqu'elles nécessitent un mécanisme de stockage spécifique.

Le composant concerné devra permettre :

- d'associer une ressource à un projet ;
- de récupérer les informations nécessaires à son affichage ;
- de supprimer ou remplacer une ressource lorsque cela est nécessaire ;
- d'éviter l'exposition de ressources non destinées à être publiques.

Le mécanisme concret de stockage des fichiers sera déterminé en fonction de l'architecture et de l'hébergement retenus.

---

### 16.12 Gestion des erreurs

Les composants doivent gérer les erreurs de manière cohérente.

Le système doit permettre de distinguer notamment :

- les erreurs de validation ;
- les erreurs d'authentification ;
- les erreurs d'autorisation ;
- les ressources inexistantes ;
- les erreurs liées à la persistance ;
- les erreurs techniques internes.

Les informations destinées à l'utilisateur doivent rester compréhensibles et ne doivent pas exposer de détails techniques sensibles.

Les informations nécessaires au diagnostic doivent pouvoir être journalisées.

---

### 16.13 Journalisation

Les composants responsables des opérations importantes doivent pouvoir produire des événements de journalisation adaptés.

La journalisation doit notamment permettre de suivre :

- les erreurs applicatives ;
- les échecs d'authentification ;
- les opérations d'administration importantes ;
- les problèmes d'accès aux données ;
- les événements nécessaires au diagnostic technique.

La journalisation ne doit pas inclure inutilement de secrets ou d'informations sensibles.

---

### 16.14 Dépendances entre composants

Les dépendances entre composants doivent être limitées aux besoins réellement nécessaires au fonctionnement de l'application.

Une dépendance doit être orientée de manière à éviter qu'un composant de bas niveau dépende inutilement d'un composant de présentation.

La structure retenue devra favoriser :

- un couplage limité ;
- des responsabilités clairement identifiées ;
- la possibilité de tester les composants indépendamment lorsque cela est pertinent ;
- la possibilité de remplacer ou faire évoluer un composant sans remise en cause globale de l'application.

La structure exacte des dépendances sera définie dans la conception détaillée de l'architecture.

---

### 16.15 Vue logique simplifiée

La répartition logique des responsabilités peut être représentée de manière simplifiée comme suit :

`Utilisateur`
↓  
`Interface publique / Interface d'administration`
↓  
`Logique applicative`
↓  
`Modules métier`
↓  
`Accès aux données`
↓  
`Mécanisme de persistance`

Des composants transverses peuvent intervenir à plusieurs niveaux, notamment :

- authentification ;
- autorisation ;
- validation ;
- journalisation ;
- gestion des erreurs ;
- sécurité.

Cette représentation est une vue logique et ne définit pas à elle seule le nombre de processus, de services ou d'unités de déploiement.

---

### 16.16 Évolution de la décomposition

La décomposition des composants pourra évoluer au cours du projet si de nouveaux besoins ou contraintes apparaissent.

Une responsabilité pourra être isolée dans un composant indépendant lorsque cela apporte un bénéfice identifiable en matière de :

- maintenabilité ;
- sécurité ;
- performance ;
- déploiement ;
- évolutivité ;
- exploitation.

Toute séparation supplémentaire entraînant une augmentation significative de la complexité devra être justifiée par un besoin réel.

---

## 17. Organisation interne de la partie serveur

Cette section étudie l'organisation interne de la partie serveur de **Fidel Portfolio**.

L'objectif est de définir une structure permettant de séparer clairement les responsabilités liées à la logique métier, aux traitements applicatifs, à la persistance et aux interfaces techniques, tout en conservant une complexité adaptée au périmètre de la V1.

Le choix de cette organisation reste indépendant du langage et du framework qui seront utilisés.

---

### 17.1 Responsabilités à organiser

La partie serveur devra notamment prendre en charge :

- l'authentification de l'administrateur ;
- l'autorisation des opérations protégées ;
- la gestion des projets ;
- la validation des données ;
- l'application des règles métier ;
- l'accès aux données persistantes ;
- la gestion des erreurs ;
- la journalisation des événements pertinents ;
- la mise à disposition des fonctionnalités nécessaires à la partie cliente.

Ces responsabilités doivent être séparées suffisamment pour éviter qu'un même composant concentre la présentation technique, la logique métier et l'accès aux données.

---

### 17.2 Architecture en couches

Une architecture en couches organise généralement l'application selon plusieurs niveaux de responsabilité.

Une organisation possible serait :

`Interface / Entrées`
↓  
`Logique applicative`
↓  
`Logique métier`
↓  
`Accès aux données`

#### Avantages

- structure relativement simple à comprendre ;
- séparation claire des responsabilités ;
- adaptée à une application CRUD ;
- facilité de test ;
- bonne compatibilité avec de nombreux frameworks ;
- complexité limitée pour une V1.

#### Inconvénients

- risque de couplage important entre les couches si les dépendances ne sont pas maîtrisées ;
- possibilité de créer des couches très dépendantes du framework ou du mécanisme de persistance ;
- risque de logique métier dispersée si les responsabilités sont mal définies.

---

### 17.3 Architecture hexagonale

L'architecture hexagonale vise à isoler la logique métier des technologies externes.

Le cœur applicatif communique avec les éléments extérieurs par l'intermédiaire de ports et d'adaptateurs.

Une représentation simplifiée serait :

`Interface utilisateur / API`
↓
`Adaptateur entrant`
↓
`Application / Domaine`
↓
`Port`
↓
`Adaptateur de persistance`
↓
`Stockage`

L'application métier ne dépend donc pas directement de la technologie utilisée pour le stockage ou pour les communications.

#### Avantages

- forte séparation entre logique métier et infrastructure ;
- bonne testabilité ;
- remplacement plus facile de certains composants techniques ;
- limitation du couplage avec les frameworks ;
- architecture adaptée à l'évolution du projet.

#### Inconvénients

- davantage d'abstractions ;
- nombre de fichiers et d'interfaces potentiellement plus important ;
- apprentissage plus important ;
- risque de complexité excessive pour une application de petite taille si elle est appliquée de manière trop stricte.

---

### 17.4 Clean Architecture

La Clean Architecture poursuit un objectif proche de l'architecture hexagonale : maintenir les règles métier indépendantes des technologies externes.

Les dépendances doivent principalement être dirigées vers le cœur de l'application.

Une organisation conceptuelle peut distinguer :

- les entités métier ;
- les cas d'utilisation ;
- les adaptateurs ;
- les composants techniques externes.

#### Avantages

- forte indépendance de la logique métier ;
- bonne testabilité ;
- responsabilités clairement séparées ;
- limitation de la dépendance aux frameworks et à la persistance.

#### Inconvénients

- structure plus complexe ;
- nombreuses abstractions possibles ;
- risque de surarchitecture pour une application dont le domaine métier reste limité.

---

### 17.5 Comparaison

| Critère | Architecture en couches | Hexagonale | Clean Architecture |
|---------|-------------------------|------------|--------------------|
| Simplicité | Très bonne | Moyenne | Moyenne |
| Séparation des responsabilités | Bonne | Très bonne | Très bonne |
| Testabilité | Bonne | Très bonne | Très bonne |
| Indépendance du framework | Moyenne | Très bonne | Très bonne |
| Indépendance de la persistance | Moyenne | Très bonne | Très bonne |
| Adaptation au CRUD de la V1 | Très bonne | Bonne | Bonne |
| Complexité de mise en œuvre | Faible | Moyenne | Moyenne à élevée |
| Risque de surarchitecture | Faible | Moyen | Moyen à élevé |
| Évolutivité | Bonne | Très bonne | Très bonne |

---

### 17.6 Organisation retenue

Pour la V1 de **Fidel Portfolio**, une organisation **modulaire en couches avec séparation explicite de la logique métier et de l'infrastructure** est retenue.

Cette organisation vise à conserver la simplicité d'une architecture en couches tout en appliquant certains principes issus des architectures hexagonale et Clean Architecture.

La partie serveur devra notamment distinguer :

- les interfaces d'entrée ;
- les cas d'utilisation applicatifs ;
- les règles et objets métier ;
- les mécanismes d'accès aux données ;
- les composants techniques externes.

La V1 ne nécessite pas l'application stricte de toutes les abstractions d'une architecture hexagonale ou Clean Architecture.

Les abstractions devront être introduites lorsqu'elles permettent réellement :

- de réduire le couplage ;
- d'améliorer la testabilité ;
- de protéger la logique métier des détails techniques ;
- de faciliter une évolution raisonnablement prévisible.

---

### 17.7 Organisation logique proposée

La structure logique pourra suivre le principe suivant :

`Interface technique`
↓
`Application / Cas d'utilisation`
↓
`Domaine`
↓
`Abstractions d'accès aux ressources`

Les composants techniques externes viennent implémenter les abstractions nécessaires :

`Persistance`
`Authentification`
`Journalisation`
`Services externes`

La direction exacte des dépendances sera précisée dans la documentation d'architecture.

---

### 17.8 Couche d'interface

La couche d'interface est responsable de la réception des demandes provenant de l'extérieur de la partie serveur.

Elle doit notamment :

- recevoir les demandes ;
- extraire les données nécessaires ;
- déclencher le cas d'utilisation correspondant ;
- transmettre le résultat ;
- transformer les erreurs applicatives en réponses adaptées au mécanisme de communication retenu.

Elle ne doit pas contenir la logique métier principale.

---

### 17.9 Couche applicative

La couche applicative orchestre les cas d'utilisation de l'application.

Elle pourra notamment gérer les opérations suivantes :

- consulter les projets ;
- consulter un projet ;
- créer un projet ;
- modifier un projet ;
- supprimer un projet ;
- authentifier l'administrateur ;
- terminer une session d'administration.

Cette couche coordonne les différents éléments nécessaires à l'exécution d'un cas d'utilisation sans dépendre inutilement des détails de l'interface utilisateur.

---

### 17.10 Domaine

Le domaine regroupe les concepts et règles métier propres au portfolio.

Il pourra notamment représenter :

- un projet ;
- une catégorie ;
- une technologie ;
- les règles nécessaires à la validité d'un projet ;
- les relations entre ces éléments.

Le domaine doit rester aussi indépendant que possible des détails liés :

- au stockage ;
- au protocole de communication ;
- au framework ;
- à l'hébergement.

---

### 17.11 Infrastructure

L'infrastructure regroupe les éléments techniques nécessaires au fonctionnement de l'application mais qui ne constituent pas directement sa logique métier.

Elle pourra notamment comprendre :

- le mécanisme de persistance ;
- les adaptateurs d'accès aux données ;
- les mécanismes d'authentification ;
- la journalisation ;
- l'accès aux éventuels services externes ;
- la gestion technique des fichiers.

Les composants d'infrastructure doivent être remplaçables dans une mesure raisonnable sans nécessiter une réécriture importante de la logique métier.

---

### 17.12 Règle de dépendance

Les composants contenant les règles métier ne doivent pas dépendre directement des détails techniques lorsque cette dépendance peut être évitée raisonnablement.

La direction recherchée est :

`Infrastructure → Application / Domaine`

et non :

`Domaine → technologie de persistance`

Par exemple, les règles définissant la validité d'un projet ne doivent pas dépendre directement du système de gestion de données finalement choisi.

---

### 17.13 Conséquences du choix

Cette organisation implique notamment :

- une séparation entre logique métier et logique technique ;
- des cas d'utilisation clairement identifiés ;
- une couche dédiée aux interactions externes ;
- une abstraction raisonnable de l'accès aux données ;
- la possibilité de tester la logique métier sans dépendre systématiquement de l'infrastructure réelle ;
- une discipline dans la direction des dépendances.

Elle ne nécessite pas de multiplier artificiellement les couches, interfaces ou abstractions lorsque celles-ci n'apportent aucun bénéfice au projet.