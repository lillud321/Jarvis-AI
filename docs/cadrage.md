# Cadrage de JARVIS

JARVIS sera un assistant local, francophone et polyvalent. La première interaction se fera par écrit. La question de cadrage est de savoir quelles capacités permettront de traiter des demandes variées et quels outils locaux les rendront utilisables.

| Capacité recherchée | Ce que le modèle doit savoir faire | Appui à prévoir dans JARVIS |
| --- | --- | --- |
| Comprendre et dialoguer | Suivre une demande et ses précisions, expliquer, enseigner, simuler un échange et demander les informations manquantes | Conversation écrite avec historique |
| Rechercher et synthétiser | Repérer les informations pertinentes, comparer des sources ou des versions et justifier sa réponse | Recherche dans les fichiers autorisés et références aux passages retrouvés |
| Interpréter plusieurs formats | Relier texte, images, graphiques, tableaux ou paroles à une question et signaler les éléments incertains | Lecture de documents, vision, reconnaissance de caractères, transcription audio locale et calcul sur les données |
| Raisonner et planifier | Tenir compte des objectifs, du public et des contraintes, comparer des options et adapter le résultat à un changement | Contexte du projet et vérifications de cohérence |
| Produire et réviser | Rédiger, proposer du code pour une petite application ou une intégration, construire des supports cohérents et les réviser sur demande | Outils de création et de modification de fichiers Word, Excel, PowerPoint, PDF et HTML, avec aperçu et confirmation |
| Personnaliser et progresser | Utiliser les préférences pertinentes et appliquer une correction à une nouvelle demande | Mémoire locale consultable et modifiable, exemples validés et essais rejouables après changement de modèle |
| Échanger à distance | Suivre une conversation commencée sur un autre appareil et conserver son contexte | Accès privé depuis un appareil autorisé, historique partagé et mêmes permissions. L’écrit reste le premier mode d’échange. |
| Gérer des rappels | Comprendre quoi rappeler et quand, reconnaître une échéance ambiguë et permettre sa modification ou son annulation | Rappels persistants, planification selon le fuseau horaire et notification sur l’appareil choisi, même lorsque la conversation est fermée. |
| Créer sur le PC dans un environnement contrôlé | Transformer une demande en résultat utilisable, le vérifier et le réviser | Construction et déploiement d’applications en conteneur Docker dans une cible autorisée, espace de travail isolé, entrées choisies, outils autorisés et validation des changements avant enregistrement dans les dossiers personnels. |
| Développer un projet existant | Comprendre le code et ses conventions, proposer une évolution ciblée et expliquer ses effets | Accès aux dépôts GitHub choisis, copie de travail locale, comparaison des changements et publication sur accord. |

Le harnais permettra de remplacer le modèle indépendamment des fichiers, de la mémoire et des permissions. Le choix du modèle et des outils se fera selon les capacités nécessaires et les résultats obtenus sur le PC Windows.

## Comment évaluer ces capacités

Le cours de mentorat permet d’en observer plusieurs ensemble. À partir d’un guide, d’un public et d’objectifs, JARVIS doit pouvoir proposer un déroulement et une présentation cohérents. Modifier l’effectif ou utiliser un autre sujet permettra de vérifier si la démarche se généralise. La durée, le jeu et le nombre de diapositives proviennent de l’exemple fourni.

Les usages envisagés pour les cadets, Excel, Power BI, FinanceOS, la création d’applications et la bibliothèque personnelle figurent dans les [scénarios d’essai](scenarios-essai.md). La priorité des premiers essais reste à choisir.
