# Project Portfolio 3: Access to Power BI

##  Hola Retail Group: Customer & Sales Behaviour and Product Profitability Analytics


![access to Power BI.png](Assets_Folder/Images/access_to_Power_BI.png)



# Table of Content
- [Project Title](#Project-Title)
- [My Role](#My-Role)
- [Project Overview](#Project-overview)
- [Problem Statement](#Problem-statement)
- [Stakeholder Engagement](#Stakeholder-Engagement)
    - [Target Stakeholder](#Target-stakeholder)
    - [Use Cases](#Use-cases)
    - [Stakeholders Stories](#Stakeholder-stories)
    - [Acceptance Criteria](#Acceptance-criteria)
    - [Success Criteria](#Success-criteria)
- [Data Source](#Data-source)
  - [Dataase Structure](#Access-Database-Structure)
  - [Access Database Benefit](#Benefit-of-Access-Storage)
- [Methodology](#Methodology)
  - [Tool used](#Tool-Used)
  - [Development](#Development)
  - [ETL Process](#ETL-Process)
  - [Data Modelling](#Data-modelling)
  - [DAX Measure Created](#DAX-Measure-created)
  - [Analysis](#Analysis)
  - [Visualisation](#Visualisation)
- [Detailed Insights and Recommendations](#Detailed-Insights-and-Recommendation)
  - [Dashboard 1](#Sales-Pulse-Performance,-Frequency-&-Return-(Executive-Overview))
  - [Dashboard 2](#Sales-Performance-&-Customer-Behaviour-(Net-sales-by-Customer-Demographic))
  - [Dashboard 3](#Product-portfolio-performance-(Based-on-Gross-Proft))
 
# Project Title:
Hola Retail Group: Customer & Sales Behaviour and Product Profitability


# My Role:
Business/Data Analyst

- Designed and developed the Microsoft Access database structure used to store customer, product, transaction, and store data.
- Built and deployed interactive Power BI dashboards for business insights.
- Conducted data modelling, cleaning, and transformation across multiple tables.
- Delivered actionable insights to support strategic decision-making on customer behaviour, sales performance, and product profitability.

# Project Overview

This project analyses customer behaviour, product performance, and store profitability using data sourced from an Access database. By building interactive Power BI dashboards, the project provides insights into customer demographics, seasonal sales trends, product return rates, and gross profit margins. The goal is to support data-driven decisions for product promotion, customer targeting, and operational optimization.

# Problem Statement

- Understand overall sales performance in a way that highlights areas for improvement.
- Identify key patterns in customer behaviour, such as how demographics, geography, and return trends affect profitability.
- Evaluate product performance—especially across multiple categories like cookie types—based on gross profit and customer preferences and understanding products purchases and return pattern.

This project addresses these gaps by delivering actionable, visual insights into sales trends, customer segmentation, and product-level profitability. It empowers stakeholders to make informed decisions around marketing, inventory management, customer retention, and product strategy.

# Stakeholder Engagement
### Target Stakeholder
    - Primary: Sales and Marketing Executive
    - Secondary: Store Managers, Inventoryand Customer Insights Team

### Use Cases
- Identify the top-performing products by gross profit and net sales.
- Segment customers by demographics, geography, and buying frequency.
- Detect seasonal trends in product demand and return behaviour.
- Support decision-making for marketing campaigns and inventory optimization.

### Stakeholder Stories
- As a Sales Manager, I want to identify profitable products and loyal customers so that I can boost sales and customer retention.
- As a Marketing Executive, I want to understand customer behaviour by age group, gender, and location to create targeted campaigns.
- As a Store Manager, I want to anticipate seasonal sales trends so that I can manage inventory effectively.

### Acceptance Criteria
The dashboard should:  
- Display key KPIs such as Total Revenue, COGS, Profit, Sold Quantity, and Returned Quantity.
- Allow filtering by product type, customer demographics, and geography.
- Visualize monthly trends in sales and returns.
- Provide insights into customer purchase frequency and return rates.

### Success Criteria
- Stakeholders can easily identify top-performing products and customer segments.
- Marketing teams can design targeted campaigns based on customer demographics.
- Store managers can prepare for peak sales seasons and minimize product returns.
- Data-driven insights support better marketing, inventory, and operational decisions.

# Data Source

### Access Database Structure
- Customer Table: Including demographics, contact info, and location

| Column Name | Data Type | Description |
| --- | --- | --- |
| Column ID | AutoNumber | Unique Identifier of each customer |
| First Name | Short text | Customer first name |
| Last Name | Short text | Customer last name |
| Gender | Short text | Sex orientation of each customer |
| Marital Status | Short text | Marital status of customer |
| Birth Year | Data/Time | Date of birth of customer |
| Email Address |  Short text | Email Address contact of each customer |
| Phone Number | Short text | Telephone or Mobile contact of each customer |
| Address | Short text | Housing Address of each customer |
| City | Short text | City the customer house address is |
| State | Short text | State the customer house address is |
|  Zip code | Short text | Customer address zip code |
| Country | Short text | Country customer state and city is located |
| Note | Long text | brief note that describes customer engagement with product and purchases |
    ## insert table

- Product Table: Lists cookie type, pricing, and ingredients

| Column Name | Data Type | Description |
| --- | --- | --- |
| Product ID | AutoNumber | Unique Identifier of each product |
| Product Name | Short text | Product name |
| Product Category | Short text | Product category name |
| Recipes | Short text | Compilation of all recipes used to make the product |
| Unit Cost | Currency | Cost per unit of each product |
| Unit Price | currency | Price per unit of each product |

    ## insert table



- Transaction Table: Tracks order details, quantities, returns and revenue

| Column Name | Data Type | Description |
| --- | --- | --- |
| Order ID | AutoNumber | Unique Identifier of each customer |
| Customer ID | Number | Foreign key referencing the Customer table (Customer ID) |
| Product ID | Number | Foreign key referencing product table (Product ID) |
| Order Date | Date/Time | Date of each product quantity order from each customer |
| Quantity Order | Number | Quantity of product order by customer |
| Order filled | Yes/No | If purchases have been fulfilled or not |
| Unit Price |  Currency | Price per unit of product quantity sold |
| Revenue | Calculated | multiplication of Unit Price and Quantity ordered |
| Return | Number | return product quantity count |

    ## insert table

### Benefit of Access Storage

- Easy to manage and query structured relational data
- Suitable for prototyping dashboards and small business use
- Provides a centralized source for transactional and reference data

# Methodology 

### Technical Tools Used:
- Microsoft Access – for storing and managing data
- Power BI – for building dynamic dashboards and data visualizations
- Power Query – for ETL process
- Excel (optional) – for basic cleaning or pivoting if needed

### Development:

What is the general approach in creating this solution from start to finish

- Designed database tables with mock data
- Create a relationship between table in the Access database environment
- Imported data into Power BI Desktop.
- Perform ETL (Extract, transformed and Load) with Power Query
- Conducted data Validation and cleaning 
- Created a dynamic date table for time-based reporting.
- Developed DAX measures to enrich insights.
- Generate the findings based on insights. 
- Document every process and Commentary
- Built and published interactive dashboards in Power BI service.
- Publish the Project to GitHub Pages.

### Process

#### Data Exploration & Cleaning
- 
    1. Handling missing values and duplicates.
    2. Anew column to convert birth year to age.
    3. Normalise product and customer dimension.
  4. Merged First Name and Last Name columns in the customer table to create a full name column.
  5. Combined the Transaction and Product tables using a common key (product ID) to bring in Unit Cost and Unit Price into the transaction-level dataset.
  6. Addes calculated columns:
        - COGS (Cost of Goods Sold)
        - Net Sales
        - Gross Profit 
        - Returned Salesis 
        - Sales 
        
        These enriched metrics support deeper profitability and performance analysis.
        
        - Created an automated Date Dimension table to support time-based reporting using:
            1.	= Date.StartOfYear(List.Min(#"Transaction_Tbl"[Order Date]))
            2.	= Date.EndOfYear(List.Max(#"Transaction_Tbl"[Order Date]))
            3.	= {Number.From(#"StartDate")..Number.From(#"EndDate")}

#### Data Modelling

- Structured the data into a star schema, linking fact and dimension tables (Customer, Product, Store, Transaction).
- Ensured relationships support accurate cross-table filtering and aggregation.

    ![Hola data model](Assets_Folder/Images/Hola_Data_Model.png)

  From the above Power BI data model pane image above we can see that a many to one (*:1) was establish between the Transaction table (The Fact Table) and Dimensions Table (Product, Customer, and date table).The other tables shown are the Dax measure and measure documentation tables.  

#### DAX Measures Created
- Total Revenue = SUM(Transaction[Revenue])
- COGS = SUM(Transaction[COGS])
- Gross Profit = [Total Revenue] - [COGS]
- Return Rate = DIVIDE(SUM(Transaction[Returned Quantity]), SUM(Transaction[Sold Quantity]))
- Net Sales = SUM(Transaction[Revenue]) - SUM(Transaction[Return])


#### Analysis:

- Net Sales to Customer segmentation by gender, age, location, and marital status
- Product performance by type, unit price, and return rate
- Sales trends by month and region
- Profitability by cookie type and individual product
- Store-level cost analysis (for future expansion)

#### Visualization:
- Interactive dashboards for executives
    1.	Actionable insights into overall sales performance, customer behaviour, and potential improvement areas, enabling stakeholders to make informed strategic decisions.
    2.	Analyses net sales by gender and customer demographics, return behaviour, geography, and purchasing patterns.
    3.	Insights focus on cookie category performance in terms of gross profit, customer behaviour, and sales insights.

- Designed slicers and KPIs to enable real-time, self-service analytics for stakeholders.

[![View Report](https://img.shields.io/badge/View%20Power%20BI%20Report-Click%20Here-blue)](https://app.powerbi.com/reportEmbed?reportId=3b68d49b-8c18-48c1-9783-0740d28fb8b9&autoAuth=true&ctid=2a305761-f97d-47e4-8f0f-a6c20c3feb73)


    ### Click on the above link to fully interact with the Power Bi Report

# Detailed Insights and Recommendation 

### DASHBOARD 1: SALES PULSE - PERFORMANCE, FREQUENCY & RETURN (Executive Overview)

![Dashboard 1](Assets_Folder/Images/Dashboard_1.gif)

#### KPI CARDS (Top Section)
- Total Sales (£4.4M):  
    Indicates the overall revenue generated by sales activities. Where the Revenue accounted for is the revenue generated before sales amount impacted.
- Cost of Goods Sold (COGS, £3.8M):  
    Reflects the direct costs incurred in producing goods sold, which is costing a percentage of ----- out of the Total Revenue. (Pricing strategies needs to be adjusted)
- Total Order (2.77K):  
    Represents the number of orders placed which is a healthy volume of sales activity.
- Profit (£665K):  
    Indicates net earnings from sales after subtracting costs, highlighting profitability.
- Sold Quantity (357K):  
    Reflects the total volume of items sold, which helps assess inventory movement demand performance of products.
- Returned Quantity (8K):  
    Shows returns, a vital indicator of product quality, customer satisfaction, or potential issues with specific products.

#### Targeted Vs. Actual Revenue
- Target Revenue (£4.47M) vs. Actual Revenue (£4.36M):  
    Actual revenue slightly missed the target, indicating the team nearly achieved the financial goal. This indicates need for minor/large scale adjustments in pricing             strategies.

#### Total Purchase by Purchase Frequency Category:
- 41-60 Category (515 Purchases):  
    The largest purchases frequency falls within 41-60 category, indicating that come customers has purchases any of the products between 41 – 60 times this show a strong,         loyal customer base that frequently engages with the business.
- 61-80 category (436 purchases):  
    Another significant purchases category showing substantial loyalty and engagement.
- Smaller segments (1-10, 11-25, etc.):   
    Offer opportunities to convert occasional buyers into more frequent, loyal customers through targeted marketing or incentives

#### Customer Return Rate Breakdown:
- Moya, Paddy, Emily, Taiye, Drake, Jacob, Keith, James, Sharon:
    Lists customers with the highest return rates, providing insights into customers who may have experienced product issues or dissatisfaction.  
        - Moya has the highest return rate (7.2%), suggesting targeted investigation or follow-up may be necessary.
        - The list would help to pinpoint potential areas for improving product quality, customer service, or logistical processes.

#### Monthly Sales Trend:
- Peak in July:  
    July experienced the highest sales revenue but also recorded a notable spike in returned sales, indicating a potential correlation between high sales and increased             returns. Seasonal effects or promotional impacts should be reviewed.
- Decline in August-November:  
    A significant drop following July, possibly indicating seasonal effects, changes in marketing, or demand fluctuations. Although this is also because of the dataset hasn’t     been updated with the latest records from the data source.
- Low returns:  
    Outside the July spike, returned sales remain consistently low, suggesting overall good customer satisfaction and product quality outside this specific period.

#### Key Recommendations for Stakeholders:
- Revenue & Profitability:  
    - Enhance marketing and sales strategies slightly to bridge the small gap between target and actual revenue.
- Cost Efficiency:  
    - I will strongly recommend evaluation of COGS to identify cost-saving opportunities to improve profitability.
- Customer Retention & Engagement:  
    - Focus on high-frequency customers (41-60 and 61-80 purchases) to maintain loyalty through targeted promotions.
    - Implement strategies to upgrade customers from lower frequency categories.
- Returns Management:  
    - Investigate high return rates from specific customers to reduce returns, improve satisfaction, and potentially save costs.
- Seasonal Analysis:  
    - Anticipate the July spike and subsequent decrease in sales by adjusting inventory, marketing budgets, and staffing accordingly.



### DASHBOARD 2: SALES PERFORMANCE & CUSTOMER BEHAVIOUR DASHBOARD (Net sales by Customer Demographic)

![Dashboard 2](Assets_Folder/Images/Dashboard_2.gif)  

Goal: The dashboard analyses net sales by gender and customer demographics, return behaviour, geography, and purchasing patterns.

#### Customer Gender-Based Sales Summary
Male Customers  
    - Net Sales: £2.45M  
    - Number of Male Customers: 20  
    - Trend: Strong performance, especially between July and August with peak net sales.  

Female Customers  
    - Net Sales: £1.88M  
    - Number of Female Customers: 18  
    - Trend: Similar pattern as males, peaking mid-year but with slightly lower values.  
    
 Insight: Despite similar customer count, male customers contribute more to overall sales, indicating higher average spend or order volume.

#### Gender Sales Trends by Month
- Monthly trends suggest mid-year (June to August) is the peak for both genders. Useful for inventory planning, staffing, and promotions.

#### Net Sales by Top 10 Customers
- Top Contributor: Diego – (£392.01K), Emily - (£258.95K), Daniel - (£225.17K)
- Others (e.g., Emma, Daniel, Becky) contribute between £157K–£258K.

Insight: Heavy reliance on a few key customers. A risk if top contributors churn, but also an opportunity to strengthen loyalty through incentives.

#### Geographical Distribution (Tree Map):
United States & United Kingdom are key regions:  
    - Top States in the U.S.: California (£33K), Texas (£31K), New York (£24K). 
    - Top UK Cities: Chester (£50K), Slough (12.4K), Manchester () Reading (10K+ each). 
    - Top Province in Canada: Vancouver (19K), Quebec (14K) Alberta (12K). 
    
 Insight: Sales are well-distributed, with strong performance in California, Texas, and Chester. Use this to tailor regional campaigns.

#### Total Return Quantity
- Overall Returns: 8,368 units
- By Gender:  
    - Male: 4,268
    - Female: 4,020
        
Insight: Return behaviour is fairly balanced between genders. However, male customers return slightly more. Monitor for quality or service issues.

#### Customer Demographics - Age Distribution:
Highest Concentration:
    - 31-35 age group: 1,512 customers
    - Followed by 20-25 and 26-30 age groups
    
Insight: Majority of buyers fall between 20–35 years – a young and potentially brand-loyal segment. Tailor product and marketing strategies toward this demographic.


#### Repeated Purchases by Age Categories
- Top Repeat Buyers:
    - 31–35 (31.6%)
    - 26–30 (21.1%)
- Lower Repeats:
    - 46–50 and 51–55 age groups (<6%)

Insight: Young adults (especially 31–35) are most likely to make repeated purchases – this group is your core recurring customer base. Consider loyalty programs and personalized engagement for this age band.


#### Key Recommendations for Stakeholders:
- Focus on Ages 26–35:
    - This age bracket shows both high engagement and repeat purchases. Invest in digital campaigns, referrals, and targeted loyalty programs for this group.
- Engage High-Spending Males:
    - Males are higher contributors to net sales. Use tailored offers, product bundles, or premium experiences to boost retention.
- Customer Diversification:
    - Top 10 customers form a large share of revenue. Mitigate risk by expanding efforts to nurture mid-tier customers.
- Address Product Returns:
    - Investigate common causes of returns—are they product-specific, seasonal, or service-related?
- Capitalize on Peak Months:
    - Prepare for high sales during June–August with optimized stock, marketing pushes, and support.
- Geo-Focused Strategy:
    - Double down on high-performing regions like California, Texas, and Chester, with regional campaigns and fulfilment optimization.


### DASHBOARD 3: HOLA PRODUCT PORTFOLIO PERFORMANCE (Based on Gross Profit)

![Dashboard 3](Assets_Folder/Images/Dashboard_3.gif)

#### KPI Cards (Top Section): 
Indicates net earnings from sales after subtracting costs, highlighting profitability for each cookies category.

- Classic Cookies Profit – (£182.9K)
- Basic Cookies Net Profit- (£174.4K)
- Christmas Cookies Net Profit – (£166.2K)
- Healthy Cookies Net Profit – (£141.2K)

Insight: Classic cookies lead in profit, with Healthy cookies performing lowest, suggesting room for marketing or recipe improvement in the health-conscious category.

#### Top-Selling Cookie by Name
- Peanut Butter is the highest-grossing individual cookie at £61K.
- Other top contributors:
    - Macaron (£56K)
    - Sugar (£41K)
    - Cookies with Cream (£40K)
    - Refrigerator (£39K)

Insight: Peanut Butter and Macaron dominate, showing strong customer preference. Consider bundling or promotions around these.

#### Return Quantity by Cookie Type  
- Highest Returns:
    - Classic (31%)
    - Basic (28.7%)
- Lowest Returns:
    - Christmas (18.5%)

Insight: Classic and Basic types have higher return rates. Investigate potential quality issues, delivery problems, or mismatched customer expectations.

#### Total Orders by Cookie Type  
- Christmas cookies have the most orders (922), despite being seasonal.
- Basic (643), Healthy (612), and Classic (589) follow.

Insight: Strong order volume for Christmas cookies indicates peak seasonal demand—opportunity to expand festive variants or increase stock planning for Q4.

#### Gross Profit Over Time by Cookie Type
- Christmas cookies peak between October–December.
- Classic and Basic show steady sales across most months.
- Healthy cookies show modest but steady growth mid-year (May–August).

Insight:  
- Optimize seasonal campaigns around Christmas.
- Leverage mid-year interest in Healthy cookies (possibly driven by summer or fitness trends).


#### Key Recommendations for Stakeholders:

- Double down on Peanut Butter, Macaron, and Sugar cookies
    - Promote these across channels and explore new variants.
- Address return rates in Classic & Basic cookies
    - Conduct quality assurance or gather customer feedback.
- Capitalize on seasonal demand for Christmas cookies
    - Expand product lines or launch early-bird festive promotions.
- Boost Healthy cookie appeal
    - Highlight health benefits, reformulate recipes, or rebrand to attract more health-conscious buyers.
- Use top-selling cookie data to inform bundling strategies
    - Pair popular cookies with slower sellers to balance inventory movement.







    







