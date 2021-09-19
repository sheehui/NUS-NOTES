---
layout: post
title: 'ST2334 - Chapter 2: Concepts of Random Variables'
date: '2021-09-19T22:31:00.000-08:00'
author: Shee Hui
tags: 
---

## Random Variable

Definition:

> Let S be a sample space associated with the experiment, E
>
> A *function* X, which assigns a number ot every element $s\in S$ is called a **random variable.**

Remarks

- X is a **real-valued function**

- The range space of X is the set of real numbers

    ​	$R_X=\{x|x=X(s),s\in S\}$

    ​	Each possible value x of X represents an event that is a subset of the sample 	space S

- If S has elements that are themselves real numbers, we take X(s) = s. In this case $R_X=S$

<p>&nbsp</p>

## Equivalent Events

Let E be an experiment and S its sample space.

Let X be a random variable defined on S and $R_X$ be its range space. That is, $X:S\rightarrow \R$

Let B be an event with respect to $R_X$; That is $B\sub R_X$

Suppose A is defined as $A=\{s\in S|X(s)\in B\}$

i.e A consists of all sample points,s,in S for which $X(S)\in B$

> A and B are equivalent events and **Pr(B) = Pr(A)**

<p>&nbsp</p>

## Discrete Probability Distributions

### Discrete Random Variable

Let X be a random variable

> If the number of possible values of X (i.e., $R_X$​, the range space) is <u>*finite or countable infinite*</u>, we call X a **discrete random variable.**

i.e. possible values of X may be listed as $x_1,x_2,x_3,...$​



### Probability Function

For a discrete random variable, each value of X has a certain probability f(x)

Such a function  f(x) is called the probability function, p.f.(or probability mass function, p.m.f)

The collection of pairs $(x_i,f(x_i))$ is called the probability distribution of X.

*Probability of $X=x_i$ denoted by $f(x_i)$ (i.e. $F(x_i)=Pr(X=x_i)$), must satisfy the following two conditions:*

1. $f(x_i)\geq 0\ for\ all\ x_i$​
2. $\sum^\infin_{i=0}f(x_i)=1$

<p>&nbsp</p>

## Continuous Probability Distributions

### Continuous Random Variable

> For $R_X$​, the range space of a random variable, X, is an **interval or a collection of intervals**

<p>&nbsp</p>

### Probability Density Function

Let X be a continuous random variable.

Probability density function (p.d.f) f(x) is a function, f(x), satisfying the following conditions:

1. $f(x)\geq 0$ for all $x\in R_X$

2. $\int_{R_X}f(x)\ dx=1\ or \int^\infin_{-\infin}f(x)\ dx=1$

3. For any c and d such that $c<d$, (i.e. (c,d) $\sub R_X$​)

    ​			$Pr(c\leq X\leq d)=\int^d_cf(x)\ dx$​ (area under the graph of pdf)

Remarks:

1. in continuous case, probability of X equals to fixed value 0

    ​	==> $Pr(c\leq X\leq d)=Pr(c< X\leq d)=Pr(c\leq X< d)=Pr(c< X< d)$

2. Pr(A) = 0 does not imply A = $\emptyset$

3. If X assumes values only in some interval [a,b], we may simply set f(x) = 0 for all X outside [a,b]

<p>&nbsp</p>

## Cumulative Distribution Function

>Let X be a random variable, discrete or continuous
>
>We define F(x) to be the **cumulative distribution function** of the random variable where
>
>> $F(x)=Pr(X\leq x)$

<p>&nbsp</p>

### CDF for Discrete Random Variables

> If X is a discrete random variable, then			
>
> ​		$F(x)=\sum_{t\leq x}f(t)=\sum_{t\leq x}Pr(X=t)$

the pdf of a discrete random variable is a step function

- for any two numbers a and b with $a\leq b$

    ​	$Pr(a\leq X\leq b)=Pr(X\leq b)-Pr(X<a)=F(b)-F(a^-)$

    $a^-$ : largest possible value of X that is strictly < a

- if the only possible values are integers and if a and b are integers, then

    ​		$Pr(a\leq X\leq b)=Pr(X=a\ or\ a+1\ or\ \cdots \ or\ b)$​

    ​	Also, $Pr(a\leq X \leq b)=F(b)-F(a-1)$

- $a=b$ yields $Pr(X=a)=F(a)=F(a-1)$

