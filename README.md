### Course Summary: Introduction to Statistics in Python

### Chapter 3 normal distributioin, poisson distribution & expontial distribution

#### I. Normal Distribution
**Concrete Example:**
- **Example Scenario**: The heights of adults in a population typically follow a normal distribution, with most people having heights around the mean and fewer people being much shorter or taller than average.

**Python Function: `scipy.stats.norm`**

1. **norm.cdf()**
   - **Definition**: The cumulative distribution function (CDF) calculates the probability that a random variable from a normal distribution is less than or equal to a certain value.
   - **Example**:
     ```python
     from scipy.stats import norm
     # Probability that a value is less than or equal to 1.96 in a standard normal distribution
     prob = norm.cdf(1.96)
     print(prob)  # Output: 0.9750021048517795
     ```

2. **norm.pdf()**
   - **Definition**: The probability density function (PDF) calculates the probability density of a normal distribution at a given value.
   - **Example**:
     ```python
     from scipy.stats import norm
     # Probability density at value 0 in a standard normal distribution
     density = norm.pdf(0)
     print(density)  # Output: 0.3989422804014327
     ```

3. **norm.rvs()**
   - **Definition**: The random variate sampling (RVS) function generates random numbers from a normal distribution.
   - **Example**:
     ```python
     from scipy.stats import norm
     # Generate 5 random values from a standard normal distribution
     random_values = norm.rvs(size=5)
     print(random_values)
     ```

#### II. Poisson Distribution
**Concrete Example:**
- **Example Scenario**: The number of emails a person receives per hour can be modeled using a Poisson distribution if the emails are received independently and at a constant average rate.

**Python Function: `scipy.stats.poisson`**

1. **poisson.cdf()**
   - **Definition**: The cumulative distribution function (CDF) calculates the probability that the number of events is less than or equal to a certain value.
   - **Example**:
     ```python
     from scipy.stats import poisson
     # Probability of receiving 3 or fewer emails in an hour, given the average rate is 2 emails per hour
     prob = poisson.cdf(3, 2)
     print(prob)  # Output: 0.857123460498547
     ```

2. **poisson.pmf()**
   - **Definition**: The probability mass function (PMF) calculates the probability of a given number of events occurring in a fixed interval.
   - **Example**:
     ```python
     from scipy.stats import poisson
     # Probability of receiving exactly 2 emails in an hour, given the average rate is 2 emails per hour
     prob = poisson.pmf(2, 2)
     print(prob)  # Output: 0.2706705664732254
     ```

3. **poisson.rvs()**
   - **Definition**: The random variate sampling (RVS) function generates random numbers from a Poisson distribution.
   - **Example**:
     ```python
     from scipy.stats import poisson
     # Generate 5 random values from a Poisson distribution with an average rate of 2 emails per hour
     random_values = poisson.rvs(2, size=5)
     print(random_values)
     ```

#### III. Exponential Distribution
**Concrete Example:**
- **Example Scenario**: The time between arrivals of buses at a bus stop can be modeled using an exponential distribution if the buses arrive independently and at a constant average rate.

**Python Function: `scipy.stats.expon`**

1. **expon.cdf()**
   - **Definition**: The cumulative distribution function (CDF) calculates the probability that the time between events is less than or equal to a certain value.
   - **Example**:
     ```python
     from scipy.stats import expon
     # Probability that the waiting time is less than or equal to 5 minutes, given the average rate is 1 bus per 10 minutes
     prob = expon.cdf(5, scale=10)
     print(prob)  # Output: 0.3934693402873666
     ```

2. **expon.pdf()**
   - **Definition**: The probability density function (PDF) calculates the probability density of the time between events at a given value.
   - **Example**:
     ```python
     from scipy.stats import expon
     # Probability density at 5 minutes, given the average rate is 1 bus per 10 minutes
     density = expon.pdf(5, scale=10)
     print(density)  # Output: 0.09048374180359596
     ```

3. **expon.rvs()**
   - **Definition**: The random variate sampling (RVS) function generates random numbers from an exponential distribution.
   - **Example**:
     ```python
     from scipy.stats import expon
     # Generate 5 random waiting times from an exponential distribution with an average rate of 1 bus per 10 minutes
     random_values = expon.rvs(scale=10, size=5)
     print(random_values)
     ```

These summaries provide concrete examples and Python applications of the normal, Poisson, and exponential distributions using the `scipy.stats` library.
