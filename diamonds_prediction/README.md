# Diamond Price Prediction Using Feedforward Neural Network
## 1. Summary
Objective: To predict the price of diamond, based on the following features:
- 4C (cut,clarity,color,carat)
- dimensions (x,y,z)
- depth
- table

The dataset is obtained from:
https://www.kaggle.com/datasets/shivam2503/diamonds

## 2. IDE and Framework
- This project is created using Google Colab as the main IDE.
- The main frameworks used are Pandas, Numpy, Scikit-learn and TensorFlow Keras

## 3. Methodology
### 3.1. Data Pipeline
1. The data is first loaded and preprocessed, such that unwanted features are removed.
2. Categorical features are encoded ordinally.
3. The data is split into train-validation-test sets, with a ratio of 60:20:20.

### 3.2. Model Pipeline
- A feedforward neural network is constructed that is catered for regression problem.
- The model is trained with a batch size of 64 and for 100 epochs.
- Early stopping is applied in this training.
- The training stops at epoch 27, with a training MAE of 754 and validation MAE of 371

## 4. Results
1. The model are tested with test data.
2. The evaluation result:
  - Test loss = 603971.56
  - Test MAE = 362.76
  - Test MSE = 603971.56

The model is also used to made prediction with test data.
A graph of prediction vs. label is plotted, as shown in the image below.
![plot](https://user-images.githubusercontent.com/68054684/165890675-6a8a2603-1092-4cc5-9dbb-80ca7ce89ba2.png)

