# Etape 4 . Changement de timbre de voix matrice (513,50) avec embedding.

Un notebooks pour **Essayer de transferer le timbre de voix avec un embedding** via différents modèles

## Contenu des notebooks

Le notebook (*.ipynb) inclut les étapes suivantes :

* **Prétraitement des données**.
* **Normalisation des spectrogrammes**.
* **create_mask** qui me permet de caché le padding effectué
* **Définition du/des modèles**. (Linéaire, convolutionnel, hybride, Transfomers)
* **Fonctions d’entraînement suivi d'un tester**.
* **La fonction `tester`** a pour but de visualiser les résultats (courbes, spectrogrammes, audios)
* **fonction changement_de_personne_avance** permet de changer directement les personnes que l'on veut dynamiquement 

## Structure du projet

```text
.
├── data/
│   ├── spec_pad.ipynb              # contient les données paddées
│   ├── ...                         # contient des données paddées autrements ou non
├── notebooks/
│   ├── processing.ipynb            #comment j'ai preprocessé les données
│   ├── projet_embedding.ipynb      # contient les modeles et leurs affichages
├── images/
│   ├── affichage/                  # Résultats des loss des modèles
└── README.md                       # Ce fichier
```

### les data sont dans parties et data_P3_P4
