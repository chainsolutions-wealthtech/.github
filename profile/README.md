# ChainSolutions WealthTech

Organisation GitHub cible pour les projets WealthTech, BRVM, OPCVM, MCP, automatisation, migration et gouvernance technique.

## Rôle de cette organisation

`chainsolutions-wealthtech` est l'organisation GitHub de référence pour centraliser progressivement les projets techniques WealthTech / ChainSolutions.

Elle sert de cible principale pour :

- les dépôts applicatifs WealthTech ;
- les projets BRVM Chain Solution ;
- les projets OPCVM / FundAfrica ;
- le serveur MCP WealthTech ;
- les outils d'automatisation ;
- les agents, compétences et workflows d'ingénierie ;
- la documentation technique ;
- les migrations depuis les comptes sources ;
- les Pull Requests contrôlées ;
- la gouvernance technique long terme.

## Règle d'organisation cible

La règle cible est la suivante :

> Tout nouveau dépôt durable WealthTech / ChainSolutions doit être créé dans `chainsolutions-wealthtech`, sauf exception explicitement documentée.

Les comptes sources ou historiques actuellement identifiés sont :

- `Patricked-code` ;
- `Wealthtechinnovations`.

Les anciens remotes Git peuvent rester temporairement utilisés en lecture, mais les dépôts cibles, la documentation de migration, les workflows et les nouvelles branches de travail doivent être alignés progressivement sur `chainsolutions-wealthtech`.

## Dépôts structurants

| Dépôt | Rôle cible |
|---|---|
| `.github` | Profil public/organisationnel, règles générales et cadrage transverse. |
| `MCP` | Serveur MCP WealthTech, pont ChatGPT/GitHub/S1/S2 et opérations contrôlées. |
| `api` | Cible de migration pour l'API OPCVM / FundAfrica. |
| `Front` | Cible de migration pour le frontend OPCVM / FundAfrica. |
| `Stablecoin` | Cible de gouvernance du projet Stablecoin. |
| `Investbourse` | Cible de gouvernance du projet Investbourse. |
| `civitech-commune-saas` | Cible de gouvernance du projet Civitech Commune SaaS. |

## Règle MCP et Git

Le MCP doit utiliser `chainsolutions-wealthtech` comme organisation cible principale pour les nouveaux dépôts, la documentation et les workflows de migration.

Pour les projets déjà présents sur serveur, la bascule Git ne doit pas être faite brutalement. Elle doit respecter l'ordre suivant :

1. inventorier l'état Git local sur serveur ;
2. vérifier le remote GitHub actuel ;
3. vérifier l'existence du dépôt cible dans `chainsolutions-wealthtech` ;
4. migrer ou importer le code dans le dépôt cible ;
5. vérifier les branches, tags, historiques et fichiers sensibles ;
6. seulement ensuite remplacer le remote `origin` côté serveur ;
7. effectuer un `git fetch`, puis un `git status -sb` ;
8. valider que la production n'a pas été modifiée par erreur.

## État de paramétrage au 2026-07-08

Le connecteur GitHub utilisé par ChatGPT dispose d'un accès administrateur aux dépôts existants de l'organisation `chainsolutions-wealthtech`.

Le MCP serveur expose actuellement des actions Git contrôlées sur les projets autorisés, notamment le statut Git et le pull contrôlé. Le changement direct de remote serveur n'est pas exposé par les outils MCP actuels et doit être ajouté comme action contrôlée séparée avant toute bascule serveur.

## Principe de sécurité

Aucun secret, fichier `.env`, clé privée, dump de base de données, sauvegarde serveur ou fichier de production sensible ne doit être commité dans GitHub.

Les opérations doivent rester progressives, vérifiables et réversibles.
