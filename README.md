# deep-learning-challenge
## Overview of the Analysis
The purpose of this analysis is to train and evaluate a binary classification neural network model that can predict whether applicants will be successful if funded by nonprofit foundation Alphabet Soup.

### About the Data
The dataset includes 34,299 records, and 12 columns.
* The features include:
    - <strong>EIN</strong> and <strong>NAME</strong> (Identification columns)
    - <strong>APPLICATION_TYPE</strong> (Alphabet Soup application type)
    - <strong>AFFILIATION</strong> (Affiliated sector of industry)
    - <strong>CLASSIFICATION</strong> (Government organization classification)
    - <strong>USE_CASE</strong> (Use case for funding)
    - <strong>ORGANIZATION</strong> (Organization type)
    - <strong>STATUS</strong> (Active status)
    - <strong>INCOME_AMT</strong> (Income classification)
    - <strong>SPECIAL_CONSIDERATIONS</strong> (Special considerations for application)
    - <strong>ASK_AMT</strong> (Funding amount requested)
* The target value is:
    - <strong>IS_SUCCESSFUL</strong> (Was the money used effectively)
* What variable(s) should be removed from the input data because they are neither targets nor features?
    - The identification columns were removed
### Neural Network Model Process
1. Preprocess Data
2. Separate the features from the target
3. Split the data for training and testing
4. Create NN model and fit the data
5. Optimize NN model

## Results
### Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
    - Hidden layers: 6
    - Neurons per layer: 9, 9, 3, 5, 9, 9
    - Activation function: sigmoid
    - These results were chosen by the auto-optimizer tuner. 
* Were you able to achieve the target model performance?
    - No, I was not able to achieve a model with over 75% accuracy
* What steps did you take in your attempts to increase model performance?
    - First Optimization Attempt: Change number of Epochs
    - Second Attempt: Change activation function for output layer to linear
    - Third Attempt: Reduce neurons in hidden layers
    - Fourth Attempt: Add a third hidden layer
    - Fifth Attempt: Ordinal encoding for the income amount column
    - Sixth Attempt: Use auto-optimizing tuner


## Summary

The optimization attempts resulted in little to no changes to the loss score and accuracy score. I ended up proceeding with the neural network model chosen by the auto-optimizer because it at least yielded an accuracy score of 73.3%, but even this was only 1% better than the other attempts. I suspect that better results may come from further preprocessing the data so cleaner data can be fed into the model.
