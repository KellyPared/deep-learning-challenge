# deep-learning-challenge
## About
The Alphabet Soup nonprofit foundation has provided funding to over 34,000 organizations over the years. However, not all organizations have been successful in their ventures. To select the applicants with the best chance of success in their ventures, Alphabet Soup needs a tool that can predict whether an applicant will be successful if funded by them.

In this project, I will use machine learning and neural networks to create a classifier that can predict the success of an organization if funded by Alphabet Soup. I will use various features from the provided dataset such as the application type, affiliated sector of industry, government organization classification, use case for funding, organization type, income classification, special considerations for application, funding amount requested, and active status of the organization.

## Dataset
The provided dataset contains metadata about over 34,000 organizations that have received funding from Alphabet Soup over the years. It includes identification columns such as EIN and NAME, and columns that capture information about the organization's application type, affiliated sector of industry, government organization classification, use case for funding, organization type, income classification, special considerations for application, funding amount requested, and active status.
          * EIN and NAME—Identification columns
          * APPLICATION_TYPE—Alphabet Soup application type
          * AFFILIATION—Affiliated sector of industry
          * CLASSIFICATION—Government organization classification
          * USE_CASE—Use case for funding
          * ORGANIZATION—Organization type
          * STATUS—Active status
          * INCOME_AMT—Income classification
          * SPECIAL_CONSIDERATIONS—Special considerations for application
          * ASK_AMT—Funding amount requested
          * IS_SUCCESSFUL—Was the money used effectively

<img width="283" alt="Screenshot 2023-05-07 at 9 53 19 AM" src="https://user-images.githubusercontent.com/40581033/236681717-fd8ffafe-2368-4a75-9873-d796f62391c1.png">

## Overview of the analysis:
The purpose of this analysis was to create a deep learning model that can predict if an organization will be successful if they receive funding from Alphabet Soup.

## Methodology
I will use a combination of exploratory data analysis, data cleaning, feature engineering, and machine learning algorithms to develop the predictive model. 

## Results:

### Data Preprocessing:

The target variable for the model was 'IS_SUCCESSFUL'.
The features for the model were all the remaining columns in the dataset after dropping 'EIN' and 'NAME'.
The variables 'EIN' and 'NAME' were removed from the input data because they are neither targets nor features.
In the 'INCOME AMT' column, 25% ofthe data is NaN.  This
### Compiling, Training, and Evaluating the Model:

#### Original Model

<img width="538" alt="Screenshot 2023-05-07 at 9 37 08 AM" src="https://user-images.githubusercontent.com/40581033/236680835-b4c7f02d-a4da-4c5a-b1a7-a7a01e195e6f.png">

For the neural network model, 30 neurons were selected for the first layer, followed by 20 neurons in the second layer, and a final output layer with 1 neuron since we are dealing with binary classification.
The activation function used in the hidden layers was ReLU (Rectified Linear Unit), and for the output layer, we used Sigmoid.
With the first model I wasa able to get a 73% accuracy. However, I was not able to achieve the target model performance of 75% accuracy. 

To increase the model performance, I tried increasing the number of neurons and layers, changing the activation functions, and adjusting the learning rate. However, I still had a loss of 55.6% and and accuracy of 72.4% 

<img width="557" alt="Screenshot 2023-05-07 at 9 37 50 AM" src="https://user-images.githubusercontent.com/40581033/236680867-87867207-4561-450d-8c36-a3f1409e2710.png">

268/268 - 0s - loss: 0.5567 - accuracy: 0.7248 - 251ms/epoch - 936us/step
Loss: 0.5567113757133484, Accuracy: 0.724781334400177

I continued to modify my model, but each time managed to get a lower accuract and higher loss.
<img width="505" alt="Screenshot 2023-05-07 at 9 32 47 AM" src="https://user-images.githubusercontent.com/40581033/236680623-57b5541d-7dd4-4af7-a95a-a4e8c872b84a.png">

I attempted 5 new models all resulting in lower accuracy rates. In so,me cases my training accuracy was high but validation accuracy was low, it probably meant that my model was overfitting to the training data and was not generalizing well to new data.

<img width="495" alt="Screenshot 2023-05-07 at 9 33 00 AM" src="https://user-images.githubusercontent.com/40581033/236680638-effb6b1a-0289-4569-b27b-b8116c4e4a24.png">


## Conclusion
By creating a predictive model that can identify organizations with the best chance of success, Alphabet Soup can improve their funding selection process and increase the overall impact of their contributions. The neural network model that was created achieved an accuracy score of around 73% on the testing data. While this accuracy score is not as high as our target model performance of 75%, it is still a decent accuracy score.





Regenerate response
