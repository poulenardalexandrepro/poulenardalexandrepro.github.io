---
layout: default
title: "Alexandre POULENARD"
description: "BTS SIO option SLAM — Lycée Simone Weil"
---

**Recherche un stage de développement d'applications** (5 semaines, à partir du 11/01/2027).

## Présentation

Je suis étudiant de 2ème année en BTS SIO option SLAM au lycée Simone Weil. Je me forme à la conception et au développement d'applications, du modèle de données jusqu'à l'interface. J'aime les projets concrets, que je teste et que je documente. Je cherche un stage pour travailler en équipe sur un vrai projet et progresser auprès de développeurs expérimentés.

### Compétences techniques

- **Langages :** Python, PHP, JavaScript, SQL, HTML5 / CSS3, C#, Ocaml, Dart
- **Outils et frameworks :** Git / GitHub, Linux, PlantUML, Cybersécurité OWASP, API REST, Markdown, Visual Studio, Android Studio, MariaDB, NoSQL Firebase, MySQL


## Projets

### Médiathèque Les Tilleuls

![Capture d'écran de l'application [nom du projet IA]]({{ '/assets/capture-projet-ia.png' | relative_url }})

**Ce que fait l'application :** Une application web IA pour la Médiathèque Les Tilleuls qui répond automatiquement aux questions des usagers et agents d'accueil sur le règlement de la médiathèque. Le modèle de langage (Ollama) génère des réponses courtes citant les articles pertinents, résolvant ainsi le problème des 40 appels/emails hebdomadaires redondants. L'IA apporte la rapidité et la précision : réponses instantanées, calcul des pénalités de retard, et refus des demandes hors sujet..

**Mon rôle :** 
- **Backend FastAPI** (`main.py`) : routes HTTP, authentification par code d'accès, limite de requêtes par visiteur, journalisation des temps de réponse
- **Intégration Ollama** : appels à l'API de chat du modèle IA avec prompt structuré
- **Prompt détaillé** (`prompt.txt`) : vous avez écrit les règles précises (3 phrases max, citation des articles, refus des demandes hors sujet, calculs de pénalités)
- **Jeu de test exhaustif** (`cas.json`) : 11 cas couvrant le circuit nominal, les calculs avec plafond, les demandes hors sujet et les tentatives de détournement
- **Évaluation automatisée** (`evaluer.py`) : script autonome de test qui rejoint le taux de réussite et le temps médian
- **Déploiement en production** : Docker + docker-compose avec Cloudflare Tunnel pour exposer publiquement l'app avec un tunnel sécurisé.

**Technologies :**   

| Élément | Détail |  
|--------|--------|
| **Python** | 99,5 % du code (FastAPI, httpx, json, logging) |
| **API / Modèle IA** | Ollama (API `/api/chat`) — modèle `qwen2.5:3b` par défaut |
| **Framework web** | FastAPI 0.115 + Uvicorn (serveur ASGI) |
| **Base de données** | Aucune — état sans persistance (l'IA ne retient rien entre requêtes) |
| **Infrastructure** | Docker + docker-compose + Cloudflare Tunnel (accès HTTPS public) |
| **Sécurité** | Code d'accès 8+ caractères, limite 10 req/min par IP, taille d'entrée bornée (2000 caractères) |

[Voir le dépôt GitHub](https://github.com/poulenardalexandrepro/Projet_IA)


## CV et contact

<a class="btn" href="{{ '/cv/CV_POULENARD_Alexandre.pdf' | relative_url }}" download>Télécharger mon CV (PDF)</a>

- **E-mail :** [poulenardalexandre.pro@gmail.com](mailto:poulenardalexandre.pro@gmail.com)
- **LinkedIn :** [linkedin.com/in/Alexandre POULENARD](www.linkedin.com/in/alexandre-poulenard-25265b397)
- **GitHub :** [github.com/poulenardalexandrepro](https://github.com/poulenardalexandrepro)
