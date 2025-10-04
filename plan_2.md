# Rangr_Compass_CRM: CRM Project Plan
**Project:** Build a CRM Solution in Palantir Foundry
**Deadline:** Submit by October 16, 2025
**Time Available:** 1-2 hours weekdays, 4-6 hours weekends
**Vacation:** October 17-26 (hard constraint)

---

## Executive Summary

Build **Rangr Contact CRM**, a functional CRM application in Palantir Foundry that enables sales representatives to manage customer relationships. The application will demonstrate ability to translate business needs into working software using Foundry's Pipeline Builder, Ontology, and Workshop components.

### Success Criteria
- ✅ Working data pipeline with company and person datasets
- ✅ Ontology with Company and Person objects and their relationship
- ✅ Workshop UI with list and detail views
- ✅ At least one functional Action (Add Person)
- ✅ Ability to make live edits during demo presentation
- ✅ Complete documentation with screenshots/video

### User Persona
**Meet Alex**, a sales representative at a tech company. Alex needs a simple tool to:
- View all companies and their associated contacts
- Quickly see contact details and interaction history
- Log new contacts and interactions efficiently
- Track relationship status with customers

*Every feature decision should serve Alex's needs.*

---

## Phase 1: Foundation & Learning (Oct 3-6)

### Tonight: Friday, October 3 [1-2 hours]
**Goals:**
- [ ] Complete "Step 01 - Speedrun: Your first E2E Workflow" course **To Do: 1 hour**
- [x] Write user persona (15 minutes) - create persona.md file
- [x] Browse provided company and person datasets
- [x] Decide on project name: **Rangr Compass CRM**
- [x] Set up project folder structure in Foundry

**Outcome:** Foundational understanding of Pipeline Builder, Ontology, and Workshop.

**Notes:**
- Don't aim for perfection on the Speedrun—aim for comprehension
- While browsing datasets, note column names, data types, and quality issues
- Keep persona.md open during entire project as reference

---

### Weekend: Saturday & Sunday, October 4-5 [8-12 hours total]

#### Saturday, October 4 [4-6 hours]
**Goals:**
- [x] Ingest company dataset into your project folder
- [x] Ingest person dataset into your project folder
- [x] Start Pipeline Builder: Create initial transforms
  - [ ] Clean company data (standardize column names, fix data types)
  - [ ] Clean person data (standardize column names, fix data types)
  - [ ] Explore data quality issues (nulls, duplicates)
- [ ] Watch Ontology tutorials (30-45 minutes)
- [ ] Document pipeline with screenshots

**Pipeline Checklist:**
- Rename columns to consistent format (e.g., snake_case or camelCase)
- Handle missing values appropriately
- Ensure key fields for joining are clean (company_id, person_id, etc.)
- Create intermediate datasets as needed

**Outcome:** Clean, prepared datasets ready for ontology mapping.

#### Sunday, October 5 [4-6 hours]
**Goals:**
- [ ] Complete pipeline: Join company and person datasets
- [ ] Open Ontology Manager
- [ ] Create Company Object
  - [ ] Map to clean company dataset
  - [ ] Define key properties (name, industry, status, etc.)
  - [ ] Set primary key
- [ ] Create Person Object
  - [ ] Map to clean person dataset
  - [ ] Define key properties (name, email, phone, role, etc.)
  - [ ] Set primary key
- [ ] Create Link: Company ↔ Person ("has contacts")
- [ ] Test ontology queries to verify relationships
- [ ] Take screenshots of Ontology Manager

**Ontology Checklist:**
- Company object must have: name, id, and at least 2-3 other relevant properties
- Person object must have: name, email, company_id (for linking)
- Link should be bidirectional and properly configured
- Test that you can query "Show me all people for Company X"

**Critical Success Indicator:** By end of Sunday, you should be able to query your ontology and see companies with their related people. If this isn't working, don't move forward—debug it.

**Outcome:** Functioning ontology that represents your data as real-world objects.

---

### Monday, October 6 [1-2 hours]
**Goals:**
- [ ] Create new Workshop application named "ContactHub"
- [ ] Build simplest possible view: Table of all companies
- [ ] Verify you can see company data in Workshop
- [ ] Debug any connection issues between Ontology and Workshop

**Workshop Checklist:**
- Start with pre-built table component
- Display 3-5 key company fields (name, industry, status)
- Make sure data loads—don't worry about styling yet

**Outcome:** You can see your company data in a Workshop UI.

**Notes:**
- If stuck here for more than 90 minutes, this is a red flag
- Reach out for help or review Workshop tutorials
- Don't proceed until you have ONE working view

---

## Phase 2: Core CRM Functionality (Oct 7-10)

### Tuesday, October 7 [1-2 hours]
**Goals:**
- [ ] Add company detail page
- [ ] Implement navigation: clicking a company opens detail view
- [ ] Display company information on detail page
- [ ] Display related people for that company

