# ML_Term_Project
Machine Learning Term project of IOG5018

### Download dataset:
[dataset.zip](https://github.com/e96031413/ML_Term_Project/blob/main/dataset.zip)
After unzipping the file, you will get 3 different folders.

If you want to train with CNN, make sure you use **dataset256x256(by train and val)**, For those who want want to train with ML based method, you can use **either dataset256x256(by class)** or **dataset64x64(by class)**.

The main difference between these two folders are just their image size (256 and 64) and folder structure(by training/val set split or by class split)

### ML based method:
Using Scikit learn, **without hyperparameter search:**

**Image size: 256x256**

Note: We combine KNN, LogisticRegression and SVM to train our Voting Classifier model
|               |  KNN |LogisticRegression | RandomForest|     SVM     |   Voting Classifier|
|---------------|------|-------------------|-------------|-------------|--------------------|
| Test Accuracy |57.08%| 61.3%             |      63.98% |    63.21%   |     60.9%          |

Using Scikit learn, **with hyperparameter search**:

**Image size: 256x256**
|               |  KNN |LogisticRegression | RandomForest|     SVM     |   Voting Classifier| AdaBoost| Gradient Boosting|
|---------------|------|-------------------|-------------|-------------|--------------------|---------|------------------|
| Test Accuracy |60.53%| 61.3%             |      63.98% |    70.49%   |     60.9%          |   66.6% |        64.36%    |


Using Scikit learn, **without hyperparameter search:**

**Image size: 64x64**

Note: We combine KNN, LogisticRegression and SVM to train our Voting Classifier model

|               | LogisticRegression | RandomForest|     SVM     | Voting Classifier| 
|---------------|--------------------|-------------|-------------|------------------|
| Test Accuracy |58.5%               |      65.2%  |    63.5%    |     63.2%        |

Using Scikit learn, **with hyperparameter search:**

**Image size: 64x64**
|               |    KNN   |     SVM     |  MLP        | 
|---------------|----------|-------------|-------------|
| Test Accuracy |   65.5%  |    63.8%    |     62.8%   |


### CNN based method:

**Image size: 256x256**

Pre-trained model from [keras application](https://keras.io/api/applications/) and add some custom layer on it
|               | ResNet50|  VGG16| InceptionResNetV2 | DenseNet201 |
|---------------|---------|-------|-------------------|-------------|
| Test Accuracy |   91.36%| 92.08%|      94.96%       |    96.4%    |


### CNN + ML method:

**Image size: 256x256**
|               |   CNN | CNN+SVM| CNN+XGBoost|
|---------------|-------|--------|------------|
| Test Accuracy | 74.71%|  77.58%|   78.61%   |


### CNN + ML method:

**Original Image size:**
|               |   CNN | CNN+SVM| CNN+XGBoost|
|---------------|-------|--------|------------|
| Test Accuracy | 71.84%|  70.11%|   75.86%   |
