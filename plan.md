# Rangr Compass CRM: Project Plan

**Project:** Rangr Compass CRM
**Timeline:** October 3, 2025 - October 16, 2025
**Objective:** To design, build, and present a functional CRM prototype in Palantir Foundry that effectively solves a core business need, culminating in a successful work sample presentation.

---

## 1. Guiding Principles & Strategy

This project will be executed with a "consultant mindset." The primary goal is not just to demonstrate technical skills but to show the ability to translate a business need into a valuable tool.

* **User Persona:** All features will be built to serve "Alex," a sales representative who needs a simple, clear tool to view customer relationships and log interactions.
* **Prioritization:** We will ruthlessly prioritize features to ensure a robust, functional MVP is completed well before the deadline.
* **Focus:** The emphasis is on functionality (Ontology, Links, Actions) and a clear narrative over complex, cosmetic UI features. The live-edit portion of the demo is the most critical component to practice.

---

## 2. Scope Definition (The "Sweet Spot")

To avoid over-engineering, the project scope is defined in tiers. We will not move to the next tier until the current one is 100% complete.

### ✅ Must-Haves (Core Deliverables)
* [ ] Functioning Data Pipeline (Ingest, Clean, Join)
* [ ] Ontology with `Company` and `Person` objects
* [ ] A `one-to-many` link between `Company` and `Person`
* [ ] A two-page Workshop app (Company List -> Company Detail)
* [ ] **Action #1:** "Add New Person" linked to a company
* [ ] **Action #2:** "Log an Interaction" for a person

### ⭐ Should-Haves (If time permits)
* [ ] A simple KPI card on the main page (e.g., "Total Contacts")
* [ ] Basic filtering on the company list view

### ❌ Out of Scope (Common Time Traps to Avoid)
* Complex multi-page dashboards or visualizations
* Additional object types (e.g., Opportunities, Deals)
* Authentication, permissions, or user-specific views

---

## 3. Detailed Execution Plan

### Phase 1: Foundation & Core Logic (Oct 3 - Oct 6)
*The goal of this phase is to build the entire backend data model. By the end of Monday, the "brain" of the application will be complete and ready to be connected to a user interface.*

#### **Tonight (Friday, Oct 3)**
- [ ] **Task:** Complete the "Step 01 - Speedrun: Your first E2E Workflow" course. **To Do: 1 hour**
- [x] **Task:** Open the provided datasets and familiarize yourself with the columns and data types.
- [x] **Task:** Solidify the "Alex" user persona: write down 2-3 specific tasks Alex needs to accomplish.
- **Deliverable:** Foundational knowledge of the Foundry workflow.

#### **This Weekend (Saturday, Oct 4 & Sunday, Oct 5)**
- [ ] **Task:** **WORK IN PARALLEL.** Begin ingesting the data in **Pipeline Builder**. As soon as you have a preliminary output, switch to the **Ontology Manager** to start creating the `Company` and `Person` objects.
- [ ] **Task:** Iterate between the two tools. Clean a column in the pipeline, then map it as a property in the Ontology. Create the join in the pipeline, then configure the `Company`↔`Person` link in the Ontology.
- [ ] **Task:** By Sunday evening, ensure the Ontology is fully configured with objects, properties, and a functional link.
- **Deliverable:** A clean data pipeline feeding a fully configured, linked Ontology.

#### **Monday, Oct 6**
- [ ] **Task:** Create a new **Workshop** application.
- [ ] **Task:** Add a single page with one **Object Table** widget.
- [ ] **Task:** Configure the table to display the `Company` objects from your Ontology.
- **Deliverable:** A working Workshop page that successfully reads and displays data, validating that the entire backend is functioning correctly.

---

### Phase 2: Application Build & Functionality (Oct 7 - Oct 10)
*The goal of this phase is to build the "Must-Have" user-facing features and begin documenting the process.*

#### **Tuesday, Oct 7 & Wednesday, Oct 8**
- [ ] **Task:** Build out the two-page UI in Workshop: a main page with the company list and a detail page.
- [ ] **Task:** Configure the navigation so that clicking a company on the main page takes you to its detail page.
- [ ] **Task:** On the detail page, display the selected company's properties and a table of its linked `Person` objects.
- [ ] **Task:** Go back to the **Ontology Manager** and build **Action #1: "Add New Person."**
- [ ] **Task:** Add a button to the UI to trigger this action. Test it thoroughly.
- **Deliverable:** A navigable two-page app with the ability to add new contacts.

#### **Thursday, Oct 9 & Friday, Oct 10**
- [ ] **Task:** Build **Action #2: "Log an Interaction."** This should allow the user to select a person and add a note.
- [ ] **Task:** Add a button for this action and test it.
- [ ] **Task:** **Begin documentation.** Start taking clear screenshots of your Pipeline, Ontology configuration (especially the link), and Workshop pages.
- [ ] **Task:** Create your GitHub repository and draft the initial `README.md` with the project description.
- **Deliverable:** A feature-complete MVP that meets all "Must-Have" requirements. Initial documentation started.

---

### Phase 3: Polish, Practice & Submission (Oct 11 - Oct 16)
*The goal of this final phase is to polish the application, prepare for the presentation, and master the live-edit scenarios.*

#### **Final Weekend (Saturday, Oct 11 & Sunday, Oct 12)**
- [ ] **Task (Sat):** Add one "Should-Have" feature, like the KPI card. Add clear titles and descriptions in the UI.
- [ ] **Task (Sat):** Write and refine the script for your 5-minute presentation.
- [ ] **Task (Sat):** Do a screen recording of a walkthrough of the finished app.
- [ ] **Task (Sun):** **PRACTICE LIVE EDITS.** Spend the majority of your time on this. Work through the scenarios below, narrating your steps out loud.
- **Deliverable:** A polished application, a final presentation script, and confidence in making live modifications.

#### **Final Days (Monday, Oct 13 - Wednesday, Oct 15)**
- [ ] **Task:** Do one full run-through of your 5-minute demo each night.
- [ ] **Task:** Do one live-edit practice scenario each night.
- [ ] **Task:** Finalize your `README.md` file on GitHub. Create a GIF from your screen recording and embed it.
- **Deliverable:** A fully rehearsed presentation and a complete project portfolio artifact.

#### **Submission Day (Thursday, Oct 16)**
- [ ] **Task:** Do one final review of the project and submission instructions.
- [ ] **Task:** Submit the project for review.
- [ ] **Task:** Log off and prepare for your well-deserved vacation.

---

### Live Edit Practice Scenarios

Practice these until you can do them smoothly while explaining your steps.

1.  **Add a Property:** "Can you add a 'Status' property (e.g., 'Active', 'Lead') to the Person object and have it appear in the details table?"
2.  **Add a Filter:** "Could you add a dropdown filter to the main page to show only companies in a specific state?"
3.  **Modify the UI based on Data:** "Can you make it so that any person with the 'Lead' status appears in yellow in the contacts table?"
4.  **Change a Calculation (if applicable):** "If you had a KPI, could you change it from 'Total Contacts' to 'Average Contacts per Company'?"
