# Guide de contribution

## Statut des documents

Les documents du projet utilisent les statuts suivants :

| Statut | Signification |
|---|---|
| `Brouillon` | Le document existe mais son contenu est encore incomplet ou exploratoire. |
| `En cours de rédaction` | Le document est activement rédigé ou modifié et n'est pas encore stabilisé. |
| `À valider` | La rédaction prévue est terminée, mais le contenu doit encore être relu ou validé. |
| `Validé` | Le document a été relu et son contenu constitue la référence actuelle du projet. |

Un document `Validé` peut être modifié ultérieurement si le projet évolue. Toute modification significative peut temporairement replacer le document dans l'état `En cours de rédaction` ou `À valider`.

## Workflow Git

main
↑
develop
↑
feature/*

## Convention de nommage des branches

feature/
fix/
docs/
chore/
refactor/
security/
ci/

# Convention de commits

Les messages de commit suivent les conventions Gitmoji et Conventional Commits.

| Gitmoji | Code | Type | Utilisation |
|---------|------|------|-------------|
| 📝 | `:memo:` | `docs:` | Documentation |
| ✨ | `:sparkles:` | `feat:` | Nouvelle fonctionnalité |
| 🐛 | `:bug:` | `fix:` | Correction de bug |
| ♻️ | `:recycle:` | `refactor:` | Refactorisation |
| 🔧 | `:wrench:` | `chore:` | Configuration et maintenance |
| 👷 | `:construction_worker:` | `ci:` | Pipeline CI/CD |
| 🔒 | `:lock:` | `security:` | Sécurité |
| ⚡ | `:zap:` | `perf:` | Optimisation des performances |
| 🎨 | `:art:` | `style:` | Mise en forme et UI |
| ✅ | `:white_check_mark:` | `test:` | Ajout ou modification de tests |
| 📦 | `:package:` | `build:` | Dépendances et build |
| 🔥 | `:fire:` | `remove:` | Suppression de code ou de fichiers |

## Pull Requests

Les modifications ne sont pas intégrées directement dans les branches protégées.

Le workflow suivant est utilisé :

- les branches de travail (`feature/*`, `fix/*`, `docs/*`, etc.) sont fusionnées dans `develop` via une Pull Request ;
- `develop` sert de branche d'intégration ;
- les modifications validées sont ensuite fusionnées de `develop` vers `main` via une Pull Request ;
- `main` représente la version stable du projet.

Avant de créer une Pull Request :

- vérifier que la branche est à jour ;
- vérifier les modifications avec `git diff` ;
- effectuer les contrôles et tests disponibles ;
- utiliser un titre décrivant clairement les changements ;
- documenter les principaux changements dans la description de la Pull Request.