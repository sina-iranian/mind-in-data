## 📉 4️⃣ Regression Analysis

### 🔹 Purpose
Regression quantifies how **independent variables (X)** affect a **dependent variable (Y)**.  
It’s used for **prediction**, **trend analysis**, and **explanatory modeling**.

---

### 🔹 Linear Regression Model
\[
\hat{y} = b_0 + b_1 x_1 + \varepsilon
\]

- **b₀:** intercept (baseline value)  
- **b₁:** slope (change in Y for one-unit change in X)  
- **ε:** random error term  

---

### 🔹 Correlation vs Regression

| Aspect | Correlation | Regression |
|---------|--------------|-------------|
| **Measures** | Association | Cause-effect |
| **Symmetry** | Symmetric | Directional |
| **Output** | Single r-value | Predictive equation |

---

### 🔹 Core Metrics

| Metric | Meaning | Range / Interpretation |
|---------|----------|------------------------|
| **R²** | % variance in Y explained by X | 0 → 1 |
| **Adjusted R²** | R² adjusted for number of predictors | Penalizes unnecessary variables |
| **t-stat / p-value** | Tests variable significance | p < 0.05 → significant |
| **F-statistic** | Tests overall model fit | p < 0.05 → model valid |

---

### 🔹 OLS Assumptions

| Assumption | Meaning |
|-------------|----------|
| **Linearity** | Relationship between X and Y is linear |
| **No Endogeneity** | Errors not correlated with predictors |
| **Homoscedasticity** | Constant error variance |
| **No Autocorrelation** | Errors independent across observations |
| **No Multicollinearity** | Predictors not highly correlated |

---

### 🔹 Common Methods
- **OLS (Ordinary Least Squares):** simplest, baseline estimator  
- **GLS (Generalized Least Squares):** fixes heteroscedasticity  
- **MLE (Maximum Likelihood Estimation):** optimizes parameters  
- **Bayesian Regression:** adds prior beliefs  
- **Kernel / Gaussian Processes:** nonlinear alternatives  

---

### 🔹 Interpretation
- **Intercept (b₀):** expected Y when all X = 0  
- **Slope (bᵢ):** average change in Y per 1-unit change in X  
- **p < 0.05:** coefficient statistically significant  
- **High R²:** strong explanatory power, but check for overfitting  
