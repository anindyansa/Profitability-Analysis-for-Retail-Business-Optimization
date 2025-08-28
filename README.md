# judul 
## Table of Contents


### Project Overview
Power BI dashboard analyzing profit and revenue across Home Appliances, Groceries, Apparel, and Electronics. Includes data cleaning, formatting, and visualization to turn raw sales data into actionable business insights.

<p align="center">  
   <img width="901" height="505" alt="image" src="https://github.com/user-attachments/assets/7b84bf62-311f-4868-9747-6b3fe815e560" />
</p>

### Data Sources 
For this profitability analysis, we used three main datasets that support the business objective of identifying profitability factors by product and category. Below is a description of each dataset:

**a.) Sales_Data** : This dataset contains information related to product sales across various categories and regions. It includes 100 entries detailing products, categories, regions, and distribution channels. The data focuses on product sales details used for revenue calculation.

**b.) Cost_Profit_Data** : This dataset includes data on production costs, distribution costs, and net profit. It serves to calculate and analyze product profitability margins by taking into account different cost components.

**c.) Additional_Info** : This dataset provides supplementary information on sales seasons, sales dates, and customer demographics. It helps in understanding seasonal trends as well as customer segmentation relevant to profitability.

The following are the complete dataset columns along with their descriptions:

|Column|Description|
|--------|--------|
|Product_ID|Unique identifier for each product|
|Product_Category|Product category (e.g., Electronics, Apparel, Household Appliances)|
|Region|Sales region of the product (e.g., Jakarta, Surabaya, Bali)|
|Sales_Channel|Sales channel (e.g., Online, Physical Store)|
|Unit_Price|Selling price per unit|
|Units_Sold|Number of units sold|
|Total_Revenue|Total revenue generated from the product|
|Production_Cost|Production cost per unit|
|Distribution_Cost|Distribution cost per unit|
|Discount_Percentage|Percentage of discount applied|
|Net_Profit|Net profit after deducting production, distribution, and discount costs|
|Season|Sales season or quarter (e.g., Q1, Q2, etc.)|
|Date_Sold|Date of product sale|
|Customer_Age_Group|Customer age group (e.g., 18–25, 26–35, 36–45)|

### Data Cleaning/Data Preparation 
The data preparation and cleaning stage aims to ensure data quality and consistency for analysis. This process involves several steps to handle incomplete, inconsistent, or improperly formatted data. The main steps include:

**1. Handling Missing Values** 
- Discount_Percentage column: If this column contains missing values, it is assumed that no discount was applied. Therefore, missing entries are replaced with “0%” to avoid inconsistencies during analysis.
- Net_Profit column: Rows with missing or null values in this column are removed from the dataset to maintain data integrity, since net profit is a critical metric that must be available for every product entry.

**2. Ensuring Date Format Consistency**
- Date_Sold column: To maintain consistency, the Date_Sold column is standardized to a uniform format (e.g., YYYY-MM-DD). This standardization facilitates time-based analyses, such as identifying seasonal trends or calculating monthly sales.

### Results/Findings 
The analysis results are summarized as follows :

**1. Net Profit Overview – KPI Card**

<p align="center">   
   <img width="201" height="222" alt="image" src="https://github.com/user-attachments/assets/535d49bb-b5b6-4fe0-86fd-64318955855d" />
</p>

***Data*** : `Total_Revenue`, `Net_Profit` 

***Insight*** :
- Provides a concise overview of the company’s real financial condition by highlighting the differences between gross revenue, costs, and net profit. This allows management to quickly understand the overall actual profitability after all expenses are taken into account.
- Analysis period: January–April 2024, covering all regions and product categories.
- By region, Surabaya recorded the highest net profit of Rp268K, while Bali posted the lowest at Rp80K.
- Initial findings indicate that high revenue does not always translate into high net profit, making cost efficiency in each region a critical factor.
  
***Managerial Recommendation*** : 
- Net profit can serve as a key indicator of the company’s financial health during January–April 2024.
- Comparing revenue, costs, and net profit helps identify the proportion of expenses relative to gross revenue.
- The difference shown (in terms of marginal cost) can be used as a basis to evaluate whether distribution, production, and discount policies remain efficient or instead create unnecessary burdens.
- The highest-contributing region (Surabaya) can serve as a benchmark, while underperforming regions (Bali) require cost and sales strategy evaluation to improve profitability.

**2. Category Comparison Performance – Table with Slicer**

<p align="center">  
   <img width="327" height="226" alt="image" src="https://github.com/user-attachments/assets/7642ada3-ba3b-4e96-aed9-2ef041975c7d" />
</p>  
 
***Data*** : `Product_Category`, `Units_Sold`  ,  `Units_Sold` , `Total_Revenue`  ,`Net_Profit` ,  `Region` , `Date_Sold`   

