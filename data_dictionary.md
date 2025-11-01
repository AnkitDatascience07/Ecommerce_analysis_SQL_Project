## Data Dictionary: A Guide to the Target Brazil E-commerce Dataset

### Dataset Overview

This document provides a comprehensive guide to the 8 interconnected tables that make up the Target Brazil e-commerce dataset. Spanning over 100,000 orders from late 2016 to late 2018, this rich dataset is the foundation of our entire analysis, offering deep insights into every facet of the business—from customer geography to product details and payment preferences.

---

### Table Definitions & Analytical Value

#### 1. The `orders` Table
This is the central table of the dataset, tracking the complete lifecycle of every customer order from the moment of purchase to final delivery.

| Column | Data Type | Description |
| :--- | :--- | :--- |
| `order_id` | STRING | Unique identifier for each order. |
| `customer_id` | STRING | Foreign key linking to the `customers` table. |
| `order_status` | STRING | Current status of the order (e.g., delivered, shipped, canceled). |
| `order_purchase_timestamp` | TIMESTAMP | The exact moment the order was placed by the customer. |
| `order_approved_at` | TIMESTAMP | Timestamp for when the payment was successfully approved. |
| `order_delivered_carrier_date` | TIMESTAMP | Timestamp for when the package was handed off to the logistics carrier. |
| `order_delivered_customer_date`| TIMESTAMP | The actual date and time the customer received the order. |
| `order_estimated_delivery_date`| TIMESTAMP | The delivery date promised to the customer at the time of purchase. |

**Analytical Value:**
*   **`order_purchase_timestamp`** is the backbone of our time-series analysis, allowing us to track sales trends and seasonality.
*   **`order_status`** is essential for filtering to completed transactions (`'delivered'`) to ensure analysis is based on successful sales.
*   The **delivery timestamps** are critical for calculating actual delivery times. Comparing `order_delivered_customer_date` against `order_estimated_delivery_date` allows us to quantify how well we are meeting customer expectations.

#### 2. The `customers` Table
Contains key information about each unique customer, with a strong focus on their geographic location.

| Column | Data Type | Description |
| :--- | :--- | :--- |
| `customer_id` | STRING | A unique identifier for a specific order instance. |
| `customer_unique_id` | STRING | A persistent identifier for a customer across all their orders. |
| `customer_zip_code_prefix` | INTEGER | The first 5 digits of the customer's postal code. |
| `customer_city` | STRING | The customer's city. |
| `customer_state` | STRING | The two-letter code for the Brazilian state (e.g., SP for São Paulo). |

**Analytical Value:**
*   **`customer_state`** and **`customer_city`** are the primary fields for all geographic analysis, helping us identify key markets and regional customer density.
*   **`customer_unique_id`** is used to analyze customer retention and calculate repeat purchase rates.

#### 3. The `order_items` Table
Provides a detailed breakdown of the products and costs associated with each individual order.

| Column | Data Type | Description |
| :--- | :--- | :--- |
| `order_id` | STRING | Foreign key linking to the `orders` table. |
| `order_item_id` | INTEGER | A sequential number for each item within a multi-item order. |
| `product_id` | STRING | Foreign key linking to the `products` table. |
| `seller_id` | STRING | Foreign key linking to the `sellers` table. |
| `shipping_limit_date` | TIMESTAMP | The deadline for the seller to ship the item. |
| `price` | FLOAT | The price of the individual item in Brazilian Reals (R$). |
| `freight_value` | FLOAT | The shipping cost for the individual item. |

**Analytical Value:**
*   **`price`** and **`freight_value`** are the core components of our revenue and logistics cost analysis. Summing these provides the total order value.
*   A `order_item_id` greater than 1 signifies that an order contained multiple products, enabling analysis of basket size.

#### 4. The `payments` Table
Details the payment method, value, and installment plan for each transaction.

| Column | Data Type | Description |
| :--- | :--- | :--- |
| `order_id` | STRING | Foreign key linking to the `orders` table. |
| `payment_sequential` | INTEGER | Sequence number for multi-method payments. |
| `payment_type` | STRING | Method of payment (e.g., `credit_card`, `boleto`, `voucher`). |
| `payment_installments` | INTEGER | The number of installments chosen by the customer. |
| `payment_value` | FLOAT | The total value of the payment transaction. |

**Analytical Value:**
*   **`payment_type`** provides clear insight into customer financial preferences.
*   **`payment_installments`** is a powerful indicator of customer purchasing behavior and price sensitivity, especially for higher-value items.

#### 5. The `products` Table
A catalog of all unique products, containing descriptive information and physical attributes.

| Column | Data Type | Description |
| :--- | :--- | :--- |
| `product_id` | STRING | Unique identifier for each product. |
| `product_category_name` | STRING | The product's category (in Portuguese). |
| `product_weight_g` | INTEGER | Product weight in grams. |
| `product_length_cm` | INTEGER | Product dimensions (length, height, width) in centimeters. |

**Analytical Value:**
*   **`product_category_name`** is key to understanding which product lines are the most successful.
*   The **physical dimensions** and **weight** are crucial inputs for logistics planning and calculating shipping costs.

#### 6. The `sellers`, `order_reviews`, and `geolocation` Tables
These supplementary tables provide additional context for a deeper analysis:
*   **`sellers`**: Contains the geographic location (`seller_city`, `seller_state`) of each seller, which is vital for supply chain and logistics analysis.
*   **`order_reviews`**: Contains the customer-provided `review_score` (1-5), allowing for direct measurement of customer satisfaction linked to specific orders.
*   **`geolocation`**: A mapping table that links Brazilian zip code prefixes to latitude (`geolocation_lat`) and longitude (`geolocation_lng`) coordinates, enabling powerful map-based visualizations and distance calculations.

---

### Dataset Context & Usage Notes
*   **Data Integrity:** The core transaction tables (`orders`, `order_items`) have a high degree of completeness. Delivery date information is available for over 96% of completed orders.
*   **Timestamps:** All timestamps are recorded in Coordinated Universal Time (UTC).
*   **Currency:** All monetary values (`price`, `freight_value`, `payment_value`) are in **Brazilian Reals (R$)**.
*   **Primary Keys:** The primary relationship in this database links `customers` to `orders` and `orders` to `order_items` and `payments`.
