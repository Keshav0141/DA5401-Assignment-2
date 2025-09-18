# 🎬 DA5401 Assignment 2 – PCA: Dimensionality Reduction, Visualization, and Classification

### 👨‍🎓 Student Info  
**Name:** Aryan Prasad  
**Roll Number:** DA25M007  

---

## 📌 Assignment Objective  
The goal of this assignment is to explore **dimensionality reduction using PCA** and evaluate its effect on classification:  

- Perform one-hot encoding & standardization on the Mushroom dataset.  
- Apply **Principal Component Analysis (PCA)** to reduce dimensionality.  
- Compare **Logistic Regression performance** on the original data vs. PCA-transformed data.  
- Deliver insights on the trade-off between dimensionality reduction, variance retention, and classification performance.  

---

## 🧾 Hypothesis  
Reducing high-dimensional, redundant categorical features into a smaller set of principal components can **preserve classification performance** while eliminating collinearity and improving efficiency.  

---

## 📂 Dataset  
- **Target variable:** `class` → edible (`e`) or poisonous (`p`).  
- **Features:** Entirely categorical, expanded into **55 one-hot encoded features**.  

---

## 🛠️ Part A: Data Preprocessing  
- Performed **one-hot encoding** of categorical features.  
- Applied **StandardScaler** to normalize the binary-encoded features.  
- Prepared feature matrix `X_scaled` and target vector `y`.  

---

## 📊 Part B: PCA & Visualization  
- Applied PCA without specifying components initially.  
- Generated **scree plot** (explained variance per component + cumulative variance).  
- Identified optimal number of PCs needed to capture ~95% variance.  
- Projected dataset into **2D PCA space** and visualized separability of edible vs poisonous mushrooms.  

---

## 🤖 Part C: Logistic Regression – Performance Evaluation  

### Baseline Model (Original Features)  
- Trained on all **55 standardized features**.  
- Achieved near-perfect classification metrics (Accuracy, Precision, Recall, F1).  

### PCA-Transformed Model  
- Trained on PCA-reduced features.  
- With **21 PCs (~67% variance retained)**, the model achieved ~99.9% accuracy, nearly identical to the baseline.  
- Accuracy plateaued beyond 21 PCs, showing that additional components provided no performance benefit.  

---

## 📖 The Data Story  
1. State hypothesis: PCA reduces dimensionality while preserving class-separating information.  
2. Apply preprocessing → one-hot encoding & scaling.  
3. Perform PCA → visualize explained variance & select components.  
4. Compare Logistic Regression on original vs. PCA data.  
5. Conclude on the trade-off between variance retention and performance.  

---

## 🔍 Key Insights  
- **Accuracy vs Components:**  
  - With <10 PCs → accuracy low (~87–96%).  
  - With ~21 PCs → accuracy peaks (~99.9%).  
  - With all 55 PCs (~95% variance) → no improvement over 21 PCs.  
- **Dimensionality reduced:** 55 → 21 features.  
- **Variance trade-off:** Only ~67% variance retained, but enough for perfect class separation.  
- **PCA benefits:** Removed collinearity & redundancy, produced a compact representation with no loss in predictive performance.  

---

## 🏁 Conclusion  
- PCA successfully reduced the feature space while preserving classification accuracy.  
- Only the **class-relevant variance** is needed — remaining variance represents redundancy or noise.  
- Logistic Regression confirmed PCA’s effectiveness as a dimensionality reduction tool in high-dimensional categorical datasets.  

---  
