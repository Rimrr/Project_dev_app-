# Fiche de cadrage : Ordonnances incomplètes en pharmacie

> Remplir chaque rubrique en une à trois phrases. Les rubriques marquées (obligatoire) sont vérifiées par `pytest`.

## Besoin en une phrase (obligatoire)

Détecter automatiquement les ordonnances auxquelles il manque une information obligatoire (dosage, durée, signature, identité du patient) avant la délivrance.

## Utilisateur final (obligatoire)

Le pharmacien ou le préparateur au comptoir, qui vérifie chaque ordonnance avant de délivrer les médicaments.

## Approche retenue (obligatoire)

Cocher une seule case :

- [x] Règles métier
- [ ] Machine learning
- [ ] RAG
- [ ] Modèle génératif seul

## Justification (obligatoire, citer au moins deux critères de la grille : (a) données étiquetées, (b) vérifiabilité, (c) coût par requête, (d) conséquence d'une erreur)

J'ai choisi les règles métier car (b) chaque alerte est vérifiable par le pharmacien, qui voit exactement quel champ manque, et (d) une erreur sur un médicament peut nuire au patient, donc la logique doit rester explicite et contrôlable. De plus, (c) le coût par requête est quasi nul avec des règles.

## Données nécessaires et leur origine (obligatoire)

La liste des mentions obligatoires d'une ordonnance, issue de la réglementation pharmaceutique, et quelques ordonnances types (complètes et incomplètes) pour tester les règles.

## Métrique de succès et seuil d'acceptation (obligatoire)

Rappel des ordonnances incomplètes détectées, avec un