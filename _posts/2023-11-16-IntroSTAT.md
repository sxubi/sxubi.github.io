---
layout: post
mathjax: true
categories: media
title: "Introductory Statistics"
---
![Static Badge](https://img.shields.io/badge/Category-Notes-blue) ![Static Badge](https://img.shields.io/badge/Subject-Mathematics-forestgreen) ![Static Badge](https://img.shields.io/badge/Updating-brown)  

Please note that this post is only for personal learning purposes and has no commercial use. The copyright belongs to the lecturers (or the authors of the textbooks).    

## <center>Basic Concepts of Data</center>

### Understanding the World Through Data
* *Summary*: A numerical, graphical, or verbal description of an aspect of data that is on hand.
* *Generalization*: A numerical, graphical, or verbal description of a broader set of units than those on which data was been recorded.
* *Causal Claim*: A claim that changing the value of one variable will influence the value of another variable.
* *Prediction*: A guess about the value of an unknown variable, based on other known variables.

### The Taxamony of Data
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


## <center>Summarizing Data</center>
### Summarizing Categorical Data
*Contingency table*: A table that shows the counts or frequencies of observations that occur in every combination of levels of two categorical variables. Used to display the relationship between variables.

We can also choose to present these counts in graphical form by constructing a *bar chart*.

Converting counts into proportions:
* *Joint Proportion*: The proportion of observations of multiple variables that appear in a combination of levels of those variables.
* *Marginal Proportion*: The proportion of observations in one variable that appear in a single level of that variable.
* *Conditional Proportion*: The proportion of observations in one level of one variable that appear in a level of a second variable.

### Summarizing Numerical Data
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
* **Mean**
     
$$\bar x=\frac{x_1+x_2+\cdots+x_n}{n}.$$

* **Median**: Is resistant to the presence of outliers.
* **Mode**: Most common observation.
    
(2) Measures of spread
* **Variance**:

$$s^2=\frac{1}{n-1}\sum_{i=1}^n(x_i-\bar x)^2.$$

* **Standard deviation**:

$$s=\sqrt{\frac{1}{n-1}\sum_{i=1}^n(x_i-\bar x)^2}.$$

### The Grammar of Graphic
A plot can be decomposed into 3 primary elements:
* The data
* The aesthetic mapping of the variables in the data to visual cues
* The geometry used to encode the observations on the plot.

### Summarizing Numerical Associations
The **correlation coefficient** $$r$$ between two variables $$x$$ and $$y$$ is

$$r=\frac{1}{n-1}\sum_{i=1}^n\left(\frac{x_i-\bar x}{s_x}\right)\left(\frac{y_i-\bar y}{s_y}\right).$$

The **simple linear model**: 

$$\hat y = b_0+b_1x.$$

A more precise linear model: the **least square line**. The least squares slope is given by

$$b_1=r\frac{s_y}{s_x},$$

and the least squares intercept is 

$$b_0=\bar y-b_1\bar x.$$

The **residual** is

$$\hat e_i=y_i-\hat y_i.$$

### Multiple Linear Regression
**Dummy variable**: A variable that is 1 if an observation takes a particular level of a categorical variable and 0 otherwise. A categorical variable and 0 otherwise. A categorical variable with $$k$$ levels can be encoded using $$k-1$$ dummy variables.

**Multiple linear regression**: A method of explaining a continuous numerical variable $$y$$ in terms of a linear function of $$p$$ explanatory variables $$x_i$$, which can be numerical or dummy variables.   

$$\hat y=b_0+b_1x_1+b_2x_2+\cdots+b_px_p.$$

The $$b_i$$'s are called *coefficients.*


## <center>Probability</center>
### Introducing Probability
Some basic terminology:
* *Experiment*: An action that can result in a finite number of possible outcomes.
* *Outcomem space*: The collection of all the possible outcomes of an experiment, denoted by $$\Omega$$.
* *Event*: A collection of outcomes as a result of the experiment being performed, denoted by $$A,B,C,\cdots$$

Axioms of probability:
* **Rule 1** The chance of any event is at least $$0$$, $$P(A)\geq 0$$ for any event $$A$$.    
* **Rule 2** The chance of an out come being in $$\Omega$$ is $$1$$.    
  *Impossible event*: An event with no outcomes in it.    
  *Union of events*: $$A\cup B$$, consists of all the outcomes that are either in $$A$$ or $$B$$.    
  *Intersection of events*: $$A\cap B$$, consists of all outcomes in both $$A$$ and $$B$$.    
  *Mutually exclusive events*: $$A\cap B=\varnothing$$, events $$A$$ and $$B$$ do not overlap. $$P(A\cap B)=0$$.
* **Rule 3** If $$A$$ and $$B$$ are mutually exclusie, then $$P(A\cup B)=P(A)+P(B).$$ Also called the *addition rule*.
  Suppose $$A$$ is an event in $$\Omega$$. The *complement* of $$A$$ is written as $$A^C$$. We have $$A\cup A^C=1,P(A)+P(A^C)=1.$$

### Calculating Chances
The **conditional probability** of $$B$$ *given* $$A$$ is given by

$$P(B|A)=\frac{P(A\cap B)}{P(A)}.$$

**Independent events** Two events are *independent* if the probabilities for the second event remain the same if we know that the first event has happened, no matter how the first event turns out. Otherwise the events are called *dependent*. If $$A$$ and $$B$$ are independent, then $$P(B|A)=P(B)$$.     
**Check for independence** If $$A$$ and $$B$$ are independent, then $$P(A\cap B)=P(A)\times P(B).$$

**The inclusion-exclusion principle** The union of two events is

$$P(A\cup B)=P(A)+P(B)-P(A\cap B).$$

### Random Variables
**Random variable** A random variable $$X$$ is a function that associates real numbers with outcomes from a random experiment which are in an outcome space $$\Omega$$, i.e. $$X:\Omega\mapsto\mathbb{R}$$.

**Probability distribution of a random variable** The set of possible values of $$X$$, along with the associated probabilities, is called the *probability distribution* for the random variable $$X$$.

**Discrete and continuous random variable** Discrete random variables are restricted to take particular values in an interval. Continuous random variables can take any value in some specific interval.

**The probability mass function (pmf)** $$f(x)=P(X=x)$$.

**Bernoulli distribution** $$X$$ is a random variable that takes the value $$1$$ with probability $$p$$ and the value $$0$$ with probability $$1-p$$.

**Discrete uniform random distribution** $$X$$ takes the value $$1,2,\cdots,n$$ with $$\displaystyle P(X=k)=\frac{1}{n}$$ for $$k=1,2,\cdots,n$$.

**Binomial distribution** A random experiment has two outcomes: success and failure, and the probability of success is $$p$$. Repeat the experiment $$n$$ times, and let $$X$$ count the number of sucesses in $$n$$ independent trails. Write as $$X\sim\text{Bin}(n,p)$$. 

$$\displaystyle P(X=k)=\binom{n}{k}p^k(1-p)^{n-k},\quad \binom{n}{k}=\frac{n!}{k!(n-k)!}.$$

**Hypergeometric distribution** The population consists of $$N$$ units, and each time draw a unit, all the units are equally likely to be drawn. The population consists of two types of units: success and failure. Draw a sample of size $$n$$ without replacement. Let $$X$$ be the number of successes in $$n$$ draws,

$$P(X=k)=\displaystyle\frac{\binom{G}{k}\binom{N-G}{n-k}}{\binom{N}{n}},$$

where $$N$$ is the size of polulation, $$G$$ is the number of successes in the population. 

**The cumulative distribution function (cdf)** $$F(X)=P(X\leq x)$$.

### Expected Value and Variance of Random Variable
**Expected value of a random variable** $$E(X)=\sum_x xP(X=x)=\sum_x xf(x).$$      
**Properties of expectation** 
* Expected value of a constant is just the constant itself: $$E(c)=cf(c)=c.$$
* Constant multiple of a random variable: $$E(cX)=\sum_x cxf(x)=cE(x).$$
* Additivity: $$X,Y$$ are two independent variable, $$E(X+Y)=E(X)+E(Y).$$
* Linearity: $$E(aX+bY)=aE(x)+bE(Y).$$
* Expectation of a function of a random variable: $$Y=g(X)$$. Then $$E(Y)=E(g(X))=\sum_xg(x)f(x).$$

Bernoulli random variables: $$E(X)=p.$$ Binomial random variable: $$E(X)=np.$$    

**Variance of a random variable** $$\mu=E(X),g(X)=(X-\mu)^2$$. The variance of $$X$$ is $$Var(X)=E(g(X))=E[(X-\mu)^2].$$     
**Standard deviation of a random variable** $$SD(X)=\sqrt{Var(X)}.$$     
**Computational formula for variance** $$Var(X)=E(X^2)-\mu^2.$$     
**Properties of variance and standard deviation**
* The variance of a constant is $$0$$.     
* Variance of a constant multiple: $$Var(cX)=c^2Var(X),SD(cX)=|c|SD(X)$$.    
* Variance is unchanged by adding a constant: $$Var(X+c)=Var(X).$$     
* Additivity: If $$X,Y$$ are independent, then $$Var(X+Y)=Var(X)+Var(Y),Var(X-Y)=Var(X)+Var(Y).$$

Bernoulli random variables: $$Var(X)=p(1-p).$$ Binomial random variables: $$Var(X)=np(1-p).$$    

**IID random variables** The independent variables having the same pmf and cdf.      
For IID random variables, their sum $$S_n=\sum_i^n x_i.$$ Then $$E(S_n)=nE(X_1),Var(S_n)=nVar(X_1), SD(S_n)=\sqrt{n}SD(X_1).$$ The average of the random variables is $$\bar X=\displaystyle\frac{S_n}{n}$$. $$\hat X$$ is called the *sample mean*. $$E(\hat X)=E(X_1),Var(\hat X)=\displaystyle\frac{1}{n}Var(X_1}, SD(\hat X)=\displaystyle\frac{1}{\sqrt{n}}SD(X_1)$$.      
**Standard error** $$S_n,\hat X$$ are computed from the sample, they are called *statistics*. Use the term *standard error* to denote the standard deviation of statistics: $$SE(S_n),SE(\hat X).$$       

**Probability denisty function of a continuous distribution** $$f(x)\geq 0,\displaystyle\int_{-\infty}^{\infty} f(x)dx=1.$$     
**Probability that lies in a interval** $$P(a<X<b)=\displaystyle\int_a^b f(x)dx.$$       
**Cumulative distribution function** $$F(X)=P(X\leq x)=\displaystyle\int_{-\infty}^x f(t)dt.$$

## <center>Generation</center>
### From Samples to Populations
**Sample** The subset of units that are observed, measured and analyzed.      
**Population** The set of units from which the sample is drawn.     
**Statistic** A numerical summary of a sample.     
**Population parameter** A numerical summary of a population.

Types of statistical bias:
* **Selection bias** When the mechanism used to choose units for the sample tends to select certain units with a higher probability than other units.
* **Measurement bias** When your process of measuring a variable systematically misses the target in one direction.
* **Non-response bias** When certain units originally selected for the sample fail to provide data and those non-responders different in meaningful ways from the responders.

Types of variation:
* **Sampling variability** If the sample is drawn from the population with some amount of randomness, the sampling variability describes the variability from one sample to the next.
* **Measurement variability** When we take multiple measurements on the same object and we get variations in measurements from one sample to the next.

**Sampling Distribution** The distribution of a statistic upon repeated sampling.


### Condifence Intervals
**Standard Error (SE)** The standard deviation of the sampling distribution of a statistic.       
**Confidence Interval** An interval of two values that represent lower and upper bounds on the statistic that captures most of the sampling distribution.      
**A Point Estimate** Given the sample average $$\bar{x}$$, the standard deviation of the sample $$s$$, and the number of sample $$n$$, we want to infer the population average $$\mu$$ by $$\bar x$$. The standard error of $$\bar x$$ is

$$SE(\bar x)\approx\frac{\sigma}{\sqrt{n}},\quad s\approx\sigma\quad\Rightarrow\quad SE(\bar x)\approx\frac{s}{\sqrt{n}}.$$

**The Normal Distribution** $$X\sim N(\mu,\sigma)$$. The standard normal distribution: $$\mu=0,\sigma=1.$$ We assumem that the sampling distribution is normal.

| Interval | Area under the normal curve |
| :--: |  :--: |
| Between -1 and 1 | 0.68 |
| Between -1.96 and 1.96 | 0.95 |
| Between -2.58 and 2.58 | 0.99 |

E.g. we have a sample mean $$\bar x$$ and a standard error $$SE$$, the 95% condifence interval is $$[\bar x-1.96SE,\bar x+1.96SE]$$, i.e. 95% condifent for the population mean lies in the interval.

#### Bootstrapping
**The Boostrap Algorithm** Used to assess sampling variability.     
&emsp; 1. Treat the sample as a boostrap population;     
&emsp; 2. Draw a new sample with replacement from the boostrap population;       
&emsp; 3. Calculate the statistic of interest on the new sample;       
&emsp; 4. Repeat steps 2 and 3 many times to build up a bootstrap sampling distribution.     
**Bootstrap Confidence Interval (percentile method)** For a 95% condifence interval, calculate the 2.5% and 97.5% quantiles of the boostrap distribution.    


## <center>Generalization</center>
### Hypothesis Testing I
*Null Hypothesis* A description of the chance process for generating data. Sometimes referred to as $$H_0$$. E.g. "The occurrence of a death is independent of the presence of Gilbert."

*Alternative Hypothesis* The assertion that a mechanism other than the null hypothesis generated the data. Sometimes referred to as $$H_A.$$ E.g. "The occurrence of a death is dependent on the presence of Gilbert."

*Test Statistic* A numerical summary of the observed data that bears on the *null hypothesis*. Under the null hypothesis it has a sampling distribution (also called a “Null Distribution”). In our case the proportion difference of deaths $$\hat p_\text{gilbert}-\hat p_\text{no gilbert}$$ is the statistic.

*p-value* The probability of a test statistic as rare or even more rare than the one observed under the assumptions of the null hypothesis. If the p-value is high, then the data is consistent with the null hypothesis. The p-value could be estimated using the proportion of statistics from the simulated null distribution that are more than the observed statistic.

The data frame `code_blue`:
```
# A tibble: 1,641 × 3
   shift death staff     
   <dbl> <chr> <chr>     
 1   626 no    no_gilbert
 2   590 no    no_gilbert
 3  1209 no    no_gilbert
...
```
Create the sampling distribution under the null hypothesis
```
library(infer)

null <- code_blue %>%
  specify(response = death,
          explanatory = staff, 
          success = "yes") %>%
  hypothesize(null = "independence") %>%
  generate(reps = 5000, type = "permute") %>%
  calculate(stat = "diff in props")

null %>%
  ggplot(aes(x = stat)) +
  geom_bar(col = "white", bins = 23) +
  theme_bw() +
  labs(x = "Difference in Proportions")
```

### Hypothesis Testing II
Want to show that the distribution of first digits of the vote numbers satisifies the Benford's Law:

$$H_0:\quad p_1=0.301,\quad p_2=0.176,\quad\cdots$$

*Chi-squared statistic* A statistic used to measure the distance between two categorical distributions, one observed and one expected. For a distribution with $$k$$ categories, $$O_i$$ observed counts in each category, and $$E_i$$ expected counts,

$$\chi^2=\sum_{i=1}^k\frac{(O_i-E_i)^2}{E_i}.$$

```
library(infer)

p_benfords <- c("1" = log10(1 + 1/1),
                "2" = log10(1 + 1/2),
                .....)

obs_stat <- iran %>%
  specify(response = first_digit) %>%
  hypothesize(null = "point", p = p_benfords) %>%
  calculate(stat = "Chisq")

null <- iran %>%
  specify(response = first_digit) %>%
  hypothesize(null = "point", p = p_benfords) %>%
  generate(reps = 5000, type = "draw") %>%
  calculate(stat = "Chisq")

null %>%
  visualize() +
  shade_p_value(obs_stat, direction = "right")
# This creates the null distribution of
the statistic (chi_square) and the observed chi-square
```

### Wrong by Design
Statistical errors:

| Truth | Test Conclusion: Reject $$H_0$$ | Test Conclusion: Fail to reject $$H_0$$ |
| :--: |  :--: | :--: |
| $$H_0$$ is true | *Type I Error* | Good decision |
| $$H_A$$ is true | Good decision | *Type II Error* |

*Significance level* $$\alpha$$: A number between 0 and 1 that serves as the threshold for the p-value. The null hypothesis is rejected when the p-value $$<\alpha$$, and the finding is found “statistically significant”. By convention $$\alpha =0.05$$. 

*Two-sided hypotheses*: We have $$H_0:\hat p_\text{gilbert}-\hat p_\text{no gilbert}=0$$. A two-sided hypothesis: $$H_A:\hat p_\text{gilbert}-\hat p_\text{no gilbert}\neq 0$$. A one-sided hypothesis: $$H_A:\hat p_\text{gilbert}-\hat p_\text{no gilbert}< 0$$ or $$>0$$. 

Consider the CPR study which wants to find out whether the survival rate is affected by `control` or `treatement`. The data frame
```
   group      outcome
1 control     died
2 treatment   survived
3 control     survived
...
```
The statistic is the difference of survival rates: $$\hat p_C-\hat p_T$$. The null distribution
```
library(infer)
set.seed(47)

obs_stat <- cpr %>%
  specify(response = outcome, explanatory = group, success = "survived") %>%
  calculate(stat = "diff in props", order = c("treatment", "control")) 

null <- cpr %>%
  specify(response = outcome, explanatory = group, success = "survived") %>%
  hypothesize(null = "independence") %>%
  generate(reps = 1000, type = "permute") %>%
  calculate(stat = "diff in props", order = c("treatment", "control")) 

cpr_tail <- null %>%
  get_p_value(obs_stat, direction = "right") %>%
  pull()

null %>%
  visualize() +
  shade_p_value(obs_stat, direction = "right")

null %>%
  visualize() +
  shade_p_value(obs_stat, direction = "both")
# A double-sided hypothesis, p-value is doubled 
```

*Power* The probability of rejecting the null hypothesis when the null hypothesis is false. This probability depends on how big the effect is (e.g., how good the medical treatment is) as well as the sample size. Suppose the probability of commiting a Type II error is $$\beta$$, then the power is $$1-\beta$$. 


## <center>Causation</center>
### Defining Causality
*Counterfactual* Relating to or expressing what has not happened or is not the case.    
*Cause* “A causes B” if, in a world where A didn’t happen, B no longer happens.

Strategies for estimating causal effects:
* Different units at the same time
  *Matching*: finding a different unit in a close match for every possible important variable, but differs on the variable of interest.
* Same unit at different times

### Experiments
*Average Treatment Effect*  A population parameter that captures the effect of being administered a particular treatment, averaged over each group. Most often estimated by a difference in sample means or a difference in sample proportions. (e.g. Difference of proportions of getting a good job, from cal grad or not)

The design of an experiment to determine whether the *treatment* affects the outcome at group level is *Randomized Controlled Trail (RCT)*. 

*Control* (noun)  A second condition to which a subject or unit could be assigned that draws a contrast with the treatment condition. (verb) Actions taken to eliminate other possible causal factors and ensure that the only difference between the treatment and control group is the factor of interest.

A question: would reading notes as a webpage lead to a deeper understanding? The treatment group (website) and the control group (pdf)

```
---------------------------------
name    group      understanding
---------------------------------
A       pdf        deep
B       pdf        shallow
...
C       website    shallow
D       website    deep
...
---------------------------------
```

*Random Assignmnet* The process of assigning subjects to either the treatment or control group in a random fashion, where they’re equally likely to be assigned to each group.

*Replication* The practice of assigning multiple subjects to both the treatment and control group. Also, the practice of repeating an experiment a second time to see if the result is consistent.

## <center>Prediction</center>
### The Method of Least Squares
*Response Variable* The variable that is being predicted. Also called the dependent or outcome variable. Indicated by $$y$$ or $$Y$$ when treated as a random variable.

*Predictor Variable(s)* The variable or variables that used to predict the response. Also called the independent variables or the features. Indicated by $$x_1,x_2,\cdots$$

*Regression Model* A statistical model used to predict a numerical response variable.

*Classification Model* A statistical model used to predict a categorical response variable.

*The Method of Least Squares* Define a line that has the lowest residual sum of squares of all possible
lines.

*Redidual Sum of Squares (RSS)* For observations of a response variable $$y_i$$, predictions of its value (fitted values) $$\hat y_i$$, and a data set with $$n$$ observations, the RSS is

$$RSS=\sum_{i=1}^n(y_i-\hat y_i)^2.$$

### Evaluating and Improving Predictions
*R-squared* ($$R^2$$) A statistics that measures the proportion of the total variability in the $$y$$-variable (total sum of squares, TSS) that is explained away using our model involving $$x$$ (sum of squares due to regression, SSR).

$$R^2=\frac{SSR}{TSS}=\frac{\sum_{i=1}^n(\hat y_i-\bar y_i)^2}{\sum_{i=1}^n(y_i-\bar y)^2},\quad R^2=1-\frac{RSS}{TSS}=1-\frac{\sum_{i=1}^n(y_i-\hat y_i)^2}{\sum_{i=1}^n(y_i-\bar y)^2}.$$

Properties of $$R^2$$:     
&emsp; 1. Always between $$0$$ and $$1$$;     
&emsp; 2. $$R^2$$ near 1 means predictions are more accurate.      

```
library(tidyverse)
library(broom)
m1 <- lm(Graduates ~ Poverty, data = poverty)
glance(m1)
glance(m1) %>%
  select(r.squared)
```

Improving predictions:    
&emsp; 1. Adding predictions;     
&emsp; 2. Non-linear transformation;    
```
flights <- flights %>%
  mutate(log_dist = log(distance))
lm_log <- lm(avg_speed ~ log_dist, data = flights)
```
&emsp; 3. Polynomials.
```
lm_poly <- lm(y ~ ploy(x = x, degree = 3, raw = TRUE), data = df)
lm_ploy
```

#### Overfitting
*Overfitting* The practice of using a predictive model is very effective at explaining the data used to fit it and correspondingly poor at making predictions on new data. Usually a result of applying a model that is too complex.

*Training Set* The set of observations used to fit a predictive model; i.e. estimate the model coefficients.     
*Testing Set* The set of observations used to assess the accuracy of a predictive model. This set is disjoint from the training set.    
A standard partition: dedicate 80% of the observations to the training set.

Example: predicting final exam scores v.s. study hour    
* Model 1: A linear model
* Model 2: A 5th degree polynomial
```
set.seed(13)
# randomly sample train/test set split
set_type <- sample(x = c('train', 'test'),
                  size = 200,
                  replace = TRUE,
                  prob = c(0.8, 0.2))
biology <- biology %>%
    mutate(set_type = set_type)
biology
```
The data frame
```
  hours score set_type
  <dbl> <dbl> <chr>
1 9.78  88.7  train
2 5.26  60.8  test
...
```
Then
```
biology_train <- biology %>%
    filter(set_type == 'train')
biology_test <- biology %>%
    filter(set_type == 'test')

# use the training data to fit the model
lm_slr <- lm(score ~ hours, data = biology_train)
lm_poly <- lm(score ~ poly(hours, degree = 20, raw = T), 
              data = biology_train)

# calculating the training r square
glance(lm_slr) %>%
    select(r.squared)
glance(lm_poly) %>%
    select(r.squared)

# get predictions on test set
score_pred_linear <- predict(lm_slr, newdata = biology_test)
score_pred_poly <- predict(lm_poly, newdata = biology_test)
# calculate R squared for test set
biology_test %>%
    mutate(score_pred_linear = score_pred_linear,
           score_pred_poly = score_pred_poly,
           resid_sq_linear = (score - score_pred_linear)^2,
           resid_sq_poly = (score - score_pred_poly)^2) %>%
    summarize(TSS = sum((score - mean(score))^2),
              RSS_linear = sum(resid_sq_linear),
              RSS_poly = sum(resid_sq_poly)) %>%
    mutate(Rsq_linear = 1 - RSS_linear/TSS,
           Rsq_poly = 1 - RSS_poly/TSS) %>%
    select(Rsq_linear, Rsq_poly)
```