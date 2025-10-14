# 📘 Advanced Regression Concepts — Practical Data Science Notes
*(Based on uploaded lectures: Overfitting, 2D/3D Regression, Dummy Variables, F-Regression, and Final Scenario)*

---

## ⚖️ 1️⃣ Overfitting, Underfitting & Regularization

### 🔹 Model Fit Spectrum
| Term | Meaning | Problem |
|------|----------|----------|
| **Underfitting** | Model too simple; misses real patterns | Poor training & test performance |
| **Overfitting** | Model too complex; memorizes noise | High training accuracy, poor generalization |

✅ **Fixes:**  
- Use **train/test split** (e.g., 80/20).  
- Apply **Regularization** (L1 / L2).  
- Simplify model or collect more data.

### 🔹 Regularization Types
| Type | Formula | Effect |
|------|----------|--------|
| **L1 (Lasso)** | `Loss + λΣ|w|` | Shrinks weights, sets some to 0 → feature selection |
| **L2 (Ridge)** | `Loss + λΣw²` | Penalizes large weights → more stable model |

### 🔹 Core Regression Loss Functions
| Task | Function | Formula |
|-------|-----------|----------|
| Regression | **MSE** | (1/n)Σ(y−ŷ)² — penalizes large errors |
| Regression | **MAE** | (1/n)Σ|y−ŷ| — robust to outliers |
| Regression | **Huber** | Combines MSE + MAE; smooth near 0 |
| Classification | **Binary Cross-Entropy** | −(1/n)Σ[y log ŷ + (1−y) log (1−ŷ)] |
| Classification | **Hinge (SVM)** | Σ max(0, 1−y ŷ) |

---

## 🧠 2️⃣ Train–Test Split (scikit-learn)
```python
from sklearn.model_selection import train_test_split
import numpy as np

a = np.arange(1, 101)
train, test = train_test_split(a, test_size=0.2, shuffle=False, random_state=42)
