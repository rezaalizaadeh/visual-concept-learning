# Visual Concept Learning Across Symbolic and Object-Like Categories

This project investigates how convolutional neural networks develop internal representations of visual concepts across different domains.

Using EMNIST Letters and Fashion-MNIST, the study examines not only classification performance but also the emergence, organization, and robustness of learned representations through a series of analyses inspired by cognitive science and machine learning.

---

## Research Questions

- How do architecture and training hyperparameters affect visual concept learning?
- Do deeper layers develop more linearly separable representations?
- Does representation geometry reflect similarity between visual categories?
- Are classification errors structured or random?
- How robust are learned concepts to noise and adversarial perturbations?

---

## Datasets

| Dataset | Classes | Train | Test |
|----------|----------|----------|----------|
| EMNIST Letters | 26 | 124,800 | 20,800 |
| Fashion-MNIST | 10 | 60,000 | 10,000 |

---

## Methodology

The project combines:

- CNN model selection
- Layer-wise linear readouts
- Representation similarity analysis
- Hierarchical clustering
- Error analysis through confusion matrices
- Psychometric robustness curves
- FGSM adversarial attacks
- Adversarial fine-tuning

---

## Main Results

### EMNIST Letters

- Accuracy: **93.86%**
- Macro-F1: **93.82%**

### Fashion-MNIST

- Accuracy: **89.24%**
- Macro-F1: **89.00%**

### Linear Readouts

| Representation | Accuracy |
|---------------|-----------|
| Pixels | 61.11% |
| Block 1 | 68.50% |
| Block 2 | 92.93% |
| Block 3 | 94.04% |

These results indicate that deeper CNN layers learn progressively more separable visual representations.

---

## Repository Contents

- `visual_concept_learning.ipynb` – complete project notebook
- `figures/` – selected visualizations and results

---

## Technologies

PyTorch · NumPy · Scikit-Learn · Matplotlib · Seaborn
