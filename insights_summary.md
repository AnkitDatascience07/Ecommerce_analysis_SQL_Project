# Target Brazil: An E-Commerce Business Intelligence Study (2016-2018)

## Project Overview

This project is a comprehensive analysis of Target's e-commerce operations in Brazil from 2016 to 2018. As a data analyst, I leveraged SQL to query a large-scale database to uncover critical insights across customer behavior, geographic sales patterns, and logistical performance. The primary objective was to translate raw data into a clear, actionable strategic roadmap to drive business growth and enhance operational efficiency.

## Key Business Questions

This analysis was structured to answer key questions vital to the business:
1.  **Growth & Performance:** What is the true trajectory of our growth, and which geographic markets are driving it?
2.  **Customer Experience:** Is there a consistent customer experience across Brazil, particularly regarding delivery times?
3.  **Behavioral Patterns:** What are the distinct purchasing habits of our Brazilian customers, from preferred shopping times to payment methods?

## Tech Stack

*   **Language:** SQL (Google BigQuery Dialect)
*   **Database:** Google BigQuery
*   **Visualization:** Tableau / Power BI / Google Looker Studio *(please edit with the tool you used)*

---

## Analysis of Target Brazil: Key Findings & Strategic Recommendations

### Executive Summary

Our analysis of Target's e-commerce data from 2016 to 2018 reveals a story of remarkable, rapid growth in the Brazilian market. However, this growth has been heavily concentrated, creating a "two-speed" business:

1.  **The Core:** A highly profitable and logistically efficient operation centered in metropolitan hubs like São Paulo.
2.  **The Frontier:** The vast, untapped potential of the rest of the country, which is currently held back by significant delivery and logistics challenges.

Our future success depends on bridging this gap. This analysis provides a data-driven roadmap to optimize our core operations, strategically expand into new regions, and build a truly national brand.

### Key Finding 1: Growth is Explosive but Geographically Concentrated

The business is expanding at an impressive rate, with order volume growing over 100% in 2018. However, this success is overwhelmingly driven by a single state: **São Paulo**, which accounts for nearly 42% of our entire customer base.

*   **Insight:** São Paulo is our engine. It is not just our largest market but also our most efficient, boasting the fastest average delivery times (8.2 days) and a highly engaged customer base.
*   **The Opportunity:** While São Paulo is our anchor, there is a clear and immediate opportunity for growth in secondary markets like Rio de Janeiro and Minas Gerais. These states show strong demand but have not yet received the strategic focus required to reach their full potential.

*(Placeholder for Customer Distribution by State Map)*
![Customer Distribution Map](visualizations/customer_distribution_map.png)

### Key Finding 2: A Critical Divide in Customer Experience

The data reveals a stark difference in the customer experience between regions. This operational divide is the single biggest threat to our national expansion and brand reputation.

*   **Insight:** A delivery in São Paulo takes, on average, just **8 days**. In stark contrast, an order to more remote northern states like Roraima (RR) can take over **18 days**. This vast disparity means a "Target customer" in one part of Brazil has a fundamentally different, and worse, experience than in another.
*   **The Problem:** High freight costs and long delivery times in these "frontier" states create dissatisfied customers and make sustainable growth almost impossible. We cannot become a national leader with a fractured logistics network.

*(Placeholder for Average Delivery Time by State Chart)*
![Delivery Time Chart](visualizations/delivery_time_chart.png)

### Key Finding 3: Brazilian Customers Have Clear & Actionable Habits

Our analysis of purchase timestamps and payment data paints a clear picture of the Brazilian online shopper, giving us a powerful tool to tailor our strategy.

*   **Insight:**
    *   **Peak Shopping Time:** The majority of orders (35%) are placed in the **afternoon (1-6 PM)**.
    *   **Peak Shopping Season:** Sales spike dramatically in the months leading up to the holidays, particularly **August and November**.
    *   **Preferred Payment:** **Credit cards** are the dominant payment method (74% of transactions), and the use of **installments** is extremely popular, signaling that customers value financial flexibility.
*   **The Takeaway:** These patterns are consistent and predictable. They provide a clear guide for when to schedule marketing campaigns, how to manage website server load, and which payment features to emphasize.

---

## Strategic Recommendations

Based on these findings, we propose a three-pronged strategy to build upon our successes and address our core challenges.

#### **Recommendation 1: Defend the Core, Expand Smartly**
Instead of a broad, unfocused expansion, we should pursue a targeted, two-stage approach.

*   **Action:** Continue to nurture the São Paulo market while launching a strategic expansion into high-potential secondary markets like **Rio de Janeiro** and **Minas Gerais**. Before a full marketing push, we must first ensure our logistics and delivery performance in these new regions can match the "São Paulo standard."

#### **Recommendation 2: Fix the Logistics Frontier**
To build a trusted national brand, we must solve the delivery problem in our most challenging regions.

*   **Action:** Prioritize logistics optimization for the northern and interior states. This requires actively exploring partnerships with regional delivery carriers who have better local knowledge. In the medium term, we should conduct a cost-benefit analysis for establishing a new fulfillment center in a strategic location like **Recife** to drastically cut delivery times to the entire Northeast region.

#### **Recommendation 3: Align with Customer Behavior**
We should use the clear patterns in customer behavior to our advantage to increase conversion and efficiency.

*   **Action:**
    *   Align major marketing promotions with observed peak shopping times (**afternoons**) and key sales months (**August, November**).
    *   Prominently feature and promote flexible **credit card installment options** during checkout and in all marketing materials to directly appeal to established customer preferences and drive higher average order values.

## How to Use This Project

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/AnkitDatascience07/Ecommerce_analysis_SQL_Project.git
    ```
2.  **Run the Analysis:** The complete set of queries used for this study can be found in `sql_queries/analysis.sql`. These queries are written for Google BigQuery and can be executed directly in the BQ console.
3.  **View the Visualizations:** Key charts and dashboards are located in the `/visualizations` folder. *(Ensure you create these visuals and add them to the folder)*.
