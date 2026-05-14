# CAFE SALES ANALYSIS PROJECT
### OBJECTIVE
The objective of this project is to properly clean and validate a retail sales dataset and perform an exploratory analysis to identify sales patterns, customer behavior trends and potential business improvement opportunities.


### DATASET
Dataset obtained from Kaggle containing **10.000** records with the following information:
- **Transaction ID**: Unique identifier for each transaction.
- **Item**: Product sold.
- **Quantity**: Number of units sold. 
- **Price per unit**: Unit selling price.
- **Total spent**: Transaction total revenue.
- **Payment method**: Cash, credit card or digital wallet.
- **Location**: In-store or takeaway.
- **Transaction date**.


### METHODOLOGY
1.	Data cleaning:
    - Handling problematic values.
    - Validating numerical integrity.
    - Inferring missing values based on detected patterns.
2.	Exploratory Data Analysis:
    - Identifying sales patterns and customer behavior.
    - Analyzing product performance.
    - Comparing categories.
3.	Business insights and recommendations:
    - Extracting actionable insights from the analysis.
    - Identifying potential business optimization opportunities.


### KEY INSIGHTS
- **KPIs**:
    - A total of **10.000 transactions** were analyzed.
    - Total revenue of **$890.960**, making an average income of **$89 per transaction**.
    - A total of **30.180 products** were sold, making an average of **3 products sold per transaction**.
- **Salad** is the highest revenue-generating product, contributing **21.43% of total revenue** despite representing only **12.72% of transactions**. This suggests a strong balance between sales frequency and ticket value.
- **Coffee** is the most frequently purchased item (**12.91% of transactions**) but contributes only **8.76% of total revenue**, indicating a relatively low unit value.
- **Tea** and **Cookie** show similar behavior: **high transaction frequency but limited revenue** contribution, suggesting they may be underpriced or commonly purchased as low-value complementary items.
- **Smoothies** generate a disproportionately high share of revenue relative to their transaction volume, indicating **strong revenue efficiency** per sale.
 
| item     | item_percentage | total_spent_per_item | total_revenue_percentage |
|----------|-----------------|----------------------|--------------------------|
| Salad    | 12.72           | 190950               | 21,43                    |
| Sandwich | 11.31           | 137160               | 15,39                    |
| Smoothie | 10.96           | 133440               | 14,98                    |
| Juice    | 11.71           | 105150               | 11,8                     |
| Cake     | 11.39           | 104040               | 11,68                    |
| Coffee   | 12.91           | 78080                | 8,76                     |
| Tea      | 12.07           | 54750                | 6,15                     |
| Unknown  | 4.80            | 51410                | 5,77                     |
| Cookie   | 12.13           | 35980                | 4,04                     |

- **Revenue distribution across payment methods is remarkably balanced**.
- Cash is slightly less used than digital methods, which may reflect a gradual shift toward digital payments.
- The high percentage of `Unknown` payment methods suggests potential data collection limitations that could affect deeper behavioral analysis.

| payment_method | payment_method_percentage | total_spent_per_payment_method | total_revenue_percentage |
|----------------|---------------------------|--------------------------------|--------------------------|
| Unknown        | 31.78                     | 278135                         | 31,22                    |
| Credit Card    | 22.73                     | 204660                         | 22,97                    |
| Digital Wallet | 22.91                     | 204140                         | 22,91                    |
| Cash           | 22.58                     | 204025                         | 22,9                     |

- **In-store and takeaway** sales show **highly similar** transaction volume, revenue generation, and number of products sold.
- **Higher-value items** such as salads, sandwiches, and smoothies show a **slight preference for in-store consumption**.
- Meanwhile, coffee, cake, and cookies are more frequently associated with takeaway purchases.

| location | location_percentage | total_spent_per_location | total_revenue_percentage |
|----------|---------------------|--------------------------|--------------------------|
| Unknown  | 39.61               | 353695                   | 39,7                     |
| In-store | 30.17               | 271740                   | 30,5                     |
| Takeaway | 30.22               | 265525                   | 29,8                     |

| location | nr_products |
|----------|-------------|
| Takeaway | 9144        |
| In-store | 9133        |

