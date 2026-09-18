# Data model

This document mirrors the current FLEET spreadsheet at a conceptual level.

## Operational entities

### VEHICLES
Master vehicle records and current assignment/state.

### DRIVERS
Driver identities and operational linkage.

### EQUIPMENT
Expected vehicle equipment catalog.

### DRIVER_FOLDER
Driver-folder checklist/reference items.

### VEHICLE_DOCUMENTS
Vehicle document metadata and expiry tracking.

### SERVICE_TYPES
Service/maintenance taxonomy.

### SERVICE_HISTORY
Vehicle maintenance/service events.

### TASKS
Operational assignments and conversational workflows.

### TASK_MESSAGES
Inbound/outbound messaging history related to tasks.

### HANDOVERS
Vehicle acceptance/return inspection sessions.

### HANDOVER_ITEMS
Detailed inspection results.

### PHOTOS
Photo references connected to workflows/entities.

### ISSUES
Detected deficiencies, damage, missing equipment, or other problems.

### ODOMETER_LOG
Immutable odometer observations with provenance.

### REPORT_PDFS
Generated report references.

### AUDIT_LOG
System-level change/activity trail.

### SETTINGS
Runtime configuration.

## ID families

Current records use stable prefixes such as:

- VEH-
- DRV-
- TSK-
- HND-
- ISS-
- ODO-
- MSG-

These IDs should remain organization-neutral.
