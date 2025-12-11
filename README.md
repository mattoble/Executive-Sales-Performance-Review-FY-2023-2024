# Project Background & Overview
A US-based retail company has seen rapid catalog expansion across Electronics, Clothing, and Home Goods. Despite generating over **$142M in revenue**, sales leadership lacked visibility into regional profitability and seasonal drivers.

This dashboard consolidated **200,000 sales records** to create a single source of truth. The goal was to analyze revenue trends, regional performance, and product efficacy to assist the Sales Director in optimizing inventory for the upcoming fiscal year.

**Key Business Questions:**
* How does seasonality (Quarter/Month) impact revenue?
* Which regions are underperforming despite high transaction volumes?
* Which product categories drive the highest profit margins vs. raw revenue?


# Data Structure Overview
The analysis is based on the **[Product Sales Dataset (2023-2024)](https://www.kaggle.com/datasets/yashyennewar/product-sales-dataset-2023-2024)** from Kaggle, which simulates 200,000 verified sales transactions across the United States.

* **Source:** Kaggle Public Dataset (Synthetic Retail Data)
* **Volume:** 200,000 Records

**Entity Relationship Diagram (ERD):**
![Data Model](images/DataModel.png)

# Executive Summary
**Headline: Q4 Holiday Sales drive nearly 45% of annual revenue, while the East Region outperforms the South by 79%.**

Over the 2023-2024 period, the company generated **$142.4M in Revenue** and **$31.5M in Profit**, maintaining a healthy **22.15% Profit Margin**. The most critical finding is the extreme dependency on Q4 sales; revenue consistently triples in the final quarter compared to Q1-Q3 averages, indicating a high sensitivity to holiday shopping cycles.

**High-Level Metrics:**
* **Total Revenue:** $142.4 Million
* **Total Profit:** $31.5 Million
* **Avg Order Value:** $712
* **Top Category:** Electronics ($57.5M Revenue)

![Dashboard Overview](images/Dashboard.png)

# Insights Deep Dive
### Extreme Seasonality in Q4
* Revenue remains relatively flat between Q1 and Q3 (~$11M - $13M per quarter) but spikes aggressively in Q4 to over **$32M**.
* Q4 alone accounts for nearly **45% of total annual revenue**, driven largely by "Electronics" and "Home & Furniture" purchases.
* The company operates effectively as a "Holiday Business." Supply chain failures in October/November would be catastrophic, risking nearly half the year's revenue.

![Dashboard Overview](images/Seasonality-Q4.png)

### The "East vs. South" Disparity
* The East Region is the dominant market, generating **$45M** in revenue. In contrast, the South Region lags significantly at **$25.1M**.
* The East Region outperforms the South by **79%**, despite selling similar product mixes.
* This discrepancy suggests either a lack of brand presence in the South or logistics issues preventing market penetration in states like Mississippi and Florida.

![Dashboard Overview](images/Location.png)

### Electronics is the Highest Earner, but Clothing & Apparel is the Volume Leader
* While "Electronics" is the top *Category* ($57.5M) earner, the highest-grossing *Category* is **Clothing & Apparel** (62.31K units), beating out Electronics (51.22K units), and Home & Furniture (50.57K units).

![Dashboard Overview](images/Categories.png)


# Recommendations
Based on the analysis, I recommend the following actions for the Sales Director:

* Given the 300% revenue surge in Q4, logistics teams must ensure "Clothing & Apparel", "Electronics" and "Home & Furniture" stocks are fully replenished by September 30th to prevent stockouts during the critical holiday window.
* Launch a targeted marketing campaign or a localized survey in the South Region to understand why market share is nearly half that of the East.
* The "Accessories" category is currently the lowest profit generator ($10M). Consider bundling these with high-performing Smartphones to increase their sell-through rate.

# Caveats & Assumptions
* This dataset is synthetic. While it effectively mimics retail trends (like seasonality), certain real-world nuances—such as customer returns or supply chain delays—are not present, which may result in cleaner-than-average profit margins.
* The dataset contained zero missing values (`Null` count = 0), ensuring high accuracy in the reported KPIs.
* All financial values are assumed to be in **USD** based on the "United States" country field.
