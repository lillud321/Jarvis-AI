# Scénarios d’essai proposés

Ces exemples permettront d’évaluer les capacités du [cadrage](cadrage.md). Les paramètres du cours de mentorat décrivent le jeu d’essai fourni. Les essais restent à réaliser.

| Usage | Exemple de demande | Résultat observable |
| --- | --- | --- |
| Poser des questions et poursuivre la discussion | « À quoi sert une clé primaire en SQL ? » puis « Montre-moi avec une table de clients. » | La réponse de suivi reprend le sujet et donne un exemple correct en français. |
| Créer une petite application puis la modifier | « Crée une page pour noter les scores de deux équipes. » Puis demander un bouton pour corriger le dernier point. | Ouvrir la page sur le PC, ajouter des points aux deux équipes et annuler le dernier point. L’utilisateur peut examiner les fichiers proposés avant leur enregistrement. |
| Aider à intégrer l’IA dans FinanceOS | « Comment expliquer les écarts entre le budget et les dépenses du mois ? » | JARVIS aide à définir l’entrée, à proposer le code d’intégration et à évaluer un prototype sur des données fictives. Chaque montant de l’explication doit pouvoir être rapproché du rapport source. |
| Travailler dans Excel | « À partir de ces lignes, comment calculer le total par projet et par période ? » | Proposer une formule ou une transformation Power Query M, expliquer où la saisir et vérifier le total sur quelques lignes fournies. |
| Travailler dans Power BI | « Pourquoi ma mesure DAX donne-t-elle le même montant pour chaque projet ? » | Demander les relations et la mesure utiles, expliquer le contexte de filtre et proposer une correction vérifiable sur deux projets et sur le total. |

## Lire, modifier et créer des fichiers

Depuis la conversation écrite, choisir un document local ou décrire le fichier à créer. Pour une modification, JARVIS présentera les changements et proposera d’enregistrer une copie après confirmation.

| Format | Lire | Modifier | Créer |
| --- | --- | --- | --- |
| Word (.docx) | Retrouver une décision dans un compte rendu et indiquer la section | Reformuler un paragraphe en conservant son style | Produire un compte rendu à partir de notes |
| Excel (.xlsx) | Expliquer une formule en indiquant la feuille et la cellule | Ajouter une colonne d’écart avec une formule par ligne | Construire un classeur budget/réel avec des totaux |
| PowerPoint (.pptx) | Résumer une présentation en citant les diapositives | Actualiser un chiffre sur une diapositive en conservant sa mise en page | Produire une présentation à partir d’un plan |
| PDF (.pdf) | Retrouver une échéance et citer la page | Annoter un passage ou réordonner des pages | Générer un rapport paginé |

Pour valider chaque format, comparer la réponse de lecture à la source, rouvrir la copie modifiée et le nouveau fichier dans leur application, puis vérifier le contenu et la mise en page. Pour Excel, vérifier aussi le recalcul des formules après un changement de valeur. Les premiers essais PDF porteront sur du texte sélectionnable. La lecture des numérisations par reconnaissance de caractères et la retouche du texte existant seront évaluées séparément.

## Analyser une image, un graphique ou un tableau

Depuis la conversation écrite, joindre une image ou sélectionner un document local, puis poser une question sur son contenu. Le harnais devra pouvoir solliciter un modèle visuel ou un outil local de reconnaissance de caractères selon le format.

| Source | Question à essayer | Vérification |
| --- | --- | --- |
| Photo d’un équipement | « Quels ports vois-tu et quelles étiquettes peux-tu lire ? » | Situer chaque élément sur la photo et signaler les inscriptions illisibles. |
| Capture d’un graphique Power BI | « À quel mois les dépenses dépassent-elles le budget ? » | Identifier les séries, les unités et les mois visibles. Distinguer une valeur affichée d’une estimation visuelle. |
| Tableau Excel ou CSV | « Quels projets ont le plus grand dépassement ? » | Calculer les écarts à partir des cellules, classer les projets et citer les colonnes ou lignes utilisées. |
| Tableau photographié ou PDF numérisé | « Reconstitue ce tableau et vérifie le total. » | Préserver les en-têtes et l’association ligne-colonne, signaler les cellules incertaines et recalculer le total lorsque les montants sont lisibles. |

## Personnalisation et progression proposées

L’utilisateur peut demander « Retiens que je travaille dans Excel en français ». JARVIS conserve cette préférence localement et la réutilise dans une prochaine conversation consacrée à Excel. Le profil doit être consultable, modifiable et effaçable. Une convention propre à FinanceOS peut être rattachée à ce projet. Si JARVIS déduit une préférence à partir d’une correction, il propose de la retenir et attend la confirmation.

Pour faire progresser une compétence, conserver des exemples validés avec leur résultat attendu. Par exemple, après la correction d’une mesure DAX, rejouer le cas sur deux projets et vérifier aussi le total. Ces exemples permettront de comparer les résultats après une évolution du harnais ou un changement de modèle. La mémoire et les exemples restent utilisables avec un autre modèle, sans exiger son réentraînement.

## Chemin proposé

Commencer avec une conversation locale. L’essai de suivi vérifie que le modèle reçoit le contexte. L’utilisateur écrit au clavier et lit la réponse à l’écran. La voix pourra faire l’objet d’un livrable ultérieur.

