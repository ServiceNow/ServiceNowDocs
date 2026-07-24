---
title: Grant audit roles
description: The Audit Admin assigns a Field Service for Audit role to a person or group to enable them to create, view, update, or delete audit tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/fsm-audit-t-grant-roles.html
release: australia
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 1
breadcrumb: [Configure, Retail]
---

# Grant audit roles

The Audit Admin assigns a Field Service for Audit role to a person or group to enable them to create, view, update, or delete audit tasks.

## Before you begin

The Audit Admin performing this task must have role-management access on the ServiceNow instance. Field Service for Audit must be installed.

Identify the correct role before proceeding:

-   Assign `sn_fsm_audit.author` to a workflow or integration that only creates audit tasks.
-   Assign `sn_fsm_audit.auditor` to a field technician or compliance reviewer who reads and updates audit tasks.
-   Assign `sn_fsm_audit.audit_admin` to a privileged administrator who manages the full audit task lifecycle, including deleting records.

## About this task

An Author who also needs to work on existing tasks must be granted `sn_fsm_audit.auditor` in addition to `sn_fsm_audit.author`.

## Procedure

1.  Navigate to **User Administration &gt; Users** to assign a role to an individual, or **User Administration &gt; Groups** to assign a role to a group.

2.  Open the person or group record.

3.  In the **Roles** related list, click **Edit**.

4.  Search for the audit role to assign.

5.  Move the role to the **Roles List** column.

6.  Click **Save**.


## Result

The Auditor, Audit Admin, or Author can perform the operations permitted by the assigned role. Role changes take effect at the recipient's next login.

## What to do next

When custom access rules are active, granting `sn_fsm_audit.auditor` is the first step — but access to a specific task also depends on rules the Audit Admin has configured. See [How access to audit tasks works](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

**Related topics**  


[Roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Components installed with Field Service for Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-reference.md)

