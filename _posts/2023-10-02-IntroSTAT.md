---
layout: post
mathjax: true
categories: media
title: "Introductory Statistics"
---
![Static Badge](https://img.shields.io/badge/Category-Notes-blue) ![Static Badge](https://img.shields.io/badge/Subject-Mathematics-seagreen) ![Static Badge](https://img.shields.io/badge/Updating-brown)  

Please note that this post is only for personal learning purposes and has no commercial use. The copyright belongs to the lecturers (or the authors of the textbooks).    

### <center>Basic Concepts of Data</center>

#### Understanding the World Through Data
* *Summary*: A numerical, graphical, or verbal description of an aspect of data that is on hand.
* *Generalization*: A numerical, graphical, or verbal description of a broader set of units than those on which data was been recorded.
* *Causal Claim*: A claim that changing the value of one variable will influence the value of another variable.
* *Prediction*: A guess about the value of an unknown variable, based on other known variables.

#### The Taxamony of Data
*Variable*: A characteristic of an object or observational unit that can be measured and recorded.   

*Types of variable*:
<ul><li><i>Numerical Variable</i>: Take numbers as values and where the magnitude of the number has a quantitative meaning.</li><ul>
<li><i>Continuous Numerical Variable</i>: Takes values on an interval of the real number line.</li>
<li><i>Discrete Numerical Variable</i>: Takes values that have jumps between them.</li></ul></ul>
<ul>
<li><i>Categorical Variable</i>: Take categories as values. Each unique category is called a level. </li><ul>
<li><i>Ordinal Categorical Variable</i>: With levels that have a natural ordering.</li>
<li><i>Nominal Categorical Variable</i>: With levels with no ordering.</li></ul></ul>

*Data Frame*: An array that associates the observations (downs the rows) with the variables measured on each observation (across the columns). Each cell stores a value observed for a variable on an observation.

*Unit of Observation*: The class of object on which the variables are observed.


### <center>Summarizing Data</center>
#### Summarizing Categorical Data
*Contingency table*: A table that shows the counts or frequencies of observations that occur in every combination of levels of two categorical variables. Used to display the relationship between variables.

We can also choose to present these counts in graphical form by constructing a *bar chart*.

Converting counts into proportions:
* *Joint Proportion*: The proportion of observations of multiple variables that appear in a combination of levels of those variables.
* *Marginal Proportion*: The proportion of observations in one variable that appear in a single level of that variable.
* *Conditional Proportion*: The proportion of observations in one level of one variable that appear in a level of a second variable.

#### Summarizing Numerical Data
Constructing graphical summaries:
* *Dot plot*: A one-dimensional scatter plot. No information lost.
* *Histogram*: Involves aggregation, determined by the binwidth.
* *Density plot*: Shift from bars to a smooth line.
* *Violin plot*: Density curves for different variables.
* *Blox plot*: Similar to violin plots but with less smoothing.

Describing distributions:
* Modality: count the number of peaks (unimodal, bimodal, multimodal, uniform)
* Skew: describes the behavior of tail (left skew, right skew, symmetric)

Constructiong numerical summaries:    
(1) Measures of center
* *Mean*
     
$$\bar x=\frac{x_1+x_2+\cdots+x_n}{n}.$$

* *Median*: Is resistant to the presence of outliers.
* *Mode*: Most common observation.
    
(2) Measures of spread
* *Variance*:

$$s^2=\frac{1}{n-1}\sum_{i=1}^n(x_i-\bar x)^2.$$

* *Standard deviation*:

$$s=\sqrt{\frac{1}{n-1}\sum_{i=1}^n(x_i-\bar x)^2}.$$

#### The Grammar of Graphic
A plot can be decomposed into 3 primary elements:
* The data
* The aesthetic mapping of the variables in the data to visual cues
* The geometry used to encode the observations on the plot.

#### Summarizing Numerical Associations
The *correlation coefficient* $$r$$ between two variables $$x$$ and $$y$$ is

$$r=\frac{1}{n-1}\sum_{i=1}^n\left(\frac{x_i-\bar x}{s_x}\right)\left(\frac{y_i-\bar y}{s_y}\right).$$

The *simple linear model*: 

$$\hat y = b_0+b_1x.$$

A more precise linear model: the *least square line*. The least squares slope is given by

$$b_1=r\frac{s_y}{s_x},$$

and the least squares intercept is 

$$b_0=\bar y-b_1\bar x.$$

The *residual* is

$$\hat e_i=y_i-\hat y_i.$$

#### Multiple Linear Regression
*Dummy variable*: A variable that is 1 if an observation takes a particular level of a categorical variable and 0 otherwise. A categorical variable and 0 otherwise. A categorical variable with $$k$$ levels can be encoded using $$k-1$$ dummy variables.

*Multiple linear regression*: A method of explaining a continuous numerical variable $$y$$ in terms of a linear function of $$p$$ explanatory variables $$x_i$$, which can be numerical or dummy variables.   

$$\hat y=b_0+b_1x_1+b_2x_2+\cdots+b_px_p.$$

The $$b_i$$'s are called *coefficients.*


### <center>Probability</center>
#### Introducing Probability
Some basic terminology:
* *Experiment*: An action that can result in a finite number of possible outcomes.
* *Outcomem space*: The collection of all the possible outcomes of an experiment, denoted by $$\Omega$$.
* *Event*: A collection of outcomes as a result of the experiment being performed, denoted by $$A,B,C,\cdots$$

Axioms of probability:
* **Rule 1**: The chance of any event is at least $$0$$, $$P(A)\geq 0$$ for any event $$A$$.    
* **Rule 2**: The chance of an out come being in $$\Omega$$ is $$1$$.    
  *Impossible event*: An event with no outcomes in it.    
  *Union of events*: $$A\cup B$$, consists of all the outcomes that are either in $$A$$ or $$B$$.    
  *Intersection of events*: $$A\cap B$$, consists of all outcomes in both $$A$$ and $$B$$.    
  *Mutually exclusive events*: $$A\cap B=\varnothing$$, events $$A$$ and $$B$$ do not overlap. $$P(A\cap B)=0$$.
* **Rule 3**: If $$A$$ and $$B$$ are mutually exclusie, then $$P(A\cup B)=P(A)+P(B).$$ Also called the *addition rule*.
  Suppose $$A$$ is an event in $$\Omega$$. The *complement* of $$A$$ is written as $$A^C$$. We have $$A\cup A^C=1,P(A)+P(A^C)=1.$$

#### Calculating Chances
The *conditional probability* of $$B$$ *given* $$A$$ is given by

$$P(B|A)=\frac{P(A\cap B)}{P(A)}.$$
