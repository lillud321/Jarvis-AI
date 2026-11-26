# Cadrage de JARVIS

La première interface sera une conversation écrite en français. Les usages ci-dessous sont des points de départ. D’autres pourront être ajoutés à mesure que les besoins se précisent.

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

## Personnalisation et progression proposées

L’utilisateur peut demander « Retiens que je travaille dans Excel en français ». JARVIS conserve cette préférence localement et la réutilise dans une prochaine conversation consacrée à Excel. Le profil doit être consultable, modifiable et effaçable. Une convention propre à FinanceOS peut être rattachée à ce projet. Si JARVIS déduit une préférence à partir d’une correction, il propose de la retenir et attend la confirmation.

Pour faire progresser une compétence, conserver des exemples validés avec leur résultat attendu. Par exemple, après la correction d’une mesure DAX, rejouer le cas sur deux projets et vérifier aussi le total. Ces exemples permettront de comparer les résultats après une évolution du harnais ou un changement de modèle. La mémoire et les exemples restent utilisables avec un autre modèle, sans exiger son réentraînement.

## Chemin proposé

Commencer avec une conversation locale. L’essai de suivi vérifie que le modèle reçoit le contexte. L’utilisateur écrit au clavier et lit la réponse à l’écran. La voix pourra faire l’objet d’un livrable ultérieur.

Utiliser ensuite cette conversation pour décrire une petite application à une seule fonction. Une page HTML autonome permet de vérifier rapidement si JARVIS comprend une demande, produit une application utilisable et sait la modifier après un premier essai.

Pour FinanceOS, commencer par choisir une fonctionnalité qui gagnerait à utiliser l’IA. Pour l’exemple des écarts budgétaires, FinanceOS calculerait les totaux et les écarts. Le modèle local recevrait les agrégats nécessaires et proposerait une explication. Comparer cette explication aux chiffres avant de décider si elle mérite une place dans l’application. JARVIS pourrait aider à écrire et réviser ce code quel que soit le modèle choisi pour FinanceOS.

## Questions encore ouvertes

- Quelle petite application et quelle fonctionnalité de FinanceOS serviront de premiers essais ?
- Quelles informations conserver d’une session à l’autre, et quelles écritures présenter pour confirmation ?

La reprise de dossiers et les diagnostics Docker restent des usages ultérieurs. La [feuille de route](feuille-de-route.md) situe ces travaux dans le projet.
