# Share-Tool

## Description
SharedTool is an **ASP.NET MVC application** designed to manage and share tools inside an organization or workshop.  
The system allows users to **view available tools, request to borrow them, and track borrowing history**.

Administrators can manage tools and control borrowing approvals, while users can browse and request tools when needed.

The project uses **ASP.NET Identity** for authentication and role management.

---

## Main Features

### User Management
- Authentication using ASP.NET Identity
- Role-based access control
- Users can request to borrow tools

### Tool Management
- Add, edit, and delete tools
- Track available quantity
- Store tool description and image

### Borrowing System
- Users can request tools
- Admin approval for borrowing
- Track borrowing date and status

---

## Technologies Used

- ASP.NET MVC
- C#
- Entity Framework
- SQL Server
- HTML / CSS / JavaScript

---

## Installation Guide

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/SharedTool.git
```

### 2. Configure the Database

Open **SQL Server Management Studio (SSMS)** and run the following scripts.

First run:

```
SharedTool.DAL/Queries/FirstInitial.sql
```

This script will:

- Create the database
- Create all tables
- Configure relationships and constraints

---

### 3. Insert Seed Data

After running the first script, run:

```
SharedTool.DAL/Queries/data.sql
```

This script contains **initial seed data required by the system**.

---

### 4. Configure Connection String

Open the **Web.config** file in the MVC project and update the SQL Server connection string.

---

### 5. Run the Application

Open the solution in **Visual Studio** and run the project.

---

## Project Architecture

The solution follows a layered architecture:

```
SharedTool
│
├── SharedTool (ASP.NET MVC - Presentation Layer)
├── SharedTool.Business (Business Logic)
└── SharedTool.DAL (Data Access Layer & Database Scripts)
```

---

## Purpose

This project demonstrates how to build a **structured ASP.NET MVC application with layered architecture**, database management, and role-based user access.

It also shows how to implement a **simple resource sharing system** where tools can be managed and borrowed by users.
