# Course-introduction-to-stat-with-python

### Course Takeaways: Introduction to Statistics in Python

#### I. What's the Chance
**Example:**
- **Coin Flip**: Calculating the probability of flipping heads on a fair coin.
  - Probability Formula: \( P(\text{event}) = \frac{\text{# ways event can happen}}{\text{total # of possible outcomes}} \)
  - For a coin flip: \( P(\text{heads}) = \frac{1}{2} = 50\% \)

**Python Application:**
- **Assigning Salespeople**:
  - Calculate the probability of assigning a specific salesperson.
  - For Brian: \( P(\text{Brian}) = \frac{1}{4} = 25\% \)
  - Example in Python:
    ```python
    import pandas as pd
    sales_counts = pd.DataFrame({'name': ['Amir', 'Brian', 'Claire', 'Damian'], 'n_sales': [178, 128, 75, 69]})
    print(sales_counts.sample())
    ```

#### II. Discrete & Continuous Distributions
**Definition:**
- **Discrete Distribution**: Describes the probability of each possible outcome in a scenario with distinct, separate values (e.g., rolling a die).
- **Continuous Distribution**: Describes the probability of outcomes in a continuous range (e.g., waiting time for a bus).

**Examples:**
- **Discrete Distribution**:
  - Rolling a fair die.
  - Expected value of a fair die roll: \( \frac{1+2+3+4+5+6}{6} = 3.5 \)
  - Python:
    ```python
    die = pd.DataFrame({'number': [1, 2, 3, 4, 5, 6], 'prob': [1/6]*6})
    np.mean(die['number'])
    ```
- **Continuous Distribution**:
  - Waiting time for a bus uniformly distributed between 0 and 12 minutes.
  - Probability \( P(4 \leq \text{wait time} \leq 7) \):
    ```python
    from scipy.stats import uniform
    uniform.cdf(7, 0, 12) - uniform.cdf(4, 0, 12)
    ```

#### III. Binomial Distribution
**Definition:**
- The binomial distribution is the probability distribution of the number of successes in a sequence of independent trials, each with the same probability of success.

**Example:**
- **Coin Flipping**:
  - Probability of getting exactly 7 heads in 10 flips of a fair coin:
    ```python
    from scipy.stats import binom
    binom.pmf(7, 10, 0.5)
    ```
  - Probability of getting 7 or fewer heads in 10 flips:
    ```python
    binom.cdf(7, 10, 0.5)
    ```

#### IV. Python Functions
**Definition & Example of Each:**

- **Probability Mass Function (PMF)**:
  - **Definition**: The PMF gives the probability that a discrete random variable is exactly equal to some value.
  - **Example**: Probability of 7 heads in 10 coin flips:
    ```python
    from scipy.stats import binom
    binom.pmf(7, 10, 0.5)
    ```

- **Cumulative Distribution Function (CDF)**:
  - **Definition**: The CDF gives the probability that a random variable is less than or equal to a certain value.
  - **Example**: Probability of getting 7 or fewer heads in 10 coin flips:
    ```python
    binom.cdf(7, 10, 0.5)
    ```

- **Random Variate Sampling (RVS)**:
  - **Definition**: The RVS function generates random numbers according to a specified probability distribution.
  - **Example**: Generating 10 random numbers from a uniform distribution between 0 and 5:
    ```python
    from scipy.stats import uniform
    uniform.rvs(0, 5, size=10)
    ```
  - Generating random outcomes for binomial distribution:
    ```python
    from scipy.stats import binom
    binom.rvs(3, 0.5, size=10)
    ```


    ### V. Python Functions: Explanation of Arguments

#### 1. Probability Mass Function (PMF)
**Function: `binom.pmf(k, n, p)`**

- **Arguments:**
  - `k`: The number of successes (integer). This is the specific value at which you want to evaluate the PMF.
  - `n`: The number of trials (integer). This is the total number of independent trials or experiments.
  - `p`: The probability of success on each trial (float). This value should be between 0 and 1.

**Example:**
```python
from scipy.stats import binom
# Probability of getting exactly 7 heads in 10 coin flips
prob = binom.pmf(7, 10, 0.5)
print(prob)
```

#### 2. Cumulative Distribution Function (CDF)
**Function: `binom.cdf(k, n, p)`**

- **Arguments:**
  - `k`: The number of successes (integer). This is the specific value up to which you want to evaluate the cumulative probability.
  - `n`: The number of trials (integer). This is the total number of independent trials or experiments.
  - `p`: The probability of success on each trial (float). This value should be between 0 and 1.

**Example:**
```python
from scipy.stats import binom
# Probability of getting 7 or fewer heads in 10 coin flips
cumulative_prob = binom.cdf(7, 10, 0.5)
print(cumulative_prob)
```

#### 3. Random Variate Sampling (RVS)
**Function: `uniform.rvs(loc=0, scale=1, size=1)` and `binom.rvs(n, p, size=1)`**

- **Uniform Distribution (`uniform.rvs`)**:
  - **Arguments:**
    - `loc`: The lower bound of the distribution (float). This is the starting point of the distribution.
    - `scale`: The width of the distribution (float). This determines the range over which values are uniformly distributed.
    - `size`: The number of random variates to generate (integer or tuple of integers). This defines the shape of the output array.
    
  **Example:**
  ```python
  from scipy.stats import uniform
  # Generating 10 random numbers from a uniform distribution between 0 and 5
  random_numbers = uniform.rvs(loc=0, scale=5, size=10)
  print(random_numbers)
  ```

- **Binomial Distribution (`binom.rvs`)**:
  - **Arguments:**
    - `n`: The number of trials (integer). This is the total number of independent trials or experiments.
    - `p`: The probability of success on each trial (float). This value should be between 0 and 1.
    - `size`: The number of random variates to generate (integer or tuple of integers). This defines the shape of the output array.

  **Example:**
  ```python
  from scipy.stats import binom
  # Generating random outcomes for 10 trials of a binomial distribution with n=3 and p=0.5
  random_outcomes = binom.rvs(n=3, p=0.5, size=10)
  print(random_outcomes)
  ```

These explanations detail the arguments for each function used in the course, providing clarity on how to use them in various statistical analyses.

These takeaways provide a concise summary of the key concepts, examples, and Python applications covered in the course on Introduction to Statistics in Python.
