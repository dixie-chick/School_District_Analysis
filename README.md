# School_District_Analysis
pandas environment analysis

## Purpose
In this analysis, the pandas library in jupyter notebook was used to address seven schools within a district to capture key metrics including the top 5 performing schools and 5 worst performing schools, average math and reading scores, school budgets, and how school size, type and budget affect overall school performance. DataFrames for each output were created for easy visualization. After running this analysis, the school board notified that the completed csv file shows evidence of academic dishonesty, specifically the ninth grade scores for Thomas High School (THS). In order to uphold state-testing standards, the school district analysis was ran again, replacing the math and reading scores for Thomas High to understand how this change affected the overall analysis.

## Process & Data
After running the analysis, we can see how each of the seven school district metrics was affected by the changes in the data:

- **School summary:** In the first analysis, merge() was used to generate a single school data summary based on school name for student_data and school_data
To solve for the 9th Grade THS scores, np.nan was used to remove their math and reading from the district summary DataFrame:

![school_district_1](https://user-images.githubusercontent.com/79612565/114319759-b58cb900-9ac7-11eb-945b-ffb97c4673b4.png)

![school_district_2](https://user-images.githubusercontent.com/79612565/114319768-bcb3c700-9ac7-11eb-86e5-4e52af70bc2f.png)


- **District summary:** In the first analysis, a snapshot across all schools in the district was created after calculating passing_math, passing_reading and overall_passing count and percentages:
 ![district_summary_1](https://user-images.githubusercontent.com/79612565/114319771-c1787b00-9ac7-11eb-8d75-1e30fde1a7ba.png)

 
 After taking THS 9th grade out of the school summary, we can see the the average scores and percentages increase marginally for the distrcit:
![district_summary_2](https://user-images.githubusercontent.com/79612565/114319778-c5a49880-9ac7-11eb-865d-f4e117072a9b.png)

Did Removing the THS scores affect top performing schools and worse performing schools? As seen below, not really:
![top_perform_1](https://user-images.githubusercontent.com/79612565/114320079-1c5ea200-9ac9-11eb-93f6-4c826941b704.png)
![top_perform_2](https://user-images.githubusercontent.com/79612565/114320081-1e286580-9ac9-11eb-9fe8-047cc1eadbb3.png)


## Challenges
- **Determining data types:** all of the columns needed for calucaltions are intergers so any data which contained numbers as strings rather than intergers must be converted using float
- **Missing Data**: with such large amounts of data, it's important to address anything missing
- **Cleaning Data:** in this anlysis, pre-fixes and suffixes skewed school records and must be removed from student_name. These names cannot be dropped sicne it would affect total student count, negatively impacting the analysis

## Does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
To wrap it up, replacing THS 9th grade scores marginally affected the overall district analysis since there is so much data across. Therefore, the school board may still use this analysis to understand test scores, budgeting and overall performance. 

A few changes which are easily apparent are:

1. Math and reading scores by grade replaced with NaN
**Math**
![math_grades](https://user-images.githubusercontent.com/79612565/114320562-3a2d0680-9acb-11eb-897a-ee7033ed8b60.png)

**Reading**
![reading](https://user-images.githubusercontent.com/79612565/114320564-3c8f6080-9acb-11eb-8c95-64e297e25807.png)

2. Scores by school spending: insignificant effect for THS spending bin $630-$644
![spending](https://user-images.githubusercontent.com/79612565/114321042-ae68a980-9acd-11eb-90aa-d985cb09d570.png)

3. Scores by school size: Little effect on school size replacing THS 9th grade
![size](https://user-images.githubusercontent.com/79612565/114321022-a1e45100-9acd-11eb-9465-45c07259c5ce.png)

4. Scores by school type: The Charter schools still rank as the top performing schools

![type](https://user-images.githubusercontent.com/79612565/114321015-9abd4300-9acd-11eb-9667-a9310947ac8b.png)

