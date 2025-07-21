# 📦 Supplier Inventory Cost Simulation

This project uses **Monte Carlo simulation** to model and compare the performance of different suppliers in a B2B supply chain, based on their delivery times. It aims to minimize **total inventory cost**, composed of **holding** and **shortage** costs, under stochastic demand.

## 📁 Files

- `ch18.ipynb`: Main Jupyter Notebook for simulation.
- `B2B_Order_Data.csv`: Dataset containing supplier order and delivery dates.

---

## 🧮 Problem Setup

### 🎯 Objective
To identify the most cost-effective supplier by simulating the total inventory cost across:
- Holding cost (for keeping inventory in stock)
- Shortage cost (for not meeting demand)

### 🧠 Key Concepts Used
- **Monte Carlo simulation**: Repeated random sampling to estimate outcomes.
- **Inventory management**: Balance between having too much or too little inventory.
- **Lead time analysis**: Measure of supplier responsiveness.
- **Gaussian distribution**: Models daily customer demand.
- **Cost optimization**: Choose supplier with lowest average simulated cost.

---

## 📊 Dataset Description

`B2B_Order_Data.csv` contains:
- `Order_Date`: Date the order was placed.
- `Expected_Delivery_Date`: Promised delivery date by the supplier.
- `Supplier_ID`: ID of the supplier (SUP1, SUP2, SUP3).

We compute:

```python
Delivery_Time = Expected_Delivery_Date - Order_Date (in days)
