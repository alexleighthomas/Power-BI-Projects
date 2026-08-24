<h1> 📊 Power BI Data Analytics Project </h1>
<h2> Data Transformation, DAX, and Interactive Reporting — Data Technician Bootcamp </h2>
<p1> This project showcases my end‑to‑end Power BI skills developed during the Data Technician Bootcamp, including data cleaning, modelling, DAX calculations, and interactive report design. The work was completed through hands‑on labs aligned with the PL‑300: Power BI Data Analyst curriculum. </p1>

<h2> 🧰 Core Skills Demonstrated </h2>
<h3> ✔️ Data Cleaning & Transformation (Power Query) </h3>
<p1> 

- Removed errors, duplicates, and null values

- Split, merged, and reshaped columns

- Converted data types and enforced schema consistency

- Created custom columns using M‑language logic

- Applied transformations such as:
  - Group By
    
  - Replace Values
    
  - Conditional Columns
    
  - Parameter creation
    
  - Query referencing

These steps ensured the dataset was fully prepared for modelling and analysis. </p1>

<h3> ✔️ Data Modelling & Semantic Layer </h3>

<p1> 

- Built star‑schema models with fact and dimension tables

- Managed relationships (one‑to‑many, cross‑filter direction)

- Configured semantic models for efficient reporting

- Created hierarchies (e.g., Year → Month → Day)

- Set up model properties such as formatting, summarisation, and data categories </p1>

<img width="533" height="273" alt="image" src="https://github.com/user-attachments/assets/19e5ab76-a126-4e93-abbe-541d31446045" />

<p2> This diagram shows the star‑schema data model used in Power BI, with clearly defined fact and dimension tables. It highlights how relationships were created between tables such as Sales, Product, Region, Reseller, and Salesperson to support efficient reporting. Hierarchies, formatting, and semantic properties were configured to ensure clean, reliable analytics and smooth interaction across visuals and DAX measures. </p2> 

<h3> ✔️ DAX Calculated Columns & Measures </h3>
<p1>  
Developed DAX expressions to support deeper analysis, including:
- Calculated Columns

  - Category flags

  - Date breakdowns

  - Custom logic fields

- Measures
  - SUM, AVERAGE, COUNT

  - Year‑to‑Date (YTD)

  - Month‑over‑Month (MoM)

  - Percentage of Total

  - KPI metrics for sales performance

These measures enabled dynamic, interactive reporting across multiple visuals. </p1>

<h4> 📐 DAX Measures for Regional Sales Percentages </h4>
<p1> These DAX measures calculate sales percentages at different geographic levels: Region, Country, and Group. They use DIVIDE(), CALCULATE(), and REMOVEFILTERS() to control context, and ISINSCOPE() to ensure correct behaviour inside hierarchical visuals such as matrices. </p1>

<img width="686" height="287" alt="image" src="https://github.com/user-attachments/assets/c3f7f230-54d0-436c-9c02-dcb1c62b841d" />

<h4> 1. Sales % All Region
Percentage of total sales across all regions, ignoring the Region filter. </h4>
<p2> Sales % All Region =
DIVIDE(
    SUM(Sales[Sales]),
    CALCULATE(
        SUM(Sales[Sales]),
        REMOVEFILTERS(Region)
    )
)
</p2> 

<h4> 2. Sales % Country
Percentage of total sales for the country, ignoring the Region level. With ISINSCOPE() for correct matrix behaviour: </h4>
<p2> Sales % Country =
IF(
    ISINSCOPE(Region[Region]),
    DIVIDE(
        SUM(Sales[Sales]),
        CALCULATE(
            SUM(Sales[Sales]),
            REMOVEFILTERS(Region[Region])
        )
    )
) </p2>

<h4> 3. Sales % Group
Percentage of total sales for the group, ignoring both Region and Country filters. With ISINSCOPE() for hierarchical accuracy: </h4>

<p2> Sales % Group =
IF(
    ISINSCOPE(Region[Region]) || ISINSCOPE(Region[Country]),
    DIVIDE(
        SUM(Sales[Sales]),
        CALCULATE(
            SUM(Sales[Sales]),
            REMOVEFILTERS(Region[Region], Region[Country])
        )
    )
) </p2>

<h3> ✔️ Interactive Report Design </h3>

<p1> 
Built multi‑page Power BI reports featuring:

- Slicers (date, product, region, category)

- Filters (visual‑level, page‑level, report‑level)

- Drill‑down and drill‑through navigation

- Bookmarks and selection controls

- Custom themes and formatting

The reports were designed for clarity, usability, and business relevance. </p1>

<h3> ✔️ Visualisations Created </h3>
<p1> 
A wide range of visuals were used to tell a clear data story:

- Bar charts — product performance, regional sales

- Line charts — sales trends over time

- Pie charts — category distribution

- Maps — geographic sales insights

- Cards & KPIs — key metrics at a glance

- Tables & matrices — detailed breakdowns

- Custom visuals (where appropriate) </p1>

<h2> 📈 Retail & Sales Data Storytelling </h2>

<p1> 
The project focused heavily on retail and sales datasets, using Power BI to uncover:

High‑performing products

- Seasonal trends

- Regional sales differences

- Customer behaviour patterns

- KPI performance against targets

Through interactive dashboards, stakeholders can explore:

- Which products drive the most revenue

- How sales change month‑to‑month

- Which regions underperform

- Where to focus marketing or operational improvements

This demonstrates my ability to turn raw data into meaningful business insights. </p1>

<img width="678" height="353" alt="image" src="https://github.com/user-attachments/assets/f328554c-44f1-4961-a1e2-6ecafcf00ec1" />

<p2> This dashboard presents key retail and sales insights using Power BI, including monthly sales and profit margin trends, product‑level performance, and category‑level quantities sold. Interactive filters allow users to explore results by year and region, while the visuals highlight high‑performing products, seasonal patterns, and regional differences in customer behaviour. It demonstrates how Power BI can turn raw sales data into clear, actionable business insights. </p2>

<h2> 🚀 Tools & Platforms Used </h2>

<p1> 
- Power BI Desktop

- Power BI Service (Publishing & Sharing)

- Power Query

- DAX

- PL‑300 XtremeLabs environment </p1>

<h2> 📁 Portfolio Contents </h2>
<p1> 

- Data transformation workflows

- Semantic model configuration

- DAX measures and calculated columns

- Interactive Power BI reports

- Retail and sales dashboards

- Visual storytelling summaries </p1>
