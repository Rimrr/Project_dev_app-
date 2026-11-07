# Fiche de cadrage : Priorisation des avis négatifs

> Remplir chaque rubrique en une à trois phrases. Les rubriques marquées (obligatoire) sont vérifiées par `pytest`.

## Besoin en une phrase (obligatoire)

Repérer automatiquement les avis clients négatifs parmi un grand volume d'avis, afin qu'ils soient traités en priorité.

## Utilisateur final (obligatoire)

Le responsable du service client, qui doit répondre rapidement aux clients mécontents sans lire tous les avis un par un.

## Approche retenue (obligatoire)

Cocher une seule case :

- [ ] Règles métier
- [x] Machine learning
- [ ] RAG
- [ ] Modèle génératif seul

## Justification (obligatoire, citer au moins deux critères de la grille : (a) données étiquetées, (b) vérifiabilité, (c) coût par requête, (d) conséquence d'une erreur)

J'ai choisi le machine learning car (a) on dispose d'avis étiquetés positif ou négatif, ce qui permet d'entraîner un classifieur supervisé, et (c) le coût par requête est très faible une fois le modèle entraîné, ce qui permet de traiter beaucoup d'avis. De plus, (b) chaque prédiction est vérifiable en relisant l'avis.

## Données nécessaires et leur origine (obligatoire)

Un jeu d'avis clients étiquetés positif ou négatif : le jeu de démonstration généré au TP2, à compléter si possible par des avis réels anonymisés.

## Métrique de succès et seuil d'acceptation (obligatoire)

Rappel et F1-score sur la classe « négatif », mesurés sur un jeu de test séparé de l'entraînement, avec un seuil d'acceptation à fixer (par exemple au moins 85 %).

## Conséquence d'une erreur et validation humaine prévue (obligatoire)

Un avis négatif manqué reste sans réponse et peut nuire à la réputation ; un avis positif classé négatif fait seulement perdre un peu de temps. Le modèle ne fait que prioriser : un humain lit l'avis avant toute réponse.

## Risques éthiques ou de confidentialité (obligatoire)

Les avis peuvent contenir des noms ou des informations personnelles, à anonymiser. Le modèle peut aussi se tromper sur l'ironie ou certaines formulations, et ne doit pas servir à pénaliser des clients.

## Approche écartée et pourquoi (facultatif)

Les règles métier par mots-clés, car elles gèrent mal l'ironie et la variété des formulations.