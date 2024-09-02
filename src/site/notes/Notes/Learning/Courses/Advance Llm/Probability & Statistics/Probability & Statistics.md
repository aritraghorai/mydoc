---
{"dg-publish":true,"permalink":"/notes/learning/courses/advance-llm/probability-and-statistics/probability-and-statistics/","title":"Probability & Statistics Index"}
---

## Notes
- [Week 1](https://d3c33hcgiwev3.cloudfront.net/GbR11MUHS_yDIqO7aTHkLg_b962c2adf46f40238483044966e6b7f1_M4ML-C3-W1.pdf?Expires=1725062400&Signature=MJ-u~~-cVeRp9jJ~tNlvasX3IudG5K0eynuv0l1uZeoELid320D~K~BUtvHm0U2f0-dooQjisFhi3~7Xn7G3a9M60Q1lsx55dvzZ0nB3bIdCZKADfKMGwTa1iOelBzOt3YU73UUVq~g28V7qbmU8-E4F88sqcuzGzMlfBfxEwzk_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
- [Week 2](https://d3c33hcgiwev3.cloudfront.net/AOiQfHCySw6mzx9zD2nPXg_d50535afb5ef4bb38d8655009de4b8f1_M4ML-C3-W2.pdf?Expires=1725148800&Signature=HdEtoyMe3xToOCoH-HL5-ztMl0ODUgr5aUj3u1teQ5yHEJwY1-~xpLGhgwfOPMRdgDk~4fOMiMZ8wxbgxoy~33v8ERuBUr~Hktgxr1j0uz-7pnzrQB238-H4TMkoouwJNOAI0i7zYeZYP~vOQjBUWamqFTny3D38qzyfC2iylC4_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)

##  What is Probability?
**Probability** is a branch of mathematics that deals with the likelihood or chance of different outcomes occurring in a random event. It quantifies uncertainty and measures how likely it is for a specific event to happen.

The probability of an event is a number between 0 and 1, where:
- **0** indicates an impossible event.
- **1** indicates a certain event.
- A probability closer to 0 means the event is less likely to occur, while a probability closer to 1 means it is more likely to occur.

### Key Concepts in Probability:

1. **Experiment**: A process or action that produces a set of results. For example, rolling a die or flipping a coin.
   
2. **Outcome**: A possible result of an experiment. For example, getting a 3 when rolling a die.
   
3. **Event**: A set of one or more outcomes. For example, getting an odd number when rolling a die (which includes the outcomes 1, 3, and 5).

4. **Sample Space (S)**: The set of all possible outcomes of an experiment. For a die, the sample space is {1, 2, 3, 4, 5, 6}.

5. **Probability of an Event (P(E))**: The ratio of the number of favourable outcomes to the total number of outcomes in the sample space. Mathematically, it's expressed as:
  $$
   
   P(E) = \frac{\text{Number of favorable outcomes}}{\text{Total number of outcomes in the sample space}}
$$

### Types of Probability:

1. **Theoretical Probability**: Based on the reasoning behind probability. It is calculated by analyzing the possible outcomes of an experiment without actually performing the experiment. 

2. **Experimental Probability**: Based on actual experiments or trials. It is calculated by conducting an experiment and recording the outcomes.

3. **Subjective Probability**: Based on personal judgement, experience, or intuition rather than on systematic calculation or experimentation.

### Example:

If you toss a fair coin, there are two possible outcomes: heads (H) or tails (T). The probability of getting heads is:
$$\
P(\text{Heads}) = \frac{1}{2}
\
$$
since there is one favourable outcome (getting heads) and two possible outcomes (heads or tails).

## Complement of probability
![Probability & Statistics.png](/img/user/assets/Probability%20&%20Statistics.png)

## Sum of probability(Disjoint Event)
![[Pasted image 20240828153759.png\|Pasted image 20240828153759.png]]

## Sum of Probability (Joined event)
![Probability & Statistics-2.png](/img/user/assets/Probability%20&%20Statistics-2.png)
![Probability & Statistics-3.png](/img/user/assets/Probability%20&%20Statistics-3.png)

## Disjoint(Mutually Exclusive) vs Joined Event
![Probability & Statistics-4.png](/img/user/assets/Probability%20&%20Statistics-4.png)

![Probability & Statistics-5.png](/img/user/assets/Probability%20&%20Statistics-5.png)

## Product Rule Independent Event
![Probability & Statistics-6.png](/img/user/assets/Probability%20&%20Statistics-6.png)

***If Event are independent then the probability is the product of all the event***

## Conditional Probability
![Probability & Statistics Conditional.png](/img/user/assets/Probability%20&%20Statistics%20Conditional.png)

***A condition can chance the probability completely***


Conditional probability is the probability of an event occurring given that another event has already occurred. It helps us understand how the likelihood of an event changes when we know that a related event has taken place.

Mathematically, the conditional probability of event **A** given event **B** is denoted as **P(A | B)** and is calculated using the formula:
$$
\
P(A | B) = \frac{P(A \cap B)}{P(B)}
\

$$
where:

- **P(A ∩ B)** is the probability that both events **A** and **B** occur.
- **P(B)** is the probability that event **B** occurs.

**Key Points:**

1. **Dependent Events**: Conditional probability applies to situations where the occurrence of one event affects the probability of another.
   
2. **Bayes' Theorem**: Conditional probability is a fundamental concept used in Bayes' theorem, which relates the conditional and marginal probabilities of random events.

3. **Example**: If you have a deck of cards and want to know the probability of drawing an ace given that you have drawn a spade, conditional probability would help calculate this. There are 13 spades, and only one of them is an ace, so:
$$
P(\text{Ace | Spade}) = \frac{P(\text{Ace} \cap \text{Spade})}{P(\text{Spade})} = \frac{1/52}{13/52} = \frac{1}{13}.
\
$$

Understanding conditional probability is essential in statistics, machine learning, and many fields that deal with uncertainty and data.

## Bayes Theorem

Bayes' theorem is a fundamental concept in probability theory and statistics that describes how to update the probability of a hypothesis based on new evidence. It's particularly useful in scenarios where you need to revise probabilities given new data. 

The formula for Bayes' theorem is:
$$
\
P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}
\

$$
Where:
- \(P(A|B)\) is the **posterior probability**: the probability of event \(A\) occurring given that \(B\) is true.
- \(P(B|A)\) is the **likelihood**: the probability of event \(B\) occurring given that \(A\) is true.
- \(P(A)\) is the **prior probability**: the initial probability of event \(A\) before taking into account any evidence.
- \(P(B)\) is the **marginal likelihood**: the total probability of event \(B\) occurring under all possible scenarios.

### Example of Using Bayes' Theorem

Let's consider an example to illustrate Bayes' theorem:

Suppose there is a medical test for a disease that has a 99% accuracy rate. The probability of having the disease (prior probability \(P(A)\)) is 0.1%. The probability of the test returning a positive result when a person actually has the disease (likelihood \(P(B|A)\)) is 99%, and the probability of a false positive (test is positive when the person doesn't have the disease) is 5%.

We want to find out the probability that a person actually has the disease given that they tested positive (posterior probability \(P(A|B)\)).

Given:
$$
 (P(A) = 0.001)
$$
$$
(P(B|A) = -1.99)
$$
$$
(P(B|\text{not } A) = 0.05)
$$
$$
(P(\text{not } A) = 1 - P(A) = 0.999)
$$

First, calculate \(P(B)\):
$$
\
P(B) = P(B|A) \cdot P(A) + P(B|\text{not } A) \cdot P(\text{not } A)
\
$$

$$
\
P(B) = 0.99 \cdot 0.001 + 0.05 \cdot 0.999
\
$$

$$
\
P(B) = 0.00099 + 0.04995 = 0.05094
\
$$

Now, apply Bayes' theorem:

$$
\
P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)} = \frac{0.99 \cdot 0.001}{0.05094}
\
$$

