## Income-Analytics-Dashboard

## Project Summary

This project showcases a complete analytical dashboard in Power BI that visualizes income data from two sources — Wise and PayPal. The goal is to analyze incoming payments, client behavior, and key performance indicators (KPIs) across a full year, combining technical processing and stylish storytelling.

## Tools & Technologies

- Power BI Desktop
- Power Query (M)
- DAX (Data Analysis Expressions)
- CSV data sources

## Key Objectives

- Combine Wise and PayPal income data into a unified dataset
- Clean and transform raw data (currency, text, dates, empty fields)
- Exclude irrelevant personal or aggregated transactions (e.g., Wise top-ups)
- Create consistent KPI metrics for tracking income and client activity
- Build a clear, visual, and intuitive dashboard using dark theme styling

## Project Workflow

# 1. Data Preparation
- Loaded two separate CSV files (Wise & PayPal)
- Cleaned raw PayPal data (converted numeric formats, excluded personal top-ups, ensured date integrity)
- Removed PayPal transactions already present in Wise exports to prevent double counting
- Added helper columns:
- Source (Wise / PayPal)
- CheckCount (set to 1 for each row to represent transactions)
- ClientName (based on Payer Name or parsed email for PayPal)
- AmountClean (parsed numeric format with proper locale)
- Created and applied date hierarchy (Year > Quarter > Month)

# 2. Data Model
- Merged both tables into a single Statistic table
- Established relationships with Date where needed
- Removed circular dependencies and unnecessary columns
- Defined measures:
- Total Income
- Total Payments
- Avg Payment (overall and by source)
- Total Receipts
- Unique Clients (by source)
- WiseIncome, PayPalIncome and similar breakdowns

## Design Theme

- Dark Mode
- Primary accents in yellow and orange
- Icons for each KPI (money bag, person, receipt, calendar)
- Clean typography and grid layout
- Manual border and padding adjustments for clarity
- Adaptive labels and consistent formatting

## Learnings & Highlights

- Careful attention to data integrity, avoiding double-counting
- Use of calculated columns and DAX measures for modularity
- Combination of technical accuracy and aesthetic design
- Balanced between interactivity (slicers, filters) and simplicity
- Project completed without using paid visuals or pro features
- Deep dive into real-life income analytics and segmentation by source

## Future Improvements (Optional)
- Add parameter toggle for switching between Total / Source views
- Client segmentation by volume/frequency
- Profit margin analysis (if cost data available)
- Export to mobile view / embedded reporting
