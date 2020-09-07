*Question 1: On Shopify, we have exactly 100 sneaker shops, and each of these shops sells only one model of shoe. We want to do some analysis of the average order value (AOV). When we look at orders data over a 30 day window, we naively calculate an AOV of $3145.13. Given that we know these shops are selling sneakers, a relatively affordable item, something seems wrong with our analysis.Think about what could be going wrong with our calculation. Think about a better way to evaluate this data. 
What metric would you report for this dataset?
What is its value?*

# Power BI Analysis - EDA
Using Power BI we can easily do basic EDA statistics for the given data in order to Visualize Patterns, Influencers and the important metric to desribe the data in the best manner


### Methods Used
* Histograms
* Quartiles
* Influencers

### Technologies
* Power BI Graphs and DAX

## 1. Metric - for Analysing Orders

![Image of Metric](https://github.com/digvijay52/Shopify-Winter-2021-Challenge/blob/master/Images/Main_Metric.PNG)

- Due to outliers present in the data we cannot analyse the orders using mean thus we can use median to have an idea.
- Altough InterQuartile Range would be the best metric instead of median in this case in order to have a inference of the orders being placed.
- Thus our Range here is 163 - 390.
- From this we can safely infer that accoridng to the current market a general business can 
  expect to set an price and sell their product between in this range.


## 2. Avergae Order Graph - Outlier Evaluation and Pattern

![Image of Average_Order](https://github.com/digvijay52/Shopify-Winter-2021-Challenge/blob/master/Images/Average_order.PNG)

- Now in order to analyze the anomlies we have to consider all the aspects whihc inlcude ShopID, Time, UserID
  - From the ShopID Data we can clearly observer that y two shops have extremely High average order. Thus we
    clearly say that they would represent the rest of market fairly and the shops should be categrized as outliers.
  - From the Time Perspective we observe that the Average Order Amount as well as the Total items of Purchase Increase almost 
    every 2-4 days thus giving us an idea that some is regularly doign bulk purchasing.
  - The last insight here is that the User with the ID 607 is the one who is doing all the bulk purchases and thus the data of this
    customer represent an outlier.
    
## 3. Basic EDA and Influencers

![Image of EDA](https://github.com/digvijay52/Shopify-Winter-2021-Challenge/blob/master/Images/Basic%20EDA.PNG)

- Basic EDA helps us undersand the disrtibution and correlation factors.
  - This first point here would be about the payment method distribution that most of the users use Credit Cards to do Payments.
  - Secondly, although we did understand about the outliers from the previous graph. But just to understand things in more detail we 
    can say that purchases from shop 77-78 increase order by 43k and purhaces by user 607 increase orders 703K. Its clear that these are two main
    factors for the data anomalies.
  - IMP NOTE: The sentences in the influnecers section of the graph should not be taken literally as they do not actaully represent the entire data, thus 
    this is not the best way to analyze outliers.
