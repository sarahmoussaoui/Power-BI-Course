# Power BI Course

Files and projects from a hands-on **Power BI Desktop for Business Intelligence** course (Maven Analytics). The course project puts you in the role of a Business Intelligence Analyst at **AdventureWorks**, a global manufacturer of cycling equipment and accessories, building a report that tracks KPIs (orders, revenue, profit, returns), compares regional performance, analyzes products, and profiles customers.

## Table of Contents

- [Course Outline](#course-outline)
- [Repository Structure](#repository-structure)
- [Dataset](#dataset)
- [Report Pages](#report-pages)
- [Work-in-Progress Reports](#work-in-progress-reports)
- [Getting Started](#getting-started)
- [Credits](#credits)

## Course Outline

| # | Module | Topics |
|---|--------|--------|
| 1 | Introducing Power BI Desktop | Installation, the Power BI workflow, Power BI vs. Excel |
| 2 | Connecting & Shaping Data | Connecting to data, transforming tables, profiling tools, merging and appending queries |
| 3 | Creating a Data Model | Table relationships, cardinality, filter flow |
| 4 | Calculating Measures with DAX | DAX syntax, calculated columns, measures, common functions |
| 5 | Visualizing Data with Dashboards | Charts, formatting, interactions, filters, bookmarks |
| 6 | Optimizing Power BI Performance | Optimization and external tools |

## Repository Structure

```
Microsoft Power BI Desktop for Business Intelligence/
├── AdventureWorks Raw Data/
│   └── AdventureWorks Raw Data/
│       ├── AdventureWorks Calendar Lookup.csv
│       ├── AdventureWorks Customer Lookup.csv
│       ├── AdventureWorks Product Categories Lookup.csv
│       ├── AdventureWorks Product Subcategories Lookup.csv
│       ├── AdventureWorks Product Lookup.csv
│       ├── AdventureWorks Territory Lookup.csv
│       ├── AdventureWorks Returns Data.csv
│       ├── Sales Data/               # Sales Data 2020, 2021, 2022
│       └── Product Category Sales (Unpivot Demo).csv
├── AdventureWorks PBIX Files/
│   └── AdventureWorks PBIX Files/
│       ├── AdventureWorks Report_FINAL.pbix
│       └── WIP Reports/              # Report saved at each stage of the course
├── AdventureWorks Images/            # Logo and icons used in the report design
├── Power BI for Business Intelligence.pdf   # Course eBook (210 pages)
└── (original .zip archives of the folders above)
```

## Dataset

| File | Description | Rows (approx.) |
|------|-------------|----------------|
| Sales Data 2020 / 2021 / 2022 | Order lines (order date, stock date, order number, product, customer, territory, quantity) | 2,600 / 23,900 / 29,500 |
| Product Lookup | Product name, model, SKU, color, size, style, cost, and price | 290 |
| Product Categories / Subcategories Lookup | Product hierarchy (category → subcategory → product) | 4 / 37 |
| Customer Lookup | Name, birth date, marital status, gender, income, children, education, occupation, home ownership | 18,150 |
| Territory Lookup | Sales region, country, and continent | 10 |
| Returns Data | Returned products by date, territory, and quantity | 1,800 |
| Calendar Lookup | Date table (2020 onward) | 910 |
| Product Category Sales (Unpivot Demo) | Small table used to practice unpivoting columns in Power Query | 20 |

## Report Pages

The final report (`AdventureWorks Report_FINAL.pbix`) has eight pages:

| Page | Content |
|------|---------|
| **Exec Dashboard** | KPI cards and comparisons with the previous month for orders, revenue, profit, and returns; return rate; trend line chart; top products; most ordered and most returned product type |
| **Map** | Orders by country and continent on a map |
| **Product Detail** | Product-level performance with a selected-product view |
| **Customer Detail** | Customer analysis and profiling |
| **Category Tooltip** | Custom tooltip page shown when hovering over category visuals |
| **Q&A** | Natural-language questions with Power BI's Q&A visual |
| **Decomposition Tree** | AI visual to break measures down by multiple dimensions |
| **Key Influencers** | AI visual to find the factors that drive a metric |

Main measures (in a dedicated measure table): Total Orders, Total Revenue, Total Profit, Total Returns, Return Rate, and previous-month versions of orders, revenue, and returns.

## Work-in-Progress Reports

The `WIP Reports/` folder contains the report as it stood at the end of each stage, so you can follow the build step by step:

1. `Power Query Complete`: data connected and cleaned
2. `Data Model Complete`: relationships added
3. `DAX Complete`: calculated columns and measures added
4. `Visualization Complete`: dashboards built
5. `AI Complete`: AI visuals added

## Getting Started

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Windows only).
2. Clone the repository:
   ```bash
   git clone https://github.com/sarahmoussaoui/Power-BI-Course.git
   ```
3. Open `AdventureWorks Report_FINAL.pbix` to explore the finished report, or start from a file in `WIP Reports/`.
4. If you see a refresh error, the data sources are pointing to a different location. Go to **Home → Transform data → Data source settings**, choose **Change Source**, and point each file to the `AdventureWorks Raw Data` folder in this repository.

## Credits

Course, dataset, and eBook by [Maven Analytics](https://www.mavenanalytics.io) (instructors Chris Dutton and Aaron Parry). The AdventureWorks data is a fictional dataset used for training. This repository contains my personal work and notes from the course, for learning purposes only.