Utiliser ensuite cette conversation pour décrire une petite application à une seule fonction. Une page HTML autonome permet de vérifier rapidement si JARVIS comprend une demande, produit une application utilisable et sait la modifier après un premier essai.

Pour FinanceOS, commencer par choisir une fonctionnalité qui gagnerait à utiliser l’IA. Pour l’exemple des écarts budgétaires, FinanceOS calculerait les totaux et les écarts. Le modèle local recevrait les agrégats nécessaires et proposerait une explication. Comparer cette explication aux chiffres avant de décider si elle mérite une place dans l’application. JARVIS pourrait aider à écrire et réviser ce code quel que soit le modèle choisi pour FinanceOS.

## Autres usages retenus

| Capacité | Essai de validation proposé |
| --- | --- |
| Rechercher dans la bibliothèque personnelle | Retrouver une formule déjà validée dans les fichiers autorisés, citer le fichier et ouvrir le passage pertinent. |
| Apprendre avec un tuteur | Faire pratiquer les jointures SQL une question à la fois, attendre la réponse et adapter l’explication à l’erreur commise. |
| Simuler une conversation | Jouer un gestionnaire qui examine une proposition pour FinanceOS, puis donner une rétroaction fondée sur les réponses de l’utilisateur. |
| Comparer des options | Ramener trois soumissions à une base comparable et relever les coûts ou conditions à préciser. |
| Planifier une activité sous contraintes | Construire les rotations selon l’effectif, le local, le temps et les animateurs. Adapter le plan si un animateur est absent. |
| Transformer un enregistrement en suivi | Transcrire localement un extrait et associer les décisions, responsables et échéances exprimés aux passages horodatés. |
| Comparer deux versions d’un projet | Relever les changements, indiquer leur effet pour l’utilisateur et proposer des vérifications ciblées. |
| Animer des jeux et des scénarios interactifs | Faire évoluer une enquête selon les choix du groupe tout en conservant une histoire cohérente. |

## Accès à distance et rappels

Commencer une conversation sur le PC, puis la reprendre par écrit depuis un téléphone sur le réseau cellulaire. Demander « Rappelle-moi jeudi à 17 h de prendre le projecteur ». Vérifier la date et l’heure comprises, fermer la conversation et vérifier la réception sur le téléphone. Sur un second essai, reporter le rappel depuis le PC et vérifier que seule la nouvelle échéance déclenche une notification.

## Préparer une formation pour les cadets

**Demande type.** Fournir le guide pédagogique, le nombre de jeunes, leur niveau et les objectifs de l’instructeur. Préciser la durée, le matériel et les contraintes de groupe. Si une donnée manque et change la faisabilité de l’activité, la demander ou signaler l’hypothèse proposée.

1. Relever l’objectif du guide et ses points d’enseignement. Relier chaque adaptation aux objectifs de l’instructeur et signaler tout élément reporté.
2. Générer un **plan pour l’instructeur** avec le minutage, les groupes, le matériel, les consignes, les questions et une façon de vérifier les apprentissages.
3. Générer une **présentation pour les jeunes** avec les exemples, les consignes à projeter et les activités. Le format de référence est une présentation HTML utilisable hors ligne.
4. Vérifier la durée totale, la place de chaque participant et la correspondance entre les activités du plan et les diapositives. Si l’effectif change, adapter les deux supports ensemble.

**Cas de référence.** Pour l’OCOM M303.02 sur le mentorat, le guide prévoit une leçon de 30 minutes. Le plan personnalisé fourni associe cinq segments à 14 diapositives et prévoit quatre équipes de trois à cinq cadets. La présentation propose un Jeopardy du mentorat et une discussion de groupe. Ce scénario sert à vérifier que le jeu soutient l’objectif pédagogique et que le plan indique à l’instructeur quand le lancer et comment exploiter les réponses.

## Créer dans un espace contrôlé

Autoriser JARVIS à travailler sur une copie d’un classeur fictif et lui demander une petite application qui en résume les données. Prévisualiser le résultat, demander une correction, puis choisir le fichier à exporter. Vérifier que le classeur original reste intact, qu’un fichier témoin hors périmètre est inaccessible et qu’abandonner l’essai laisse le dossier de destination intact.

## Déployer une création dans Docker

Demander une petite application, approuver son déploiement dans l’environnement de test, puis ouvrir l’application à l’adresse prévue. Vérifier le résultat après redémarrage du conteneur, puis arrêter et retirer ce déploiement en préservant les autres services et les données persistantes.

## Contribuer à un projet existant

Dans FinanceOS, partir du module de rapports existant et proposer une évolution en utilisant des transactions fictives. Dans le jeu de cartes, retrouver la logique du tour et proposer une modification de règle. Dans les deux cas, vérifier que le changement suit les conventions du dépôt et que l’utilisateur peut examiner les différences avant publication.

## Créer un agent spécialisé

Demander un agent de révision Power BI qui explique une mesure DAX et propose des vérifications à partir d’un exemple fourni. Examiner son profil, l’utiliser sur deux mesures différentes, puis vérifier qu’il conserve ses consignes et que son rôle de lecture seule empêche toute modification du classeur.
