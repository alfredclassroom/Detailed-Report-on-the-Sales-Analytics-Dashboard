# Detailed-Report-on-the-Sales-Analytics-Dashboard
This dashboard provides a multi-dimensional view of Safisana’s financial and operational performance over several years. It helps the management team
Track and compare Sales and Operational Costs annually

Monitor key Production Outputs (Electricity and Fertilizer)

Evaluate Profitability, both generally and by specific waste types

Identify trends and anomalies in monthly sales performance

Detailed Insights from Each Visual
1. Yearly Electricity Generated (Bar Chart)

    Highest production: 2022 (1.26M) and 2024 (1.13M).

    Lower in years like 2020 and 2018, suggesting production capacity or resource supply may fluctuate.

    2022 stands out for performance, potentially reflecting operational stability.

2. Yearly Fertilizer Produced

    Consistent production: ranges from 1.02M to 1.18M tons.

    Fertilizer output is steady but peaked in 2022 and 2020.

    May be linked to operational cost efficiency or waste processing volumes.

3. Yearly Operational Cost (Donut Chart)

    Fairly evenly distributed among years (each about 10-11%).

    Suggests operational cost is relatively stable year-to-year with minor variations.

    2023 and 2024 slightly higher costs (~11.8% and 11.1%).

4. Yearly Profit Margin by Waste Type

    Waste IDs like 805, 802, 900, 968 show very high margins (44% to 57%).

    Negative margins seen for IDs like 1038 (-6.39%), 1061 (-10.21%), and 1092 (-41.95%).

    Suggests a need to reassess waste sourcing, pricing, or processing strategies for low-performing waste streams.

5. Yearly Profit Margin (Bar Chart)

    Peak margin: 2017 (33.58%), followed by 2018 and 2016.

    Margins have declined in 2020, 2022, and 2024.

    Indicates either rising costs or weaker sales pricing in recent years.

6. Monthly Sales (Line Chart)

    Sales show seasonal or cyclical patterns, with some peak months each year.

    Recent years show flatter performance than earlier years.

    Suggests slower recovery or demand pressure post-peak seasons.

7. Yearly Top Sales (Bar Chart)

    Highest sales recorded in 2024 (12.1K) and 2022 (12.5K).

    Gradual increase in sales units over time — positive growth despite margin pressure.

    Indicates operational scaling and market expansion potential.

📌 Dashboard Summary & Recommendations
✅ What’s Working Well

    Electricity and fertilizer production are consistent.

    Waste sources like 802, 805, and 900 are highly profitable.

    Top sales volumes have grown year-over-year.

⚠️ Areas of Concern

    Sales and margins are declining, possibly due to cost increases or pricing inefficiencies.

    Some waste streams are generating negative profit margins, dragging down overall performance.

    Operational costs remain significant, though somewhat stable.

📈 Recommendations

    Deep-dive into low-margin waste IDs and optimize or discontinue them.

    Review pricing strategy – especially for fertilizer products.

    Increase focus on high-performing waste types like 805 and 968.

    Evaluate seasonal patterns to optimize production and sales push.

    Invest in cost optimization without sacrificing production quality.

Detailed Report and DAX Analysis
🔹 1. List of Measures with Explanations
Measure Name	DAX Formula	Purpose / Insight
Total Sales	SUM(Safisana_Sample_Data[Total_Sales_GHS])	Calculates overall sales revenue in Ghana Cedis. Key revenue performance indicator.
Total Sales LY	CALCULATE([Total Sales], DATEADD('Date Table'[Date], -1, YEAR))	Compares current total sales to the same period last year (Year-over-Year).
Total Profit	SUM(Safisana_Sample_Data[Profit_GHS])	Total net profit over selected period.
Total Profit LY	CALCULATE([Total Profit], DATEADD('Date Table'[Date], -1, YEAR))	YoY profit comparison.
Total OPP_Cost	SUM(Safisana_Sample_Data[Operational_Cost_GHS])	Shows total operational expenditure. Helps in cost control analysis.
Total OPP_Cost LY	CALCULATE([Total OPP_Cost], DATEADD('Date Table'[Date], -1, YEAR))	Tracks operational cost trend YoY.
Profit Margin	DIVIDE([Total Profit], [Total Sales])	Indicates operational efficiency and profitability (% of revenue retained as profit).
Profit Margin LY	CALCULATE([Profit Margin], DATEADD('Date Table'[Date], -1, YEAR))	Tracks improvement/decline in profitability YoY.


Insights from KPIs, Charts, and Graphs

Assuming your dashboard contains visuals like card KPIs, bar/line charts, and maybe a YoY trend line, here’s what each metric typically reveals:
✅ KPI Cards (Big Numbers)

    Total Sales: Overall company revenue. If increasing, market demand is likely growing or sales efforts are more effective.

    Total Profit: Indicates efficiency — high profits with stable/reduced costs suggest improved margin or product pricing.

    Profit Margin: A high margin (say, 20%+) is great. If margin is decreasing while sales rise, costs may be increasing faster than revenue.

    Total OPP_Cost: Helps spot inefficiencies. A rising cost trend should be justified by rising sales/profit — else it’s a red flag.

📈 Year-over-Year (YoY) Comparisons

    Sales/Profit/Cost YoY Charts: Compare current vs previous year performance.

        If Total Sales is up, but Profit Margin is down, costs are rising.

        If Sales and Profit Margin both drop, investigate sales strategy or external factors (e.g., fuel prices, supply chain).

📉 Line Charts

    Likely used to display trends over time (monthly/quarterly):

        Identify seasonality in sales or costs.

        Useful for forecasting future performance using historical trends.

