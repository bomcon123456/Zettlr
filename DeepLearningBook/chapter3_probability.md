1. What are the 3 possible sources of uncertainty:

- Inherent stochasticity in the system being model (E.g: qubit)
- Incomplete observability (e.g: Monty Hall problem)
- Incomplete modeling

2. What is frequentist probability?
- It's the probability related directly to the rates at which events occurs (e.g: how many time does the coin turn head)

3. What is Bayesian probability?
\- It's the probability related to qualitative levels of certainty (e.g: you have 50% to suceed)

4. What is the standard deviation?
-  $std = \sqrt{Var}$ 

5. What is Laplace distribution?
- $Laplace(x;\mu ; \gamma) = \frac{1}{2 \gamma}exp(-\frac{|x- \mu|}{\gamma})$  

6. To accomplish a probability distribution with a sharp point at $x=0$, which distribution to use?
- Exponential distribution

7. To accomplish a probability distribution with a sharp point at $x= \mu$, which distribution to use?
- Laplace distribution

8. What is Dirac delta function, $\delta(x)$ ?
- $\delta(x)$ is defined such that it is zero-values everywhere except 0
- $\int{\delta(x)dx}=1$ 
- ![5c86461bcc9c135d7adee9f2c7a01b46.png](..\assets\5c86461bcc9c135d7adee9f2c7a01b46.png)
- ![dirac_func](..\assets\Dirac_function_approximation.gif)


9. One common way of combining distributions is to construct a **mixture distribution**. A mixture distribution is made up of several component distributions. On each trial, the choice of which component distribution generates the sample is determined by sampling a component identity from a multinoulli distribution
![mixture_distribution.png](..\assets\mixture_distribution.png)

10. What is latent variable?
- A Latent variable is a random variable that we cannot observe directly.
- E.g: the component identity variable c of the mixture model

11. What is Gaussian mixture?
- When the components $p(x|c=i)$ are Gaussians.
- Every component has a separted mean, covariance.
- **Prior Probability** $\alpha_i = P(c=i)$ given to each component $i$
- **Posterior probability** $P(c|x)$ because it's computed after observation of x
![gaussian_mixture.png](..\assets\gaussian_mixture.png)


12. What does the word "prior" means in prior probability $P(c=i)$ ?
- The word “prior” indicates that it expresses the model’s beliefs about $c$ before it has observed $x$.

13.  Why is $P(c|x)$ call posterior probability?
- Because it's computed after observation of $x$.

14. What is the softplus function?
- $\varsigma = log(1+exp(x))$
- ![softplus.png](..\assets\softplus.png)


15. What is the relation of softplus with max function?
- It's the softened version of $max(0,x)$.

16. What is sigmoid function?
- ![sigmoid.png](..\assets\sigmoid.png)
- ![sigmoid.png](..\assets\sigmoid.png)

17. What is the derivatives of sigmoid?
- ![sigmoid_dev.png](..\assets\sigmoid_dev.png)

18. Should know:
![good_statistics_equations.png](..\assets\good_statistics_equations.png)
