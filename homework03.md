<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>

#### [Home](/index.md)

## 22/10 - Homework 03

### INDEX
[Researches about theory (R)](#researches-about-theory-r)
 - [7_R.](#7_r)
 - [8_R.](#8_r)
 - [9_R.](#9_r)
 
[Applications / Practice (A)](#applications--practice-a)

[Researches about applications (RA)](#researches-about-applications-ra)


### Researches about theory (R)  

#### 7_R. 
First, we are going to discuss about **marginal**, **joint** and **conditional** distribution, so given 2 variables X and Y we can describe those distributions as follows:
 - **Marginal**: By *marginal distribution* we mean the a subset of a collection in a bivariate distribution table (usually situated in the most right row and in the bottom row) and are indicated by the **Total** lable, so it refers to the total occurrencies of an Y variable in all the X variable columns, and the total of each X variable columns, in all the Y variable rows. So for every bivariate distribution table, we have 2 univariate marginal distribution, one for X and one for Y.

 - **Joint**: With *Joint Distribution* we mean all the single values contained in the X,Y cells, so given 2 sets of variables X, Y, the joint distribution is  probability ditribution that each of X,Y land in any particular range or discrete set of values specified for that variable.

 - **Conditional**: Given two *jointly distributed* 
random variables X and Y, we mean by conditional distribution of **Y** given **X** as the probability distribution of Y when we expect X to be a particular value.

A pratical example below for the *Marginal* and *Joint* distribution:

![Brainkart Example](/images/hw03/7_r.png)

The values in the purple box, are the Marginal distribution value, the orange one are the Joint distribution value, and let's say that we want the marks distribution of the people between 20-22 years, that's where we have our conditonal distribution in a blue box. 

[Back Up](#index)  

#### 8_R.  
The **statistical independence** is usually referred to variables, we can say that two variables are statistically independent if there is no way that the probability of a certain value in one variable will affect the distribution of the other one, so if there is absolutely no correlation between the distribution and the variable we are considering. Let's take for example the distribution of student's grades divided by gender, we can imagine that there is no correlation (and indeed there shouldn't be) between the grades distribution and the student's genders and indeed the grades distribution remains pretty much similiar at the gender variable changing. The fact that the relative joint frequencies are equal to the products of the corresponding marginal frequencies happens because of the mathematical definition of independence;  
Considering a bivariate distribution table with $$X_{i}$$ and $$Y_{j}$$ values, we define the independence by the following conditions:

$$
\frac{n_{ij}}{n_{.j}} = \frac{n_{i.}}{n}
$$

That means that all the conditional distributions have the same shape of the relative marginal distribution.

Switching rows with columns instead we would have:

$$
\frac{n_{ij}}{n_{i.}} = \frac{n_{.j}}{n}
$$

We can see that this is basically the same of the previous formula, so we get to the same conclusion in both formulas:

$$
n_{ij}n = n_{i.}n_{.j}
$$

and that's the basical condition of independence.
To rewrite that in terms of frequency, we just need to  divide everything for n:

$$
\frac{n_{ij}n}{n} = \frac{n_{i.}n_{.j}}{n}
$$

so, after simplifications:

$$
\frac{n_{ij}}{n} = \frac{n_{i.}n_{.j}}{n}
$$

By that we can rewrite that formula as:

$$
f_{ij} = f_{i}\cdot f_{j} \Rightarrow
Freq\left\{ x=x_{i} \wedge y=y_{j}\right\} \Rightarrow 
Freq\left\{x=x_{i}\right\} \cdot Freq\left\{ y=y_{j}\right\}
$$
and that explains why the relative joint frequencies are equals to the products of the corresponding marginal frequencies.

[Back Up](#index)

#### 9_R.



 - **Sources**:
    - [Wikipedia](https://en.wikipedia.org/wiki/Marginal_distribution)
    - [Brainkart](http://www.brainkart.com/article/Bivariate-Frequency-Distributions_35069)
 
 ---
 
### Applications / Practice (A)  

---

### Researches about applications (RA)
