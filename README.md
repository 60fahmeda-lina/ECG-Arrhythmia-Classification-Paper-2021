ECG Arrhythmia Classification Using 1D CNN
This project implements a lightweight 1-D Convolutional Neural Network (CNN) for the early detection and classification of heart arrhythmias. By leveraging a combination of Resampling techniques and a Gaussian Mixture Model, the system achieves high accuracy with low computational complexity, making it suitable for deployment on edge devices.

 Project Overview
Heart diseases are a leading cause of death globally. This classification model aims to provide an efficient tool for medical experts to diagnose cardiovascular diseases using 1-D ECG signals.

Dataset: MIT-BIH Arrhythmia Dataset (109,446 ECG samples).
Classification: 5 classes based on AAMI standards (Normal, Supraventricular, Ventricular, Fusion, and Unknown).

Performance: Achieved an overall accuracy of 98.25%.
Metrics: F1-score of 98.24%, Precision of 97.58%, and Recall of 96.79%.

 Methodology
1. Preprocessing
The model uses specific techniques to balance the dataset and improve signal quality:

-Resampling: Combines oversampling of minority classes and undersampling of majority classes to reach 20,000 samples per class.

-White Gaussian Noise: Added for generalization of training data and to help track the R-wave peak with desired Signal-to-Noise Ratio (SNR).

2. 1-D CNN Architecture
The proposed model is a 10-layer architecture designed to be computationally light:

-3 Convolutional Layers: Extract deep features from raw ECG signals.
-3 Pooling Layers: Max pooling (sizes 3 and 2) to reduce parameters and prevent over-fitting.
-2 Dense Layers: One flattened layer followed by two dense layers.

Optimization: Uses Adam optimizer, Batch Normalization, and a Dropout rate of 0.2.

Output Layer: Uses a Softmax function for final class prediction.

📊 Results Analysis
The model was compared against several existing algorithms:

Paper	Year	Method	Classes	Accuracy:
-Joshi et al. [12]	2014	SVM	5	86.40%
-Zubair et al. [14]	2016	CNN + Softmax	5	92.70%
-Dan et al. [19]	2017	1D-CNN	5	97.50%
-Proposed Model	2021	1D-CNN + Resampling	5	98.25%

🚀 Getting Started
Prerequisites
-Python 3.x 
-TensorFlow / Keras 
-NumPy / Pandas

Installation
Clone the repository:git@github.com:60fahmeda-lina/ECG-Arrhythmia-Classification-Paper-2021.git



Bash
pip install tensorflow pandas numpy matplotlib
📁 Repository Structure

Dataset/dataset-link.txt: Link to the MIT-BIH dataset on PhysioNet.
