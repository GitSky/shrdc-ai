# Cell Neuclei Detection using Semantic Segmentation with U-Net
## 1. Summary
- Objective: To detect cell nuclei from biomedical images effectively.
- As cell nuclei vary in shapes and sizes, semantic segmentation proves to be the best approach to detect them.
- A deep learning model is trained and deployed for this task.
- The model is trained with the well known 2018 Data Science Bowl dataset (source: https://www.kaggle.com/c/data-science-bowl-2018)

## 2. IDE and Framework
- This project is created using Google Colab as the main IDE.
- The main frameworks used are TensorFlow, Numpy, Matplotlib, OpenCV and Scikit-learn.

## 3. Methodology
### 3.1. Data Pipeline
1. The dataset files contains a train folder for training data and test folder for testing data, in the format of images for inputs and image masks for the labels.
2. The input images are preprocessed with feature scaling.
3. The labels are preprocessed such that the values are in binary of 0 and 1.
4. No data augmentation is applied for the dataset.
5. The train data is split into train-validation sets, with a ratio of 80:20

### 3.2. Model Pipeline
- The model architecture used for this project is U-Net.
- In summary, the model consist of two components, the downward stack, which serves as the feature extractor, and upward stack, which helps to produce pixel-wise output.
- The model is trained with a batch size of 16 and 10 epochs. 
- The training completed with a training accuracy of 97% and validation accuracy of 97%. 

## 4. Results
1. Upon evaluating the model with test data, the model obtain the following test results:
- Loss = 0.0894
- Accuracy = 0.9633

2. Some predictions are also made with the model using some of the test data. The actual output masks and prediction masks are shown in figures below.

![cell](https://user-images.githubusercontent.com/68054684/165924648-c2e85357-666b-4fd8-ad26-a5f7b4a8eea7.png)

![cell2](https://user-images.githubusercontent.com/68054684/165924996-604a0013-9cbe-4260-914d-b48a944671fb.png)

![cell3](https://user-images.githubusercontent.com/68054684/165925029-ddb8b110-3904-40dd-9b2c-3a69c514ae73.png)



