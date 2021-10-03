# Realized volatility kaggle competition

A solution of the [Optiver Realized Volatility Kaggle competition](https://www.kaggle.com/c/optiver-realized-volatility-prediction/data).

In this competition, 10 minutes of book data are given and it is asked to predict the volatility value in the following 10 minutes. The realized volatility, <img src="https://latex.codecogs.com/svg.latex?\sigma" title="\sigma" /></a>, is computed from the log returns over all consecutive book updates:



<img src="https://latex.codecogs.com/svg.latex?\sigma&space;=&space;\sqrt{\sum_{t}r_{t-1,&space;t}^2}" title="\sigma = \sqrt{\sum_{t}r_{t-1, t}^2}" /></a>

For order book data the weighted average price (WAP) is used as the price of the stock. The formula of WAP can be written as below, which takes the top-level price and volume information into account:

<img src="https://latex.codecogs.com/svg.latex?WAP&space;=&space;\frac{BidPrice_{1}*AskSize_{1}&space;&plus;&space;AskPrice_{1}*BidSize_{1}}{BidSize_{1}&space;&plus;&space;AskSize_{1}}" title="WAP = \frac{BidPrice_{1}*AskSize_{1} + AskPrice_{1}*BidSize_{1}}{BidSize_{1} + AskSize_{1}}" /></a>

Returns are widely used in finance, however, log returns are preferred whenever some mathematical modeling is required. Calling <img src="https://latex.codecogs.com/svg.latex?WAP_t" title="WAP_t" /></a> the WAP price of the stock at time t, we can define the log return between <img src="https://latex.codecogs.com/svg.latex?t_1" title="t_1" /></a> and <img src="https://latex.codecogs.com/svg.latex?t_2" title="t_2" /></a> as:


<img src="https://latex.codecogs.com/svg.latex?r_{t_1,&space;t_2}&space;=&space;\log&space;\left(&space;\frac{WAP_{t_2}}{WAP_{t_1}}&space;\right)" title="r_{t_1, t_2} = \log \left( \frac{WAP_{t_2}}{WAP_{t_1}} \right)" /></a>


# Position on the leader board

The root mean squared percent error (RMSPE) on unseen data is 0.22046, which is better than 33\% of the competitors (3965 competitors)
