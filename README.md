# JARVIS-AI

JARVIS est un projet d’assistant personnel local et francophone. Il doit permettre de poser des questions en français, de créer des applications simples et d’explorer des intégrations d’IA locale dans FinanceOS. L’utilisateur garde la maîtrise de ses données et des actions effectuées en son nom.

## Objectifs

- **Assurer la continuité.** Retrouver une conversation, une décision ou un diagnostic et reprendre le travail là où il s’est arrêté.
- **Pouvoir changer d’IA.** Confier la mémoire, les outils et les permissions à JARVIS pour pouvoir remplacer le modèle au fil du temps. Ollama est le premier moteur envisagé.
- **Garder les données en local.** Prévoir un fonctionnement sur le PC et le réseau privé. Les conversations, configurations personnelles et secrets restent sur les appareils de l’utilisateur.
- **Garder le contrôle des actions.** Commencer par la consultation. Pour toute modification proposée, montrer l’action et sa cible, puis demander une confirmation explicite.

## État du projet

Le premier livrable établit la structure du dépôt, les objectifs et la feuille de route. Le deuxième livrable précise les usages prioritaires et la façon d’y répondre. L’installation de l’environnement local vient en troisième, puis le harnais IA en quatrième.

## Structure du dépôt

| Emplacement | Contenu |
| --- | --- |
| [README.md](README.md) | Présentation, objectifs et état du projet |
| [docs/cadrage.md](docs/cadrage.md) | Usages envisagés, démarche et décisions à prendre |
| [docs/architecture.md](docs/architecture.md) | Architecture prévue et responsabilités des composants |
| [docs/feuille-de-route.md](docs/feuille-de-route.md) | Livrables, ordre de réalisation et critères de validation |

Les dossiers de code et de tests seront ajoutés avec la première fonctionnalité exécutable.
