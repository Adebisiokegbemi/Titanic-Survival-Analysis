# Titanic-Survival-Analysis
Data Source
The dataset used for this analysis was gotten from the kaggle. The dataset consist of titanic ship passenger details with 891 rows and 12 Columns with lots of missing data.

Tool used for analysis
Microsoft Excel

Justification for Using Microsoft Excel
I used Microsoft Excel for this analysis because this dataset is not  large, contains 891 rows and 12 columns. Excel can handle this amount of data and pivot table which is a powerful tools for used summarizing, analysing and to allowing quickly cross tabulate different variables and explore relationships in the dataset for this analysis.

Data cleaning and processing
The data consists of missing values and inconsistencies. To enhance the readability of the data, ensure data consistencies and accuracy, I took the following steps across the columns below;

Pclass: The Pclass in the titanic data set initially represented with numerical values  from 1 to 3. To enhance the understanding of the data, I recode each numerical value as 1 to be 1st Class, 2 to be 2nd Class and 3 to be 3rd class using the IF function: IF([@Pclass]=1,"1st Class",IF([@Pclass]=2,"2nd Class","3rd Class")) and named the column passenger class
Survived:  I used the IF function to recode the numerical values. For 0 to be dead and 1 to be alive and named the column survival status
Name: I used text to column to extract each passenger title to serve as a proxy for social status, which may have influenced survival rates. For example,  Sir and Lady are likely to belong to higher classes, to infer age group and marital status, and to verify gender information in case where the sex field might have errors or be missing and named the column  Passenger Title
![image](https://github.com/user-attachments/assets/a8d6760b-f72f-4745-8d3b-841510bd95e8)


Sex: to ensure data consistency and accurate labelling of all values as either Male or Female so I use the Proper Function 
Age:  some of the passengers age were missing and some were in decimal place. To correct this, I formatted the decimal to whole number using the round up formular and  I replaced the missing values in age column by using descriptive statistics as common approaches in replacing missing values with mean, median or mode age of the available data. In this case I used the mode (24). This is to to promote a more accurate representation of the passengers ages on the titanic.
Age category: the age column was categorized into distinct age categories to facilitate easily analysis and to make it easier to compare survival rates across different age groups.  I also used the if functions to categorised the age: IF([@Age]<13,"Children",IF([@Age]<18,"Teens",IF([@Age]<30,"Young Adults",IF([@Age]<60,"Mid aged Adults","Seniors"))))
Embarked: I  replaced the missing embarked with mode (S) as it is the highest occurrence embarkment . on research, I found out the three embarkment points of the titanic ship England (Southampton) , France (Cherbourg”) and Ireland (Queenstown). I used the if function =IF([@Embarked]="Q","Queenstown",IF([@Embarked]="S","Southampton","Cherbourg")) to rename the embarked and named it embarkment and it is used for this analysis. With this findings,  I ensured that the port names were accurately represented in the dataset. 
Cabin: There  were lots of missing values in the cabin, so I excluded it in my analysis.
Tickets: It has complex strings which on critical analysis it doesn’t answer my research questions.  I believe that doesn’t have a clear and direct relationship with survival rates and other key factors I intend to analyze, so I excluded it from my analysis.
Fare: This shows the cost of each passenger's tickets, I rounded this up to 2 decimal place and format data type to currency (pounds) 
![image](https://github.com/user-attachments/assets/7364f2fc-cbe4-404f-8545-b5564b9779b5)


