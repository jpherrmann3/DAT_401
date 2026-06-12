# Exam 2 Practice Solutions

## Problem 1

The alternative hypothesis for part (a) is:

$$
H_1 < 20
$$

Rational: We want to see test if the drying time decreased. To flip it, we want to test if the distribution of current paint drying times explains the new paint drying times with our desired p value. Since we only care if time decreases, this is a single tailed tests, specifically left tail.

The alternative hypothesis for part (b) is:

$$
H_1 > 20
$$

Rational: To see if drying time increased, we want to test the right tail. Our null hypothesis is that drying times are either the same or decreased. In order to reject the null, the drying time increase must not be explained by the current distribution and fail the right side tail test.

## Problem 2

Part (a)

$$
H_0: \theta = 0.8
$$

The composite null is H0 >= .8 (ie at least 80% shooting would satisfy the requirement). Worst case, he shoots "exactly 80%"

$$
H_1: \theta < 0.8
$$

Since he is "bragging" we need to show that he shoots less than 80%. Greater than or equal to it would prove his point.

Part (b)

(iii) is the right answer

Part (c)

Since we have a discrete variable (a shot can either be made or miss), we have a binomial distribution.

The pmf for binomial would be:

$$
pmf = \left(\begin{array}{c}n\\x\end{array}\right)p^x(1-p)^{n-x}
$$

To calculate the type I error (rejecting the null when we shouldn't have), we would take the sum of the probability mass function. In this case:

$$
\alpha = \sum_{x=0}^{k}\left(\begin{array}{c}50\\x\end{array}\right)0.8^x(0.2)^{50-x}
$$

Part (d)

$$
p = \sum_{x=0}^{32}\left(\begin{array}{c}50\\x\end{array}\right)0.8^x(0.2)^{50-x}
$$

## Problem 3

Since $\bar{x} > 12.6$, she would reject the null. Now we will check the two parts to see what error occurs.

Part (a)
Since $\mu \ne 12.3$, she is correct to reject the null. No Error

Part(b)
Since $\mu = 12.3$, she is incorrect to reject the null. Thus a Type I error.

## Problem 4

Since we don't know the population standard deviation, we must use the t-distribution:

$$
E = \frac{t \cdot s}{\sqrt{n}}
$$

Since it is double sided, we will use the first t-value because:

- $p = \frac{1}{2}\alpha$ and $\alpha = 1 - 0.95$ (our confidence level)
- $df = n - 1= 10 - 1 = 9$
- lower.tail should be false as we should the top .25 of the distribution, not the bottom.

The t value is $2.2621572$. Plugging that into our formula, we get:

$$
E = \frac{2.2621572 \cdot 0.29}{\sqrt{10}}\\
= 0.2074535061
$$

Taking it around the sample mean, we get:

$$
\text{Upper Bound} = 5.68 + 0.2074535061 = 5.887453506 \\
\text{Lower Bound} = 5.68 - 0.2074535061 = 5.472546494
$$

Making our confidence interval about [5.8875, 5.4725]

## Problem 5

n = 300

x = 102

$\hat{p}= 102/300 = 0.34$

$$
ME = z \cdot \sqrt{\frac{\hat{p}(1-\hat{p})}{n}} \\

0.05 = z \cdot \sqrt{\frac{.34(1-.34)}{300}} \\

0.05 = z \cdot 0.0273495887 \\

\frac{0.05}{0.0273495887} = z \\

z = 1.82818

$$

This corresponds to a confidence level of .96784 using the z table. Since this is a 2 sided test, we need to take the confidence level, multiple it by 2 and subtract from 1 to get the p value:
$$
p = 1 - 2(1 - 0.96784) = 0.93568
$$

## Problem 6

Here we are given the population standard deviation $\sigma = 10^6$. The ME is given at $0.5 \cdot 10^6$, and a confidence level of 95%.

Since we know the population standard devation we can use the z score for 95% confidence, which is $1.959964$ (given in the problem with the r function `qnorm`).

the ME function is:

$$
ME = z \cdot \frac{\sigma}{\sqrt{n}}
$$

We can rearrange this to solve for n:

$$
\sqrt{n} = z \cdot \frac{\sigma}{ME} \\
n = \left(z \cdot \frac{\sigma}{ME}\right)^2
$$

Plugging in the numbers:

$$
n = \left(1.959964 \cdot \frac{10^6}{0.5 \cdot 10^6}\right)^2 \\
n = 15.36583553
$$

Since we can't take a fraction of a measurement, we need to round up to the nearest whole number, which is 16 measurements.

## Problem 7

The likelihood function is:
$$
L(\theta) = \prod_{i=1}^n P(X = x_i) = \prod_{i=1}^n (1-\theta)^{x_i - 1} \cdot \theta
$$

To find the MLE, we can take the log of the likelihood function and then take the derivative with respect to $\theta$ and set it equal to 0.

$$
\log L(\theta) = \sum_{i=1}^n \log((1-\theta)^{x_i - 1} \cdot \theta) \\
= \sum_{i=1}^n (x_i - 1) \log(1-\theta) + \sum_{i=1}^n \log(\theta) \\
= (n - \sum_{i=1}^n x_i) \log(1-\theta) + n \log(\theta)
$$
Taking the derivative with respect to $\theta$:
$$
\frac{d}{d\theta} \log L(\theta) = (n - \sum_{i=1}^n x_i) \cdot \frac{-1}{1-\theta} + n \cdot \frac{1}{\theta} \\
= \frac{n - \sum_{i=1}^n x_i}{1-\theta} + \frac{n}{\theta}
$$
Setting this equal to 0 and solving for $\theta$:

$$
\frac{n - \sum_{i=1}^n x_i}{1-\theta} + \frac{n}{\theta} = 0 \\
\frac{n - \sum_{i=1}^n x_i}{1-\theta} = -\frac{n}{\theta} \\
\theta (n - \sum_{i=1}^n x_i) = -n (1-\theta) \\
\theta n - \theta \sum_{i=1}^n x_i = -n + n\theta \\
\theta n - \theta \sum_{i=1}^n x_i - n\theta = -n \\
-\theta \sum_{i=1}^n x_i = -n \\
\theta = \frac{n}{\sum_{i=1}^n x_i}
$$

## Problem 9

Let $X_1,\dots,X_n$ be iid from a Gamma distribution with shape $k=4$ and scale $\theta>0$:

$$
f(x;\theta)=\frac{1}{\Gamma(k)\theta^k}x^{k-1}e^{-x/\theta},\qquad x>0.
$$

You observe the sample $n=8$:
[2.3, 1.8, 3.1, 2.7, 2.0, 1.5, 2.9, 3.4].

Tasks (try these and then tell me your answers):
1. Derive the MLE $\hat{\theta}_{MLE}$ symbolically in terms of the sample.
2. Compute the numeric value of $\hat{\theta}_{MLE}$ for the given sample (show your work).


