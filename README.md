# Prediction Based on Accelerometer Signals

## Overview
This project involves the differentiation between 20 mobile device users based on accelerometer signals using various machine learning models. The project was completed as part of the Practical Machine Learning course at the Faculty of Mathematics and Information Technology, University of Bucharest.

## Project Structure

- **Task**:
  - The objective is to classify 20 users based on accelerometer data from their mobile devices. Each user has 450 signal recordings, with each recording being 1.5 seconds long at 100 Hz, resulting in 150 values per recording. The signals contain values for the x, y, and z axes.
  - The dataset consists of 9,000 labeled samples for training and 5,000 unlabeled samples for testing.

- **Exploratory Data Analysis and Pre-processing**:
  - **Signal Consistency**: The dataset was checked for null values and inconsistencies in signal length. Signals with more than 150 values were trimmed, while those with less were padded either by mean values or by the last entry, with the latter method proving more effective.
  - **Class Encoding**: The classes, originally labeled from 1 to 20, were shifted left by 1 (0 to 19) for compatibility with neural network models.
  - **Label Distribution**: The classes were evenly distributed, each having 450 samples.
  - **Signal Normalization**: Both normalized and original signals were compared, but no significant accuracy difference was found, so original signals were used for training.

- **Model Building and Training**:
  1. **Neural Network**:
     - A neural network with 3 hidden layers was implemented. After hyperparameter tuning using KFold cross-validation and RandomSearch, the network achieved 91% accuracy on the training set and 55% accuracy on the test set.
  
  2. **Convolutional Neural Network (CNN)**:
     - A CNN was built with 4 convolution layers, followed by pooling, dropout, and dense layers. This model achieved 99% validation accuracy and 60% test accuracy.
  
  3. **Support Vector Machine (SVM)**:
     - An SVM model was also implemented. After hyperparameter tuning using grid search, the SVM achieved 85% test accuracy and 67% validation accuracy, outperforming the neural network models.

## Results
- **Neural Network**: 
  - Validation Accuracy: 89%
  - Test Accuracy: 55%
  
- **Convolutional Neural Network (CNN)**: 
  - Validation Accuracy: 99%
  - Test Accuracy: 60%
  
- **Support Vector Machine (SVM)**:
  - Validation Accuracy: 99%
  - Test Accuracy: 67%
  
The SVM model produced the best results in terms of both validation and test accuracy.

## How to Run
1. **Clone the Repository**:
    ```bash
    git clone https://github.com/madalin312/accelerometer_signal_classification
    ```
2. **Install Dependencies**:
    - Ensure you have Python and the necessary libraries installed:
  
3. **Run the Project**:
    - You can execute the cells in the jupyter notebook using a Python kernel.

## Bibliography
- [Kaggle PML 2022 - Smart Device Competition](https://www.kaggle.com/competitions/pml-2022-smart/)

## Author
- **Radu Madalin-Cristian**, University of Bucharest, Faculty of Mathematics and Information Technology


