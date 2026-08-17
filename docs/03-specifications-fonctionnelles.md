# Spécifications fonctionnelles

| Élément | Valeur |
|---------|--------|
| Projet | Fidel Portfolio |
| Document | Spécifications fonctionnelles |
| Version | 1.0 |
| Auteur | Fidel Nziengui Ateba |
| Statut | En cours de rédaction |
| Dernière mise à jour | 17/08/2026 |

---

← [Cahier des charges](02-cahier-des-charges.md) | [Spécifications techniques →](04-specifications-techniques.md)

## Sommaire

1. [Introduction](#1-introduction)
2. [Acteurs](#2-acteurs)
3. [Vue d'ensemble fonctionnelle](#3-vue-densemble-fonctionnelle)
4. [Parcours utilisateurs](#4-parcours-utilisateurs)
5. [User Stories](#5-user-stories)
6. [Spécifications des fonctionnalités](#6-spécifications-des-fonctionnalités)
7. [Règles métier](#7-règles-métier)
8. [Cas particuliers et gestion des erreurs](#8-cas-particuliers-et-gestion-des-erreurs)
9. [Traçabilité](#9-traçabilité)
10. [Documents liés](#10-documents-liés)

---

## 1. Introduction

### 1.1 Objet du document

Ce document décrit les spécifications fonctionnelles du projet **Fidel Portfolio**.

Il traduit les besoins et les exigences fonctionnelles définis lors des phases de cadrage en comportements attendus de l'application.

Il précise notamment les fonctionnalités accessibles aux utilisateurs, les parcours de navigation, les règles de fonctionnement ainsi que les comportements attendus dans les différents cas d'utilisation.

### 1.2 Objectifs

Les spécifications fonctionnelles ont pour objectifs de :

- définir précisément le comportement attendu de l'application ;
- formaliser les interactions entre les utilisateurs et le portfolio ;
- servir de référence lors de la conception et du développement ;
- permettre la définition ultérieure des cas de test ;
- assurer la traçabilité entre les besoins, les exigences, les fonctionnalités et les tests.

### 1.3 Périmètre

Ce document couvre les fonctionnalités prévues pour la **version 1 (V1)** de Fidel Portfolio.

Il porte notamment sur :

- la consultation de la page d'accueil ;
- la consultation des projets ;
- la consultation détaillée d'un projet ;
- la recherche et le filtrage des projets ;
- l'accès aux liens externes ;
- la prise de contact ;
- la gestion du thème clair ou sombre ;
- les principaux comportements de navigation et d'interface.

Les choix d'implémentation, de technologies, d'infrastructure et d'architecture ne sont pas définis dans ce document. Ils seront traités dans les documents techniques correspondants.

---

## 2. Acteurs

Cette section identifie les différents types d'utilisateurs susceptibles d'interagir avec l'application.

La V1 du portfolio ne prévoit pas de système d'authentification ni de gestion de comptes utilisateurs. Les acteurs accèdent donc aux fonctionnalités publiques de l'application sans authentification.

### 2.1 Visiteur

Le **visiteur** représente l'acteur principal de l'application.

Il peut notamment :

- consulter la page d'accueil ;
- découvrir le profil et le positionnement professionnel du développeur ;
- accéder à la liste des projets ;
- rechercher des projets à l'aide de mots-clés ;
- filtrer les projets par catégorie ;
- consulter la présentation détaillée d'un projet ;
- accéder à une démonstration lorsqu'elle est disponible ;
- accéder au dépôt d'un projet lorsque celui-ci est public ;
- accéder aux profils externes proposés, notamment GitHub et LinkedIn ;
- contacter le développeur par courrier électronique ;
- choisir entre le thème clair et le thème sombre.

### 2.2 Recruteur ou responsable technique

Le **recruteur ou responsable technique** constitue un profil particulier de visiteur dont l'objectif principal est d'évaluer le profil professionnel du développeur.

Il doit notamment pouvoir :

- identifier rapidement les domaines de compétences ;
- consulter les technologies utilisées ;
- examiner les réalisations présentées ;
- comprendre les objectifs et le contexte des projets ;
- comprendre la méthodologie suivie ;
- identifier les difficultés rencontrées et les solutions apportées ;
- consulter les résultats obtenus ;
- accéder aux ressources publiques associées aux projets lorsqu'elles sont disponibles.

### 2.3 Client potentiel

Le **client potentiel** consulte le portfolio afin d'évaluer la capacité du développeur à répondre à un besoin ou à participer à un projet.

Il doit notamment pouvoir :

- consulter les réalisations ;
- identifier les compétences mobilisées ;
- comprendre la démarche adoptée sur les projets ;
- consulter les résultats présentés ;
- contacter facilement le développeur.

### 2.4 Synthèse des acteurs

| Acteur | Objectif principal | Authentification |
|--------|--------------------|------------------|
| Visiteur | Découvrir le profil, les compétences et les projets. | Non |
| Recruteur / Responsable technique | Évaluer les compétences, réalisations et méthodes de travail. | Non |
| Client potentiel | Évaluer les réalisations avant une éventuelle prise de contact. | Non |

---

## 3. Vue d'ensemble fonctionnelle

La V1 de **Fidel Portfolio** permet à un visiteur de découvrir le profil professionnel du développeur, d'explorer ses réalisations et d'identifier les compétences et méthodes mobilisées dans ses différents projets.

L'application est organisée autour de plusieurs blocs fonctionnels complémentaires.

### 3.1 Accueil

La page d'accueil constitue le point d'entrée principal du portfolio.

Elle doit permettre au visiteur de :

- identifier rapidement le développeur ;
- comprendre son positionnement professionnel ;
- obtenir une première vision de ses domaines de compétences ;
- accéder à la présentation des projets grâce à un appel à l'action **« Découvrir mes projets »** ;
- accéder aux principaux moyens de contact et profils externes proposés.

La page d'accueil privilégie une présentation visuelle du profil. Les projets ne sont pas directement présentés sur cette page afin de conserver une séparation claire entre la présentation du développeur et la consultation de ses réalisations.

### 3.2 Consultation des projets

Une page dédiée permet au visiteur de consulter l'ensemble des projets présentés dans le portfolio.

Les projets sont affichés sous forme de cartes synthétiques.

Chaque carte présente au minimum :

- le titre du projet ;
- un résumé ;
- les principales technologies utilisées ;
- la ou les catégories associées ;
- un accès à la présentation détaillée du projet.

Les projets peuvent notamment être associés aux catégories suivantes :

- Développement ;
- DevOps ;
- DevSecOps ;
- Cloud ;
- Autres.

Un même projet peut être associé à plusieurs catégories lorsque cela est pertinent.

### 3.3 Consultation détaillée d'un projet

Chaque projet dispose d'une page de présentation dédiée.

Cette page permet au visiteur de comprendre le projet au-delà de sa simple description.

Elle peut notamment présenter :

- le contexte du projet ;
- son objectif ;
- sa description ;
- les technologies et outils utilisés ;
- la méthodologie suivie ;
- les principales étapes de réalisation ;
- les difficultés rencontrées ;
- les solutions apportées ;
- les résultats obtenus ;
- des schémas, captures ou autres éléments visuels pertinents.

Lorsque le projet dispose d'une démonstration publique, un accès à celle-ci peut être proposé.

Lorsque le dépôt de code source est public, un lien vers celui-ci peut également être proposé.

Lorsqu'un projet ou son code source ne peut pas être rendu public, l'interface doit l'indiquer clairement, par exemple à l'aide d'une mention **« Dépôt privé »** ou **« Code non public »**, sans exposer d'informations confidentielles.

### 3.4 Recherche de projets

La page des projets propose un système de recherche par mots-clés.

Le visiteur peut saisir un ou plusieurs termes afin d'identifier les projets correspondant à sa recherche.

La recherche peut s'appuyer sur les informations associées aux projets, notamment :

- le titre ;
- la description ;
- les technologies ;
- les catégories ;
- les mots-clés associés au projet.

La liste affichée est actualisée afin de ne présenter que les projets correspondant à la recherche.

Lorsqu'aucun projet ne correspond aux critères saisis, l'application affiche un message indiquant :

**« Aucun projet correspondant. »**

Le visiteur doit alors pouvoir réinitialiser sa recherche.

### 3.5 Filtrage des projets

Le visiteur peut filtrer les projets selon leur catégorie.

Les catégories prévues pour la V1 comprennent notamment :

- Développement ;
- DevOps ;
- DevSecOps ;
- Cloud ;
- Autres.

Le filtrage permet de réduire la liste des projets affichés sans modifier leur contenu.

Le visiteur doit pouvoir réinitialiser les filtres afin d'afficher de nouveau l'ensemble des projets.

### 3.6 Liens externes et ressources

Le portfolio peut proposer des accès vers des ressources externes associées au développeur ou aux projets.

Ces ressources comprennent notamment :

- le profil GitHub ;
- le profil LinkedIn ;
- les dépôts publics associés aux projets ;
- les démonstrations publiques disponibles.

L'absence d'une ressource publique ne doit pas empêcher la consultation de la présentation détaillée du projet.

### 3.7 Contact

Le portfolio permet au visiteur de contacter le développeur sans nécessiter de compte utilisateur ni de formulaire de contact.

Une action **« Me contacter »** permet d'ouvrir le client de messagerie configuré sur l'appareil du visiteur.

Cette action peut préparer automatiquement :

- l'adresse électronique du destinataire ;
- l'objet du message ;
- éventuellement un contenu initial.

Le visiteur reste libre de modifier le contenu du courrier électronique avant son envoi.

### 3.8 Gestion du thème

L'application propose au minimum deux modes d'affichage :

- thème clair ;
- thème sombre.

Le visiteur peut basculer entre les deux modes.

Le choix effectué doit être mémorisé afin que le thème sélectionné puisse être restauré lors d'une visite ultérieure depuis le même environnement.

### 3.9 Adaptation aux différents écrans

Les fonctionnalités de la V1 doivent être utilisables aussi bien sur ordinateur que sur appareil mobile.

La présentation s'adapte à la taille de l'écran tout en conservant :

- l'accès aux principales fonctionnalités ;
- la lisibilité du contenu ;
- la navigation ;
- la recherche et les filtres ;
- la consultation des projets ;
- les actions de contact et les liens externes.

### 3.10 Animations et transitions

L'interface peut utiliser des animations afin d'améliorer la présentation et de valoriser l'expérience utilisateur.

Elles peuvent notamment concerner :

- les transitions entre certains états de l'interface ;
- l'apparition progressive de contenus ;
- les éléments apparaissant lors du défilement ;
- les interactions avec certains composants.

Les animations ne doivent pas empêcher ou ralentir l'accès aux informations et fonctionnalités principales.

### 3.11 Synthèse fonctionnelle

| ID | Bloc fonctionnel | Fonction principale |
|----|------------------|---------------------|
| BF-001 | Accueil | Présenter le profil et orienter le visiteur vers les projets. |
| BF-002 | Projets | Présenter l'ensemble des réalisations. |
| BF-003 | Détail d'un projet | Présenter en profondeur une réalisation et la démarche suivie. |
| BF-004 | Recherche | Rechercher des projets à partir de mots-clés. |
| BF-005 | Filtrage | Filtrer les projets selon leur catégorie. |
| BF-006 | Ressources externes | Accéder aux profils, dépôts et démonstrations publics. |
| BF-007 | Contact | Permettre la prise de contact par courrier électronique. |
| BF-008 | Thème | Basculer entre les thèmes clair et sombre et conserver la préférence. |
| BF-009 | Responsive | Permettre l'utilisation du portfolio sur différentes tailles d'écran. |
| BF-010 | Animations | Enrichir l'expérience visuelle sans nuire à l'utilisation. |

---

## 4. Parcours utilisateurs

Cette section décrit les principaux parcours permettant aux visiteurs d'atteindre leurs objectifs dans l'application.

Les parcours doivent rester simples et limiter le nombre d'actions nécessaires pour accéder aux informations essentielles.

### 4.1 Découverte du profil

**Objectif :** permettre à un visiteur de comprendre rapidement le positionnement professionnel du développeur.

**Parcours :**

1. Le visiteur accède à la page d'accueil.
2. Il découvre la présentation du développeur et son positionnement professionnel.
3. Il identifie les principaux domaines de compétences présentés.
4. Il peut accéder aux profils externes proposés, notamment GitHub et LinkedIn.
5. Il peut poursuivre sa visite en sélectionnant l'action **« Découvrir mes projets »**.

**Résultat attendu :** le visiteur dispose d'une première compréhension du profil et peut accéder facilement aux réalisations.

---

### 4.2 Découverte des projets

**Objectif :** permettre au visiteur de parcourir les réalisations du développeur.

**Parcours :**

1. Depuis la page d'accueil, le visiteur sélectionne **« Découvrir mes projets »**.
2. L'application affiche la page regroupant les projets.
3. Le visiteur consulte les différentes cartes présentées.
4. Chaque carte lui permet d'identifier le titre, le résumé, les technologies et les catégories associées au projet.
5. Le visiteur sélectionne **« Voir le détail »** sur le projet qui l'intéresse.
6. L'application affiche la page détaillée correspondante.

**Résultat attendu :** le visiteur peut passer rapidement d'une présentation générale des réalisations à l'étude détaillée d'un projet.

---

### 4.3 Consultation détaillée d'un projet

**Objectif :** permettre au visiteur d'évaluer une réalisation et de comprendre la démarche suivie.

**Parcours :**

1. Le visiteur sélectionne un projet depuis la liste des projets.
2. L'application affiche sa page détaillée.
3. Le visiteur peut consulter notamment :
   - le contexte ;
   - l'objectif ;
   - la description du projet ;
   - les technologies et outils utilisés ;
   - la méthodologie suivie ;
   - les principales étapes de réalisation ;
   - les difficultés rencontrées ;
   - les solutions apportées ;
   - les résultats obtenus ;
   - les éventuels schémas ou captures disponibles.
4. Si une démonstration publique existe, le visiteur peut sélectionner **« Voir la démo »**.
5. Si le dépôt est public, le visiteur peut sélectionner **« Voir le dépôt »**.
6. Si le dépôt ou le code n'est pas public, l'application affiche une indication telle que **« Dépôt privé »** ou **« Code non public »**.

**Résultat attendu :** le visiteur peut comprendre non seulement ce qui a été réalisé, mais également les compétences et la démarche mobilisées pour réaliser le projet.

---

### 4.4 Recherche d'un projet

**Objectif :** permettre au visiteur d'identifier rapidement les projets correspondant à un sujet, une technologie ou un mot-clé.

**Parcours :**

1. Le visiteur accède à la page des projets.
2. Il saisit un mot-clé dans le champ de recherche.
3. L'application recherche les correspondances dans les informations associées aux projets.
4. La liste des projets affichés est adaptée aux résultats obtenus.
5. Le visiteur peut sélectionner un projet correspondant pour consulter son détail.

Si aucune correspondance n'est trouvée :

1. L'application affiche **« Aucun projet correspondant. »**
2. Une action permettant de réinitialiser la recherche est proposée.
3. Le visiteur peut revenir à la liste complète des projets.

**Résultat attendu :** le visiteur peut retrouver une réalisation pertinente sans devoir parcourir manuellement l'ensemble des projets.

---

### 4.5 Filtrage des projets

**Objectif :** permettre au visiteur de consulter les projets appartenant à un domaine particulier.

**Parcours :**

1. Le visiteur accède à la page des projets.
2. Il sélectionne une catégorie, par exemple :
   - Développement ;
   - DevOps ;
   - DevSecOps ;
   - Cloud ;
   - Autres.
3. L'application affiche les projets correspondant au filtre sélectionné.
4. Le visiteur peut consulter le détail d'un projet.
5. Il peut réinitialiser le filtre afin d'afficher de nouveau l'ensemble des projets.

**Résultat attendu :** le visiteur peut cibler rapidement les réalisations correspondant au domaine qu'il souhaite évaluer.

---

### 4.6 Prise de contact

**Objectif :** permettre au visiteur de contacter facilement le développeur.

**Parcours :**

1. Le visiteur sélectionne l'action **« Me contacter »**.
2. L'application déclenche l'ouverture du client de messagerie configuré sur son appareil.
3. L'adresse électronique du développeur est automatiquement renseignée.
4. Un objet et éventuellement un contenu initial peuvent être proposés.
5. Le visiteur peut modifier le message avant de l'envoyer depuis son propre client de messagerie.

**Résultat attendu :** le visiteur peut initier une prise de contact sans création de compte ni saisie dans un formulaire du portfolio.

---

### 4.7 Changement de thème

**Objectif :** permettre au visiteur d'adapter l'affichage à sa préférence.

**Parcours :**

1. Le visiteur accède au portfolio.
2. Il sélectionne le contrôle permettant de basculer entre le thème clair et le thème sombre.
3. L'interface applique le thème sélectionné.
4. Le choix est mémorisé.
5. Lors d'une visite ultérieure depuis le même environnement, l'application restaure la préférence enregistrée.

**Résultat attendu :** le visiteur retrouve son mode d'affichage préféré entre deux visites.

---

### 4.8 Synthèse des parcours

| ID | Parcours | Point de départ | Résultat principal |
|----|----------|-----------------|--------------------|
| PU-001 | Découverte du profil | Accueil | Compréhension du profil professionnel |
| PU-002 | Découverte des projets | Accueil | Accès à la liste des réalisations |
| PU-003 | Consultation d'un projet | Liste des projets | Compréhension détaillée d'une réalisation |
| PU-004 | Recherche d'un projet | Projets | Identification de projets par mots-clés |
| PU-005 | Filtrage des projets | Projets | Identification de projets par catégorie |
| PU-006 | Prise de contact | Interface du portfolio | Ouverture du client de messagerie |
| PU-007 | Changement de thème | Interface du portfolio | Application et mémorisation du thème choisi |

---

## 5. User Stories

Les User Stories décrivent les principales fonctionnalités de l'application du point de vue de ses utilisateurs.

Elles sont formulées selon la structure suivante :

> En tant que **[acteur]**, je veux **[action]**, afin de **[objectif]**.

### 5.1 Consultation du profil

#### US-001 — Découvrir le profil

**En tant que visiteur**,  
je veux identifier rapidement le profil et le positionnement professionnel du développeur,  
afin de comprendre ses domaines de compétences.

#### US-002 — Accéder aux projets depuis l'accueil

**En tant que visiteur**,  
je veux pouvoir sélectionner l'action **« Découvrir mes projets »**,  
afin d'accéder aux réalisations présentées dans le portfolio.

---

### 5.2 Consultation des projets

#### US-003 — Consulter la liste des projets

**En tant que visiteur**,  
je veux consulter l'ensemble des projets présentés,  
afin d'obtenir une vue d'ensemble des réalisations du développeur.

#### US-004 — Identifier rapidement un projet

**En tant que visiteur**,  
je veux voir pour chaque projet son titre, son résumé, ses principales technologies et ses catégories,  
afin d'identifier rapidement les projets susceptibles de m'intéresser.

#### US-005 — Consulter le détail d'un projet

**En tant que visiteur**,  
je veux accéder à une page détaillée pour chaque projet,  
afin de comprendre son contexte, ses objectifs, sa réalisation et les compétences mobilisées.

#### US-006 — Comprendre la démarche suivie

**En tant que recruteur ou responsable technique**,  
je veux consulter la méthodologie, les difficultés rencontrées, les solutions apportées et les résultats obtenus,  
afin d'évaluer la démarche de travail du développeur.

---

### 5.3 Recherche et filtrage

#### US-007 — Rechercher un projet

**En tant que visiteur**,  
je veux rechercher des projets à partir de mots-clés,  
afin d'identifier rapidement les réalisations correspondant à mon besoin ou à mon domaine d'intérêt.

#### US-008 — Filtrer les projets

**En tant que visiteur**,  
je veux filtrer les projets selon leur catégorie,  
afin de consulter uniquement les réalisations appartenant à un domaine particulier.

#### US-009 — Réinitialiser la recherche et les filtres

**En tant que visiteur**,  
je veux pouvoir réinitialiser mes critères de recherche et de filtrage,  
afin de retrouver l'ensemble des projets disponibles.

---

### 5.4 Ressources associées aux projets

#### US-010 — Accéder à une démonstration

**En tant que visiteur**,  
je veux pouvoir accéder à la démonstration publique d'un projet lorsqu'elle existe,  
afin d'observer concrètement le résultat obtenu.

#### US-011 — Accéder au dépôt public

**En tant que visiteur**,  
je veux pouvoir accéder au dépôt public d'un projet lorsqu'il est disponible,  
afin de consulter les ressources techniques rendues publiques.

#### US-012 — Identifier un projet non public

**En tant que visiteur**,  
je veux être informé lorsqu'un dépôt ou le code d'un projet n'est pas public,  
afin de comprendre l'absence de lien vers son code source.

---

### 5.5 Liens professionnels et contact

#### US-013 — Accéder aux profils professionnels

**En tant que visiteur**,  
je veux pouvoir accéder aux profils GitHub et LinkedIn du développeur,  
afin de consulter ses autres informations et activités professionnelles publiques.

#### US-014 — Contacter le développeur

**En tant que visiteur**,  
je veux pouvoir initier l'envoi d'un courrier électronique au développeur,  
afin de pouvoir facilement prendre contact avec lui.

---

### 5.6 Préférences d'affichage

#### US-015 — Changer de thème

**En tant que visiteur**,  
je veux pouvoir choisir entre un thème clair et un thème sombre,  
afin d'adapter l'affichage à ma préférence.

#### US-016 — Conserver le thème sélectionné

**En tant que visiteur**,  
je veux que mon choix de thème soit conservé entre mes visites,  
afin de retrouver automatiquement mon mode d'affichage préféré.

---

### 5.7 Consultation sur différents appareils

#### US-017 — Consulter le portfolio sur différents écrans

**En tant que visiteur**,  
je veux pouvoir consulter et utiliser les fonctionnalités du portfolio sur ordinateur et sur appareil mobile,  
afin de bénéficier d'une expérience adaptée à mon appareil.

---

### 5.8 Synthèse des User Stories

| ID | Fonctionnalité | Acteur principal | Priorité |
|----|----------------|------------------|----------|
| US-001 | Découvrir le profil | Visiteur | Haute |
| US-002 | Accéder aux projets depuis l'accueil | Visiteur | Haute |
| US-003 | Consulter la liste des projets | Visiteur | Haute |
| US-004 | Identifier rapidement un projet | Visiteur | Haute |
| US-005 | Consulter le détail d'un projet | Visiteur | Haute |
| US-006 | Comprendre la démarche suivie | Recruteur / Responsable technique | Haute |
| US-007 | Rechercher un projet | Visiteur | Haute |
| US-008 | Filtrer les projets | Visiteur | Haute |
| US-009 | Réinitialiser la recherche et les filtres | Visiteur | Haute |
| US-010 | Accéder à une démonstration | Visiteur | Moyenne |
| US-011 | Accéder au dépôt public | Visiteur | Haute |
| US-012 | Identifier un projet non public | Visiteur | Haute |
| US-013 | Accéder aux profils professionnels | Visiteur | Haute |
| US-014 | Contacter le développeur | Visiteur | Haute |
| US-015 | Changer de thème | Visiteur | Moyenne |
| US-016 | Conserver le thème sélectionné | Visiteur | Moyenne |
| US-017 | Consulter le portfolio sur différents écrans | Visiteur | Haute |

---

## 6. Spécifications des fonctionnalités

Cette section décrit le comportement attendu des principales fonctionnalités de la V1 de **Fidel Portfolio**.

Chaque fonctionnalité est identifiée par un identifiant unique `SF-xxx` afin de faciliter sa traçabilité avec les besoins, les User Stories et les futurs cas de test.

---

### 6.1 Présentation du profil

#### SF-001 — Affichage de la page d'accueil

| Élément | Description |
|---------|-------------|
| Objectif | Présenter rapidement le profil professionnel du développeur. |
| Acteur | Visiteur |
| Priorité | Haute |
| User Stories | US-001, US-002 |

La page d'accueil doit permettre au visiteur d'identifier rapidement le développeur et son positionnement professionnel.

Elle doit présenter au minimum :

- l'identité du développeur ;
- son positionnement professionnel ;
- une présentation synthétique de ses domaines de compétences ;
- un élément visuel représentant le développeur ;
- une action **« Découvrir mes projets »**.

L'action **« Découvrir mes projets »** dirige le visiteur vers la page regroupant les projets.

La page d'accueil ne présente pas directement une sélection de projets.

**Résultat attendu :** le visiteur comprend rapidement le positionnement professionnel du développeur et peut poursuivre vers ses réalisations.

---

### 6.2 Consultation des projets

#### SF-002 — Affichage de la liste des projets

| Élément | Description |
|---------|-------------|
| Objectif | Permettre la consultation des réalisations. |
| Acteur | Visiteur |
| Priorité | Haute |
| User Stories | US-003, US-004 |

La page des projets doit afficher les projets disponibles sous forme de cartes.

Chaque carte doit présenter au minimum :

- le titre du projet ;
- un résumé ;
- les principales technologies utilisées ;
- la ou les catégories associées ;
- une action **« Voir le détail »**.

Un projet peut appartenir à plusieurs catégories.

La sélection de **« Voir le détail »** ouvre la page dédiée au projet sélectionné.

---

#### SF-003 — Consultation détaillée d'un projet

| Élément | Description |
|---------|-------------|
| Objectif | Permettre une analyse détaillée d'une réalisation. |
| Acteur | Visiteur |
| Priorité | Haute |
| User Stories | US-005, US-006 |

Chaque projet doit disposer d'une page de présentation dédiée.

Cette page doit pouvoir présenter :

- le nom du projet ;
- son contexte ;
- son objectif ;
- sa description ;
- les technologies et outils mobilisés ;
- les catégories associées ;
- la méthodologie suivie ;
- les principales étapes de réalisation ;
- les difficultés rencontrées ;
- les solutions apportées ;
- les résultats obtenus ;
- des schémas ou captures lorsque ceux-ci sont pertinents.

Les informations qui ne sont pas applicables à un projet peuvent être omises.

**Résultat attendu :** le visiteur doit pouvoir comprendre ce qui a été réalisé, dans quel contexte et selon quelle démarche.

---

### 6.3 Recherche et filtrage

#### SF-004 — Recherche par mots-clés

| Élément | Description |
|---------|-------------|
| Objectif | Retrouver rapidement des projets pertinents. |
| Acteur | Visiteur |
| Priorité | Haute |
| User Stories | US-007, US-009 |

La page des projets doit proposer un champ de recherche.

Le visiteur peut saisir un mot-clé afin de rechercher les projets correspondants.

La recherche peut porter sur les informations associées au projet, notamment :

- le titre ;
- la description ;
- les technologies ;
- les catégories ;
- les mots-clés associés.

Les projets ne correspondant pas à la recherche ne doivent plus apparaître dans les résultats affichés.

Si aucun projet ne correspond à la recherche, l'application affiche :

**« Aucun projet correspondant. »**

Une action permettant de réinitialiser la recherche doit être disponible.

---

#### SF-005 — Filtrage par catégorie

| Élément | Description |
|---------|-------------|
| Objectif | Permettre de cibler les projets selon un domaine. |
| Acteur | Visiteur |
| Priorité | Haute |
| User Stories | US-008, US-009 |

Le visiteur doit pouvoir filtrer les projets selon leur catégorie.

Les catégories initialement prévues sont :

- Développement ;
- DevOps ;
- DevSecOps ;
- Cloud ;
- Autres.

Lorsqu'une catégorie est sélectionnée, seuls les projets associés à cette catégorie sont affichés.

Une action de réinitialisation permet de revenir à l'affichage de l'ensemble des projets.

La recherche par mots-clés et le filtrage peuvent être utilisés simultanément. Dans ce cas, seuls les projets satisfaisant les critères actifs sont affichés.

---

### 6.4 Ressources associées aux projets

#### SF-006 — Accès à une démonstration

| Élément | Description |
|---------|-------------|
| Objectif | Permettre l'accès au résultat public d'un projet. |
| Acteur | Visiteur |
| Priorité | Moyenne |
| User Story | US-010 |

Lorsqu'une démonstration publique est disponible pour un projet, sa page détaillée doit proposer une action **« Voir la démo »**.

Cette action dirige le visiteur vers la démonstration correspondante.

Si aucune démonstration n'existe, l'action ne doit pas être proposée.

---

#### SF-007 — Accès au dépôt d'un projet

| Élément | Description |
|---------|-------------|
| Objectif | Permettre la consultation du code rendu public. |
| Acteur | Visiteur |
| Priorité | Haute |
| User Stories | US-011, US-012 |

Lorsqu'un dépôt public est associé à un projet, sa page détaillée doit proposer une action **« Voir le dépôt »**.

Lorsque le dépôt n'est pas public, aucun lien vers le code source privé ne doit être exposé.

Une indication telle que **« Dépôt privé »** ou **« Code non public »** peut être affichée afin d'expliquer l'absence d'accès au dépôt.

---

### 6.5 Profils externes et contact

#### SF-008 — Accès aux profils professionnels

| Élément | Description |
|---------|-------------|
| Objectif | Permettre l'accès aux profils professionnels externes. |
| Acteur | Visiteur |
| Priorité | Haute |
| User Story | US-013 |

Le portfolio doit proposer un accès aux profils professionnels publics du développeur.

La V1 prévoit notamment :

- GitHub ;
- LinkedIn.

La sélection d'un lien dirige le visiteur vers le profil externe correspondant.

---

#### SF-009 — Prise de contact

| Élément | Description |
|---------|-------------|
| Objectif | Permettre au visiteur d'initier une prise de contact. |
| Acteur | Visiteur |
| Priorité | Haute |
| User Story | US-014 |

Une action **« Me contacter »** doit être accessible depuis le portfolio.

Lorsqu'elle est sélectionnée :

1. le client de messagerie configuré sur l'appareil du visiteur est sollicité ;
2. l'adresse électronique du développeur est renseignée ;
3. un objet peut être prérempli ;
4. un contenu initial peut éventuellement être proposé.

L'envoi du message est réalisé depuis le client de messagerie du visiteur et non directement par le portfolio.

Aucun formulaire de contact n'est requis pour la V1.

---

### 6.6 Gestion du thème

#### SF-010 — Changement de thème

| Élément | Description |
|---------|-------------|
| Objectif | Permettre au visiteur de personnaliser l'affichage. |
| Acteur | Visiteur |
| Priorité | Moyenne |
| User Story | US-015 |

L'interface doit proposer :

- un thème clair ;
- un thème sombre.

Le visiteur doit pouvoir basculer entre les deux thèmes depuis l'interface.

Le changement doit être appliqué à l'ensemble de l'interface concernée.

---

#### SF-011 — Mémorisation du thème

| Élément | Description |
|---------|-------------|
| Objectif | Conserver la préférence d'affichage du visiteur. |
| Acteur | Visiteur |
| Priorité | Moyenne |
| User Story | US-016 |

Lorsqu'un visiteur sélectionne un thème, son choix doit être conservé entre ses visites lorsque son environnement le permet.

Lors d'une visite ultérieure, le thème précédemment choisi doit être restauré automatiquement.

Le mécanisme technique utilisé pour assurer cette persistance sera défini dans les spécifications techniques.

---

### 6.7 Adaptation de l'interface

#### SF-012 — Consultation sur différents écrans

| Élément | Description |
|---------|-------------|
| Objectif | Garantir l'accès aux fonctionnalités principales sur différentes tailles d'écran. |
| Acteur | Visiteur |
| Priorité | Haute |
| User Story | US-017 |

Le portfolio doit pouvoir être consulté sur ordinateur et sur appareil mobile.

L'adaptation de l'interface ne doit pas supprimer l'accès aux fonctionnalités principales, notamment :

- la navigation ;
- la consultation des projets ;
- la recherche ;
- le filtrage ;
- la consultation détaillée d'un projet ;
- le changement de thème ;
- les liens externes ;
- la prise de contact.

Les modalités techniques précises d'adaptation aux différentes tailles d'écran seront définies dans les spécifications techniques.

---

### 6.8 Animations de l'interface

#### SF-013 — Animations et transitions

| Élément | Description |
|---------|-------------|
| Objectif | Enrichir l'expérience visuelle du portfolio. |
| Acteur | Visiteur |
| Priorité | Moyenne |

L'interface peut proposer des animations et transitions, notamment :

- des transitions entre certains états ;
- des apparitions progressives de contenu ;
- des animations déclenchées lors du défilement ;
- des retours visuels lors des interactions.

Les animations doivent rester secondaires par rapport au contenu et ne doivent pas empêcher l'utilisation des fonctionnalités principales.

Les contraintes de performance et d'accessibilité associées aux animations seront précisées dans les spécifications non fonctionnelles et techniques.

---

## 7. Règles métier

Cette section définit les règles fonctionnelles qui doivent être respectées indépendamment de l'interface ou des choix techniques d'implémentation.

Chaque règle est identifiée par un identifiant unique `RM-xxx` afin de faciliter sa traçabilité et sa vérification.

### 7.1 Gestion des projets

#### RM-001 — Présentation minimale d'un projet

Tout projet publié dans le portfolio doit disposer des informations minimales nécessaires à sa compréhension.

Un projet doit au minimum comporter :

- un titre ;
- un résumé ;
- une description ;
- un objectif ;
- au moins une catégorie ;
- les principales technologies ou outils mobilisés.

Les informations complémentaires telles que les difficultés rencontrées, les solutions apportées, les résultats obtenus, les schémas ou les captures peuvent être ajoutées lorsqu'elles sont pertinentes.

---

#### RM-002 — Catégorisation des projets

Chaque projet doit être associé à au moins une catégorie.

Un projet peut appartenir à plusieurs catégories.

Les catégories prévues pour la V1 sont notamment :

- Développement ;
- DevOps ;
- DevSecOps ;
- Cloud ;
- Autres.

---

#### RM-003 — Accès au détail d'un projet

Tout projet affiché dans la liste des projets doit disposer d'une page de présentation détaillée accessible depuis sa carte.

L'accès à cette présentation ne dépend pas de l'existence d'une démonstration ou d'un dépôt public.

---

### 7.2 Démonstrations et dépôts

#### RM-004 — Disponibilité d'une démonstration

L'action **« Voir la démo »** ne doit être proposée que lorsqu'une démonstration publique et accessible est associée au projet.

L'absence de démonstration ne doit pas empêcher la consultation de la page détaillée du projet.

---

#### RM-005 — Disponibilité du dépôt

L'action **« Voir le dépôt »** ne doit être proposée que lorsqu'un dépôt public est associé au projet.

Aucun lien permettant d'accéder à un dépôt privé ne doit être exposé publiquement.

---

#### RM-006 — Identification des ressources non publiques

Lorsqu'un projet ou son code source ne peut pas être rendu public, cette situation peut être indiquée au visiteur à l'aide d'une mention telle que :

- **« Dépôt privé »** ;
- **« Code non public »**.

Cette indication ne doit révéler aucune information confidentielle relative au projet.

---

### 7.3 Recherche et filtrage

#### RM-007 — Recherche par mots-clés

La recherche doit permettre d'identifier les projets à partir des informations utilisées pour leur indexation fonctionnelle, notamment :

- le titre ;
- la description ;
- les technologies ;
- les catégories ;
- les mots-clés associés.

---

#### RM-008 — Combinaison de la recherche et des filtres

La recherche par mots-clés et le filtrage par catégorie peuvent être utilisés simultanément.

Lorsque plusieurs critères sont actifs, seuls les projets correspondant à l'ensemble des critères applicables doivent être affichés.

---

#### RM-009 — Absence de résultat

Lorsqu'aucun projet ne correspond aux critères actifs, aucun résultat incorrect ne doit être présenté.

L'application doit afficher le message :

**« Aucun projet correspondant. »**

Une action permettant de réinitialiser les critères doit être proposée.

---

#### RM-010 — Réinitialisation des critères

La réinitialisation de la recherche et des filtres doit permettre de revenir à l'affichage de l'ensemble des projets disponibles.

---

### 7.4 Contact

#### RM-011 — Prise de contact

La prise de contact depuis la V1 est réalisée par l'intermédiaire du client de messagerie du visiteur.

Le portfolio ne réalise pas directement l'envoi du courrier électronique.

Aucun compte utilisateur ni formulaire de contact n'est requis pour cette fonctionnalité.

---

### 7.5 Préférences d'affichage

#### RM-012 — Thèmes disponibles

La V1 doit proposer au minimum :

- un thème clair ;
- un thème sombre.

---

#### RM-013 — Conservation du thème

Lorsqu'un visiteur choisit explicitement un thème, cette préférence doit être conservée entre ses visites lorsque son environnement permet cette mémorisation.

Le choix explicite du visiteur doit être privilégié lors des visites suivantes.

---

### 7.6 Navigation et accès au contenu

#### RM-014 — Accès public

Les contenus prévus dans la V1 du portfolio sont accessibles sans création de compte ni authentification.

---

#### RM-015 — Accès aux projets depuis l'accueil

La page d'accueil doit proposer une action **« Découvrir mes projets »** permettant d'accéder à la liste des projets.

Les projets ne sont pas directement affichés sur la page d'accueil.

---

#### RM-016 — Accès aux fonctionnalités essentielles

Les fonctionnalités essentielles doivent rester accessibles sur les formats d'écran pris en charge par la V1.

Une adaptation de l'interface ne doit pas entraîner la suppression fonctionnelle de la consultation des projets, de la navigation, de la recherche, du filtrage ou de la prise de contact.

---

## 8. Cas particuliers et gestion des erreurs

Cette section décrit les comportements attendus lorsque certaines données sont absentes, qu'une ressource n'est pas disponible ou qu'une action ne peut pas être réalisée normalement.

L'objectif est de garantir que l'utilisateur puisse comprendre la situation et poursuivre sa navigation sans être confronté à une interface incohérente ou bloquante.

### 8.1 Recherche sans résultat

#### CP-001 — Aucun projet correspondant

Lorsqu'aucun projet ne correspond à la recherche ou aux filtres sélectionnés :

- aucune carte projet non pertinente ne doit être affichée ;
- le message **« Aucun projet correspondant. »** doit être présenté ;
- une action permettant de réinitialiser les critères doit être disponible.

Après réinitialisation, l'ensemble des projets doit de nouveau être affiché.

---

### 8.2 Recherche vide

#### CP-002 — Champ de recherche vide

Lorsque le champ de recherche est vide et qu'aucun filtre n'est actif, l'ensemble des projets disponibles doit être affiché.

La suppression du contenu précédemment saisi dans le champ de recherche doit permettre de revenir à la liste correspondant aux éventuels filtres encore actifs.

---

### 8.3 Projet inexistant

#### CP-003 — Accès à un projet inexistant

Lorsqu'un visiteur tente d'accéder à une page projet inexistante ou qui n'est plus disponible, l'application ne doit pas afficher une page vide ou provoquer un blocage de la navigation.

Elle doit :

- informer le visiteur que le projet demandé n'est pas disponible ;
- lui permettre de revenir à la liste des projets ;
- lui permettre de poursuivre sa navigation dans le portfolio.

---

### 8.4 Démonstration indisponible

#### CP-004 — Absence de démonstration

Lorsqu'aucune démonstration publique n'est associée à un projet, l'action **« Voir la démo »** ne doit pas être affichée.

La page détaillée du projet reste accessible normalement.

---

### 8.5 Dépôt non public

#### CP-005 — Dépôt privé ou code non public

Lorsqu'un dépôt ne peut pas être rendu public :

- aucun lien vers le dépôt privé ne doit être exposé ;
- aucune information confidentielle ne doit être affichée ;
- une mention telle que **« Dépôt privé »** ou **« Code non public »** peut être présentée.

La présentation détaillée du projet doit rester consultable.

---

### 8.6 Ressource externe indisponible

#### CP-006 — Lien externe inaccessible

Les liens externes proposés par le portfolio doivent correspondre à des ressources configurées comme disponibles.

Lorsqu'une ressource externe n'est plus disponible, son indisponibilité ne doit pas empêcher l'utilisation du reste du portfolio.

Les liens devenus invalides doivent pouvoir être retirés ou corrigés lors de la maintenance du projet.

---

### 8.7 Échec de mémorisation du thème

#### CP-007 — Préférence de thème non conservée

Lorsque l'environnement du visiteur ne permet pas de conserver sa préférence de thème :

- le changement de thème doit continuer à fonctionner pendant la visite en cours ;
- l'impossibilité de conserver la préférence ne doit pas bloquer la navigation ;
- l'application doit utiliser son comportement d'affichage par défaut lors d'une visite ultérieure si aucune préférence ne peut être récupérée.

---

### 8.8 Client de messagerie indisponible

#### CP-008 — Impossible d'ouvrir le client de messagerie

La fonctionnalité **« Me contacter »** repose sur la capacité de l'environnement du visiteur à traiter un lien de courrier électronique.

Si aucun client de messagerie compatible n'est configuré, le portfolio ne peut pas garantir l'ouverture d'une application de messagerie.

Cette situation ne doit pas empêcher la poursuite de la navigation dans le portfolio.

---

### 8.9 Contenu visuel indisponible

#### CP-009 — Élément visuel facultatif absent

Lorsqu'un projet ne dispose pas de schéma, de capture ou d'autre contenu visuel facultatif, la page détaillée doit rester cohérente et entièrement consultable.

Aucun emplacement vide ou élément d'interface inutile ne doit être affiché uniquement pour représenter un contenu inexistant.

---

### 8.10 Animations non disponibles

#### CP-010 — Animation désactivée ou non exécutée

Les animations constituent un enrichissement visuel et ne doivent pas être nécessaires à la compréhension ou à l'utilisation du portfolio.

Si une animation ne peut pas être exécutée ou doit être réduite pour des raisons d'accessibilité, le contenu concerné doit rester accessible et compréhensible.

---

### 8.11 Synthèse des cas particuliers

| ID | Situation | Comportement attendu |
|----|-----------|----------------------|
| CP-001 | Aucun résultat de recherche | Afficher un message et proposer une réinitialisation |
| CP-002 | Recherche vide | Afficher les projets correspondant aux éventuels filtres actifs |
| CP-003 | Projet inexistant | Informer le visiteur et proposer un retour vers les projets |
| CP-004 | Démonstration absente | Ne pas afficher l'action « Voir la démo » |
| CP-005 | Dépôt privé | Ne pas exposer le lien et indiquer éventuellement son caractère privé |
| CP-006 | Ressource externe indisponible | Ne pas bloquer le reste du portfolio |
| CP-007 | Thème non mémorisable | Maintenir le fonctionnement de la visite en cours |
| CP-008 | Client de messagerie indisponible | Ne pas bloquer la navigation |
| CP-009 | Contenu visuel facultatif absent | Adapter la présentation sans emplacement vide |
| CP-010 | Animation indisponible ou réduite | Maintenir l'accès au contenu et aux fonctionnalités |

---

## 9. Traçabilité

Cette section assure la traçabilité entre les besoins identifiés lors de l'analyse, les User Stories et les spécifications fonctionnelles définies dans le présent document.

Les cas de test seront associés aux fonctionnalités lors de la rédaction de la documentation de test.

### 9.1 Traçabilité des besoins utilisateurs

| Besoin | User Story | Spécification fonctionnelle | Règle métier | Test |
|--------|------------|------------------------------|---------------|------|
| BU-001 | US-001 | SF-001 | RM-014, RM-015 | À définir |
| BU-002 | US-002, US-003, US-004, US-005 | SF-001, SF-002, SF-003 | RM-001, RM-002, RM-003, RM-015 | À définir |
| BU-003 | US-004, US-005, US-006 | SF-002, SF-003 | RM-001, RM-002 | À définir |
| BU-004 | US-005, US-006 | SF-003 | RM-001 | À définir |
| BU-005 | US-014 | SF-009 | RM-011 | À définir |
| BU-006 | US-001, US-002, US-003, US-007, US-008 | SF-001, SF-002, SF-004, SF-005 | RM-007, RM-008, RM-009, RM-010, RM-015 | À définir |

### 9.2 Traçabilité des User Stories

| User Story | Spécification | Règle(s) métier associée(s) | Cas particulier |
|------------|---------------|-----------------------------|-----------------|
| US-001 | SF-001 | RM-014 | — |
| US-002 | SF-001 | RM-015 | — |
| US-003 | SF-002 | RM-001, RM-002, RM-003 | — |
| US-004 | SF-002 | RM-001, RM-002 | — |
| US-005 | SF-003 | RM-001, RM-003 | CP-003, CP-009 |
| US-006 | SF-003 | RM-001 | CP-009 |
| US-007 | SF-004 | RM-007, RM-008, RM-009, RM-010 | CP-001, CP-002 |
| US-008 | SF-005 | RM-002, RM-008, RM-009, RM-010 | CP-001 |
| US-009 | SF-004, SF-005 | RM-009, RM-010 | CP-001, CP-002 |
| US-010 | SF-006 | RM-004 | CP-004, CP-006 |
| US-011 | SF-007 | RM-005 | CP-006 |
| US-012 | SF-007 | RM-005, RM-006 | CP-005 |
| US-013 | SF-008 | — | CP-006 |
| US-014 | SF-009 | RM-011 | CP-008 |
| US-015 | SF-010 | RM-012 | — |
| US-016 | SF-011 | RM-013 | CP-007 |
| US-017 | SF-012 | RM-016 | — |

### 9.3 Traçabilité des fonctionnalités

| Spécification | Fonctionnalité | User Story(s) |
|---------------|----------------|---------------|
| SF-001 | Présentation du profil et accès aux projets | US-001, US-002 |
| SF-002 | Liste des projets | US-003, US-004 |
| SF-003 | Présentation détaillée d'un projet | US-005, US-006 |
| SF-004 | Recherche par mots-clés | US-007, US-009 |
| SF-005 | Filtrage par catégorie | US-008, US-009 |
| SF-006 | Accès à une démonstration | US-010 |
| SF-007 | Accès au dépôt d'un projet | US-011, US-012 |
| SF-008 | Accès aux profils professionnels | US-013 |
| SF-009 | Prise de contact | US-014 |
| SF-010 | Changement de thème | US-015 |
| SF-011 | Mémorisation du thème | US-016 |
| SF-012 | Consultation sur différents écrans | US-017 |
| SF-013 | Animations et transitions | — |

### 9.4 Évolution de la traçabilité

La matrice de traçabilité sera complétée au fur et à mesure de l'avancement du projet.

Les futurs cas de test devront permettre de vérifier que les comportements définis dans les spécifications fonctionnelles sont correctement implémentés.

Les identifiants utilisés dans la documentation devront être conservés afin de maintenir les relations entre :

**Besoin → User Story → Spécification fonctionnelle → Règle métier → Cas de test**

---

## 10. Documents liés

Les documents suivants participent à la définition et à la réalisation du projet :

- [Glossaire](00-glossaire.md)
- [Vision du projet](01-vision-projet.md)
- [Analyse des besoins](01a-analyse-des-besoins.md)
- [Cahier des charges](02-cahier-des-charges.md)
- [Spécifications techniques](04-specifications-techniques.md)
- [Architecture](05-architecture.md)
- [Sécurité](06-securite.md)
- [Tests](07-tests.md)

---

**Document précédent :**  
➡️ [Cahier des charges](02-cahier-des-charges.md)

**Document suivant :**  
➡️ [Spécifications techniques](04-specifications-techniques.md)