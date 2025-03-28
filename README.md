# BANK-CHURN-PREDICTION

## Dataset Source

https://www.kaggle.com/datasets/adammaus/predicting-churn-for-bank-customers

## Description

This project leverages bank customer churn dataset and classification machine learning techniques to accurately predict customer churn, enabling proactive decision-making and improved customer retention
The project goal is to use this model to help the bank to retain its customers since Customers switching from one company to another  makes the company loose revenue.

<table border="1">
    <caption><strong>Key Factors Influencing Customer Churn in Banking</strong></caption>
    <thead>
        <tr>
            <th>Bank Churn Features</th>
            <th>Churn Influence</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Account tenure</td>
            <td>Longer tenure usually means lower churn risk.</td>
        </tr>
        <tr>
            <td>Credit score</td>
            <td>Poor credit/payment issues may indicate churn risk.</td>
        </tr>
        <tr>
            <td>Number of products (savings, credit cards, loans)</td>
            <td>More services often increase retention.</td>
        </tr>
        <tr>
            <td>Active or dormant status</td>
            <td>Low engagement signals potential churn.</td>
        </tr>
        <tr>
            <td>Monthly transactions</td>
            <td>Unpaid bills or reduced spending may predict churn.</td>
        </tr>
        <tr>
            <td>Customer complaints</td>
            <td>Frequent complaints can indicate dissatisfaction.</td>
        </tr>
    </tbody>
</table>

## Milestone 1

### Data Preprocessing

   <b>a.Data cleaning</b>
   
   Removed and fixed errors(e.g., handling missing values, duplicates, or incorrect data).
   
   <b>b.Data Transformation</b>
   
   Encoded categorical variables and scaled numerical features.
   
<b>c.Data Quality Handling</b>
   
   Detected and resolved outliers, ensuring consistency in data.
   
   #### Summary
   
   Started by identifying missing values in the dataset to check for any incomplete records. Next, I handled categorical variables by applying one-hot encoding, which converts text-based data into numerical format so that machine learning models can understand it. After that, I scaled numerical features using StandardScaler to ensure all numerical data is on the same scale, improving model performance.

To maintain data quality, I detected and removed outliers using the Z-score method, which filters out extreme values that could negatively impact model accuracy. I also removed duplicate rows to prevent redundant information from skewing the results. Once the data was clean, I saved the processed dataset into a dedicated data/ directory to keep things organized.

Finally, I updated the .gitignore file to exclude the cleaned dataset from version control. This prevents large or unnecessary files from being tracked in Git, keeping the repository clean and efficient. By following this structured approach, I ensured that the dataset was properly cleaned, optimized, and ready for analysis.

  ### Exploratory Data Analysis
  
<b>a.Descriptive Statistics</b>

Computed summary statistics (mean, median, mode, standard deviation) to understand the data distribution.

<b>b.Data Visualization</b>

Used histograms, box plots, and scatter plots to explore trends, distributions, and relationships.

## Milestone  2

### Data Modelling

<b>a. Model Selection & Training</b>

Machine learning Model -Logistic Regression.

Splitting data into training and testing sets.

Trained models on the dataset using appropriate hyperparameters.

<b>b. Model Evaluation & Optimization</b>

Evaluated models using metrics like accuracy, precision, recall, F1-score, and ROC-AUC.

Performed hyperparameter tuning (e.g., GridSearchCV, RandomizedSearchCV).

Used cross-validation to assess model stability.















