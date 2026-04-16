# Optimisation d'un Réseau de Logistique

TP de Graphes & Réseaux — Université Paul Valéry Montpellier 3

## Description

Ce projet porte sur l'optimisation d'un réseau de livraison de colis, en partant d'une petite commune (Saint-Gély-du-Fesc) jusqu'à la métropole de Montpellier. Il couvre quatre grandes étapes progressives.

**Exercice I — Les débuts locaux**
Modélisation du réseau routier sous forme de graphe pondéré et implémentation de l'algorithme de Dijkstra pour trouver l'itinéraire le plus rapide entre l'entrepôt et un client, avec application sur les vraies données cartographiques de Saint-Gély-du-Fesc via osmnx.

**Exercice II — Passage à l'échelle**
Face à l'extension sur toute la métropole de Montpellier (~18 000 intersections), on implémente A* avec une heuristique GPS pour accélérer la recherche. Un benchmark sur 50 paires de noeuds aléatoires compare statistiquement Dijkstra et A*.

**Exercice III — Transition écologique**
Remplacement des camionnettes par des vélos-cargos électriques avec freinage régénératif. Les poids des arêtes deviennent des consommations énergétiques pouvant être négatives (descentes). On démontre l'échec de Dijkstra/A* sur ce cas et on implémente Bellman-Ford pour gérer les poids négatifs.

**Exercice IV — Optimisation des tournées**
Un livreur doit visiter N clients et revenir au dépôt (problème du voyageur de commerce). On compare le brute-force, la méthode exacte Held-Karp, l'heuristique gloutonne et l'amélioration locale 2-opt. Application finale sur 20 clients aléatoires dans Montpellier avec affichage de la tournée sur carte.

## Contenu

```
MOUTCHACHOU_lydia_Bekakria_Ahmed_exo4.ipynb   # Notebook principal
```

## Prérequis

```
pip install osmnx python-tsp numpy matplotlib requests
```

## Auteurs

- Ahmed Bekakria
- Lydia Moutchachou
