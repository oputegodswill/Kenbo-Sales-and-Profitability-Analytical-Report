KENBO SALES AND PROFITABILITY ANALYSIS REPORT
Technical Report | Analyst: Godswill Opute
Dataset: sales_analysis.csv (10,000 orders, 13 fields) | Tool: Power BI 

<img width="1366" height="816" alt="DASHBOARD" src="https://github.com/user-attachments/assets/bf7c32e1-a3e5-43fa-bcc2-a8461ee20889" />

 
Kenbo Sales and Profitability Dashboard built in Power BI
1. Introduction
I analyzed sales and profitability data for Kenbo. The dataset contains 10,000 order records with 13 fields including Order_Date, Region, Product_Category, Customer_Segment, Quantity, Unit_Price, Discount_Rate, Revenue, Cost, Profit, and Payment_Method. I performed the entire analysis and visualization in Power BI and built the dashboard shown above.
2. Objective
My objectives were:
1. To calculate total revenue $11,952,419.48 and total profit $4,189,497.68 and identify peak month, top region, largest customer segment, and top product category.
2. To measure sales trend over time and identify seasonal patterns.
3. To analyze revenue by product category, regional revenue, profit by customer segment and payment method, and revenue by customer segment.
4. To identify payment method profitability and customer segment contribution.
5. To build a single Power BI dashboard that consolidates sales and profitability KPIs.
3. Data Story
Scale: I analyzed 10,000 orders generating $11,952,419.48 total revenue and $4,189,497.68 total profit. Profit margin = 35.05% (Profit/Revenue).

Top KPIs I found:
- Revenue Peak Month: July $1,049,945.00 (dashboard shows 1049.95K) - highest monthly revenue.
- Top Region By Revenue: North $3,038,232.15 (3038.23K) - 25.42% of total.
- Largest Customer Segment: Corporate $3,994,927.24 (3994.93K) - 33.43% of revenue, followed by Home Office $3,979,059.12 and Consumer $3,978,433.12 - almost equal.
- Top Product Category: Electronics $2,433,318.37 (2433.32K) - 20.36% of total revenue, followed by Beauty $2,427,867.16.

Regional Mix: North $3,038,232.15, East $2,987,841.70, West $2,983,709.68, South $2,942,635.95 - North leads by only $95k (3.2% variance) - very balanced, no region dominates.

Product Mix: Electronics $2,433,318.37, Beauty $2,427,867.16, Sports $2,380,619.74, Home & Kitchen $2,377,096.07, Clothing $2,333,518.14 - Electronics top but only 4.3% above Clothing - balanced portfolio.

Monthly Trend: January $1,030,685.81, February dip $953,256.37, April low $979,309.98, July peak $1,049,945, September peak $1,046,701.70, November dip $918,265.05, December recovery $1,008,849.83 - U-shaped with two peaks.
4. Stake-holders
Management & CEO: My top 4 KPI cards (Revenue Peak Month July, Top Region North, Largest Customer Segment Corporate, Top Product Category Electronics) give instant view of performance. North and Electronics are consistent winners.

Finance Team: My Regional Revenue bar (North 3038.23K, East 2987.84K, West 2983.71K, South 2942.64K) and Revenue by Customer Segment bar (Corporate 3994.93K, Home Office 3979.06K, Consumer 3978.43K) show balanced revenue distribution - no concentration risk.

Sales & Marketing: My Sales Trend over time line chart shows monthly fluctuations - February and November dips need investigation, July and September peaks should be replicated. Revenue by Product Category bar shows Electronics and Beauty top - focus marketing there.

Operations: Regional Revenue balanced - inventory can be distributed evenly across 4 regions.

Customer Insights: Profit by Customer Segment donut - Corporate 33.43%, Home Office 33.33%, Consumer 33.25% - perfectly balanced, no segment dominates profit. Corporate slightly highest profit $1,400,460.21.

Payment Team: Profit by Payment Method pie - Debit Card 20.51% ($859,227.34) top, UPI 20.33% ($851,559.69), Cash on Delivery 20.31% ($851,024.82), Credit Card 19.7% (~$826k), Net Banking 19.12% ($801k) - balanced, no payment method dominates profit.
5. Tools Used
I used Power BI.

