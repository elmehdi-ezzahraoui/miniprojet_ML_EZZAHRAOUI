# Mini-Projet : Classification Fashion-MNIST avec un Perceptron Multicouche (MLP)

Ce projet présente l'implémentation, l'entraînement et l'évaluation d'un Perceptron Multicouche (MLP) en PyTorch sur le jeu de données **Fashion-MNIST**. Il propose une comparaison entre une approche bas niveau (*From Scratch*) et une approche modulaire (*Concise*), ainsi qu'une étude expérimentale de l'impact de la taille de la couche cachée (`num_hiddens`).

---

## 📂 Structure du Projet

```text
mini_projet_mlp_EZZAHAOUI/
├── data/
│   └── FashionMNIST/
│       └── raw/                    # Données brutes téléchargées automatiquement
├── figures/
│   ├── comparison_num_hiddens.png  # Graphique comparatif des capacités (num_hiddens)
│   └── mlp_baseline_curves.png     # Courbes de convergence du modèle de référence
├── notebooks/
│   ├── 1_MLP_FashionMNIST.ipynb    # Notebook principal (Data, Scratch, Concise, Baseline)
│   └── 2_Advanced_Experiments.ipynb # Notebook d'expérimentations avancées (Variation num_hiddens)
├── report/
│   └── rapport_DL_EZZAHAOUI.pdf    # Rapport final compilé au format PDF
├── venv/                           # Environnement virtuel Python
├── README.md                       # Documentation et guide de reproduction
└── requirements.txt                # Liste des dépendances Python
```

---

## 🛠️ Configuration et Prérequis

### 1. Activer l'Environnement Virtuel

Si vous utilisez le dossier `venv` inclus dans le projet :

* **Sous Windows (PowerShell) :**
  ```bash
  .\venv\Scripts\Activate.ps1
  ```
* **Sous Linux / macOS :**
  ```bash
  source venv/bin/activate
  ```

### 2. Installation des Dépendances

Si vous souhaitez réinstaller les dépendances dans un nouvel environnement :

```bash
pip install -r requirements.txt
```

---

## 🚀 Guide de Reproduction des Résultats

Pour reproduire l'intégralité des graphiques, logs et résultats du rapport, exécutez les deux notebooks dans l'ordre suivant :

### Étape 1 : Exécution du Notebook Principal (`notebooks/1_MLP_FashionMNIST.ipynb`)

1. **Chargement des Données :** Téléchargement automatique et pré-traitement de Fashion-MNIST ($28 \times 28$ pixels, 10 classes).
2. **Implémentation *From Scratch* & Concise :** Définition manuelle des tenseurs de poids/biais puis construction modulaire via `nn.Sequential`.
3. **Inspection Interne :** Affichage de la structure du réseau (203 530 paramètres) ainsi que des formes (*shapes*) et gradients des tenseurs.
4. **Entraînement de la Baseline :** Exécution de l'entraînement sur 10 époques (`num_hiddens = 256`, `lr = 0.1`).
   * *Résultat généré :* Exportation automatique du graphique de convergence dans `figures/mlp_baseline_curves.png`.

### Étape 2 : Exécution des Expérimentations (`notebooks/2_Advanced_Experiments.ipynb`)

1. **Variation de `num_hiddens` :** Entraînement et évaluation comparative des configurations à 64, 128, 256 et 512 neurones cachés.
2. **Génération du Comparatif :** 
   * *Résultat généré :* Exportation automatique de la courbe comparative dans `figures/comparison_num_hiddens.png`.

---

## 👤 Auteur
* **Étudiant :** EZZAHRAOUI El-Mehdi