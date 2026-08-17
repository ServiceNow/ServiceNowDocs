---
title: Field Service for Audit
description: Field Service for Audit is a shared plugin that any product can use to create, assign, and track audit tasks on a common data model and access structure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/fsm-audit-overview.html
release: australia
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Retail Store Audit Operations, Explore, Retail]
---

# Field Service for Audit

Field Service for Audit is a shared plugin that any product can use to create, assign, and track audit tasks on a common data model and access structure.

Field Service for Audit \(`sn_fsm_audit`\) provides the shared infrastructure that Retail Store Audit and other consuming products use to create and manage audit work. It defines a single audit task type, three roles, and a consistent outcome model so audit results are comparable across teams and products.

Field Service for Audit manages the underlying audit task data and access rules. Auditors read, update, and record outcomes on audit tasks. Audit Admins manage and delete audit task records. Authors create audit tasks on behalf of a workflow or process.

**Note:** Field Service for Audit does not include any user experience in current version.

## Audit tasks

An audit task \(`wm_audit_task`\) is a work item that tracks and records the outcome of a single piece of audit work. It inherits standard assignment, scheduling, and lifecycle fields from the platform work-management task type and adds two audit-specific fields.

|Field|Description|Set by|
|-----|-----------|------|
|Result|The Auditor's outcome — Pass or Fail. Empty until the Auditor sets it on completion.|Auditor|
|Task Plan Template Item|Links the audit task to a reusable task template. Visible only when the Task Plan Templates application is installed.|Author or consuming product|

When an audit task is completed or cancelled, all fields become read-only for every role.

## Access

Access to audit tasks is determined by role. Auditors can view and update tasks. Audit Admins can view, update, and delete them. Authors can create tasks but cannot open or edit existing ones.

Consuming products can set up additional access rules to further refine which audit tasks each Auditor can see and fulfill — for example, limiting visibility to tasks linked to cases already assigned to them.

## Roles

|Role|Persona|What this role enables|
|----|-------|----------------------|
|`sn_fsm_audit.author`|Consumer workflow or system actor|Create audit tasks. Access is limited to the creation form — cannot open or edit a task after it is saved.|
|`sn_fsm_audit.auditor`|Auditor or compliance reviewer|Read and update audit tasks. Set the Pass or Fail result on completion. Cannot delete tasks.|
|`sn_fsm_audit.audit_admin`|Privileged administrator|Full lifecycle access — create, read, update, and delete audit tasks.|

**Parent Topic:**[Retail Store Audit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-overview.md)

**Related topics**  


[Retail Store Audit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-overview.md)

[Grant Field Service for Audit roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-t-grant-roles.md)

[Components installed with Field Service for Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-reference.md)

