# Architecture prévue

## Première conversation locale

L’interface transmet le message au harnais de JARVIS. Le harnais retrouve la conversation dans le stockage local, prépare le contexte puis appelle le modèle sélectionné au moyen d’un adaptateur. JARVIS enregistre la réponse et le nom du modèle utilisé dans la conversation.

| Composant | Responsabilité prévue |
| --- | --- |
| Interface en français | Choisir une conversation et un modèle, afficher les réponses et recueillir les confirmations |
| Mémoire locale | Conserver les messages, décisions et diagnostics indépendamment du modèle |
| Harnais IA | Préparer le contexte, appeler l’adaptateur et traiter la réponse ou la demande d’outil |
| Adaptateur Ollama | Communiquer avec le moteur local et signaler les modèles disponibles ou une erreur de connexion |
| Gestion des outils et permissions | Vérifier chaque opération et recueillir l’accord de l’utilisateur lorsqu’une modification est demandée |

## Profil et exemples validés

Le stockage local de JARVIS distinguera l’historique, les préférences personnelles ou propres à un projet et les exemples de travail validés. Le harnais sélectionnera les éléments pertinents pour la demande courante. L’interface permettra de consulter, corriger et supprimer une préférence. Une préférence supprimée devra cesser d’être appliquée aux nouveaux échanges.

## Changement de modèle

Passer de Qwen à Gemma dans Ollama conserve l’identifiant de la conversation. Le harnais recharge le contexte disponible et applique les mêmes permissions au prochain échange. Un futur moteur pourra être pris en charge en ajoutant un adaptateur. Si le moteur local est indisponible, l’interface le signale et conserve l’historique.

## Accès distant et rappels

L’interface distante devra rejoindre JARVIS par un accès privé authentifié. Le harnais continuera d’appliquer les permissions de l’utilisateur. Le modèle interprétera la demande de rappel. Un service de planification conservera l’échéance et déclenchera la notification indépendamment de la conversation. Le choix de l’hôte disponible aux heures prévues, du mécanisme d’accès distant et du canal de notification reste ouvert.

## Exemple de permission

« Quel est l’état du conteneur ? » peut déclencher une consultation si cet outil a été autorisé. Pour « Redémarre ce conteneur », JARVIS présente le conteneur ciblé et l’opération proposée. Seule la confirmation de l’utilisateur autorise cette opération précise.

## Espace de création local

Le harnais présentera le résultat demandé, les fichiers d’entrée et les opérations nécessaires avant d’obtenir l’accord de l’utilisateur. Un composant local fera respecter ces autorisations indépendamment du modèle, y compris pour les demandes reçues à distance. Les outils travailleront sur des copies dans un espace dédié, avec des accès limités aux fichiers, aux programmes et au réseau. Les éventuels programmes produits devront être essayés dans ce même périmètre.

L’utilisateur pourra inspecter le résultat, demander une révision, l’écarter ou confirmer son export vers une destination précise. Le choix du mécanisme d’isolation sur Windows reste à valider.

Pour une application conteneurisée, JARVIS pourra préparer le Dockerfile et, au besoin, la configuration Compose. Il proposera la cible, les ports et les volumes avant de construire l’image et de lancer le conteneur dans l’environnement de test autorisé. Un service de déploiement limitera les opérations au projet et à la cible approuvés. Le contenu généré ne recevra pas d’accès au moteur Docker de l’hôte. L’installation du moteur Docker, si elle est nécessaire, relève de la préparation de l’environnement (livrable 3).

## Intégration GitHub prévue

Une GitHub App dédiée donnera accès aux dépôts sélectionnés. Le harnais commencera en lecture seule et conservera les identifiants hors du contexte du modèle et des applications générées. Les changements seront préparés dans une copie de travail isolée. Avant publication, présenter le dépôt, la branche et les différences. La fusion vers la branche principale restera une décision distincte de l’ouverture d’une demande de fusion.

## Agents spécialisés

Sur demande, JARVIS proposera une fiche d’agent précisant sa mission, ses sources, ses outils et le résultat attendu. L’utilisateur pourra valider la fiche, la modifier ou la retirer. Le harnais pourra utiliser le même modèle local pour plusieurs rôles et transmettre à chacun le seul contexte utile. À chaque exécution, les accès seront limités aux autorisations communes à la tâche, au profil et à l’utilisateur. Les confirmations requises pour écrire ou publier resteront gérées par le harnais.

## Sélection des modèles et consultation externe

Un agent définit une mission et des outils. Le harnais peut lui attribuer différents modèles selon la tâche. Une liste locale associera les modèles disponibles aux capacités évaluées sur le PC, par exemple analyse financière et boursière, intelligence d’affaires et programmation. L’utilisateur pourra voir le choix et le modifier. Plusieurs domaines pourront partager le même modèle si les essais le justifient.

Si une tâche dépasse les capacités locales évaluées, JARVIS expliquera la difficulté et pourra proposer un second avis via un adaptateur Anthropic (Claude) ou OpenAI. Cette option sera désactivée par défaut. JARVIS préparera localement la question minimale, avec des données fictives ou agrégées si possible. Il retirera les identifiants, secrets et détails indirectement reconnaissables. Si le contexte reste identifiable, il signalera le risque et proposera de reformuler ou de rester en local.

Avant chaque transmission, afficher le fournisseur, le modèle, le motif et l’intégralité du contenu à transmettre. L’accord portera sur ce contenu exact et ce destinataire. Toute modification demandera une nouvelle confirmation. Le refus, l’absence de réponse ou l’indisponibilité du service laisseront la tâche en local. L’historique complet, les fichiers sources et le profil personnel restent hors de la requête. La consultation externe ne confère aucun accès aux outils de JARVIS.
