# Extra Trees vs Random Forest Comparison

## Overview

This document compares **ExtraTreesClassifier (Extremely Randomized Trees)** and **RandomForestClassifier**, focusing on their splitting strategies and computational performance.

---

## (a) Splitting Strategy

### Random Forest

* At each node:

  * A random subset of features (`max_features`) is selected.
  * For each selected feature, **all possible split thresholds** are evaluated.
  * The split that **optimizes the chosen criterion** (e.g., Gini, entropy) is selected.

**Characteristics:**

* Greedy optimization
* Lower bias
* Higher computational cost per split

---

### Extra Trees

* At each node:

  * A random subset of features is selected.
  * For each feature, **random split thresholds** are generated.
  * The best split is chosen **only among these random candidates**.

**Characteristics:**

* Higher randomness
* Slightly higher bias
* Reduced variance
* Lower computational cost

---

### Key Differences

| Aspect              | Random Forest               | Extra Trees       |
| ------------------- | --------------------------- | ----------------- |
| Feature selection   | Random subset               | Random subset     |
| Threshold selection | Optimal (exhaustive search) | Random thresholds |
| Randomness level    | Moderate                    | High              |
| Bias                | Lower                       | Slightly higher   |
| Variance            | Higher                      | Lower             |

---

## (b) Speed Comparison

### Training Time

**Random Forest:**

* Slower training
* Requires evaluating many split candidates per feature
* Computationally intensive

**Extra Trees:**

* Faster training
* Avoids exhaustive search for best splits
* Reduced computation at each node

---

### Prediction Time

* Both models:

  * Traverse all trees
  * Aggregate predictions (majority voting)

**Conclusion:**

* Prediction speed is generally **similar** for both methods
* Minor differences may arise due to tree depth or ensemble size

---

### Summary Table

| Phase            | Random Forest | Extra Trees |
| ---------------- | ------------- | ----------- |
| Training Speed   | Slower        | Faster      |
| Prediction Speed | Similar       | Similar     |

---

## Practical Takeaways

* **Use Extra Trees when:**

  * Training speed is important
  * Dataset is large or high-dimensional
  * Overfitting needs to be reduced

* **Use Random Forest when:**

  * More precise splits are required
  * Slightly better accuracy is desired

---

## Conclusion

Extra Trees introduce additional randomness in the splitting process, which reduces variance and improves training efficiency at the cost of slightly increased bias. Random Forests, by contrast, prioritize optimal splits, often achieving marginally better accuracy but at higher computational expense.
