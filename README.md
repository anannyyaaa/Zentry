# Zentry
# Finance Intelligence Platform

A full-stack personal finance management platform that helps users track expenses, monitor budgets, detect unusual spending patterns, and gain actionable insights into their financial habits.

## Overview

Traditional expense trackers only show where money was spent. Finance Intelligence Platform goes a step further by analyzing spending behavior, identifying anomalies, forecasting future balances, and generating a financial health score to help users make smarter financial decisions.

## Problem Statement

Many individuals struggle to:

* Understand where their money is going
* Detect overspending before it becomes a problem
* Monitor recurring subscriptions
* Maintain monthly budgets
* Track overall financial health

This platform provides a centralized solution for managing personal finances while delivering intelligent insights through data-driven analysis.

---

## Features

### User Authentication

* Secure user registration and login
* JWT-based authentication
* Password hashing using bcrypt
* Protected routes and session management

### Expense Management

* Add, edit, and delete expenses
* Categorize transactions
* Track income and expenses separately
* Search and filter transaction history

### Budget Tracking

* Set monthly budgets
* Monitor spending against budget limits
* Budget utilization analytics
* Budget alerts and notifications

### Spending Analytics

* Monthly spending breakdown
* Category-wise expenditure analysis
* Interactive charts and visualizations
* Historical spending trends

### Anomaly Detection

Detect unusual spending behavior by comparing current expenses with historical spending patterns.

Example:

* Average food spending: ₹5,000/month
* Current food spending: ₹9,000/month

System flags the category as anomalous and alerts the user.

### Subscription Detection

Automatically identifies recurring expenses such as:

* Netflix
* Spotify
* Gym memberships
* SaaS subscriptions
* Utility bills

Provides a summary of recurring financial commitments.

### Balance Forecasting

Predicts end-of-month account balance based on:

* Historical spending patterns
* Current spending rate
* Recurring expenses
* Monthly income

Helps users proactively manage finances.

### Financial Health Score

Generates a score based on:

* Savings rate
* Budget adherence
* Expense consistency
* Subscription burden
* Spending discipline

Provides actionable recommendations for improvement.

---

## Tech Stack

### Frontend

* React.js
* Tailwind CSS
* Axios
* Chart.js / Recharts

### Backend

* Node.js
* Express.js
* JWT Authentication
* REST APIs

### Database

* PostgreSQL

### Caching

* Redis

### Deployment

* Vercel (Frontend)
* Render / Railway (Backend)
* Neon PostgreSQL

---

## System Architecture

Client → React Frontend

↓

Express API Server

↓

Redis Cache Layer

↓

PostgreSQL Database

---

## Database Design

### Users

* id
* name
* email
* password_hash
* created_at

### Transactions

* id
* user_id
* amount
* type (income/expense)
* category
* description
* transaction_date

### Budgets

* id
* user_id
* category
* monthly_limit

### Financial Scores

* id
* user_id
* score
* generated_at

---

## API Endpoints

### Authentication

POST /api/auth/register

POST /api/auth/login

GET /api/auth/profile

---

### Transactions

GET /api/transactions

POST /api/transactions

PUT /api/transactions/:id

DELETE /api/transactions/:id

---

### Budgets

GET /api/budgets

POST /api/budgets

PUT /api/budgets/:id

DELETE /api/budgets/:id

---

### Analytics

GET /api/analytics/spending

GET /api/analytics/anomalies

GET /api/analytics/forecast

GET /api/analytics/financial-health

---

## Key Backend Concepts Demonstrated

* REST API Design
* Authentication & Authorization
* Database Schema Design
* PostgreSQL Joins
* Database Indexing
* Transaction Management
* Redis Caching
* Pagination
* Error Handling
* Data Aggregation
* Financial Analytics
* Backend Architecture Design

---

## Future Enhancements

* UPI Integration
* Bank Account Aggregation
* AI-Based Financial Advisor
* Investment Portfolio Tracking
* Goal-Based Savings Planner
* SMS & Email Alerts
* Multi-Currency Support

---

## Learning Outcomes

Through this project, I gained practical experience with:

* Building scalable backend systems
* Designing relational databases
* Implementing authentication and authorization
* Financial data modeling
* Developing analytics-driven applications
* Deploying full-stack applications in production

---

## Author

Ananya Sharma

B.Tech Mechanical & Automation Engineering

IGDTUW, Delhi
