# Machine Learning Trading Bot

## OBJECTIVE: Use machine learning algorithms in order to maximize a trading strategy.

### The following libraries and dependecies are used throughout this notebook.

<img width="400" alt="Screen Shot 2022-10-06 at 11 48 40 PM" src="https://user-images.githubusercontent.com/108194033/194476716-00460891-c84e-410e-827b-3ba3364bc4d2.png">

### Below shows the Actual Returns vs the Strategy Returns of the algorithmic model.

<img width="570" alt="Actual_vs_Strategy_Cumulative_Returns" src="https://user-images.githubusercontent.com/108194033/194478682-0756384d-8b56-479d-aa56-20c7699fe705.png">

### Conclusions of the Baseline Trading Algorithm:
Judging by the chart above, the algorithmic model follows the same trend as the actual data, but the cumulative returns of the model are lagging below the actual cumulative returns.  This shows with the precision score of buys being 56%, or the percentage of buy predictions that were correct, catching 96% of the buys that were actual buys. This yields an F1 score of .71, somewhat successful.

### The next step asked to change the timeframe parameters, which I changed from 3 months to 24 months. Below is the reflection of the new parameters Actual Returns vs Strategy Returns chart, as well as the classification report.

<img width="570" alt="Screen Shot 2022-10-09 at 11 23 13 PM" src="https://user-images.githubusercontent.com/108194033/194803599-23609593-dd07-4f6c-9bda-653794c7373f.png">

<img width="445" alt="Screen Shot 2022-10-09 at 11 24 51 PM" src="https://user-images.githubusercontent.com/108194033/194803762-10e4b4a7-f1fe-44dd-883e-db85eb76779a.png">

### Conclusions of 24-month parameter:
The precision score didn't change, however the recall was 100% and the F1 Score increased by .01. Taking a larger timeframe of data appears to have helped the strategy model, as evident of the increased cumulative returns.

### Finally, adjusting the SMA of both the Fast and Slow windows is another change to the strategy model that could give us better results. For all of the tests above, SMA_Fast = 4 and SMA_Slow = 100. Using the original 3-month timeframe, and changing the SMA_Fast = 50 and SMA_Slow = 200, the results are shown below.

<img width="571" alt="Screen Shot 2022-10-09 at 11 38 20 PM" src="https://user-images.githubusercontent.com/108194033/194804299-89d31eac-8c80-4a72-ae1e-dc16c610686b.png">

<img width="435" alt="Screen Shot 2022-10-09 at 11 38 30 PM" src="https://user-images.githubusercontent.com/108194033/194804316-18ad225a-11f9-489a-9fb2-a3bf52f7bbd8.png">

### Conclusions of the 3-month timeframe with adjusted SMAs:
We increased the precision and F1 Score and had nearly a perfect recall score, however this strategy shows significantly less cumulative returns.

## LogisticRegression Model:
### As a final step, we were asked to classify the training model with one of the classifiers. I used LogisticRegression. Below are the results.

<img width="569" alt="Screen Shot 2022-10-09 at 11 52 39 PM" src="https://user-images.githubusercontent.com/108194033/194805557-9ac7c2bb-f152-4434-bf02-a79379b3db9b.png">

### Conclusion:
This LogisticRegression model appears to outperform all other models and the Actual Returns, as evident of the very higher cumulative returns. However, the drop off from late 2020 to early 2021 is very concerning. Therefore, the original strategy with the SMA_Fast = 4, SMA_Slow = 100 and a 3-month time period gives us the greatest cumulative returns and an upward returns action as the chart completes.
