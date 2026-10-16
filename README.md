# Retail Demand Planning Studio MVP v1.1

## Deploy to Vercel
1. Extract this ZIP.
2. Upload the **contents** to the root of GitHub repository `Retail-Demand-Planning`. `app/` and `package.json` must be at the top level.
3. In Vercel → Settings → Build and Deployment, leave Root Directory EMPTY.
4. Framework: Next.js. Build command: `npm run build`. Install command: `npm install`.
5. Commit and deploy.

Requires Node.js 18+ for local run (`npm install`, `npm run dev`).

## Features
- Reproducible mock history: 150 SKUs x 156 weeks.
- Dashboard, CSV/XLSX import, SKU+week upsert in session, data-quality review, SKU pattern heuristics, forecast methods selector, illustrative ROP/replenishment, S&OP scenario, Excel exports.
- Imported data is not persistent; refresh resets it. Connect PostgreSQL/Supabase before live business use.
- ARIMA/SARIMA, full backtesting, production model tournament, BOM-based MRP, approvals and persistent audit logs are not implemented in this MVP. Auto-selection and replenishment calculations are prototype logic and must be validated before operational use.

Import columns: `sku, product, category, brand, week, actual, price, promo, stockout, availability`.
