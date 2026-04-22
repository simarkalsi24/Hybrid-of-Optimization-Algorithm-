# Hybrid Metaheuristic Optimization for CNN-based Leaf Disease Classification

## 📖 Overview

This repository explores the impact of hybrid metaheuristic optimization algorithms on the performance of Convolutional Neural Networks (CNNs) for plant leaf disease classification.

The core idea behind this work is simple:

> If individual optimization algorithms can improve CNN performance, what happens when we combine them?

To answer this, a consistent CNN architecture was trained and optimized using different hybrid combinations of metaheuristic algorithms. The objective was to evaluate whether hybrid strategies can improve convergence, stability, and accuracy compared to standalone methods.

---

## 🎯 Motivation

In earlier experiments (available in a separate repository), individual optimization algorithms such as:

- Ant Lion Optimization (ALO)  
- Whale Optimization Algorithm (WOA)  
- Dragonfly Algorithm (DA)  
- Particle Swarm Optimization (PSO)  

were used to tune CNN hyperparameters.

While these algorithms improved performance, each has its own strengths:
- Some are better at **exploration** (global search)
- Others are better at **exploitation** (local refinement)

This led to the key question:

> Can combining these algorithms create a better balance between exploration and exploitation?

This repository is an attempt to systematically explore that idea.

---

## 🧠 Approach

A unified framework is followed across all experiments:

1. A lightweight CNN model is defined  
2. Hyperparameters (learning rate, dropout) are optimized  
3. Metaheuristic algorithms evaluate candidate solutions  
4. Best parameters are selected  
5. Final model is retrained and evaluated  

Each hybrid method follows a two-phase strategy:

- **Phase 1 → Exploration**
- **Phase 2 → Exploitation**

---

## 📂 Repository Structure

---

## Hybrid Codes for Algorithm

- ALO + Whale Optimization  
- ALO + Dragonfly Algorithm  
- ALO + PSO Algortihm
- PSO + Whale Optimization  

Each implementation maintains a consistent CNN backbone and evaluation strategy.

## Keras files for model loading

- hybrid_alo_da_best_model
- hybrid_alo_pso_best_model
- hybrid_alo_woa_best_model
- hybrid_pso_woa_best_model
---

## 📊 Key Observations

- Hybrid optimization improves performance over standalone algorithms  
- Phase-based hybridization leads to stable convergence  
- Even with a small search budget, strong results are achieved  
- Lightweight CNN performs effectively when properly optimized  


---

## 📌 Note

This repository focuses on hybrid optimization strategies.  
Standalone optimization implementations are available in a separate repository.
