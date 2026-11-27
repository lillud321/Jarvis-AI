# Feuille de route

| Livrable | État | Critère de validation |
| --- | --- | --- |
| 1. Fondation du dépôt GitHub | Réalisé | Le README explique le projet et ses objectifs. Il donne accès à l’architecture prévue et à cette feuille de route. |
| 2. [Cadrage du projet](cadrage.md) | En réflexion | Identifier les capacités recherchées, les outils nécessaires et les situations permettant de les évaluer. |
| 3. Installation et validation sur le PC Windows | À réaliser | Inventorier les outils et modèles présents, installer seulement les prérequis manquants et consigner les étapes dans un guide Windows. Depuis le PC, obtenir une réponse de l’API locale d’Ollama et consigner une première mesure de délai et de mémoire selon le [plan de déploiement](deploiement-reprise.md). |
| 4. Harnais IA local | À réaliser | Démarrer une conversation avec un modèle Ollama, passer à un second modèle et reprendre le même échange avec son contexte. Viser moins de 30 secondes de manipulation pour remplacer le modèle principal déjà installé et compatible, puis vérifier la reprise du contexte et des permissions. Mesurer séparément le délai jusqu’à la première réponse. |
| 5. Mémoire, profil et suivi | Prévu | Après un redémarrage, retrouver par recherche une décision, le problème associé et la prochaine action. Dans une nouvelle conversation, vérifier qu’une préférence choisie s’applique après changement de modèle, puis qu’elle cesse de s’appliquer après suppression. |
| 6. Diagnostics en lecture seule | Prévu | Depuis JARVIS, consulter l’état d’un service local autorisé et retrouver le résultat dans l’historique. Docker est le premier cas envisagé. |
| 7. Actions avec confirmation | Prévu | Prévisualiser une modification et sa cible. Vérifier qu’un refus laisse la cible intacte et qu’une confirmation exécute uniquement l’action approuvée. |
| 8. Progression par exemples validés | Prévu | Ajouter un cas Excel ou Power BI corrigé avec son résultat attendu, puis le rejouer après une évolution de JARVIS pour vérifier si la correction tient. |
| 9. Production et révision de fichiers | Prévu | Créer, lire et modifier des fichiers dans les formats retenus. Vérifier leur contenu après réouverture. |
| 10. Compréhension de contenus multimodaux | Prévu | Interpréter des images, tableaux, graphiques et enregistrements avec des outils locaux adaptés et vérifier les éléments cités. |
| 11. Recherche, raisonnement et production coordonnée | Prévu | Retrouver les sources pertinentes, adapter une proposition aux contraintes et répercuter une correction dans plusieurs supports. Évaluer le transfert sur un second contexte. |
| 12. Accès privé à distance | Prévu | Depuis un appareil autorisé hors du domicile, reprendre par écrit une conversation locale et retrouver son contexte avec les mêmes permissions. |
| 13. Rappels et notifications | Prévu | Programmer un rappel, recevoir la notification à l’heure convenue avec la conversation fermée et vérifier qu’un rappel annulé ne se déclenche plus. |
| 14. Création locale en environnement contrôlé | Prévu | Produire et prévisualiser un résultat dans un espace dédié. Vérifier que les fichiers hors périmètre sont inaccessibles et que seule une sortie approuvée rejoint sa destination. Pour Docker, construire une image, déployer le conteneur dans la cible approuvée, vérifier son fonctionnement et pouvoir retirer ce déploiement. |
| 15. Développement assisté sur GitHub | Prévu | Lire un dépôt autorisé, préparer une modification locale et présenter les différences. Sur accord, publier sur une branche de travail et ouvrir une demande de fusion pour révision. |
| 16. Création et utilisation d’agents spécialisés | Prévu | Créer un profil à partir d’une demande, examiner ses accès et le réutiliser sur une seconde tâche. Vérifier que ses outils respectent les permissions accordées. |
| 17. Sélection du modèle selon la tâche | Prévu | Comparer justesse, délai et consommation de mémoire sur une même tâche, valider la délégation par le modèle principal, changer les affectations des spécialistes depuis les paramètres et pouvoir rétablir le profil précédent. |
| 18. Second avis externe avec consentement | Prévu | Préparer localement une demande dépersonnalisée, vérifier le contenu et le destinataire, puis tester les chemins d’accord et de refus. |
| 19. Installation reproductible et reprise | Prévu | Valider d’abord le déploiement sur PC seul, vérifier l’inventaire et restaurer un projet témoin sur une cible vierge selon le [plan de reprise](deploiement-reprise.md). Vérifier la reprise après remplacement du PC ou du NAS et la récupération de changements non publiés. Mesurer le délai et les données récupérées. |

## Migration ultérieure vers le Synology

Développer et valider la première version intégralement sur Windows. Après cette validation, migrer le harnais et ses données selon le [plan de déploiement](deploiement-reprise.md), puis vérifier le fonctionnement avec Ollama et les outils restés sur le PC.

## Validation

Les [scénarios d’essai](scenarios-essai.md) conservent les usages retenus, dont la formation des cadets. Un scénario peut évaluer plusieurs capacités. Les essais seront choisis en fonction du livrable à valider.

## Intégrations envisagées

Open WebUI, Tailscale et n8n pourront être intégrés selon les besoins. Pour chaque intégration, préciser les informations consultables et les actions autorisées avant son développement.

[Retour à la présentation du projet](../README.md)
