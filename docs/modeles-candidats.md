# Modèles candidats pour le PC Windows

Sélection du 27 novembre 2026 pour une RTX 3080 de 10 Go et 32 Go de RAM. Les rôles sont des hypothèses à vérifier. Commencer par relever le modèle déjà installé avec `ollama list` pour établir une référence.

| Modèle Ollama | Taille indicative sur disque | Premier rôle à essayer |
| --- | --- | --- |
| [qwen3.5:9b](https://ollama.com/library/qwen3.5:9b) | 6,6 à 7,6 Go selon la variante | Cerveau principal, conversation en français et choix d’un outil |
| [gemma4:e2b](https://ollama.com/library/gemma4/tags) | 4,6 à 7,5 Go selon la variante | Deuxième famille pour comparer les réponses courtes et la lecture de captures |
| [qwen3.6:27b](https://ollama.com/library/qwen3.6:27b) | Environ 17 Go pour les poids Q4_K_M, prévoir aussi les composants visuels | Analyse approfondie de rapports financiers, de mesures DAX ou de tableaux |
| [qwen3-coder:30b](https://ollama.com/library/qwen3-coder:30b) | 19 Go | Changements de code et révision sur une copie d’un projet |

## Décider sur les résultats

Comparer d’abord le modèle déjà présent et le candidat principal sur les mêmes demandes. En finance, utiliser des rapports datés, vérifier les chiffres par un calcul indépendant et demander les sources. En BI, vérifier une mesure sur les lignes et sur le total. Pour le code, vérifier le comportement modifié et les fonctions existantes. Pour la vision, inclure une valeur illisible que le modèle doit signaler.

Essayer les grands modèles un à la fois avec un contexte modéré. Relever la variante exacte, la qualité du résultat, les erreurs, les appels d’outils, le délai à froid et à chaud et la mémoire maximale. Le pilote restera sur le PC. Le second avis externe décrit dans l’architecture reste facultatif et soumis au consentement.
