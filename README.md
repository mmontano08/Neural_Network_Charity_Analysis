# Neural_Network_Charity_Analysis

## Overview of the analysis:
The purpose of the analysis is to utlize our knowledge with machine learning and neural networks, as we will use the features provided to help create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. 

We received a CSV file from Alphabet Soup's business team containing more than 34,0000 organizations that have received funding from the business over the years. We will be creating three technical analysis:

1. Preprocessing Data for a Neural Network Model
2. Compile, Train, and Evaluate the Model
3. Optimize the Model

## Results:

### Data Preprocessing:
We used Pandas and the Scikit-Learn's to preprocess the dataset in order to compile and train.

- The target variable that is considered for this model is the **IS_SUCCESSFUL**.
- The feature variables that are being considered for this model are:
  - **APPLICATION_TYPE, AFFILIATON, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, and ASK_AMT**
- THE variables that are neither targets nor features, and that were removed from the input data are:
  - **EIN and NAME**

### Compiling, Training, and Evaluating the Model:

- The model was made with an input feature and two hidden layers, First hidden layer had 80 neurons with the ReLU activated function, the second layer had 30 neurons with the ReLU activated function and "sigmoid" was selected for the output layer.

![Module19_Compile_Train_Evaluate](https://user-images.githubusercontent.com/83566868/133007344-d29331b7-9c36-4c94-a11e-aeeabdaf75fa.png)

- This model was not able to achieve the target of 75%. The accuracy for this model was 48%. 

![Module19_AccuracyRate](https://user-images.githubusercontent.com/83566868/133007358-e0ff978a-4a0e-443e-9539-c117eb2ef9cd.png)

- The steps that I took to increase the model performance was changing the "hidden_nodes_layer1" to 120, "hidden_nodes_layer2" to 60 and both were with "tanh" activated. Doing this allowed me to closely achieve the target model performance to 0.7429 = 74%

![Module19_PerformanceChange](https://user-images.githubusercontent.com/83566868/133007370-228c1533-d9b4-436a-add0-692a03507091.png)

![Module19_FinalAccuracy](https://user-images.githubusercontent.com/83566868/133007380-0a614a98-7f3c-4f94-bfc3-c068ba643fab.png)

## Summary:
My final attempt model ended up with an accuracy very close to the ideal target of 75%, coming up short 1%, resulting at 74%. This is a result of adding additonal neurons, hidden layers, and also changing the activation function. My recommnedation for how a different model(s) can or could resolve this type of classification problem is first to have as much data as possible, this will allow us to use the Random Forest Classifier. This type of classification model provides the highest accuracy. The random forest technique also handles big data with numerous variables. 
