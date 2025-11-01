# Target Brazil: An E-Commerce Business Intelligence Study (2016-2018)

<p align="center">
  <img src="https://img.shields.io/badge/SQL-00758F?style=for-the-badge&logo=sql&logoColor=white" alt="SQL Badge"/>
  <img src="https://img.shields.io/badge/Google_BigQuery-4285F4?style=for-the-badge&logo=google-bigquery&logoColor=white" alt="BigQuery Badge"/>
  <img src="https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white" alt="Tableau Badge"/>
</p>

## 1. Project Overview

This project is a comprehensive analysis of Target's e-commerce operations in Brazil from 2016 to 2018. As a data analyst, I leveraged SQL to query a large-scale database to uncover critical insights across customer behavior, geographic sales patterns, and logistical performance. The primary objective was to translate raw data into a clear, actionable strategic roadmap to drive business growth and enhance operational efficiency.

## 2. Business Context: Charting a Course in the Brazilian E-commerce Market

Between 2016 and 2018, Target embarked on a strategic expansion into Brazil, aiming to establish a significant foothold in Latin America's largest and most dynamic e-commerce market. For this expansion to succeed, Target needed to deeply understand the local landscape. This analysis serves as that crucial strategic guide, answering fundamental questions about **market opportunity**, **operational reality**, and **customer behavior**. The insights derived from this project are designed to be actionable and impact every level of the business, from executive strategy to on-the-ground logistics.

## 3. Tech Stack

*   **Language:** SQL (Google BigQuery Dialect)
*   **Database:** Google BigQuery

---

## 4. Key Findings & Strategic Recommendations

### Executive Summary

Our analysis of Target's e-commerce data from 2016 to 2018 reveals a story of remarkable, rapid growth. However, this growth has been heavily concentrated, creating a "two-speed" business: a highly profitable core centered in metropolitan hubs like São Paulo, and the vast, untapped potential of the rest of the country, held back by significant logistics challenges. Our future success depends on bridging this gap.

### Finding 1: Growth is Explosive but Geographically Concentrated
The business is expanding at an impressive rate, with order volume growing over 100% in 2018. However, this success is overwhelmingly driven by a single state: **São Paulo**, which accounts for nearly 42% of our entire customer base.

*   **Insight:** São Paulo is our engine—our largest and most efficient market, boasting the fastest delivery times.
*   **Opportunity:** There is a clear opportunity for growth in secondary markets like Rio de Janeiro and Minas Gerais that show strong demand but have not yet received strategic focus.


### Finding 2: A Critical Divide in Customer Experience
The data reveals a stark difference in customer experience across regions, posing a threat to our national brand reputation.

*   **Insight:** A delivery in São Paulo takes, on average, just **8 days**. In stark contrast, an order to more remote northern states can take over **18 days**.
*   **Problem:** High freight costs and long delivery times in these "frontier" states create dissatisfied customers and make sustainable growth almost impossible.


### Finding 3: Brazilian Customers Have Clear & Actionable Habits
Our analysis paints a clear picture of the Brazilian online shopper, giving us a powerful tool to tailor our strategy.

*   **Insight:**
    *   **Peak Shopping Time:** 35% of orders are placed in the **afternoon (1-6 PM)**.
    *   **Peak Shopping Season:** Sales spike in **August and November**.
    *   **Preferred Payment:** **Credit cards** are the dominant method (74%), and the use of **installments** is extremely popular.
*   **Takeaway:** These consistent patterns provide a clear guide for marketing campaigns, website load management, and payment feature promotions.

---

## 5. Strategic Recommendations

Based on these findings, we propose a three-pronged strategy to build upon our successes and address our core challenges.

#### **Recommendation 1: Defend the Core, Expand Smartly**
*   **Action:** Continue to nurture the São Paulo market while launching a strategic expansion into high-potential secondary markets like **Rio de Janeiro** and **Minas Gerais**. Before a full marketing push, we must ensure logistics in these regions can match the "São Paulo standard."

#### **Recommendation 2: Fix the Logistics Frontier**
*   **Action:** Prioritize logistics optimization for the northern and interior states by exploring partnerships with regional delivery carriers. In the medium term, analyze the ROI of a new fulfillment center in a strategic location like **Recife**.

#### **Recommendation 3: Align with Customer Behavior**
*   **Action:**
    *   Align major marketing promotions with peak shopping times (**afternoons**) and key sales months (**August, November**).
    *   Prominently feature flexible **credit card installment options** in marketing and at checkout to appeal to established customer preferences and drive higher average order values.

## 6. Project Structure & Usage

The repository is structured to separate the analysis from supplementary materials.
To replicate this analysis:
1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/AnkitDatascience07/Ecommerce_analysis_SQL_Project.git
    ```
2.  **The Data:** For a complete guide to the tables, fields, and relationships used in this project, please see the `DATA_DICTIONARY.md` file.
3.  **Run the Analysis:** The complete set of queries can be found in `sql_queries/analysis.sql`. These are written for Google BigQuery and can be executed in the BQ console.

## 7. Future Analysis Opportunities

*   **Customer Segmentation:** Conduct an RFM (Recency, Frequency, Monetary) analysis to identify high-value customer segments for targeted marketing.
*   **Product Category Deep-Dive:** Analyze which product categories are most profitable and which are frequently purchased together (basket analysis).
*   **Review Score Analysis:** Use the `review_score` to quantify the impact of late deliveries on customer satisfaction.










