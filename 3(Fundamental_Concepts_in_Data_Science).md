# 📈 Inferential Statistics & Hypothesis Testing

## 1️⃣ Core Idea
Descriptive statistics summarize what **has happened**.  
Inferential statistics estimate what **might be true for the population**, based on a sample.

---

## 2️⃣ Key Concepts
- **Population vs Sample:** Population = all data points; Sample = observed subset.  
- **Parameter vs Statistic:**  
  - Population → parameters (μ, σ², ρ)  
  - Sample → statistics (x̄, s², r)
- **Estimator:** Formula that approximates a population parameter.  
- **Estimate:** Actual numerical result from the sample.  
- **Good estimators:** unbiased (mean = true parameter) and efficient (lowest variance).

---

## 3️⃣ The Normal Distribution (N~(μ,σ²))
- Bell-shaped, symmetric curve.  
- Mean (μ) = expected value; Variance (σ²) = spread.  
- 68–95–99.7 Rule → 68% within 1σ, 95% within 2σ, 99.7% within 3σ.  
- **Standardization:**  
  `z = (x - μ) / σ` → converts any Normal variable into a Standard Normal (mean 0, sd 1).  
- **Purpose:** compare different datasets, detect outliers, build confidence intervals, test hypotheses.

---

## 4️⃣ Central Limit Theorem (CLT)
No matter the population’s distribution, the **sampling distribution of the mean** becomes approximately **Normal** as sample size increases.  
- Mean of sampling dist.: μₓ̄ = μ  
- Variance: σ²ₓ̄ = σ² / n  
✅ Foundation of confidence intervals, hypothesis testing, and regression.

---

## 5️⃣ Confidence Intervals (CI)
A range of plausible values for a population parameter.

**General formula:**  
`x̄ ± (reliability factor × standard error)`

Where:
- For large samples (σ known): use z  
  → `x̄ ± zα/2 * (σ / √n)`  
- For small samples (σ unknown): use t  
  → `x̄ ± t(df, α/2) * (s / √n)`

**Interpretation:**  
We are (1−α)*100% confident that the true population mean lies within the interval.  
**CI width:** increases with σ and confidence level, decreases with sample size n.

---

## 6️⃣ Student’s t-Distribution
- Used when population variance is unknown or sample size is small.  
- Fatter tails than Normal → accounts for more uncertainty.  
- Notation: `t(ν)` where ν = degrees of freedom.  
- Converges to Normal as n → ∞.

---

## 7️⃣ Hypothesis Testing

### 🔹 Purpose
To make **data-driven decisions** by evaluating claims about a population.

### 🔹 Steps
1. **State hypotheses**  
   - H₀ (null): current belief or status quo  
   - H₁ (alternative): claim we want to test  
   e.g. H₀: μ = 50, H₁: μ ≠ 50  
2. **Set significance level (α)**  
   - Common choices: 0.10, 0.05, 0.01  
3. **Compute test statistic**  
   - z or t value depending on known/unknown variance.  
4. **Find p-value or critical value**  
5. **Make decision**  
   - Reject H₀ if |test statistic| > |critical| or p-value < α.  
   - Otherwise, fail to reject H₀.

---

## 8️⃣ Statistical Errors
| Type | Meaning | Symbol | Example |
|------|----------|---------|----------|
| I | Rejecting a true null (false positive) | α | Concluding a drug works when it doesn’t |
| II | Failing to reject a false null (false negative) | β | Missing a real effect |

Smaller α → fewer false positives, but higher risk of missing true effects (β ↑).

---

## 9️⃣ p-Value
- Smallest α at which we can reject H₀.  
- If **p < 0.05** → reject H₀ (statistically significant).  
- The smaller the p-value, the stronger the evidence against H₀.

---

## 🔟 Test Formulas (Summary)

| Case | Statistic | Decision Basis |
|-------|------------|----------------|
| One mean, σ known | `Z = (x̄ − μ₀) / (σ / √n)` | z-critical or p-value |
| One mean, σ unknown | `T = (x̄ − μ₀) / (s / √n)` | t-critical or p-value |
| Two means (independent, σ known) | `Z = (x̄₁ − x̄₂) / √(σ₁²/n₁ + σ₂²/n₂)` | |
| Two means (unknown, equal variances) | `T = (x̄₁ − x̄₂) / √(sp²/n₁ + sp²/n₂)` | sp² = pooled variance |
| Paired samples | `T = (d̄ − μ₀) / (sd / √n)` | |

---

## 11️⃣ Visual Interpretation
- **Two-tailed tests:** reject H₀ when result falls in extreme tails.  
- **One-tailed tests:** check directionality (>, <).  
- **p-value approach:** directly measures the strength of evidence against H₀.

---

## 12️⃣ Practical Insight for Data Analytics
- Statistical testing quantifies *evidence* instead of intuition.  
- **Confidence intervals** → quantify uncertainty in estimates.  
- **p-values** → quantify evidence strength.  
- **CLT + Normal approximation** → enable analysis on nearly any large dataset.  
- Core for: **A/B testing**, **feature evaluation**, **model validation**, and **business experimentation.**

---

✅ **Summary**
Inferential statistics bridges **sample data → population insight**.  
Hypothesis testing gives the **decision-making logic** behind all analytical conclusions.
