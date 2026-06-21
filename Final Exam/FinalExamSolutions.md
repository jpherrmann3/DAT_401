# Final Exam Solutions

1. To determine independence of events, we can calculate the probabilities of the events and their intersections.

- P(A) = 3/6 = 1/2 (since there are 3 even numbers on a die)
- P(B) = 3/6 = 1/2 (since there are 3 odd numbers on a die)
- P(C) = 2/6 = 1/3 (since there are 2 even numbers greater than 3 on a die)
- P(D) = 6/36 = 1/6 (since there are 6 outcomes where the two dice show the same number)
- P(A ∩ D) = 3/36 = 1/12 (since there are 3 outcomes where the first die shows an even number and both dice show the same number)
- P(B ∩ D) = 3/36 = 1/12 (since there are 3 outcomes where the first die shows an odd number and both dice show the same number)
- P(C ∩ D) = 2/36 = 1/18 (since there are 2 outcomes where the second die shows an even number greater than 3 and both dice show the same number)

Now we can check for independence:

- P(A ∩ D) = P(A) * P(D) = (1/2) * (1/6) = 1/12 (independent)
- P(B ∩ D) = P(B) * P(D) = (1/2) * (1/6) = 1/12 (independent)
- P(C ∩ D) = P(C) * P(D) = (1/3) * (1/6) = 1/18 (independent)

Therefore, the correct answer is (b) A & D are independent, and so are B & D, as well as C & D.

2. Is a Bayes' theorem problem. We want to find P(Spam | Marked as Spam). First we can record the probabilities we do know:

- P(Spam) = 0.11
- P(Not Spam) = 0.89
- P(Marked as Spam | Spam) = 0.95
- P(Marked as Spam | Not Spam) = 0.04

Bayes' theorem states that:

P(A | B) = (P(B | A) * P(A)) / P(B)

Applying our probabilities to this formula, we get:

P(Spam | Marked as Spam) = (P(Marked as Spam | Spam) * P(Spam)) / P(Marked as Spam)

Using the total probability theorem, we can find P(Marked as Spam):

P(Marked as Spam) = P(Marked as Spam | Spam) * P(Spam) + P(Marked as Spam | Not Spam) * P(Not Spam)
                   = (0.95 * 0.11) + (0.04 * 0.89)
                   = 0.1045 + 0.0356
                   = 0.1401

Therefore, P(Spam | Marked as Spam) = (0.95 * 0.11) / 0.1401 = 0.746.

3. Another Bayes' thereom problem. We need to find P(Disease | Positive Test). First we can record the probabilities we do know:

P(Disease) = 0.005
P(Healthy) = 0.995
P(Positive Test | Disease) = 0.95
P(Positive Test | Healthy) = 0.01

Using Bayes' theorem, we can find P(Disease | Positive Test):

P(Disease | Positive Test) = (P(Positive Test | Disease) * P(Disease)) / P(Positive Test)

Using the total probability theorem, we can find P(Positive Test):

P(Positive Test) = P(Positive Test | Disease) * P(Disease) + P(Positive Test | Healthy) * P(Healthy)
                   = (0.95 * 0.005) + (0.01 * 0.995)
                   = 0.00475 + 0.00995
                   = 0.0147

Therefore, P(Disease | Positive Test) = (0.95 * 0.005) / 0.0147 = 0.323.

4. To find the posterior distribution, we can use Bayes' theorem for continuous distributions:

$$
\pi(\theta | x) = \frac{P(X = x | \theta) \pi(\theta)}{P(X = x)}
$$

The likelihood function P(X = x | θ) for a binomial distribution is given by:
$$
P(X = x | \theta) = \binom{n}{x} \theta^x (1 - \theta)^{n - x}
$$
The prior distribution π(θ) is given by the Beta distribution:
$$
\pi(\theta) = \frac{1}{B(\alpha, \beta)} \theta^{\alpha - 1} (1 - \theta)^{\beta - 1}
$$
The marginal likelihood P(X = x) can be calculated by integrating the product of the likelihood and the prior over all possible values of θ:
$$
P(X = x) = \int_0^1 P(X = x | \theta) \pi(\theta) d\theta
$$
This integral can be solved using the properties of the Beta distribution, and it turns out that the posterior distribution π(θ | x) is also a Beta distribution with updated parameters:
$$
\pi(\theta | x) = Beta(\alpha + x, \beta + n - x)
$$
Therefore, the posterior distribution is still a Beta distribution with parameters α + x and β + n - x.

5. To find the maximum likelihood estimate (MLE) of the parameter θ for an exponential distribution, we can write down the likelihood function based on the given probability density function (PDF):

$$
\hat{\theta}_{MLE} = \arg\max_{\theta} L(\theta) = \arg\max_{\theta} \prod_{i=1}^{n} f(x_i; \theta)
$$

The likelihood function for the exponential distribution is given by:
$$
L(\theta) = \prod_{i=1}^{n} \theta e^{-\theta x_i} = \theta^n e^{-\theta \sum_{i=1}^{n} x_i}
$$

To find the MLE, we can take the natural logarithm of the likelihood function to simplify the calculations:
$$
\ln L(\theta) = n \ln \theta - \theta \sum_{i=1}^{n} x_i
$$
Next, we can take the derivative of the log-likelihood function with respect to θ and set it equal to zero to find the critical points:
$$
\frac{d}{d\theta} \ln L(\theta) = \frac{n}{\theta} - \sum_{i=1}^{n} x_i = 0
$$
Solving for θ gives us:
$$
\hat{\theta}_{MLE} = \frac{n}{\sum_{i=1}^{n} x_i}
$$
Therefore, the maximum likelihood estimate of the parameter θ for the exponential distribution is given by the formula above.

6. (a) To compute a 95% confidence interval for the true percent of accounts receivable that are more than 30 days overdue, we can use the formula for a confidence interval for a proportion:
$$
CI = \hat{p} \pm z \sqrt{\frac{\hat{p}(1 - \hat{p})}{n}}
$$
Where:
- $\hat{p}$ is the sample proportion (300/500 = 0.6)
- $z$ is the z-score corresponding to the desired confidence level (for 95%, z ≈ 1.96)
- $n$ is the sample size (500)
- Calculating the confidence interval:
$$
CI = 0.6 \pm 1.96 \sqrt{\frac{0.6(1 - 0.6)}{500}}
$$
$$
CI = 0.6 \pm 1.96 \sqrt{\frac{0.24}{500}}
$$
$$
CI = 0.6 \pm 1.96 \sqrt{0.00048}
$$
$$
CI = 0.6 \pm 1.96 \times 0.0219
$$
$$
CI = 0.6 \pm 0.0429
$$
Therefore, the 95% confidence interval for the true percent of accounts receivable that are more than 30 days overdue is approximately (0.5571, 0.6429).

(b) To find the smallest sample size $n$ for which the officer would obtain margin of error at most of 0.01, with a confidence level of 95%, we can rerrange the formula for the margin of error:

$$
ME = z \sqrt{\frac{\hat{p}(1 - \hat{p})}{n}}
$$
Rearranging for $n$:
$$
n = \left( \frac{z}{ME} \right)^2 \hat{p}(1 - \hat{p})
$$
Substituting the known values:
$$
n = \left( \frac{1.96}{0.01} \right)^2 (0.6)(0.4) = 9219.84
$$
Therefore, the smallest sample size required is approximately 9220.