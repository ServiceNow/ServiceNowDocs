---
title: Roles
description: Field Service for Audit defines three roles that map to three personas — Author, Auditor, and Audit Admin — each with a distinct set of permissions on the wm\_audit\_task table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/fsm-audit-roles.html
release: australia
topic_type: concept
last_updated: "2026-07-09"
reading_time_minutes: 2
breadcrumb: [Retail Store Audit Operations, Explore, Retail]
---

# Roles

Field Service for Audit defines three roles that map to three personas — Author, Auditor, and Audit Admin — each with a distinct set of permissions on the `wm_audit_task` table.

## Personas and roles

|Persona|Role|Typical user|Access summary|
|-------|----|------------|--------------|
|Author|`sn_fsm_audit.author`|Workflow actor or system integration|Create audit tasks; read and write fields on a new record during form rendering only \(`isNewRecord()` guard\). Cannot read or edit existing records unless also granted `sn_fsm_audit.auditor`.|
|Auditor|`sn_fsm_audit.auditor`|Field technician, compliance reviewer|Read and write audit tasks. Cannot delete.|
|Audit Admin|`sn_fsm_audit.audit_admin`|Privileged administrator|Full CRUD — create, read, write, and delete audit tasks.|

## Author role detail

The `sn_fsm_audit.author` role is intentionally narrow. It exists to allow workflow actors and system integrations to create audit-task records and render the creation form without being able to read or modify existing records. The read and write ACLs for `sn_fsm_audit.author` include an `isNewRecord()` guard, so access applies only while the record has not yet been saved.

To read or edit an existing audit task, an Author must also hold `sn_fsm_audit.auditor` or `sn_fsm_audit.audit_admin`.

## Non-personas

The following are explicitly not supported by this app's roles or ACLs:

-   **Cross-consumer auditor** — a single user auditing across multiple consuming apps in the same instance. Not supported by design.
-   **Consumer-specific personas** \(assigner, fulfiller, consumer manager\) — these roles belong to consuming apps and are never referenced from this app's ACLs.

## Role assignment

Roles are assigned to users or groups through standard ServiceNow role-management tools. Consuming apps may also grant their own users the audit roles as part of their own installation process.

**Parent Topic:**[Retail Store Audit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-overview.md)

**Related topics**  


[Access control framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-access-control.md)

[Grant audit roles to users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-t-grant-roles.md)

[Components installed with Field Service for Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-reference.md)

