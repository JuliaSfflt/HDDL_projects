Projet 1

Le but de ce projet est de développer un modèle capable de prédire l'artiste d'une œuvre d'art à partir de son image, dans le cadre du défi Art Challenge. Nous utiliserons un jeu de données comportant des œuvres d'art en haute et basse qualité, ainsi que des informations sur les artistes. L’objectif est de construire un réseau de neurones convolutifs (CNN) pour effectuer cette tâche de classification d'images. Ce rapport présente la démarche suivie, notamment le choix des images à étudier, l'architecture du réseau utilisée, ainsi que les différentes étapes de prétraitement et d'entraînement du modèle.


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

Après avoir séparé le jeux de donnée en une partie d'entrainement et de test, nous avons construit une architecture à 7 couches (3 d'encodeurs, 3 de décodeurs et une couche latente) et entrainer divers modèles, afin de séléctionner les hyperparamètres les plus adaptés à notre jeu de données (soit pour lesquels la perte serait la plus faible). Pour tester les performances de notre séléction et nous assurer de sa pertinence, nous avons comparé les images de test à leur reconstruction par notre CVAE. Nous avons également afficher  une représentation graphique de l'espace latent obtenu.


Enfin, nous avons générer cinq échantillons pour chaque classe de CVAE afin d'attester visuellement de la quelité de notre modèle.


Projet 3 : 

L’objectif de ce projet est d’explorer l’apprentissage auto-supervisé (Self-Supervised Learning - SSL) pour la détection d’anomalies sur des jeux de données d’images industriels. Nous avons travaillé sur deux bases de données principales : MVTec_AD avec les catégories bottle, hazelnut, capsule et toothbrush, Auto_VI avec la catégorie engine_wiring.

Afin de tirer parti des données non étiquetées, nous avons implémenté plusieurs tâches prétextes qui permettent au modèle d’apprendre des représentations latentes pertinentes :
- Colorization : reconstruction des couleurs à partir d’images en niveaux de gris,
- Inpainting : restauration de parties manquantes d’une image,
- Masked Autoencoder : reconstruction d’images à partir de patches partiellement masqués.

L’entraînement a été réalisé exclusivement sur des images sans anomalies pour permettre aux modèles d’apprendre les caractéristiques des données "conformes". Lors de l’évaluation, la reconstruction des images présentant des anomalies s’avère plus difficile pour les modèles, ce qui génère une erreur de reconstruction élevée. Cette erreur devient ainsi un indicateur pour identifier les anomalies.


Projet 4 : 

L'objectif de ce mini-projet est de comparer un RNN, un LSTM et un GRU, ainsi que les modèles plus traditionnels comme le MLP et le CNN, sur le dataset IMDB pour la tâche d'analyse de sentiments. Cela signifie qu'à partir des commentaires sur les films dans le dataset IMDB, nous cherchons à construire un modèle capable d'évaluer si un commentaire est positif ou négatif.

Pour réaliser la comparaison entre ces modèles, il est nécessaire d'expliquer et d'évaluer :

- Le choix des architectures : les types de couches, les tailles des couches et les fonctions d'activation.
- Le choix des hyperparamètres : taille des lots (batch size), taux d'apprentissage (learning rate), nombre d'époques (epochs), poids de régularisation...
- Le choix de la fonction de perte (loss function).
- Comparer le temps d'exécution des différents modèles, leur mémoire et leur précision.
   
