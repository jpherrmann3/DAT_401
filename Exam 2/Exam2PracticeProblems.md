# Exam 2 Practice Problems

1. **(10 pts)** The average drying time of a manufacture's paint is 20 minutes. Investigating the effectiveness of a modification in the chemical composition of their paint, the manufacturer wants to test the null hypothesis $H_0: \mu = 20$ against a suitable alternative, where $\mu$ is the average drying time of the modified paint.

(a) What alternative hypothesis should they use if they do no want to make the modification in the chemical composition of paint unless it decreases the drying time?

(b) What alternative hypothesis should the manufacturer use if the new process is actually cheaper and she wants to make the modification unless it increases the drying time of the paint?

2. **(15 pts)** Suppose a basketball player claimed to be a $80%$ free-throw shooter. We think his bragging has no ground in reality and want to challenge him. To test this claim, we have him attempt 50 free throws.

(a) Set up a suitable (simple!) null hypothesis, as well as a composite alternative hypothesis regarding the parameter $\theta =$ probability of success in a single free throw. (Note: you van first think of some suitable composite null hypothesis, and as its worse case scenario, extract appropriate simple null hypothesis).

$H_0: \theta = $ _____  VS $H_1: \theta$ _____.

(b) Suppose you want to run the test base on statistic $X =$ number of successful shots in the 50 trials. Which of the these intervals is the most reasonable choice for critical (i.e. rejection) region? (circle one)

(i) $C = \{x \in \mathbb{R} | k \le x \le 50\}$, for some $k \in \{0, \ldots, 50\}$

(ii) $C = \{x \in \mathbb{R} | k_1 \le x \le k_2\}$, for some $0 \le k_1 < k_2$.

(iii) $C = \{x \in \mathbb{N} | 0 \le k\}$, for some $k \in \mathbb{N}$

(iv) $C = \{x \in \mathbb{N} | 0 \ge k\}$, for some $k \in \mathbb{N}$


(c) What is the distribution of $X$? Find the expression for $\alpha = P_{H_0}$ (type I error) (in terms of $k$), but do not try to calculate it, just set up the expression.

(d) If the observed value of your test statistic $X$ is 32, what is the p-value? (Don't calculate it, just set up the expression).

3. **(10 pts.)** A biologist wants to test the null hypothesis that the mean wingspan of a certain kind of insect is 12.3
mm against the alternative that it is not 12.3 mm. If she takes a random sample and decides to accept the null
hypothesis if and only if the mean of the sample falls between 12.0mm and 12.6mm, what decision will she make if
she gets ¯x = 12.9 mm and will it be in error if

(a) μ = 12.5 mm?

(b) μ = 12.3 mm?


4. (10 pts.) The length of the skulls of 10 fossil skeletons of an extinct species of bird has a mean of 5.68 cm and
a sample standard deviation of 0.29 cm. Assuming that such measurements are normally distributed, find a 95%
confidence interval for the mean length of the skulls of this species of bird.

You may want to use one of the following:

qt(p=0.025, df=9, lower.tail=FALSE) = 2.2621572

qt(p=0.05, df=9, lower.tail=FALSE) = 1.8331129

qnorm(p=0.025, mean=0, sd=1, lower.tail=FALSE) = 1.959964

qnorm(p=0.05, mean=0, sd=1, lower.tail=FALSE) = 1.6448536

5. (15 pts.) In a random sample of 300 persons eating lunch at a department store cafeteria, only 102 had dessert.
If we use sample proportion ˆp as an estimate of the corresponding true proportion p, with what (approximate)
confidence can we assert that our error |ˆp − p| is less than 0.05?

6. (15 pts.) Equipment for measuring concentration of bacteria has standard deviation σ = 106 bacteria/(ml of
fluid). How many measurements should you make to obtain a margin of error of at most 0.5 · 106 bacteria/ml with a
confidence level of 95%?

You may want to use one of the following:

qt(p=0.025, df=9, lower.tail=FALSE) = 2.2621572

qt(p=0.05, df=9, lower.tail=FALSE) = 1.8331129

qnorm(p=0.025, mean=0, sd=1, lower.tail=FALSE) = 1.959964

qnorm(p=0.05, mean=0, sd=1, lower.tail=FALSE) = 1.644853

7. (10 pts.) Let X = number of trials in a certain experiment until first success (including the successful trial). The
probability of success of a single trial is the unknown value θ ∈ (0, 1) and the trials are assumed to be independent.
Based on a simple random sample (x1, x2, ..., xn), where xi is the number of trials until first success in the i-th
experiment, find ˆθM LE , the maximum likely estimate of θ. (Hint: X ∼ Geom(θ), i.e. X has geometric distribution
with pmf f (k; θ) = P (X = k) = (1 − θ)k−1 · θ, k = 1, 2, 3, ...).

8. (15 pts.) A sample of size n is drawn from Gamma(k = 5, θ) population, where θ > 0 is unknown, called scale
parameter. This gamma distribution has density

$$
f(x; \theta) = \{
    \begin{array}{ll}
        \frac{1}{\Gamma(k) \theta^k} x^{k-1} e^{-x/\theta}, & x > 0 \\
        0, & \text{otherwise}
    \end{array}
$$

Find ˆθMLE, the maximum likelihood estimate of the unknown parameter θ.