***Insight*** :
- This visualization presents sales performance in terms of revenue, net profit, operating costs, and margins. Data is segmented by product category, region, and period, allowing management to assess each dimension’s contribution to profitability and to identify both strengths and underperforming areas.
- Overall Performance: From a total revenue of $3,000,191, the company achieved $765,955 net profit with a 25.5% margin. While healthy, profit distribution across categories is uneven.
- Home Appliances delivered the highest profit ($257,709 | 33.6%) with a 28.3% margin.
- Groceries contributed strongly ($226,309 | 29.5%) and achieved the highest efficiency with a 31.5% margin.
- Apparel generated moderate profit ($164,244 | 21.4%) with a 28.9% margin, acting as a balancing category.
- Electronics recorded the highest revenue ($814,995) but the lowest profit ($117,693 | 15.4% margin) due to high cost/distribution burdens.
- Surabaya achieved the highest profit ($267,888), mainly from Electronics and Groceries. However, Home Appliances showed weak margins despite strong sales volume. Notably, no sales were recorded in April, signaling distribution or seasonal demand issues. Bali posted the lowest profit ($79,556) with heavy reliance on Home Appliances, causing volatility. In April, Electronics sales led to a major loss (- $41,302), turning overall profit negative.

***Managerial Recommendation*** : 
- Groceries act as a cash cow with high margins and low risk, making them a top priority for expansion due to consistent contribution.
- Home Appliances, despite large profits, remain inefficient as high sales volume does not align with margins. Distribution and production need evaluation to boost effectiveness.
- Electronics face pressured margins; cost reviews, discount strategies, supplier renegotiation, or price adjustments are necessary to improve profitability.
- Apparel serves as a stabilizer but requires product and pricing differentiation to avoid recurring losses.
- The company can strengthen high-profit categories (Groceries) while addressing inefficiencies in Home Appliances & Electronics.
- Surabaya risks losing momentum; improving Home Appliances’ profitability is key for regional stability.
- Bali is overly dependent on Home Appliances; diversification into Groceries and cost efficiency in Electronics & Apparel are crucial for mid-term growth.

**3. Discount Effectiveness Analysis – Line & Stacked Bar Chart**

<p align="center">
  <img width="324" height="222" alt="image" src="https://github.com/user-attachments/assets/8fc08f33-940d-424b-8079-1812d00cfa41" />
</p>

***Data*** : `Product_Category` , `Total_Revenue` , `Net_Profit` , `Discount_Percentage` 

***Insight*** :
- This visualization analyzes the relationship between discount levels, revenue, and net profit across product categories. The objective is to measure the effectiveness of discounts in driving profitability while identifying whether current discount strategies are optimal or instead burden overall performance.
- Electronics: Lowest average discount (8%) but also the smallest profit contribution ($117,693). This suggests that lower discounts do not necessarily ensure profitability, likely due to thin margins or relatively high cost of goods sold.
- Groceries: Highest discount rate (13%) yet still delivers substantial profit ($226,309). This indicates that high sales volume can offset aggressive discounting, keeping profitability intact.
- Home Appliances: Highest profit ($257,709) with a moderate discount rate (9%). This reflects an effective discount strategy—moderate in size, yet able to generate high revenue ($912,539) while sustaining strong margins.
- Apparel: Medium profit contribution ($164,244) with a 10% discount. Compared to categories with similar revenue, Apparel is less efficient in leveraging discounts to improve profit, suggesting the need for revised promotion strategies and product positioning.

***Managerial Recommendation*** : 
- Home Appliances: Maintain moderate discounts (7–10%) to safeguard profitability, position as a cash cow, and prioritize long-term promotional investments.
- Groceries: Apply aggressive yet controlled discounts (max 12%). Alternatives include bundling or subscription models (e.g., monthly packages) to sustain sales volume without eroding margins.
- Electronics: Reassess cost structure in production and logistics. Priorities include supplier renegotiation and supply chain efficiency. If discounts prove ineffective, consider price repositioning or reducing category focus.
- Apparel: Avoid excessive discounting outside peak seasons. Instead, emphasize product differentiation or limited-edition campaigns to add value without relying heavily on discounts.
- Selective Discounting: Apply a loss leader strategy only to highly competitive categories or new products, while retaining premium pricing in high-margin categories to preserve brand value.
- Cross-Subsidizing: Utilize profits from high-margin categories (Home Appliances, Groceries) to support categories that require deeper discounts as market entry levers.
- Marketing Targeting: Position discount-sensitive categories for seasonal promotions, while profitable categories without discount reliance should focus on brand building.

**4. Sales Volume Dynamics – Clustered Bar Chart**

<p align="center">   
   <img width="369" height="226" alt="image" src="https://github.com/user-attachments/assets/eb08c5de-bee3-4692-abbb-bbff7ed6a526" />
</p>
   
***Data*** : `Product_Category` , `Units_Sold` 

