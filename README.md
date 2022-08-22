# final-project-description
ABSTRACT:
________________________________________
According to the dataset considered, this situation deals with violation of laws and the features related to citations in court from different areas for different people. Most of the times when there is violation of law, the authorities settle it using charges. Few times there are cases where people are charged without commiting any violations or there are cases where people resist the charges for a inevitable reason. so in this work, for a citation, we are going to find if the hearing Status is issued or not meaning we are trying to understand how features of citations are affecting people who face any hearing status and people who don't have one. This helps us to know better about the current mindset of people and the mistakes made by them and in-turn provide a analysis for judistriction for easy flow of their work.

Trying to produce an intelligent, analytic solution for above discussed problem Using machine Learning techniques.
STEPS INVOLVED:
•	Data Acquisition
•	Data Analysis and Pre-Processing
•	Removing the columns which are insignificant
•	Exploratory data analysis
•	Future Engineering
•	Data Partitioning 
•	Modelling
Firstly,I imported all the necessary libraries 
converting the normal data like csv file into python understandable data such as array object of Numpy or Data Frame object of pandas. 
As data is very large, we are considering only a sample which we can handle
It is observed that the data has columns like 
     CitationNo                  
 1   LienCode                    
 2   ViolationDate               
 3   DueDate                     
 4   Agency                       
 5   FineAmount
understanding the basics of the data loaded. To have knowledge of number of columns, number of rows, their statistics, correlations etc. So that we can perform Data pre-processing STEP.
Here in this process it is found that the data has columns like liencode, violationdate, duedate, agency, etc.It is observed that the violation code section column has got around 190 unique values, The column block has got around 3412 unique values, The columns lot and neighborhood has got around 818,249 unique values respectively.

 DATAPREPROCESSING:
cleaning the data like removing the empty values, removing insignificant columns, removing outliers, encoding the data or filtering high correlation. preparing the data for giving it as input to the algorithm etc.   

1.	The original dataset has 204161 rows and 30 columns
2.	We are considering only first 50000 rows and 30 columns as population for the research.
3.	As the population has many columns, missing values and outliers. We will  be processing the population with many different dimensionality reduction steps as follows
a.	First removal of the columns with large number of categorical values as both one-hot encoding or label encoding will not reduce the dimension or will add bias to data.
b.	Second handling the missing values, as in the population we have missing values in only 2 columns and they are only 0.0044%  of the total data. So we will remove the rows with missing values.
c.	In few columns with continuous data, there were outliers which are being removed using Isolation Forest algorithm.
d.	Now object type of data has to be vectorized. Here we are using label encoder to handle columns with moderately high columns 
•	The process of data analysis involved, removing the columns which are insignificant
1.	columns with large number of unique values
2.	i am not performing time series analysis.as it is difficult to obtain appropriate measures, and there are problems with accurately identifying the correct model to represent the data. so, removing the columns with time related data.
3.	Exploratory Data Analysis (EDA) is an approach to analyzing datasets to summarize their main characteristics, often with visual methods. EDA is used for seeing what the data can tell us before the modeling task.
4.	This plot shows the information of distribution of lien code from the figure we can observe that lien code type n has the highest number of records when compared to the other type.
5.	2) This plot shows the information of distribution of agency. From the figure we can observe that the department of housing and community development type has the highest number of records when compared to the other type.
6.	3) This plot shows the information of distribution of citationstatus.From the figure we can observe that the type occured(o) has the highest number of records when compared to the other type.
7.	Distribution of violation code :This plot shows the information of distribution of violation-code article. From the figure we can observe that the type PM has the highest number of records when compared to the other type.
8.	Distribution of officer presence requested: This plot shows the information of distribution of violation-code article. From the figure we can observe that the type PM has the highest number of records when compared to the other type.
This Dist-plot shows the information of distribution of fine amount.it can be observed that most people paid a fine amount in between 0 to 1000.the highest fine amount would be 800
The pie plot is for citation status it can be observed that the citation status is  Occured for almost all the Citations. Where o stands for-Occured p-passed v-violated a-abscond
Future engineering:
Finding the percentage of missing values and handling them by removing the rows where there are missing values as the percentage of missing values is very less.
Handling outliers:
•	Finding outliers through different methods and getting rid of them by Using the Isolation Forest algorithm to finalize on the outliers
After outlier removal using the Isolation Forest
Handling the object/categorical type of columns
Eda on the processed dataset:
Setting the Features and Labels:
1)Selecting the Hearing-Status as labels 
2)So as to predict in which instance people can got to that extent for violation charges
3)If a citation has Hearing or not is only considered.
In the correlation matrix I have used a high correlation filter and removed all the values with high correlation values.
Data partitioning: 
As dataset is large. so, we are going with random samples for Training and Testing going with random state '7' as it has more instances in minority class

We are going with random samples for Training and Testing sets.
As in population, we have very less positive values
93.49377704420752% negative values
6.506222955792479% positive values
when random state '7' was used for splitting, it has more instances in minority class i.e. more positive values which helps in testing more on minority class
In training set, we are having
93.61251289486158% negative values
6.387487105138429% positive values
In testing set, we are having
93.0188468830155% negative values
6.9811531169844985% positive values
it is observed that both the training and testing set are following the ratios of the population.

selected metric system:
Accuracy Score
Precision Score
Recall
f1-Score
Confusion Matrix
ROC curve
out of all the above metrics, 'accuracy' helped the most in many cases like Decision tree, Random Forest, Logistic Regression where rest of the metrics like Recall, F1-score, precision were are 100% except for SVM Algorithm. Confusion matrix and ROC curve helped to understand the model better.
Results
we were able to classify the instances as having a hearing or not having with a very good performance of 99.96+ % even when there were few outliers were left in the data. Random Forest was best and decision tree, Logistic Regression was also performing close to best and SVM had many difficulties in classification as it is sensitive to the outliers.
Next steps:
1.	we have only considered a sample data from the population. for the complete data the procedure for data pre-processing may change
2.	all the outliers were not removed, few were left in the dataset. further understanding of the data in better way is possible.
3.	much better algorithms can be researched on that can handle the outliers like voting classifier.
4.	research can be done in finding a better representative sample. for training, validation and testing purposes by understanding the distributions of different random sample. And etc.
references:
•	1. https://medium.com/swlh/top-five-methods-to-identify-outliers-in-data-2777a87dd7fe
•	2. https://towardsdatascience.com/feature-selection-correlation-and-p-value-da8921bfb3cf







