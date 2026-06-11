# DAT 401 EXAM 1 PRACTICE PROBLEMS

SHOW ALL YOUR WORK IN FREE RESPONSE QUESTIONS! NO WORK, NO CREDIT!
PLEASE SUBMIT QUESTIONS IN ORDER OF THEIR APPEARANCE!

1. What is the probability that in 7 rolls of a fair die, number 5 appears at least twice?

2. A blood test indicates the presence of a particular disease 96% of the time when the disease is actually present. The same test indicates the presence of the disease 1.2% of the time when the disease is not present. One percent of the population actually has the disease. If a person gets tested and the test turns positive (suggesting the disease), what is the probability that the person does have the disease?

3. A random variable $X$ with the range $RX = \{0, 1, 2, 3, 4\}$ has the following distribution:


| k | 0 | 1 | 2 | 3 | 4 |
|---|---|---|---|---|---|
| P(X=k) | 0.1 | 0.3 | 0.3 | 0.1 | ?? |

Find $E[X]$ and $var[X]$. (Note that you first need to determine $P (X = 4)$).

4. Consider two boxes, call them box I and box II. Box I contains 3 blue and 5 red marbles, while box II contains 5 blue and 2 red marbles. Suppose you cast a die in order to randomly pick a box. If the die shows number 1, you choose box I. Otherwise, you choose box II. Now, from the chosen box, pick a single marble at random. If following this procedure you chose a red marble, what is the probability that it was drawn from box I? (round the answer to 4
decimal places).

5. Let X = the number of sixes in 10 rolls of a die. Recall that in the documentation for `pbinom()`, for the argument `lower.tail` it says: `lower.tail`: logical; if `TRUE` (default), probabilities are $P[X≤x]$, otherwise, $P[X>x]$.

I. Which of the following R commands could be used to find $P (X ≥ 4)$? (check all that apply)

- (a) `pbinom(q=4,size=10,prob=1/6,lower.tail=T)`
- (b) `pbinom(q=4,size=10,prob=1/6,lower.tail=F)`
- (c) `pbinom(q=3.5,size=10,prob=1/6,lower.tail=F)`
- (d) `pbinom(q=3,size=10,prob=1/6,lower.tail=F)`
- (e) `pbinom(q=3,size=10,prob=1/6)`
- (f) `pbinom(q=3.9,size=10,prob=1/6,lower.tail=FALSE)`
- (g) `pbinom(q=4.1,size=10,prob=1/6,lower.tail=F)`

II. Which of the following R commands could be used to find $P (4 ≤ X ≤ 9)$? (check all that apply)
- (a) `pbinom(q=9,size=10,prob=1/6) - pbinom(q=3,size=10,prob=1/6)`
- (b) `pbinom(q=9,size=10,prob=1/6) - pbinom(q=4,size=10,prob=1/6)`
- (c) `pbinom(q=9,size=10,prob=1/6) - pbinom(q=3.5,size=10,prob=1/6)`
- (d) `pbinom(q=9,size=10,prob=1/6,lower.tail=F) - pbinom(q=3,size=10,prob=1/6,lower.tail=F)`
- (e) `pbinom(q=9.2,size=10,prob=1/6,lower.tail=T) + pbinom(q=3,size=10,prob=1/6,lower.tail=F)`

7. A mechanical assembly consists of a rod with a bearing on each end. The three parts are manufactured independently, and all vary a bit from part to part. The length of the rod has mean $µ_R = 80$ millimeters (mm) and standard deviation $σ_R = 0.003$ mm. The length of a bearing has mean $µ_B = 30$ mm and standard deviation
$σ_B = 0.002$ mm. What are the mean $µ_A$ and standard deviation $σ_A$ of the total length of the assembly, rounded to
three decimal places ? (circle one)
1

- (a) $µ_A = 110$, $σ_A = 0.007$
- (b) $µ_A = 140$, $σ_A = 0.007$
- (c) $µ_A = 140$, $σ_A = 0.005$
- (d) $µ_A = 140$, $σ_A = 0.004$
- (e) $µ_A = 110$, $σ_A = 0.004$
- (f) none of the above

8. Let $X ∼ N (µ = 1, σ2 = 4)$.

I. Which of the following R commands could you use to find P (X ≥ 5)? (circle one)

- (a) `pnorm(5, mean=1, sd=2, lower.tail=T)`
- (b) `pnorm(5, mean=1, sd=2, lower.tail=F)`
- (c) `pnorm(5, mean=1, sd=4, lower.tail=F)`
- (d) `qnorm(5, mean=1, sd=2, lower.tail=F)`
- (e) `qt(5, mean=1, sd=2)`
- (f) `dnorm(5, mean=1, sd=4, lower.tail=F)`
- (g) none of the above

II. Which of the following could you use to find P (5 ≤ X ≤ 9)? (check all that apply)