$$
\
P(A|B) \approx \frac{0.00099}{0.05094} \approx 0.0194
\
$$

Thus, the probability that a person actually has the disease given a positive test result is about 1.94%, which is quite low, despite the test's high accuracy. This illustrates how Bayes' theorem takes into account both the accuracy of the test and the rarity of the condition.

## Random Variable
A **random variable** is a variable that represents a numerical outcome of a random phenomenon. In probability theory and statistics, a random variable can take on different values, each with an associated probability. 

There are two main types of random variables:

1. **Discrete Random Variable**: This type of random variable has a finite or countable number of possible values. For example, the number of heads in 10 flips of a coin is a discrete random variable because it can only take on certain integer values (0, 1, 2, ..., 10).

2. **Continuous Random Variable**: This type of random variable has an infinite number of possible values within a given range. For example, the height of a randomly selected person is a continuous random variable because it can take on any value within a range (e.g., 150 cm to 200 cm).

## Probability Distribution
### Probability Mass Function
![Probability & Statistics-7.png](/img/user/assets/Probability%20&%20Statistics-7.png)

### Binomial Distribution
The **Binomial Distribution** is a discrete probability distribution that describes the number of successes in a fixed number of independent trials of a binary experiment (an experiment with only two possible outcomes: success or failure).

