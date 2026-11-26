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

## Changement de modèle

Passer de Qwen à Gemma dans Ollama conserve l’identifiant de la conversation. Le harnais recharge le contexte disponible et applique les mêmes permissions au prochain échange. Un futur moteur pourra être pris en charge en ajoutant un adaptateur. Si le moteur local est indisponible, l’interface le signale et conserve l’historique.

## Exemple de permission

« Quel est l’état du conteneur ? » peut déclencher une consultation si cet outil a été autorisé. Pour « Redémarre ce conteneur », JARVIS présente le conteneur ciblé et l’opération proposée. Seule la confirmation de l’utilisateur autorise cette opération précise.
