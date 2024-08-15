**Titanic Dataset Preprocessing**

This repository includes scripts for preprocessing the Titanic dataset. The preprocessing steps include handling missing values and removing outliers.

**Dataset**

The Titanic dataset contains the following columns:

* PassengerId: Identifier for each passenger.
*  Survived: Survival status (0 = No, 1 = Yes).
*  Pclass: Ticket class.
*  Name: Name of the passenger.
*  Sex: Gender of the passenger.
*  Age: Age of the passenger.
*  SibSp: Number of siblings/spouses aboard.
*  Parch: Number of parents/children aboard.
*  Ticket: Ticket number.
*  Fare: Fare paid for the ticket.
*  Cabin: Cabin number.
*  Embarked: Port of embarkation.

**Prerequisites**

* Python 3.x
* pandas library

  **Scripts**

  **1. Data Cleaning**
   
This script handles missing values in the dataset and drops columns with excessive missing data.

**Description:**

**Loading the Dataset:**---> Reads the dataset from train.csv.

**Filling Missing Values:**

'Age' is filled with the median age.
'Fare' is filled with the mean fare.
'Embarked' is filled with the mode of the 'Embarked' column.

**Dropping Columns:**

* The 'Cabin' column is dropped due to excessive missing values.
* As 'PassengerId' has unique passenger info so should drop it.

**Output:**

Prints a completion message and the final shape of the dataset after cleaning.

**2. Outlier Removal**

This script removes outliers from numeric columns using the Interquartile Range (IQR) method.

**Description:**

**Function Definition:**--> Defines a function to remove outliers from numeric columns.

Uses IQR to calculate the bounds for outliers.

Filters the DataFrame to remove outliers and prints the number of outliers removed from each column.

**Output:**

Returns the cleaned DataFrame and the total number of outliers removed.

**Conclusion**

**Data Cleaning:**  Missing values in 'Age', 'Fare', and 'Embarked' were handled, and the 'Cabin' and 'PassengerId' column was dropped.

**Outlier Removal:**  Outliers were removed from numeric columns, and the total number of outliers removed was reported.

