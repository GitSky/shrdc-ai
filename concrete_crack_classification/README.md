# Identifying Concrete Cracks with Image Classification using Convolutional Neural Network
## 1. Summary
- Objective: To create a convolutional neural network model that can identify concrete cracks on concrete with a high accuracy.
- The problem is modelled as a binary classification problem which are with cracks (positive) and without cracks (negative).
- The model is trained with a dataset of 2000 images (1000 images of concrete in good condition and 1000 images of concrete with cracks).

The dataset can be found at https://data.mendeley.com/datasets/5y9wdsg2zt/2.

## 2. IDE and Framework
- This project is created using Google Colab as the main IDE.
- The main frameworks used are Numpy, Matplotlib and TensorFlow Keras.

## 3. Methodology
### 3.1. Data Pipeline
1. The image data are loaded along with their corresponding labels.
2. The data is first split into train-validation set, with a ratio of 70:30.
3. The validation data is then further split into two portion to obtain some test data, with a ratio of 80:20.
4. The overall train-validation-test split ratio is 70:24:6.
5. No data augmentation is applied as the data size and variation are already sufficient.

### 3.2. Model Pipeline
- The input layer is designed to receive coloured images with a dimension of 160x160. The full shape will be (160,160,3).
- Transfer learning is applied for building the deep learning model of this project. 
- Firstly, a preprocessing layer is created that will change the pixel values of input images to a range of -1 to 1. 
- This layer serves as the feature scaler and it is also a requirement for the transfer learning model to output the correct signals.
- For feature extractor, a pretrained model of MobileNet v2 is used.
- The model is readily available within TensorFlow Keras package, with ImageNet pretrained parameters.
- It is also frozen hence will not update during model training.
- A global average pooling and dense layer are used as the classifier to output softmax signals. 
- The softmax signals are used to identify the predicted class.

## 4. Results
1. Upon evaluating the model with test data, the model obtain the following test results:
- Loss = 0.044
- Accuracy = 0.979

2. Some predictions are also been made with the model, and compared with the actual results.
![crack](https://user-images.githubusercontent.com/68054684/165901587-6cf258a3-2459-4835-882b-27f3c5027729.png)

