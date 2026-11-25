
# Business Intelligence Dashboard

An interactive Business Intelligence dashboard for analyzing sales, purchases, and profit margins. The application provides key performance indicators (KPIs), interactive charts, and detailed data tables to support commercial performance analysis.

## Features

- **Sales Analysis:** Track sales revenue, quantities sold, customers, and product performance.
- **Purchase Analysis:** Monitor purchase costs, quantities, suppliers, and purchasing trends.
- **Profit Margin Analysis:** Calculate and analyze profit margins using the Weighted Average Cost (WAC / CMUP) method.
- **Interactive Visualizations:** Explore business data through dynamic charts, KPIs, and filters.

## Technologies

- HTML5 & CSS3
- JavaScript (ES Modules)
- Chart.js
- Vite
- CSV

## Installation

```bash
git clone https://github.com/LinaDiaf/Dashboard-BI.git
cd Dashboard-BI
npm install
node generate-merged.js
npm run dev
```

Open the local URL provided by Vite to access the dashboard.

## Project Structure

- `src/main.js` — Application entry point and navigation.
- `src/parser.js` — CSV data parsing.
- `src/ventes.js` — Sales analysis.
- `src/achats.js` — Purchase analysis.
- `src/marges.js` — Profit margin calculations and analysis.
- `src/utils.js` — Shared utility functions.
- `generate-merged.js` — Generates the consolidated dataset.

## Live Demo

[Open the Dashboard](https://dashbordbi.vercel.app)

## Repository

[GitHub — LinaDiaf/Dashboard-BI](https://github.com/LinaDiaf/Dashboard-BI)
