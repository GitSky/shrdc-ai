# Breast Cancer Prediction Using Feedforward Neural Network

## 1. Summary
- Objective: To create a highly accurate deep learning model to predict breast cancer (whether the tumour is malignant or benign).
- The model is trained with Wisconsin Breast Cancer Dataset (source: https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)

## 2. IDE and Framework
- This project is created using Google Colab as the main IDE.
- The main frameworks used are Pandas, Scikit-learn and TensorFlow Keras.

## 3. Methodology
### 3.1. Data Pipeline
1. The data is first loaded and preprocessed, such that unwanted features are removed, and label is encoded in one-hot format.
2. The data is splitted into train-validation-test sets, with a ratio of 60:20:20.

### 3.2. Model Pipeline
- A feedforward neural network is constructed that is catered for classification problem.
- The model is trained with a batch size of 16 and for 25 epochs.
- The training completed with a training accuracy of 99% and validation accuracy of 96%.

## 4. Results
Upon evaluating the model with test data, the model obtain the following test results:
- Train score: Loss = 0.045, Accuracy = 0.993
- Test score: Loss = 0.097, Accuracy = 0.965
