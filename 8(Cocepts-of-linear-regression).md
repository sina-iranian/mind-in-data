🔹 1️⃣ VIF — Variance Inflation Factor

What it means:
VIF tells you whether two (or more) independent variables in your regression are too similar or correlated.

If two predictors carry almost the same information, the model gets confused — it can’t tell which one actually influences the target (this problem is called multicollinearity).

Simple example:
You’re predicting car price using both:

Engine size (in liters)

Horsepower

Since horsepower and engine size are highly related, both increase together.
This redundancy inflates their “variance” → your model becomes unstable.

How to interpret VIF:

VIF Value	Meaning
1	Perfect — no correlation
1–5	Moderate correlation (OK)
> 5	High correlation (remove or fix)
> 10	Serious multicollinearity problem ⚠️

✅ Goal: keep VIF values low so that each predictor adds unique information.

### 🔹 2️⃣ MSE — Mean Squared Error

**What it means:**  
MSE measures how far your model’s predictions are from the real values — on average.

\[
MSE = \frac{1}{n} \sum (y_i - \hat{y}_i)^2
\]

- **yᵢ** → actual value  
- **ŷᵢ** → predicted value  

You **square** the errors to punish large mistakes more heavily.  
MSE is great when you want to be extra sensitive to big prediction errors.

**Example:**  
If your model predicts \$25,000 for a car that costs \$35,000 →  
the 10k error becomes \(10{,}000^2 = 100{,}000{,}000\) in MSE.

✅ **Smaller MSE = better model fit**  
⚠️ **Sensitive to outliers**, since big errors are squared.

---

### 🔹 3️⃣ MAE — Mean Absolute Error

**What it means:**  
MAE measures the average size of errors, without squaring them.

\[
MAE = \frac{1}{n} \sum |y_i - \hat{y}_i|
\]

It’s basically the **average absolute difference** between predicted and actual values.

---

### ⚖️ Key Difference Between MSE and MAE

| Metric | Description | Outlier Sensitivity |
|---------|--------------|--------------------|
| **MSE** | Squared errors (focuses on large mistakes) | High |
| **MAE** | Average absolute errors (equal weight) | Low |

✅ Use **MAE** when outliers exist or all mistakes should count equally.  
✅ Use **MSE** when you want to **strongly penalize big mistakes**.


🔹 4️⃣ F-Regression — Feature Significance Test

What it means:
F-regression checks which independent variables (features) are actually useful in explaining your target.

It performs a mini regression for each variable separately and gives two numbers:

F-statistic: strength of relationship

p-value: probability the variable adds no value

How to read results:

Variable	P-value	Decision
SAT Score	0.000	Keep (strong predictor)
Random Column	0.67	Drop (not useful)

✅ Low p-value (< 0.05) → feature is significant
⚠️ F-regression tests variables individually — it doesn’t consider interactions between them.

Think of it as a filter to remove irrelevant features before final modeling.

🔹 5️⃣ Regularization — Keeping the Model in Check

What it means:
Regularization prevents overfitting by adding a penalty to large coefficients (model weights).
It forces the model to stay simple, stable, and generalizable.

Analogy:
Imagine you’re fitting a line to data.
Without regularization → model tries too hard to fit every point (wavy line).
With regularization → smoother, simpler line that generalizes better.

🧮 Two Main Types
Type	Formula	Effect	Use Case
L1 (Lasso)	`Loss + λΣ	w	`
L2 (Ridge)	Loss + λΣw²	Keeps all weights small → stabilizes model	Multicollinearity control
Elastic Net	Combination of L1 + L2	Balances between selection and stability	Mixed datasets

λ (lambda): regularization strength → higher = more penalty.

✅ Helps avoid overfitting
✅ Makes coefficients more interpretable
✅ Often improves test accuracy even if training accuracy drops slightly


## 🔹 6️⃣ Homoscedasticity vs. Heteroscedasticity

**Meaning:**  
These terms describe the **spread of residuals (errors)** in your regression model.

### 🧮 Homoscedasticity
All residuals have **constant variance** — errors are evenly spread along the prediction line.

**Example:**  
Predicting car prices → error size is about the same for cheap and luxury cars.

✅ This is **good** — it’s one of the core assumptions of linear regression.

### ⚠️ Heteroscedasticity
Residuals’ variance **changes** — errors get larger or smaller as predicted values increase.

**Example:**  
Your model predicts cheap cars accurately but is very wrong for expensive cars → error variance grows with price.

**Why it’s bad:**
- Violates regression assumptions.  
- Coefficients remain unbiased, but **standard errors and p-values become unreliable**.  
- Makes it harder to trust hypothesis testing and confidence intervals.

**Detection:**
- Plot residuals vs. fitted values → look for a cone or funnel shape (bad).  
- Use statistical tests like **Breusch–Pagan test**.

**Fixes:**
- Apply a **log transformation** to target or predictors.  
- Use **weighted least squares** or **robust standard errors**.

---

## 🧩 Summary Table

| Concept | Purpose | Key Takeaway |
|----------|----------|--------------|
| **VIF** | Detects correlated predictors | Keep VIF < 5 for stability |
| **MSE** | Measures squared error | Punishes large mistakes |
| **MAE** | Measures absolute error | Robust to outliers |
| **F-Regression** | Finds significant features | Keep variables with p < 0.05 |
| **Regularization** | Reduces overfitting | Simplifies model (L1, L2) |
| **Homoscedasticity** | Constant residual variance | Ideal regression assumption |
| **Heteroscedasticity** | Unequal residual variance | Causes unreliable inference |

---

✅ **In Short:**
> A well-behaved regression model should have  
> - Low VIF, low error (MSE/MAE)  
> - Statistically significant features (F-test)  
> - Regularization to prevent overfitting  
> - Homoscedastic (stable) residuals for trustworthy predictions
