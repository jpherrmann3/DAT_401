# Final Exam Practice Problems

1. Two dice are cas (call them the first and second die). Denote events

A = the first die show even number

B = the first die shows odd number

C = the second die shows even number greater than 3

D = the two numbers on the dice are equal

Which of the following statements i true (in all its parts)?

(a) A & D are independent, and so are B & D, but not C & D

(b) A & D are independent, and so are B & D, as well as C & D

(c) A & D are independent, and so are C & D, but not B & D

(d) A & D are not independent, nor B & D, but C & D are independent

(e) None of the above statements are entirely true (in its all parts).

2. It is estimated that 11% of emails are spam. A software has been applied to filter spam emails before they reach your inbox. The software can correctly detect 95% of spam emails before they reach your inbox, and the probability for false positive (a non-spam email incorrectly classified as spam) is 4%. If an email is marked by the software as spam, what is the probability that it is indeed a spam email?

3. A laboratory blood test is 95% effective in detecting a certain disease when it is in fact present. However, the test also yields a false positive result for 1% of the healthy persons tested. If 0.5 percent of the population actually has the disease, what is the probability that a person has the disease given that the test result is positive?

4. Assume that prior distribution of probability of success $\theta$ in a single Bernoulli trial is a density of $Beta(\alpha, \beta)$, that is:

$$
\pi(\theta) = \left\{
\begin{array}{ll}
  \frac{1}{B(\alpha, \beta)} \theta^{\alpha - 1} (1 - \theta)^{\beta - 1} & \text{if } 0 < \theta < 1, \\
  0 & \text{otherwise}.
\end{array}
\right.
$$

We take $n$ independent trials an let $X$ be the number of success in these $n$ trials. So, $X \sim Bin(n; \theta)$.

For a given observed value $X = x$, find posterior distribution $\pi(\theta|x)$ for any given outcome $x$ (= total number of successes), for any $\theta \in \mathbb{R}$ (don't forget the case $\theta \notin (0, 1$). Is the posterior still a beta distribution?

5. A sample size $n$ is drawn from an exponential distribution which is defined as

$$
f(x; \theta) = \left\{
\begin{array}{ll}
  \theta e^{-\theta x} & \text{if } x > 0, \\
  0 & \text{otherwise}.
\end{array}
\right.
$$

Find the $\hat{\theta}_{MLE}$, the maximum likelihood estimate of unknown parameter $\theta$.

6. A financial office r for a company wants to estimate the percent of accounts receivablet hat are more thatn 30 days overdue. He surveys 500 accounts and finds that 300 are more than 30 days overdue.

(a) Compute a 95% confidence interval for the true percent of accounts receivable that are more than 30 days overdue.

(b) What is the smallest sample size $n$ for which the officer would obtain margin of error of at most 0.01 with confidence level of 95%?

7. A researcher wants to study if there is a linear relationship between the petal length and petal width of Iris flowers. The following ocmmands were used in R:

```R
data(iris)
mod <- lm(Petal.Width ~ Petal.Length, data = iris)
```

```text
Call:
lm(formula = Petal.Width ~ Petal.Length, data = iris)

Residuals:
     Min       1Q   Median       3Q      Max
-0.56515 -0.12358 -0.01898  0.13288  0.64272

Coefficients:
             Estimate Std. Error t value Pr(>|t|)
(Intercept)   -0.363076  0.039762  -9.131 4.7e-16 ***
Petal.Length   0.415755  0.009582  43.387  < 2e-16 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 0.2065 on 148 degress of freedom
Multiple R-squared:   0.9271,    Adjusted R-squared: 0.9266
F-statistic: 1882 on 1 and 148 degrees of freedom, p-value: < 2.2e-16
```

(a) If we denote by $\beta_1$ coefficient that multiplies Petal.legnth in the model, and $\beta_0$ is the slope. Based on the output, what is te estimated model of relation between Y=Petal.Width and X=Petal.Length?

(b) Conduct a test to determine whether there is linear associate between X and Y at a confidence level 90%. State the null and alternative hypothesis, decision rule by p-value and your conclusion.

(c) According to the model, what is the estimate of the mean of Petal. Width Y when the Petal. Length x is 6? That is, find $\hat{\mu}_{Y|X=6}$.

8. A multiple-choice test question has six possible answers. The question is designed to be very difficult, with exactly one correct answer, but with none of the remaining responses being obeviously worng. The question occurs on an exam taken by 400 students. Let $X$ be the number of students who answer the question correctly and $p$ denotes the probability of a randomly chosen student answering the question correctly. The designers of the question would like to demonstrate that at least some students know what the correct answer is. That is, they want to test whether more people answer the question correctly than it would be excpected just by pure chance. Which hypothesis test and its critical region should be used?

(a) $H_0: p = 0.5 \text{ vs. } H_A = p > 0.5$; critical region: $X < k$ for some $k \in \mathbb{N}$

(b) $H_0: p = 0.5 \text{ vs. } H_A = p > 0.5$; critical region: $X > k$ for some $k \in \mathbb{N}$

(c) $H_0: p = 1/6 \text{ vs. } H_A = p > 1/6$; critical region: $X < k$ for some $k \in \mathbb{N}$

(d) $H_0: p = 1/6 \text{ vs. } H_A = p > 1/6$; critical region: $X > k$ for some $k \in \mathbb{N}$
