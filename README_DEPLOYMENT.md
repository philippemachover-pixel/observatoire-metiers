# Observatoire des métiers - version GitHub Pages

Contenu du dossier à déposer à la racine du repository GitHub :

- `index.html` : page principale du site ;
- `app_data_part1.js` : première partie des données ;
- `app_data_part2.js` : seconde partie des données ;
- `app_salary_data.js` : fourchettes de salaires indicatives par métier ;
- `tools/build_salary_data.mjs` : générateur permettant de reconstruire `app_salary_data.js` ;
- `ft_logo.png` : logo utilisé par les liens France Travail ;
- `.nojekyll` : fichier vide évitant que GitHub Pages applique un traitement Jekyll inutile.

Important : les fichiers `app_data_part1.js`, `app_data_part2.js` et `app_salary_data.js` doivent être dans le même dossier que `index.html`.

Ordre de chargement dans le HTML :

```html
<script src="app_data_part1.js"></script>
<script src="app_data_part2.js"></script>
<script src="app_salary_data.js"></script>
```

Pour reconstruire les fourchettes de salaires à partir des données Insee :

```bash
node tools/build_salary_data.mjs
```

GitHub Pages cherchera automatiquement un fichier `index.html` placé à la racine de la source de publication.
