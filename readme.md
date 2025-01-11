Here's a structured, full Markdown version of the README file:

```markdown
# Roxiler Systems Assignment

This project is a full-stack application that provides a transaction dashboard. It includes a backend built with **Node.js**, **Express**, and **MongoDB**, and a frontend built with **React** and **Tailwind CSS**.

---

## Table of Contents

- [Installation](#installation)
- [Backend](#backend)
  - [API Endpoints](#api-endpoints)
- [Frontend](#frontend)
  - [Components](#components)
- [Running the Application](#running-the-application)

---

## Installation

To get started with this project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/roxiler-systems-assignment.git
   cd roxiler-systems-assignment
   ```

2. Install dependencies for both backend and frontend:

   ```bash
   # Install backend dependencies
   cd backend
   npm install

   # Install frontend dependencies
   cd ../frontend
   npm install
   ```

---

## Backend

The backend is built with **Node.js**, **Express**, and **MongoDB**. It provides several API endpoints to interact with the transaction data.

### API Endpoints

#### 1. **Initialize Database**

- **URL**: `/api/initDatabase`  
- **Method**: `GET`  
- **Description**: Fetches transaction data from an external source and initializes the database.

#### 2. **List Transactions**

- **URL**: `/api/transactions`  
- **Method**: `GET`  
- **Query Parameters**:
  - `month` (string): The month to filter transactions (default: `"March"`).
  - `search` (string): The search text to filter transactions.
  - `page` (number): The page number for pagination (default: `1`).
  - `perPage` (number): The number of transactions per page (default: `10`).
  - `sortField` (string): The field to sort transactions by (default: `"dateOfSale"`).
  - `sortDirection` (string): The sort direction (`"asc"` or `"desc"`, default: `"asc"`).
- **Description**: Lists transactions with search and pagination.

#### 3. **Statistics**

- **URL**: `/api/statistics`  
- **Method**: `GET`  
- **Query Parameters**:
  - `month` (string): The month to filter transactions (default: `"March"`).
- **Description**: Provides statistics for the total sale amount, total sold items, and total not sold items for a given month.

#### 4. **Bar Chart**

- **URL**: `/api/barChart`  
- **Method**: `GET`  
- **Query Parameters**:
  - `month` (string): The month to filter transactions (default: `"March"`).
- **Description**: Provides data for a bar chart showing the number of items sold based on price range for a given month.

#### 5. **Pie Chart**

- **URL**: `/api/pieChart`  
- **Method**: `GET`  
- **Query Parameters**:
  - `month` (string): The month to filter transactions.
- **Description**: Provides data for a pie chart showing the distribution of items sold by category for a given month.

#### 6. **Combined Response**

- **URL**: `/api/combinedResponse`  
- **Method**: `GET`  
- **Query Parameters**:
  - `month` (string): The month to filter transactions.
- **Description**: Provides a combined response with transactions, statistics, bar chart data, and pie chart data for a given month.

---

## Frontend

The frontend is built with **React** and **Tailwind CSS**. It provides a user interface to interact with the transaction data.

### Components

1. **`App.jsx`**:  
   The main component that renders the transaction dashboard.

2. **`MonthAndSearch.jsx`**:  
   A component for selecting the month and searching transactions.

3. **`TransactionTable.jsx`**:  
   A component for displaying the list of transactions with pagination.

4. **`Statistics.jsx`**:  
   A component for displaying statistics for the selected month.

5. **`BarChart.jsx`**:  
   A component for displaying a bar chart of items sold based on price range for the selected month.

6. **`PerPage.jsx`**:  
   A component for selecting the number of transactions per page.

---

## Running the Application

To run the application, follow these steps:

1. Start the backend server:
   ```bash
   cd backend
   npm start
   ```

2. Start the frontend development server:
   ```bash
   cd frontend
   npm start
   ```

3. Open your browser and navigate to `http://localhost:3000` to view the application.

---
