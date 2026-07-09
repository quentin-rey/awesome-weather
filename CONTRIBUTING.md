# Contribuer à Awesome Weather

Merci de vouloir améliorer cette liste ! Voici comment proposer une ressource.

## Avant de proposer

- Vérifiez que la ressource n'est pas déjà listée dans le [README](README.md).
- Vérifiez que le lien est fonctionnel (pas de 404, pas de redirection vers
  une page d'erreur).
- La ressource doit être utile pour la météo, le suivi de phénomènes
  météorologiques ou la veille en temps de crise (MSGU / VISOV).

## Format d'une nouvelle ressource

Chaque entrée doit suivre ce format :

```markdown
- [Nom du service][ref] - Description courte en une phrase. *Gratuit/Freemium/Payant · Zone couverte*
```

Exemple :

```markdown
- [Open-Meteo][open-meteo] - API météo simple, gratuite et rapide. *Gratuit (open source) · Monde*
```

Puis ajoutez la référence du lien à la fin du fichier, dans le bloc de liens,
par ordre d'apparition dans le document :

```markdown
[open-meteo]: https://open-meteo.com
```

### Champs attendus

- **Nom du service**
- **URL**
- **Catégorie** existante, ou nouvelle catégorie proposée si aucune ne convient
- **Gratuit / Freemium / Payant**
- **Zone couverte** (ex : France, Europe, Monde)

## Guide d'usage (optionnel)

Pour certaines ressources dont l'usage n'est pas évident en veille de crise
(lecture d'une carte, seuils à connaître, limites du service...), une page
dédiée peut être ajoutée dans [`guides/`](guides/).

Ce n'est pas systématique : réservez un guide aux ressources où une
explication apporte une vraie valeur (ex : comment lire les seuils de
[VigiCrues](guides/vigicrues.md)), pas aux ressources dont l'usage est déjà
évident (ex : consulter un bulletin météo classique).

Pour ajouter un guide :

1. Créez `guides/<slug>.md` (même slug que la référence de lien utilisée
   dans le README, ex : `vigicrues` pour `[vigicrues]`).
2. Structurez-le en sections courtes et actionnables : ce qu'on regarde,
   comment l'interpréter, les pièges ou limites à connaître en contexte de
   crise. Pas besoin d'une documentation exhaustive de l'outil.
3. Depuis le README, ajoutez `— [📖 Guide d'usage](guides/<slug>.md)` à la
   fin de la ligne correspondante.
4. Les liens et le style du guide passent par les mêmes contrôles CI
   (`link-check.yml`, `markdownlint.yml`) que le reste du dépôt.

## Ouvrir une contribution

1. Ouvrez une Issue pour discuter de l'ajout, ou proposez directement une
   Pull Request.
2. Placez la ressource dans la catégorie la plus pertinente. Si aucune
   catégorie n'est adaptée, vous pouvez en proposer une nouvelle.
3. Un workflow CI ([`link-check.yml`](.github/workflows/link-check.yml))
   vérifie automatiquement que les liens du README répondent correctement.
   Assurez-vous que votre lien passe ce contrôle avant de soumettre.

## Ce qui n'a pas sa place ici

- Les ressources payantes sans offre gratuite substantielle, sauf si elles
  sont une référence incontournable dans leur domaine.
- Les ressources non fiables, obsolètes, ou dont le contenu n'est plus
  maintenu.
- Les doublons fonctionnels d'une ressource déjà listée, sauf si l'apport
  est clairement différenciant.
