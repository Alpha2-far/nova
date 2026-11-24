# NOMA — Animation de la Home

Référence : https://innovix.framer.website/ · relevé du 24 novembre 2026.

L’inventaire ci-dessous provient du HTML publié, de son bloc `__framer__appearAnimationsContent`, du module de Home et des composants de bouton, service, projet, article et compteur. Le navigateur piloté est indisponible dans cette session : il s’agit d’une lecture des paramètres publiés, pas d’une comparaison visuelle filmée.

| Effet de la référence | Paramètres publiés | Adaptation NOMA |
| --- | --- | --- |
| Titre de hero | Caractère par caractère, déplacement vertical de 10 px, durée 0,5 s, délai 0,05 s | Même découpage, 1,2 s par caractère et 45 ms entre caractères ; ensemble autour de 3 s |
| Introduction, bouton et images de hero | Opacité presque nulle et déplacement de 60 px ; durée 0,4–0,6 s | Entrées de 1,6–1,8 s, avec les éléments décalés dans le temps |
| Présentation | Texte et action depuis la droite, 50 px ; image depuis la gauche, 50 px | Texte sur 1,8 s, collage sur 2 s ; sur petits écrans, entrée verticale pour éviter les débordements |
| Image avant du collage | Décalage des éléments de présentation | Départ 250 ms après le collage arrière |
| Compteurs | Comptage numérique sur 1,5 s | De 00 à 06 en 2,4 s ; aucune autre statistique n’est ajoutée |
| Titres de sections et cartes | Entrée verticale de 50 px, opacité, courbe `(0.5, 1, 0.89, 1)` | Même direction et courbe, durée 1,6 s et décalages entre cartes |
| Service au survol | Fond sombre, aperçu d’image tourné de 7°, changement de couleurs | Même interaction avec les visuels NOMA ; transitions de 0,8–0,9 s, réservées aux pointeurs précis |
| Boutons et flèches | Variantes de couleur et deux icônes qui se remplacent | Deux flèches diagonales, changement progressif sur 650 ms |
| Carte de projet au survol | Zoom 1,1 ; voile d’opacité 0,6 ; flèche centrale | Même zoom et voile, durée 0,9–1,1 s |
| Image des cartes éditoriales | Zoom 1,1 au survol | Même zoom sur les cartes de vision NOMA, sans leur inventer de destination |
| Carrousel | Trois cartes visibles, flèches, boucle ; **autoplay et glissement manuel désactivés sur la Home publiée** | Flèches actives, boucle manuelle, déplacement de 1,8 s ; trois cartes d’approche originales ; liste statique sur mobile |
| Footer | Apparitions de contenu | Titres, action et colonnes apparaissent progressivement sans masquer le fond |

## Fonctionnement

Les effets utilisent uniquement CSS, `IntersectionObserver`, `requestAnimationFrame` et l’API Web Animations native pour le carrousel. Aucun module Framer ni aucune bibliothèque ne sont importés.

Chaque apparition se joue une seule fois. Le contenu reste affiché lorsque JavaScript ou `IntersectionObserver` est indisponible. Une préférence de réduction des mouvements active dès l’ouverture, ou modifiée pendant la visite, révèle les contenus immédiatement, arrête le compteur et restaure les cartes statiques.

Les décorations et les duplications du carrousel sont ignorées par les technologies d’assistance. Les flèches de commande sont de vrais boutons utilisables au clavier. Un élément atteint au clavier apparaît immédiatement.

## Vérification effectuée

- Syntaxe du JavaScript vérifiée avec Node.
- Observer : seuil 0,12, désinscription après la première apparition.
- Compteur : 03 à mi-parcours et 06 à la fin, sans redémarrage sur une seconde entrée.
- Arrêt des effets lorsque la préférence de réduction des mouvements change.
- Repli visible sans observer et sans animation.
- Images locales présentes et identifiants HTML uniques.

La comparaison visuelle animée sur desktop et mobile reste à réaliser lorsque l’accès au navigateur sera disponible.
