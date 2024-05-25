- [Fundamental of Machine Learning](#fundamental-of-machine-learning)
    - [Types of Machine Learning](#types-of-machine-learning)
    - [Supervised machine learning](#supervised-machine-learning)
      - [Regression](#regression)
        - [Regression Evaluation Metrics](#regression-evaluation-metrics)
      - [Classification](#classification)
      - [Binary Classification](#binary-classification)
    - [Multiclass Classification](#multiclass-classification)
    - [Unsupervised machine learning](#unsupervised-machine-learning)
      - [Clustering](#clustering)
    - [Deep Learning](#deep-learning)
      - [How does a neural network learn?](#how-does-a-neural-network-learn)
  - [Azure Machine Learning](#azure-machine-learning)
    - [Azure Machine Learning Studio](#azure-machine-learning-studio)
  

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
   
### Supervised machine learning
- training data includes both feature values and known label values.
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
  - Form of supervised machine learning in which the labels predicted by the model is in _numberic value._
  - Example
      - the number of ice creams sold on a given day, based on the temperature, rainfall, and windspeed.
  
  - Regression models are trained to predict numeric lable values based on training data taht includes both features and known labels.
  - Uses algorithm like linear regression
  
  ##### Regression Evaluation Metrics
  - Mean Absolute Error MAE
  - Mean Squared Error MSE
  - Root Mean Squared Error RMSE
  - Coefficient of determinatino R^2 

#### Classification
  - form of supervised machine learning labels are category or class.
  - models calculate probability values for class assignment
  - evaluation metrics assess model performance by comparing predicted classes to the actual classes
  
  - Types
      - **Binary Classification**
      - **Multiclass Classification**

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
- determine relationships between the features of the observations in the training data
- Types
    - **Clustering**
  
#### Clustering
- identifies similarities between observations based on their features, and groups them into discrete clusters.
- Example
    - group of similar flowers based on their size, numbers of leaves, and number of petals
- Metrics
    - average distance to cluster center
    - average distance to other center
    - maximum distance to cluster center
    - silhouette


### Deep Learning
- advanced form of machine learning that tries to emulate learning process of human brain
- creation of an artificial neural network
  - are made up of multiple layers of neurons - deeply nested function
  - each nuron is a function that operates on an input value and a **weight**
  - the function is wrapped in an activation function that determines whether to pass the output on
  - deep neural network DNNs
  
#### How does a neural network learn?
1.  The training and validation datasets are defined, and the training features are fed into the input layer.
2.  Neurons in each layer of the netowork apply their weights and feed the data through the network
3.  The output layer produces a vector containing the calculated values.
4.  A loss function is used to compare the predicted values to the known values and aggregate the difference to calcuate loss
5.  Optimization function can be used to evaluate the influence of each weight in the network on the loss, and determine how they can be adjusted to reduce overall loss.
6.  The changers to the weights are backpropagated to the layers in the network, replacing the previously used values.
7.  The process is repated over multiple iterations known as epochs until the loss is minimized and the model predicts acceptably accurately.


## Azure Machine Learning
Cloud service for training, deploying, and managing machine learning models.
- The primary resource required is Azure Machine Learning Workspace


### Azure Machine Learning Studio
- browser based portal for managing ML resources and jobs
  
  Exercise: [Use automated machine learning to train a model](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/01-machine-learning.html)
