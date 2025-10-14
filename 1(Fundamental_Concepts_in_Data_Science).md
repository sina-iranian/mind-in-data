# 🧠 Fundamental Concepts in Data Science

## 1️⃣ Combinatorics
- **Permutation:** arranging *n* distinct elements → `Pₙ = n!`
- **Variation:** choosing *p* elements from *n* when order matters  
  - With repetition → `Vₙ,ₚ = nᵖ`  
  - Without repetition → `Vₙ,ₚ = n! / (n - p)!`
- **Combination:** choosing *p* elements from *n* when order doesn’t matter → `Cₙ,ₚ = n! / [(n - p)! p!]`
- **Symmetry:** `C(n, p) = C(n, n − p)`
- **With Repetition:** `C̅ₙ,ₚ = (n + p − 1)! / [(n − 1)! p!]`
- **Applications:** lottery odds, ad selection, workout design, team formation.

---

## 2️⃣ Key Intuition
- **Permutation:** order matters, no repetition.  
- **Combination:** order doesn’t matter.  
- **With repetition:** reuse allowed.  
- **Without repetition:** one-time use only.  
- These concepts form the base for **sampling**, **probability**, and **model enumeration** in data science.

---

## 3️⃣ Bayesian Inference & Probability
- **Union:** `P(A ∪ B) = P(A) + P(B) − P(A ∩ B)`
- **Intersection:** outcomes satisfying both A and B.
- **Mutually Exclusive:** `A ∩ B = ∅`
- **Conditional Probability:** `P(A|B) = P(A ∩ B) / P(B)`
- **Independent:** `P(A|B) = P(A)`
- **Law of Total Probability:** `P(A) = Σ P(A|Bᵢ) P(Bᵢ)`
- **Multiplication Rule:** `P(A ∩ B) = P(A|B) P(B)`
- **Bayes’ Theorem:**  
  `P(A|B) = [P(B|A) × P(A)] / P(B)`
- Used for **belief updates** and **inference models** (e.g., diagnostics, spam filtering, AI reasoning).

---

## 4️⃣ Summary Insight
Combinatorics explains **how many ways** outcomes can occur.  
Bayesian inference explains **how likely** they are.  
Together they form the mathematical foundation of **data science**, **machine learning**, and **probabilistic reasoning**.
