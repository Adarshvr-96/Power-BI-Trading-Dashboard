
# 📊 Power BI Trading Strategy Dashboard

This project is a fully interactive **Power BI dashboard** built to analyze and compare the performance of multiple trading strategies. The dashboard enables users to track key trading KPIs, explore time-based insights, and drill down into trade-level details.

---

## 🔍 Project Objective

To provide a data-driven comparison between different trading strategies by visualizing performance metrics such as total profit/loss, win/loss ratio, and trade distribution across time.

---

## 📁 Project Structure





---

## ⚙️ Step-by-Step Development Process

### 1. 📥 Data Collection

- Gathered trade logs from **three different Excel files**, each representing a unique strategy:
  - `strategy_1.xlsx`
  - `strategy_2.xlsx`
  - `strategy_3.xlsx`

---

### 2. 🔧 Data Preparation in Power Query

- Loaded all three files into Power Query.
- Added a **custom column** in each file named `strategy_name`:
  - Filled with values: `Strategy_1`, `Strategy_2`, `Strategy_3`
- Appended all three tables into a new unified table named 
`total_trade`.

*Snapshot*

![Image](https://github.com/user-attachments/assets/3716ff78-d12a-4d9c-a58e-30fbe1d79015)


- Cleaned and transformed data:
  - Removed nulls and duplicates
  - Parsed date and time fields
  - Ensured proper data types

---

### 3. 🧠 Data Modeling (Power BI)

- Created relationships (if additional date or dimension tables were used).
- Defined key calculated **DAX measures**:
  - `Total PnL = SUM(total_trade[PnL])`
  - `Win Count = COUNTROWS(FILTER(total_trade, total_trade[PnL] > 0))`
  - `Loss Count = COUNTROWS(FILTER(total_trade, total_trade[PnL] < 0))`
  - `Entry Hour = HOUR(total_trade[Entry Datetime])`

---

### 4. 📊 Dashboard Pages

#### a. **Strategy Summary Page**
- KPI cards: Total PnL, Win Count, Loss Count
- Bar charts for strategy comparison
- Date and strategy slicers
- 🔁 **Drillthrough** enabled to navigate to detailed view per strategy

#### b. **Detailed Report Page**
- Line Chart: Cumulative PnL over time
- Bar Chart: Entry Hour vs Total PnL
- Interactive Table: Trade-level data (Symbol, Entry/Exit times, PnL, etc.)
- Dynamic filters for focused analysis

---

## 🧰 Tools & Technologies

- Power BI Desktop
- Power Query Editor
- DAX (Data Analysis Expressions)
- Microsoft Excel (Data Source)

---

## 📌 Key Features

- ✅ Drillthrough navigation between summary and details

![Image](https://github.com/user-attachments/assets/5c81eee6-544b-4441-a991-4bc9c48e89c8)

- ✅ Interactive filters and dynamic visuals
- ✅ Comparative analysis across multiple strategies
- ✅ Clean, minimal, and user-friendly dashboard layout

---

## 🚀 Getting Started

1. Clone this repository.
2. Replace the Excel files in `/Data` with your own strategy files (ensure consistent structure).
3. Open the `.pbix` file in Power BI Desktop.
4. Click **Refresh** to load updated data into the model.
5. Explore the dashboard and analyze performance metrics.

---

## 📸 Dashboard Previews

| Summary Page | Detailed Page |
|--------------|----------------|
|![Image](https://github.com/user-attachments/assets/894051f6-4142-4ed7-829c-cf854edd7cfb)|![Image](https://github.com/user-attachments/assets/b5fba1f2-e749-4d08-ad9b-ce996433e1bc)|


---
