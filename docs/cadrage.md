# Cadrage de JARVIS

Les trois usages exprimés sont la conversation en français, la création de petites applications et l’aide à l’intégration de l’IA dans FinanceOS. Les essais ci-dessous sont des propositions de travail.

| Usage | Exemple de demande | Résultat observable |
| --- | --- | --- |
| Poser des questions et poursuivre la discussion | « À quoi sert une clé primaire en SQL ? » puis « Montre-moi avec une table de clients. » | La réponse de suivi reprend le sujet et donne un exemple correct en français. Si la voix est retenue, l’essai commence au microphone. |
| Créer une petite application puis la modifier | « Crée une page pour noter les scores de deux équipes. » Puis demander un bouton pour corriger le dernier point. | Ouvrir la page sur le PC, ajouter des points aux deux équipes et annuler le dernier point. L’utilisateur peut examiner les fichiers proposés avant leur enregistrement. |
| Aider à intégrer l’IA dans FinanceOS | « Comment expliquer les écarts entre le budget et les dépenses du mois ? » | JARVIS aide à définir l’entrée, à proposer le code d’intégration et à évaluer un prototype sur des données fictives. Chaque montant de l’explication doit pouvoir être rapproché du rapport source. |

## Chemin proposé

Commencer avec une conversation locale. L’essai de suivi vérifie que le modèle reçoit le contexte. Le choix entre clavier, microphone et réponse lue à voix haute détermine les logiciels à prévoir lors de l’installation.

Utiliser ensuite cette conversation pour décrire une petite application à une seule fonction. Une page HTML autonome permet de vérifier rapidement si JARVIS comprend une demande, produit une application utilisable et sait la modifier après un premier essai.

Pour FinanceOS, commencer par choisir une fonctionnalité qui gagnerait à utiliser l’IA. Pour l’exemple des écarts budgétaires, FinanceOS calculerait les totaux et les écarts. Le modèle local recevrait les agrégats nécessaires et proposerait une explication. Comparer cette explication aux chiffres avant de décider si elle mérite une place dans l’application. JARVIS pourrait aider à écrire et réviser ce code quel que soit le modèle choisi pour FinanceOS.

## Questions encore ouvertes

- La première conversation doit-elle permettre de taper, de dicter une question ou de tenir un échange vocal complet ?
- Quelle petite application et quelle fonctionnalité de FinanceOS serviront de premiers essais ?
- Quelles informations conserver d’une session à l’autre, et quelles écritures présenter pour confirmation ?

La reprise de dossiers et les diagnostics Docker restent des usages ultérieurs. La [feuille de route](feuille-de-route.md) situe ces travaux dans le projet.
