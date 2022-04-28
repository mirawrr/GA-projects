
# Project 1: Analysis of SAT & ACT Tests


This project is an analysis of the participation rates and aggregated scores in SAT and ACT test across the United States, across the years 2019 to 2021.




## Problem Statement


The COVID-19 pandemic had reportedly reduced the overall participation rates in SAT & ACT tests in the United States, as many test sessions had to be cancelled due to school/test centre closures or reduced testing capacity. [(Sources: College Board](https://newsroom.collegeboard.org/sat-program-results-capture-impact-of-covid-on-class-of-2021)[ & Forbes)](https://www.forbes.com/sites/michaeltnietzel/2021/10/13/the-number-of-students-taking-the-act-dropped-22-this-year/?sh=5a60caf7c60a) 

Though standardized tests remain a controversial topic for students, administrators and legislators, a number of colleges still rely on those tests in assessing students' application into their programmes. During the pandemic period, several schools temporarily waived SAT/ACT requirement for college entrance applications as the pandemic had disrupted testing for many applicants. 

In 2022, as COVID-19 is becoming endemic and school and testing centers have resumed operations, some schools such as MIT have also reinstated the SAT/ACT requirement. [(Source: NYTimes)](https://www.nytimes.com/2022/03/28/education/mit-sat-act-scores-admission.html) 


As an employee of a consulting firm that specialises in the education sector, my team has been tasked to analyse trends in SAT and ACT participation rates and aggregated scores for each state in the US from 2019 to 2021. Based on the findings, we will provide recommendations to the College Board and ACT Inc. on their resource prioritisation strategy to improve participation rates in future SAT/ACT tests especially for states that were most adversely affected due to the pandemic. 
    

## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|*string*|SAT/ACT|This is a region in the USA| 
|year|*int*|SAT/ACT|Year of test taken| 
|participation_sat|*int*|SAT|Percentage of students who sat for the SAT test| 
|ebrw_sat|*int*|SAT|Average score for SAT Evidence-Based Reading and Writing section| 
|math_sat|*int*|SAT|Average score for SAT Math section| 
|total_sat|*int*|SAT|Average SAT total score| 
|participation_act|*int*|ACT|Percentage of students who sat for the ACT test| 
|composite_act|*int*|ACT|Average ACT composite score| 

## Summary of Analysis

The COVID-19 pandemic generally had a negative impact on the participation rates and aggregrated scores in SAT and ACT tests, across states in the US. The mean/median of SAT/ACT participation rates and aggregated scores certainly decreased across board over the period from 2019 to 2021. 

**ACT & SAT participation during the pandemic**

When the pandemic was at its peak in 2020 and 2021, all states tightened restrictions to curb the spread of the virus. This led to many SAT/ACT testing centres to be closed or reduce their testing capacity and therefore affected the participation rates within each state. However, some states were in fact, worst off than others. Key findings as follows: 

*ACT*    
* There are 5 states that maintained 100% participation rate in ACT from 2019 to 2021 However, none of the states demonstrated year-on-year improvement in participation rates from 2019 to 2021.    
* There are 6 states that had above average participation rate in ACT in 2019, but experienced significant decline in participation rate from 2019 to 2021.
  
*SAT*
* None of the states maintained 100% participation rate in SAT from 2019 to 2021. Interestingly, one state i.e. New Mexico saw year-on-year improvement in participation rates from 2019 to 2021. 
* There are 5 states that had above average participation rate in SAT in 2019, but experienced significant decline in participation rate from 2019 to 2021.    

**ACT & SAT aggregated scores during the pandemic**

There is strong negative correlation between participation rates and aggregated scores for ACT and SAT. Therefore, it is expected that as participation rates dropped during the pandemic, aggregrated scores would generally increase. However, the experience certainly varied across states.  

*ACT Composite Score*
* None of the states maintained the same ACT composite score from 2019 to 2021. Likewise, none of the states experienced a year-on-year improvement in ACT composite score from 2019 to 2021. 
* 13 states experienced year-on-year decline in ACT composite scores from 2019 to 2021. 
* There are 5 states that had above average ACT composite score in 2019, but experienced a decline in composite score from 2019 to 2021. However, the percentage difference is small - between 0.4% to 0.8%. 
    
*SAT Total Score*
* None of the states maintained the same SAT total score from 2019 to 2021. Interestingly, 5 states experienced a year-on-year improvement in SAT total scores from 2019 to 2021.
* 9 states experienced year-on-year decline in SAT total scores from 2019 to 2021. 
* There are 5 states that had above average SAT total score in 2019, but experienced significant decline in composite score from 2019 to 2021. The percentage difference is between 1% to 8%.
   

## Conclusions & Recommendations

In 2022, more colleges are likely to reinstate the SAT/ACT requirement for enrollment applications and more testing centres will resume operations. In preparation for this, the College Board and ACT Inc. will need to re-allocate their resources for support more testing operations.  

In order to improve future participation rates in SAT and ACT, the College Board and ACT Inc. should consider allocating more resources to states that meet two criteria:

    1. Above average participation rate in pre-pandemic period i.e. 2019, and
    2. Greatest decline in participation rate from 2019 to 2021. 




**ACT Inc. should focus on the following states:**

ACT | State |Participation Rate (2019) |% Difference in participation rate (2019 to 2021) |
--- | --- | --- | --- |
1 | New Mexico |0.63|-0.63|
2 | Arizona |0.73|-0.52|
3 | Oklahoma |1.00|-0.42|
4 | Minnesota |0.95|-0.36|
5 | South Carolina|0.78|-0.35|

**College Board should focus on the following states:**

SAT | State |Participation Rate (2019)|% Difference in participation rate (2019 to 2021) |
--- | --- | --- | --- |
1 | Maine |0.99|-0.70|
2 | Oregon |0.51|-0.66|
3 | California |0.63|-0.61|
4 | Washington |0.70|-0.61|
5 | Massachusetts |0.81|-0.58|

This would allow these states to bounce back to their pre-pandemic levels faster, and will likely increase the overall participation rates in the respective tests. 