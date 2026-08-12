# Sprint 11 - Salesforce APIs and External Integrations

## Overview

This sprint focuses on integrating Salesforce with external systems using REST APIs, Apex Callouts, Named Credentials, and Queueable Apex.

The project simulates a recruitment integration where selected candidates are automatically synchronized with an external recruitment platform.

---

## Business Problem

Recruiting companies use external recruitment systems.

When a student is selected, Salesforce must automatically send candidate information to the company's recruitment platform.

---

## Architecture

Application Selected
        ↓
Trigger
        ↓
Service Layer
        ↓
Queueable Apex
        ↓
Named Credential
        ↓
REST API
        ↓
External Recruitment System

---

## Features Implemented

- REST API Integration
- Apex HTTP Callouts
- Queueable Apex
- Named Credentials
- JSON Request Processing
- Integration Status Tracking
- Retry Strategy
- Error Handling
- Idempotency Design

---

## API Contract

### Endpoint

POST /candidates

### Method

POST

### Request JSON

```json
{
  "studentId":"STU10045",
  "name":"Ananya",
  "email":"ananya@example.com",
  "branch":"CSE",
  "cgpa":8.4
}
```

### Success Response

```json
{
  "status":"Success",
  "candidateId":"EXT1001"
}
```

---

## Error Handling

Handled Status Codes:

- 400 Bad Request
- 401 Unauthorized
- 403 Forbidden
- 500 Internal Server Error

---

## Authentication

Authentication is managed using Salesforce Named Credentials.

No credentials are hard-coded inside Apex code.

---

## Retry Strategy

If synchronization fails:

Pending
↓
Retry Required
↓
Queueable Retry
↓
Success

---

## Idempotency Strategy

Duplicate submissions are prevented using:

- Application Id
- External Reference Id
- Integration Status Tracking

---

## Technologies Used

- Salesforce
- Apex
- Queueable Apex
- REST APIs
- JSON
- Named Credentials
- Salesforce Connect

---

## Key Learnings

- Salesforce Integrations
- API Contracts
- HTTP Methods
- JSON Processing
- Secure Authentication
- Integration Reliability
- Error Handling
- Idempotency

---

## Author

Gayathri Ettela

Salesforce Developer Bridge Program
