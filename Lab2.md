# Lab 2


#### Question 1.

Suppose Curtis collected data on the stop light on 19th and main. In
particular, he took 70 trips through the intersection and recorded
whether the light was green (success) or not.

##### 1.1 Specify, plot, and justify a beta prior that matches your belief about the probability that you will have a green light at the intersection. (4 points)

##### 1.2 Assume Curtis got green lights on 41 of his trips. Use `binom.test()` to report an MLE and 95% uncertainty interval for the proportion of green lights (4 points)

##### 1.3 Update your figure from Q1.1 to add the posterior distribution while keeping the prior distribution, given 41 green lights. Include a 95 uncertainty interval on the figure. (4 points)

##### 1.4 Assume others used the following prior distributions. Create a figure (faceted or overlaid curves?) showing the priors and posteriors in these situations (4 points)

- Beta(.01, .01)
- Beta(1, 1)
- Beta(7, 3)
- Beta(3, 7)
- Beta(70, 30)
- Beta(30, 70)

##### 1.5 Given the results from the previous questions, which method of estimation and uncertainty interval do you prefer? (4 points)

#### Question 2.

During lab 1, we all rolled a die at the beginning of class.

     [1] 6 2 6 2 2 2 6 3 3 6 6 1

The rolls ended up with the following outcomes 6, 2, 6, 2, 2, 2, 6, 3,
3, 6, 6, 1. We stated that a multinomial distribution could be used to
model these outcomes.

##### 2.1 What are are the parameters in the multinomial distribution? How do we interpret these parameters? (2 points)

##### 2.2 Assume that we will use a Dirichlet prior distribution with all $\alpha_i = 1$. What would be your prior mean for all of the parameters in the multinomial distribution? (2 points)

##### 2.3 Given the Dirichlet prior distribution specified in Q2.2 and the collected data, what are the posterior means for the model parameters? (4 points)

##### 2.3 Construct 95% uncertainty intervals for each of the parameters. Hint: we can take samples using `rdirichlet` from `MCMCpack` and summarize those samples to construct uncertainty intervals. (4 points)

##### 2.4 Do you think it is likely that we are using fair dice (equal probability of rolling any number)? Why or why not? (2 points)

##### 2.5 What are the MLE estimates of the parameters in the model? (2 points)
