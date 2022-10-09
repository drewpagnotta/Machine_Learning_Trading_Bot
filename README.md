# Machine Learning Trading Bot

## OBJECTIVE: Use machine learning algorithms in order to maximize a trading strategy.

### The following libraries and dependecies are used throughout this notebook.

<img width="400" alt="Screen Shot 2022-10-06 at 11 48 40 PM" src="https://user-images.githubusercontent.com/108194033/194476716-00460891-c84e-410e-827b-3ba3364bc4d2.png">

### Below shows the Actual Returns vs the Strategy Returns of the algorithmic model.

<img width="570" alt="Actual_vs_Strategy_Cumulative_Returns" src="https://user-images.githubusercontent.com/108194033/194478682-0756384d-8b56-479d-aa56-20c7699fe705.png">

### Conclusions of the Baseline Trading Algorithm:
Judging by the chart above, the algorithmic model follows the same trend as the actual data, but the cumulative returns of the model are lagging below the actual cumulative returns.  This shows with the precision score of buys being 56%, or the percentage of buy predictions that were correct, catching 96% of the buys that were actual buys. This yields an F1 score of .71, somewhat successful.
