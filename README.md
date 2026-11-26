# Warehouse Inventory Management System

An Oracle Database project for managing warehouse inventory, suppliers, and inbound shipments. Developed as part of a Database course project.

## Overview

The Warehouse Inventory Management System manages:

- Inventory items and their stock quantities.
- Suppliers and their contact information.
- Incoming shipments from suppliers.
- Shipment costs and inventory updates.
- Discontinued items and inventory validation.
- Shipment activity logging and database reporting.

## Tech Stack

| Technology              | Purpose                   |
| ----------------------- | ------------------------- |
| Oracle Database 23 Free | Relational database       |
| Docker                  | Database containerization |
| Docker Compose          | Container management      |
| SQL / PL/SQL            | Database logic            |
| Visual Studio Code      | Development environment   |

## Project Structure

```text
warehouse-inventory/
│
├── compose.yaml
├── README.md
│
├── sql/
│   ├── person-1-database-administration/
│   ├── person-2-database-design/
│   ├── person-3-functions/
│   ├── person-4-stored-procedure/
│   ├── person-5-reporting/
│   └── person-6-blocking-deadlock/
```

## Database Schema

### Items

| Column         | Description                      |
| -------------- | -------------------------------- |
| ItemID         | Primary key                      |
| Name           | Item name                        |
| Category       | Item category                    |
| UnitCost       | Cost per unit                    |
| StockQuantity  | Available stock                  |
| IsDiscontinued | Whether the item is discontinued |

### Suppliers

| Column     | Description           |
| ---------- | --------------------- |
| SupplierID | Primary key           |
| Name       | Supplier name         |
| Phone      | Supplier phone number |

### Shipments

| Column     | Description                       |
| ---------- | --------------------------------- |
| ShipmentID | Primary key                       |
| ItemID     | Foreign key referencing Items     |
| SupplierID | Foreign key referencing Suppliers |
| ShipDate   | Shipment date                     |
| Quantity   | Received quantity                 |
| TotalCost  | Total shipment cost               |

## Team Responsibilities

| Person   | Responsibility                          |
| -------- | --------------------------------------- |
| Person 1 | Database Administration                 |
| Person 2 | Database Design & Trigger               |
| Person 3 | SQL Functions                           |
| Person 4 | Stored Procedure & Additional SQL Query |
| Person 5 | Reporting & Views                       |
| Person 6 | Blocking & Deadlock Demonstrations      |

## Database Requirements

The project includes:

- Database users and custom roles.
- System and object privileges.
- Primary keys, foreign keys and constraints.
- Sequences for ID generation.
- PL/SQL functions and stored procedures.
- Triggers and audit logging.
- SQL views and reporting.
- Transaction blocking and deadlock demonstrations.

## Setup

### Prerequisites

- Docker Desktop
- Visual Studio Code
- Oracle SQL Developer extension for VS Code

### 1. Clone the repository

```bash
git clone <repository-url>
cd warehouse-inventory
```

### 2. Start Oracle Database

```bash
docker compose up -d
```

### 3. Check the container

```bash
docker compose ps
```

### 4. Database Connection

| Setting                     | Value     |
| --------------------------- | --------- |
| Host                        | localhost |
| Port                        | 1521      |
| Service Name                | FREEPDB1  |
| Initial administrative user | SYSTEM    |

Use the password configured in `compose.yaml`.

### 5. Execute SQL Scripts

Execute the SQL scripts using the appropriate Oracle database accounts and in the order specified by the project requirements.

## Development Status

**Project status:** In Development

- [x] Project structure initialized
- [x] Oracle Docker environment configured
- [x] Initial database administration setup
- [ ] Create project database users
- [ ] Create database tables and constraints
- [ ] Insert reference data
- [ ] Implement SQL functions
- [ ] Implement shipment stored procedure
- [ ] Implement reporting and views
- [ ] Implement audit trigger
- [ ] Demonstrate blocking and deadlocks
- [ ] Complete testing and documentation

## Academic Project

**Project:** Warehouse Inventory System
**Database:** Oracle Database
**Course:** Database 2

Developed collaboratively by a team of six students.

