# Return on Financial Investment in American Public School Systems
##### Chase Yarbrough, Jinyoung Eum, Ved Mohan

### Introduction
Education is a pillar of society that factors into decisions with a variety of scopes with both short term and long term implications. A strong public education system has resounding implications ranging from which district families chose to settle in, adjacent property valuations, and larger more abstract relationships such as the financial growth of countries in the long run.

##### Motivation
Given a limited amount of funding each year, state and federal administrations are tasked with investing in various aspects of public education in order to improve the overall quality of learning.
Our goal was to create a tool which demonstrates which areas to target spending and investments in order to receive the highest return on education quality.

##### Problem Statement
X dollars invested in Y area will result in an average increase in educational performance by Z.

### Data
Two different sources of data were used, testing data and financial data

##### Test Data
Test score data from  National Assessment of Educational Progress (NAEP testing). NAEP has been selected as it is a standardized test administered at two grade levels, 4th grade and 8th grade. There are two different scores, measuring Math and English performance.

Some characteristics of this data:
1. Test scores are available biyearly in each state from 2007 to 2017.
2. Tests were given to 4th and 8th graders in Math and Reading and the average score by state is used.
3. For 8th graders the average math test score is 282 and the average reading test score is 265.
4. For 4th graders the average math test score is 240 and the average reading test score is 221.


Dataset source: 
* https://nces.ed.gov/nationsreportcard/


##### Financial Data
Financial data was sourced from the United States Census. Data between 2008 and 2017 tracked individual areas of investment on a state by state basis. The categories were as follows:

* Salaries and Wages
* Employee Benefits
* Pupil Support Services
* Staff Support Services
* General Administration
* School Administration
* Operation and Maintenance of plant
* Pupil Transportation
* Other

ENTER SNAPSHOT OF DATA HERE

Dataset source: 
* https://www.census.gov/data/tables/2008/econ/school-finances/secondary-education-finance.html


#### Dividing Further into the Dataset
Plotting Overall Score Average over the Years 2007-2017

![Image 1](project1.PNG)"

Score average is slightly skewed, but loosely follows a gaussian distribution. This allowed us to continue without applying a normalization transformation such as Box-Cox. However, due to the order of magnitude difference between factors, columns were normalized relative to themselves.

### Procedure
We intend to perform a linear regression on aspects of each school system’s financing as well as the past year’s test scores against the current test scores to give an overall predictive formula for the change in a school’s performance based on differences in a state’s financial plan.
![Image 2](project2.PNG)"

A preliminary check was done using a Pearson Correlation test. This checked the individual correlations between All Financial Investment Areas and Overall Score Average
![Image 3](project3.PNG)"

Highest correlation is Per Pupil Instructional Spending at 0.38. This seems reasonable: increasing spending per capita would positively affect performance. However, Pearson Correlation does not account for the impact of the variables combined. 

#### Supervised

In order to build on the preliminary exploration, a multiple regression model was created. Test and training data were split 20:80 respectively. 

Model Performance:

* Mean Absolute Error: 0.0151
* Mean Squared Error: 0.0003
* Root Mean Squared Error: 0.0176

![Image 4](project4.PNG)"

A sampling of the model performance (blue) versus actual data (orange)

A summary of the coefficients returned:

![Image 5](project5.PNG)"




To explore whether further investigation was required, the highest correlated factors were clustered by Overall Score Averages. Interestingly there was a strong linear correspondance, however, no clear clustering pattern emerged. 

INSERT IMAGE OF 

The

#### Unsupervised


### Supervised




![Image 6](project6.PNG)"
![Image 7](project7.PNG)"

### Unsupervised
![Image 8](Screen Shot 2020-04-08 at 11.24.17 PM.png)"
![Image 9](Screen Shot 2020-04-08 at 6.38.24 PM (1).png)"
![Image 10](Screen Shot 2020-04-08 at 6.38.41 PM (1).png)"
![Image 11](Screen Shot 2020-04-08 at 6.40.01 PM (1).png)"


### Conclusion
