# machine-learning
The repository for machine learning path cohort.
Here below is an **outline** about how we built our ML models for CANCERWISE

## Library

Here's a list of libraries that we use to build our ML models:
1. **Matplotlib**
2. **Numpy**
3. **Tensorflow**
4. **Pandas**
5. **Seaborn**
6. **Sklearn**

## Dataset

In this Capstone Project, we use 3 datasets to create our models:
1. [Lung Cancer Dataset](https://www.kaggle.com/datasets/mysarahmadbhat/lung-cancer) - from Kaggle
2. [Cervical Cancer Dataset](https://www.kaggle.com/datasets/loveall/cervical-cancer-risk-classification) - from Kaggle
3. [Brain Tumor Dataset](https://data.world/seekersoftec/risk-of-brain-tumor/workspace/file?filename=risk_of_brain_tumor.csv) - from Data World

## Data Preprocessing

Here are the data preprocessing steps that we apply to our datasets:
1. **Feature Selection**
2. **Imputing Missing Values**
3. **Drop Duplicate Data**
4. **Remove Outliers**
6. **Split the Data** (into a training set, validation set, and test set)
7. **Feature Scaling**
8. **Resample the Data**

## Model Development

Our neural network consists of 2-3 layers:
1. We use **ReLU** as the activation function for the input layer and the hidden layer
2. We use **Sigmoid** as the activation function for the output layer

## Training

We use: 
1. **BinaryCrossentropy** to compute our model losses
2. **Adam** as our models optimizer 
3. **Accuracy** as our metrics to evaluate our models

## Result (Evaluation)

**Lung Cancer Model**

![image](https://github.com/cancerwise/machine-learning/assets/92629964/2f5b38a4-bcf9-45cd-a51f-627a2fdb32b4)

**Cervical Cancer Model**

![image](https://github.com/cancerwise/machine-learning/assets/92629964/e16f9c68-45be-4509-83af-2b0439c62d46)

**Brain Tumor Model**

![image](https://github.com/cancerwise/machine-learning/assets/92629964/5e1cec44-087c-4416-8676-9b686f31093a)

## Saving Our Models

Here's how to save the model:

`!mkdir -p saved_model
model.save('saved_model/my_model')`

Here's how to save the model in (.h5) format:

`model.save('my_model.h5')`

Here's how to download the model that has already been saved:

`from google.colab import files`

`files.download('saved_model/my_model/variables/variables.data-00000-of-00001')`

`files.download('saved_model/my_model/variables/variables.index')`

`files.download('saved_model/my_model/fingerprint.pb')`

`files.download('saved_model/my_model/keras_metadata.pb')`

`files.download('saved_model/my_model/saved_model.pb')`

`files.download('my_model.h5')`
