# School_District_Analysis

## Overview

The purpose of this analysis is to clean the [student data](/Resources/students_complete.csv) by removing Thomas High School 9th grade grades, then merge it with [school data](/Resources/schools_complete.csv) to produce a completed set of school & student data. Then summaries and analyses are performed for the following breakdowns: 
* an overall breakdown of the district
* a summary by school (presented as both inclusive and exclusive of Thomas High 9th graders)
* High and Low performing schools
* Math and Reading scores by grades per school
* Math and Reading scores by school spending
* Math and Reading scores by school size
* Math and reading scores by school type (charter or district)

## Results

#### How is the district summary affected?
The district summary is minimally affected but does decrease the passing percentages by a very minute amount.

District with Thomas High School's 9th graders:

![District_w_THSGr9](/Resources/District_w_THSGr9.PNG)

District without Thomas High School's 9th graders:

![District_wo_THSGr9](/Resources/District_wo_THSGr9.PNG)

#### How is the school summary affected?

The school summary is only affected in the data row for Thomas High School. Other school data remains the same. 

#### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

Replacing the ninth graders' reading and math scores by `numpy.nan` causes Thomas High School's % passing math, % passing reading and % overall passing to all drop by a significant margin.

Non-replaced
![NonReplacedSchoolSummary](/Resources/NonReplacedSchoolSummary.PNG)

Replaced
![ReplacedSchoolSummary](/Resources/ReplacedSchoolSummary.PNG)

#### How does replacing the ninth-grade scores affect the following:

##### Scores by Grade

Replacing the ninth-grade scores affects the scores by grade in that the data frame will show `NaN` for Thomas High School.

![NaNTHSGr9](/Resources/NaNTHSGr9.PNG)

##### Scores by school spending

Scores by school spending is minisculy reflected by the manual update, however the remainder of the data (ie: `per_school_capita`) remains the same

Per Capita Kept
![PerCapitaKept](/Resources/PerCapitaKept.PNG)

Per Capita Removed
![PerCapitaRemoved](/Resources/PerCapitaRemoved.PNG)

#### Scores by school size & type

Similar to scores by school spending, the total students does not change since the 9th graders are not removed in their existence but the passing math, reading and overall pass is also updated with the manual update but the difference is not visible when applying a 0 decimal places format and still remains in the medium school size bin. Further more, Thomas High School is still a Charter high school and it's changes are small enough to similarly be invisible when applying the 0 decimal places formatting. 



## Summary

Overall, changes to the data was minute but most reflective in the stages where nineth grader `NaN` data was used. Once exclusions were applied, the changes were miniscule but when applied to zero decimal places, were not visible.
