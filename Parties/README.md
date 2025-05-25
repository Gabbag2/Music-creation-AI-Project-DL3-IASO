# Projet Deep Learning – Gabriel Rochon 

> Ce dépôt regroupe mes test en génération de sons et transfert de tonalité. Chaque partie (P1 à P4) est contenue dans un notebook pour contourner mes problèmes de GPU non reconnus par Python.
---


## 📂 Structure du projet

```text
.
├── notebooks/
│   ├── P1.ipynb                           # Partie 1 : L'essaie de géneration de nouvelles musiques (dataset scrappé)
│   ├── P2.ipynb                           # Partie 2 : L'essaie de transfert de style entre différentes musiques (dataset scrappé)
│   ├── P3.ipynb                           # Partie 3 : Premiere partie de transfert de style entre différentes personnes
│   ├── P4.ipynb                           # Partie 4 : Version finale du transfert de style
│   └── Autres/
│       └── notebooks_originals.ipynb      # Versions avec les chemins originaux si erreur dans les nouveaux path
├── data/
│   └── data_P3_P4/                        # Data telecharger de kaggle sur les voix humaines
└── README.md                              # Ce fichier
```

> **À lire en priorité :** `/P4/projet_embedding.ipynb` (version finale de la Partie 4)

---

## 📝 Description des parties

| Partie | Source des données   | Objectif                                                                          |
| :----: | ---------------------| --------------------------------------------------------------------------------- |
|   P1   | (dataset scrappé)    | Essayer de générer de nouvelles musiques                                          |
|   P2   | (dataset scrappé)    | Essayer de transferer de style entre différentes musiques                         |
|   P3   | Kaggle               | Essayer de transferer le style entre différentes personnes P1                     |
|   P4   | Kaggle               | Essayer de transferer le style entre différentes personnes avec un embedding      |

 
## Autres:

Les programmes étant assez similaire sont décrit dans chaque README
