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
The purpose of this analysis was to create a deep learning model that could predict if an organization would be successful if they received funding from Alphabet Soup.

## Methodology
I used a combination of exploratory data analysis, data cleaning, feature engineering, and machine learning algorithms to develop the predictive model.

## Results:

### Data Preprocessing:

The target variable for the model was 'IS_SUCCESSFUL'.
The features for the model were all the remaining columns in the dataset after dropping 'EIN' and 'NAME'.
The variables 'EIN' and 'NAME' were removed from the input data because they are neither targets nor features. There was consideration to remove Income Amt because in the 'INCOME AMT' column, 25% ofthe data is NaN.  This could have an effect on the outcome of the data.

### Compiling, Training, and Evaluating the Model:

#### Original Model

<img width="538" alt="Screenshot 2023-05-07 at 9 37 08 AM" src="https://user-images.githubusercontent.com/40581033/236680835-b4c7f02d-a4da-4c5a-b1a7-a7a01e195e6f.png">

For the neural network model, 30 neurons were selected for the first layer, followed by 20 neurons in the second layer, and a final output layer with 1 neuron since we are dealing with binary classification. The numbers were chosen to try to avoid overfitting.
The activation function used in the hidden layers was ReLU (Rectified Linear Unit), and for the output layer, we used Sigmoid.
With the first model I was able to get a 73% accuracy. However, I was not able to achieve the target model performance of 75% accuracy. 

To increase the model performance, I tried increasing the number of neurons and layers, changing the activation functions, and adjusting the learning rate. However, I still had a loss of 55.6% and and accuracy of 72.4% 

<img width="557" alt="Screenshot 2023-05-07 at 9 37 50 AM" src="https://user-images.githubusercontent.com/40581033/236680867-87867207-4561-450d-8c36-a3f1409e2710.png">

268/268 - 0s - loss: 0.5567 - accuracy: 0.7248 - 251ms/epoch - 936us/step
Loss: 0.5567113757133484, Accuracy: 0.724781334400177

I continued to modify my model, but each time managed to get a lower accuract and higher loss.
<img width="505" alt="Screenshot 2023-05-07 at 9 32 47 AM" src="https://user-images.githubusercontent.com/40581033/236680623-57b5541d-7dd4-4af7-a95a-a4e8c872b84a.png">

I attempted 5 new models all resulting in lower accuracy rates. In some cases my training accuracy was high but validation accuracy was low, it probably meant that my model was overfitting to the training data and was not generalizing well to new data. I tried adding more neurons or layers can improve the performance of the model by increasing its capacity to learn complex representations from the input data.

<img width="495" alt="Screenshot 2023-05-07 at 9 33 00 AM" src="https://user-images.githubusercontent.com/40581033/236680638-effb6b1a-0289-4569-b27b-b8116c4e4a24.png">

Finally I attempted a randomForestclassification on my data. The precision for class 0 is 0.79, meaning that when the model predicts that an organization will not be successful (class 0), it is correct about 79% of the time. The precision for class 1 is 0.75, meaning that when the model predicts that an organization will be successful (class 1), it is correct about 75% of the time.

The recall metric measured the proportion of true positives of all actual positives. The recall for class 0 was 0.69, meaning that the model correctly identified 69% of the organizations that will not be successful. 
The recall for class 1 ws 0.84, meaning that the model correctly identifies 84% of the organizations that will be successful (class 1).

The F1-score is the harmonic mean of precision and recall, and provides a single score that balances both metrics. The F1-score for class 0 is 0.73, and the F1-score for class 1 is 0.79.

The model's accuracy is 0.77, meaning that it correctly classifies 77% of the samples in the dataset. Therefore the RandomForestClassifer was the better model to run on this data. This is because RFC are better at handling large datasets and tend to be better at overfitting but it is not good at looking at relationships between features.

THe neural network models are good at handling non-linear relationships but can sometimes overfit the the data.

<img width="518" alt="Screenshot 2023-05-07 at 10 04 15 AM" src="https://user-images.githubusercontent.com/40581033/236682301-8586c189-534d-4b93-8ab7-2ed003b423d8.png">


## Summary and Conclusion
By creating a predictive model that can identify organizations with the best chance of success, Alphabet Soup can improve their funding selection process and increase the overall impact of their contributions. The neural network model that was created achieved an accuracy score of around 73% on the testing data. While this accuracy score is not as high as our target model performance of 75%, it is still a decent accuracy score.
