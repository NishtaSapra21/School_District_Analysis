# School District Analysis

## __Overview__

This analysis replaces math and reading scores of all ninth graders with “NaN” of Thomas High School due the evidence of alteration of academic dishonesty and recalculates all scores for school  and district summary DataFrames as well as reports of scores per school spending, per school size, per school type, top and bottom schools of district and average math and reading scores for each grade level from each school.

## __Results__

* __Impact on District Summary__

   After replacing ninth grade scores of  “Thomas High School “ with “NaN”; the district summary doesn’t affect in terms of no. of schools, no. of students and budget    but Average Math Score changed from **__79.0 to 78.9__**, Average Reading Score remained almost same, Percentage Math Score changed from **__75% to 74.8% __**, Percentage Reading Score changed from **__86% to 85.7%__**and Overall Percentage changed from **__65% to 64.9%__**.  These are not significant changes.     

* __Impact on School Summary__

   School summary remains same for all schools except “Thomas High School” as math and reading scores of their ninth graders are  replaced with “Nan”; so Pandas          ignored that data in counting and we have a new summary for “Thomas High School”.

   | Thoams High School| Type|Total Students|Total School Budget|Per Student Budget|Average Math Score|Average Reading Score|% Passing Math|% Passing Reading|% Overall Passing|
   |--|--------|-----|--------------|--------|----------|-----------|-----------|-----------|-----------|
   |Before NaN|	Charter|	1635|	$1,043,130.00|	$638.00|	83.418349|	83.848930|	93.272171|	97.308869|	90.948012|
   |After NaN|	Charter|	1635|	$1,043,130.00|	$638.00|83.350937|	83.896082|	66.911315|	69.663609|	65.076453| 
   |After new student count|	Charter|	1635|	$1,043,130.00|	$638.00|83.350937|	83.896082|	93.185690|	97.018739|	90.630324|
  
   Also, after replacing student count of “Thomas High School” with new student count which contains only 10th,11th and 12th graders, there is difference in         school summary DataFrame for “Thomas High School”.
   
* __Impact on Thomas High School Performance__

   Let’s consider the case of overall performance of Thomas High School students including ninth graders with “Nan” scores; refering above table we can see that it          decreased significantly; but when we recalculated all scores with new student count (10th, 11th and 12th graders only) , there is not much performance difference.    In fact, Thomas High School remains at two of top five schools of district in both the analysis. 

* __Impact after Replacing Ninth-Grader Scores__

    * __Math and reading scores by grade__ 
    
       Thomas High School’s math and reading grade scores replaced with ‘nan’  in scores by grade DataFrames.
    
    * __Scores by school spending__
    
       Thomas High School is in the spending range of $631 to $645. Considering following table it is seen that scores by __school spending__ are not affected much.
      
      |Thomas High School|Range|Average Math Score|Average Reading Score|% Math Score| % Reading Score| % Overall Score|
      |------------------|-----|------------------|---------------------|------------|----------------|----------------|
      |School Spending Before NaN|$631-645|	78.518855|	81.624473|	73.484209|	84.391793|	62.857656|
      |School Spending After NaN|$631-645|	78.502002|	81.636261|	73.462589|	84.319261|	62.778233|
    
    * __Scores by school size__
    
      Thomas High School falls in the size range 1000 -2000 students. i.e., “Medium” size range. Considering following table it is seen that scores by __school size__ are not affected much.
      
      |Thomas High School|Size|Average Math Score|Average Reading Score|% Math Score| % Reading Score| % Overall Score|
      |------------------|-----|------------------|---------------------|------------|----------------|----------------|
      |School Size Before NaN|Medium (1000-1999)|	83.374684|	83.864438|	93.599695|	96.790680|	90.621535|
      |School Size After NaN|Medium (1000-1999)|	83.361201|	83.873869|	93.582398|	96.732654|	90.557997|
     
      The total students of Thomas High School were 1635 including ninth graders ; after remving  461 ninth graders , new student count is 1174 that includes only 10th ,  11th and 12th  graders. 
    
    * __Scores by school type__
    
      Considering following table, Thomas High School is of “Charter” type and  scores by __school type__ are not affected much. It is almost same. 

      |Thomas High School|Type|Average Math Score|Average Reading Score|% Math Score| % Reading Score| % Overall Score|
      |------------------|-----|------------------|---------------------|------------|----------------|----------------|
      |Scores Before NaN |Charter|	83.473852|	83.896421|	93.620830|	96.586489|	90.432244|
      |Scores After NaN| Charter|	83.465425|	83.902315|	93.610020|	96.550223|	90.392533|


## __Summary__

Four changes after reading and math scores for the ninth grade at Thomas High School has been replaced with “NaNs”:

1. Average math and reading scores, percentage of math and reading scores and overall percentage have been changed for Thomas High School in School Summary.
2. Statistics shows that after removing ninth graders from calculating scores all  reports have been changed but by very small number, difference is ignorable. 
3. “Total Budget” and “Per Student Budget” for Thomas High School not affected. 
4. District Summary not affected much. 