<p>&nbsp</p>

### CDF for Continuous Random Variables

> If X is a continuous random variable, then
>
> ​		$F(x)=\int^x_{-\infin}f(t)\ dt$

- if the derivative exists, $f(x)=\frac{d\ F(x)}{dx}$

- $Pr(a\leq X\leq b)=Pr(a<X\leq b)=F(b)-F(a)$

- F(x) is a non-decreasing function

    ​		if $x_1<x_2$, then $F(x_1)\leq F(x_2)$

- $0\leq F(x)\leq 1$

<p>&nbsp</p>

## Mean and Variance of a Random Variable

### Expected Values

1. If X is a discrete random variable taking on values $x_1,x_2,\cdots$ with probability function $f_X(x)$,

    > the mean or expected value of X, denoted by E(X) as well as by $\mu_x$ is defined by
    >
    > > $\mu_x = E(X) = \sum_ix_if_X(x_i)=\sum_xxf_X(x)$​

    *expected value is not necessarily a possible value of the random variable X

2. If X is a continuous random variable with probability density function $f_X(x)$​, 

    >  the mean of X is defined by
    >
    >  > $\mu_x=E(X)=\int^\infin_{-\infin}xf_X(x)\ dx$

    "weighted average"

Remarks:

1. E(X) exists provided the sum or integral exists

2. if $f_X(x)=1/N$ for each of the N values of x, the mean

    ​			$E(X)=\sum_ix_if(x_i)=\frac{1}{N}\sum_ix_i$

    becomes the average of N items

<p>&nbsp</p>

### Expectation of a Function of a RV

For any function g(X) of a random variable X with p.f. $f_X(x)$

> 1. $E[g(X)]=\sum_xg(x)f_X(x)$​

> 2. $E[g(X)]=\int^\infin_{-\infin}g(x)f_X(x)\ dx$

#### Special Cases

1. $g(x)=(x-\mu_x)^2$​​ ---> definition of variance of a given RV, X

    > Let x be a RV with p.f. f(x), then the **variance** of X is defined as 
    >
    > > $\sigma^2=V(X)=E[(X-\mu_x)^2]$
    > >
    > > ​		$=\left\{    \begin{array}{ll}      \sum_x(x-\mu_x)^2f_X(x), & \text{if X is discrete,}\\      \int^\infin_{-\infin}(x-\mu_x)^2f_X(x)\ dx, & \text{if X is continuous}.    \end{array}  \right.$​

    Remarks:

    (a) $V(X)\geq 0$

    (b) $V(X)=E(X^2)-[E(X)]^2$

    > **Standard deviation** of X: $\sigma_x=\sqrt{V(X)}$

2. $g(x)=x^k$

    then $E(X^k)$​ is called the **k-th moment of X**

<p>&nbsp</p>

### Properties of Expections

#### ***Property 1***

> *$E(aX+b)=\sum_x(ax+b)f_X(x)=aE(X)+b$*

<u>Two special cases:</u>

​	(a) Put b = 0, we have E(aX) = aE(X)

​	(b) Put a = 1, we have E(X + b) = E(X) + b

<image src="./../../assets/img/st2334/st2334_2_1.png">
<p>&nbsp</p>

#### ***Property 2***

> *$V(X)=E(X^2)-[E(X)]^2$​*

<image src="./../../assets/img/st2334/st2334_2_2.png">

<p>&nbsp</p>

#### ***Property 3***

> $V(aX+b)=a^2V(X)$, where a and b constants

<image src="./../../assets/img/st2334/st2334_2_3.png">

<p>&nbsp</p>

### Chebyshev's Inequality

!!From the knowledge of E(X) and V(X) we cannot reconstruct the probability distribution of X

$\implies \textrm{we cannot compute quantities like }Pr(|X-E(X)|\leq c)$​​, where c is a positive constant

Let X be a random variable with $E(X)=\mu$ and $V(X)=\sigma^2$

Then,

> $Pr(|X-\mu|\geq k\sigma)\leq 1/k^2$, for any $k>0$ or $Pr(|X-\mu|<k\sigma)\geq1-1/k^2$

the probability that value of X lies at least k standard deviation from its mean is at most $1/k^2$

*Remarks:*

1. inequality is true for all distributions with finite mean and variance
2. theorem gives a lower bound on the probability that $|X-\mu|<k\sigma$. No guarantee that this lower bound is close to the exact probability.