| location | item     | total_revenue_percentage | X | location | item     | nr_transactions |
|----------|----------|--------------------------|---|----------|----------|-----------------|
| In-store | Salad    | 6,89                     | X | In-store | Salad    | 406             |
| Takeaway | Salad    | 6,25                     | X | Takeaway | Cookie   | 402             |
| In-store | Sandwich | 5,06                     | X | Takeaway | Coffee   | 396             |
| Takeaway | Sandwich | 4,73                     | X | Takeaway | Salad    | 378             |
| In-store | Smoothie | 4,28                     | X | In-store | Cookie   | 373             |
| Takeaway | Smoothie | 4,14                     | X | In-store | Sandwich | 370             |
| In-store | Juice    | 3,71                     | X | In-store | Tea      | 369             |
| Takeaway | Cake     | 3,53                     | X | Takeaway | Tea      | 368             |
| In-store | Cake     | 3,34                     | X | In-store | Juice    | 361             |
| Takeaway | Juice    | 3,34                     | X | In-store | Coffee   | 352             |
| Takeaway | Coffee   | 2,73                     | X | Takeaway | Sandwich | 345             |
| In-store | Coffee   | 2,42                     | X | Takeaway | Cake     | 343             |
| In-store | Tea      | 1,91                     | X | Takeaway | Juice    | 341             |
| Takeaway | Tea      | 1,86                     | X | In-store | Smoothie | 322             |
| Takeaway | Cookie   | 1,37                     | X | In-store | Cake     | 321             |
| In-store | Cookie   | 1,22                     | X | Takeaway | Smoothie | 304             |


### Monthly Trends

- **June, October and March** are the **strongest-performing** months in terms of revenue and transaction volume.
- **February** shows the **weakest performance** across both metrics.
- Despite minor fluctuations, **sales remain relatively stable throughout the year**, suggesting low seasonality impact on the business.

| month     | month_percentage | total_spent_per_month | total_revenue_percentage |
|-----------|------------------|-----------------------|--------------------------|
| June      | 8.18             | 73530                 | 8,25                     |
| October   | 8.38             | 73140                 | 8,21                     |
| January   | 8.18             | 72540                 | 8,14                     |
| March     | 8.27             | 72160                 | 8,1                      |
| December  | 7.95             | 71770                 | 8,06                     |
| April     | 7.74             | 71790                 | 8,06                     |
| August    | 8.03             | 71125                 | 7,98                     |
| November  | 7.84             | 69670                 | 7,82                     |
| May       | 7.77             | 69575                 | 7,81                     |
| July      | 7.91             | 68775                 | 7,72                     |
| September | 7.88             | 68710                 | 7,71                     |
| February  | 7.27             | 66440                 | 7,46                     |
| NULL      | 4.60             | 41735                 | 4,68                     |

- The most common transaction value is **$60**, making it the **modal transaction amount**.
- Most purchases are concentrated around medium-value transactions rather than very small or very large orders.
- The distribution suggests relatively **consistent customer spending behavior**.

| total_spent | nr_transactions_per_total_spent |
|-------------|---------------------------------|
| 10          | 249                             |
| 15          | 212                             |
| 20          | 518                             |
| 30          | 968                             |
| 40          | 969                             |
| 45          | 238                             |
| 50          | 496                             |
| 60          | 1019                            |
| 75          | 250                             |
| 80          | 720                             |
| 90          | 510                             |
| 100         | 542                             |
| 120         | 996                             |
| 150         | 766                             |
| 160         | 466                             |
| 200         | 789                             |
| 250         | 269                             |


### BUSINESS RECOMMENDATIONS

- **Review the pricing strategy for Coffee, Tea and Cookies**. Despite being among the most frequently purchased items, their contribution to total revenue is relatively low.
- **Promote high-performing categories such as Salads, Sandwiches and Smoothies**, which generate a disproportionately high share of revenue.
- Improve data collection processes to reduce the high proportion of 'Unknown' values in payment methods and locations, enabling more reliable customer behavior analysis.
- Since **takeaway and in-store** performance are highly balanced, both channels **should continue receiving similar strategic attention** and operational investment.
- The low seasonality observed throughout the year suggests relatively stable customer demand, which may simplify inventory and staffing planning.
