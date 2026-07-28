---
title: Components installed with Field Service for Audit
description: Several types of components such as tables, user roles, script includes, and access control rules are installed when the Field Service for Audit plugin is activated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/fsm-audit-reference.html
release: australia
topic_type: reference
last_updated: "2026-07-28"
reading_time_minutes: 1
breadcrumb: [Components installed with plugins, Reference, Retail]
---

# Components installed with Field Service for Audit

Several types of components such as tables, user roles, script includes, and access control rules are installed when the Field Service for Audit plugin is activated.

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
|sn\_fsm\_audit.author|Allows Authors to create audit tasks. Limited to the creation form — cannot read or edit existing records unless `sn_fsm_audit.auditor` is also granted.|
|sn\_fsm\_audit.auditor|Allows Auditors to read and update audit tasks and record the Pass or Fail result. Cannot delete tasks.|
|sn\_fsm\_audit.audit\_admin|Allows Audit Admins to create, read, update, and delete audit tasks. Includes access to configure custom access rules.|

**Parent Topic:**[Components installed with plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-components-installed-with-plugins.md)

**Related topics**  


[Roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Custom access rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Grant audit roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-t-grant-roles.md)

