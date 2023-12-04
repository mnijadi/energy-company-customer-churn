# EDA Summary

In this section, we will summarize the findings from our exploratory data analysis.

## Insights

1. The data is imbalanced, with churned clients representing 10%.
2. Consumption data is highly skewed to the right.
3. Consumption seems to be higher for non-churned clients.
4. There is a fair amount of correlation between consumption variables.
5. The margin is higher for churned clients.
6. The higher the number of products a client has, the lower the risk of churn.
7. Historical energy and power prices don't reveal any difference in behaviour for the off peak period. However, for the mid peak and peak periods, churned clients paid higher prices in average.

## Recommendations

- One way to deal with the high skewness of the consumption data is to apply a log transformation, to make it more symmetric, and for having a robust model.
- Our variables have different scales, standardization would be a good idea before applying any model.
- Historical data has some interesting insights we can add to the clients' data, such as the central tendency and dispersion of prices.
- There are many variables in our dataset, but due to correlations and weak associations with churn, we can drop many of them, and keep only those related with consumption and margin. Even then, we still need more data to better explain churn, such as competitors' prices, average prices in the market, clients' feedback, etc.
