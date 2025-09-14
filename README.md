# 🔧 Repair & Installation Management System — README

> **Project:** Website for Managing Repair & Installation of Electrical / Electronic Components

---

## 🚀 Overview

This project is a web-based management system that centralizes and automates the business processes of a small-to-medium enterprise operating in electrical and electronic device repair & installation. The system supports receiving customer requests, creating service orders, assigning technicians, tracking job progress, managing spare parts inventory, warranty lookups and reporting — improving operational efficiency and customer experience.

---

## ✨ Key Features

* **Customer-facing:** account registration/login, submit service requests (with images & warranty info), track order status, view order history, view products/parts and promotions.
* **Service desk (CSKH):** view registrations, create service orders, check warranty, assign technicians, update orders, and communicate with customers.
* **Technician:** view assigned jobs, update job status, record diagnostics & parts used, request additional parts, confirm completion.
* **Management:** inventory (parts) management, approve parts requests, generate statistics/reports (parts, orders, revenue), and manage service orders.
* **Admin:** user & role management (create/update/lock accounts), system overview.

---

## 👥 Actors & Use Cases (summary)

* **Guest / Visitor:** register, browse services & parts, view warranty policy.
* **Customer:** login, place/track service orders, pay/cancel orders, rate services.
* **Customer Service (CSKH):** manage registrations, create & update service orders, assign technicians.
* **Technician:** accept/perform assigned jobs, update statuses, log parts & results.
* **Manager:** inventory control, reporting, oversee orders and staff requests.
* **Admin:** full user and system administration.

> Full actor & use-case breakdown and scenarios are documented in the project report.

---

## 🏗 Architecture & Technology Stack

* **Backend / Framework:** ASP.NET Core MVC (C#).
* **Frontend:** Standard web stack (HTML, CSS, JavaScript).
* **Database:** Microsoft SQL Server (relational DB; ERD and DB relationships included in documentation).
* **Design approach:** Object-oriented analysis & design with Use Case diagrams, ER diagrams, class/sequence modeling.

---

## 🗄 Data Model & Screens (what's included)

* **ERD & DB relationship diagrams** describing entities: users (roles), customers, service orders, parts (inventory), warranties, payments, notifications/logs.
* **Implemented UI pages / mockups:** search/list pages for service orders, customers, parts and warranties; parts management CRUD; service order CRUD and payment UI; statistics and detailed reports screens.

---

## 🛠 Installation (developer setup)

> The following is a general guide based on the technologies in the report. Adapt paths/commands to your environment.

1. **Prerequisites**

   * .NET SDK (compatible with ASP.NET Core used in the project)
   * Microsoft SQL Server (or SQL Server Express)
   * Visual Studio / VS Code (recommended)
   * (Optional) Node.js if any frontend build tooling is used

2. **Database**

   * Create a new SQL Server database (e.g. `RepairManagementDB`).
   * Run the provided SQL scripts / migrations to create the schema and seed initial data (see `database/` or `migrations/` folder in repo).

3. **Configure the application**

   * Edit `appsettings.json` (or environment variables) to point to your SQL Server connection string and other environment-specific settings (SMTP, payment gateway placeholders if any).
   * Ensure any required secrets are set (JWT keys, SMTP credentials) in secure environment variables.

4. **Build & Run**

```bash
# from repo root
dotnet restore
dotnet build
dotnet run --project ./src/YourProject.Web
```

* Visit `http://localhost:5000` (or configured port) to access the web UI.

---

## ✅ Testing

* Perform functional tests per role:

  * Guest flows: registration, submit request, warranty lookup.
  * Customer flows: order placement, tracking, payment, rating.
  * CSKH flows: create/assign/update orders, communication.
  * Technician flows: accept job, record diagnostics, request parts.
  * Manager/Admin flows: inventory operations, reporting, user management.

> UI mockups and test scenarios are documented in the project report.

---

## 📌 Notes on Implementation & Project Scope

* The system is designed as a simulation of a small-to-medium company workflow: customer-facing features, internal staff roles, and inventory & warranty management are covered. Detailed functional specifications, process flows and use-case scenarios are included in the original report.

---

## 🔮 Future Improvements (suggestions)

* Add role-based API + SPA frontend for better UX (React/Vue).
* Real-time notifications (WebSocket) for order/assignment updates.
* Integrate a payment gateway for online payments and shipment tracking.
* Add automated tests (unit, integration, e2e) and CI/CD pipeline.
* Add analytics dashboard with historical trends and exportable reports.

---

## 📂 Project Documents & Reference

Primary project documentation, diagrams, UI mockups and analysis are contained in the original Word report submitted with this project. See the report for: objectives, actor/use-case lists, ERD, UI screenshots and implementation notes.