- (a) `pnorm(9, mean=1, sd=2) - pnorm(5, mean=1, sd=2)`
- (b) `pnorm(9, mean=1, sd=2) + pnorm(5, mean=1, sd=2,lower.tail=F)`
- (c) `pnorm(9, mean=1, sd=2, lower.tail=F) - pnorm(5, mean=1, sd=2, lower.tail=F)`
- (d) `pnorm(9, mean=1, sd=2) - pnorm(4.9, mean=1, sd=2)`
- (e) `pnorm(9.1, mean=1, sd=2) - pnorm(5, mean=1, sd=2,lower.tail=F)`
- (f) `pnorm(9, mean=1, sd=2, lower.tail=T) - pnorm(5, mean=1, sd=2, lower.tail=T)`

9. A random sample $(X1, X2, ..., X20)$ of size 20 was drawn from the binomial distribution `X ∼ Bin(n = 12; p = 1/5)`.

- (a) What are the population mean µX = E[X] and the population variance σ2 X = var[X]?
- (b) What are the mean $µ_{\bar{X}}$ and the variance $σ^2_{\bar{X}} = var[ \bar{X}]$ of the sample mean $\bar{X} = 1/20\sum_{i=1}^{20} X_i$?

10. At a certain college, the Admission Committee for Data Science Undergraduate Program decided to send the offer letter to 180 applicants. From the past experience, 30% of applicants who received the offer letter actually accept it and become students of the college. Assume applicants decide whether to accept the offer independently of each other, and that each of them has 30% probability of accepting the offer. Let S be the number of applicants (out of these 180) who accept the offer and become students of the college. Which of the following R codes gives us the output that best approximates P (50 ≤ S ≤ 60), the probability that the number of 1st-year students in the upcoming academic year will be between 50 and 60. (Hint: Recall that binomial random variable `Bin(n; p)` has mean $µ = np$ and variance $σ^2 = npq = np(1 − p)$. Also recall that `pnorm(q,mean,sd)=P (Y ≤ q)`, where `Y ∼ N (µ =mean; σ2=sd2)`.

- (a) `pnorm(60, mean=54, sd=37.8) - pnorm(q=49, mean=54, sd=37.8)`
- (b) `pnorm(q=60, mean=54, sd=sqrt(37.8)) - pnorm(q=49, mean=54, sd=sqrt(37.8))`
- (c) `pnorm(q=54, mean=54, sd=sqrt(37.8))`
- (d) `pnorm(q=60-50, mean=54, sd=sqrt(37.8))`
- (e) `pnorm(q=60, mean=180, sd=sqrt(37.8)) - pnorm(49, mean=180, sd=sqrt(37.8))`


Scaling rule: $\mathrm{Var}(aY)=a^2\mathrm{Var}(Y)$

For independent variables: $\mathrm{Var}\left(\sum X_i\right)=\sum \mathrm{Var}(X_i)$

Yes — you can make it much faster than re-plugging into ($\binom{n}{k}p^k q^{n-k}$) four separate times.

Here ($X \sim \text{Bin}(n=11,p=\tfrac16)$), ($q=\tfrac56$), and you want ($P(X\le 3)$).

Fast pen-and-paper method: compute (P(0)) once, then recurse
Start with
$$[
P(0)=q^{11}=\left(\frac56\right)^{11}.
]$$

Then use the ratio
$$[
\frac{P(k+1)}{P(k)}=\frac{n-k}{k+1}\cdot\frac{p}{q}.
]$$
So
$$[
P(k+1)=P(k)\left(\frac{n-k}{k+1}\right)\left(\frac{p}{q}\right).
]$$

For this problem, ($\frac{p}{q}=\frac{1/6}{5/6}=\frac15$).

($P(0)=\left(\frac56\right)^{11}$)
($P(1)=P(0)\cdot \frac{11}{1}\cdot\frac15 = P(0)\cdot\frac{11}{5}$)
($P(2)=P(1)\cdot \frac{10}{2}\cdot\frac15 = P(1)\cdot 1$) (nice simplification!)
($P(3)=P(2)\cdot \frac{9}{3}\cdot\frac15 = P(2)\cdot\frac35$)
So the sum is quick:
$$[
P(X\le 3)=P(0)+P(1)+P(2)+P(3)
= P(0)\left(1+\frac{11}{5}+\frac{11}{5}+\frac{11}{5}\cdot 1\cdot\frac35\right).
]$$

If you want a clean exact-number shortcut, factor the common denominator (6^{11}):
$$[
P(X\le 3)=\frac{5^{11}+11\cdot 5^{10}+55\cdot 5^9+165\cdot 5^8}{6^{11}}
=\frac{5^8(125+275+275+165)}{6^{11}}
=\frac{328{,}125{,}000}{362{,}797{,}056}\approx 0.9044.
]$$

Fastest if calculators/R are allowed
In R: `pbinom(3, size=11, prob=1/6)`.

Quick approximation (if they allow approximations)
Since (np=11/6\approx 1.833) is small, Poisson((\lambda=np)) gives a decent estimate:
[
P(X\le 3)\approx e^{-\lambda}\left(1+\lambda+\frac{\lambda^2}{2}+\frac{\lambda^3}{6}\right).
]
But on an exact-probability question, the recursion method above is the best “by hand” speedup.

If you want, I can show how to do the recursion with minimal arithmetic on a basic calculator (basically 2–3 multiplications per step).