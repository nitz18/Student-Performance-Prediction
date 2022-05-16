# Student Performance Dataset


### Summary 

The problem addressed is to predict students’ academic performance in secondary schools (and to then use the results to intervene and help at-risk students do better). The data is from students in secondary education of two Portuguese schools. The data attributes include student grades, demographic, social and school related features, and was collected by using school reports and questionnaires. The dataset provided for this project measures the students’ performance in the subject of Portuguese language (por).
Problem type: Classification (5-class)* or Regression.
For individual projects, choose either regression or classification to work on. For team projects, do both regression and classification.

### Data Description

The full dataset is posted on the UCI website (includes mathematics and Portuguese topics). For this project we will use the only the Portuguese dataset. The number of input attributes per data point is 30, not counting the grade features (Gx). 13 of the attributes are integer valued, 13 are binary-valued categorical, and 4 are multi-valued categorical. There are no missing values. In detail:

1. school - student's school (binary: 'GP' - Gabriel Pereira or 'MS' - Mousinho da Silveira)
2. sex - student's sex (binary: 'F' - female or 'M' - male)
3. age - student's age (numeric: from 15 to 22)
4. address - student's home address type (binary: 'U' - urban or 'R' - rural)
5. famsize - family size (binary: 'LE3' - less or equal to 3 or 'GT3' - greater than 3)
6. Pstatus - parent's cohabitation status (binary: 'T' - living together or 'A' - apart)
7. Medu - mother's education (numeric: 0 - none, 1 - primary education (4th grade), 2 - 5th
to 9th grade, 3 secondary education or 4 higher education)
8. Fedu - father's education (numeric: 0 - none, 1 - primary education (4th grade), 2 -5th to 9th grade, 3 - secondary education or 4 - higher education)
9. Mjob - mother's job (nominal: 'teacher', 'health' care related, civil 'services' (e.g. administrative or police), 'at_home' or 'other')
10. Fjob - father's job (nominal: 'teacher', 'health' care related, civil 'services' (e.g. administrative or police), 'at_home' or 'other')
11. reason - reason to choose this school (nominal: close to 'home', school 'reputation', 'course' preference or 'other')
12. guardian - student's guardian (nominal: 'mother', 'father' or 'other')
13. traveltime - home to school travel time (numeric: 1 - <15 min., 2 - 15 to 30 min., 3 - 30
min. to 1 hour, or 4 - >1 hour)
14. studytime - weekly study time (numeric: 1 - <2 hours, 2 - 2 to 5 hours, 3 - 5 to 10 hours,
or 4 - >10 hours)
15. failures - number of past class failures (numeric: n if 1<=n<3, else 4)
16. schoolsup - extra educational support (binary: yes or no)
p. 9 of 15
17. famsup - family educational support (binary: yes or no)
18. paid - extra paid classes within the course subject (Math or Portuguese) (binary: yes or
no)
19. activities - extra-curricular activities (binary: yes or no)
20. nursery - attended nursery school (binary: yes or no)
21. higher - wants to take higher education (binary: yes or no)
22. internet - Internet access at home (binary: yes or no)
23. romantic - with a romantic relationship (binary: yes or no)
24. famrel - quality of family relationships (numeric: from 1 - very bad to 5 - excellent)
25. freetime - free time after school (numeric: from 1 - very low to 5 - very high)
26. goout - going out with friends (numeric: from 1 - very low to 5 - very high)
27. Dalc - workday alcohol consumption (numeric: from 1 - very low to 5 - very high)
28. Walc - weekend alcohol consumption (numeric: from 1 - very low to 5 - very high)
29. health - current health status (numeric: from 1 - very bad to 5 - very good)
30. absences - number of school absences (numeric: from 0 to 93)
The following grades are related with the course subject; some you will use as features, and some as output targets, as described below:
31. G1 - first period grade (numeric: from 0 to 20)
32. G2 - second period grade (numeric: from 0 to 20)
33. G3 - final grade (numeric: from 0 to 20, output target)

For the classification problem, convert the output variable from 𝑦 ∈ [0,20] into a 5-class categorical value (I, II, III, IV, V) based on the rules below:
For example, if your mission is to predict G3, you need to replace the original G3 column with a new G3 column based on the above mapping, and use the new G3 as your output value. If you are using G1 as a feature, then leave G1 in numeric form.
Required training and test sets
2 datasets are provided and required: one training set (for you to use as you like for training, validation, cross-validation, etc.); one test set to use on your final model, to estimate its performance on unknowns.

###Your Missions

You have 3 missions (3 ML problems to solve). This applies to both the regression and the classification problem:
1. Predict first-period academic performance without any prior academic performance data: remove the G2 and G3 columns from the original dataset, then predict G1.
 p. 10 of 15
2. Predict final-period academic performance without any prior academic performance data: remove the G1 and G2 columns from the original dataset, then predict G3.
3. Predict final academic performance using all available prior academic performance data: Keep G1 and G2 columns inside the dataset as features, then predict G3.
