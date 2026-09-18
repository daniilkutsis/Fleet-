# FLEET

Personal fleet-management and transport-operations system.

## Purpose

FLEET is a personal system for managing vehicles, drivers, handovers, issues, odometer history, service history, documents, tasks, and conversational workflows.

The current runtime is built around Google Sheets and Google Chat, but those are implementation details rather than the product identity.

## Current architecture

- **Google Sheets** — operational data/state store
- **Google Chat** — conversational driver/operator interface
- **Apps Script** — workflow/orchestration layer
- **GitHub** — source of truth for code and architecture

## Core entities

- Vehicles
- Drivers
- Equipment
- Vehicle documents
- Service types/history
- Tasks
- Handovers
- Handover items
- Photos
- Issues
- Odometer log
- Task messages
- Audit log
- Report PDFs
- Settings

## Design principles

1. FLEET is organization-agnostic.
2. Company names and customer-specific branding must not be hard-coded into core logic.
3. Operational data and secrets do not belong in Git.
4. Conversational interfaces are clients; structured state remains authoritative.
5. Critical real-world actions should remain human-confirmed until explicitly automated.

## Status

Initial baseline repository created from the currently deployed FLEET system.

Next step: export the full Apps Script project into this repository and make GitHub the canonical code source.
