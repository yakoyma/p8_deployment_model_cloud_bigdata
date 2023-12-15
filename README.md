# Projet 8 : Déployez un modèle dans le cloud

Parcours Data Scientist d'OpenClassrooms en partenariat avec CentraleSupélec.

L'objectif du projet est de développer dans un environnement Big Data une première chaîne de traitement des données qui comprend le preprocessing et une étape de réduction de dimension. L'architecture Big Data doit permettre le passage à l’échelle avec des données massives.

La source des données est la suivante : https://www.kaggle.com/datasets/moltean/fruits

La composition du jeu de données :
- Un dossier "fruits-360-dataset" comportant des images prétraitées et des images comportant plusieurs fruits.
- Un dossier "fruits-360-original-size" comportant les images origninales des fruits.


## L'architecture Big Data sur le cloud d'Amazon Web Services (AWS) est composée de 3 services :
- Le service IAM (Identity and Access Management) permet de gérer les utilisateurs.
- Le service S3 (Simple Storage Service) sert à stocker les données.
- Le service EC2 (Elastic Compute Cloud) est le serveur qui permet de réaliser les calculs.


## Les étapes de la chaîne de traitement des données :
- La configuration de la communication entre les services S3 et EC2 (utilisation du package Boto 3) et de Spark (SparkSession, Hadoop et SparkContext).
- L'importation des données dans un Spark dataframe (utilisation de PySpark, l'API Python de Spark).
- L'extraction de features par le Transfer Learning (utilisation de la librairie TensorFlow et des algorithmes de Deep Learning : réseaux de neurones convolutifs ou CNN).
- Le preprocessing (vectorisation et standardisation).
- La réduction de dimension (PCA).
- L'export et la sauvegarde du résultat de la réduction de dimension sur S3.

