- [Fundamental of Machine Learning](#fundamental-of-machine-learning)
    - [Types of Machine Learning](#types-of-machine-learning)
    - [Reinforcement Learning](#reinforcement-learning)
    - [Supervised machine learning](#supervised-machine-learning)
      - [Regression](#regression)
        - [Regression Evaluation Metrics](#regression-evaluation-metrics)
      - [Classification](#classification)
      - [Binary Classification](#binary-classification)
    - [Multiclass Classification](#multiclass-classification)
    - [Unsupervised machine learning](#unsupervised-machine-learning)
      - [Clustering](#clustering)
    - [Anamoly detection](#anamoly-detection)
    - [Deep Learning](#deep-learning)
      - [How does a neural network learn?](#how-does-a-neural-network-learn)
  - [ML Pipelines](#ml-pipelines)
  - [Forecasing and prediction](#forecasing-and-prediction)
- [Azure Machine Learning](#azure-machine-learning)
    - [Azure ML Studio - Compute](#azure-ml-studio---compute)
    - [Azure ML Studio - Data labeling](#azure-ml-studio---data-labeling)
    - [Azure ML Studio - Data Store](#azure-ml-studio---data-store)
    - [Azure ML workspace](#azure-ml-workspace)
    - [Azure ML Endpoints](#azure-ml-endpoints)
    - [Azure AutoML](#azure-automl)
    - [Azure Machine Learning Studio (classic)](#azure-machine-learning-studio-classic)
  - [Data Modeling steps](#data-modeling-steps)
  - [Automated Machine Learning](#automated-machine-learning)
  

# Fundamental of Machine Learning

Fundamental concept - use data from past observations to predict unknown outcomes or values.

Machine Learning as a function
  - Machine learning encapsulates **_function_** to calculate output
  - Process of defining the function is known as **_training_**
  - **_Inferencing_** predicts new values.

Steps involved:
  - Observed attributers or features of training data is called **_label_**
  - An **_algorithm_** is applied to the data to determine relationship between the features and labels.
  - Result of the algorithm is a **_model_** that encapsulates the calculation
  - This conmpletes **_training_** phase and this model can be used for **_inferencing_**

### Types of Machine Learning
1. Supervised machine learning
2. Unsupervised machine learning
3. Reinforcement learning

### Reinforcement Learning
- no data
- an environment and ML model generates data to reach a goal
- decsion-driven 
- Game AI, Learning Tasks, Robot navigation
  
### Supervised machine learning
- training data includes both feature values and known label values.
- task driven
- used to train models to predict unknown labels
- training data involves multiple iterations with appropriate algorithm, evaluation model performance and refining the model until acceptable level of predecitive accuracy.
  
- **Key elements**
    - Split the data randomly - dataset for training and dataset for validating the trained model
    - Algorithm to fit the training data to a model
    - Validation data to validate model prediction
    - Compare actual label with predicted labels
    - Aggregate difference between predicted and actual label to indicate accuracy

- Types
    - **Regression**
    - **Classification**
  
#### Regression
  - Form of supervised machine learning in which the labels predicted by the model is in _numberic value_
  - Example
      - the number of ice creams sold on a given day, based on the temperature, rainfall, and windspeed.
      - predicting the sea level in meters for the next 10 years
      - number of gift cards selling next month
  
  - Regression models are trained to predict numeric label values based on training data taht includes both features and known labels.
  - Uses algorithm like linear regression
  
  ##### Regression Evaluation Metrics
  - Mean Absolute Error MAE
  - Mean Squared Error MSE
  - Root Mean Squared Error RMSE
      - The Residual histogram presents the frequency of residual values distribution. Residual is the difference between predicted and actual values. It represents the amount of error in the model.
      - If we have a good model, we should expect that most of the errors are small. They will cluster around 0 on the Residual histogram.
  - Coefficient of determinatino R^2 

#### Classification
  - form of supervised machine learning labels are category or class.
  - models calculate probability values for class assignment
  - evaluation metrics assess model performance by comparing predicted classes to the actual classes
    - Example
        - a banking system that predicts whether a loan will be repaid
    - algorithms
        - logistic regression
        - decision tree and random forest
        - neural networks
  - Types
      - **Binary Classification**
      - **Multiclass Classification**
  - confusion matrix
      - table to visualise the model predictions vs ground truth labels
      - error matrix
      - 
#### Binary Classification
  - label determines whether the observed item is or is not (1 or 0) an instance of a specific class
  - like true false or positive negative predictions
  - Evaluation metrics
      - accuracy - measures the proportion of predictions that the model got right
      - recall - measures the proportion of positive cases that the model identified correctly, also true positive rate TPR
      - precision - measures the proportion of predicted positive cases where the true label is actually postive
      - F1-score - overall metrics that combined recall and precision (2 x Precision x Recall) ÷ (Precision + Recall)

### Multiclass Classification
  - extends binary classification to predict a label that represents on of multiple possible classes
  - Example
      - the species of a penguin (Adelie, Gentoo, or Chinstrap) based on its physical measurements.
  - Two kind of algorithm that can be used
      - one vs rest (OvR) algorithms
      - multinomial algorithms
  
### Unsupervised machine learning
- training data includes only features values without any known labels
- data-driven
- determine relationships between the features of the observations in the training data
- Types
    - **Clustering**
    - anamoly detection
  
#### Clustering
- grouping unlabeled data based on similarities and differences
- identifies similarities between observations based on their features, and groups them into discrete clusters.
- most common clustering algorithm is **_K-mean_** clustering
- Example
    - group of similar flowers based on their size, numbers of leaves, and number of petals
    - A medical research project uses a large anonymized dataset of brain scan images that are categorized into predefined brain haemorrhage types. You need to use machine learning to support early detection of the different brain haemorrhage types in the images before the images are reviewed by a person.
- Metrics
    - average distance to cluster center
    - average distance to other center
    - maximum distance to cluster center
    - silhouette

### Anamoly detection
  - the process of finding outliers within a dataset called an anomaly
  - data or patterns appear suspcious or malicious
  - ex
      - intrusion detection
      - fraud detection
      - systems health monitoring

### Deep Learning
- advanced form of machine learning that tries to emulate learning process of human brain
- creation of an artificial **neural network**
  - are made up of multiple layers of neurons - deeply nested function
    - input layers >> hidden layers >> ouput layers
  - each neuron is a function that operates on an input value and a **weight**
  - the function is wrapped in an activation function that determines whether to pass the output on
  - deep neural network DNNs
- What is Feed Forward FNN?
  - Neural Networks where connections between nodes do not form a cycle 
    - always move forward
- What is Backpropagation BP?
  - Moves backwards through the neural network adjusting weights to improve outcome in next iterations
- Loss function
  - a function that compares the ground truth to the prediction to determine the error rate 
  - essentially, how bad the network performed
- Activation function  - an algorithm applied to a hidden layer node that affects connected output eg ReLu
- Dense   - when the next layer increases the amount of nodes
- Sparse  - when the next layer decreases the amount of nodes
  
#### How does a neural network learn?
1.  The training and validation datasets are defined, and the training features are fed into the input layer.
2.  Neurons in each layer of the netowork apply their weights and feed the data through the network
3.  The output layer produces a vector containing the calculated values.
4.  A loss function is used to compare the predicted values to the known values and aggregate the difference to calcuate loss
5.  Optimization function can be used to evaluate the influence of each weight in the network on the loss, and determine how they can be adjusted to reduce overall loss.
6.  The changers to the weights are backpropagated to the layers in the network, replacing the previously used values.
7.  The process is repated over multiple iterations known as epochs until the loss is minimized and the model predicts acceptably accurately.

## ML Pipelines
Data Labeling >> Feature Enginering >> Training >> Hyperparameter tuning >> Serving >> Inference (real-time endpoint or batch processing)

  - Model evaluation
      - The Model evaluation module outputs a confusion matrix showing the number of true positives, false negatives, false positives, and true negatives, as well as ROC, Precision/Recall, and Lift curves.
  - Feature Engineering
      - process of using domain knowledge fo the data to create feature that help algorithms learn better
      - in Azure ML, scaling and normalisation are used

## Forecasing and prediction
- forecasting
    - prediction with relevant data
    - analysis of trends
    - not guessing
- prediction
    - future prediction without relevant data
    - uses statistics to predict future outcomes
    - uses decision theory

# Azure Machine Learning
- Cloud service for training, deploying, and managing machine learning models.
- The primary resource required is Azure Machine Learning Workspace
- Features
    - automated machine learning
        - MLOps
        - end to end automation of ML model pipelines
        - pipelines
    - azure machine learning designer
        - drag and drop interface to visually build test and deploy ML models
        - can use Python and R to write custom code
    - data and compute maanagement
    - Azure ML SDK for python
        - desgined specifically to interact with Azure ML service
    - Juptyer notebooks
        - build and document ML models    
  
### Azure ML Studio - Compute
- 4 kinds of compute
    - compute instances
    - compute clusters
    - inference clusters
    - attached compute

### Azure ML Studio - Data labeling
- types of labeling
  - Human in the loop labelling
  - Machine learning assisted labeling

### Azure ML Studio - Data Store
- securely connect to your storage service on azure
- types
    - blob storage
    - file share
    - data lake storage
    - Azure SQL database
    - Azure Postgres database
    - Azure MySQL Database

### Azure ML workspace
- workspaces are places to collaborate with colleage to create ML artifacts and group related work

### Azure ML Endpoints
- allows you to deploy machine learning models as a web serivce
- types:
    - realtime endpoints
        - Uses AKS and ACI
    - pipeline endpoints
        - uses an ML pipeline

### Azure AutoML
- automates the process of creating ML model
- you supply a dataset, choose a task type and then autoML will train and tune model
- types of task
    - classification: binary or multi class classfication
    - regression: numerical data
    - time series forecasting: value based on time, multivariate regression model
- Data Guard Rails
    - automatic featurisation: scaling or normalisation techniques
    - sequence of checks to ensure high quality data
  
### Azure Machine Learning Studio (classic)
- old one, - do not have pipleine

## Data Modeling steps
  - Feature selection
  - Finding and removing data outliers
  - Impute missing values
  - Normalize numeric features

You have a dataset that contains information about taxi journeys that occurred during a given period.
You need to train a model to predict the fare of a taxi journey.
What should you use as a feature?

ANS:
The label is the column you want to predict. The identified Featuresare the inputs you give the model to predict the Label.
Example:
The provided data set contains the following columns:
vendor_id: The ID of the taxi vendor is a feature.
rate_code: The rate type of the taxi trip is a feature.
passenger_count: The number of passengers on the trip is a feature. trip_time_in_secs: The amount of time the trip took. You want to predict the fare of the trip before the trip is completed. At that moment, you don't know how long the trip would take. Thus, the trip time is not a feature and you'll exclude this column from the model. trip_distance: The distance of the trip is a feature. payment_type: The payment method (cash or credit card) is a feature. fare_amount: The total taxi fare paid is the label.
Reference:
https://docs.microsoft.com/en-us/dotnet/machine-learning/tutorials/predict-prices


## Automated Machine Learning