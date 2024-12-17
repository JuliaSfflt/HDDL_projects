Objectif de fin (date):
- Projet 1 : 27 octobre
- Projet 2 : 17 novembre
- Projet 3 : 1 décembre
- Projet 4 : 15 décembre


Projet 1

1) Problème de classification: On choisit d'utiliser un CNN car les données sont des images et on veut conserver leur structure (ie sans flatten)
   Pensez à redimensionner les images. On choisit d'entrainer le réseau sur les images en high quality pour minimiser les pertes associées au redimensionnement. On pourra aussi comparer les performances high et low quality par la suite.
   Attention aux catégories après le split
   Utiliser le data augmentation pour les catégories qui ont moins de _________ images.
3) Problème du nombre d'image pour les artistes qui n'en ont pas peint assez pour que l'apprentissage "fonctionne"

Projet 2 : 
résumé 

Projet 3 : 
L’objectif de ce projet est d’explorer l’apprentissage auto-supervisé (Self-Supervised Learning - SSL) pour la détection d’anomalies sur des jeux de données d’images industriels. Nous avons travaillé sur deux bases de données principales : MVTec_AD avec les catégories bottle, hazelnut, capsule et toothbrush, Auto_VI avec la catégorie engine_wiring.

Afin de tirer parti des données non étiquetées, nous avons implémenté plusieurs tâches prétextes qui permettent au modèle d’apprendre des représentations latentes pertinentes :
- Colorization : reconstruction des couleurs à partir d’images en niveaux de gris,
- Inpainting : restauration de parties manquantes d’une image,
- Masked Autoencoder : reconstruction d’images à partir de patches partiellement masqués.

L’entraînement a été réalisé exclusivement sur des images sans anomalies pour permettre aux modèles d’apprendre les caractéristiques des données "conformes". Lors de l’évaluation, la reconstruction des images présentant des anomalies s’avère plus difficile pour les modèles, ce qui génère une erreur de reconstruction élevée. Cette erreur devient ainsi un indicateur pour identifier les anomalies.


   
