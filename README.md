# A/B test Note

#### A/B test successful mindset
1. Hypothesis: what are we trying to test - If we change X, it will impact Y / If we remove likes from photos on Instagram, then maybe more people will post photos.
2. Methodology: discuss how to run the experiment. two cohorts: control group- people who see like on photos/test group - people who don't see like on photos.
3. Metrics: which metrics we're measuring? track the number of photos being posted. Other metrics: bounce rate of sharing a photo, or CTR of other buttons on the app.
4. Tradeoffs: potential pitfalls to the proposed features. People's perception of hiding the like button. Loneliness is hard to quantify and missed in the data-driven mindset.
5. Impact: how this info can impact the team.    

source: https://www.youtube.com/watch?v=jEpwNaHjD68

## Chapter 1
- A/B intro
  - an experiment designed to test which version is better
  - based on metric(s): signup rate, average sales per user, etc
  - using random assignment and analyzing results
- A/B test use case
  | Good Use of A/B Testing:                   | Do Not A/B Test If:                                 |
|------------------------------------------|------------------------------------------------------|
| Optimizing conversion rates              | No sufficient traffic/"small" sample size             |
| Releasing new app features               | No clear logical hypothesis                           |
| Evaluating incremental effects of ads    | Ethical considerations                                |
| Assessing the impact of drug trials      | High opportunity cost                                 |

- A/B test process
  1. Specify the goal and designs/experiences
  2. Randomly sample users for enrollment
  3. Randomly assign users to control or test group
  4. Log user actions and compute metrics
  5. Test for statistically significant differences
- Value of randomization
  - Generalizability and representativeness
  - Minimizing bias between groups
  - Establishing causality by isolating treatment effect
- The value of A/B testing
  - Reduce uncertainty around the impact of new designs and features
  - Decision-making --> scientific, evidence-based - not intuition
  - Generous value for the investment: simple changes lead to major wins
  - Continuous optimization at the mature stage of the business
  - Correlation does not imply causation
- Hierarchy of evidence (image)
- Types of metrics
  - Primary (goal/north-star): Best describes the success of the business or mission
  - Granular metrics: Best explain users' behavior
  - Instrumentation/guardrail metrics
- Quantitative categorization
  - Means/percentiles: average sales, median time on page
  - Proportions: Signup rate: signups/total visitors
  - Ratios: Click-through-rate(CTR): clicks/page visits or clicks/ad impressions
  - Metrics can be combined to form a more comprehensive success/failure criteria
- Metrics requirements
  - Stable/robust against the unimportant difference
  - Sensitive to the important changes
  - Measurable within logging limitations
  - Non-gameable
  
## Chapter 2
- Defining hypotheses: A hypothesis is a statement explaining an event/a starting point for further investigation/an idea we want to test
- Hypothesis format:
  - Based on X, we believe that if we do Y
  - Then Z will happen
  - As measured by metric(s) M
  - e.g. Based on user experience research, we believe that if we update our checkout page design, then the percentage of purchasing customers will increase as measured by the purchase rate.
- Distribution parameters:
  - d follows a normal distribution <br>
    d = $p_{B}$ - $p_{A}$ <br>
    H0: d = $p_{B}$ - $p_{A}$ = 0 <br>
    HA: d = $p_{B}$ - $p_{A}$ ≠ 0 <br>
  - If observed difference 'd' is unlikely: reject the Null hypothesis
- Terminalogy 
  - Power (1- β): Commonly set at 80%; β = Type II error = False negative
  - Minimum Detectable Effect (MDE): Smallest difference we care to capture
  - Significance level α: Commonly set at 5%; α = Type I error = False positive
  - P-value: The p-value in statistics is a measure of the probability of obtaining results as extreme as the observed results of a statistical hypothesis test, assuming that the null hypothesis is true. In simpler terms, it tells us how likely it is to observe the data if the null hypothesis is true; If p-value < α, Reject Null hypothesis; If p-value > α, Fail to reject Null hypothesis
- Power analysis: sample size estimation
- Multiple comparisons corrections
  
  | Single Comparison                      | Multiple Comparisons                            |
|----------------------------------------|-------------------------------------------------|
| Control (A) versus Treatment (B)       | Multiple variants (A/B/n tests)                 |
| One metric                             | Multiple metrics                                |
| No subcategories                       | Granular categories                             |
- Correction methods
   - Bonferroni Correction: <br>
     $\text{Adjusted significance level α*} = \frac{\alpha}{m} \$<br>
     
     α = Desired overall significance level (e.g., 0.05 for 5% significance)<br>
     m = Number of comparisons<br>
   - Sidak correction: <br>
   
   $\text{Adjusted significance level}\$ $α_{S}$ = $1 - (1 - \alpha)^{\frac{1}{m}} $
         
     α = Desired overall significance level (e.g., 0.05 for 5% significance)<br>
     m = Number of comparisons<br>
## Chapter 3
- Data cleaning and EDA
- Sanity checks for validation
- Analyzing difference in proportions
- proportions_ztest , proportion_confint

## Chapter 4
- Analyzing differences in means
- Non-parametric tests
- Delta method for ratio metrics
- Best practices and advanced topics
