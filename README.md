# FRAUD_TRANSACTION_PREDICTION
## Introduction
Fraud transaction prediction is a critical area of study in the realm of data science and machine learning, primarily aimed at detecting fraudulent activities in financial transactions or any other domain where deception or misrepresentation may occur. With the rise of online transactions and digital payment systems, fraudsters have become increasingly sophisticated in their techniques, making it essential for businesses and financial institutions to employ advanced methods to safeguard their operations and customers.
## Objective
The objective of fraud transaction prediction is to develop predictive models that can identify and flag potentially fraudulent transactions in real-time or near-real-time, minimizing the impact of fraudulent activities on businesses and consumers. These models are trained on historical transaction data, which includes both legitimate and fraudulent examples. By learning patterns and characteristics from this data, the models can generalize and detect suspicious activities in new transactions.
## About the data
The data set is extracted from Kaggle. The data contained 6362620 rows and 11 columns.
## Methodology
### Data Cleaning
In the cleaning process, I have checked for null values and there was no null values in the data. Then I dropped unnecessary columns such as step, nameOrig and nameDest. After that I have dealt with Multicollinearity. It was noticed that variables - ‘oldbalanceOrg’ , ‘newbalanceOrig’ , 'oldbalanceDest' and 'newbalanceDest' have a high VIF value, meaning they can be predicted by other independent variables in the dataset. There are not much outliers in the data. So I ignored that part.
### Analyzing the data
After carefully analyzing the data, the data is found imbalanced.  We can see that the target column is highly imbalanced. For handling the imabalanced dataset we need to use the SMOTE technique. 
### Scaling the data
Before scaling we'll have to encode all categorical variables to numerical. Here all columns are numerical. So there was no need to do encoding.
Why do we scale datasets?
Different features might have different units, ranges, or magnitudes. If we don't scale the features, some variables with larger scales might dominate the learning process, leading to biased results.
Scaling can help machine learning algorithms converge faster.
Here I have used a MinMax scalar to scale the datasets. MinMaxScaler is a data preprocessing technique used in machine learning to scale numerical features to a specific range. It transforms the original features into a new range, typically between 0 and 1, by preserving the relative relationships between data points.
### Performing the column_transformations to convert all columns into numerical form
 Applied LabelEncoder to encode the target column.
 Column Transformation (Categorical to Numerical)
### Applying SMOTE technique
SMOTE (Synthetic Minority Over-sampling Technique) is a data augmentation method commonly used in imbalanced machine learning problems, particularly in the context of binary classification tasks. Imbalanced datasets are those where one class (the minority class) is significantly underrepresented compared to the other class (the majority class). In such cases, traditional machine learning algorithms may struggle to learn from the data and tend to favor the majority class, leading to biased and inaccurate predictions.
### Modeling
Logistic Regression - It is a popular and straightforward algorithm used for binary classification tasks, making it a suitable choice for fraud transaction prediction where the goal is to predict whether a transaction is fraudulent or not (binary outcome). In this context, the dependent variable (target) is binary (fraudulent or not fraudulent), and the independent variables (features) can be numerical or categorical. This model has given good results. Its accuracy scopre is 99.97%.
 
