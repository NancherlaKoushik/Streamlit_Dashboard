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


### Full Dashboard View 



https://github.com/user-attachments/assets/6bf1f66f-f947-4e5d-b8dc-7fadde331b58



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


