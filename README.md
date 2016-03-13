# Udacity Data Analyst Nanodegree Statistics Project
**Arif Hikmet Onat Balta**

## Introduction

In this project, I tested a perceptual phenomenon "Stroop Effect" using statistical methods. 
I used Minitab statistical software during my analysis.

In a Stroop task, participants are presented with a list of words, with each word displayed in a color of ink. 
The participant’s task is to say out loud the color of the ink in which the word is printed. 
The task has two conditions: a congruent words condition, and an incongruent words condition. 
In the congruent words condition, the words being displayed are color words whose names match the colors 
in which they are printed. 
In the incongruent words condition, the words displayed are color words whose names do not match the colors 
in which they are printed. 
In each case, we measure the time it takes to name the ink colors in equally-sized lists. 
Each participant will go through and record a time from each condition.

For an interactive Stroop Effect experiment, click [here](https://faculty.washington.edu/chudler/java/ready.html)

Data set used in this project can be downloaded [here](https://drive.google.com/file/d/0B9Yf01UaIbUgQXpYb2NhZ29yX1U/view)

## Questions For Investigation

**1. What is our independent variable? What is our dependent variable?**

Our independent variable is word condition, which can be either congruent or incongruent 
and the dependent variable is the response time.

**2. What is an appropriate set of hypotheses for this task? What kind of statistical test do you expect to perform?**

Our null hypothesis is, population average response time is same for congruent and incongruent tasks and our alternative hypothesis is,
population average response time is not same for congruent and incongruent tasks.

* H0: μc - μi = 0 
* Ha: μc - μi ≠ 0

where,

* μc: population average response time for congruent tasks
* μi: Population average response time for incongruent tasks

Before deciding what kind of statistical test to perform, 
we should test our independent variables whether these two variables are normally distributed or not

![Normality Tests](http://imagizer.imageshack.us/v2/1024x768q90/921/OtOBws.png)

After implementing Kolmogorov-Smirnov normality test on these two variables, we see that both of our variables are normally distributed
with a 95% probability since our chosen α value (0.05) is less than  both p-values of this test.

In this case, we should use a paired t-test (also known as dependent t-test) because we are investigating whether there is a 
statistically significant difference in the mean of a dependent variable between two related groups.

We can't use a z-test in our case because we don't have any information about population parameters.


**3. Report some descriptive statistics regarding this dataset. Include at least one measure of central tendency 
and at least one measure of variability.**

![Descriptive Statistics](http://imagizer.imageshack.us/v2/800x600q90/921/5RGma8.png)

**4. Provide one or two visualizations that show the distribution of the sample data. 
Write one or two sentences noting what you observe about the plot or plots.**

![Visualizations](http://imagizer.imageshack.us/v2/1024x768q90/924/opRsln.png)

It looks like congruent tasks are completed faster than incongruent tasks.

**5. Now, perform the statistical test and report your results. What is your confidence level and your critical statistic value? 
Do you reject the null hypothesis or fail to reject it? Come to a conclusion in terms of the experiment task. 
Did the results match up with your expectations?**

Results after doint a paired t-test using Minitab:

![Test Results](http://imagizer.imageshack.us/v2/800x600q90/924/AY8tPF.png)

At 95% confidence level, we reject H0 and conclude saying that 
population average response time is not same for congruent and incongruent tasks.
We can say that, people can not identify color words whose names match the colors in which they are printed 
and words whose names do not match the colors  at the same speed.
This is an expected result for me.
