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

L'objectif de ce projet est d'étendre nos connaissances acquises sur les autoencodeurs variationnels (variational autoencoders ou VAE) aux autoencodeurs variationnel conditionnel (conditional variational autoencoders ou CVAE). Dans les deux cas, ces modèles sont utilisés pour la génération d'images ; l'apport du second est que l'utilisateur peut spécifier la classe de l'image qu'il souhaite générer (conditionnement). 

Dans le cadre de ce projet, nous avons utilisé le jeu de données *Fashion MNIST*, lequel est composé de 70 000 images en niveaux de gris représentant des articles de mode répartis en 10 catégories : 
- T-shirt/top
- Pants
- Pullover
- Dress
- Coat
- Sandal
- Shirt
- Sneaker
- Bag
- Ankle boot.

Après avoir séparé le jeux de donnée en une partie d'entrainement et de test, nous avons construit une architecture à 7 couches (3 d'encodeurs, 3 de décodeurs et une couche latente) et entrainer divers modèles, afin de séléctionner les hyperparamètres les plus adaptés à notre jeu de données (soit pour lesquels la perte serait la plus faible). Pour tester les performances de notre séléction et nous assurer de sa pertinence, nous avons comparé les images de test à leur reconstruction par notre CVAE.

Enfin, nous avons générer 


Projet 3 : 
L’objectif de ce projet est d’explorer l’apprentissage auto-supervisé (Self-Supervised Learning - SSL) pour la détection d’anomalies sur des jeux de données d’images industriels. Nous avons travaillé sur deux bases de données principales : MVTec_AD avec les catégories bottle, hazelnut, capsule et toothbrush, Auto_VI avec la catégorie engine_wiring.

Afin de tirer parti des données non étiquetées, nous avons implémenté plusieurs tâches prétextes qui permettent au modèle d’apprendre des représentations latentes pertinentes :
- Colorization : reconstruction des couleurs à partir d’images en niveaux de gris,
- Inpainting : restauration de parties manquantes d’une image,
- Masked Autoencoder : reconstruction d’images à partir de patches partiellement masqués.

L’entraînement a été réalisé exclusivement sur des images sans anomalies pour permettre aux modèles d’apprendre les caractéristiques des données "conformes". Lors de l’évaluation, la reconstruction des images présentant des anomalies s’avère plus difficile pour les modèles, ce qui génère une erreur de reconstruction élevée. Cette erreur devient ainsi un indicateur pour identifier les anomalies.


   
