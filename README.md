# deep-learning-challenge
## About
The Alphabet Soup nonprofit foundation has provided funding to over 34,000 organizations over the years. However, not all organizations have been successful in their ventures. To select the applicants with the best chance of success in their ventures, Alphabet Soup needs a tool that can predict whether an applicant will be successful if funded by them.

In this project, I will use machine learning and neural networks to create a classifier that can predict the success of an organization if funded by Alphabet Soup. I will use various features from the provided dataset such as the application type, affiliated sector of industry, government organization classification, use case for funding, organization type, income classification, special considerations for application, funding amount requested, and active status of the organization.

## Dataset
The provided dataset contains metadata about over 34,000 organizations that have received funding from Alphabet Soup over the years. It includes identification columns such as EIN and NAME, and columns that capture information about the organization's application type, affiliated sector of industry, government organization classification, use case for funding, organization type, income classification, special considerations for application, funding amount requested, and active status.

## Overview of the analysis:
The purpose of this analysis was to create a deep learning model that can predict if an organization will be successful if they receive funding from Alphabet Soup.

## Methodology
I will use a combination of exploratory data analysis, data cleaning, feature engineering, and machine learning algorithms to develop the predictive model. 

## Results:

Data Preprocessing:

The target variable for the model was 'IS_SUCCESSFUL'.
The features for the model were all the remaining columns in the dataset after dropping 'EIN' and 'NAME'.
The variables 'EIN' and 'NAME' were removed from the input data because they are neither targets nor features.
In the 'INCOME AMT' column, 25% ofthe data is NaN.  This
## Compiling, Training, and Evaluating the Model:

For the neural network model, 30 neurons were selected for the first layer, followed by 20 neurons in the second layer, and a final output layer with 1 neuron since we are dealing with binary classification.
The activation function used in the hidden layers was ReLU (Rectified Linear Unit), and for the output layer, we used Sigmoid.
With the first model I wasa able to get a 73% accuracy. However, I was not able to achieve the target model performance of 75% accuracy. 
To increase the model performance, I tried increasing the number of neurons and layers, changing the activation functions, and adjusting the learning rate.

I attempted 5 new models all resulting in lower accuracy rates.

## Conclusion
By creating a predictive model that can identify organizations with the best chance of success, Alphabet Soup can improve their funding selection process and increase the overall impact of their contributions. The neural network model that was created achieved an accuracy score of around 73% on the testing data. While this accuracy score is not as high as our target model performance of 75%, it is still a decent accuracy score.





Regenerate response
