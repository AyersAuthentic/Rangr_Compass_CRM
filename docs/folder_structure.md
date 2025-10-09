## Foundry Project Folder Structure

```
/Rangr Data Applicant Projects/
└── [your-username]/
    └── Rangr_Compass_CRM/
        ├── 01_raw_data/
        │   ├── companies_raw
        │   └── people_raw
        │
        ├── 02_cleaned_data/
        │   ├── companies_cleaned
        │   └── people_cleaned
        │
        ├── 03_integrated_data/
        │   └── companies_with_contacts
        │
        └── 04_ontology_ready/
            ├── company_final
            └── person_final
```

## Why This Structure Works

### 📁 **Clear Data Lineage**
Each folder represents a stage in your pipeline:
- `01_raw_data` → Shows you started with source data
- `02_cleaned_data` → Shows transformation logic
- `03_integrated_data` → Shows joining/enrichment
- `04_ontology_ready` → Final datasets mapped to ontology

### 🎯 **Easy to Navigate During Demo**
When they ask "show me your pipeline," you can say:
> "I organized the data flow in four stages: raw ingestion, cleaning, integration, and ontology-ready outputs. Let me walk you through..."

### 🔧 **Easy for Live Edits**
If they ask you to modify something, you know exactly where to find each dataset.

## Alternative: Simpler Structure (If Time Is Tight)

If you want to keep it simpler:

```
/Rangr Data Applicant Projects/
└── [your-username]/
    └── Rangr_Compass_CRM/
        ├── raw/
        │   ├── companies_raw
        │   └── people_raw
        │
        ├── processed/
        │   ├── companies_cleaned
        │   ├── people_cleaned
        │   └── companies_people_joined
        │
        └── final/
            ├── company_dataset
            └── person_dataset
```

## What Goes Where

### **01_raw_data / raw/**
- Direct CSV imports, untouched
- No transformations yet
- Purpose: "This is what I received"

### **02_cleaned_data / processed/**
- Column renaming (Company_Name → company_name)
- Data type fixes
- Null handling
- String cleaning (trim whitespace, lowercase for joining)

### **03_integrated_data / processed/**
- Joined datasets
- Calculated fields (e.g., contact_count per company)
- Enrichment

### **04_ontology_ready / final/**
- Final datasets that map to ontology objects
- Clean, validated, ready for Workshop
- These are what your Company and Person objects point to

## Naming Conventions

### ✅ **Good Names:**
- `companies_raw`
- `companies_cleaned`
- `companies_with_contact_count`
- `people_cleaned`
- `company_person_joined`

### ❌ **Avoid:**
- `dataset1`, `dataset2` (not descriptive)
- `final_final_v2` (shows iteration confusion)
- `test_data` (doesn't belong in production demo)

## Pipeline Builder Organization

Within Pipeline Builder, your transform nodes should follow this flow:

```
[Import companies_raw]
    ↓
[Clean: Rename columns, trim whitespace]
    ↓
[Save: companies_cleaned]
    ↓
[Import people_raw]
    ↓
[Clean: Rename columns, standardize]
    ↓
[Save: people_cleaned]
    ↓
[Join: companies_cleaned + people_cleaned]
    ↓
[Enrich: Add contact_count, etc.]
    ↓
[Split or Save]
    ↓
[Save: company_dataset] [Save: person_dataset]
```

## Tips for Foundry Folders

### 1. **Use Descriptive Dataset Names**
The dataset name will show up in your ontology mapping, so make it clear:
- Not: `data1`
- Yes: `company_dataset_for_ontology`

### 2. **Keep Intermediate Datasets**
Don't delete your intermediate cleaning steps. During the demo, you can show:
> "Here's the raw data with issues... and here's after cleaning... and here's the final joined dataset"

### 3. **Document in Dataset Descriptions**
Foundry lets you add descriptions to datasets. Use them!
- `companies_raw`: "Raw company data, 100 rows, 5 columns"
- `companies_cleaned`: "Cleaned company names, standardized columns"

### 4. **One Project Folder, Everything Inside**
Keep all your CRM work under `Rangr_Compass_CRM/`. Don't scatter datasets across multiple folders.

## What Your Folder Structure Shows

### **Organized Structure = Professional Approach**
✅ "I think systematically about data flow"
✅ "I make it easy for others to understand my work"
✅ "I build for maintainability"

### **Messy Structure = Amateur Approach**
❌ Random dataset names
❌ No clear progression
❌ Hard to explain during demo

## For Tomorrow (Saturday)

**Start with this minimal structure:**

```
Rangr_Compass_CRM/
├── raw/
│   ├── companies_raw
│   └── people_raw
└── final/
    ├── company_dataset
    └── person_dataset
```

**As you build, if you create intermediate datasets, organize them into:**
```
Rangr_Compass_CRM/
├── raw/
├── cleaned/        ← Add this if you create cleaning steps
└── final/
```

Don't over-engineer the structure tomorrow. **Get something working first**, then organize.

## During Your Demo

**When showing your pipeline:**
> "I organized my project into logical stages. Starting with raw data here, I applied transformations to clean and standardize column names, then created these final datasets that feed into my ontology..."

**This takes 15 seconds but shows professionalism.**

## Bottom Line

**Recommendation for You:**
Use the **simple 3-folder structure** (raw / processed / final) to start. It's:
- Clear enough to be professional
- Simple enough to build quickly
- Easy enough to explain

You can always add more organization later if needed.

