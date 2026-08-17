---
title: Grant Field Service for Audit roles
description: The Audit Admin assigns a Field Service for Audit role to a person or group to enable them to create, view, update, or delete audit tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/fsm-audit-t-grant-roles.html
release: australia
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Configure, Retail]
---

# Grant Field Service for Audit roles

The Audit Admin assigns a Field Service for Audit role to a person or group to enable them to create, view, update, or delete audit tasks.

## Before you begin

The Audit Admin performing this task must have role-management access on the ServiceNow instance. Field Service for Audit must be installed.

Identify the correct role before proceeding:

|Assign this role|To|
|----------------|---|
|`sn_fsm_audit.author`|A workflow or integration that creates audit tasks only.|
|`sn_fsm_audit.auditor`|An auditor or compliance reviewer who reads and updates tasks.|
|`sn_fsm_audit.audit_admin`|A privileged administrator who manages the full task lifecycle.|

**Note:** An Author who also needs to work on existing tasks must receive `sn_fsm_audit.auditor` in addition to `sn_fsm_audit.author`.

Role required: `sn_fsm_audit.author`, `sn_fsm_audit.auditor`, or `sn_fsm_audit.audit_admin`.

## Procedure

1.  Navigate to **User Administration &gt; Users** to assign a role to an individual, or **User Administration &gt; Groups** to assign a role to a group.

2.  Open the person or group record.

3.  In the **Roles** related list, click **Edit**.

4.  Search for and select the audit role.

5.  Move the role to the **Roles List** column, then click **Save**.


## Result

The Auditor, Audit Admin, or Author can perform operations allowed by the assigned role. Changes take effect at the recipient's next login.

**Related topics**  


[Field Service for Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-overview.md)

[Components installed with Field Service for Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-reference.md)

