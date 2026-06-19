Visual Concept Learning

Analysis of visual concept learning in convolutional neural networks through representation learning, clustering, robustness evaluation, and adversarial analysis.

Overview

This project investigates how convolutional neural networks (CNNs) learn visual concepts and develop increasingly discriminative internal representations.

The study was conducted on two datasets:

* EMNIST Letters
* Fashion-MNIST

Beyond classification performance, the project explores representation geometry, hierarchical feature learning, robustness to noise, and adversarial vulnerability.

Key Results

Dataset	Accuracy	Macro-F1
EMNIST Letters	93.86%	93.82%
Fashion-MNIST	89.24%	89.00%

Linear Readouts

Representation	Accuracy
Pixels	61.11%
Block 1	68.50%
Block 2	92.93%
Block 3	94.04%

The results show that deeper layers learn increasingly separable visual representations.

Experiments

* CNN architecture comparison
* Linear readouts across layers
* Representation similarity analysis
* Hierarchical clustering
* Confusion matrix analysis
* Psychometric robustness curves
* FGSM adversarial attacks
* Adversarial fine-tuning

Repository

visual_concept_learning.ipynb    # Complete project notebook

Technologies

Python · PyTorch · NumPy · Scikit-Learn · Matplotlib

Author

Reza Mahin Mohammadalizadeh
University of Padua
