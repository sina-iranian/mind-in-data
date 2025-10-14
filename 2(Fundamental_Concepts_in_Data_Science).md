# 📊 Statistical & Distribution Foundations for Data Analytics

## 1️⃣ Descriptive Statistics
- **Types of Data**
  - *Categorical* → groups (e.g., brand, color)
  - *Numerical* → measurable values  
    - Discrete (countable) Continuous (measurable)
- **Levels of Measurement**
  - Nominal (no order) Ordinal (has order)
  - Interval (no true 0) Ratio (has true 0)
- **Central Tendency**
  - Mean = AVERAGE() Median = MEDIAN() Mode = MODE.SNGL()
- **Dispersion**
  - Variance (σ² or s²) Standard Deviation (σ or s)  
  - Sample vs Population formulas differ by n vs n–1
- **Shape**
  - Skewness → asymmetry direction (use =SKEW())  
- **Relationships**
  - Covariance = COVARIANCE.S() Correlation = CORREL()  
  - Corr ∈ [–1, 1] → strength + direction of relation
- **Visualization**
  - Bar / Pie / Pareto (for categories)  
  - Histogram (for numeric bins)  
  - Scatter plot (for bivariate relation)

---

## 2️⃣ Probability Essentials
- **Basics:** P(A) = favorable / total outcomes  
- **Complement:** P(A′) = 1 – P(A)  
- **Union:** P(A ∪ B) = P(A)+P(B)–P(A ∩ B)  
- **Conditional:** P(A | B) = P(A ∩ B) / P(B)  
- **Independent:** P(A | B)=P(A)  
- **Bayes’ Theorem:** P(A | B) = [P(B | A) P(A)] / P(B)  
- **Expected Value:** E(X)=Σ x · P(x) (measure of average payoff)

---

## 3️⃣ Probability Distributions
### 🔹 Discrete
| Distribution | Notation | Mean | Variance | Use |
|---------------|-----------|------|-----------|-----|
| Uniform | Y ~ U(a,b) | (a+b)/2 | (b–a)²/12 | Equal outcomes |
| Bernoulli | Y ~ Bern(p) | p | p(1–p) | Single trial |
| Binomial | Y ~ B(n,p) | n p | n p (1–p) | n Bernoulli trials |
| Poisson | Y ~ Po(λ) | λ | λ | Events / time or space |

**Poisson proof insight:** E(Y)=λ Var(Y)=λ.

---

### 🔹 Continuous
| Distribution | Notation | Mean | Variance | Key Insight |
|---------------|-----------|------|-----------|--------------|
| Normal | Y ~ N(μ, σ²) | μ | σ² | Symmetric bell curve; 68% within ±1σ |
| Standard Normal | Z=(Y–μ)/σ | 0 | 1 | Enables Z-scores |
| t (Students) | Y ~ t(k) | μ | s² k/(k–2) | Small-sample Normal approx. |
| χ² (Chi-Squared) | Y ~ χ²(k) | k | 2k | Goodness-of-fit tests |
| Exponential | Y ~ Exp(λ) | 1/λ | 1/λ² | Waiting time model |
| Logistic | Y ~ Logistic(μ,s) | μ | (s² π²)/3 | Models binary outcomes |

---

## 4️⃣ Normal Distribution Key Formulas
- PDF:  f(y)= (1 / (σ√(2π))) e^{−(y–μ)² / (2σ²)}  
- E(Y)=μ  Var(Y)=σ²  
- Standardization:  z = (y – μ)/σ  
- 68-95-99.7 rule:  ≈ 68% within 1σ, 95% within 2σ, 99.7% within 3σ

---

## 5️⃣ Integrals & Expected Value (Continuous Case)
- **Expected Value:**  E(Y)=∫ y · f(y) dy  
- **Variance:**  Var(Y)=E(Y²)–[E(Y)]²  
- Integration tools (Wolfram Alpha etc.) can numerically compute E(Y) or P(a < Y < b).

---

## 6️⃣ Applied Example – Finance Payoff
- Expected payoff E(P)=Σ (probability × outcome)  
- Example: 0.4×250 + 0.6×0 = $100 → accept deal if premium < $100.  
Shows how probability supports rational decision-making.

---

## 7️⃣ Analytical Mindset for Data Analytics
1. **Describe** → summarize data (Descriptive Stats)  
2. **Model** → assign probabilities (Distributions)  
3. **Infer** → estimate and predict (Bayesian/Statistical Inference)  
4. **Decide** → use expected values for rational choices  

Together, these topics build the statistical reasoning every data analyst needs.
