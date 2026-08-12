# Sprint 10 - LWC Architecture and Component Communication

## Overview

This sprint focuses on building Lightning Web Components (LWCs) that work together as a complete application. The project demonstrates component communication, reusable component design, form handling, Lightning Data Service (LDS), and reactive data updates.

---

## Features Implemented

- Parent to Child Communication using @api
- Child to Parent Communication using Custom Events
- Student Profile Form
- Lightning Data Service (LDS)
- Client-side Validation
- Server-side Validation
- Reactive Data Updates
- Reusable Components
- Loading, Success, Empty and Error States

---

## Component Structure

StudentPortal
│
├── StudentSummary
├── StudentProfile
├── EligibleJobs
│ ├── JobCard
│ └── EmptyState
├── MyApplications
│ ├── ApplicationCard
│ └── EmptyState
└── OfferSummary
└── StatusBadge

---

## Communication Flow

### Parent → Child

Uses @api properties.

Example:

```javascript
@api job;
```

### Child → Parent

Uses Custom Events.

```javascript
this.dispatchEvent(
    new CustomEvent('viewdetails')
);
```

---

## Validation Strategy

### Client Side

- Required Fields
- Email Validation
- CGPA Validation

### Server Side

- Business Rules
- Data Integrity
- Eligibility Checks

---

## Reusable Components

### StatusBadge

Displays application, interview, and offer status.

### EmptyState

Displays meaningful messages when no data exists.

---

## Technologies Used

- Salesforce Lightning Web Components (LWC)
- Apex
- Lightning Data Service (LDS)
- SOQL
- Salesforce Platform

---

## Key Learnings

- Component Communication
- Data Ownership
- Reactive Data
- Reusability
- Application Architecture
- Enterprise UI Design

---

## Author

Gayathri Ettela

Salesforce Developer Bridge Program
