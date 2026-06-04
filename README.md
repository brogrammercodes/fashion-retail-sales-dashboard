# End-to-End Sales Data Analysis & Visualization — Fashion Retail

An end-to-end **Power BI** business-intelligence project that turns a raw fashion-retail
sales dataset into an interactive, three-page analytical dashboard covering revenue,
customer behaviour & returns, and inventory & category performance.

![Sales Performance & Revenue](Page%201.png)

---

## 📊 Project Overview

The goal of this project is to analyse a fashion retailer's product-level sales data and
surface the insights a merchandising / category team needs to answer questions such as:

- Which **brands and categories** drive the most revenue?
- How healthy is the **average order value (AOV)** and how deep are our **discounts**?
- **Why are customers returning** products, and which categories return the most?
- How is **stock** distributed across brands and categories?
- How do **seasonality** and **customer ratings** affect sales and returns?

The report was built following a typical BI workflow: **data import → cleaning &
modelling → DAX measures → visualization → theming & layout → export**.

---

## 🗂️ Repository Contents

| File | Description |
|------|-------------|
| `Fashion Dataset.pbix` | The Power BI Desktop report (data model, DAX measures, and all 3 dashboard pages). |
| `Fashion Dataset.pdf` | Static PDF export of the full dashboard for quick viewing without Power BI. |
| `Column Definitions.xlsx` | Data dictionary describing every column in the source dataset. |
| `Colour Code.xlsx` | The colour palette / hex codes used for the report theme. |
| `Page 1.png`, `Page 2.png`, `Page 3.png` | Branded background images used in the report design. |

---

## 🧱 Data Model

The report is built on a single fact table, **`fashion_dataset`**, with the following
fields (see `Column Definitions.xlsx` for full definitions):

| Column | Definition |
|--------|------------|
| `product_id` | Unique identifier assigned to each product |
| `category` | Product category or type (Clothing, Footwear, Accessories) |
| `brand` | Brand / manufacturer name of the product |
| `season` | Intended season (Summer, Winter, All-Season) |
| `size` | Product size (S, M, L, XL, or numeric) |
| `color` | Product colour |
| `original_price` | Original listed price before discounts |
| `markdown_percentage` | Percentage discount applied to the original price |
| `current_price` | Final selling price after markdown |
| `purchase_date` | Date the product was purchased |
| `stock_quantity` | Units available in inventory |
| `customer_rating` | Customer rating (1–5 scale) |
| `is_returned` | Whether the product was returned |
| `return_reason` | Reason provided for a return (if returned) |

### DAX measures & calculated columns

| Measure / Column | Purpose |
|------------------|---------|
| `Average Order Value` | Average revenue per order |
| `Discount` | Total / effective discount given |
| `% Return` | Return rate by category |
| `Rating Category` | Buckets customer ratings into rating bands |
| Date Hierarchy on `purchase_date` | Enables month-level time analysis |

---

## 📈 Dashboard Pages

### 1. Sales Performance & Revenue
KPI cards for **Total Revenue**, **Average Order Value**, **product coverage**, and
**total Discount**, plus a bar chart of **revenue by brand**.

### 2. Customer Behavior & Returns
A **brand slicer** driving:
- **Returns by reason** (bar chart)
- **Sales/orders by season** (line chart)
- **Return % by category** (ribbon chart)
- **Order distribution by rating category** (pie chart)

### 3. Inventory & Category Performance
- **Stock quantity by brand & category** (clustered column chart)
- **Orders by month** (bar chart)
- **Average Order Value by category** (line chart)
- **Average Order Value by brand** (bar chart)

---

## 🎨 Design

- Custom Power BI **theme** using a warm fashion palette
  (`#cb997e`, `#ddbea9`, `#ffe8d6`, `#b7b7a4`, `#a5a58d`, `#6b705c`) on a `#ffd1c0`
  background.
- Branded **editorial fashion imagery** as page backgrounds for a magazine-style look.
- Consistent page headers and an interactive, slicer-driven experience.

---

## 🚀 How to Use

1. **Quick view:** open `Fashion Dataset.pdf` to browse all three dashboard pages.
2. **Interactive view:** install [Power BI Desktop](https://powerbi.microsoft.com/desktop/)
   (free) and open `Fashion Dataset.pbix`. Use the slicers to filter by brand and explore
   the visuals.

---

## 🛠️ Tools & Skills Demonstrated

- **Power BI Desktop** — data modelling, report design, theming
- **Power Query** — data import & cleaning
- **DAX** — measures and calculated columns
- **Data visualization & storytelling** — KPI cards, bar / line / ribbon / pie / clustered
  column charts, and slicer-based interactivity
- **Dashboard design** — custom theme, layout, and branded visuals

---

## 📄 License

This project is provided for educational and portfolio purposes.
