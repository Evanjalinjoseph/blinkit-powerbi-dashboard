# blinkit-powerbi-dashboard
Power BI dashboard project built using BlinkIT Grocery Data with data modeling, relationships, DAX measures, and retail sales analysis.
## Project Overview
This project is a retail analytics dashboard created in Power BI using the BlinkIT Grocery Data dataset.  
The dashboard helps analyze sales performance, item characteristics, outlet details, rating trends, and outlet distribution.
## Dashboard Features
- Total Sales KPI
- Total Item Weight KPI
- Total Rating KPI
- Sales by Outlet Establishment Year
- Outlet Identifier by Outlet Location Type
- Total Sales by Item Type
- Item Type by Item Fat Content
- Rating and Outlet Size Gauge
- Outlet Type summary table
- Slicers for Item Identifier and Item Type
- ## Dataset Columns Used
- Item Fat Content
- Item Identifier
- Item Type
- Item Visibility
- Item Weight
- Outlet Establishment Year
- Outlet Identifier
- Outlet Location Type
- Outlet Size
- Outlet Type
- Rating
- Sales
- ## Data Model / Relationships
The dashboard was modeled using a star schema approach.

### Tables Created
1. BlinkIT Grocery Data (Fact Table)
2. Dim_Items
3. Dim_Outlets

### Relationships Created
- Dim_Items[Item Identifier] -> BlinkIT Grocery Data[Item Identifier]
- Dim_Outlets[Outlet Identifier] -> BlinkIT Grocery Data[Outlet Identifier]

### Relationship Type
- One-to-Many (1:*)
- Single direction filter flow from dimension tables to fact table

This design improves filtering, reporting performance, and DAX calculation accuracy.

## DAX Measure Example
```DAX
Total Sales = SUM('BlinkIT Grocery Data'[Sales])



