
# VBA Stock Market Analysis

Performing data analysis on stocks data using Excel and Visual Basic for Applications (VBA).

## Background

The client/stakeholders were interested in performing an analysis of thousands of stocks over multiple years using Excel and VBA.

## Overview of Project

This analysis aims to provide the “total daily volume” and “yearly return”  for twelve stocks of interest for a given year as shown in Fig 1.1

![green_data_analysis_example.jpg](Images/green_data_analysis_example.jpg)<br />
<sub>Figure 1.1 example of summary table

### Purpose

The purpose of this project had two objectives: (1) To provide an initial analysis of thousands of stocks to find the “total daily volume” and “yearly return” for each stock over a given year. (2) To edit or refactor our initial analysis to loop through all the data one time to collect the same information. Then, we will compare the outcome against the initial analysis to determine whether refactoring the code successfully made the VBA script run faster.

### Analysis of Outcomes

Aligned with the purpose of the project, we created a code in VBA and then refactored it. The initial code (asynchronous) iterates over the entire year's worth of stock data once for each “stock of interest”. This required twelve separate iterations over the entire year's data. The results for each of the two years analyzed is shown below in Fig 1.2 and Fig 1.3

![AllStockAnalysis_2017__with_data.png](Images/AllStockAnalysis_2017__with_data.png)<br />
<sub> Figure 1.2 Initial AllStockAnalysis_2017<br />
<p>&nbsp;</p>

![AllStockAnalysis_2018__with_data.png](Images/AllStockAnalysis_2018__with_data.png)<br />
<sub>Figure 1.3 Initial_AllStockAnalysis_2018<br />
 

The refactored (synchronous) code iterated over all data for a given year only once while still capturing all necessary values needed to update the summary table as shown below in Fig 1.4 and 1.5

![VBA_Challenge_2017_with_data.png](Images/VBA_Challenge_2017_with_data.png)<br />
<sub>Figure 1.4 VBA_Challenge_2017_Refactored<br />
<p>&nbsp;</p>

![VBA_Challenge_2018__with_data.png](Images/VBA_Challenge_2018__with_data.png)<br />
<sub>Figure 1.5 VBA_Challenge_2018_Refactored<br />

If we compare the output values in the summary tables for the original code (AllStockAnalysis) and the refactored code (VBA_Challenge), we can see that both outcomes are the same as shown in Fig 1.2 to 1.5. This means that our refactored code preserved the same functionalities as our original code, but with improved runtimes.


## Results

### Outcomes of Original Code Analysis (AllStockAnalysis)

- Runtime for year 2017 was **1.121094**

![AllStockAnalysis_2017.png](Resources/AllStockAnalysis_2017.png)

- Runtime for year 2018 was **1.132813**

![AllStockAnalysis_2018.png](Resources/AllStockAnalysis_2018.png)

### Outcomes of Refactored Code Analysis (VBA_Challenge)

- Runtime for year 2017 was **0.1328125**

![VBA_Challenge_2017.png](Resources/VBA_Challenge_2017.png)

- Runtime for year 2018 was **0.1367188**

![VBA_Challenge_2018.png](Resources/VBA_Challenge_2018.png)

### Overall decrease in runtime and decrease in percentage using 2017 data

Overall decrease = original time (asynchronous time) - new time (synchronous time)<br />

Overall decrease = 1.121094 - 0.1328125<br />

Overall decrease = **0.9882815**

Percentage runtime reduction = (overall decrease / original time) *100<br />

Percentage runtime reduction = (0.9882815 / 1.121094)* 100 = **88.15%**

### Overall decrease in runtime and decrease in percentage using 2018 data

Overall decrease = original time (asynchronous time) - new time (synchronous time<br />

Overall decrease = 1.132813 -  0.1367188<br />

Overall decrease = **0.9960942**


Percentage runtime reduction = (overall decrease / original time) *100<br />

Percentage runtime reduction = (0.9960942 / 1.132813)* 100 = **87.93%**

## Summary
 
### Pros and Cons:
#### In general:
 
- In general, the advantages of refactoring a code include a reduced runtime which saved time while maintaining all the same functionalities of the original code. 
- It also reduces complexity and redundancies and increases maintainability of the code.
- However, changes are not always self-evident to the customers. Since functionality is preserved, it's harder for them to recognize the improvements.
- Additionally, anytime code is refactored there is a potential of introducing new bugs and errors to an already working code.
- Sometimes when large teams are working on refactoring the same code, coordination can represent a challenge since it requires greater communication within the team.
 
 
#### Specific for the refactored VBA code

- By refactoring the already working VBA code, we achieved an **88%** decrease in runtime while preserving the functionality and obtaining identical summary results as shown in tables Fig 1.2 to 1.5.
- We improved the legibility and comprehensibility of the code, now it is easier to read without the additional nested ”for loop” and macros.
- On the downside, we had to account for the time added to refactor the code.
 
 [Markdown Reference 1](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)<br />
 [Markdown Reference 2](https://www.markdownguide.org/basic-syntax/)<br />
 [pros and cons of refactoring code](https://www.ionos.com/digitalguide/websites/web-development/what-is-refactoring/)<br />
