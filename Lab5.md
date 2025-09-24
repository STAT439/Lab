# Lab 5


#### Part 1. Logistic Regression with a categorical predictor

Following the thread from the activity on Tuesday, we will consider a
case where we have a binary outcome and a categorical predictor with
three levels.

There are two formulations of this model, the first is known as the
reference case model. In this formulation the $\beta$ coefficients
correspond to differences from the reference case class.

The second is the cell means model which can more directly estimate
probabilities associated with each class.

### 1. Data Simulation (6 points)

Use the cell means model and simulate data with the following properties

- Let there be a total of 150 observations, 50 from `x = "1"`, 50 from
  $x = ``2"$, and 50 from $x = ``3"$.

- Set the coefficient values to the following values:$\beta_0$ = 0,
  $\beta_1 = 1$, and $\beta_2 = -1$.

- Simulate a binary outcome at each x value.

- Create a plot that displays the pi values along with observed binary
  responses.

### 2. Contingency Table (6 points)

Using your simulated data, print a contingency table and determine
whether you’d detect any association between the two variables (binary
outcome and categorical predictor).

### 3. Model fitting (6 points)

Fit your data using either an MLE or Bayesian approach, report point
estimates and uncertainty intervals for the beta values. Hint, you can
get the cell means coding with `y ~ x - 1`

### 4. Probability Scale (6 points)

With this model framework, we can also directly estimate uncertainty
intervals for the probabilities using $\pi = logit^{-1}(\beta)$. Compute
uncertainty intervals for the probability of success for each class and
add them to an updated version of the figure from part 1.

### 5. Alternative Models (6 points)

Why do the two models below give you incorrect results?

``` r
model.fit <- glm(y ~ as.numeric(x) - 1, data = log_data, family = binomial)
model.fit <- glm(y ~ x - 1, data = log_data)
```
