# [Assist'Client]

> Projet IA — BTS SIO 2 SLAM — [Arthur CHAIZE] — octobre 2026
> **URL publique** : https://[…].trycloudflare.com — code d'accès envoyé à l'enseignant par e-mail

## 1. Concevoir

**Sujet choisi** : [1 - Assistant de FAQ]

**L'organisation (fictive) et son besoin**, en trois phrases : qui, quel problème aujourd'hui, ce que l'application change.
La médiathèque les Tilleuls reçoit trop de questions qui sont très récurrente, donc on veut créer une application pour répondre aux
clients sans avoir besoin d'harceler les employés.

**Trois cas d'usage**, sous la forme « En tant que …, je veux …, afin de … » :

1. En tant que concepteur je dois répondre au problème
2. Je veux faire gagner du temps aux employés
3. Afin de recevoir ma paye

**Ce que l'application ne fait pas** (au moins deux limites assumées) : …

## 2. Le modèle et la machine

| | |
|---|---|
| Carte graphique et mémoire vidéo (VRAM) | NVIDIA RTX 3060 TI 8 Go |
| Mémoire vive 2.2 Go |
| Modèle retenu | `qwen2.5:3b` |

## 3. Piloter — le journal

| Séance | Ce qui est fait | Ce qui a bloqué, et comment c'est réglé |
|---|---|---|
| Lundi 05/10 | … | … |
| Mardi 06/10 | … | … |

## 4. Mesurer

Jeu de **10 cas au moins** dans `cas.json`, dont au moins deux hors sujet et un qui tente de détourner les consignes.

| | Modèle retenu | Modèle comparé |
|---|---|---|
| Réussite (sur N cas × 3 essais) | … % | … % |
| Temps de réponse médian | … s | … s |

**Ce que les échecs montrent** (deux exemples commentés, et ce que vous avez changé) : …

## 5. Sécuriser

| Risque | Ce qui pourrait arriver | Mesure prise dans le projet |
|---|---|---|
| L'URL est publique | n'importe qui utilise votre PC et votre électricité | code d'accès, limite de requêtes |
| Ollama exposé | … | … |
| Détournement des consignes | … | … |
| Données personnelles | … | … |
| Secrets dans le dépôt | … | … |

## 6. Mettre en production — comment refaire

```bash
cp .env.example .env      # puis remplir
docker compose up -d --build
docker compose ps
docker compose logs tunnel
```

## 7. Usage de l'IA pendant le projet

Ce que vous avez demandé à un assistant, et ce que vous avez gardé, modifié ou refusé.
