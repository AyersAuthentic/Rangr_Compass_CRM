### Notes: Foundry End-to-End Workflow

#### The Core Concept: From Data to Decision

The entire Foundry workflow is designed to transform raw, disconnected data into a fully interactive, operational application. It follows a clear, logical path:

**Raw Data → [Pipeline Builder] → Clean Data → [Ontology Manager] → Modeled World → [Workshop] → Interactive Application**

---

### Key Terminology

* **Project:** A container for all your work—your data, pipelines, and applications.
* **Dataset:** A table of data within Foundry. It can be raw (just uploaded) or clean (the output of a pipeline).
* **Ontology:** The central concept. A digital twin or semantic model of your real-world operations. It's the "brain" of your entire system.
* **Object:** A real-world "noun" that you define in the Ontology (e.g., a `Company`, a `Person`, an `Airport`).
* **Property:** An "adjective" or attribute of an Object (e.g., the `Company` object has a `Name` property and an `Address` property). Properties are mapped to columns in your clean dataset.
* **Link:** A "verb" that defines the relationship between two Objects (e.g., a `Company` *has many* `Persons`).
* **Action:** A user-driven event that modifies data in the Ontology (e.g., *adding* a new person, *updating* a company's status).

---

### The Workflow in Detail

#### 1. Data Ingestion: Getting Data In

* **Tool:** Foundry Data Connection / Project Interface
* **Purpose:** To bring raw data into your project space.
* **Process:** You start by creating or selecting a project. You then upload your raw data files (like `.csv` or `.xlsx`) which become raw **datasets**.
* **Outcome:** Your source data is now inside Foundry, ready to be processed.

#### 2. Data Transformation: Cleaning the Data

* **Tool:** **Pipeline Builder**
* **Purpose:** To take one or more raw datasets and clean, transform, and join them to produce a high-quality, structured output. This is the "T" in ETL.
* **Analogy:** A visual data recipe. You start with ingredients (raw datasets) and apply a series of steps (transforms) to produce a finished dish (a clean dataset).
* **Key Actions:**
    * **Inputs:** Adding your raw datasets to the pipeline graph.
    * **Transforms:** Applying functions like `rename columns`, `cast data types`, `filter rows`, and, most importantly, `join` to combine different datasets.
    * **Outputs:** Defining the clean dataset that your pipeline will produce.
* **Outcome:** A clean, reliable dataset that is ready to be modeled in the Ontology.

#### 3. The Semantic Layer: Modeling the World

* **Tool:** **Ontology Manager**
* **Purpose:** This is the most critical part of the Foundry workflow. You teach Foundry what your data *means* in a real-world context.
* **Process:**
    1.  **Create Object Types:** You define your "nouns" (e.g., create a `Company` object and a `Person` object).
    2.  **Map to Data:** You point each Object Type to a clean dataset from Pipeline Builder.
    3.  **Define Properties:** You map the properties of your object (e.g., `Company Name`) to the specific columns in that dataset.
    4.  **Create Links:** You define the relationships between objects (e.g., create a link from `Company` to `Person` using the `company_id` column that exists in both).
* **Outcome:** A rich, understandable model of your world. Foundry no longer just sees tables; it understands `Companies` that have `Employees`.

#### 4. Application Building: Creating the User Interface

* **Tool:** **Workshop**
* **Purpose:** To build a user-facing web application without writing code, using the Objects from your Ontology as the building blocks.
* **Analogy:** Building with digital Legos.
* **Process:**
    * You add **Widgets** (like an `Object Table`, a `Filter List`, `Charts`, `Buttons`) to a canvas.
    * You configure each widget to be "backed" by the Ontology. For example, you tell the `Object Table` widget to display all of your `Company` objects.
    * You configure interactivity, like making it so that clicking on a company in a table displays its details on the side of the page.
* **Outcome:** A fully functional, interactive web application for end-users.

#### 5. Closing the Loop: Taking Action

* **Tools:** **Ontology Manager** (for configuration) & **Workshop** (for use)
* **Purpose:** To allow users to not just *view* data, but to *change* and *add to* it from the application interface.
* **Process:**
    1.  **Configure in Ontology:** You define an **Action** in the Ontology Manager (e.g., an "Add New Person" action that requires a name, email, and company ID as inputs). You configure the rules for how this action should modify the underlying dataset.
    2.  **Use in Workshop:** You add a `Button` widget to your Workshop application and configure it to trigger the "Add New Person" action, which will pop up a form for the user to fill out.
* **Outcome:** A dynamic, operational application where user decisions can be written back into the system, closing the data-to-decision loop.

---

### Putting It All Together (Your CRM Project)

1.  **Data Ingestion:** You will upload `companies.csv` and `people.csv` as two raw datasets.
2.  **Pipeline Builder:** You will create a pipeline to join these two datasets together into one clean `contacts_master` dataset.
3.  **Ontology Manager:** You will create a `Company` object and a `Person` object, mapping them to the `contacts_master` dataset. Then, you will create a **Link** between them.
4.  **Workshop:** You will build a simple UI that shows a list of all `Company` objects. Clicking a company will show the linked `Person` objects.
5.  **Actions:** You will create an "Add New Person" **Action** so you can add a new contact to a company directly from your Workshop app.


---

# Step by Step Tutorial Walk Through

## Setup

1. Create a tutorial project folder in the main Foundry folder.

## Introduction (Data Ingestion)
1. Upload the `companies.csv` and `people.csv` files to the tutorial project folder.
- Open the target folder for the project
- Click on New
- Click on Upload Files
- Toggle Upload as individual structured datasets

## Transformation