📊 Bar/Column Charts

    Often show category-level breakdowns (e.g., by product, region, waste type):

        Which departments/products generate the most sales or incur the highest cost.

        If using a date hierarchy (Year → Month), bar charts can show monthly comparisons or growth.

📌 Summary of the Dashboard

This dashboard likely helps Safisana:

    Track overall financial health via Total Sales, Profit, and Profit Margin.

    Compare performance year-over-year to assess growth and seasonal patterns.

    Monitor operational costs to identify areas for cost control.

    Gain insights into efficiency and profitability trends, critical for sustainability and investment.

🔁 How to Replicate This Dashboard Step-by-Step
🛠️ 1. Data Import

    Import your Excel or CSV with fields like:

        Date, Total_Sales_GHS, Profit_GHS, Operational_Cost_GHS

🧱 2. Modeling

    Create a Date Table (mark it as Date Table).

    Link Date field in Safisana_Sample_Data to Date Table[Date].

🧮 3. Create Measures (DAX)

Paste the DAX formulas for:

    Total Sales, Total Profit, Total OPP_Cost, and their LY counterparts

    Profit Margin and Profit Margin LY

📐 4. Create Visuals

    KPI Cards: For Sales, Profit, Profit Margin, OPP Cost

    Line Chart: Sales/Profit over time (monthly)

    Bar Chart: Compare current vs LY sales/profit

    YoY Comparison Chart: Add small multiples if needed

🎨 5. Add Filters/Slicers

    Use filters for Year, Month, or Location (if applicable)

✏️ 6. Design Tips

    Use consistent colors (e.g., green = profit, red = cost)

    Add titles like “Safisana Operations Dashboard” and date slicers

    Consider using Tooltips to show LY values or % change



Executive Summary

The dashboard offers a comprehensive view of Safisana Ghana Ltd's financial and operational performance across several KPIs, including sales, operational cost, electricity generation, fertilizer production, profit margins, and monthly trends.

Despite strong production figures, sales and profits have declined compared to the previous year, indicating inefficiencies or external pressures affecting revenue and margins.
📊 Key Performance Indicators (KPIs)
1. Sales – Current vs Prior Year

    Current: GH₵1,399,034

    Prior Year: GH₵1,504,876 → ↓ 7.03%

    📉 Insight: There's a year-over-year decline in revenue, signaling possible market contraction, pricing issues, or demand reduction.

2. Operational Cost – Current vs Prior Year

    Current: GH₵1,064,685

    Prior Year: GH₵1,129,351 → ↓ 5.73%

    📉 Insight: A slight reduction in costs, which is positive, but not enough to offset the fall in revenue.

3. Profit – Current vs Prior Year

    Current: GH₵334,349

    Prior Year: GH₵375,525 → ↓ 10.96%

    📉 Insight: Profits have fallen significantly more than revenue, suggesting margin compression or fixed costs impact.

4. Profit Margin – Current vs Prior Year

    Current: 23.90%

    Prior Year: 24.95% → ↓ 4.23%

    📉 Insight: Profitability per cedi of sales has slightly decreased. Efficiency and value capture may be declining.

⚡ Operational & Production Analysis
5. Yearly Electricity Generated

    Most recent (2024): 1.13M kWh, down from a peak of 1.26M in 2022.

    📉 Insight: A moderate drop in electricity generation since 2022 may be due to equipment efficiency, maintenance, or input availability.

6. Yearly Fertilizer Produced

    Fairly stable, e.g.:

        2024: 1.13M units

        2022: 1.18M units

    📊 Insight: Fertilizer production is consistent. Suggests operations are running normally with low production volatility.

7. Yearly Operational Cost (Donut Chart)

    Evenly distributed over years (~10–12% per year).

    📊 Insight: Costs are spread fairly across years, but 2023 shows the highest single-year cost (11.8%), which could explain recent profitability issues.

📈 Financial Performance Trends
8. Yearly Profit Margin (Bar Chart)

    Highest in 2018 (~37%) and 2016

    Trending downward since then

    📉 Insight: The company is becoming less profitable over time, which is a concern. Likely due to rising costs or pricing pressure.

9. Monthly Sales Trend

    Fluctuating sales without clear upward momentum

    📉 Insight: Lack of consistent monthly growth may indicate seasonality, market volatility, or sales inconsistency.

🧾 Waste Stream Analysis
10. Profit Margin by Waste Type (Table)

    Best-performing waste types:

        805: 57.73%

        802: 48.59%

        968: 53.62%

    Poor-performing waste types:

        1038: -6.39%

        1061: -10.21%

        1092: -41.95%

    📊 Insight: Some waste types are highly profitable, while others generate negative margins. There’s room to optimize or eliminate low-margin streams.

📌 Overall Insights & Recommendations
✅ Strengths:

    Stable fertilizer production

    Operational costs slightly reduced

    Some waste streams highly profitable

⚠️ Weaknesses:

    Declining sales and profits

    Falling profit margins

    Negative margin on some waste streams

💡 Opportunities:

    Optimize waste selection and processing for profit

    Improve electricity generation efficiency

    Investigate revenue diversification or pricing strategies

❗ Threats:

    Market instability impacting revenue

    Cost creep reducing margins

    Dependency on underperforming waste inputs

📥 Suggested Actions

    Review low-margin waste categories and assess elimination or redesign.

    Investigate causes of sales decline – market share, demand drop, customer retention?

    Improve efficiency in electricity production to reduce costs.

    Conduct pricing analysis to ensure profitability in product lines.
