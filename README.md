# Hybrid Metaheuristic Optimization for CNN-based Leaf Disease Classification

## 📖 Overview

This repository explores the impact of hybrid metaheuristic optimization algorithms on the performance of Convolutional Neural Networks (CNNs) for plant leaf disease classification.

The core idea behind this work is simple:

> *If individual optimization algorithms can improve CNN performance, what happens when we combine them?*

To answer this, a consistent CNN architecture was trained and optimized using different hybrid combinations of metaheuristic algorithms. The objective was to evaluate whether hybrid strategies can improve convergence, stability, and overall accuracy compared to standalone methods.

---

## 🎯 Motivation

In earlier experiments (available in a separate repository), individual optimization algorithms such as:

- Ant Lion Optimization (ALO)  
- Whale Optimization Algorithm (WOA)  
- Dragonfly Algorithm (DA)  
- Particle Swarm Optimization (PSO)  

were applied to tune CNN hyperparameters.

While these algorithms improved performance, each has its own strengths:
- Some are better at **exploration** (global search)
- Others are better at **exploitation** (local refinement)

This led to a natural extension:

> *Can combining these algorithms create a better balance between exploration and exploitation?*

This repository is an attempt to systematically explore that idea using a unified experimental setup.

---

## 🧠 Approach

A consistent framework is followed across all experiments:

1. A lightweight CNN model is defined  
2. Key hyperparameters (learning rate and dropout) are optimized  
3. Metaheuristic algorithms evaluate candidate solutions  
4. The best configuration is selected  
5. The final model is retrained and evaluated  

Each hybrid method follows a two-phase optimization strategy:

- **Phase 1 → Exploration** (diversified global search)  
- **Phase 2 → Exploitation** (refinement of promising solutions)  

---

## 📂 Repository Structure

### 🔹 Hybrid Codes for Algorithms

This folder contains Jupyter notebooks implementing different hybrid optimization strategies:

- ALO + Whale Optimization  
- ALO + Dragonfly Algorithm  
- ALO + PSO  
- PSO + Whale Optimization  

Each implementation uses the same CNN architecture and evaluation pipeline to ensure fair comparison.

---

### 🔹 Keras Files for Model Loading

This folder contains pretrained models obtained using each hybrid approach:

- `hybrid_alo_da_best_model.keras`  
- `hybrid_alo_pso_best_model.keras`  
- `hybrid_alo_woa_best_model.keras`  
- `hybrid_pso_woa_best_model.keras`  

These models can be directly loaded for inference or further evaluation.

---

### 🔹 Results

This folder contains all experimental outputs and analysis:

- **Figures** → Training curves, confusion matrices, and performance plots  
- **CSV Files** → Logs, hyperparameter search results, and evaluation data  
- **Classification Reports & Summary** → Precision, recall, F1-score, and accuracy metrics  
- **HybridResults.ipynb** → Notebook for analysis and visualization  

---

## 📊 Key Observations

- Hybrid optimization improves performance compared to standalone algorithms  
- Phase-based hybridization leads to more stable convergence  
- Even with a limited search budget, strong results are achieved  
- A lightweight CNN architecture performs effectively when properly optimized  

---

## 📌 Note

This repository focuses specifically on hybrid optimization strategies.  
Standalone optimization implementations are available in a separate repository.
