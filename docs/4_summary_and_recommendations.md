# Recommendations

After building a model that seems to be useful, here are the main takeaways on how to to make the model talk, and evaluate its impact on the business.

- We used the model to compare between the total revenue between two cases, one where the discount strategy is applied, and one where it is not. Since the discount would affect the revenue very severely, we had to evaluate this very carefully.
- We relied on some assumptions along the way, the most important is that any customer likely to churn, when given a discount, would not. This isn't necessarily true, but for now this is what the business wants from us.
- We calculated the revenue based on the forecasted consumption and forecasted energy price for the next 12 months, assuming that any customer that is going to churn, will do so in the next 60 days.
- We loaded the model and made predictions of churn probabilities instead of the actual churn labels, that way, we had the felxibility to evaluate the strategy for different thresholds, and select the one that works best for the business.
- After doing a few comparisons for different threshold, we found that 0.58 is the best threshold to use, since it maximizes the revenue (1.7% increase in the total yearly revenue), this is a clear indication that despite the model relying on limited data, it is still useful and can be used to make impactful decision.
- To improve this analysis, we talked about:
  - Focusing on profitable clients instead of giving everyone with a high chance of churn a discount.
  - Changing the discount strategy to be more flexible, and give different discounts to different customers based on their churn probability and profitability.
