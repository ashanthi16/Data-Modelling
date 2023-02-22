## Data-Modelling
### **1.0 Introduction**
Purpose of this report is to further analyse the key factors driving high staff turnover issue. Applying appropriate machine learning models to distinguish the relationships, patterns causing this employee attrition matter and predict the next potential leavers and make practical recommendations to RI Consultant management to conquer this challenge.

There will be several steps undertaken to go through this process and this report will describe the below content

 *Univariate and Multivariate analysis to understand all the columns individually as well as their relationships with each other
 
 *Create several data models with various clusters
 
 *Evaluating the best cluster by comparing the models
 
 *Analyse the cluster and its characteristics for prediction and recommendation for the management


### **3.0 Methodology**
#### **3.1 Overview**

The main focus of this project is to find the answers to below questions.

*What makes employees leave the company?

*Why do employees think that Revolution Consulting is not a good company to work?

*Do the employees go through unnecessary challenges in the workplace which affect their personal life?

*Are there a Gender discrimination in the company like Gender biased pay gap?

*Any pay gap within the ages?

*Are the employees not valued or paid according to their expertise levels or effort they put in so that they are not motivated to work in Revolution Consulting

In order to answer these questions few data models will be created from this dataset and different clusters to investigate the patterns and relationships among the models. Based on these relationships and patterns, predictions can be made to find the next set of leavers from the company. Also the organization will be able to understand the possible causes and characteristics for this high turnover ratios and create a management action plan to retain its employees.

### **3.2 Process**

*First step was to undergo univariate analysis of all the columns to understand characteristics of the each and every columns. As there were 21 columns to explore, this evaluation helped to decide which columns are more important and directly relates to answering the research goals.

*Then processed a multivariate analysis to identify the relationships and patterns of the dataset

*Decision was to subset two sets of data frames to use for the model. 

* 1. One data frame with all columns and in order to work out this method, had to transform all the categorical columns to a numerical column and subset as a new 
data frame.
* 2. Second data frame with only numerical variables and subset a new data frame.
     
*In order to find out the best k for the k means model, evaluated elbow method and silhouette coefficient score. Also found the most appropriate epsilon for the DBSCAN as well.

*Created 4 data models, 2 models using k means and 2 models with DBSCAN

### **3.3 Evaluation strategy**

*First step was to draw two plots for Elbow method and Silhouette coefficient score to find the most appropriate k. In the elbow plot, best k was chosen when there’s a significant WCSS drop. In the Silhouette plot best k was selected based on the highest silhouette coefficient was shown.

*Then based on the k means scores two models were plotted with subsetting all the columns and subsetting only the numerical columns.

*For the DBSCAN, the distance graph was plotted to find the most appropriate epsilon. Then afterwards two models were plotted subsetting all the columns and subsetting only numerical columns.

*Then created 4 plots using the same variables to compare how the clusters look in the graphs.

*Best model was chosen how the clusters are sensibly distributed among the models and the best cluster within that model was chosen by the clusters which had highest turnover ratios as my research goal was to identify the causes for the turnover and predict next possible leavers.


### **4.0 Data modelling and exploration**
#### **4.1 Exploratory Analysis**
#####**4.1.1Univariate Analysis** 
Below columns were analysed individually to get an understanding of the dataset

Fig 1 – This pie graphs shows what percentage of resigned and current employees in this dataset. The majority in this dataset - 84% are current employees and the remaining 16% is only the resigned staff. Even though the resigned portion is comparatively a low figure, but the characteristics of the resigned staff will be a vital analysing factor when predicting the next in line for resignation.

Fig 2 – This Age analysis swarmplot displays the fact that majority of the employees are within the age group 25 – 40 and comparatively there’s a smaller number of employees are within the age group 50 to 60.

Fig 3 – Business Travel Analysis pie graphs brings out the fact that 71% of employees travel rarely and only 19% travel frequently and remaining 10% not travelling at all. According to these statics we could say that Business Travelling wouldn’t be a reason for the employee high turnover rates, if the employees in this organisation are not looking forward for business travelling. This could be further analysed with other variables.

Fig 4 – According to Business Unit Analysis pie graph, highest percentage of employees are Consultants 65% and remaining 30 % and 4 % are Sales and Business Operations respectively.

Fig 5 – This boxplot chart analysing the education level describe the fact that, education levels has been ranking from 1 to 5 and 1 being the lowest level and 5 being the highest. The mean education level is 3 and most of the employees are with the education level ranking 2 to 4. There’s very few we could see who have achieved the highest level of education.

