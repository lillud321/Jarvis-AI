# Déploiement et reprise prévus

## Ordre de déploiement retenu

Une interface web privée dessert le PC et le téléphone. Le service central (harnais) possède la mémoire, les autorisations, les rappels et la file de travaux. Un service d’exécution sur Windows reçoit les tâches autorisées, utilise Ollama et les outils locaux et renvoie les résultats. Chaque tâche a un identifiant et un état durable.

**Phase 1 — PC Windows.** Développer et valider l’ensemble sur le PC seul. L’interface web, le harnais, la mémoire, les rappels, la file de travaux, Ollama et les outils d’exécution fonctionneront sur cette machine. Le NAS ne constitue aucun prérequis pour cette phase.

**Phase 2 — Migration du service central.** Une fois la version PC validée, vérifier la compatibilité du Synology, sauvegarder l’état du service central, suspendre ses écritures sur le PC, puis restaurer cet état sur le NAS. Reconnecter le service d’exécution Windows et vérifier une conversation, un rappel et une tâche avant de réactiver les traitements. Une seule instance du planificateur doit être active. Les modèles et les espaces d’exécution restent sur le PC.

Après la migration, si le PC dort, l’interface hébergée sur le NAS peut consulter les données existantes, accepter une demande et déclencher les rappels déjà programmés si leur canal est disponible. Les tâches nécessitant le PC restent en attente. À chaque étape validée, enregistrer le résultat, les modifications locales utiles et la prochaine étape. Après une interruption, vérifier les effets déjà produits avant toute reprise.

## Dimensionnement et disponibilité

Le poste prévu est un PC Windows doté d’une RTX 3080 de 10 Go de VRAM et de 32 Go de RAM. Le stockage annoncé est d’environ 1 To. Relever l’espace réellement libre, le processeur, les modèles installés et leur version lors de l’inventaire. Lors de la préparation de la phase 2, consigner le modèle du Synology, sa mémoire disponible et sa capacité à héberger le service central.

La justesse prime. Pour une question courante, viser une réponse courte en 30 à 60 secondes, chargement initial mesuré séparément. Pour une refonte complexe, une durée allant jusqu’à deux jours est acceptable si le travail progresse et reste récupérable. Comparer sur une même tâche un modèle compact chargé principalement sur le GPU et un modèle quantifié plus grand réparti entre GPU et RAM. Mesurer l’exactitude, le temps total, la mémoire maximale et la réactivité du PC. Le disque conservera les modèles, les projets et les points de reprise. Les tailles et délais utilisables seront déterminés sur le poste réel.

Pour un travail long, prévoir une file persistante, un état consultable et la possibilité de servir une question courte entre deux étapes. Un point de reprise inclut la version des fichiers, les changements validés, les vérifications effectuées et la prochaine action. Dans une installation entièrement sur le PC, sa mise en veille suspend aussi le service central.

## Inventaire à maintenir

| Élément | Source de restauration prévue |
| --- | --- |
| Application, services, dépendances et scripts | Version étiquetée du dépôt, fichier Compose, lanceur Windows, versions des images et prérequis matériels |
| Mémoire et activité | Sauvegarde cohérente de la base avec conversations, préférences, permissions, rappels, tâches et points de reprise |
| Fichiers de travail | Sauvegarde des documents, pièces jointes, résultats et travaux en cours du PC, y compris les changements non publiés |
| Modèles et agents | Profils et réglages sauvegardés, identifiants et versions des modèles. Archiver les poids difficiles à retrouver |
| Accès privés | Sauvegarde chiffrée distincte ou procédure de réautorisation. Prévoir une clé de récupération accessible après perte du NAS |

Conserver une copie récupérable hors des appareils à remplacer. Associer chaque sauvegarde à sa date, à la version de JARVIS et à son inventaire. Le tableau d’état prévu affichera les versions, les services joignables, les modèles disponibles, la dernière sauvegarde et la date de la dernière restauration vérifiée.

## Remplacement d’un appareil

| Panne simulée | Démarche de remise en service à valider |
| --- | --- |
| Perte du PC | Réinstaller le service d’exécution et Ollama sur le poste de remplacement, récupérer les modèles et les changements locaux sauvegardés, autoriser le poste auprès du harnais et reprendre une tâche témoin. |
| Perte du NAS | Déployer la version compatible du service central sur le nouveau NAS ou temporairement sur le PC. Restaurer la base, les fichiers et les accès depuis la copie indépendante, puis reconnecter le poste de calcul. |
| Perte des deux appareils | Reconstruire le service central à partir du dépôt et de la sauvegarde indépendante, puis rattacher un poste de calcul neuf. Vérifier ensemble l’inventaire et les fonctions restaurées. |

## Exercice de reprise

Sur une cible vierge, récupérer la version compatible, restaurer la base et les fichiers, reconnecter les accès puis démarrer les services. En environnement de vérification, suspendre les notifications et publications réelles pour éviter les doublons. Relire une conversation connue, ouvrir une pièce jointe, contrôler un rappel et reprendre un projet témoin au dernier point validé. Mesurer le temps de remise en service et l’ancienneté des dernières données récupérées. Ces résultats serviront à fixer les objectifs de reprise.
