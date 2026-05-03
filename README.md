# TP 2 — Perceptron multicouche (MLP)

**Université Abdelmalek Essaâdi — ENSA Al Hoceima — TDIA2-S4**  
Travaux pratiques sur les réseaux **MLP** avec TensorFlow / Keras.

## Référence du sujet

Les consignes détaillées (données, architectures imposées, hyperparamètres, métriques) sont dans le polycopié :

**`TP2-TDIA2.pdf`** — en général à la racine du dossier cours (`Deep Learning`), à côté de ce dépôt. **Lisez ce PDF en premier** : ce README ne fait que résumer la structure des notebooks du repo.

---

## Contenu du dossier

| Fichier | Thème |
|--------|--------|
| `Exercice_01_MLP_MNIST.ipynb` | Classification MNIST (784 → 128 → 64 → 10, softmax) |
| `Exercice_02_MLP_CIFAR10.ipynb` | Classification CIFAR-10 (3072 → 512 → 256 → 10) |
| `Exercice_03_MLP_Breast_Cancer.ipynb` | Classification binaire Breast Cancer Wisconsin (30 → 64 → 32 → 1, sigmoid) |
| `Exercice_04_MLP_Boston_Housing.ipynb` | Régression Boston Housing (13 → 64 → 32 → 1, MSE / RMSE) |

Un compte rendu au format PDF peut aussi être présent dans ce dossier (`*_MLP_CompteRendu.pdf`).

---

## Rappel rapide des specs (voir le PDF pour le détail officiel)

1. **MNIST** — Adam, `categorical_crossentropy`, accuracy ; 5 époques, batch 64, `validation_split=0.2`.
2. **CIFAR-10** — même famille de perte / optimiseur ; 10 époques, batch 64, validation 20 %.
3. **Breast Cancer** — Adam, `binary_crossentropy`, accuracy ; 10 époques, batch 32 ; évaluation sur jeu de test.
4. **Boston Housing** — Adam, `mean_squared_error`, métrique RMSE ; 50 époques, batch 32.

---

## Environnement

- Python 3.x  
- **TensorFlow** (Keras inclus) — installer avec : `pip install tensorflow`

Les notebooks téléchargent les jeux de données au premier lancement (MNIST / CIFAR-10 via Keras ; Breast Cancer souvent via scikit-learn ; Boston peut nécessiter une source compatible avec votre version des libs — suivre les imports dans le notebook).

