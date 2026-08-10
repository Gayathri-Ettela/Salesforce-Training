# Sprint 9 – Lightning Web Components (LWC)

## Overview

Sprint 9 focuses on building interactive user interfaces using **Lightning Web Components (LWC)** in Salesforce.

In this sprint, the Placement Management System is connected to a user interface so that students can view eligible jobs and apply for them.

## Objectives

* Understand the basics of LWC.
* Create an Eligible Jobs component.
* Display Salesforce data in LWC.
* Handle user events.
* Call Apex imperatively.
* Build the Apply workflow.
* Handle success, failure, and loading states.
* Prevent duplicate applications.
* Understand parent-child component communication.
* Refresh the UI after data changes.

## Architecture

```text
Student
   ↓
Lightning Web Component
   ↓
Apex Controller
   ↓
Application Service
   ↓
Salesforce Database
```

## Main Components

### Eligible Jobs

Displays jobs for which the student is eligible.

### Job Card

Displays individual job information and provides the Apply button.

## Apply Workflow

```text
Student clicks Apply
        ↓
LWC Event Handler
        ↓
Imperative Apex
        ↓
Application Service
        ↓
Eligibility Validation
        ↓
Duplicate Check
        ↓
Application Created
        ↓
UI Updated
```

## Important Concepts

* LWC
* Data Binding
* Events
* Wire Service
* Lightning Data Service
* Imperative Apex
* Parent-to-Child Communication
* Child-to-Parent Communication
* Custom Events
* Loading and Error Handling
* UI Refresh

## Project Structure

```text
Sprint-09-LWC/
│
├── README.md
├── architecture/
├── force-app/
├── screenshots/
└── learning-notes/
```

## Key Learning

The main principle learned in this sprint is:

> **The UI requests. The business layer decides.**

Business rules should remain in the Apex/service layer instead of being duplicated inside JavaScript.

## Outcome

By the end of Sprint 9, the Placement Management System provides a user-friendly interface where students can view eligible jobs and submit applications through Salesforce LWC.