I imported sales_analysis.csv (10,000 rows) as CSV source in Power BI Desktop. In Power Query, I transformed Order_Date from Excel serial (45522 etc.) to date, extracted Month Name and Year, checked for nulls - 0 nulls. I created calculated columns and measures in DAX:
- Total Revenue = SUM(Revenue) = $11,952,419.48
- Total Profit = SUM(Profit) = $4,189,497.68
- Profit Margin = DIVIDE([Total Profit], [Total Revenue]) = 35.05%
- Peak Month = CALCULATE(MAX) logic - July $1,049,945.
- Top Region = MAX Region by Revenue - North $3,038,232.15.
- Largest Customer Segment = MAX Segment by Revenue - Corporate $3,994,927.24.
- Top Product Category = MAX Category by Revenue - Electronics $2,433,318.37.
I built visuals: Cards for top KPIs with dark background, Line chart for Sales Trend over time (Order_Date Month to Axis, SUM(Revenue) to Values with data labels 1030.69K etc.), Column chart for Revenue by Product Category (Product_Category to Axis, SUM(Revenue) to Values), Donut chart for Profit by Customer Segment (Customer_Segment to Legend, SUM(Profit) to Values with % labels 33.43% etc.), Bar chart for Regional Revenue (Region to Axis, SUM(Revenue) to Values), Pie chart for Profit by Payment Method (Payment_Method to Legend, SUM(Profit) to Values with % labels), and 100% stacked bar for Revenue by Customer Segment (Customer_Segment to Axis, SUM(Revenue) to Values).
I assembled dashboard in Power BI with beige background, dark gray KPI cards, and synchronized slicers.
6. Pre-Analysis Board
In Power Query, I confirmed 10,000 rows, 13 columns, 0 critical nulls. Revenue SUM $11,952,419.48 validated, Profit SUM $4,189,497.68 validated. Order_Date range Excel serial 45462 (2024) to 45522 - converted to 2024 dates, but dashboard shows 12 months trend (Jan-Dec) with July peak - data spans one full year.
I checked dimensions: Region 4 unique (North 2,548 orders, East 2,506, West 2,486, South 2,460 - balanced), Product_Category 5 unique (Electronics, Beauty, Sports, Home & Kitchen, Clothing), Customer_Segment 3 unique (Corporate, Home Office, Consumer - almost equal 33% each), Payment_Method 5 unique (Debit Card 2,074, Cash on Delivery 2,017, UPI 2,011, Credit Card 1,963, Net Banking 1,935 - balanced).
I identified need to create Month hierarchy and Year filter.
7. In-Analysis Board
In Power BI Report View:
Built Top KPIs using DAX measures - Revenue Peak Month = July $1,049,945, Top Region = North $3,038,232.15, Largest Segment = Corporate $3,994,927.24, Top Category = Electronics $2,433,318.37.
Built Sales Trend over time line chart - Order_Date Month to X-axis, Revenue to Y-axis, with data labels: Jan 1030.69K, Feb 953.26K (dip), Mar 992.36K, Apr 979.31K, May 1014.43K, Jun 987.70K, Jul 1049.95K (peak), Aug 996.24K, Sep 1046.70K (second peak), Oct 974.67K, Nov 918.27K (lowest), Dec 1008.85K (recovery).
Built Revenue by Product Category column chart - Product_Category to X, Revenue to Y: Electronics 2433.32K tallest, Clothing 2333.52K shortest.
Built Profit by Customer Segment donut - Customer_Segment to Legend, Profit to Values: Corporate 33.43% ($1,400,460.21), Home Office 33.33% ($1,396,206.25), Consumer 33.25% ($1,392,831.22) - almost equal.
Built Regional Revenue bar - Region to Y, Revenue to X: North 3038.23K top, South 2942.64K bottom.
Built Profit by Payment Method pie - Payment_Method to Legend, Profit to Values: Debit Card 20.51% ($859,227.34) top, Net Banking 19.12% bottom.
Built Revenue by Customer Segment 100% bar - Customer_Segment to Y, Revenue to X: Corporate 3994.93K, Home Office 3979.06K, Consumer 3978.43K.
Validated all numbers against raw CSV - totals match exactly.
8. Dashboard
My Power BI dashboard (DASHBOARD.png) has 3 layers:

Top Layer - 4 KPI Cards (dark gray background white text): Revenue Peak Month July, Top Region By Revenue North, Largest Customer Segment Corporate, Top Product Category Electronics.

