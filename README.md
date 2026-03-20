# Deep Generative Modeling for Label Noise Detection

This project proposes a deep generative approach to detect noisy labels in image datasets.

## 🚀 Overview

Noisy labels are common in real-world datasets and can degrade model performance.  
We model the data generation process using a latent-variable generative model and detect label noise via posterior inference.

**Key ideas:**
- Treat **clean label** as a latent variable
- Model **observed label** via a corruption process
- Use **variational inference** to estimate label consistency

---

## 🧠 Method

**Generative process:**

- y ~ p(y)  
- z ~ N(0, I)  
- x ~ p(x | y, z)  
- ỹ ~ p(ỹ | y)

**Noise score:**

s(x, ỹ) = 1 - q(y = ỹ | x)

Higher score → more likely to be a noisy label

---

## 📊 Results

- Dataset: CIFAR-10  
- Noise types:
  - Symmetric noise  
  - Asymmetric noise  

**ROC-AUC:**
- Original: 0.612  
- Fixed-C: 0.638  
- Final: **0.720**

---

## 📂 Project Structure