**UI Checklist:**
- Company list page: table with clickable rows
- Company detail page: company info card + table of related people
- Basic navigation working (click company → see detail)

**Outcome:** Two-page application with basic navigation.

---

### Wednesday, October 8 [1-2 hours]
**Goals:**
- [ ] Return to Ontology Manager
- [ ] Create "Add New Person" Action
  - [ ] Define input fields (name, email, phone, role)
  - [ ] Link new person to a company
  - [ ] Configure write-back to dataset
- [ ] Test Action in Ontology Manager

**Action Checklist:**
- Required fields: name, email, company_id
- Optional fields: phone, role, notes
- Validation: email format, required fields
- Test with sample data before integrating to UI

**Outcome:** Functioning Action that creates new Person records.

---

### Thursday, October 9 [1-2 hours]
**Goals:**
- [ ] Add "Add New Person" button to Workshop UI
- [ ] Test full workflow: click button → fill form → create person → see in list
- [ ] Debug any issues with Action integration
- [ ] **CHECKPOINT:** Review against success criteria

**Checkpoint Questions:**
- Can you view companies? ✅
- Can you see people linked to companies? ✅
- Can you add a new person? ✅
- Is the data flowing correctly through Pipeline → Ontology → Workshop? ✅

**Critical Decision Point:** If all checkpoints pass, proceed to stretch goals. If any fail, spend Friday debugging before moving forward.

**Outcome:** Minimum viable CRM application is complete.

---

### Friday, October 10 [1-2 hours]

#### If Checkpoints Passed (Stretch Goals):
**Goals:**
- [ ] Create "Log Interaction" Action
  - [ ] Fields: person_id, interaction_type (call/email/meeting), date, notes
  - [ ] Link to Person object
- [ ] Add interaction logging button to person detail view
- [ ] Test interaction creation workflow

#### If Checkpoints Failed (Recovery Mode):
**Goals:**
- [ ] Debug core functionality issues
- [ ] Simplify scope if necessary
- [ ] Ensure basic app is working before weekend

**Outcome:** Enhanced CRM with interaction tracking OR stable core CRM.

---

## Phase 3: Documentation & Demo Prep (Oct 11-16)

### Weekend: Saturday & Sunday, October 11-12 [8-12 hours total]

#### Saturday, October 11 [4-6 hours]
**Goals:**
- [ ] Polish Workshop UI
  - [ ] Add clear page titles and descriptions
  - [ ] Ensure button labels are descriptive
  - [ ] Add simple KPI card (e.g., "Total Companies: X")
- [ ] Create demo script (write it out word-for-word)
- [ ] Record 5-minute demo video (first draft)
- [ ] Take final screenshots of all components

**Demo Script Structure (5 minutes):**
1. **Introduction (30 sec):** "I built ContactHub to help sales reps like Alex manage customer relationships..."
2. **Architecture Overview (2 min):** Show Pipeline → Ontology → Workshop flow
3. **Live Demo (2 min):** Navigate UI, demonstrate Add Person Action
4. **Value Proposition (30 sec):** "This enables Alex to quickly access contacts and log interactions..."

**Polish Checklist:**
- All pages have clear titles
- Buttons are clearly labeled ("Add New Contact", not just "Add")
- No lorem ipsum or placeholder text
- Data looks realistic (not test123@test.com)

---

#### Sunday, October 12 [4-6 hours]
**Goals:**
- [ ] Practice live edit scenarios (3-4 hours)
- [ ] Re-record demo video (final version)
- [ ] Create GitHub repository for documentation
- [ ] Start README.md with project overview

**Live Edit Practice Scenarios:**
1. **Add a new property to Person object**
   - Add "Status" field (Lead/Active/Former)
   - Verify it appears in UI
   - Time yourself: should take 3-5 minutes

2. **Add a filter to Workshop view**
   - Filter companies by industry or status
   - Practice explaining your steps out loud

3. **Modify existing Action**
   - Add validation to "Add Person" (e.g., email required)
   - Test the change

4. **Handle a curveball**
   - Practice saying: "I'd approach this by... let me try..."
   - Practice staying calm if something doesn't work

**Practice Goals:**
- Complete each scenario 2-3 times until smooth
- Narrate your thought process out loud
- Know where every menu and button is located

**Outcome:** Confident, polished demo and ability to handle live edits.

---

### Monday-Wednesday, October 13-15 [3-6 hours total]

#### Monday, October 13 [1-2 hours]
**Goals:**
- [ ] Final demo run-through (record yourself)
- [ ] Complete README.md
  - [ ] Project overview
  - [ ] Architecture diagram or description
  - [ ] Key features list
  - [ ] Screenshots embedded
- [ ] Prepare answers to likely questions

**Likely Interview Questions:**
- "Walk me through your data pipeline decisions"
- "Why did you structure the ontology this way?"
- "What would you add if you had more time?"
- "How would you scale this for 10,000 companies?"
- "What was the hardest part of building this?"

