# FLEET architecture

## System role

FLEET is a personal, organization-agnostic fleet and transport operations system.

A concrete company can be a tenant/source/integration context, but must not define the system identity.

## Current data model

The active Google Sheet currently contains these logical tables:

- TASK_MESSAGES
- AUDIT_LOG
- REPORT_PDFS
- SETTINGS
- VEHICLES
- DRIVERS
- EQUIPMENT
- DRIVER_FOLDER
- VEHICLE_DOCUMENTS
- SERVICE_TYPES
- SERVICE_HISTORY
- TASKS
- HANDOVERS
- HANDOVER_ITEMS
- PHOTOS
- ISSUES
- ODOMETER_LOG

## Main workflow

Vehicle / Driver
→ Task
→ Conversation
→ Structured response
→ Handover / Odometer / Issue
→ Audit trail

## Separation of concerns

### Code
Canonical source: GitHub.

### Operational state
Current source: Google Sheets.

### User interaction
Current client: Google Chat.

### Files/photos/reports
Current storage: Google Drive.

## Non-goals

The repository must not contain:

- live driver personal data;
- live task-message payloads;
- raw Google Chat JSON;
- OAuth tokens or API secrets;
- production spreadsheets or exports containing operational data.

## Direction

The runtime should gradually move toward adapters:

- storage adapter
- messaging adapter
- document/file adapter
- organization/tenant configuration
- workflow engine

This keeps the FLEET core independent from any one company or Google product.
