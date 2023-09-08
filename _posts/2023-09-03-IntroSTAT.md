---
layout: post
mathjax: true
categories: media
title: "Introductory Statistics"
---

Please note that this post is only for personal learning purposes and has no commercial use. The copyright belongs to the lecturers (or the authors of the textbooks).    

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

```
     Variables
--------------------------------
     Length    Depth     Type
--------------------------------
1      43.5     18.1        A     <- Unit of observation
2      48.1     15.1        B
3      49.0     19.5        C
---------------------------------
```

#### Summarizing Categorical Data
*Contingency table*: A table that shows the counts or frequencies of observations that occur in every combination of levels of two categorical variables. Used to display the relationship between variables.
```
-------------------------------------------
        Science     Engineering     Total
-------------------------------------------
Male         50             150       200
Female      150             150       300
Total       200             300       500
-------------------------------------------
```
We can also choose to present these counts in graphical form by constructing a *bar chart*.

Converting counts into proportions:
* *Joint Proportion*: The proportion of observations of multiple variables that appear in a combination of levels of those variables.
* *Marginal Proportion*: The proportion of observations in one variable that appear in a single level of that variable.
* *Conditional Proportion*: The proportion of observations in one level of one variable that appear in a level of a second variable.

```
-------------------------------------------
        Science     Engineering     Total
-------------------------------------------
Male   |    0.1             150    |  200
       |     joint proportion      |
Female |    0.3             150    |  300   0.1/0.4: conditional proportion
        ----------------------------
Total       0.4             300       500
            Marginal proportion
-------------------------------------------
```

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
<ul><li> Measures of center
<ul>
     <li><i>Mean</i></li>
     
     $$\bar x=\frac{x_1+x_2+\cdots+x_n}{n}.$$

     <li><i>Median</i>: Is resistant to the presence of outliers</li>
     <li><i>Mode</i>: Most common observation.</li>
</ul>

     
</li>
<li> Measures of spread
     <li><i>*Variance*</i></li>

     $$s^2=\frac{1}{n-1}\sum_{i=1}^n(x_i-\bar x)^2.$$

     <li><i>Standard deviation</i></li>

     $$s=\sqrt{\frac{1}{n-1}\sum_{i=1}^n(x_i-\bar x)^2}.$$
</li></ul>
