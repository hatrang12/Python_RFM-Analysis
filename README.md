# Python_RFM Analysis

The project uses Python to classify customer segments by analyzing data from a retail company around the world, and then proposes appropriate solutions to deploy for each separate consumer group as needed. from the Marketing Director

<p align="center">
<img src="https://github.com/hatrang12/Python_RFM-Analysis/blob/main/pic.png" align="center" width="400" height="400" >

## I. **Introduction**

## **1. Business questions**

- SuperStore is a global retail company. The Marketing Department wants to run marketing campaigns during the Christmas and New Year holidays to thank customers for their past support of the company. In addition, potential customers can be upgraded to become loyal customers.
- The Marketing Director also proposed a plan to use the RFM model in Python to segment customers and then launch appropriate marketing campaigns. Analyze the current situation of the company and give suggestions to the Marketing team
- With the retail model of Superstore company, which indicator should be most focused on in the 3 indicators R, F, and M?

### **2. Dataset**

Dataset includes 3 different related tables including: transaction information, segmentation information, returned orders of customers purchasing products from 12/2010 to 12/2011.

- **Transaction information dataframe**
![1](https://github.com/hatrang12/Python_RFM-Analysis/assets/107136018/85bef089-ce32-4331-8d76-9c96c5ccc001)

- **Returned orders dataframe**: We have to filter orders that were not returned before RFM analysis.

```python
returned.info()
returned.head()
```
![2](https://github.com/hatrang12/Python_RFM-Analysis/assets/107136018/4dad1457-3a26-4399-bd35-0c3e5c0b3fcf)


- **Segmentation dataframe**: 'Product ID' is not unique because some products have same Product ID but have different Product Name => drop 'Product Name' then remove duplicate records so that 'Product ID' will be unique.

![3](https://github.com/hatrang12/Python_RFM-Analysis/assets/107136018/f70100f5-6c3e-48dd-a178-02e9bdbc058d)


### **3. RFM Model**

- RFM is a the abbreviation that stands for Recency, Frequency, and Monetary Value, and each component relates to important client criteria. These RFM measures are important to evaluate customer behavior since frequency and monetary value have a direct impact on a customer's lifetime value, whereas recency influences retention, a number that reflects engagement.
- RFM analysis numerically ranks a customer in each of these three categories, generally on a scale of 1 to 5 (the higher the number, the better the result). The “best” customer would receive a top score in every category.
- Businesses without a direct monetary component, such as those focused on viewership, readership, or surfing-oriented products, may opt for Engagement parameters in lieu of Monetary factors. This adaptation results in the utilization of RFE, a variance of RFM. Moreover, the Engagement parameter can be delineated as a composite value derived from metrics such as bounce rate, visit duration, number of pages visited, time spent per page, among others.

## **II. Data visualization**

### 1. Average Recency by RFM Segments

![Capture5](https://github.com/hatrang12/Python_RFM-Analysis/assets/107136018/87525b9a-c622-4e3a-b738-cefbbc6f6d05)

### 2. Average Frequency by RFM Segments

![Capture6](https://github.com/hatrang12/Python_RFM-Analysis/assets/107136018/be82a792-fcb7-46f9-8fc2-f2f370f6e0ad)

### 3. Total sales by RFM Segments

![Capture7](https://github.com/hatrang12/Python_RFM-Analysis/assets/107136018/961c103a-4052-4e7d-a196-d0495a0aa0f1)

### 4. Total customer by RFM Segments

![Capture8](https://github.com/hatrang12/Python_RFM-Analysis/assets/107136018/5708f419-30b3-4e3e-825c-58d22cff048e)

## IV. Insights

- The data presented in the table reveals a notable high mean value for Recency, indicating that customers are inclined to discontinue their association with Superstore in the future. Conversely, there is an absence of positive signals in Frequency, with a mean value of 4.3, falling below the normal range, and a median of 2, signaling a significant concern for SuperStore. Despite these challenges, the Monetary aspect exhibits a positive side, with a mean value exceeding 2000
- The charts illustrating revenue and customer distribution across segments highlight that the Champions group, constituting 19.15% of the customer base, contributes more than 60% of the revenue. Following closely in revenue are the Loyal and At-risk groups, contributing 12% and 8.2%, respectively. However, Hibernating and Lost customers account for 16.4% and 13.1%, respectively, yet purchase fewer types of products, at 3.3% and 1.4%, respectively. The Need Attention group, comprising 5% of revenue, represents only 6.2% of total customers, necessitating special attention
- Examining the chart depicting customer segments, it is evident that the Championship group constitutes the largest portion at around 60%, signifying that Superstore possesses a considerable number of loyal customers
- The revenue chart underscores the significance of the Championship and Loyal groups as the highest contributors to the store's earnings
- The division of other customer groups into potential and in-danger categories reveals opportunities and risks. Potential customers include Hibernating customers, potential loyalists, promising, and new customers

## V. Recommendations

- To address these insights, it is imperative for Superstore to concentrate efforts on increasing both Recency and Frequency values. This strategic focus will likely contribute to customer retention and overall store performance
- Superstore should focus efforts on engaging with the Need Attention group, understanding their preferences, and implementing strategies to enhance their contribution to both revenue and overall customer satisfaction
- To maintain this strong customer base, Superstore should implement targeted marketing campaigns, such as personalized offers, exclusive discounts, and special services, to reinforce the loyalty of the Championship group
- Superstore should implement marketing campaigns tailored to the Championship and Loyal groups, focusing on strategies like birthday gifts, new product experiences, discounted offerings, and personalized customer care to strengthen their loyalty
- For potential customers, Superstore should introduce a loyalty program, engage actively on social media, and encourage customer referrals. In contrast, in-danger customers should be identified and rewarded for their value, while feedback should be actively sought and utilized for continuous improvement
