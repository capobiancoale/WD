# 🚲 Rental Bike Management System — University Database Project

![SQL](https://img.shields.io/badge/SQL-DDL%20%2F%20DML-blue?style=flat-square)
![Database](https://img.shields.io/badge/Database-Relational-orange?style=flat-square)
![Reporting](https://img.shields.io/badge/Reporting-KPI%20Dashboard-green?style=flat-square)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square)

---

## 📋 Project Overview

This repository contains the full implementation of a **Rental Bike Management System**, developed as part of a university database course. The project covers the complete database lifecycle — from schema design to data population and advanced analytical reporting.

The system models a bike-sharing application capable of tracking users, subscriptions, rides, routes, and billing data. It provides a foundation for operational management and strategic decision-making through a set of KPI-focused analytical queries.

---

## 🎯 Objectives

- Design and implement a normalized relational database schema using **DDL (Data Definition Language)**
- Populate the database with realistic, consistent sample data using **DML (Data Manipulation Language)**
- Develop **advanced analytical reports** to monitor key business performance indicators (KPIs)
- Demonstrate proficiency in SQL query design, including aggregations, joins, subqueries, and window functions

---

## 🗂️ Repository Structure

```
rental-bike-db/
│
├── ddl/
│   └── schema.sql              # Table definitions, constraints, indexes
│
├── dml/
│   └── populate.sql            # INSERT statements with sample dataset
│
├── reports/
│   ├── most_frequent_routes.sql
│   ├── avg_cost_per_ride.sql
│   ├── avg_subscription_cost.sql
│   └── avg_ride_duration.sql
│
└── README.md
```

---

## 🏗️ Database Schema

The schema is designed following **3rd Normal Form (3NF)** principles to ensure data integrity and minimize redundancy. Key entities include:

| Entity | Description |
|---|---|
| `Users` | Registered customers with profile and contact information |
| `Bikes` | Fleet inventory with type, status, and location data |
| `Stations` | Docking stations with geolocation attributes |
| `Rides` | Individual trip records linking users, bikes, and routes |
| `Routes` | Origin–destination pairs with distance and duration |
| `Subscriptions` | Membership plans and user subscription history |
| `Payments` | Billing records associated with rides and subscriptions |

---

## 📊 KPI Reports

The analytical layer includes four core reports designed to support business intelligence and operational monitoring:

### 1. Most Frequent Routes
> Identifies the top-performing origin–destination pairs by ride volume.

Useful for fleet redistribution, demand forecasting, and infrastructure planning. The query aggregates ride counts by route and ranks results using window functions.

### 2. Average Cost per Ride
> Calculates the mean revenue generated per individual ride.

Segments by user type, time period, and bike category to reveal pricing efficiency and revenue distribution patterns across the fleet.

### 3. Average Subscription Cost
> Computes the average revenue per active subscription plan.

Breaks down subscription economics by plan tier and enrollment period, supporting pricing strategy and customer lifetime value analysis.

### 4. Average Ride Duration
> Measures the mean duration of completed rides across all users and routes.

Provides insight into usage behaviour, station proximity, and potential operational bottlenecks such as bike availability or route congestion.

---

## 🛠️ Technologies Used

| Tool | Purpose |
|---|---|
| SQL (DDL) | Schema definition — tables, constraints, primary/foreign keys, indexes |
| SQL (DML) | Data population — INSERT statements with referential integrity |
| SQL (DQL) | Analytical queries — aggregations, JOINs, subqueries, window functions |


---

## 📈 Sample KPI Output

```
-- Most Frequent Routes (sample output)
+------------------+------------------+------------+
| origin_station   | dest_station     | ride_count |
+------------------+------------------+------------+
| Central Park N   | Times Square     |        342 |
| Brooklyn Bridge  | Manhattan Pier   |        289 |
| Grand Central    | Union Square     |        251 |
+------------------+------------------+------------+

-- Average Cost per Ride (sample output)
+-------------+------------------+
| user_type   | avg_cost_eur     |
+-------------+------------------+
| Subscriber  |            1.85  |
| Guest       |            4.20  |
+-------------+------------------+
```

---

## 📚 Academic Context

| Field | Details |
|---|---|
| **Course** | Database Management Warehouse / SQL Programming |
| **Degree** | Master Data Science for Management |
| **Institution** | Catholic University of the Sacred Heart, Milan |
| **Academic Year** | 2025 / 2026 |
| **Author** | Alessio Capobianco |

---

## 👤 Author

**Alessio Capobianco**
- 📧 [Alessiocapobianco3@gmail.com](mailto:Alessiocapobianco3@gmail.com)
- 💼 [LinkedIn](https://www.linkedin.com/in/alessio-capobianco/)


---

*This project was developed for academic purposes as part of the MSc in Data Science for Management curriculum.*
