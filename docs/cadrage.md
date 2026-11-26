# Cadrage de JARVIS

**État du livrable 2 — réflexion amorcée, premier usage à choisir.**

## Qu’est-ce qui justifierait d’ouvrir JARVIS chaque semaine ?

Deux besoins ressortent du projet. Le premier apparaît quand on reprend un dossier après plusieurs jours et qu’il faut reconstituer les décisions déjà prises. Le second apparaît quand un service local fonctionne mal et qu’il faut consulter plusieurs interfaces pour comprendre son état. Le choix du premier besoin à traiter change ce qu’il faut installer, les données à conserver et les permissions à donner.

| Usage candidat | Première version envisageable | Comment juger son utilité |
| --- | --- | --- |
| Reprendre un projet | Saisir une décision et la prochaine action dans une fiche locale. Permettre à JARVIS de retrouver la fiche et de citer l’entrée utilisée. | Revenir quelques jours plus tard et demander « Où en étions-nous ? ». Vérifier la décision et la prochaine action dans la fiche d’origine. |
| Diagnostiquer un service | Choisir un seul service Docker et autoriser la consultation de son état. Afficher l’observation et l’heure de lecture. | Demander « Est-ce que ce service fonctionne ? ». Comparer la réponse à l’état réel et vérifier que JARVIS indique quand il manque de l’information. |

## Comment y arriver ?

**Point de départ proposé.** Commencer par la reprise d’un projet. Une seule fiche suffit pour essayer le scénario sur le PC Windows, et cet essai ne dépend d’aucun accès au NAS. Si les diagnostics reviennent plus souvent dans l’usage quotidien, le scénario Docker peut passer en premier.

1. Choisir une situation réellement vécue. Écrire la question que l’on aurait posée, la réponse attendue et ce qu’il a fallu faire pour l’obtenir aujourd’hui.
2. Examiner ce que les outils déjà présents permettent de faire sur cette même situation. Relever ce que JARVIS doit apporter de plus pour mériter son développement.
3. Définir le minimum nécessaire pour l’essai. Identifier la source des faits, le modèle local à essayer, les accès permis et les décisions qui doivent rester entre les mains de l’utilisateur.
4. Rejouer la situation avec la première version. Comparer l’exactitude de la réponse, les manipulations nécessaires et la possibilité de vérifier le résultat. Utiliser ces observations pour choisir la prochaine amélioration.

## Décisions à prendre ensemble

- Quel usage revient le plus souvent, et quel exemple concret servira de premier essai ?
- Quelles informations JARVIS peut-il conserver automatiquement ? Lesquelles veut-on relire avant de les enregistrer comme décisions ?
- Qu’est-ce qui rendrait la première version assez utile pour y revenir la semaine suivante ?

Le cadrage sera terminé lorsque le premier usage, le périmètre de la première version, les moyens nécessaires et un critère de réussite observable auront été convenus et consignés ici. La [feuille de route](feuille-de-route.md) pourra alors être ajustée à ces choix.
