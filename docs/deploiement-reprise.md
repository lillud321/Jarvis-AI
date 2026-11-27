# Déploiement et reprise prévus

## Une application, deux installations possibles

Une interface web privée dessert le PC et le téléphone. Le service central (harnais) possède la mémoire, les autorisations, les rappels et la file de travaux. Un service d’exécution sur Windows reçoit les tâches autorisées, utilise Ollama et les outils locaux et renvoie les résultats. Chaque tâche a un identifiant et un état durable.

Pour le premier essai, les deux services peuvent tourner sur le PC. La cible proposée place le service central sur le Synology sous réserve de vérifier son modèle, sa mémoire disponible et la compatibilité de Container Manager. Les mêmes réglages de connexion permettent de déplacer un composant. Le lancement Windows et le déploiement conteneurisé du service central sont des livrables à construire.

Si le PC dort, l’interface hébergée sur le NAS peut consulter les données existantes, accepter une demande et déclencher les rappels déjà programmés si leur canal est disponible. Les tâches nécessitant le PC restent en attente. À chaque étape validée, enregistrer le résultat, les modifications locales utiles et la prochaine étape. Après une interruption, vérifier les effets déjà produits avant toute reprise.

## Inventaire à maintenir

| Élément | Source de restauration prévue |
| --- | --- |
| Application, services, dépendances et scripts | Version étiquetée du dépôt, fichier Compose, lanceur Windows, versions des images et prérequis matériels |
| Mémoire et activité | Sauvegarde cohérente de la base avec conversations, préférences, permissions, rappels, tâches et points de reprise |
| Fichiers de travail | Sauvegarde des documents, pièces jointes, résultats et travaux en cours du PC, y compris les changements non publiés |
| Modèles et agents | Profils et réglages sauvegardés, identifiants et versions des modèles. Archiver les poids difficiles à retrouver |
| Accès privés | Sauvegarde chiffrée distincte ou procédure de réautorisation. Prévoir une clé de récupération accessible après perte du NAS |

Conserver une copie récupérable hors des appareils à remplacer. Associer chaque sauvegarde à sa date, à la version de JARVIS et à son inventaire. Le tableau d’état prévu affichera les versions, les services joignables, les modèles disponibles, la dernière sauvegarde et la date de la dernière restauration vérifiée.

## Exercice de reprise

Sur une cible vierge, récupérer la version compatible, restaurer la base et les fichiers, reconnecter les accès puis démarrer les services. En environnement de vérification, suspendre les notifications et publications réelles pour éviter les doublons. Relire une conversation connue, ouvrir une pièce jointe, contrôler un rappel et reprendre un projet témoin au dernier point validé. Mesurer le temps de remise en service et l’ancienneté des dernières données récupérées. Ces résultats serviront à fixer les objectifs de reprise.
