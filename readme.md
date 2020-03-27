# Introduction:
Algorithmic trading is a method of executing a large order (too large to fill all at once) using automated pre-programmed trading instructions accounting for variables such as time, price, and volume to send small slices of the order (child orders) out to the market over time. Any strategy for algorithmic trading requires an identified opportunity that is profitable in terms of improved earnings or cost reduction.
In our project, we use some algorithms to train the stock data then try to predict the future price.

## Key Words:
Linear Regression, SVM, Auto Regression, RNN, LSTM, Bootstrap, R-square

### Goal:
This project aims to find the stock trade rule in the finance market. Based on the result, I want to predict the next 30 days’ stock value. And I expect that the prediction can fit well with our last test data, or wave within a range that I can accept.

#### Methodology
1. Machine Learning - Linear Regression
2. Machine Learning – SVM
3. Machine Learning - Auto Regression
4. Deep Learning – LSTM
5. Deep Learning – RNN

##### Conclusion:
As the machine learning part. We use Linear Regression, SVM and Auto Regression to predict the price of the stock. Since Linear Regression is a simple and quick model, we can get a rough forecast. The MSE of Linear Regression is 5.895, which can give our next models a reference evaluation. Since Linear Regression doesn’t perform the same result every time, we want to find a model that has a stable prediction result. At the SVM model step, we try two types: RBF and linear. Considering the feature of this model, we think RBF is a good choice to predict the trend of the price, but not a good to predict specific value. The performance of SVM linear is similar to Linear Regression. The MSE of SVM linear is 7.027, but the reason is different. The essential difference comes from loss function. The loss function of SVM Linear is Maximize spacing; however, the Linear Regression’s loss function is cross-entropy. The last model we choose is Auto Regression. After modified with bootstrap, it is the best one that can predict price in the machine learning part with MSE 6.36.

As the deep learning part. We use basic RNN cell, basic LSTM cell and LSTM cell with peephole connections three methods to do the stock prediction. As we can see Basic RNN and Basic LSTM will have deviations as time grows. Deviations of basic RNN appear at 1500 days and basic LSTM appear at 1530 days. We figure that deviations of basic RNN are because of the fall of RNN. Deviations of basic LSTM is because the amount of the data set is only 1566 to process. And for the LSTM with peephole connections is also have a deviation at 1500 days. And all 3 methods at around 900 days the training target has a mutation and predictions will have an error. In general, both RNN and LSTM model can roughly predict the trend of the stock successfully on whether the stock price will rise or drop, but the amount of the gradient of stock may seem not that accurate for our data is not large enough to train a more consummate model to predict the stock price concisely.

If a market maker wants to make money from the stock, we suggest using deep learning to predict the specific value. However, if the market maker wants to make a long-term gain from the stock, this will not predict very particularly accurately.
