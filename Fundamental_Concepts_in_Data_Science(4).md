# 📊 Hypothesis Testing, Python & Regression — Core Data Analytics Notes

*(Based on course materials 21–25 — key concepts every data analyst must know.)*

---

## 🧪 1️⃣ Hypothesis Testing

### 🔹 The Scientific Approach
Data-driven decision-making follows the scientific method: observe → measure → hypothesize → test → conclude.

### 🔹 Key Terms
| Concept | Meaning |
|----------|----------|
| **Hypothesis** | A claim or assumption that can be tested statistically. |
| **Null Hypothesis (H₀)** | Status quo — no effect or no difference. |
| **Alternative Hypothesis (H₁)** | Opposes H₀ — claims there is an effect or difference. |
| **Significance Level (α)** | Probability of rejecting a true H₀ (common: 0.10, 0.05, 0.01). |
| **p-Value** | Probability of observing data as extreme as current sample, assuming H₀ is true. |

### 🔹 Decisions
| Decision | Condition | Interpretation |
|-----------|------------|----------------|
| **Reject H₀** | p < α | Sufficient evidence for change/effect. |
| **Fail to Reject H₀** | p ≥ α | No strong evidence; retain status quo. |

### 🔹 Types of Errors
| Error | Description | Symbol |
|--------|--------------|---------|
| Type I | Rejecting a true H₀ (false positive) | α |
| Type II | Failing to reject a false H₀ (false negative) | β |

Reducing α decreases false positives but increases risk of missing true effects.

### 🔹 Test Statistic Formulas
| Case | Statistic | Formula |
|------|------------|----------|
| One mean (σ known) | Z | (x̄ − μ₀) / (σ / √n) |
| One mean (σ unknown) | T | (x̄ − μ₀) / (s / √n) |
| Two independent means (σ known) | Z | ((x̄₁ − x̄₂) − μ₀) / √(σ₁²/n₁ + σ₂²/n₂) |
| Two independent means (σ unknown, equal var.) | T | ((x̄₁ − x̄₂) − μ₀) / √(sp²/n₁ + sp²/n₂) |
| Paired samples | T | (d̄ − μ₀) / (sd / √n) |

### 🔹 One- vs Two-Tailed Tests
- **Two-tailed:** check for any difference (≠)  
- **One-tailed:** check for directional effect (> or <)

### 🔹 Visual Logic
Critical regions (tails) mark where extreme results occur.  
If your test statistic falls inside → reject H₀.

---

## 🧮 2️⃣ Using an Online P-Value Calculator
1. Enter **test statistic** (Z or T).  
2. Choose **tail type** (one- or two-tailed).  
3. Input **degrees of freedom** if using T.  
4. Click calculate → get **p-value** and **decision**.

✅ **Interpretation**
- p < 0.05 → Reject H₀ (significant)
- p ≥ 0.05 → Fail to reject H₀ (not significant)

---

🔹 Built-ins PYTHON for Analytics

len(), sum(), max(), min(), type(), round(), abs(), int(), float(), str()


