# A/B test Note

## A/B test process
1. hypothesis: what are we trying to test - If we change X, it will impact Y / If we remove likes from photos on Instagram, then maybe more people will post photos.
2. Methodology: discuss how to run the experiment. two cohorts: control group- people who see like on photos/test group - people who don't see like on photos.
3. Metrics: which metrics we're measuring? track the number of photos being posted. Other metrics: bounce rate of sharing a photo, or CTR of other buttons on the app.
4. Tradeoffs: potential pitfalls to the proposed features. People's perception of hiding the like button. Loneliness is hard to quantify and missed in the data-driven mindset.
5. Impact: how this info can impact the team.    

source: https://www.youtube.com/watch?v=jEpwNaHjD68

## Chapter 1
- A/B testing steps and use-cases
- Metrics definition and estimation
- .sample() , .corr() , pairplot , heatmap
  
## Chapter 2
- Formulating A/B testing hypotheses
- Error rates, power, effect size
- Power analysis: sample size estimation
- Multiple comparisons corrections
  
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
