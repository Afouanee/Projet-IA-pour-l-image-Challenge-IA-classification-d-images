# CLAUDE.md

Contexte pour un futur agent travaillant sur ce dépôt.

## Contexte

Projet académique ESIEE Paris (E5, module Challenge IA). Objectif : comparer deux
approches de classification d'images (chien vs chat) : Bag of Visual Words (vision
classique) et un CNN (deep learning).

## Structure

- `RK_Image_Classification_Bag_of_Visual_Words.py` — pipeline complet BoVW :
  extraction de descripteurs ORB (`cv2`), dictionnaire visuel par k-means (`scipy`),
  histogrammes de mots visuels, classification `LinearSVC` (scikit-learn). Script
  linéaire, pensé pour être exécuté cellule par cellule (issu d'un notebook converti).
- `cnn.py` — CNN Keras (`Sequential`, `Conv2D`/`MaxPooling2D`/`Dense`), entraîné via
  `ImageDataGenerator.flow_from_directory` sur une arborescence `dataset/training_set`
  / `dataset/test_set` avec sous-dossiers par classe.
- `MNIST.ipynb` — notebook d'exploration ORB/keypoints, une seule cellule. Corrigé
  pour être syntaxiquement valide (imports propres, plus de `???`), mais reste un
  brouillon d'exploration, pas un pipeline complet.
- `Bases Kaggle_ImageNet .ipynb` — notebook vide (2 cellules sans contenu), jamais
  rempli.
- `Rapport_projet.docx` et le PDF associé — livrables écrits du projet.

## Datasets

Aucun dataset n'est inclus dans le dépôt (taille, droits de redistribution Kaggle).
Les scripts attendent une arborescence locale `dataset/training_set/<classe>/` et
`dataset/test_set/<classe>/` (convention Keras `flow_from_directory`) qu'il faut
recréer manuellement à partir des sources citées dans le README (Dogs & Cats, Intel
Image Classification, MNIST).

## Limites connues

- Pas de `requirements.txt` : versions des libs (OpenCV, Keras, scikit-learn, scipy)
  non figées.
- Aucun des scripts/notebooks n'est exécutable tel quel sans le dataset local.
- `MNIST.ipynb` reste un brouillon (une cellule d'exploration ORB), pas un pipeline
  MNIST complet malgré son nom.
