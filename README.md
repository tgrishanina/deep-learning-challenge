## deep-learning-challenge

# Overview of the analysis: 

The purpose of this analysis was to examine a dataset of past applications for funding from Alphabet Soup and build a model that would help the organization select applicants with the best chance of success. The model was to use various features in the dataset, such as income classifications, use cases for funding, and organization types, to predict whether or not an applicant would be successful.


# Data Preprocessing

What variable(s) are the target(s) for your model?

The target for this model was the IS_SUCCESSFUL variable, which indicates whether the funding from Alphabet Soup was used effectively. 

What variable(s) are the features for your model?

The features are composed of the rest of the variables in the dataset: the affiliated sector of the industry (AFFILIATION), government organization classification (CLASSIFICATION), use case for funding (USE_CASE), organization type (ORGANIZATION), active status (STATUS), income classification (INCOME_AMT), special considerations for application (SPECIAL_CONSIDERATIONS), and funding amount requested (ASK_AMT). 

What variable(s) should be removed from the input data because they are neither targets nor features?

The two variables that were instantly removed were EIN and NAME, as they were classifiers and were neither targets nor features. 


# Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
Initially, I chose two hidden layers, with 80 neurons in the first and 30 in the second, as well as an output layer. Each layer had an activation function (ReLU for the hidden layers and sigmoid for the output layer for binary classification). The number of neurons were selected as a moderate baseline to build the model from. 

Were you able to achieve the target model performance?

Unfortunately, I was unable to achieve the target performance of 75%. This basic model had a consistent accuracy score of 72-73%. 

What steps did you take in your attempts to increase model performance?

To optimize the model, I attempted the following:
- Dropping additional feature columns that seemed superfluous (ASK_AMT, SPECIAL_CONSIDERATIONS, and STATUS)
- Adjusting the bin sizes for rare occurences in the APPLICATION_TYPE and CLASSIFICAITON columns
- Adding a third hidden layer
- Adjusting the number of neurons to 256, 128, and 64 in layers one, two and three, respectively
- Changing the activation function of the output layer from sigmoid to tanh
- Lowering the learning rate for Adam to allow the model to converge more slowly (and potentially better)

Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

The adjustments listed above were used concurrently and one at a time. Unfortunately, none of them resulted in a higher accuracy rate. 
