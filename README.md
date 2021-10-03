# Realized volatility Kaggle competition

A solution of the [Optiver Realized Volatility Kaggle competition](https://www.kaggle.com/c/optiver-realized-volatility-prediction/data).

In this competition, 10 minutes of book data are given and it is asked to predict the volatility value in the following 10 minutes. The **Realized volatility, $\sigma$,** is computed from the log returns over all consecutive book updates:

$$
\sigma = \sqrt{\sum_{t}r_{t-1, t}^2}
$$

For order book data the weighted average price (WAP) is used as the price of the stock. The formula of WAP can be written as below, which takes the top-level price and volume information into account:

$$ WAP = \frac{BidPrice_{1}*AskSize_{1} + AskPrice_{1}*BidSize_{1}}{BidSize_{1} + AskSize_{1}} $$

Returns are widely used in finance, however, **log returns** are preferred whenever some mathematical modeling is required. Calling $WAP_t$ the WAP price of the stock at time $t$, we can define the log return between $t_1$ and $t_2$ as:

$$
r_{t_1, t_2} = \log \left( \frac{WAP_{t_2}}{WAP_{t_1}} \right)
$$

# Position on the leader board

The root mean percent error on unseen data is 0.22046, which is better than 33\% of the competitors (3965 competitors)