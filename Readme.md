Sales Distribution & Performance Analysis Dashboard
📊 Project Overview
This project focuses on transforming raw commercial data (sales, returns, customer feedback, and logistics) into an interactive decision-support tool. Using Tableau, I developed a comprehensive dashboard to track sales performance, identify regional trends, and analyze profitability across different product segments.

Key Insights:
Total Sales: $2.3M

Total Profit: $281K

Total Orders: 7,859

Geographic Focus: Western Europe (France, Germany, Italy, etc.)

🏗️ Data Architecture & Logic
Data Sources
The analysis is built on four primary datasets:

Purchases (Achats): Core sales transactions.

Ratings (Évaluations): Customer satisfaction scores.

Returns (Retours): Product return data.

People (Personnes): Sales representatives/region assignments.

Joins & Relationships
To maintain data integrity and granularity, the following schema was applied:

LEFT JOIN: Purchases ↔ Évaluations and Purchases ↔ Retours (to ensure all sales are kept, even those without feedback or returns).

INNER JOIN: Purchases ↔ Personnes (to link sales directly to assigned personnel).

Logical Relationship: A logical link between Purchases and Ratings was established to preserve the granularity of satisfaction metrics at the order level (avoiding data duplication).

💡 Advanced Features & Calculations
This project goes beyond basic visualization by implementing custom logic:

Profit Margin (ROI): A calculated field determining the percentage of profit relative to sales volume.

Eco-Tax Logic: A conditional calculation applying a 5% tax to "Technology" category products, excluding those flagged as "Recycled" in the product name.

Dynamic Profit Scenarios: A parameter-driven calculation (% accroissement profit) that allows users to simulate profit growth in real-time.

Hierarchies: Interactive drill-down capabilities for Geography (Country → Region → City) and Product (Category → Sub-Category → Product Name).

🎮 How to Use the Dashboard
Global Filters: Use the right-hand pane to filter by Date (Quarter), Country, Region, or Customer Segment.

Geographic Exploration: Hover over the map bubbles to see specific performance metrics per city. Bubble size represents sales volume, while color represents ROI.

Target Tracking: The "Targets and Forecasts" chart includes reference lines to quickly identify which quarters met the $24k average threshold.

Deep Dive: Use the "Sales by Sub-category" bar chart to identify top-performing products like Photocopiers and Libraries.

📁 Repository Structure
Dashboard.twbx: The final interactive dashboard (includes data).

Visualisations_de_base.twb: Initial exploratory analysis.

Visualisations_avancées.twb: Complex charts and interactivity testing.

Tableaux_Reporting.twb: Detailed cross-tabs and conditional formatting.

Note: For the best experience, please open the .twbx file in Tableau Desktop or Tableau Public.

🚀 Next Steps
Would you like me to refine the "Eco-Tax" or "Profit Growth" formulas to ensure they are mathematically optimized for your specific dataset?

Or should I help you write a "Key Findings" section summarizing the actual business trends shown in your screenshot (e.g., why the Enterprise segment is performing differently than the Public segment)?