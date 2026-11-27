# Feuille de route

| Livrable | État | Critère de validation |
| --- | --- | --- |
| 1. Fondation du dépôt GitHub | Réalisé | Le README explique le projet et ses objectifs. Il donne accès à l’architecture prévue et à cette feuille de route. |
| 2. [Cadrage du projet](cadrage.md) | En réflexion | Choisir un premier usage réel et consigner le résultat attendu, le périmètre de la première version, les moyens nécessaires et un critère de réussite observable. |
| 3. Installation et validation sur le PC Windows | À réaliser | Inventorier les outils et modèles présents, installer seulement les prérequis manquants et consigner les étapes dans un guide Windows. Depuis le PC, envoyer une question à l’API locale d’Ollama et obtenir la réponse d’un modèle installé. |
| 4. Harnais IA local | À réaliser | Démarrer une conversation avec un modèle Ollama, passer à un second modèle et reprendre le même échange avec son contexte. Le choix du modèle conserve les permissions définies dans JARVIS. |
| 5. Mémoire, profil et suivi | Prévu | Après un redémarrage, retrouver par recherche une décision, le problème associé et la prochaine action. Dans une nouvelle conversation, vérifier qu’une préférence choisie s’applique après changement de modèle, puis qu’elle cesse de s’appliquer après suppression. |
| 6. Diagnostics en lecture seule | Prévu | Depuis JARVIS, consulter l’état d’un service local autorisé et retrouver le résultat dans l’historique. Docker est le premier cas envisagé. |
| 7. Actions avec confirmation | Prévu | Prévisualiser une modification et sa cible. Vérifier qu’un refus laisse la cible intacte et qu’une confirmation exécute uniquement l’action approuvée. |
| 8. Progression par exemples validés | Prévu | Ajouter un cas Excel ou Power BI corrigé avec son résultat attendu, puis le rejouer après une évolution de JARVIS pour vérifier si la correction tient. |
| 9. Documents Word, Excel, PowerPoint et PDF | Prévu | Pour chacun des quatre formats, réussir les trois essais du [cadrage](cadrage.md) en lisant une information vérifiable, en modifiant une copie et en créant un fichier utilisable. |
| 10. Analyse locale d’images, de graphiques et de tableaux | Prévu | Répondre aux questions du [cadrage](cadrage.md) sur une photo, une capture Power BI, un tableau structuré et un tableau numérisé. Vérifier les chiffres contre les sources et signaler les valeurs illisibles ou estimées. |
| 11. Huit usages complémentaires | Prévu | Réaliser les huit essais du [cadrage](cadrage.md#autres-usages-retenus) couvrant recherche personnelle, tutorat, simulation, comparaison d’options, planification, suivi audio, comparaison de versions et jeu interactif. |
| 12. Formation personnalisée pour les cadets | Prévu | À partir d’un guide, de l’effectif et des objectifs, produire un plan d’instruction minuté et une présentation synchronisée. Vérifier leur cohérence sur le [cas du mentorat](cadrage.md#préparer-une-formation-pour-les-cadets). |

## Essais utilisateurs proposés

Dès que le harnais permet un échange local, essayer une question écrite en français sur une formule Excel ou une mesure DAX avec une relance, puis la création et la révision d’une petite application. Pour FinanceOS, choisir une fonctionnalité et réaliser un essai avec des données fictives. Les exemples et les résultats attendus figurent dans le [cadrage](cadrage.md).

## Intégrations envisagées

Open WebUI, le NAS Synology, Tailscale et n8n pourront être intégrés selon les besoins. Pour chaque intégration, préciser les informations consultables et les actions autorisées avant son développement.

[Retour à la présentation du projet](../README.md)