Fig 6 – Gender Analysis pie chart exhibits that majority of the employees 60% are Male and remaining 40% are Females. This depicts the fact that company is not gender biased as there’s no major difference between the representation of two genders.

Fig 7 – Job Satisfaction Analysis is a ranking bar chart where 1 being not very satisfied to 4 being highly satisfied. According to these statics most of the employees are within the rank 3 to 4 which portraysthe fact, employees are satisfied with their jobs. There’s very few who are not satisfied with the job and this range needs to be further analysed to boost up their satisfaction level.

Fig 8 – Marital Status Analysis pie chart comes up with the findings of 46% of employees are married and 32 % are single whereas only 22 % are divorced. This is vital information to be analysed further with other columns to predict how marital status could impact employee’s job.

Fig 9 – Monthly Income Analysis histogram demonstrates that most of the employees are within the salary range 2500 – 5000. Only few numbers of employees are in the high-end salary bracket. Further we could say that monthly income is not affectively distributed among the company as most of the employees are within the low-end salary scheme.

Fig 10 – Over Time Analysis pie graph portraits that 72% employees are not doing any overtime and only 28% are doing overtime in their job roles. This analyse the fact that Over Time could not be a factor for the high staff turnover ratios.

Fig 11 – Percent Salary Hike graph characterizes the element that most of the employees are within the range of 10% – 15% hike and very few of the employees are in the highest salary hike which is ranging 20% - 27%.

Fig 12 – Performance Rating Analysis histogram illustrates the aspect that all the employee’sperformance ratings are within 3 to 4 which is the high end and among them the highest number of employees are in the level 3. These statics depicts that performance rating variable is not a reason for the employees to leave the organisation.

Fig 13 – Average Weekly Hours Worked Analysis depicts the results that most of the employees are working 40 hours per week and very few of them worked beyond normal office hours and there’s a very low number of employees work within 60 – 75 hours range and these employees should be further analysed as its not a healthy attribute for the organisation.

Fig 14 – Total Working Years Analysis graph shows that majority of the employees are within the range of 0 – 10 years of career. Comparatively very few who have worked 20 – 40 years in their career.

Fig 15 – Training Times Last Year Analysis Histogram shows that majority of the employees have received 2 to 3 trainings last year. Around 50 employees who hasn’t received any training last year and these employees should be further analysed to see if they are just started new commers.

Fig 16 – Work Life Balance Violin graph represents the fact that most of the employees have ranked 3 which says they moderately balance the work life and further analysisshould be done to the employee who ranked 1 and 2 says not having a work life balance.

Fig 17 – Years at Company Analysis stripplot signifies the point that mainstream of the employees are within the range of yeas 0 to 10 but within that criterion more towards 0 to 5 years. The numbers keep decreasing the range 10 – 40 years and only 1 employee who has worked 40 years in the company.

Fig 18 – Years Since Last Promotion violin graph indicates that majority of the staff haven’t had a promotion at all and there are some employees who had promotions since 1 to 2 years. This is a variable which needs to be further analysed to have a good understanding.

Fig 19 – Years with Current Manager Analysis boxenplot chart illustrates the static that mainstream of the employees are in the range 1- 6 years. There are considerable amount of employees who haven’t completed a year with the current manager and that’s another area which needs to be further analysed to understand if employees are happy with their current manager.

Key Findings

* Majority of the employees belong to the young work force
* 71% of employee are not doing travelling in their roles and assuming that Business Travel variable could not be a reason for high staff turnover
* 65% of employees are Consultants
* Employees mean Education Level is 3 and most of the employees are within the range 3-4. Only very few in the high-end Education Level which is 5
* Not a Gender bias company. Fair number of employees represent both genders.
* Most of the employees are satisfied with their jobs but special attention should be given to the employees who are not satisfied to boos up their satisfaction levels
* Majority – 46% of employees are married 32% single
* Most of the employees are within the salary range 2500 to 5000 and highest among that is employees receiving salary of 2500.
* 72% of employee are not doing Overtime and this variable is not contributing to the high staff turnover rates.
* Employees salary hike is within the range 10% - 15%
* All the employees are within the performance rating 3 – 4 and this depicts the fact that all employees perform well.
* Most of the employees work 40 hours a week and the employees who work more than that should be further analysed 
* Most of the employees moderately have a work life balance (ranked 3) and further analysis should be done for the employees ranked 1-2.
* Majority of the staff hasn’t got a promotion at all and need to examine more on this fact as to see if they are new commers or what reason they couldn’t have a promotion

