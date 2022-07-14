# Pandas_School_District_Analysis
## DESCRIPTION
Analyzing and aggregating data on student funding and students standardized test scores to showcase trends and school performance.

### SITUATION/TASK
* A high-level snapshot of the district's key metrics, presented in a table format
* An overview of the key metrics for each school, presented in a table format
* Tables presenting each of the following metrics:
  * Top 5 and bottom 5 performing schools, based on the overall passing rate
  * The average math score received by students in each grade level at each school
  * The average reading score received by students in each grade level at each school
  * School performance based on the budget per student
  * School performance based on the school size
  * School performance based on the type of school
  
#### CHALLENGE
The grades of the ninth graders at Thomas High School have been changed. While administrators do not know the full extent               of this academic dishonesty, they want to uphold the standards of state testing and have turned to you for help.
After assessing the situation with the school superintendent and Maria, you decide the best approach is to:

### APPROACH
* Remove the ninth-grade math and reading scores from Thomas High School.
* Keep all other data associated with the ninth-grade students and Thomas High School intact.
*	Filter DataFrames using logical operators.
*	Replace the incorrect values with NaN.
*	Explain how your PyCitySchools analysis changes after you handle the incorrect data.  
Also:
* Create a duplicate of PyCitySchools.ipynb and rename it PyCitySchools_Challenge.ipynb.
* Correct the students' names so there are no professional prefixes or suffixes.
* Replace the reading and math scores for ninth graders at Thomas High School with NaN.
   * Use loc on the student_data_df DataFrame to select the columns by condition.
   * Set the column you want equal to "NaN" by using np.nan for the reading and math scores separately.
   (Hint: Read the Pandas documentation on the loc method (Links to an external site.)
 * Merge the clean student data with the school dataset.
 *	After removing the reading and math scores, answer the following questions:

### RESULTS
 * How is the district summary affected?

Removing the math & reading scores for 9th graders from Thomas High School, has an almost no effect
but negative impact nonetheless on the overall district summary. The average math and reading scores
dropped from 78.98% to 78.00% and 81.87 to 80.89, respectively. Because the overall percentage change is very minimal, 
from 80.39% to 79.26% after the 9th grade scores have been removed, it is safe to say that the overall district summary
was not hugely impacted. 

 * How is the school summary affected?

Unlike the district summary, the school summary was greatly inpacted. For THS, the average math and reading scores went from 83.41 to 59.85 and 83.84 to 60.24, respectively, after the removal of the scores for 9th graders. As a result,the % Passing Math and reading scored for THS went from 93.27 to 66.9 and 93.31 to 69.66, though the %Overall Passing did not change.

 * How does removing the ninth graders’ math and reading scores affect Thomas High School’s performance, relative to the other schools?

Prior to the removal of 9th grade math and reading scores, Thomas High School (THS) was the second top-performing
school. After the removal and average scores in math and reading going from 83.41 to 59.84 and 83.84 to 60.24 respectively, 
Thomas High School is the lowest performing school. While Pena HS rose to number1 top-performing school.

 * How does removing the ninth-grade scores affect the Math and Reading Scores by Grade.

The THS 9th graders received a math & reading score of "0" from previously, 83.6
All other grades, 10th, 11th & 12th in THS maintained their scores.
All other grades, 9th, 10th, 111th, 12th in all the other schools were not impacted.

 * Scores by School Spending, Scores by School Size, and Scores by School Type? 

|Scores by School Spending:      |      |  |
| ------------- |:-------------:| -----:|
|Before      | |  |
|Avg_math:     83.41  | Avg_Reading: 83.84      | %Passing_Reading:    97.31|
|After  
|Avg_math:     59.84  |Avg_Reading:     60.24    | %Passing_Reading:    69.66|

The above shows a change in scores by school spending




* Scores by School Size: 
Thomas High School is in school size bin Medium (1000-2000). Scores before and after differs by medium schoool size as follows:

|Scores by School Size:     |      |  |  |  |
| ------------- |:-------------:|:-----:|:-----:|:------:|
|Before      | |  | | |
|Avg_math:   83.37  | Avg_Reading: 83.86   | %Passing_Reading: 96.79| %Passing_math:  93.60 | %Overall Passing:  94.82 |
|After  
|Avg_math:    78.7 |   Avg_Reading: 79.1    | %Passing_Reading:     91| %Passing_math:     88 |  %Overall Passing:     90 |




* Scores by School Type:

| Scores by School Type:   |      |  |  |  |
| ------------- |:-------------:|:-----:|:-----:|:------:|
|Before      |School Type | Avg_math  |Avg_Reading | %Passing_Reading |
|          |Charter   |83.5| 83.9 |97 |
|After  
|          |Charter  | 80.5|80.9 | 93|

There were no changes in District type schools.

* Conclusion: All scores by (school spending, school size, school type) were all impacted/dropped due to the removal of the THS 9th grade math and reading scores.

### Outcomes of Challenge:
* Open Jupyter Notebook files from local directories using a development environment.
* Read an external CSV file into a DataFrame.
* Format a DataFrame column.
* Determine data types of row values in a DataFrame
* Retrieve data from specific columns of a DataFrame
* Merge, filter, slice, and sort a DataFrame.
* Apply the groupby() function to a DataFrame.
* Use multiple methods to perform a function on a DataFrame.
* Perform mathematical calculations on columns of a DataFrame or Series.

### SOFTWARE/TOOLS/LIBRARIES
Anaconda 4.13, Jupyter Notebook, Pandas, PythonData environment using Python 3.7.6                  
