# End-to-End Supply Chain Analytics & Power BI Dashboard

An end-to-end Supply Chain Analytics solution built with **Power BI**, providing actionable insights across procurement, production, inventory management, shipping logistics, and sales performance.

---

## 📊 Overview

This project analyzes key operational metrics across the entire supply chain lifecycle:
- **Procurement & Supplier Performance**: Lead times, purchase orders, quality scores, supplier tiers.
- **Production Efficiency**: Daily output, defect rates, batch tracking, capacity utilization across manufacturing facilities.
- **Inventory Control**: Stock levels vs. safety stock, reorder point monitoring, stockout risk mitigation.
- **Logistics & Shipments**: Carrier performance, shipping costs, delivery statuses, transit delay factors.
- **Sales & Profitability**: Customer channels, gross/net revenue, order margins, discount analysis.

---

## 📁 Repository Structure

```text
├── Images/                  # Dashboard icons, design assets, and visual elements
├── dashboard1.pbix          # Interactive Power BI Dashboard report
├── dim_customer.csv         # Customer details, channels, and tiers
├── dim_date.csv             # Date dimension table
├── dim_facility.csv         # Manufacturing and warehouse facility specs
├── dim_product.csv          # Product catalog, pricing, cost, specs
├── dim_supplier.csv         # Supplier details, specialty, and ratings
├── fact_inventory.csv       # Stock levels, safety stock, and reorder levels
├── fact_procurement.csv     # Purchase orders, lead times, and unit costs
├── fact_production.csv      # Production batches, quantities, defect rates
├── fact_sales.csv           # Sales transactions, revenue, and margins
├── fact_shipment.csv        # Shipment logistics, tracking, carriers, delays
└── README.md                # Project documentation
```

---

## 🛠️ Data Model & Architecture

The analytical model follows a **Star Schema / Multi-Fact Galaxy Schema** linking dimension tables with multiple business process fact tables:

- **Dimensions**:
  - `dim_customer`: Customer ID, Key, Name, Country, Channel, Size.
  - `dim_facility`: Facility ID, Key, Name, Location, Specialization, Capacity.
  - `dim_product`: Product ID, SKU Key, Name, Category, Product Line, Cost & Price.
  - `dim_supplier`: Supplier ID, Key, Name, Location, Specialty, Tier, Quality Score.
  - `dim_date`: Temporal reference for order, production, shipment, and inventory dates.

- **Fact Tables**:
  - `fact_procurement`: PO tracking, supplier delivery lead times, procurement spend.
  - `fact_production`: Plant-level production volume and defective units.
  - `fact_inventory`: Facility-level stock on hand vs. safety stock limits.
  - `fact_shipment`: Logistics carriers, transit status, freight costs, delivery dates.
  - `fact_sales`: Sales orders, quantities, net revenue, total costs, profit margins.

---

## 🚀 Getting Started

1. **Clone the repository**:
   ```bash
   git clone <REPO_URL>
   ```
2. **Open the Dashboard**:
   - Double-click [`dashboard1.pbix`](./dashboard1.pbix) in Power BI Desktop.
   - If prompted to refresh data sources, verify file paths point to the local CSVs.
