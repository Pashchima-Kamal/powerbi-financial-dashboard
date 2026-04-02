# Power BI Financial Dashboard


An interactive three-page financial report built in Power BI Desktop, analysing sales, profit, and market performance across countries, products, and segments using the Microsoft Financial Sample dataset.


—--


## Tools
- Power BI Desktop
- Microsoft Financial Sample dataset


—--


## Project structure
```
powerbi-financial-dashboard/
│
├── data/
│   └── Financial Sample.xlsx      
│
├── reports/
│   └── Financial_Dashboard_Final.pbix   
│
├── screenshots/
│   ├── overview.png                
│   ├── products.png               
│   ├── regional.png                
│   └── model.png                   
│
└── README.md                     
```


—--


## Report pages


### Overview
Key KPIs (Total Sales, Total Profit, Profit Margin %), profit by country bar chart, and sales over time line chart with date hierarchy drill-down. Year and Market Type slicer synced across all pages.


![Overview](screenshots/overview.png)


### Product and segment analysis
Matrix visual with conditional formatting (red to green) showing sales and profit across every product and segment combination. Donut chart showing sales split by segment.


![Products](screenshots/products.png)


### Regional analysis
Sales broken down by region and market type using a related Countries dimension table. Country-level summary table combining columns from both the fact and dimension tables.


![Regional](screenshots/regional.png)


—--


## Data model


Financials as the central fact table connected to a Countries dimension table via a one-to-many relationship on the Country key. Single-direction cross-filter from Countries into Financials.


![Model](screenshots/model.png)


—--


## Technical skills demonstrated


- Power Query: data import, column renaming, data type correction, step-based transformation history
- DAX measures: SUM(), DIVIDE(), IF(), CALCULATE() with filter context override across both same-table and related-table filters
- Data modelling: one-to-many relationships, understanding of star schema structure, cross-filter direction
- Report design: cross-filtering, synced slicers across pages, conditional formatting, date hierarchy drill-down, multi-page layout