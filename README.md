# School_District_Analysis
pandas environment analysis

## Purpose
In this analysis, the pandas library in jupyter notebook was used to address seven schools within a district to capture key metrics including the top 5 performing schools and 5 worst performing schools, average math and reading scores, school budgets, and how school size, type and budget affect overall school performance. DataFrames for each output were created for easy visualization. After running this analysis, the school board notified that the completed csv file shows evidence of academic dishonesty, specifically the ninth grade scores for Thomas High School (THS). In order to uphold state-testing standards, the school district analysis was ran again, replacing the math and reading scores for Thomas High to understand how this change affected the overall analysis.

## Process & Data
After running the analysis, we can see how each of the seven school district metrics was affected by the changes in the data:

![school_district_1](https://user-images.githubusercontent.com/79612565/114319759-b58cb900-9ac7-11eb-945b-ffb97c4673b4.png)


- **School summary:** In the first analysis, merge() was used to generate a single school data summary based on school name for student_data and school_data
To solve for the 9th Grade THS scores, np.nan was used to remove their math and reading from the district summary DataFrame:

![school_district_2](https://user-images.githubusercontent.com/79612565/114319768-bcb3c700-9ac7-11eb-86e5-4e52af70bc2f.png)



- **District summary:** In the first analysis, a snapshot across all schools in the district was created after calculating passing_math, passing_reading and overall_passing count and percentages:
 ![district_summary_1](https://user-images.githubusercontent.com/79612565/114319771-c1787b00-9ac7-11eb-8d75-1e30fde1a7ba.png)

 
 After taking THS 9th grade out of the school summary, we can see the the average scores and percentages increase marginally for the distrcit:
![district_summary_2](https://user-images.githubusercontent.com/79612565/114319778-c5a49880-9ac7-11eb-865d-f4e117072a9b.png)


## Challenges
Determining data types: all of the columns needed for calucaltions are intergers so any data which contained numbers as strings rather than intergers must be converted using float
Missing Data: with such large amounts of data, it's important to address anything missing
Cleaning Data: in this anlysis, pre-fixes and suffixes skewed school records and must be removed from student_name. These names cannot be dropped sicne it would affect total student count, negatively impacting the analysis

## To Wrap it Up
Summary: Summarize four major changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.There is a statement summarizing four major changes to the school district analysis after reading and math scores have been replaced

Does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
- Replacing the ninth-grade scores affect the following:
Math and reading scores by grade
Scores by school spending
Scores by school size
Scores by school type

removing 9th grade scores did not affect the top schools or bottom performing schools

Does budget affect top schools?

Here is the list of deliverables for the analysis of the school district: 

A high-level snapshot of the district's key metrics, presented in a table format
An overview of the key metrics for each school, presented in a table format
Tables presenting each of the following metrics:
Top 5 and bottom 5 performing schools, based on the overall passing rate
The average math score received by students in each grade level at each school
The average reading score received by students in each grade level at each school
School performance based on the budget per student
School performance based on the school size 
School performance based on the type of school
Before we can begin these tasks, we need to import the datasets into Jupyter Notebook using Python.





The school district summary will be a high-level snapshot of the district's key metrics:

Total number of students
Total number of schools
Total budget
Average math score
Average reading score
Percentage of students who passed math
Percentage of students who passed reading
Overall passing percentage
