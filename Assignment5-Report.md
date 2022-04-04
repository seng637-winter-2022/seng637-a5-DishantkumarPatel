****SENG 637 - Dependability and Reliability of Software Systems****

**Lab. Report \#5 – Software Reliability Assessment**

| Group \#: 08       |   |
|-----------------   |---|
| Student Names:     |   |
|Srujan Patel        |   |
|Jairath Chopra      |   |
|Mit Patel           |   |
|Dishantkumar Patel  |   |
# Introduction

# 

# Assessment Using Reliability Growth Testing 

Firstly, we imported the given data failure-data-a5 to C-SFRAT tool. Next, to conduct  Growth Testing we plotted all the models on all the covariates (e,f,c) to get an overall view before further analysis. 

We made a selection of all the hazard functions available in C-SFRAT namely:

-IFR Salvia & Bollinger
-IFR Generalized Salvia & Bollinger
-S Distribution
-Discrete Weibull (Order 2)
-Discrete Weibull (Type III)
-Geometric
-Negative Binomial (order 2)
-Truncated Logistic

The resulting plot is shown below:
![plot on all the covariates](media\img1.png)

The intensity plot shown below for the same data can be inferred using Ctrl+I shortcut.
![plot on all the covariates](media\img2.png)

The model comparision based on their best fit using the model comaprison tool in C-SFRAT with equal metric weights of 1.0 eac for LLF,AIC,BIC,SSE is displayed below:
![plot on all the covariates](media\img3.png)

From the table it can be inferred that the top two models are the discrete weibull type 3 on covariate F having a 1.0 critic for mean and median and the IFRGSB on covariate F having 0.998 critic for mean and median. A comparision of these two models is shown below:
![Comparision of models](media\img4.png)


Intensity Plot
![Intensity Plot](media\img5.png)

The graph shown below shows that it is a relatively declining or plateauing curve for the IFRGSB on covariate F. This indicates failure in reliability growth, since the amounts of failures starts to happen more and more as time increases. Therefore, the system does not exhibit reliability growth, as the failures over time intervals is predicted by C-SFRAT to be plateauing.

The graph for the DW3 model on covariate F indicates that there is steady realibikity growth, since the amounts of failures starts to happen less and less as time increases, measured for the next 69 intervals.
![comparision of top two](media\img6.png)


From the failure intensity graph of both the models it can be inferred that the that the failure intensity is quite large and does not show promise in hitting the 1.0 target (default value in the tool). We adjusted the target failure intensity to 0.5 as such: 
![comparision of top two](media\img6.png)

As a result, C-SFRAT implies that both models are likely to meet the new failure intensity rate target of 0.5. At an interval of 52, the DW3 model will reach the target failure intensity rate, while the IFRGSB will be around 34. As a result, a target failure intensity rate range of 0.6 or below is appropriate, whereas anything approaching 1.0 or higher is excessive.
# Assessment Using Reliability Demonstration Chart 

# 

# Comparison of Results

# Discussion on Similarity and Differences of the Two Techniques

Through reliability growth analysis the trend of the system's relability can be determined and whether or not this is an acceptable goal given the failure data. RDC analysis is very versatile, time and cost efficient way of analyzing the reliability of a system. A disadvantage of the RDC is that it cannot be used to calculate the exact quantitative value for the reliability (or availability) of the system under study RDC can only indicate that the SUT is acceptable or not.
# How the team work/effort was divided and managed
The team work was divided into two pairs. Srujan and Jairath did the part one, while Dishantkumar and Mit did part two. Everyone contributed in making the report.
# 

# Difficulties encountered, challenges overcome, and lessons learned

# Comments/feedback on the lab itself
This lab examines program reliability testing using failure data and a variety of testing techniques. We looked at reliability growth testing and reliability assessment with a reliability demonstration chart in particular. This lab also allowed us to compare multiple reliability evaluations to examine the benefits and drawbacks of each and improve our future tool usage decisions.