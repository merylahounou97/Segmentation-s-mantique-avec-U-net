# Segmentation Sémantique avec U-Net

## Description
Ce projet a pour objectif de détecter le foie et les lésions hépatiques à partir d'images de coupes thoraciques en utilisant une approche de segmentation sémantique basée sur le modèle **U-Net**. Il s'appuie sur des données médicales complexes et propose une solution pour un diagnostic précis.
![image](https://user-images.githubusercontent.com/91097262/169555839-ed1b2578-e5e3-484f-a146-8ac155087ae0.png)

---

## Fonctionnalités
- **Segmentation Sémantique** :
  - Identification et détection du foie et des lésions hépatiques.
- **Prétraitement des données** :
  - Redimensionnement et normalisation des images.
  - Encodage des masques pour les différentes classes (foie, lésions, arrière-plan).
- **Entraînement et validation** :
  - Construction du modèle U-Net.
  - Calcul de métriques spécifiques : Dice Coefficient, Jaccard Coefficient.
- **Visualisation des résultats** :
  - Comparaison graphique des images originales, masques réels et prédictions.

---

## Technologies et Outils
- **Langage** : Python
- **Frameworks** : TensorFlow, Keras
- **Bibliothèques** :
  - Manipulation des données : `pandas`, `numpy`
  - Traitement des images : `pydicom`, `pynrrd`, `skimage`, `Pillow`
  - Visualisation : `matplotlib`

---

## Structure du Projet
1. **Préparation des données** :
   - Chargement des fichiers `.dcm` et `.nrrd`.
   - Prétraitement (redimensionnement, encodage des pixels).
   - Création de masques annotés pour le foie et les lésions.

2. **Développement du modèle** :
   - Architecture basée sur **U-Net** avec convolution, pooling, et couches transposées.
   - Implémentation de métriques personnalisées :
     - `dice_coef`
     - `jacard_coef`

3. **Entraînement et évaluation** :
   - Division des données en ensembles d'entraînement et de validation.
   - Entraînement avec des callbacks (EarlyStopping, ReduceLROnPlateau).
   - Évaluation des performances sur l'ensemble de validation.

4. **Visualisation** :
   - Affichage des images originales, des masques réels et des prédictions.
   - Analyse de la distribution des pixels.

---

## Résultats
- **Performances** :
  - Dice Coefficient : **0.8357**
  - Jaccard Coefficient : **0.7182**
- **Visualisations** :
  - Comparaison graphique des masques réels et prédictions.
  - Visualisation des coupes avant et après redimensionnement.

---
