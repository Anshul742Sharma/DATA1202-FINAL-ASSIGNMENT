# DATA1202-FINAL-ASSIGNMENT
## Introduction
This repository contains the Jupyter Notebook for Data 1202 Lab 3: Data Analytics Tools. The objective in this lab is to discover different ways to convert categorical features to numerical values. The notebook contains step-by-step explanations and code solutions of:
- Replacing value: Substituting specific values in a dataset
- Encoding labels: Labeling categorical variables with numbers
- One-Hot encoding: Coverting categorical variables into binary numbers (numerical numbers)

Encoding categorical data is crucial for machine learning models, because majority of machine learning models require numerical data. This lab shows how to use several encoding methods and analyze the outcomes
## Getting Started
### Required library
To run this notebook, we will need to have python installed with some of important libraries:

- NumPy: For numerical operations
- Pandas: For data manipulation and analysis

### Installing
we can install the required libraries using:
#### pip install numpy pandas

## Encoding Techniques
### Replacing values:
A simple approach for replacing values is applied when a categorical variable has a definite mapping to numerical values. For example:

#### import pandas as pd
#### data = {'Category': ['Low', 'Medium', 'High']}
#### df = pd.DataFrame(data)
#### Define a mapping
#### mapping = {'Low': 1, 'Medium': 2, 'High': 3}
#### df['Category'] = df['Category'].map(mapping)
#### print(df)
It will replace 'Low', 'Medium', 'High' with 1, 2, 3 respectively.

### Lable encoding:
A technique used in machine learning and data analysis to convert categorical variables into numerical format. For example:

#### from sklearn.preprocessing import LabelEncoder
#### le = LabelEncoder()
#### df['Category_Label'] = le.fit_transform(df['Category'])
#### print(df)
Each unique value in the column is assigned an integer.

### One-Hot encoding:
One-Hot Encoding converts categorical variables into a series of binary variables (0s and 1s). It is useful when categories are non-ordinal. For example:

#### encoded_df = pd.get_dummies(df, columns=['Category'])
#### print(encoded_df)
This assures that an inaccurate ordinal relationship between categories is not assumed by machine learning models.

## Running the notebook
To run the notebook:
- Download the dataset auto.csv
- Open Jupyter notebook
- Navigate to directory containing Lab3_ipynb
- Open the notebook and run the cells sequentially

## Running the tests
To verify the results:
- Print the dataset before and after transformation to confirm expected changes.
- Check for missing values after encoding.
- Ensure that One-Hot Encoding creates the correct number of columns.

## Deployment
This notebook is intended for local use and educational purposes. It does not require deployment.

## Author
Anshul Sharma

## License
This project is licensed under the MIT License

## Acknowledgments
- Data 1202 course instructors
- Online Python documentation and tutorials
