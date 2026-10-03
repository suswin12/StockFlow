# StockFlow

**GitHub Repository:** https://github.com/suswin12/StockFlow

StockFlow is a full-stack inventory management system for managing products, stock levels, pricing, brands, and basic device specifications.

The project has a React + TypeScript frontend and an Express + TypeScript backend. The frontend provides the main inventory workspace, while the backend persists inventory data in JSON files.

## Features

- View inventory in a modern dashboard
- Add new products
- Edit product information
- Delete products
- Search products
- Filter by:
  - Brand
  - In-stock items
  - Low-stock items
  - Out-of-stock items
- Sort by:
  - Name
  - Price ascending
  - Price descending
  - Stock quantity
- Switch between table and grid views
- Increase/decrease stock directly from the inventory table
- Dashboard statistics for inventory
- Toast notifications for successful and failed operations
- Responsive UI built with Tailwind CSS
- Smooth UI transitions using GSAP
- Express REST API with CORS support
- JSON-based inventory persistence

## Tech Stack

### Frontend

- React 19
- TypeScript
- Vite
- Tailwind CSS
- GSAP / `@gsap/react`
- Oxlint

### Backend

- Node.js
- Express 5
- TypeScript
- CORS
- `tsx`
- JSON files for persistence

## Project Structure

```text
StockFlow/
├── backend/
│   ├── src/
│   │   ├── app.ts
│   │   ├── data.ts
│   │   ├── extra.ts
│   │   ├── IMS.ts
│   │   ├── interactions.ts
│   │   ├── inventory.json
│   │   └── removed.json
│   ├── utils/
│   │   └── vaildation.ts
│   ├── package.json
│   └── tsconfig.json
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── versions/
│   │   │   ├── v1_old/
│   │   │   ├── Version2GoodUI/
│   │   │   └── Version3Modern/
│   │   ├── types/
│   │   ├── data/
│   │   ├── App.tsx
│   │   └── main.tsx
│   ├── api/
│   │   └── api.ts
│   ├── public/
│   ├── package.json
│   └── vite.config.ts
│
└── README.md
```

## Requirements

Install the following before running the project:

- Node.js 18+ recommended
- npm

You can use another supported Node.js version, but the project dependencies should be checked if you encounter compatibility problems.

## Running Locally

The frontend and backend are separate applications, so run them in two terminals.

### 1. Start the backend

```bash
cd backend
npm install
npm run dev
```

The backend runs on:

```text
http://localhost:3000
```

Available API endpoints:

```text
GET    /products
GET    /products?search=<query>
POST   /products
PUT    /products/:id
DELETE /products/:id
```


## Stock Status

The current UI treats stock quantities as:

| Stock | Status |
|---:|---|
| `0` | Out of stock |
| `1–5` | Low stock |
| `6+` | In stock |

Stock can be adjusted directly from the product table using the `+` and `-` controls.


## Author

**Suswin Prasath**

GitHub: https://github.com/suswin12/StockFlow

## License

No license has been specified for this repository yet.
