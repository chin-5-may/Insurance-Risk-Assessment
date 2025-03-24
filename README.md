# Insurance Premium Calculation and Risk Analysis

**Assignment 4 - Group 09**

This project aims to determine the premium values for an insurance policy based on discrete random variables using Gaussian approximations and root-finding optimization techniques. We compute premiums such that the probability of a surplus falling below a threshold is minimal.

## Problem 1: Joint PMF of Two Random Variables
The task involves determining the joint probability mass function (pmf) of two random variables, X (number of policyholders) and Y (number of claims), where:
- \( S = \alpha X - \Omega Y \) (Surplus), with \( \Omega = 10 \) (payout for a claim).
- Poisson distribution for \( X \) and Binomial distribution for \( Y \) are used to model the number of policyholders and claims, respectively.

### Approach:
1. **Gaussian Approximation**:
   - For large values of \( \lambda \), the Poisson and Binomial distributions can be approximated using Gaussian distributions.
   - \( X \sim N(\lambda, \lambda) \) and \( Y \sim N(\lambda p, \lambda p(1-p)) \), where \( p \) is the probability of a claim.

2. **Surplus Calculation**:
   - The surplus \( S = \alpha X - \Omega Y \) is approximated using the Gaussian distributions of X and Y.
   - We find \( \alpha \) such that \( P(S < a) \approx 0.01 \) for specified values of \( a \).

### Results:
- Minimum alpha for Policy 1: **0.22**
- Minimum alpha for Policy 2: **2.50**

---

## Problem 2: Parameter Estimation for \( \lambda \) and \( p \)
We estimate \( \lambda \) (mean number of policies sold) and \( p \) (probability of claims) from a dataset. The task is to compute point estimates and confidence intervals for these parameters.

### Steps:
1. **Point and Interval Estimates**:
   - For \( N = 20 \) samples: 
     - Point Estimate for \( \lambda \): **100016.40**
     - 95% Confidence Interval for \( \lambda \): (99879.37, 100153.43)
     - Point Estimate for \( p \): **0.02002**
     - 95% Confidence Interval for \( p \): (-0.04137, 0.08140)

2. **Premium Calculation**:
   - Using the estimated values of \( \lambda \) and \( p \), we calculate new premiums \( \alpha \) for policies, ensuring a probability of \( P(S < a) < 0.01 \).

---

## Problem 3: Discussion
1. **Financial Stability vs Affordability**:
   - Higher premiums provide financial stability but may be less affordable for policyholders. Lower premiums improve accessibility but may not offer sufficient protection against claims.

2. **Cross-Subsidy**:
   - Cross-subsidization allows one demographic's premium to subsidize another group's losses. This can make policies more affordable for high-risk groups but may lead to dissatisfaction among low-risk groups.

3. **Independence Assumption**:
   - Assuming independence between X and Y (policy sales and claims) could lead to incorrect premium calculations. Correlations between X and Y must be considered for accurate variance estimation and surplus calculations.

---

## Conclusion:
This project demonstrates the importance of using Gaussian approximations and statistical methods for setting insurance premiums. The balance between financial stability, accessibility, and accurate risk assessment is crucial for maintaining both profitability and customer satisfaction.

---

**Links**:
- [N=20 Data](https://drive.google.com/file/d/1D7y-ggz3mYPM-Cza7lchB4TmK_blsPol/view?usp=drive_link)
- [N
