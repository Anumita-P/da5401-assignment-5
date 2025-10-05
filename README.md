

# DA5401 Assignment 5

**Visualizing Data Veracity Challenges in Multi-Label Classification**

**Name:** Anumita
**Roll No.:** BE22B004

---

## Objective

This assignment explores the challenges of real-world multi-label classification using gene expression data (Yeast dataset).
We apply **t-SNE** and **Isomap**, two non-linear dimensionality reduction techniques, to inspect data veracity issues such as:

* **Noisy / Ambiguous Labels** – points mislabeled or overlapping across classes.
* **Outliers** – unusual gene expression profiles far from main clusters.
* **Hard-to-Learn Samples** – dense mixed regions where boundaries are unclear.

---

## Dataset

* **Source:** Yeast Dataset (MULAN Repository)
* **Features (X):** 103 gene expression attributes
* **Labels (Y):** 14 functional categories (multi-label)
* **Preprocessing:** Standardization using `StandardScaler`

To simplify visualization, a new `color_label` was created with **4 categories**:

1. Top two single-label classes
2. Most frequent multi-label combination
3. “Other” category (all remaining samples)

---

## Methods

### Part A: Preprocessing

* Loaded dataset (`yeast.arff`)
* Split into **features (X)** and **labels (Y)**
* Selected categories for visualization
* Scaled features for distance-based techniques

### Part B: t-SNE & Veracity Inspection

* Applied **t-SNE** with perplexities = {5, 30, 50}
* Observed effects of varying perplexity on local vs global structure
* Identified **noisy labels, outliers, and hard-to-learn samples**

### Part C: Isomap & Manifold Learning

* Applied **Isomap (n_neighbors=10)**
* Compared global vs local preservation between Isomap and t-SNE
* Interpreted manifold complexity as **moderately curved**, not extremely twisted


---

## Technologies Used

* Python
* NumPy, Pandas
* Scikit-learn (`TSNE`, `Isomap`, `StandardScaler`)
* Matplotlib

---

