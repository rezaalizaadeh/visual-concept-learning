#Visual Concept Learning

This repository contains my project on visual concept learning with convolutional neural networks. The main idea was not only to train a classifier, but also to look inside the model and understand how its internal representations change from the first layers to the deeper layers.

The project uses two visual datasets: EMNIST Letters and Fashion-MNIST. EMNIST was used as the main dataset because handwritten letters are close to symbolic visual categories, while Fashion-MNIST was used as a second dataset to compare the results with more object-like categories.

What I investigated

The project focuses on a few main questions:

* how a CNN learns visual categories from raw images;
* whether deeper layers become more useful for classification;
* which classes are confused more often by the model;
* how the learned representations are organized;
* how robust the model is when the input images are corrupted by noise or adversarial perturbations.

Datasets

The main dataset is EMNIST Letters, which contains handwritten letters from A to Z. I also used Fashion-MNIST, which contains grayscale images of clothing categories.

For both datasets, I used the original test set only for final evaluation. The training set was split into training and validation subsets for model selection.

Model

I used a compact convolutional neural network with three convolutional blocks. The model gradually transforms the input image into higher-level feature representations, which are then used for classification.

I also compared a few architecture and hyperparameter choices before selecting the final model.

Analysis

After training the model, I performed several analyses:

* final test evaluation with accuracy and macro-F1;
* confusion matrices to inspect the most common errors;
* linear readouts from different layers to measure how class information changes across the hierarchy;
* clustering and similarity analysis of the learned representations;
* feature and activation visualization;
* psychometric curves by adding increasing Gaussian noise to the test images;
* adversarial robustness analysis using FGSM attacks;
* adversarial fine-tuning as a simple robustness improvement.

Main results

On EMNIST Letters, the final model reached about 93.9% test accuracy and 93.8% macro-F1.

On Fashion-MNIST, the model reached about 89.2% test accuracy and 89.0% macro-F1.

The linear readout analysis showed a clear improvement across layers:

Representation	Accuracy
Pixels	61.11%
Block 1	68.50%
Block 2	92.93%
Block 3	94.04%

This suggests that deeper layers learned more separable and useful representations for visual classification.

Main observations

The model showed systematic confusions between visually similar classes. For EMNIST, common errors included pairs such as I/L and G/Q. For Fashion-MNIST, most errors happened between visually similar clothing categories, such as shirts, coats, pullovers, and dresses.

The robustness experiments showed that performance decreases gradually when Gaussian noise is added, while adversarial perturbations produce a much stronger drop. After adversarial fine-tuning, the model became noticeably more robust against FGSM attacks.

Tools

* Python
* PyTorch
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

Author

Reza Mahin Mohammadalizadeh
University of Padua