***Insight*** :
- This visualization illustrates the dynamics of monthly units sold per product category. The analysis helps assess demand consistency, identify drivers and barriers to sales, and understand how sales volume affects revenue and profitability.
- January recorded a strong start (8,098 units), generating $482,085 in profit. Most categories contributed positively, especially Apparel ($145,310) and Electronics ($131,363), reflecting early-year momentum.
- February achieved the highest sales volume (8,678 units) but profit fell sharply to $326,262. This indicates that higher volume does not necessarily translate into higher profitability, likely due to distribution costs or suboptimal discount strategies. Electronics, for example, sold 1,133 units but contributed only $20,058 profit.
- March saw lower sales volume (7,294 units) yet profit increased significantly to $451,834. This suggests improved cost efficiency or pricing adjustments. Groceries contributed the most ($146,503) despite not having the highest sales, highlighting effective margin management.
- April experienced a steep decline (3,041 units) with the lowest profit ($175,384). Almost all categories weakened, particularly Apparel with just 474 units and $17,036 profit, revealing demand vulnerability and market inconsistency at the end of the period.
  
***Managerial Recommendation*** :
- Improve cost efficiency in distribution and promotions during high-volume months (e.g., February) to align sales growth with profitability. Cost structure evaluation per category should be prioritized.
- Leverage resilient categories such as Home Appliances and Groceries, which remained profitable even under weakened conditions (April). Long-term promotions should be anchored in these categories to ensure revenue stability.
- Mitigate risks in vulnerable categories (Electronics and Apparel) by revisiting discount policies, renegotiating supplier terms, or enhancing product differentiation. Without intervention, these categories may become structural burdens during downturns.
- Enhance seasonal monitoring: January–March patterns reveal gaps between volume and profit. An early-warning system based on volume and margin indicators is recommended to anticipate weakening periods.
- Diversify marketing strategies across months: prioritize volume-driven strategies during peak sales periods, while focusing on margin through premium pricing or bundling in weaker months.

**5. Donut Chart**  

<p align="center"> 
   <img width="158" height="225" alt="image" src="https://github.com/user-attachments/assets/a1362b7c-0c08-4e51-95a6-99322d24060e" />
</p>

***Data*** : `Sales_Channel`  

***Insight*** : 
- This visualization helps to understand the distribution and dynamics of sales channels by observing growth trends, dominant categories, and differences in regional contributions. 
- Online growth remains volatile (43% → 46% → 40% → 41%), showing no stable upward trend and even a decline in March. 
- Sales Category Distribution : Electronics contributes the most at 50%, reflecting strong market demand both online and offline. On the other hand, Groceries only account for 37%.
- Geographic Distribution : Surabaya leads with a 55% contribution, signaling strong channel penetration in major cities. Meanwhile, Bali lags at 37%, showing untapped potential—especially through online channels.

***Managerial Recommendation*** :
- Enhance online growth stability through continuous campaigns such as loyalty programs and seasonal promotions, or e-commerce push notifications.
- Strengthen the competitiveness of groceries online by offering attractive promotional strategies (e.g., bundled daily needs).
- Expand penetration in non-dominant regions such as Bali by leveraging online channels to target tourists and local communities.
  
**6. Age Group Revenue Distribution – Bar Chart**

<p align="center"> 
   <img width="326" height="222" alt="image" src="https://github.com/user-attachments/assets/e845947a-0439-44d4-8bca-f32bef055318" />
</p>

***Data*** : `Customer_Age_Group` , `Total_Revenue`  

***Insight*** : 
- This visualization evaluates revenue contribution by age group, benchmarked against the overall average. The analysis reveals consumption patterns unique to each segment, enabling management to tailor marketing and sales strategies more precisely.
- Age 26–35 : Offline ($465,163) and online ($480,793) both far exceed the average.
Prime spending power with consistent demand across channels. Backbone of company revenue.
- Age 36–45 : Highest offline revenue ($473,989), but online lags far behind ($142,512). Shows strong reliance on physical stores and weak digital adoption.
Key target for digital transition.
- Age 46–55 : Low offline revenue ($205,852) but dominant online ($634,251).
Selective channeling—prefers online for high-value purchases.
Strong premium potential.
- Age 18–25 : Offline revenue above average ($394,259), but online weak ($203,373).
Despite being tech-savvy, engagement strategies seem misaligned.
High untapped potential.

***Managerial Recommendation*** : 
- 18–25: Boost digital engagement via student discounts, gamification, and low-cost bundles. Enhance offline with experiential marketing (e.g., interactive events).
- 26–35: Drive omnichannel loyalty with integrated rewards, synchronized inventory, and consistent after-sales service.
- 36–45: Keep offline as the core revenue driver, while gradually shifting them online through trust-building measures (warranties, COD, after-sales support).
- 46–55: Prioritize online with premium offerings, exclusive products, priority delivery, and personalized content. Limit offline investment.

