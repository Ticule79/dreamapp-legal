# dreamapp-legal

Les quatre pages légales de DreamApp. **Ce dépôt est public et ne contient aucun code de
l'application** — il n'existe que parce que Google exige des URL publiques et stables.

## Avant de publier

Chercher `À COMPLÉTER` dans les pages : sept blocs, pour quatre informations seulement, car
certaines doivent figurer sur plusieurs pages et y dire exactement la même chose.

- identité légale et SIRET (`confidentialite`, `conditions`, `mentions-legales`) ;
- directeur de la publication (`mentions-legales`) ;
- région d'hébergement Supabase et transfert hors UE (`confidentialite`, `mentions-legales`) ;
- **médiateur de la consommation** (`conditions`) — adhésion payante, obligatoire pour tout
  professionnel vendant à des consommateurs en France, à souscrire avant la première vente.

Les blocs à compléter s'affichent en rouge sur la page : impossible de les publier sans les voir.

## Mettre en ligne

```
cd dreamapp-legal
git init
git add -A
git commit -m "Pages légales de DreamApp"
git branch -M main
git remote add origin https://github.com/Ticule79/dreamapp-legal.git
git push -u origin main
```

Puis, sur GitHub : **Settings → Pages → Source : Deploy from a branch → main / (root)**.

Les adresses deviennent alors celles que l'application appelle déjà :

- `https://ticule79.github.io/dreamapp-legal/confidentialite`
- `https://ticule79.github.io/dreamapp-legal/conditions`
- `https://ticule79.github.io/dreamapp-legal/suppression-compte`
- `https://ticule79.github.io/dreamapp-legal/mentions-legales`

Chaque page est un dossier contenant `index.html`, pour que ces adresses sans extension
fonctionnent de façon certaine.

`404.html`, à la racine, est servi automatiquement par GitHub Pages pour toute adresse inconnue
sous `/dreamapp-legal/`. Il porte le logo, une excuse, les liens vers les quatre textes et
l'adresse de contact — pour qu'un lien cassé n'empêche jamais quelqu'un d'exercer un droit.

## Après la mise en ligne

Vérifier que les quatre adresses répondent depuis un navigateur **déconnecté de GitHub** : Play
teste l'URL sans compte, et une page privée compte comme absente.

## Si un texte change

La politique de confidentialité porte un numéro de version. Une modification de fond exige de
l'incrémenter, de dater la page, et de redemander l'accord dans l'application.
