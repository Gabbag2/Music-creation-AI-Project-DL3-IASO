# Etqpe 1 . Génération de musique 

Un ensemble de notebooks et scripts pour **essayer de générer de la musique** via des modèles RNN et VAE.



## Contenu des notebooks

Chaque notebook (*.ipynb) inclut les étapes suivantes :

* **Prétraitement des données**.
* **Normalisation des spectrogrammes**.
* **(Optionnel) split_sequence** : découpe l’audio en séquences de taille fixe.
* **Définition du/des modèles**.
* **Fonctions d’entraînement suivi d'un tester**.
* **La fonction `tester`** a pour but de visualiser les résultats (courbes, spectrogrammes, audios)


## Structure du projet

```text
.
├── notebooks/
│   ├── Rnn_simple.ipynb         # RNN basique
│   ├── Rnn_architecture.ipynb   # RNN complexifié
│   └── VAE_architecture1/2.ipynb# Deux variantes de VAE
├── data/
│   └── Spec/                    # Spectrogrammes scrappés
├── images/
│   ├── Images_Rnn/              # Résultats du RNN simple
│   └── Images_Rnn_VAE/          # Résultats du RNN complexifié
└── README.md                    # Ce fichier
```