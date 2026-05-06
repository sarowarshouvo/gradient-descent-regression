# Convergence Behavior of Regression Optimization Algorithms

## 📘 Overview

The project investigates how different numerical optimization methods estimate regression parameters under varying modeling assumptions. The study compares Batch Gradient Descent (BGD) and Stochastic Gradient Descent (SGD) under both Maximum Likelihood Estimation (MLE) and Bayesian formulations.

Special attention is given to convergence behavior, optimization stability, parameter recovery, and the effect of stochastic sampling strategies.

---

## 🎯 Objectives

- Study convergence behavior of gradient-based optimization algorithms
- Compare Batch Gradient Descent (BGD) and Stochastic Gradient Descent (SGD)
- Analyze SGD with and without replacement
- Implement regression optimization from scratch using NumPy
- Investigate Bayesian parameter shrinkage effects
- Compare convex and nonlinear optimization settings
- Visualize optimization trajectories and cost surfaces

---

## 📊 Dataset Description

Two synthetic datasets were generated for controlled experimentation.

### 1. Simple Linear Regression (SLR)

Model:

\[
y_i = \beta_0 + \beta_1 x_i + \epsilon_i
\]

- Samples: 120
- Noise: Gaussian
- Predictor Range: Uniform([-2,2])
- True Parameters:
  - β₀ = 2
  - β₁ = 3

This dataset provides a convex optimization benchmark.

---

### 2. Cubic Polynomial Fitting (CPF)

Model:

\[
y_i = \beta_0 + \beta_1 x_i + \beta_2 x_i^2 + \beta_3 x_i^3 + \epsilon_i
\]

- Samples: 150
- Noise: Gaussian
- Standardized predictor values
- True Parameters:
  - β₀ = 1
  - β₁ = -2
  - β₂ = 0.5
  - β₃ = 1.2

This dataset introduces a more complex nonlinear optimization landscape.

---

## 🧠 Optimization Methods

### Batch Gradient Descent (BGD)

- Uses the full dataset for each parameter update
- Produces smooth and stable convergence
- Computationally more expensive

### Stochastic Gradient Descent (SGD)

Two variants were implemented:

- SGD with replacement
- SGD without replacement

SGD introduces noisy updates but converges efficiently with lower computational cost.

---

## ⚙️ Experimental Setup

### Objective Functions

- Maximum Likelihood Estimation (MLE)
- Bayesian Log-Posterior Optimization

### Bayesian Prior

For SLR Bayesian experiments:

\[
\beta_1 \sim N(\mu_0, \tau^2)
\]

- Prior Mean: μ₀ = 0
- Prior Variance: τ² = 2

### Metrics Tracked

- Cost convergence
- Final parameter estimates
- Optimization trajectories
- Fitted regression curves
- Final objective values

---

## 📈 Key Findings

- All optimization methods successfully converged
- BGD produced the smoothest convergence curves
- SGD exhibited noisy but efficient updates
- SGD without replacement showed slightly more stable behavior
- Bayesian optimization introduced mild parameter shrinkage
- Convex SLR optimization converged faster than nonlinear CPF optimization
- Standardization improved numerical stability for polynomial regression

---

## 🛠️ Technologies Used

- Python
- NumPy
- Matplotlib
- Pandas

---

## 📂 Repository Structure

```text
├── regression_optimization.py
├── MiniProject1_Report.pdf
├── figures/
├── README.md
└── requirements.txt
```

---

## ▶️ How to Run

```bash
pip install -r requirements.txt
python regression_optimization.py
```

---

## 📎 Included Contents

- Full Python implementation
- Mathematical derivations
- Cost convergence plots
- Optimization contour visualizations
- Regression fitting comparisons
- Final parameter summary tables

---

## 👤 Author

**Saroar Jahan Shuba**  
M.S. Computational & Quantitative Methods  
Lamar University  
Spring 2026
