# NOMA — Home responsive en HTML/CSS

Ouvrir `index.html` dans un navigateur. Tous les visuels et la police sont locaux ; aucun framework, JavaScript ou service externe n’est requis.

Pour servir la page depuis ce dossier :

```sh
python3 -m http.server 4173 --bind 127.0.0.1
```

Puis ouvrir `http://127.0.0.1:4173/`.

## Fichiers

- `index.html` : contenu et structure sémantique de Home.
- `styles.css` : styles, couleurs, typographie et proportions desktop.
- `assets/` : logos, recadrages NOMA, six concepts fictifs et police Inter.
- `REFERENCE-PROPORTIONS.md` : relevés de la capture de référence.
- `PAPER-PLAN.md` : état de la maquette Paper.

La version desktop reprend les valeurs utilisées pour construire Paper, dont la largeur de 1440 px et les bandes verticales totalisant 8237 px à cette largeur. Des règles à 1199, 1023, 767 et 359 px adaptent les colonnes, la typographie, les images et le footer aux petits écrans. Sur mobile, les quatre entrées de navigation restent visibles sous le logo ; l’action du header prend la forme d’un cercle accessible. Le footer HTML est complet, y compris les éléments que la limite MCP avait empêché d’ajouter à Paper.

Les liens vers About, Pages, Contact, les services, le portfolio, le journal et les projets pointent vers leurs futures pages `.html`. Ces pages ne sont pas créées dans cette étape. Le lien e-mail du footer est opérationnel. Les flèches du bloc Approche sont décoratives, comme repères visuels de la maquette.

Inter est distribuée sous la SIL Open Font License, conservée dans `assets/Inter-LICENSE.txt`.
