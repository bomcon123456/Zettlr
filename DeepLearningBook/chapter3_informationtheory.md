1. To quantify information, what rules do we use:
- Likely events should have low information content, and in the extreme case, events that are guaranteed to happen should have no information content whatsoever
- Less likely events should have higher information content.
-  Independent events should have additive information. For example, finding out that a tossed coin has come up as heads twice should convey twice as much information as finding out that a tossed coin has come up as heads once.

2. In order to satisty 3 properties to quantify information, how we define self-information of an event $x = x$ ?
- $I(x) = -logP(x)$ 
- Units: $nats$ if  $log = ln$; $bits; shannons$ if $log = log_2$

3. What is nat?
- The amount of information gained by observing an event of probability $\frac{1}{e}$.

4. How can we quantify the amount of uncertainty in an entire probability distribution?
- Use Shannon entropy: $H(P) = H(x) = E_{x \sim P}[I(x)] = -E_{x \sim P}[logP(x)]$. 

5. The Shannon entropy of a distribution 
- Is the expected amount of information in an event drawn from that distribution.
- Gives a lower bound on the number of bits (if the logarithm is base 2, otherwise the units are different) needed on average to encode symbols drawn from a distribution $P$.

6. Distributions that are nearly deterministic (where the outcome is nearly certain) have low entropy; distributions that are closer to uniform have high entropy.
![shannon_entropy.png](..\assets\shannon_entropy.png)

7. When x is continuous, the Shannon entropy is known as the **differential entropy**.
8. When we want to measure how diffirent two seperate probability function $P(x); Q(x)$ over the same random variable $x$, what do we use?
- ![KL_divergence.png](..\assets\KL_divergence.png)
9. What is the meaning of the value we get from KL Divergence?
- In the case of discrete variables, it is the extra amount of information (measured in bits if we use the base 2 logarithm, but in machine learning we usually use nats and the natural logarithm) needed to send a message containing symbols drawn from probability distribution $P$, when we use a code that was designed to minimize the length of messages drawn from probability distribution $Q$.
10. Properties of KL Divergence:
- Nonnegative.
- Not symmetric.
- The KL divergence is 0 if and only if P and Q are the same distribution in the case of discrete variables, or equal “almost everywhere” in the case of continuous variables. 
- Often conceptualized as measuring some sort of distance between these distributions (not true distance since it's not symmetric).
- Important consequences to the choice of whether to use  $D_{KL}(P||Q); D_{KL}(Q||P)$.
- ![kl_divergence_diff.png](..\assets\kl_divergence_diff.png)


11. What is cross-entropy?
- $H(P,Q) = H(P) + D_{KL}(P||Q) = -E_{x \sim P}\log Q(x)$. 