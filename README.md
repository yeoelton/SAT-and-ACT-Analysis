# SAT and ACT Analysis

by: Elton Yeo

### Context and Problem Statement

Currently, colleges in the U.S. consider scores from a range of assessments, among other criteria, to determine whether a student may be admitted. SAT, administered by College Board, and ACT, administered by ACT Inc, are two of the most popular national college admission tests. Policies range accross states - some mandate SAT, some mandate ACT, while others mandate neither and have their own internal assessments instead. 

SAT participation rates across the years have improved, but there is room for further improvement. The problem statement is how to improve SAT participation rates, especially in states which already have their own internal assessments, such as Iowa. 

---

### Executive Summary

In this analysis, we consider each state's participation rates for both the SAT and ACT in 2017 and 2018, and their total/composite scores, broken down by each subtest. In general, we observe that each of these variables are not normally distributed. This means that any estimations made from the current datasets would not be useful in providing generalisable recommendations. 

Notwithstanding, an in-depth look at the various participation rates and total/composite scores for the tests showed that there are many factors which could affect participation rates. For example, the mandating of either tests (as in the case of Colorado, which changed their policy in 2017, driving their rates up to 100% in 2018), the availability and costs of the test, the presence of other internal assessments, all contribute to the participation rates. 

In addition, if there is already one mandated test in a state, this typically means that participation rates for the other test would be low. Also, lower participation rates typically mean a high total/composite score 
when compared with other states. This suggests that the most motivated/able students are self-selecting to take their respective additional test, which leads to the relatively higher total/composite scores. 

---
### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**participation**|*float*|ACT/SAT 2017/18|The number of college students who take SAT or ACT at least once in any year out of the whole high school graduating class population | 
|**composite**|*float*|ACT 2017/18|The weighted average score of ACT from English, Math, Reading and Science components| 
|**total**|*integer*|SAT 2017/18|The combined total score of SAT from Evidence Based Reading and Writing and Math components|
|**math**|*SAT-integer ACT-float*|ACT/SAT 2017/18|The Math ACT/SAT score in a respective year| 
|**reading**|*float*|ACT 2017/18|The Reading ACT score in a respective year| 
|**english**|*float*|ACT 2017/18|The English ACT score in a respective year| 
|**science**|*float*|ACT 2017/18|The Science ACT score in a respective year|
|**evidence-based reading and writing**|*integer*|SAT 2017/18|The Evidence Based Reading and Writing score in a respective year|

---

### Interpretations of Results

A visual assessment of histograms and boxplots of each variable showed that they are bimodal distributions. Running the Shapiro-Wilk test on each variable also showed that except for ACT 2017 reading scores, ACT 2017 science scores, and ACT 2018 science scores, which have p values above 0.05, all other variables do not have normal distributions. 

If the distribution is not normal, then it cannot be used to draw inferences regarding the entire population. Any statistical calculations to derive confidence intervals require the underlying distribution to be a normal distribution. Without a normal distribution, we are unable to draw a valid conclusion by hypothesis testing.

Comparing SAT and ACT participation rates within 2017 and 2018 via scatterplots (see below) also confirmed the negative correlation between SAT and ACT i.e. within a state, when the SAT participation rate is high, the ACT participation rate tends to be low, and vice versa. 

---

### Business Recommendations

There could be many reasons which could affect a state's participation rate such as the state's education policies (whether they mandate SAT or ACT, at which grade or on which days that students can take SAT or ACT, how much students have to pay to take the exams etc.) and resources (how much states are investing in education, what are the expectations and educational pathways envisioned for each student, how the school system is structured etc).

In the case of Iowa, Iowa had low SAT participation rates of 2% and 3% respectively for 2017 and 2018. We also know that high schoolers in Iowa take the Iowa Statewide Assessment of Student Progress (ISASP), which was recently revised in 2018. However, reports showed that even after the implementation of the revised ISASP, "a quarter of students are not at proficient levels in math, language arts, and science compared to their peers." (source: kcrg.org) This suggests that there is room to introduce a new college admission test of higher quality i.e. the SAT, which might contribute to better abilties among students and higher levels of college readiness. 

We have two recommendations for College Board:

- Increase convenience: College board may wish to engage policy-makers in Iowa to consider offering SATs on school days and at no or subsidised cost to students.

- Quantify value of SAT: College board must show the Iowa Education Board that the SAT is superior to ISASP, be it in syllabi, college entry rates, levels of accceptance etc. 
    - College board could gather data on the number of colleges across the US which currently refer to SAT, and gather information on how widely received and used it is, to show Iowa the value proposition of switching to the SAT. 
    - College board could gather data on other states which currently mandate the SATs to consider college entry rates, or relative abiity of students who study and take the SAT, to display college readiness.

Source: https://www.kcrg.com/content/news/New-student-assessments-deemed-a-success-but-numbers-show-some-students-falling-behind-560947261.html