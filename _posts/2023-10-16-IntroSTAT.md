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

**The Normal Distribution** $$X\sim N(\mu,\sigma)$$. The standard normal distribution: $$\mu=0,\sigma=1.$$ 

| Interval | Area under the normal curve |
| :--: |  :--: |
| Between -1 and 1 | 0.68 |
| Between -1.96 and 1.96 | 0.95 |
| Between -2.58 and 2.58 | 0.99 |
