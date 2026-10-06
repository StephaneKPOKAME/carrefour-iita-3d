# Échangeur du carrefour IITA — maquette 3D interactive

Visualisation interactive d'un projet d'échangeur surélevé au carrefour IITA, à Abomey-Calavi (Bénin), l'un des carrefours les plus engorgés entre Cotonou et Calavi.

**Voir le site :** _ajouter ici l'adresse Vercel_

## Le projet

Ce site prolonge mon mémoire de licence en informatique (option Internet et multimédia, IFRI, Université d'Abomey-Calavi) : « Reconstitution 3D et compositing d'un échangeur urbain pour l'amélioration de la circulation au carrefour IITA ».

Le mémoire produisait des images et une vidéo de compositing. Sa conclusion proposait une version interactive en WebGL : ce site en est la réalisation. On peut y explorer la maquette en 3D, changer de point de vue, suivre la circulation et comparer le carrefour actuel avec le projet grâce à trois vues avant/après.

## Comment c'est fait

**Mémoire**
- Relevés de terrain : plan Google Earth, prises de vue par drone, échanges avec les usagers et les agents de circulation.
- Modélisation sous Blender : routes en courbes de Bézier, tablier extrudé le long d'une spline, piles, garde-corps, textures.
- Compositing sous After Effects : suivi de caméra avec Mocha AE, intégration des rendus, étalonnage.

**Version web**
- Baking des matériaux Blender (Cycles) pour les rendre lisibles par un navigateur.
- Optimisation du modèle : de 352 Mo et près de 8 millions de sommets à environ 9 Mo et 300 000 sommets (simplification des maillages, compression des textures).
- Reconstruction des caméras à partir des photos, puis placement des bâtiments réels du carrefour par projection de rayons.
- Affichage temps réel avec Three.js, dans une page unique sans dépendance serveur.

## Outils

Blender, Python, After Effects, Mocha AE, Three.js, glTF, OpenCV.

## Auteur

Stéphane Kpokame. Mémoire réalisé sous la supervision d'Ing. Armand Accrombessi.

Projet d'étude, sans valeur d'étude technique ou de faisabilité.
