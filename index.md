
<h1 align='center'> BANK CUSTOMER CHURN PREDICTION USING ANN </h1> 

The project focuses on predicting if a particular customer will leave or continue to stay in the bank based on various features like Tenure, Age, Balance, Gender, etc., using an Artificial Neural Network.


## Features

- Age
- Credit Score
- Gender
- Tenure
- Balance
- NumOfProducts
- HasCrCard
- IsActiveMember
- EstimatedSalary
- Geography


## Lessons Learned

There are few steps which were followed while doing this project.
1. Data Extraction: 
    Extracted thge data from the csv file from the kaggle folder.
2. Data Cleaning
    - The unnecessary columns like RowNumber, CustomerId were dropped.
    - The Object type column Gender was converted to 0 and 1 for Male and Female respectively.
    - One-Hot encoding was done for the Geographic location
    - Checked for all the null values and count.
3. Exploratory Data Analysis:
    - The correlation between each feature was checked using a pair plot
 ![Correlation_Heatmap](https://github.com/AshiniAnantharaman/Bank_Customer_Churn_Prediction/blob/main/Correlation_Heatmap.png)
    - To get a deeper insight the pairplot was plotted against all these features.
    - To check if the data is balanced or not, the count of output feature - Exited values are plotted which shows that the data is imbalanced.
    - The Age based churn was also compared using a bar chart
 ![Age_Churn_Comparison](https://github.com/AshiniAnantharaman/Bank_Customer_Churn_Prediction/blob/main/Age_churn_comparison.png)
4. Data Preparation
    All the features except for *Exited* is taken as the input feature and the output is created with the *Exited* feature.
    The dataset is then split into training and testing data and used in the model.
5. Model Building
    An Artificial Neural Network with hidden layer is created using **ReLU and sigmoidal** activation function, and the optimizer used is **adam** with a learning rate of 0.01.
    The accuracy of the model was found to be 87% and the loss measure used was **binary crossentropy**.
    
## End Results
The confusion matrix was plotted and below were the values achieved.
    
|  Description  | Precision         | Recall        | f1-score       | support      | 
| ------------- | ----------------- | ------------- | -------------- | ---------    |
| 0             | 0.87              | 0.97          |   0.92         | 1607         |
| 1             | 0.75              | 0.41          |   0.53         | 393          |
| accuracy      |                   |               |   0.86         | 2000         |
| macro avg     | 0.81              | 0.69          |   0.72         | 2000         |
| weighted avg  | 0.85              | 0.86          |   0.84         | 2000         |


## Libraries Used

- Pandas 
- Numpy 
- Seaborn 
- Matplotlib 
- tensorflow 
- keras
- sklearn
