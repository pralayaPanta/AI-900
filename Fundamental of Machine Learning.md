- [Topic: Fundamental of Machine Learning](#topic-fundamental-of-machine-learning)
    - [Types of Machine Learning](#types-of-machine-learning)
    - [Supervised machine learning](#supervised-machine-learning)
      - [Regression](#regression)
      - [Classification](#classification)
      - [Bnary Classification](#bnary-classification)
    - [Multiclass Classification](#multiclass-classification)
    - [Unsupervised machine learning](#unsupervised-machine-learning)
      - [Clustering](#clustering)
  

# Topic: Fundamental of Machine Learning

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
- Types
    - **Regression**
    - **Classification**
  
#### Regression
  - form of supervised machine learning in which the labels predicted by the model is in _numberic value._
  - Example
      - the number of ice creams sold on a given day, based on the temperature, rainfall, and windspeed.
  
#### Classification
  - form of supervised machine learning labels are category or class.
  - Types
      - **Binary Classification**
      - **Multiclass Classification**

#### Bnary Classification
  - label determines whether the observed item is or is not (1 or 0) an instance of a specific class
  - like true false or positive negative predictions

### Multiclass Classification
  - extends binary classification to predict a label that represents on of multiple possible classes
  - Example
      - the species of a penguin (Adelie, Gentoo, or Chinstrap) based on its physical measurements.
  
### Unsupervised machine learning
- training data includes only features values without any known labels
- determine relationships between the features of the observations in the training data
- Types
    - **Clustering**
  
#### Clustering
- identifies similarities between observations based on their features, and groups them into discrete clusters.
- Example
    - group of similar flowers based on their size, numbers of leaves, and number of petals
