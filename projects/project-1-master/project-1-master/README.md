# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

### Problem Statement

Problem Statement
As an SAT prep program we are always trying to increase our students SAT scores. What factors impact student's overall SAT score. Do states where more people take the test do better on the exam? Do some prospectve majors do better than others? By learning the answer to these questions we hope to better able to help our students succeed.

### Background 

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

### Datasets
* [`act_2019.csv`](./data/act_2019.csv): 2019 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State ([source](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent))
* [`sat_2019_by_intended_college_major.csv`](./data/sat_2019_by_intended_college_major.csv): 2019 SAT Scores by Intended College Major ([source](https://reports.collegeboard.org/pdf/2019-total-group-sat-suite-assessments-annual-report.pdf))

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*object*|2019 test|lists the state| 
|**sat_participation**|*float*|2019 test|percent of student in state that took the SAT (expressed as a decimal)|
|**reading_writing**|*integer*|2019 test|average SAT reading/writing score by state (range 200-800)|
|**math**|*integer*|2019 test|average SAT math score by state (range 200-800)|
|**sat_score**|*integer*|2019 test|average state score SAT (range 400-1600)| 
|**act_participation**|*float*|2019 test|percent of student in state that took the ACT (expressed as a decimal)|
|**act_score**|*integer*|2019 test|average score ACT (1-36)| 
|**major**|*object*|2019 major|prospective major of students taking SAT|
|**test_takers**|*object*|2019 major|number of test takers for each prospective major| 
|**percent**|*object*|2019 major|percent of all SAT test takers who picked that major|
|**sat_score**|*integer*|2019 major|average SAT score by major (range 400-1600).| 
|**reading_writing**|*integer*|2019 major|average SAT reading/writing score by major (range 200-800)|
|**math**|*integer*|2019 major|average SAT math score by major (range 200-800)| 

### Conclusions and Recommendations 

When picking which exam to take, students should not worry about participation rate in their state. The higher the participation rate the worse the scores for that state. The states with higher participation rates sometimes have all students take the test not just the ones who want to go to college.

Further research should be done on the states that have above average scores and high participation to see what they are doing for test prep. Perhaps some of that can be applied to our prep program.

Some prospective majors do better than others. We may need to work more with students with some prospective majors to help them improve their score.

Students who intend to study STEM majors tend to do better. Is there something about how they study we can replicate with our other students?

Students with intended majors in STEM tend to do better on the math component than the reading and writing component. Students with intended majors in humanities tend to do better on the reading and writing component then the math component. Perhaps we sould provide targeted training programs depending on intended majors. Humanities students get more math prep and stem students get more reading and writing prep.

Further research should be done on other factors that are impacting SAT scores. Factors like poverty, deomgraphics, school district, gpas, and ap tests might have an impact that would cause us to come up with new recommendations.




