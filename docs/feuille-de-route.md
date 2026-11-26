# Feuille de route

| Livrable | État | Critère de validation |
| --- | --- | --- |
| 1. Fondation du dépôt GitHub | Réalisé | Le README explique le projet et ses objectifs. Il donne accès à l’architecture prévue et à cette feuille de route. |
| 2. [Cadrage du projet](cadrage.md) | En réflexion | Choisir un premier usage réel et consigner le résultat attendu, le périmètre de la première version, les moyens nécessaires et un critère de réussite observable. |
| 3. Installation et validation sur le PC Windows | À réaliser | Inventorier les outils et modèles présents, installer seulement les prérequis manquants et consigner les étapes dans un guide Windows. Depuis le PC, envoyer une question à l’API locale d’Ollama et obtenir la réponse d’un modèle installé. |
| 4. Harnais IA local | À réaliser | Démarrer une conversation avec un modèle Ollama, passer à un second modèle et reprendre le même échange avec son contexte. Le choix du modèle conserve les permissions définies dans JARVIS. |
| 5. Mémoire et suivi | Prévu | Après un redémarrage, retrouver par recherche une décision, le problème associé et la prochaine action. |
| 6. Diagnostics en lecture seule | Prévu | Depuis JARVIS, consulter l’état d’un service local autorisé et retrouver le résultat dans l’historique. Docker est le premier cas envisagé. |
| 7. Actions avec confirmation | Prévu | Prévisualiser une modification et sa cible. Vérifier qu’un refus laisse la cible intacte et qu’une confirmation exécute uniquement l’action approuvée. |

## Intégrations envisagées

Open WebUI, le NAS Synology, Tailscale et n8n pourront être intégrés selon les besoins. Pour chaque intégration, préciser les informations consultables et les actions autorisées avant son développement.

[Retour à la présentation du projet](../README.md)