**Prepare Answers:**
- Next steps answer: "I would add a dashboard with KPIs, opportunity tracking, and email integration"
- Scaling answer: "I'd add indexing, pagination in Workshop, and data quality validations in pipeline"

---

#### Tuesday, October 14 [1-2 hours]
**Goals:**
- [ ] Practice demo again (aim for smooth 5-minute delivery)
- [ ] Practice one live edit scenario
- [ ] Review Foundry terminology
- [ ] Finalize all documentation

**Terminology to Use Confidently:**
- Pipeline Builder, transforms, datasets
- Ontology Manager, objects, properties, links
- Actions, write-backs
- Workshop, components, pages

**Final Checklist:**
- Demo video saved and uploaded
- GitHub README complete with screenshots/GIF
- All screenshots organized and labeled
- Demo script memorized (or at least outlined)

---

#### Wednesday, October 15 [1-2 hours]
**Goals:**
- [ ] Final polish and review
- [ ] One last demo run-through
- [ ] Prepare submission materials per instructions
- [ ] Get good sleep—tomorrow is submission day

**Pre-Submission Checklist:**
- Application works end-to-end ✅
- Demo video is clear and professional ✅
- Documentation is complete ✅
- You can explain every decision ✅
- You're confident in live edit scenarios ✅

---

### Thursday, October 16 [Morning]
**Goals:**
- [ ] Submit project via Candidate Portal (morning)
- [ ] Send any required follow-up emails
- [ ] Decompress and relax—you've earned it

**Outcome:** Project submitted, vacation mode activated! 🌴

---

## Emergency Contingencies

### If Behind Schedule (Check-in: Oct 9)
**Minimum Viable Product:**
- Company list view only (skip person detail page)
- One working Action: Add Person
- Basic documentation with screenshots
- 3-minute demo instead of 5-minute

**What to Cut:**
1. Interaction logging (nice-to-have)
2. KPI widgets (polish)
3. Advanced filters (stretch goal)

**What Never to Cut:**
1. Working Pipeline + Ontology
2. At least one functional Action
3. Ability to navigate the UI
4. Demo preparation and practice

### If Stuck on Technical Issues
**Resources:**
1. Foundry documentation and tutorials
2. Search for specific error messages
3. Simplify: reduce scope, use simpler approach
4. Focus on showing problem-solving process in demo

**Time Limits per Issue:**
- Don't spend more than 2 hours stuck on one problem
- If blocked for 2+ hours, simplify approach or skip feature
- Document what you tried—show problem-solving in interview

---

## Success Metrics

### Technical Completion
- [ ] Pipeline ingests and transforms both datasets
- [ ] Ontology has 2 objects and 1 link
- [ ] Workshop has working UI with navigation
- [ ] At least 1 Action functions correctly
- [ ] Can demonstrate live editing capability

### Presentation Quality
- [ ] 5-minute demo tells a clear story
- [ ] Demo focuses on business value (Alex's needs)
- [ ] Confident use of Foundry terminology
- [ ] Smooth navigation through application
- [ ] Can make live edits within 3-5 minutes

### Documentation
- [ ] GitHub repository with README
- [ ] Screenshots of Pipeline, Ontology, Workshop
- [ ] Demo video uploaded and working
- [ ] Clear explanation of architecture decisions

---

## Daily Commitment Tracker

Track your actual hours to stay on pace:

| Date | Planned Hours | Actual Hours | Tasks Completed | Notes |
|------|---------------|--------------|-----------------|-------|
| Oct 3 (Fri) | 1-2 | | | |
| Oct 4 (Sat) | 4-6 | | | |
| Oct 5 (Sun) | 4-6 | | | |
| Oct 6 (Mon) | 1-2 | | | |
| Oct 7 (Tue) | 1-2 | | | |
| Oct 8 (Wed) | 1-2 | | | |
| Oct 9 (Thu) | 1-2 | | | |
| Oct 10 (Fri) | 1-2 | | | |
| Oct 11 (Sat) | 4-6 | | | |
| Oct 12 (Sun) | 4-6 | | | |
| Oct 13 (Mon) | 1-2 | | | |
| Oct 14 (Tue) | 1-2 | | | |
| Oct 15 (Wed) | 1-2 | | | |
| Oct 16 (Thu) | 1 | | | |

**Total Planned:** 24-38 hours
**Total Actual:** _____ hours

---

## Key Principles

1. **Build for demonstration, not production** - Your app needs to work well for 5 minutes, not 5 years
2. **Persona-driven decisions** - Every feature should serve Alex's needs
3. **Functional > Beautiful** - Working ugly beats broken pretty
4. **Practice makes confident** - The live edit practice is as important as building the app
5. **Document as you go** - Screenshots at each phase, don't wait until the end
6. **Stay in scope** - Don't let "one more feature" derail your timeline

---

