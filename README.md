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
<img width="892" alt="image" src="https://github.com/user-attachments/assets/65ff6ea9-3f7b-45a2-a3d1-e282b36b30b9">
<img width="915" alt="image" src="https://github.com/user-attachments/assets/1cdc698c-bcdc-44a4-abbe-0ac109100b73">

KEY INSIGHTS AND TRENDS

Passenger Demography
The average age of the passenger is  29. passenger age ranges from 0.4 (months) to 80 years old. Majority of the passenger were travelling in third class
Passenger Survival Analysis
Survival rate based on sex and age category
Female had a significant higher survival rate 68% while Male has a survival rate of 32%. Women had a higher survival rate when compared to men. Young adults within the age category "18-29" has higher survival rate when compared to mid aged adults and seniors which account to approximately 38% of the passengers in the titanic dataset survived the titanic shipwreck. I believe the women and children first rule was enforced during the titanic evacuation and the social norms was widely followed in the cause of the event which eventually had a great impact on the survival rate of the titanic shipwreck. 
Survival analysis based on passenger class
On analysis, it was revealed that 1st class passengers has the highest survival rate of 40%, followed by third class passengers with 35%-, and second-class passengers with the lowest survival rate of  25%.

Survival rate by Embarked Point
Prior to thorough analysis, 72% of the total passenger boarded from Southampton making it the largest embarked point. 64% of the passengers that boarded from Southampton survived the titanic shipwreck with 61% being Female.

Survival rate by passenger title
Passenger title has a slight correlation with survival rates on the Titanic. However, this correlation was largely a reflection of broader factors such as gender and passenger class, which were primary determinants of survival probability. Titles associated with women, children, and higher social status generally corresponded with higher survival rates, while those associated with adult men typically had lower survival rates.
![image](https://github.com/user-attachments/assets/fbe3d3fd-8539-46d9-ada1-a57ccecbd914)

Survival rate by family size 
Having family members on board slightly improved the survival rate of titanic, I believe this  was most pronounced for passengers with smaller families and those in 1st class. Larger families, especially in 3rd class, faced more challenges in surviving the the titanic. In addition, given that the enforced women and children first rule may have also played a role in these survival patterns, particularly benefiting families with children.
![image](https://github.com/user-attachments/assets/98be03d9-a43b-4576-939d-2a523a381091)
