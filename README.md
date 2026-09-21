# IntelliDesk AI

## AI-Powered Employee Helpdesk using Salesforce + Agentforce

IntelliDesk AI is an AI-powered employee IT helpdesk built on Salesforce. The project combines Salesforce custom objects, Flow automation, Agentforce AI, reports, and dashboards to streamline employee IT support.

## Problem Statement

Employees often need a simple way to report IT issues, track their tickets, and receive support. IT teams need an organized system to manage tickets, assign technicians, monitor priorities, and track resolutions.

IntelliDesk AI provides a centralized Salesforce-based solution for managing the complete helpdesk workflow.

## Solution

The application allows employees and IT teams to:

* Create and manage helpdesk tickets
* Automatically associate employees with departments
* Automatically assign technicians
* Prioritize critical issues
* Track ticket status
* Record ticket resolution details
* Send resolution notifications
* Use Agentforce AI for ticket creation, retrieval, updates, and troubleshooting assistance
* Monitor helpdesk activity through reports and dashboards

## Key Features

### Salesforce Data Model

The application uses three main custom objects:

* Employee
* Department
* Helpdesk Ticket

Relationships:

```text
Employee
   │
   └── Department

Helpdesk Ticket
   ├── Employee
   └── Department
```

## Helpdesk Ticket Management

Each ticket contains information such as:

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

## Automation & Flows

Salesforce Flow automation handles major parts of the helpdesk lifecycle.

### Priority Automation

Critical-priority tickets automatically move from Open to In Progress.

### Department Automation

The department is automatically associated with the employee when applicable.

### Technician Assignment

Tickets are automatically assigned to the appropriate technician based on department.

### Resolution Automation

When a ticket is resolved, the resolution date is recorded and an email notification is sent to the employee.

## Agentforce AI

IntelliDesk AI integrates Salesforce Agentforce to provide an AI-powered helpdesk assistant.

The Agentforce assistant can:

* Create helpdesk tickets
* Retrieve ticket information
* Update existing tickets
* Provide troubleshooting assistance
* Return ticket numbers after successful ticket creation

This allows users to interact with the helpdesk using natural language instead of manually navigating multiple Salesforce screens.

## Reports

The project includes reports for:

* Open Helpdesk Tickets
* Ticket Status
* Ticket Priority
* Ticket Category and Department
* Technician Assignment and Resolution

## Dashboard

The IntelliDesk AI dashboard provides visual monitoring of:

* Tickets by Status
* Tickets by Priority
* Tickets by Category
* Tickets by Technician

## Technology Stack

* Salesforce
* Salesforce Flow
* Agentforce
* Salesforce Reports
* Salesforce Dashboards
* Lightning App Builder

## Project Architecture

```text
Employee
    │
    ▼
Department
    │
    ▼
Helpdesk Ticket
    │
    ├── Department Auto-Fill
    │
    ├── Technician Assignment
    │
    ├── Priority Automation
    │
    ├── Resolution Tracking
    │
    └── Email Notification

Agentforce
    │
    ├── Create Ticket
    ├── Query Ticket
    ├── Update Ticket
    └── Troubleshooting Assistance
```

## Testing

The application was tested using multiple helpdesk tickets covering different:

* Employees
* Departments
* Categories
* Priorities
* Status values

Agentforce ticket creation was also tested using Salesforce Employee and Department record IDs.

## Screenshots

### Home Page

![IntelliDesk Home](screenshots/INTELLIDESK_HOME.png)

### Employee Record

![Employee Record](screenshots/EMPLOYEE_RECORD.png)

### Department Record

![Department Record](screenshots/DEPARTMENT_RECORD.png)

### Helpdesk Ticket

![Helpdesk Ticket](screenshots/HELPDESK_TICKET_RECORD.png)

### Flows

![Flows](screenshots/FLOWS_INTELLIDESKAI.png)

### Agentforce

![Agentforce](screenshots/INTELLIDESK_AGENT.png)

### Agentforce Conversation

![Agentforce Conversation](screenshots/AGENT_SUMMARY.png)

## Future Enhancements

* Knowledge-base integration
* AI-powered ticket classification
* Automatic suggested resolutions
* SLA monitoring
* Escalation automation
* Advanced service analytics

## Project Status

**Completed**

Built as part of the PwC Launchpad Salesforce learning and project experience.
