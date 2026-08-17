---
title: Components installed with Field Service for Audit
description: Reference information for the plugin dependencies, roles, and tables installed with the Field Service for Audit plugin.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/fsm-audit-reference.html
release: australia
topic_type: reference
last_updated: "2026-07-07"
reading_time_minutes: 1
keywords: [Field Service for Audit, sn\_fsm\_audit, audit roles, wm\_audit\_task]
breadcrumb: [Components installed with plugins, Reference, Retail]
---

# Components installed with Field Service for Audit

Reference information for the plugin dependencies, roles, and tables installed with the Field Service for Audit plugin.

## Plugin dependencies

<table id="table_a3t_sxr_1cc"><thead><tr><th>

Plugin Name

</th><th>

Description

</th><th>

Plugin Dependencies

</th></tr></thead><tbody><tr><td>

Field Service for Audit

 \[sn\_fsm\_audit\]

</td><td>

Field Service for Audit enables field service teams to plan, execute, and track audit activities as part of field service management workflows.

</td><td>

com.snc.work\_management

</td></tr></tbody>
</table>## Roles

|Role|Description|
|----|-----------|
|`sn_fsm_audit.author`|Allows Authors to create audit tasks. Limited to the creation form — cannot read or edit existing records unless `sn_fsm_audit.auditor` is also granted.|
|`sn_fsm_audit.auditor`|Allows Auditors to read and update audit tasks and record the Pass or Fail result. Cannot delete tasks.|
|`sn_fsm_audit.audit_admin`|Allows Audit Admins to create, read, update, and delete audit tasks. Access to specific tasks may be further refined by custom access rules set up by the consuming product.|

## Tables

|Display name|sys\_name|Extends|
|------------|---------|-------|
|Audit Task|`wm_audit_task`|`wm_task`|

**Parent Topic:**[Components installed with plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-components-installed-with-plugins.md)

**Related topics**  


[Field Service for Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-overview.md)

[Components installed with Store Audit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-reference.md)