Middle Layer:
- Sales Trend over time: Line chart Jan-Dec, Y 900K-1100K, peak July 1049.95K, second peak Sep 1046.70K, lowest Nov 918.27K, shows fluctuating but stable around 1M per month.
- Revenue by Product Category: Column chart 5 categories 2M scale, Electronics 2433.32K tallest, Clothing 2333.52K shortest - balanced.
- Profit by Customer Segment: Donut chart 33.43% Corporate, 33.33% Home Office, 33.25% Consumer - perfectly balanced.

Bottom Layer:
- Regional Revenue: Horizontal bar, North 3038.23K top, South 2942.64K bottom - only 95K difference.
- Profit by Payment Method: Pie chart, Debit Card 20.51%, UPI 20.33%, Cash on Delivery 20.31%, Credit Card ~19.7%, Net Banking 19.12% - balanced.
- Revenue by Customer Segment: Horizontal 100% bar, Corporate 3994.93K, Home Office 3979.06K, Consumer 3978.43K - balanced.

Design: Beige background, dark gray KPI cards, black and gray bar colors, clean Power BI layout.
9. Observation
1. Balanced revenue distribution: Regions North $3.03M to South $2.94M only 3.2% variance, Customer Segments Corporate $3.99M to Consumer $3.97M only 0.4% variance, Payment Methods profit 19.12% to 20.51% only 1.4% variance, Product Categories $2.33M to $2.43M only 4.3% variance - highly diversified business, no concentration risk - this is ideal from risk management perspective.
2. Seasonal trend: Sales Trend shows two peaks July $1,049,945 and September $1,046,701.70, and two dips February $953,256 and November $918,265. November dip is 12.5% below July peak - significant - needs investigation. December recovery $1,008,849 suggests holiday push.
3. High profit margin: Total profit $4,189,497.68 on revenue $11,952,419.48 = 35.05% margin - healthy, indicates good cost control (Cost = Revenue - Profit = $7.7M).
4. Electronics leads but marginally: Electronics $2,433,318 is top but only $99k above Beauty $2,427,867 - small lead. Category leadership not strong.
5. Corporate segment slightly more profitable: Corporate profit $1,400,460.21 is highest, but only $7k more than Consumer $1,392,831 - minimal difference.
6. Payment method profitability balanced: Debit Card profit $859,227 top, Net Banking $801,196 bottom - $58k difference (7%) - no payment method dominates profit, good for payment flexibility.
10. Recommendation
1. Investigate November dip: November revenue $918,265 is lowest, 12.5% below July peak $1,049,945. I should drill down in Power BI by Region and Product_Category for November to find cause and prevent next year - maybe launch promotion in November.
2. Replicate July strategy: July peak $1,049,945 and September peak $1,046,701 - analyze what products and regions drove these peaks and replicate marketing campaigns in same months next year.
3. Maintain balanced portfolio: Since all regions, segments, payment methods, and categories are balanced (3-4% variance), I should continue diversification strategy - do not over-invest in one category like Electronics, maintain all 5 categories.
4. Focus on Electronics and Beauty: They are top 2 revenue categories ($2.43M and $2.42M) - allocate slightly more marketing budget and inventory to them to widen lead.
5. Optimize payment costs: Profit by Payment Method shows Debit Card and UPI most profitable - encourage these low-cost payment methods over Credit Card which has higher processing fees, to increase margin above 35%.
6. Protect Corporate segment: Corporate is largest segment $3,994,927 and highest profit $1,400,460 - build loyalty program for Corporate customers to retain them.
7. Plan inventory for North: North is top region $3,038,232 - ensure inventory availability in North, especially for Electronics and Beauty in July and September peaks.
11.
. Summary
I used Power BI to analyze 10,000 Kenbo orders generating $11,952,419.48 total revenue and $4,189,497.68 total profit with 35.05% profit margin.
I found July is peak month with $1,049,945, North is top region with $3,038,232.15, Corporate is largest customer segment with $3,994,927.24, and Electronics is top product category with $2,433,318.37.
My analysis shows a highly balanced and diversified business - all 4 regions within 3.2% variance, all 3 customer segments within 0.4% variance, all 5 payment methods within 1.4% variance, and all 5 product categories within 4.3% variance - indicating low concentration risk and good risk management.
Seasonal trend shows peaks in July and September and dips in February and November, with healthy 35% profit margin.
My Power BI dashboard provides a single-page view to monitor sales and profitability by month, region, product category, customer segment, and payment method for stakeholders.
