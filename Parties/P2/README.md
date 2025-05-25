# Etqpe 2 . Changement de style d'une musique 

Un notebooks pour **essayer de transferer le style d'une musique** via différents modèles

## Contenu des notebooks

Le notebook (*.ipynb) inclut les étapes suivantes :

* **Prétraitement des données**.
* **Normalisation des spectrogrammes**.
* **split_sequence** : découpe l’audio en séquences de taille fixe.
* **un one_hot** : Pour pouvoir changer le style.
* **Définition du/des modèles**. (LSTM, GRU, RNN, Transfomers, GRU_autoencoder_film)
* **Fonctions d’entraînement suivi d'un tester**.
* **La fonction `tester`** a pour but de visualiser les résultats (courbes, spectrogrammes, audios)


## Structure du projet

```text
.
├── notebooks/
│   ├── testavecajout.ipynb      # tous les modeles de changement de style testé basique
├── data/
│   └── Spec_different/          # Spectrogrammes scrappés
│   └── Spec_piano/              # Spectrogrammes scrappés
├── images/
│   ├── images_piano_to_chill/   # Résultats des modeles
└── README.md                    # Ce fichier
```