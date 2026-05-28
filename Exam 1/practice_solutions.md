# Practice Solutions

## Problem 1

### Solution

$$
P(X\ge2) = 1 - P(X=0) - P(X=1)
$$

$$
P(X=1) = \left(\begin{matrix} 7 \\ 1 \end{matrix}\right) \frac{5}{6}^{6}\left(1 - \frac{5}{6}\right)^1\\
= 7 \cdot \frac{5}{6}^{6} \cdot \frac{1}{6}
= \frac{7 \cdot 5^6}{6^7}
\approx 0.390714
$$

$$
P(X=0) = \left(\begin{matrix} 7 \\ 0 \end{matrix}\right) \frac{5}{6}^{7}\left(1 - \frac{5}{6}\right)^0\\
= 1 \cdot \frac{5}{6}^{7} \cdot 1
= \frac{5^7}{6^7}
\approx 0.279082
$$

$$
P(X\ge2) = 1 - P(X=0) - P(X=1)
= 1 - 0.279082 - 0.390714
= \boxed{0.330204}
$$

### Rational

To find $P(x\ge2)$, we can use the complement rule: $P(X\ge2) = 1 - P(X=0) - P(X=1)$. The binomial probability formula is:

$$
P(X=k) = \left(\begin{matrix} n \\ k \end{matrix}\right) p^k (1-p)^{n-k}
$$

Therefore, we can calculate $P(X=0)$ and $P(X=1)$ using the formula, where $n=7$ and $p=\frac{5}{6}$. After calculating these probabilities, we can substitute them back into the complement rule to find $P(X\ge2)$.

## Problem 2

### Solution
Known probabilities:
$$
P(T_p | D) = .96 \\
P(T_p | D^c) = .012 \\
P(D) = .01 \\
$$
We can use Bayes' Theorem to find $P(D | T_p)$:
$$
P(T_p)P(D | T_p) = P(T_p | D)P(D) \\ \\
P(D | T_p) = \frac{P(T_p | D)P(D)}{P(T_p)} 
$$

Find $P(T_p)$ using law of total probability:
$$
P(T_p) = P(T_p | D)P(D) + P(T_p | D^c)P(D^c) \\
= (.96)(.01) + (.012)(.99) \\
= .0096 + .01188 \\
= .02148
$$

Now we can find $P(D | T_p)$:
$$
P(D | T_p) = \frac{P(T_p | D)P(D)}{P(T_p)} \\
= \frac{(.96)(.01)}{.02148} \\
= \frac{.0096}{.02148} \\
\approx \boxed{0.4469}
$$

### Rational

To find the probability that a person has the disease given they tested positive, we can use Bayes' Theorem, which states:

$$
P(B)P(A | B) = P(A)P(B | A)
$$

In this case, we want to find $P(D | T_p)$. We know $P(T_p | D)$, $P(T_p | D^c)$, and $P(D)$. We can find $P(T_p)$ using the law of total probability, which states:

$$
P(A) = P(A | B)P(B) + P(A | B^c)P(B^c)
$$
After finding $P(T_p)$, we can substitute it back into Bayes' Theorem to find $P(D | T_p)$.

## Problem 3

### Solution

First, we need to find $P(X=4)$:

$$
P(X=4) = 1 - P(X=0) - P(X=1) - P(X=2) - P(X=3) \\
= 1 - 01 - 0.3 - 0.3 - 0.1 \\
= 1 - 0.8 \\
= 0.2
$$

Now we can find $E[X]$:
$$
E[X] = \sum_{i=0}^{4} i \cdot P(X=i) \\
= 0 \cdot 0.1 + 1 \cdot 0.3 + 2 \cdot 0.3 + 3 \cdot 0.1 + 4 \cdot 0.2 \\
= 0 + 0.3 + 0.6 + 0.3 + 0.8 \\
= \boxed{2.0}
$$

Now we can find $var[X]$:
$$
var[X] = E[X^2] - (E[X])^2 \\
E[X^2] = \sum_{i=0}^{4} i^2 \cdot P(X=i) \\
= 0^2 \cdot 0.1 + 1^2 \cdot 0.3 + 2^2 \cdot 0.3 + 3^2 \cdot 0.1 + 4^2 \cdot 0.2 \\
= 0 + 0.3 + 1.2 + 0.9 + 3.2 \\
= 5.6 \\
$$

$$
var[X] = E[X^2] - (E[X])^2 \\
= 5.6 - (2.0)^2 \\
= 5.6 - 4 \\
= \boxed{1.6}
$$

### Rational

To find $E[X]$, we use the formula for expected value:

$$
E[X] = \sum_{i} i \cdot P(X=i)
$$

To find $var[X]$, we use the formula for variance:
$$
var[X] = E[X^2] - (E[X])^2
$$
Where $E[X^2]$ can be calculated using the formula:
$$
E[X^2] = \sum_{i} i^2 \cdot P(X=i)
$$

## Problem 4

### Solution

Declare known probabilities:

$$
P(B_1) = \frac{1}{6} \\
P(B_2) = \frac{5}{6} \\
P(R | B_1) = \frac{5}{8} \\
P(R | B_2) = \frac{2}{7}
$$

We can use Bayes' Theorem to find $P(B_1 | R)$:
$$
P(B_1 | R)P(R) = P(R | B_1)P(B_1) \\
P(B_1 | R) = \frac{P(R | B_1)P(B_1)}{P(R)}
$$

$$
P(R) = P(R | B_1)P(B_1) + P(R | B_2)P(B_2) \\
 = \left(\frac{5}{8}\right)\left(\frac{1}{6} \right) + \left( \frac{2}{7}\right)\left(\frac{5}{6}\right)\\
 = 0.3422619
$$

$$
P(B_1 | R) = \frac{P(R | B_1)P(B_1)}{P(R)} \\
= \frac{\left(\frac{5}{8}\right)\left(\frac{1}{6} \right)}{0.3422619} \\
= \frac{0.1041667}{0.3422619} \\
\approx \boxed{0.3043}
$$

### Rational

Similar to other problems, we can use Bayes' Theorem to find the probability that the red marble was drawn from box I given that a red marble was drawn. We just need to find $P(R)$ using the law of total probability, then substitute it back into Bayes' Theorem to find $P(B_1 | R)$.

## Problem 5

### Solution

We will look at each option and see what it is calculating in R to determine which options are correct.

- (a) `pbinom(q=4,size=10,prob=1/6,lower.tail=T)`: with lower tail as True, this is computing $X \le 4$
- (b) `pbinom(q=4,size=10,prob=1/6,lower.tail=F)`: with lower tail false, we are computing $X > 4$
- (c) `pbinom(q=3.5,size=10,prob=1/6,lower.tail=F)`: with lower tail false, we are computing $X > 3.5$
- (d) `pbinom(q=3,size=10,prob=1/6,lower.tail=F)`: with lower tail false, we are computing $X > 3$
- (e) `pbinom(q=3,size=10,prob=1/6)`: Lower tail is true by default so we are computing $X \le 3$
- (f) `pbinom(q=3.9,size=10,prob=1/6,lower.tail=FALSE)`: with lower tail as false, we are computing $X > 3.9$
- (g) `pbinom(q=4.1,size=10,prob=1/6,lower.tail=F)`: with lower tail as false, we are computing $X > 4.1$

Looking at the options above, the ones that will compute $X \ge 4$ are:

c, d, and f

### Rational

I am less certain on the specifics of the function, other than the pbinom function using integers for the steps, so while using the `lower.tail=F` flag in the function will compute $x > q$. In our case, if q is less than 4, then the result from the pbinom function will be $x \ge 4$.