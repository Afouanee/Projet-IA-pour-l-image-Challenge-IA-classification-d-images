# Challenge IA — Classification d'images 🖼️

> **Deux approches de classification d'images comparées : Bag of Visual Words (OpenCV + SVM) face à un CNN (Keras).**

![Python](https://img.shields.io/badge/Python-14b8a6?style=flat-square)
![Type](https://img.shields.io/badge/ESIEE-555?style=flat-square)
[![Portfolio](https://img.shields.io/badge/Portfolio-afouanee.dev-14b8a6?style=flat-square)](https://afouanee.dev/projects/ai-image-classification-challenge)

## ✨ Aperçu
Projet ESIEE autour d'un challenge de classification d'images. L'objectif est de comparer deux familles de méthodes : une approche « historique » de vision par ordinateur (Bag of Visual Words avec descripteurs locaux et SVM) et une approche par apprentissage profond (réseau de neurones convolutif). Le dépôt démontre la maîtrise du pipeline complet — extraction de caractéristiques, vectorisation, entraînement et évaluation — sur plusieurs jeux de données classiques.

## 🚀 Fonctionnalités
- **Bag of Visual Words** : extraction de descripteurs ORB (OpenCV / `cv2`), construction d'un dictionnaire visuel par k-means (scipy), puis classification avec `LinearSVC` et `StandardScaler` (scikit-learn).
- **CNN avec Keras** : modèle `Sequential` (`Conv2D`, `MaxPooling2D`, `Flatten`, `Dense`), classification binaire (activation `sigmoid`, perte `binary_crossentropy`).
- **Augmentation de données** : `ImageDataGenerator` et chargement via `flow_from_directory`.
- **Plusieurs jeux de données** : Dogs & Cats, Intel Image Classification, MNIST.

## 🛠️ Stack technique
- **Langage** : Python
- **Bibliothèques / frameworks** : OpenCV (`cv2`), scipy (k-means), scikit-learn (`LinearSVC`, `StandardScaler`), Keras, numpy, matplotlib
- **Outils** : scripts Python et notebooks Jupyter

> ⚠️ Pas de `requirements.txt` dans le dépôt : les versions des bibliothèques ne sont pas figées.

## ▶️ Lancer le projet
```bash
# Les jeux de données ne sont PAS inclus : à télécharger depuis Kaggle dans ./data/
# Approche Bag of Visual Words :
python RK_Image_Classification_Bag_of_Visual_Words.py
# Approche CNN :
python cnn.py
# Notebooks : ouvrir MNIST.ipynb ou "Bases Kaggle_ImageNet .ipynb" dans Jupyter
```

## 📂 Structure
```
cnn.py                                       # classifieur CNN (Keras)
RK_Image_Classification_Bag_of_Visual_Words.py  # pipeline ORB + k-means + SVM
MNIST.ipynb                                  # notebook d'exploration ORB/keypoints (une cellule)
Bases Kaggle_ImageNet .ipynb                 # notebook jamais rempli (cellules vides)
data/                                        # à créer : jeux de données Kaggle (non inclus)
```

> ⚠️ Les deux notebooks sont des brouillons d'exploration, pas des pipelines complets
> et documentés : `MNIST.ipynb` ne contient qu'une cellule de test ORB/keypoints (déjà
> corrigée pour être syntaxiquement valide, mais sans dataset local elle ne s'exécute
> pas), et `Bases Kaggle_ImageNet .ipynb` est resté vide. Le pipeline réellement abouti
> et documenté est `RK_Image_Classification_Bag_of_Visual_Words.py`.
