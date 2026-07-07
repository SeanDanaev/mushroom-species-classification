# 🍄 Mushroom Classification — Edible or Poisonous?

Comparing four machine learning classification algorithms to determine whether a mushroom
is edible or poisonous, using the UCI Mushroom Dataset from Kaggle.

**Dataset:** [Mushroom Classification — Kaggle](https://www.kaggle.com/datasets/uciml/mushroom-classification/data)  
8,124 entries × 23 features (all categorical)

---

## 📌 Project Overview

Mushroom toxicity classification is a safety-critical problem where misclassification
has real consequences. This project evaluates four classification algorithms across
multiple performance metrics to identify the most reliable and generalizable model
for this task.

---

## 🔧 Tools & Libraries

- **Python** — Pandas, NumPy
- **Visualization** — Matplotlib, Seaborn
- **Modeling** — Scikit-learn (KNN, Decision Tree, Random Forest, Logistic Regression)
- **Evaluation** — Confusion Matrix, Accuracy, Precision, Recall, F1-Score

---

## 📊 Workflow

1. **Data Loading & Cleaning** — categorical column inspection, one-hot and label encoding,
   null value check
2. **Exploratory Data Analysis** — distribution plots, target class balance check,
   correlation analysis per column
3. **Modeling** — 80/20 train/test split, four algorithms trained and evaluated
4. **Visualization** — confusion matrices and bar charts comparing Precision, Recall,
   and F1-Score across all models
5. **Model Selection** — final recommendation with reasoning

---

## 📈 Results

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| K-Nearest Neighbors | 100% | 1.00 | 1.00 | 1.00 |
| Decision Tree | ~99.99% | 1.00 | ~0.9999 | ~0.9999 |
| Random Forest | 100% | 1.00 | 1.00 | 1.00 |
| Logistic Regression | 100% | 1.00 | 1.00 | 1.00 |

---

## 💡 Key Takeaways

- KNN, Random Forest, and Logistic Regression all achieved perfect scores across every
  metric. Decision Tree produced a single misclassification, resulting in a marginal
  drop in recall.
- The near-perfect performance across models can be attributed to the dataset's high
  separability and low noise, combined with effective preprocessing through one-hot and
  label encoding — conditions that allowed both linear and non-linear models to capture
  the decision boundary cleanly.
- Despite all models performing exceptionally well, **Random Forest is recommended as
  the final model** for practical use: its ensemble approach reduces the risk of
  overfitting, and its built-in feature importance ranking makes it more interpretable,
  robust, and scalable than the alternatives.

---

## 🗂️ Dataset Features (23 columns)

All features are categorical. Key columns include:

| Column | Description |
|---|---|
| `class` | Target: `e` = edible, `p` = poisonous |
| `odor` | Smell (almond, anise, foul, spicy, etc.) |
| `gill-color` | Color of the gills |
| `spore-print-color` | Color of the spore print |
| `habitat` | Environment (woods, grasses, urban, etc.) |
| `population` | Abundance (solitary, scattered, abundant, etc.) |
| `cap-shape` | Shape of the cap (bell, convex, flat, etc.) |
| `cap-color` | Color of the cap |
| `bruises` | Whether the mushroom bruises under pressure |
| `veil-type` | Veil type — all values identical (`partial`), dropped as uninformative |

*Full column descriptions with all categorical values are documented inside the notebook.*

---

## 🚀 How to Run

1. Clone this repository
2. Download the dataset from the [Kaggle link](https://www.kaggle.com/datasets/uciml/mushroom-classification/data)
   and place `mushroom.csv` in the project folder
3. Open `mushroom_classification.ipynb` in Jupyter or Google Colab
4. Run all cells in order
