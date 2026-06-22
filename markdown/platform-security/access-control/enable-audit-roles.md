---
title: Enable role auditing with Contextual Security: Role Management V2
description: Set a system property to enable the Audit Roles table to create audit records related to user roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/access-control/enable-audit-roles.html
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 1
breadcrumb: [Contextual Security Manager, Access Control List Rules, Access Management]
---

# Enable role auditing with Contextual Security: Role Management V2

Set a system property to enable the Audit Roles table to create audit records related to user roles.

## Before you begin

Role required: admin

## About this task

When enabled, the Audit Roles \[sys\_audit\_role\] table maintains changes to user records. For more information about role audits, see [Audit user roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/audit-user-roles.md). If the Contextual Security: Role Management V2 \[com.glide.role\_management.inh\_count\] plugin is installed, you must set a system property to **true** to enable role auditing.

## Procedure

1.  Navigate to the System Properties \[sys\_properties\] table.

2.  Add the **glide.role\_management.v2.audit\_roles** system property and set it to **true**.

    If the Contextual Security: Role Management V2 \[com.glide.role\_management.inh\_count\] plugin is installed, setting this property to **true** enables the Audit Roles \[sys\_audit\_role\] table to create records when user roles change. The table records role changes that occur after the property is set. Existing role assignments are not backfilled.


