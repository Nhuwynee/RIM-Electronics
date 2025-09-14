# Repair & Installation Management System — README

> **Project:** Website for Managing Repair & Installation of Electrical / Electronic Components
> Built as a student software project for Điện Máy Xanh (Da Nang, June 2025).&#x20;

---

## Overview

This project is a web-based management system that centralizes and automates the business processes of a small-to-medium enterprise operating in electrical and electronic device repair & installation. The system supports receiving customer requests, creating service orders, assigning technicians, tracking job progress, managing spare parts inventory, warranty lookups and reporting — improving operational efficiency and customer experience.&#x20;

---

## Key Features

* Customer-facing functions: account registration/login, submit service requests (with images & warranty info), track order status, view order history, view products/parts and promotions.&#x20;
* Service desk (CSKH) functions: view registrations, create service orders, check warranty, assign technicians, update orders, and communicate with customers.&#x20;
* Technician functions: view assigned jobs, update job status, record diagnostics & parts used, request additional parts, confirm completion.&#x20;
* Management functions: inventory (parts) management, approve parts requests, generate statistics/reports (parts, orders, revenue), and manage service orders.&#x20;
* Admin functions: user & role management (create/update/lock accounts), system overview.&#x20;

---

## Actors & Use Cases (summary)

* **Guest / Visitor:** register, browse services & parts, view warranty policy.
* **Customer:** login, place/track service orders, pay/cancel orders, rate services.
* **Customer Service (CSKH):** manage registrations, create & update service orders, assign technicians.
* **Technician:** accept/perform assigned jobs, update statuses, log parts & results.
* **Manager:** inventory control, reporting, oversee orders and staff requests.
* **Admin:** full user and system administration.
  (Full actor & use-case breakdown and scenarios are documented in the project report.)&#x20;

---

## Architecture & Technology Stack

* **Backend / Framework:** ASP.NET Core MVC (C#).&#x20;
* **Frontend:** Standard web stack (HTML, CSS, JavaScript).&#x20;
* **Database:** Microsoft SQL Server (relational DB; ERD and DB relationships included in documentation).&#x20;
* **Design approach:** Object-oriented analysis & design with Use Case diagrams, ER diagrams, class/sequence modeling.&#x20;

---

## Data Model & Screens (what's included)

* **ERD & DB relationship diagrams** describing entities: users (roles), customers, service orders, parts (inventory), warranties, payments, notifications/logs.&#x20;
* **Implemented UI pages / mockups** (documented): search/list pages for service orders, customers, parts and warranties; parts management CRUD; service order CRUD and payment UI; statistics and detailed reports screens.&#x20;

---

## Installation (developer setup)

> The following is a general guide based on the technologies in the report. Adapt paths/commands to your environment.

1. **Prerequisites**

   * .NET SDK (compatible with ASP.NET Core used in the project)
   * Microsoft SQL Server (or SQL Server Express)
   * Visual Studio / VS Code (recommended)
   * (Optional) Node.js if any frontend build tooling is used

2. **Database**

   * Create a new SQL Server database (name: e.g. `RepairManagementDB`).
   * Run the provided SQL scripts / migrations to create the schema and seed initial data (see `database/` or `migrations/` folder in repo). The report contains the ERD and table descriptions used by the system.&#x20;

3. **Configure the application**

   * Edit `appsettings.json` (or environment variables) to point to your SQL Server connection string and other environment-specific settings (SMTP, payment gateway placeholders if any).
   * Ensure any required secrets are set (JWT keys, SMTP credentials) in secure environment variables.

4. **Build & Run**

   * Open solution in Visual Studio and run, or from command-line:

     ```bash
     dotnet restore
     dotnet build
     dotnet run --project ./src/YourProject.Web
     ```
   * Visit `http://localhost:5000` (or configured port) to access the web UI.

---

## Testing

* Perform functional tests per role:

  * Guest flows: registration, submit request, warranty lookup.
  * Customer flows: order placement, tracking, payment, rating.
  * CSKH flows: create/assign/update orders, communication.
  * Technician flows: accept job, record diagnostics, request parts.
  * Manager/Admin flows: inventory operations, reporting, user management.
* UI mockups and test scenarios are documented in Chapter 2 (Giao diện chương trình) of the report.&#x20;

---

## Notes on Implementation & Project Scope

* The system is designed as a simulation of a small-to-medium company workflow: customer-facing features, internal staff roles, and inventory & warranty management are covered. Detailed functional specifications, process flows and use-case scenarios are included in the original report.&#x20;

---

## Future Improvements (suggestions)

* Add role-based API + SPA frontend for better UX (React/Vue).
* Real-time notifications (WebSocket) for order/assignment updates.
* Integrate a payment gateway for online payments and shipment tracking.
* Add automated tests (unit, integration, e2e) and CI/CD pipeline.
* Add analytics dashboard with historical trends and exportable reports.

---

## Project Documents & Reference

Primary project documentation, diagrams, UI mockups and analysis are contained in the original Word report submitted with this project. See the report for: objectives, actor/use-case lists, ERD, UI screenshots and implementation notes.&#x20;

---

## Authors & Acknowledgements

* Student author (SVTH) and academic supervisor: Nguyễn Thị Hà Quyên (acknowledged in the report). Thanks to the supporting faculty and reviewers.&#x20;

---

## License

Specify a license for your project (e.g., MIT) or state “All rights reserved” depending on your preference and university rules.

---

If you want, I can:

* Convert this README into a `README.md` file and attach it for download.
* Generate a short `INSTALL.md` or a `CONTRIBUTING.md` from the same project report.
* Extract specific diagrams (ERD / UseCase) into image files (if you provide the sources).

