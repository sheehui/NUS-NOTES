# Chapter 1: Basic Concept of Probability

## Operations with Events

### Basic Properties of Operations of Events

1. $(A\cap B)^{'} = A^{'}\cup B^{'}$​
2. $(A\cup B)^{'} = A^{'}\cap B^{'}$​
3. $A\cup B=A\cup (B\cap A^{'})$​
4. $A=(A\cap B)\cup(A\cap B^{'})$



### De Morgan's Law

> For any n events 
>
> 1. $(A_1\cup A_2\cup \cdots \cup A_n)^{'}=A_1^{'}\cap A_1^{'}\cap \cdots\cap A_n^{'}$​​
>
> 2. $(A_1\cap A_2\cap \cdots \cap A_n)^{'}=A_1^{'}\cup A_1^{'}\cup \cdots\cup A_n^{'}$​

<p>&nbsp;</p>

## Basic Properties of Probability

1. Pr($\emptyset$​) = 0

2. If $A_1,A_2,\cdots,A_n$ are **mutually exclusive** 

    ​					$\rightarrow Pr(\cup_{i=1}^{\infin}A_{i}) = \sum_{i=1}^{\infin}Pr(A_{i}) = \sum_{i=1}^{\infin}Pr(\empty)$

3. For any event A,

    ​					$Pr(A^{'})=1-Pr(A)$​

4. For any 2 events A and B,

    ​					$Pr(A)=Pr(A\cap B)+Pr(A\cap B^{'})$

5. For any 2 events A and B,

    ​					$Pr(A\cup B)=Pr(A) + Pr(B) - Pr(A\cap B)$

6. For any 3 events A, B and C,

    ​					$Pr(A\cup B\cup C)=Pr(A)+Pr(B)+Pr(C)-Pr(A\cap B)$ 

    ​								$-Pr(A\cap C)-Pr(B\cap C)+Pr(A\cap B\cap C)$​

    <image src="./../../assets/img/st2334/st2334_1_1.png">

    *this can be extended to n events (**Inclusion-Exclustion Principle**)

7. If $A\sub B$, then $Pr(A)\leq Pr(B)$

<p>&nbsp;</p>

### Sample Spaces with Finite Outcomes

Consider sample space *S* which contains a finite number of *k* outcomes. that is,

​													$S=\{a_1,a_2,\cdots ,a_k\}$​

Let $Pr(a_i)=p_1$ be the probability of ${a_i}$​ and

(1) $0\leq p_i\leq 1$, for $i=1,2,,\cdots ,k$​

(2) $p_1+p_2+\cdots +p_k=1$



e.g. if event a has r outcomes, $1\leq r \leq k$​​, and $A=\{a_1,a_2,\cdots ,a_k\}$​​,

​					then $Pr(A) = a_1+a_2+\cdots +a_k$

<p>&nbsp;</p>

### Sample Spaces with Equally Likely Outcomes

If all outcomes are equally likely to occur in a finite set, $Pr(a_i)=1/k$


<p>&nbsp;</p>

## Conditional Probability

The conditional probability of B given A, is defined as

​						$Pr(B|A) = \frac{Pr(A\cap B)}{Pr(A)}, \ \ if \ Pr(A)\neq0$

<image src="./../../assets/img/st2334/st2334_1_2.png">

<p>&nbsp</p>

### Multiplication Rule of Probability

$Pr(A\cap B)=Pr(A)Pr(B|A)$​​ or $Pr(A\cap B)=Pr(B)Pr(A|B)$​​, if $Pr(A)>0,Pr(B)>0$

2 events:

$Pr(A\cap B\cap C)=Pr(A)Pr(B|A)Pr(C|A\cap B)$​, if $Pr(A\cap B)>0$

In general:

<image src="./../../assets/img/st2334/st2334_1_3.png">

<p>&nbsp</p>

### Law of Total Probability

Let $A_1,A_2,\cdots ,A_n$ be a partition of sample space S

i.e. $A_1,A_2,\cdots ,A_n$ are mutually exclusive and exhaustive events such that $A_i\cap A_j=\empty\ for\ i\neq j$

Then for any event B

​				$Pr(B)=\sum_{i=1}^{n}Pr(B\cap A_i)=\sum_{i=1}^{n}Pr(B|A_i)$

<image src="./../../assets/img/st2334/st2334_1_4.png">

<p>&nbsp</p>

### Bayes' Theorem

Let $A_1,A_2,\cdots ,A_n$​​ be a partition of sample space S. Then, for k=1,...,n

​							$Pr(A_k|B)=\frac{Pr(A_k)Pr(B|A_k)}{\sum_{i=1}^{n}Pr(A_i)Pr(B|A_i)}=\frac{Pr(A_k)Pr(B|A_k)}{Pr(B)}$



<p>&nbsp</p>

## Independent Events

> Two events A and B are said to be **<u>independent</u>** $\leftrightarrow Pr(A\cup B)=Pr(A)Pr(B)$​

<p>&nbsp</p>

### Properties of Independent Events

1. Suppose $Pr(A)>0,Pr(B)>0$​. If A and B are **independent**, then

    ​					$Pr(B|A)=Pr(B)\ and\ Pr(A|B)=Pr(A)$​

2. Suppose $Pr(A)>0,Pr(B)>0$​. If A and B are **independent**, then A and B <u>cannot be</u> **mutually exclusive.**

3. Suppose $Pr(A)>0,Pr(B)>0$​​. If A and B are **mutually exclusive**, then A and B <u>cannot be</u> **independent.** ($Pr(A\cap B)=0\neq Pr(A)Pr(B)$)

4. Sample space S as well as the empty set $\empty$ are **independent of <u>any event</u>**.

5. If $A\sub B$, then A and B are **dependent** unless $B=S$

*<u>check for independence</u> with definition formula

<p>&nbsp</p>

### $n$ Independent Events

<u>Pairwise Independent Events</u>

> Set of events $A_1,A_2,\cdots ,A_n$​ are said to be **pairwise independent** if and only if
>
> ​					$Pr(A_i\cap A_j)=Pr(A_i)Pr(A_j)$​
>
> for $i\neq j$ and $i,j=1,\cdots ,n$

<p>&nbsp</p>

### $n$ Mutually Independent Events

> Set of events $A_1,A_2,\cdots ,A_n$ are said to be **mutually independent** if and only if for any subset {$A_{i_1},A_{i_2},\cdots ,A_{i_k}$} of {$A_1,A_2,\cdots ,A_n$}
>
> ​						$Pr(A_{i_1}\cap A_{i_2}\cap \cdots \cap A_{i_k})=Pr(A_{i_1})Pr(A_{i_2})\cdots Pr(A_{i_k})$

<p>&nbsp</p>

### Remarks

1. For any pair of events $A_j,A_k\ where\ j\neq k$, multiplication rule holds.

    For any three distinct events.... and so on

    Total distinct number of cases: $2^n-n-1$

2. Mutually independence $\rightarrow$ pairwise independence 

    **BUT** pairwise independence does not imply mutually independence

3. Suppose $A_1,A_2,\cdots ,A_n$​ are mutually independent events.

    ​			Let $B_i=A_i\ or A_i^{'},\ i=1,2,\cdots ,n$

    Then $B_1,B_2,\cdots ,B_n$ are also mutually independent events.

    