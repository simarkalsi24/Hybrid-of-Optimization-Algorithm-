# Pretrained Hybrid CNN Models (.keras Files)

This folder contains the final trained CNN models obtained after applying different hybrid optimization algorithms.

Each model represents the best configuration found during the optimization phase, where learning rate and dropout were tuned using hybrid metaheuristic strategies.

---

## What these models are

After completing the optimization process in the notebooks, the CNN was retrained using the best hyperparameters. The resulting models were then saved in `.keras` format.

These are not intermediate models — they are the final versions used for evaluation on the test dataset.

---

## Available models

- hybrid_alo_da_best_model.keras  
- hybrid_alo_pso_best_model.keras  
- hybrid_alo_woa_best_model.keras  
- hybrid_pso_woa_best_model.keras  

Each file corresponds to a specific hybrid optimization approach.

---

## How to use these models

You can directly load any model using TensorFlow/Keras:

```python
from tensorflow.keras.models import load_model

model = load_model("hybrid_alo_da_best_model.keras")
model.summary()