#### Key Characteristics of Binomial Distribution

1. **Fixed Number of Trials (n):** The experiment is conducted a set number of times.
2. **Two Possible Outcomes:** Each trial results in either a "success" or a "failure."
3. **Constant Probability of Success (p):** The probability of success is the same for each trial.
4. **Independence:** The trials are independent, meaning the outcome of one trial does not affect the outcome of another.

#### Binomial Probability Formula

The probability of observing exactly \(k\) successes in \(n\) trials is given by the formula:

$$
\
P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}
\
$$

where:

- \(P(X = k)\) is the probability of getting \(k\) successes in \(n\) trials.
- \(n\) is the total number of trials.
- \(k\) is the number of successes.
- \(p\) is the probability of success on any given trial.
- \(1-p\) is the probability of failure.

- $$ (\binom{n}{k} = \frac{n!}{k!(n-k)!}) $$  is the binomial coefficient, representing the number of ways to choose \(k\) successes out of \(n\) trials.

#### Example of Binomial Distribution

Suppose you have a fair coin, and you flip it 10 times. You want to find the probability of getting exactly 4 heads. Here:

- \(n = 10\) (number of trials)
- \(k = 4\) (number of successes, i.e., heads)
- \(p = 0.5\) (probability of getting a head)

The probability of getting exactly 4 heads is:

$$

P(X = 4) = \binom{10}{4} (0.5)^4 (1-0.5)^{10-4}
$$

Calculating further:

$$
P(X = 4) = \frac{10!}{4!(10-4)!} (0.5)^4 (0.5)^6 = 210 \times (0.5)^{10} = 210 \times \frac{1}{1024} \approx 0.205
$$

So, the probability of getting exactly 4 heads in 10 flips of a fair coin is about 0.205 or 20.5%.

#### Applications of Binomial Distribution

- Quality control and reliability testing
- Clinical trials (e.g., probability of a certain number of patients responding to treatment)
- Surveys and opinion polls
- Modelling binary outcomes in various fields (e.g., finance, medicine, social sciences)


### Bernoulli Distribution
The **Bernoulli distribution** is a discrete probability distribution for a random variable that takes on only two possible outcomes: 1 (success) or 0 (failure). It is the simplest type of probability distribution, often used to model binary events such as coin tosses (heads or tails), success/failure scenarios, or yes/no questions.

#### Key Characteristics of the Bernoulli Distribution

- **Random Variable**: \(X\) is a Bernoulli random variable with possible outcomes 1 (success) and 0 (failure).
- **Parameter**: The Bernoulli distribution is defined by a single parameter \(p\), which represents the probability of success (i.e., the event happening).
  $$
  (p = P(X = 1))
$$
  $$
  (1 - p = P(X = 0))
$$
- **Probability Mass Function (PMF)**:

     $$
  P(X = x) = p^x (1 - p)^{1 - x}, \quad x \in \{0, 1\}
$$
  where:
  - \(P(X = 1) = p\)
  - \(P(X = 0) = 1 - p\)

#### Moments of the Bernoulli Distribution

- **Mean (Expected Value)**: 

$$
  E(X) = p
$$
- **Variance**:

$$
  \text{Var}(X) = p(1 - p)
$$
#### Applications of Bernoulli Distribution

The Bernoulli distribution is widely used in scenarios involving binary outcomes. It serves as the foundation for more complex distributions like the Binomial distribution (which models the number of successes in a fixed number of Bernoulli trials). Examples include:

- Modelling coin tosses
- Representing success/failure scenarios in business or clinical trials
- Describing user actions in A/B testing (click vs. no click)


## Describing Distribution
### Mean Or Expected Value
![Probability & Statistics-8.png](/img/user/assets/Probability%20&%20Statistics-8.png)

### Mean and Median,mod Binomial Distribution
![Probability & Statistics Mean Median mod.png](/img/user/assets/Probability%20&%20Statistics%20Mean%20Median%20mod.png)

### Sum of Expected Value
![Probability & Statistics Sum of Expected Value.png](/img/user/assets/Probability%20&%20Statistics%20Sum%20of%20Expected%20Value.png)
### Variance
![Probability & Statistics Varience Motivation.png](/img/user/assets/Probability%20&%20Statistics%20Varience%20Motivation.png)
![Probability & Statistics-9.png](/img/user/assets/Probability%20&%20Statistics-9.png)
![Probability & Statistics-10.png](/img/user/assets/Probability%20&%20Statistics-10.png)



