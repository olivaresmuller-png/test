# Asset Analyzer

A comprehensive asset analysis and management tool built with React, Vite, Express, and PostgreSQL.

## Features

- **Dashboard**: Overview of total value, asset categories, and active alerts.
- **Asset Management**: Add, edit, and track assets with details like cost, scrap value, and useful life.
- **Depreciation Calculation**: Real-time calculation of asset depreciation (Straight Line & Double Declining methods).
- **Reports**: Generate reports including Asset List, Depreciation Schedule, and Net Value/ROI Analysis.
- **Data Import/Export**: Import assets from CSV/Excel and export reports.
- **Settings**: Configure default methods, alerts, and user preferences.
- **Admin**: User management and system audit logs.

## Tech Stack

- **Frontend**: React 19, Vite, TailwindCSS (v4), Radix UI, Framer Motion, Recharts.
- **Backend**: Node.js, Express.
- **Database**: PostgreSQL with Drizzle ORM.
- **Language**: TypeScript throughout the stack.

## Prerequisites

- Node.js (v20 or later recommended)
- PostgreSQL Database

## Setup

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd Asset-Analyzer
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    ```

3.  **Environment Variables:**
    Copy `.env.example` to `.env` and fill in your database credentials.
    ```bash
    cp .env.example .env
    ```
    Update `DATABASE_URL` in `.env`.

4.  **Database Migration:**
    Push the schema to your database.
    ```bash
    npm run db:push
    ```

5.  **Run Development Server:**
    ```bash
    npm run dev
    ```
    This starts the backend server, which also serves the frontend in development mode.

## Scripts

- `npm run dev`: Start the development server.
- `npm run build`: Build the frontend and backend for production.
- `npm run start`: Start the production server.
- `npm run check`: Run TypeScript type checking.
- `npm run db:push`: Push Drizzle schema changes to the database.

## Standalone Usage (No Server Required)

This application is designed to work completely offline in the browser.

1.  **Build the application:**
    ```bash
    npm run build
    ```
2.  **Open the App:**
    - Navigate to the `dist/public` folder.
    - Double-click `index.html`.
    - The app will load in your browser. All data is saved to your browser's Local Storage.

### Data Portability
Since there is no central server, your data lives on your device.
- To move to another computer: Go to Settings/Sync > **Export Data**.
- On the new computer: Go to Settings/Sync > **Import Data**.

## Running on GitHub (Online)

You can host this application directly on GitHub for free.

1.  **Push the code** to your GitHub repository.
2.  Go to your Repository **Settings** -> **Pages**.
3.  Under **Build and deployment**, select **Source** as **GitHub Actions**.
4.  The action configured in `.github/workflows/deploy.yml` will automatically build and deploy the app.
5.  Once the "pages build and deployment" action finishes (check the **Actions** tab), you will get a URL (e.g., `https://yourname.github.io/repo-name/`).
6.  Click the URL to use your app online!


