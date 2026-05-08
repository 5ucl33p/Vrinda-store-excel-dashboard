<img width="1380" height="728" alt="Screenshot 2026-01-27 005333" src="https://github.com/user-attachments/assets/dcecebcb-e88f-4afe-b58d-fb7b141cdcaf" />




<br>

📊 Excel First Project
Vrinda Store Annual Report 2022 — Step-by-Step Notes
✅ Dataset Columns

Index
Order ID
Cust ID
Gender
Age
Age Group
Date
Status
Channel
SKU
Category
Size
Qty
Currency
Amount
Ship City
Ship State
Ship Postal Code
Ship Country
B2B

🧹 Step 1: Data Cleaning
🔹 Apply Filters

Data → Filter ON
Checked for: Blank (null) values
Duplicate records

🔹 Gender Column Standardization

Found values: M, W, Men, Women
Replaced:
M → Men
W → Women

🔹 Quantity Column Standardization

Found values: 1, one, two, 2
Replaced:
one → 1
two → 2

✅ Purpose: Data consistency for accurate analysis

⚙️ Step 2: Data Processing

🔹 Create Age Group Column
    Inserted new column after Age
    Formula used: =IF(E2>=50,"Senior",IF(E2>=30,"Adult","Teenager"))

🔹 Create Month Column
      Inserted new column Month

Extracted month from Date:

=TEXT(G2,"mmm")

🔹 Convert Formulas to Values

Copied Age Group & Month columns

Paste Special → Values

✅ Purpose: Keep data static and avoid formula dependency

📈 Step 3: Dashboard Analysis using Pivot Tables
📊 Chart 1: Orders vs Sales by Month (Combo Chart)
Pivot Table

Insert → Pivot Table

Rows → Month

Values →

Order ID (Count)

Amount (Sum)

Formatting

Design → Grand Totals → Off (Rows & Columns)

Pivot Chart

Analyze → Pivot Chart → Combo

Amount → Column

Order Count → Line (Secondary Axis)

Final Touch

Add title

Data labels ON

Gridlines removed

Hide field buttons

Copy → Paste to Vrinda Store Report 2022

📊 Chart 2: Order Status Distribution (Pie Chart)
Pivot Table

Rows → Status

Values → Order ID (Count)

Formatting

Design → Grand Totals → Off

Pivot Chart

Analyze → Pivot Chart → Pie

Final Touch

Add data labels

Clean formatting

Copy → Paste to dashboard

📊 Chart 3: Top 5 States by Sales (Clustered Bar)
Pivot Table

Rows → Ship State

Values → Amount (Sum)

Filter & Sort

Right click State → Filter → Top 10 → Top 5

Sort → Largest to Smallest

Formatting

Design → Grand Totals → Off

Pivot Chart

Analyze → Pivot Chart → Bar → Clustered Bar

Hide field buttons

Title: Sales – Top 5 States

Axis Formatting

Double click Axis → Number → Custom:

0.0,,"M"


Add Data Labels

Copy → Paste to dashboard

📊 Chart 4: Age Group vs Gender (% of Orders)
Pivot Table

Rows → Age Group

Columns → Gender

Values → Order ID (Count)

Formatting

Design → Grand Totals → Off

Right click value → Show Values As → % of Grand Total

Reduce decimals

Pivot Chart

Analyze → Pivot Chart → Column

Formatting applied

Copy → Paste to dashboard

📊 Chart 5: Channel-wise Orders (% Share)
Pivot Table

Rows → Channel

Values → Order ID (Count)

Formatting

Design → Grand Totals → Off

Show Values As → % of Grand Total

Reduce decimals

Pivot Chart

Insert → Pivot Chart → Pie

Proper formatting

Copy → Paste to dashboard

🎛 Step 4: Adding Slicers (Interactivity)
Insert Slicers

Click any Pivot Table

Insert → Filters → Slicer

Selected:

Month

Channel

Category

Connect Slicers to All Charts

Right click slicer → Report Connections

Checked all Pivot Tables

Repeat for all 3 slicers

Dashboard Layout

Adjusted chart sizes

Placed slicers properly

All visuals aligned in one frame

✅ Result: Fully interactive Excel dashboard
