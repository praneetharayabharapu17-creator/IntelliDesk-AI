# IntelliDesk AI — Architecture

## Overview

IntelliDesk AI is built on Salesforce using custom objects, Flow automation, Agentforce, reports, and dashboards.

## Data Model

```text
Employee
   │
   └──────────────► Department

Helpdesk Ticket
   │
   ├──────────────► Employee
   │
   └──────────────► Department
```

## Core Components

### Employee

Stores employee information used for helpdesk ticket management.

### Department

Stores organizational department information and supports technician assignment.

### Helpdesk Ticket

Central object for managing IT support requests.

Important fields include:

* Ticket Number
* Issue Title
* Description
* Category
* Priority
* Status
* Employee
* Department
* Assigned Technician
* Resolution Date

## Automation Architecture

```text
Ticket Creation
      │
      ▼
Employee / Department Association
      │
      ▼
Technician Assignment
      │
      ▼
Priority-Based Automation
      │
      ▼
Ticket Resolution
      │
      ▼
Resolution Date
      │
      ▼
Email Notification
```

## Agentforce Architecture

```text
User
  │
  ▼
Agentforce — IntelliDesk AI
  │
  ├── Create Helpdesk Ticket
  ├── Query Ticket
  ├── Update Ticket
  └── Troubleshooting Assistance
  │
  ▼
Salesforce Helpdesk Ticket Data
```

## Reporting Layer

Salesforce Reports analyze:

* Ticket Status
* Ticket Priority
* Ticket Category
* Department
* Technician Assignment
* Resolution

These reports feed the IntelliDesk AI dashboard for operational monitoring.

## Technology

* Salesforce Lightning
* Salesforce Custom Objects
* Salesforce Flow
* Agentforce
* Salesforce Reports
* Salesforce Dashboards
* Lightning App Builder
