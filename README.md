Visual Concept Learning

This project investigates how convolutional neural networks (CNNs) learn visual concepts and develop increasingly abstract internal representations across hierarchical processing stages.

Rather than focusing only on classification performance, the project explores how information is represented inside the network, how representations evolve across layers, and how robust they are to noise and adversarial perturbations.

The work was developed as part of the Cognition and Computation course at the University of Padua.

⸻

Research Questions

This project explores the following questions:

* How do CNNs learn visual categories from raw images?
* Do deeper layers develop more useful and separable representations?
* How are visual concepts organized in representation space?
* How robust are learned representations to noise and adversarial perturbations?
* Do similar trends emerge across different visual domains?

⸻

Datasets

EMNIST Letters

* 26 handwritten letter classes (A–Z)
* 124,800 training samples
* 20,800 test samples

Fashion-MNIST

* 10 clothing categories
* 60,000 training samples
* 10,000 test samples

For both datasets, the original training split was divided into training and validation subsets, while the official test set was reserved for final evaluation.

⸻

Model Architecture

A compact hierarchical CNN was implemented with three convolutional blocks:

* Convolution Block 1 → 32 channels
* Convolution Block 2 → 64 channels
* Convolution Block 3 → 128 channels
* Final classification layer

Several hyperparameter configurations were compared before selecting the final model.

⸻

Analyses Performed

Hyperparameter Comparison

Comparison of multiple CNN configurations using validation accuracy and macro-F1 score.

Linear Readouts

Linear classifiers were trained on intermediate representations extracted from different layers to evaluate how class information emerges throughout the hierarchy.

Representation Analysis

* Cosine similarity matrices
* Hierarchical clustering
* Silhouette score evaluation

Error Analysis

Confusion matrices were used to identify systematic classification errors and visually similar classes.

Robustness Evaluation

Performance was evaluated under increasing levels of Gaussian noise.

Adversarial Robustness

FGSM attacks were used to investigate the vulnerability of learned representations.

Adversarial Fine-Tuning

A simple defense strategy was implemented and compared against the original model.

⸻

Results

EMNIST Letters

Metric	Value
Test Accuracy	93.86%
Macro F1	93.82%

Fashion-MNIST

Metric	Value
Test Accuracy	89.24%
Macro F1	89.00%

Linear Readout Accuracy

Representation	Accuracy
Pixels	61.11%
Block 1	68.50%
Block 2	92.93%
Block 3	94.04%

These results show that deeper layers progressively learn more discriminative representations.

⸻

Main Findings

* CNNs gradually transform raw visual inputs into increasingly separable feature representations.
* Representation quality improves substantially across the hierarchy.
* Visually similar categories tend to cluster together in feature space.
* Performance degrades under increasing noise and adversarial perturbations.
* Adversarial fine-tuning significantly improves robustness.
* Similar representation-learning trends emerge across both symbolic and object-like visual categories.

⸻

Technologies

* Python
* PyTorch
* NumPy
* Scikit-Learn
* Matplotlib
* Seaborn

⸻

Repository Structure

.
├── visual_concept_learning.ipynb
├── README.md
├── requirements.txt
└── figures/

⸻

Author

Reza Mahin Mohammadalizadeh

University of Padua
