# CONTEXT.md — EduConsultPro Salesforce CRM AI Agent Context

## 1. System Overview
**EduConsultPro** is an enterprise Salesforce CRM solution engineered by **Milan Tiwari** (Certified Salesforce Developer & AWS Cloud Practitioner). It optimizes student admissions, lead nurturing, academic course management, and case resolution for higher education institutions.

- **Repository**: [Milan727/Salesforce-CRM-for-Institutions-Project](https://github.com/Milan727/Salesforce-CRM-for-Institutions-Project)
- **Live Video Demonstration**: [YouTube Walkthrough](https://www.youtube.com/watch?v=Uvf3iYnB0dI&t=1s)
- **Primary Tech Stack**: Salesforce Platform, Apex (Triggers, Controllers, Batchable), Lightning Web Components (LWC), Visualforce, SOQL/SOSL, Flow Builder, Security Controls (OWD, Profiles, Sharing Rules).

---

## 2. Developer Credentials
- **Author**: Milan Tiwari (Software & AI-Agentic Engineer)
- **Certification**: Certified Salesforce Developer
- **GitHub**: [@Milan727](https://github.com/Milan727)

---

## 3. Directory & File Map
```
/
├── salesforce project.pdf                 # Complete architectural specification, ERD & security matrix
├── Salesforce Project Demo Video Link.md # Direct link to YouTube demonstration video
├── README.md                              # Public GitHub repository overview
├── ARCHITECTURE.md                        # Custom Object ERD, Apex architecture & security model
├── PROJECT.md                             # Technical functional domains & project specifications
└── CONTEXT.md                             # You are here! AI Agent Context
```

---

## 4. AI Agent Guidelines & Rules
When analyzing or extending this Salesforce CRM repository:

1. **Object & Data Model Compliance**:
   - Custom Objects use `__c` notation (e.g., `Student_Application__c`, `Course__c`, `Counselor_Note__c`).
   - Relationships MUST enforce Master-Detail for cascade deletion where children depend on parent lifecycle, or Lookup for optional association.

2. **Apex & Trigger Design Principles**:
   - All Apex Logic MUST strictly follow One Trigger Per Object and bulkified handler patterns (`Trigger.new`, `Trigger.oldMap`).
   - SOQL queries and DML statements MUST NEVER be placed inside `for` loops.

3. **Security & Data Sharing Rules**:
   - Maintain OWD (Org-Wide Defaults) as Private for student records.
   - Access MUST be granted explicitly via Role Hierarchy, Criteria-Based Sharing Rules, or Apex Managed Sharing.

4. **LWC Component Standards**:
   - LWCs MUST use standard `@wire` adapters for reactive data fetching and Lightning Data Service (LDS) where possible.