#####**4.1.2Multivariate Analysis**

Fig 20 – This pairplot chart investigates relationships of below variables as below

* Average Weekly Hours Worked VS Age by Resigned – Majority of the employees are working 40 hours per week and their age range is within 20 – 40. Another vital factor which this graph demonstrate is, highest number of resigned employees have worked more than 40 hours.
* Age VS Monthly Income by Resigned – Most of the employees are in the lower salary bracket which is 2500 to 5000 and majority of the resigned employees were also in the same lower salary range. Mainstream of the Age group which is 25 – 40 are in the lower salary range.
* Age VS Job Satisfaction by Resigned – Employees who are satisfied with their job mostly belong to the Age range 25- 45. Surprisingly the highest number of resigned
 employees were satisfied with their jobs.
*  Job Satisfaction VS Monthly Income by Resigned – Employees who are satisfied with their jobs are both in lower salary range as well as higher salary range. 

Fig 21 /22 – Monthly Income per Gender per Business Unit per Resigned sun burst interactive chart illustrates the attributes of many relationships as below.

* Out of the current employees there are more male consultants than female consultants and female consultants have a higher average salary compared to male consultants
* When looking at the average salary rates of other two departments female employees have a higher average compared to the male employees.
* Greater part of the employees resigned are Males and when comparing the average salaries of the resigned employees, Females had higher average compared to Males.

Fig 23 – Monthly Income VS Years Since Last Promotion Analysis displays the point that majority of the employees haven’t received a promotion and they are in the lower salary range which is less than 5000. Similarly, the second majority who received a promotion with 1 – 2 years are also in the lower salary bracket.

Fig 24 – Work Life Balance VS Years Since Last Promotion plot displays the statistics that employees who haven’t had a promotion are the majority to say that they maintain a work life balance. Employees who haven’t had a promotion at all and rated as no work life balance should be further analysed.

Fig 25 – Years at Company VS Years Since Last Promotion Analysis plot exhibits the argument that most of the employees have resigned haven’t got a promotion at all and they have been in the company for 0 -10 years. Among them the majority is within the 0 – 1 year’s range.

Fig 26 – Percent Salary Hike VS Average Weekly Hours Worked by Gender and Resigned plot reveals that employees who are at the high end of weekly hours worked irrespective of the salary percent hike, have resigned. There’s a concern regarding the current employees in that peak range.

Key Findings
* Majority of the resigned employees have worked more than 40 hours per week and they were in the salary range 2500 - 5000.
* Common Age group 25- 40 is in the lower salary range which is 2500 to 5000
* Most of the resigned employees were in the lower salary bracket which is 2500 – 5000
* Employees who have ranked the job satisfaction level 3-4 are the mostly to resigned.
* Female employees have a higher average salary compared to male employees.
* Majority of the employees haven’t received a promotion at all and they are in the less than 5000 salary range similarly the employees who received a promotion in 1-2 years also in the same salary range
* Mainstream of employees who had a work life balance haven’t had a promotion at all.
* Majority of employees who have resigned haven’t had had a promotion at all and they have been in the company 0-1 years.
* Employees who were at the higher end of average weekly hours worked, have resigned irrespective of the percent salary hike. Should be concerned about the current employees in that range.

####**4.2 Data Modelling**
#####**4.2.1 Modelling process**
I will be using two modelling processes as below

* K – means Model
* DBSCAN Mode

######**4.2.1.1 K – Means [Model 1]**
In this model I will be subsetting the whole columns for the cluster analysis. In order to work out this model, I have transformed all the categorical variables to numerical variables and subset the data as a new data frame. In this model, I would need to find the most suitable k for the model and therefore running the below methods first to identify the best k.

######**4.2.1.2 K – Means [Model2]** 
In this model I will be subsetting the numerical columns only for the cluster analysis. For this model I 
have created a separate dataset with only numerical variables. As per the model 1, most suitable k 
has to be found to this model too.

In all these K – means models the most suitable k is found out by using the below two methods

* Elbow method using Within Cluster Sum of Squares (WCSS) – This k-means algorithm aims to form the clusters in a way that minimises the WCSS. Here WCSS is recorded for each k and then plot the results.

*  Silhouette method – In this method, to calculate the mean silhouette coefficient will be using the silhouette_score() function and then plot the results to find the better k.

4.2.1.3 DBSCAN [Model 1] 
In this model I will be subsetting all the columns for cluster analysis like k means model 1. In order to 
find the appropriate number of clusters, most suitable number for the epsilon should be found out.

