# deep-learning-challenge

# Report 
## Overview of the Analysis:
The purpose of the analysis is to develop a binary classifier using a neural network or deep learning model to create a predictive tool that estimates the likelihood of success for applicants who receive funding from Alphabet Soup. The model is trained on a dataset containing relevant features and success labels. The training process focuses on optimizing the model's parameters to minimize prediction errors and achieve a desired accuracy goal, which in this case is set to be greater than 75%. This ensures that the model is reliable and can provide accurate predictions regarding the success of Alphabet Soup-funded organizations.

## Results:
### Data Preprocessing
1. What variable(s) are the target(s) for your model?

The target variable(s) for the model is IS_SUCCESSFUL

2. What variable(s) are the feature(s) for your model?

All the other columns except IS_SUCCESSFUL.

3. What variable(s) should be removed from the input data because they are neither targets nor features?

Initially EIN and NAME were dropped from the dataset as they were determined to be irrelevant for predicting the success of Alphabet Soup-funded organizations. However, during the optimization attempts, it was found that the EIN column did not contain any meaningful information for the analysis. Therefore, it remained dropped from the dataset. On the other hand, the NAME column has relevance informative for predicting success. It was considered as a feature to be included in the model.

## Compiling, Training, and Evaluating the Model:
1. How many neurons, layers, and activation functions did you select for your neural network model, and why?

For the initial model I used 3 hidden layers 80,30 and 1 neurons that were provided in the starter code. I chose relu and sigmoid as activation functions and the input dimension were the length of the input features.
![Alternate image text](/Images/layers.png)

2. Were you able to achieve the target model performance?

I didn’t achieve the target model performance with my initial model. 

![Alternate image text](/Images/initial_model.png)

3. What steps did you take in your attempts to increase model performance?

To increase the model performance, I had 3 attempts and the third attempt had higher accuracy. I was able to achieve the target model performance with my second and third models.

![Alternate image text](/Images/layers2.png) ![Alternate image text](/Images/layers3.png)

The step that made a difference in the performance was keeping the NAME column, adding a hidden layer with activation function linear made a slight improvement in the accuracy but overall, the step that optimized the model was not dropping the NAME variable from my model feature.
AlphabetSoupCharity_Optimization2:

![Alternate image text](/Images/Optimization2.png)

AlphabetSoupCharity_Optimization3:

![Alternate image text](/Images/Optimization3.png)

## Summary:
The model was optimized to achieve a predictive accuracy of 75% with a loss of 50% in classifying the success of organizations funded by Alphabet Soup. This means that the model was able to accurately predict the likelihood of success for these organizations based on the provided features, with a relatively high level of accuracy.
The accuracy of 75% indicates that the model's predictions align with the accuracy goal for the Alphabet Soup-funded organizations in the dataset. The loss of 50% suggests that there is room for improvement in terms of reducing prediction errors and further refining the model.
A recommendation for a different model that could solve this classification problem is a Random Forest classifier. Its ability to handle non-linear relationships, reduce overfitting, provide insights into feature importance, and accommodate a mix of categorical and numerical features. By leveraging these strengths, a Random Forest model could offer an alternative approach to solving the classification problem of predicting the success of Alphabet Soup-funded organizations.
