# Streamlit SuperStore EDA Dashboard

## Project Overview
This project presents an interactive Exploratory Data Analysis (EDA) dashboard for SuperStore sales data, built using Streamlit. The dashboard allows users to filter data by region, state, and city, and visualizes key sales metrics through various charts.

## Data Pipeline
1.  **Data Source:** The dashboard primarily uses a `sample.csv` file located within the repository. It also provides an option for users to upload their own CSV, TXT, XLSX, or XLS files.
2.  **Dashboard Application:** The `dashboard.py` script is a Streamlit application that:
    *   Loads the sales data (either from `sample.csv` or user upload).
    *   Converts 'Order Date' to datetime objects and allows filtering by date range.
    *   Provides sidebar filters for 'Region', 'State', and 'City'.
    *   Generates various visualizations using Plotly Express, including:
        *   Category-wise Sales (Bar Chart)
        *   Region-wise Sales (Pie Chart)
        *   Month-wise Sales (Line Chart)
        *   Hierarchical view of Sales using TreeMap (Region, Category, Sub-Category)
        *   Segment-wise Sales (Pie Chart)
        *   Relationship between Sales and Profits (Scatter Plot)
    *   Includes expandable sections to view raw data for different aggregations.
    *   Allows downloading of filtered data.

## How to Run the Dashboard Locally
1.  **Clone the repository:**
    ```bash
    git clone https://github.com/NancherlaKoushik/Streamlit_Dashboard.git
    ```
2.  **Navigate to the project directory:**
    ```bash
    cd Streamlit_Dashboard
    ```
3.  **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```
4.  **Run the Streamlit application:**
    ```bash
    streamlit run dashboard.py
    ```
    This will open the dashboard in your web browser.

## Dashboard Snapshots

### Main Dashboard View
![Main Dashboard View](https://private-us-east-1.manuscdn.com/sessionFile/ReOt4K7CeTI2NyjhvruqcG/sandbox/Dt2qU6apbIZFTKoV7DhIfK-images_1750419757093_na1fn_L2hvbWUvdWJ1bnR1L3NjcmVlbnNob3RzLzg1MDEtaWE2b3Rhb29uenR1dzFhXzIwMjUtMDYtMjBfMTEtNDEtMzJfMTc3MA.webp?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvUmVPdDRLN0NlVEkyTnlqaHZydXFjRy9zYW5kYm94L0R0MnFVNmFwYklaRlRLb1Y3RGhJZkstaW1hZ2VzXzE3NTA0MTk3NTcwOTNfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwzTmpjbVZsYm5Ob2IzUnpMemcxTURFdGFXRTJiM1JoYjI5dWVuUjFkekZoWHpJd01qVXRNRFl0TWpCZk1URXROREV0TXpKZk1UYzNNQS53ZWJwIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzY3MjI1NjAwfX19XX0_&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=uFciUvEtmipuH9bhUWonW~GNQzi90D9jQ~NUM-FoBLSlHHDFGR6nDP5~7rktCMGBBwUd1i5YYc7socPPcwSktcFQAVwZjmYCux~gwgpR1RcnxbpwXma1nmY7XTA8sNBmsPm8uZ7det20q3BgekfvdE~klfnh3fzCFd1Zvkl23TSVYRiaFTAmnsVzBkYx6J8715akL9RDPX5oHKwVxuGmKsKdIkeABvDFvulEFl1sw~ZjSZALXVD6kAwWPaxv9scie6dM4j26ICuM5L1YNDP3bMwJdnYlCHqeAegkWZNFpFA4~zXBUpxeAr7Fa9CFORRfQlea7VSazQsVZ1ZX6hmEbA__)

### Full Dashboard View (after scrolling)
![Full Dashboard View](https://private-us-east-1.manuscdn.com/sessionFile/ReOt4K7CeTI2NyjhvruqcG/sandbox/Dt2qU6apbIZFTKoV7DhIfK-images_1750419757093_na1fn_L2hvbWUvdWJ1bnR1L3NjcmVlbnNob3RzLzg1MDEtaWE2b3Rhb29uenR1dzFhXzIwMjUtMDYtMjBfMTEtNDEtNDJfODAwMg.webp?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvUmVPdDRLN0NlVEkyTnlqaHZydXFjRy9zYW5kYm94L0R0MnFVNmFwYklaRlRLb1Y3RGhJZkstaW1hZ2VzXzE3NTA0MTk3NTcwOTNfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwzTmpjbVZsYm5Ob2IzUnpMemcxTURFdGFXRTJiM1JoYjI5dWVuUjFkekZoWHpJd01qVXRNRFl0TWpCZk1URXROREV0TkRKZk9EQXdNZy53ZWJwIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzY3MjI1NjAwfX19XX0_&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=ruFLQ2U9RMRDeyvs645dmSGpye9jagMvjw9tc6On06mndRfATMEAWEZFF5bGZnCzwSN8twSt0hQVTDbl59-pyOpSJPPUKWemR2GnPEZBK83xh8Y7WEKlc2wYmcKElyuX9CklpukLzam31CvvCBbwvrPV~3gnAzvTZ3LhZmaFLOPDJAG0y4uByT0xHlaugrHO4SvpU11Zcy8BgZYxOwxzyTWnG61YCHkcu2m~YKpUsbn2JFDEflEm0QYMIzAzMnRdcAWzN-XFciq74H7lFKfFGjKuV6xXzcCJHAHpjXkWegWIW5j3iEdtwhcykk4GWrnxOBRLzSOSWcAuXnswkJ2Xyw__)

## Key Features and Insights
*   **Interactive Filtering:** Users can dynamically filter the data by selecting specific regions, states, and cities.
*   **Date Range Selection:** The dashboard allows users to analyze sales data within a custom date range.
*   **Sales Performance by Category and Region:** Visualizations provide quick insights into which product categories and geographical regions are performing best.
*   **Monthly Sales Trends:** The line chart shows the sales trend over time, helping to identify seasonality or growth patterns.
*   **Hierarchical Sales Analysis:** The treemap offers a detailed breakdown of sales across different levels of hierarchy (Region > Category > Sub-Category).
*   **Profitability Analysis:** The scatter plot visualizes the relationship between sales and profit, which can help in identifying high-profit products or areas.
*   **Data Export:** Users can download various aggregated datasets directly from the dashboard.

## Conclusion
This Streamlit dashboard provides a user-friendly and interactive platform for exploring SuperStore sales data. It's a valuable tool for business analysts to gain quick insights and make data-driven decisions.


