# Etqpe 3 . Changement de timbre de voix matrice (1025,90).

Un notebooks pour **Essayer de transferer le timbre de voix matrice** via différents modèles

## Contenu des notebooks

Le notebook (*.ipynb) inclut les étapes suivantes :

* **Prétraitement des données**.
* **Normalisation des spectrogrammes**.
* **split_sequence** : découpe l’audio en séquences de taille fixe.
* **un one_hot** : (avoironehot) Pour pouvoir changer le style.
* **create_mask** qui me permet de caché le padding effectué
* **Définition du/des modèles**. (Linéaire, convolutionnel, hybride, Transfomers)
* **Fonctions d’entraînement suivi d'un tester**.
* **La fonction `tester`** a pour but de visualiser les résultats (courbes, spectrogrammes, audios)


## Structure du projet

```text
.
├── notebooks/
│   ├── P3_convolution.ipynb      
│   ├── P3_linéaire.ipynb      
│   ├── P3_hybride.ipynb    
│   ├── test_transformers_.ipynb     
├── images/
│   ├── reconstrucions/   # Résultats des modeles linéaire et hybride
│   ├── reconstrucions/conv/   # Résultats du modele convolutionel
│   ├── changement/conv/   # Résultats du changement de style du modèle convolutionel
└── README.md                    # Ce fichier
```

### les data sont dans parties et data_P3_P4
