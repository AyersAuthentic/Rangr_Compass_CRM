# Rangr Compass CRM

![Status](https://img.shields.io/badge/Status-Completed-success)
![Platform](https://img.shields.io/badge/Platform-Palantir%20Foundry-blue)

**Author:** Kevin [Your Last Name]
**Date Completed:** October 16, 2025

---

## 1. Project Description

**Rangr Compass CRM** is a functional prototype of a Customer Relationship Management application, developed as a work sample for Rangr Data. Built entirely within the Palantir Foundry platform, this project addresses the core business need for a sales team to manage customer data effectively.

The application ingests, cleans, and models raw company and person datasets into a unified Ontology. This structured back-end powers a simple user interface where users can navigate from a company to its associated contacts. The emphasis is on robust functionality, demonstrated through Ontology-backed Actions that allow users to add new contacts and log interactions directly from the application, showcasing the ability to translate a business requirement into a practical, user-centric tool.

[A short GIF demonstrating the application's core workflow. e.g., Navigating from the company list to a detail page and logging an interaction.]

## 2. The Challenge

The objective was to design and build a CRM application within a one-month timeframe using a provided Palantir Foundry sandbox environment. The prompt specified using two datasets (companies and people) as the foundation for the application's data model.

The core goal was to assess the ability to translate a business need into an application, emphasizing **robust functionality (Actions, Links)** and clear use-case insights over complex visualizations. The final deliverable includes a 5-minute presentation and a live-edit session.

## 3. My Solution: The Consultant Mindset

I approached this challenge not just as a technical exercise, but as a rapid consulting engagement. To ensure the application was grounded in a real-world need, I developed a simple user persona:

> **Persona: "Alex," a sales representative.** Alex needs a straightforward tool to quickly view all contacts associated with a company and log new interactions (calls, meetings) without getting lost in a complex system.

The name **"Rangr Compass CRM"** reflects this goal: to provide a tool that gives sales reps like Alex clear direction and helps them navigate their customer relationships. Every feature was built to directly serve Alex's needs.

## 4. Core Features

* ✅ **Unified Company & Contact View:** A clean interface to see all companies at a glance.
* 🔗 **Linked Objects:** Clicking a company seamlessly navigates to a detail page showing all of its associated contacts, leveraging the power of the Ontology.
* ➕ **Action: Add New Contact:** A user-friendly form that allows Alex to add a new person and automatically link them to the correct company.
* 📝 **Action: Log Interaction:** A simple, powerful action to record an interaction (e.g., 'Call', 'Email', 'Meeting') with a specific contact, creating a history of communication.
* 📊 **KPI Widget:** A simple dashboard card displaying the total number of contacts in the system.

## 5. Technical Implementation

The application was built end-to-end using native Foundry tools.

### a. Data Pipeline (Pipeline Builder)
The backend pipeline was constructed in Pipeline Builder to ensure the data was clean, structured, and ready for the Ontology.
* **Ingestion:** The raw `company` and `person` CSVs were ingested into the Foundry filesystem.
* **Transformation:** Data was cleaned by renaming columns for clarity and casting data types to ensure integrity (e.g., converting string dates to timestamps).
* **Join:** The two datasets were joined on the `company_id` key to create a single, unified table ready for object mapping.

### b. Data Model (Ontology Manager)
The "brain" of the application was built in the Ontology Manager.
* **Objects:** Two core objects were created: `Company` and `Person`. Each object was mapped to the columns from the clean dataset created in Pipeline Builder.
* **Properties:** Relevant properties were configured for each object (e.g., Company Name, Address; Person Name, Email, Job Title).
* **Links:** A crucial **one-to-many link** was established, defining the relationship that a single `Company` can have many `Person` contacts. This link is the foundation of the application's relational power.
* **Actions:** Two user-facing Actions ("Add New Person", "Log Interaction") were configured to allow write-back capabilities, making the application interactive rather than read-only.

### c. User Interface (Workshop)
The front-end was built as a simple, two-page application in Workshop.
* **Page 1: Company List:** Uses an **Object Table** widget to display all `Company` objects. Clicking on a row is configured to navigate to the detail page, passing the selected `Company` object as a parameter.
* **Page 2: Company Detail View:** Displays the properties of the selected `Company` and uses a second Object Table to show only the `Person` objects linked to that specific company. Buttons on this page trigger the "Add New Person" and "Log Interaction" Actions.

## 6. Potential Next Steps

Given more time, I would expand the application's scope to further empower our user, Alex:
* **Develop a Dashboard:** Create a dedicated dashboard page with more KPIs, such as "Interactions this Month" or "Recently Added Contacts."
* **Implement Advanced Filtering:** Add filtering capabilities to the main company list (e.g., filter by region or size).
* **Create an "Opportunity" Object:** Introduce a new object to track sales deals, linking them to both Companies and Persons to provide a full 360-degree view of the sales pipeline.
* **Refine Action Logic:** Enhance the "Log Interaction" action to include follow-up dates and status updates.
