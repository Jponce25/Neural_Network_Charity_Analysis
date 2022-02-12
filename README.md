# Neural_Network_Charity_Analysis

## Overview of the analysis

Explain the purpose of this analysis.

Using machine learning and neural networks, we will use the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

We have a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special consideration for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

## Results

Using bulleted lists and images to support your answers, address the following questions.

### Data Preprocessing

<img src="https://github.com/Jponce25/Neural_Network_Charity_Analysis/blob/67bbbf67d3dbe996a34a027cf34c1f8ce4e53415/Image/Imagen1.png" width="450">

- **What variable(s) are considered the target(s) for your model?**
The variable considered as the target is "IS_SUCCESSFUL"

- **What variable(s) are considered to be the features for your model?**
we can consider different variables as the "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", "ASK_AMT"

- **What variable(s) are neither targets nor features, and should be removed from the input data?**
The "EIN" and "NAME" columns have been dropped

### Compiling, Training, and Evaluating the Model

<img src="https://github.com/Jponce25/Neural_Network_Charity_Analysis/blob/67bbbf67d3dbe996a34a027cf34c1f8ce4e53415/Image/Imagen2.png" width="500">

- **How many neurons, layers, and activation functions did you select for your neural network model, and why?**
For the neural network model we use 2 hidden layers with 80 neurons and 30. Both hidden layer have the "relu" activation function. The output layer has the "sigmoid" activation function.

- **Were you able to achieve the target model performance?**
The model was not able to reach the target 75%. The accuracy for my model was 72.33%.

- **What steps did you take to try and increase model performance?**

Attempt 1: First we try to remove additional feature 'EIN','NAME','ASK_AMT','SPECIAL_CONSIDERATIONS'. And also we try with less neurons in each hidden layer 40 for the first one and 20 for the second one, the model accuracy grew a little to 72.48%.

<img src="https://github.com/Jponce25/Neural_Network_Charity_Analysis/blob/67bbbf67d3dbe996a34a027cf34c1f8ce4e53415/Image/Imagen3.png" width="500">

Attempt 2: For this model we try to remove only 'EIN','NAME','SPECIAL_CONSIDERATIONS' features. Also we add an additional hidden layer with 40 neurons, 20 and 5. The accuracy went down again same as the first model, 72.33%.

<img src="https://github.com/Jponce25/Neural_Network_Charity_Analysis/blob/67bbbf67d3dbe996a34a027cf34c1f8ce4e53415/Image/Imagen4.png" width="500">

Attempt 3: We remove 'EIN','NAME','STATUS','SPECIAL_CONSIDERATIONS','USE_CASE'. Also we add an additional hidden layer with 60 neurons, 30 and 10. Changing activation function of first and second layer from "relu" to "selu." The accuracy of the model went down to 71.72%.

<img src="https://github.com/Jponce25/Neural_Network_Charity_Analysis/blob/67bbbf67d3dbe996a34a027cf34c1f8ce4e53415/Image/Imagen5.png" width="500">

## Summary

The model could not be increased to more than 72% accuracy, even eliminating variables that could generate noise or using different specifications increased the accuracy. 

To improve the model we could try to change the distribution between the test data and the training data, it could also be that the model we are trying with neural networks is better solved with some other supervised machine learning model.