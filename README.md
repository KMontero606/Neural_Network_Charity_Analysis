# Neural_Network_Charity_Analysis
## Overview of the analysis:
With the knowledge of machine learning and neural networks, we will use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization

## Results: Using bulleted lists and images to support your answers, address the following questions.
   - Data Preprocessing
     - What variable(s) are considered the target(s) for your model?
       - The target variable for my model is success rate of applicants funded by Alphabet Soup.
       
     - What variable(s) are considered to be the features for your model?
       - The feature variable for my model are all the other category in the dataset (Name, Application type, Affiliation, Classification, Use_case, Organization,      Status, Income amount, Special considerations).
       
     - What variable(s) are neither targets nor features, and should be removed from the input data?
       - the EIN and Ask amount were removed from the input data as it is irrelevant. 

![image](https://user-images.githubusercontent.com/106962921/196180311-4312878b-3a18-4ff2-a9f1-bfcef60e1b14.png)

   - Compiling, Training, and Evaluating the Model
     - How many neurons, layers, and activation functions did you select for your neural network model, and why?
       - There are three hidden layers with 100 neurons in the first layer, 30 neurons in the second layer and 10 neurons in the third layer. The activation functions chosen for my neural network are relu at the first layer, relut at the second layer and sigmoid for the third layer.
       
       ![image](https://user-images.githubusercontent.com/106962921/196181518-f3ec9409-47e3-40ec-9522-1db220b965b8.png)
       
     - Were you able to achieve the target model performance?
       - I was able to achieve 0.74 accuracy on the second attempt with the described model above. The first and third attempt accuracy were 0.73 and 0.74 respectively.
       
     - What steps did you take to try and increase model performance?
       - First attempt, I preprocessed the data by droping the EIN and ASK_AMT column and assess the NAME, APPLICATION_TYPE and CLASSIFICATION column for binning. Then, I designed a model with three hidden layers with 100, 80 and 30 hidden nodes for each layer respectively. The accuracy score yield to be 0.73 with loss score of 0.57.
       ![image](https://user-images.githubusercontent.com/106962921/196179463-6aa8dfc4-0a3f-4166-bd9e-79bb25877469.png)
       
       - Second attempt, I preprocessed the data by dropping the EIN onlyand assess the NAME, APPLICATION_TYPE and CLASSIFICATION column for binning. Then, I designed a model with three hidden layers with 100, 30 and 10 hidden nodes for each layer respectively and changing the third layer activation function to sigmoid. The accuracy score yield to be 0.74 with loss score of 0.53.
       
       ![image](https://user-images.githubusercontent.com/106962921/196179319-b38542c1-45ec-4e9a-bbfe-8fd77e64b5e3.png)

       - The third attempt, I used the same preprocessed data from the second attempt by changing the second layer activation function to sigmoid. The accuracy score yield of 0.74 with loss score of 0.53.
       ![image](https://user-images.githubusercontent.com/106962921/196179111-5277d785-9037-4d0d-a59b-a8211e1d467f.png)

## Summary: 
The overall results of the deep learning model designed could only yield a 0.74 accuracy with a loss score of 0.53. 
I would recommend a Random Forest model which could solve this classification problem as this particular model handles tabular data like the one provided.
