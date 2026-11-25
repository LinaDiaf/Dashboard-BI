
# Business Intelligence Dashboard — Sales, Purchases & Profit Margins

## Overview

**Dashboard BI** is an interactive web application designed to analyze commercial data and monitor business performance. It provides a centralized view of sales, purchases, and profit margins through key performance indicators (KPIs), interactive charts, detailed tables, and dynamic filters.

The application is organized into three complementary analytical sections.

## Features

### 1. Sales Analysis

- Monitor total sales revenue, including tax (TTC) and excluding tax (HT).
- Analyze quantities sold and the number of sales orders.
- Identify top-performing customers and product categories.
- Explore sales by product, category, customer, wilaya, legal structure, and sales type.
- Track monthly sales revenue trends.
- View sales rankings and detailed transaction tables.

### 2. Purchase Analysis

- Monitor total purchase costs, including tax (TTC) and excluding tax (HT).
- Analyze purchased quantities and the number of purchase orders.
- Track suppliers and product categories.
- Explore purchases by product, supplier, and purchase type.
- Compare costs across suppliers and product categories.
- Track monthly purchase trends.
- View purchase rankings and detailed transaction tables.

### 3. Profit Margin Analysis — Weighted Average Cost (WAC)

This section evaluates sales profitability using the **Weighted Average Cost (WAC)** method, also known as *Coût Moyen Unitaire Pondéré (CMUP)*.

Key capabilities include:

- Calculate unit profit margins and total profit margins (excluding tax).
- Monitor sales revenue and profit margin rates.
- Analyze profitability by product, category, and wilaya.
- Compare sales revenue, product costs, and profit margins.
- Visualize monthly profit margin trends.
- Examine purchase and sales transactions and their impact on inventory levels and WAC.

The WAC is recalculated after each purchase transaction and subsequently used to determine the cost of goods sold and the resulting profit margins.

## General Features

- Navigation between the three analytical sections.
- Dynamic filtering by date, product, category, and other relevant dimensions.
- Automatic updates of KPIs, charts, and tables based on selected filters.
- Filter reset functionality.
- Interactive data visualizations and detailed data tables.

## Technologies

| Technology | Purpose |
|---|---|
| HTML5 | Application structure |
| CSS3 | Layout and responsive design |
| JavaScript (ES Modules) | Business logic and data processing |
| Chart.js | Data visualization |
| Vite | Development environment and build tool |
| CSV | Source data storage and exchange |

## Project Structure

```text
Dashboard-BI/
│
├── index.html
├── package.json
├── package-lock.json
├── generate-merged.js
│
├── public/
│   ├── vente.csv
│   ├── achat.csv
│   └── merged_data.csv
│
└── src/
    ├── main.js
    ├── parser.js
    ├── utils.js
    ├── ventes.js
    ├── achats.js
    └── marges.js
```

### Main Modules

- **main.js**: Application entry point, data loading, and navigation management.
- **parser.js**: CSV file parsing and data transformation.
- **utils.js**: Shared utility functions for charts, aggregations, formatting, and filtering.
- **ventes.js**: Sales indicators, calculations, and visualizations.
- **achats.js**: Purchase indicators, calculations, and visualizations.
- **marges.js**: Profit margin analysis and WAC-based calculations.
- **generate-merged.js**: Generates the consolidated `merged_data.csv` file from purchase and sales data.

## Installation and Setup

### Prerequisites

- Node.js
- npm

### 1. Clone the repository

```bash
git clone https://github.com/linadi17/Dashboard-BI.git
cd Dashboard-BI
```

### 2. Install dependencies

```bash
npm install
```

### 3. Generate consolidated data

The consolidated dataset can be generated from the original purchase and sales CSV files:

```bash
node generate-merged.js
```

### 4. Run the development server

```bash
npm run dev
```

Open the local URL displayed in the terminal, usually:

```text
http://localhost:5173
```

### 5. Build for production

```bash
npm run build
```

To preview the production build locally:

```bash
npm run preview
```

## Data Sources

The application uses three CSV files:

- **vente.csv**: Sales transaction data.
- **achat.csv**: Purchase transaction data.
- **merged_data.csv**: Consolidated dataset used for profit margin analysis and WAC calculations.

The source CSV files must be placed in the `public/` directory. The consolidated dataset can be regenerated at any time using `generate-merged.js`.

---

**Business Intelligence Dashboard — Sales, Purchases & Profit Margin Analysis**

*An interactive business intelligence dashboard for commercial performance analysis.*
