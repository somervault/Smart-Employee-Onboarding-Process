# Smart Employee Onboarding Portal

A custom ServiceNow application that automates employee onboarding using the Service Catalog, Record Producers, Variable Sets, UI Policies, Client Scripts, Flows, and custom tables.

---

## Project Overview

The Smart Employee Onboarding Portal streamlines the employee onboarding process by allowing managers to submit onboarding requests through a Service Catalog item.

The application captures employee information, validates user input, dynamically adapts the form based on selections, and (in future phases) automatically generates onboarding tasks for different departments.

---

## Features Implemented

### Custom Tables

- Onboarding Request
- Onboarding Task

Relationship:

Onboarding Request
└── Multiple Onboarding Tasks

---

### Security

Created custom application roles:

- Admin
- Manager
- User

Configured Access Control Rules (ACLs) for secure access to application records.

---

### Service Catalog

Created:

- Service Catalog Item
- Employee Onboarding Record Producer

The Record Producer serves as the main entry point for submitting onboarding requests.

---

### Reusable Variable Sets

Created reusable Variable Sets:

- Employee Details
- Employment Details
- Asset Requirements
- Additional Information

These variable sets can be reused across future catalog items.

---

### Employee Details

Implemented variables:

- Employee Name
- Personal Email
- Employee Contact Number
- Manager
- Requested By

---

### Employment Details

Implemented variables:

- Department
- Job Role
- Joining Date
- Work Location

---

### Asset Requirements

Implemented variables:

- Laptop Required
- Laptop Type
- Required Software

---

### Additional Information

Implemented variables:

- Additional Remarks

---

## Dynamic Client-Side Logic

Implemented Catalog Client Scripts:

### Department → Job Role Filtering

Selecting a department dynamically updates the available Job Roles.

Examples:

Information Technology

- Software Engineer
- QA Engineer
- Cloud Engineer
- DevOps Engineer
- ServiceNow Developer

Human Resources

- HR Executive
- Talent Acquisition
- HR Manager
- HR Business Partner

Marketing

- Marketing Executive
- Digital Marketing Specialist
- Content Strategist
- SEO Specialist

Finance

- Accountant
- Financial Analyst
- Payroll Specialist
- Finance Manager

Sales

- Sales Executive
- Business Development Executive
- Account Manager
- Sales Manager

Operations

- Operations Executive
- Operations Manager
- Supply Chain Coordinator
- Logistics Coordinator

---

### Laptop Type Visibility

Implemented Catalog UI Policy:

If

Laptop Required = Yes

Then

Laptop Type becomes:

- Visible
- Mandatory

Otherwise the field is hidden automatically.

---

## Technologies Used

- ServiceNow Studio
- Service Catalog
- Record Producer
- Variable Sets
- Catalog Client Scripts
- Catalog UI Policies
- Access Control Rules (ACLs)
- Custom Tables

---

## Current Project Status

Completed

- Data Model
- Custom Tables
- Roles
- ACLs
- Record Producer
- Variable Sets
- Dynamic Form Behaviour
- Department-based Job Role Filtering
- Laptop Visibility Logic

In Progress

- Flow Designer Automation

Planned

- Automatic Task Creation
- Conditional Task Assignment
- Request Lifecycle Automation
- Notifications
- Dashboard & Reports

---

## Project Structure

Smart Employee Onboarding Portal

├── Custom Tables
│   ├── Onboarding Request
│   └── Onboarding Task
│
├── Security
│   ├── Admin
│   ├── Manager
│   └── User
│
├── Service Catalog
│   └── Employee Onboarding Record Producer
│
├── Variable Sets
│   ├── Employee Details
│   ├── Employment Details
│   ├── Asset Requirements
│   └── Additional Information
│
├── Client Scripts
│   └── Department → Job Role Filtering
│
├── UI Policies
│   └── Laptop Required → Laptop Type
│
└── Flow Designer (Upcoming)
