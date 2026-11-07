# Fiche de cadrage : Questions sur le règlement intérieur

> Remplir chaque rubrique en une à trois phrases. Les rubriques marquées (obligatoire) sont vérifiées par `pytest`.

## Besoin en une phrase (obligatoire)

Permettre de poser une question en langage naturel sur le règlement intérieur (absences, retards, sanctions, examens) et d'obtenir une réponse qui cite l'article concerné.

## Utilisateur final (obligatoire)

L'étudiant ou le membre du personnel qui cherche une règle précise sans lire tout le document, ainsi que l'administration qui reçoit moins de questions répétitives.

## Approche retenue (obligatoire)

Cocher une seule case :

- [ ] Règles métier
- [ ] Machine learning
- [x] RAG
- [ ] Modèle génératif seul

## Justification (obligatoire, citer au moins deux critères de la grille : (a) données étiquetées, (b) vérifiabilité, (c) coût par requête, (d) conséquence d'une erreur)

J'ai choisi le RAG car (b) la réponse s'appuie sur des extraits du règlement et cite l'article, donc l'utilisateur peut vérifier la source, et (d) une réponse inventée sur une sanction ou un examen pourrait induire l'étudiant en erreur. De plus, (c) le coût par requête reste faible, car on ne réentraîne aucun modèle quand le règlement change.

## Données nécessaires et leur origine (obligatoire)

Le texte officiel du règlement intérieur, fourni par l'établissement (PDF ou Word), découpé en passages par article. Il faut aussi une vingtaine de questions types avec l'article attendu pour évaluer le système.

## Métrique de succès et seuil d'acceptation (obligatoire)

Part des questions de test pour lesquelles l'article cité est le bon, avec un seuil à fixer (par exemple au moins 90 %). Le système doit aussi répondre « je ne sais pas » quand aucun article ne correspond.

## Conséquence d'une erreur et validation humaine prévue (obligatoire)

Une mauvaise réponse peut faire croire à une règle qui n'existe pas. L'outil indique toujours la source et précise que le texte officiel fait foi ; en cas de doute, l'utilisateur contacte l'administration.

## Risques éthiques ou de confidentialité (obligatoire)

Le règlement est un document public en interne, mais les questions posées peuvent révéler des situations personnelles (sanction, absence) : il faut éviter de les enregistrer avec l'identité de la personne.

## Approche écartée et pourquoi (facultatif)

Le modèle génératif seul, car il pourrait inventer des articles ou des sanctions sans source vérifiable.