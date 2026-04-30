---
title: Exploring Auditing
description: Track record changes on auditing-enabled tables. By default, the system tracks changes to the incident, change, and problem tables, among others.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Auditing]
---

# Exploring Auditing

Track record changes on auditing-enabled tables. By default, the system tracks changes to the incident, change, and problem tables, among others.

## Auditing overview

Enabling auditing tracks the creation, update, and deletion of all records in the table. If you want to audit individual fields in a table, you can hide fields you don’t want to track using a dictionary attribute.

Auditing information is kept in the following tables:

-   [Audit](../../security/concept/c_UnderstandingTheSysAuditTable.md#)
-   [Knowing about History sets](../../security/concept/c_HistorySets.md)

**Warning:** Auditing system tables that receive a large amount of traffic, such as workflow Contexts \[wf\_context\] or Event Management Alerts \[em\_alert\], can impact performance. For this reason, you can’t audit the em\_alert table as a whole. Instead, audit selected fields of interest. Set **audit=true** on both the em\_alert table and the selected fields. Try to audit as few fields as possible.

## Auditing users

Auditing has the following users.

-   admin
-   security\_admin

## Auditing benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Enable table auditing to track changes to all or some of the table's fields|[Configuring auditing for a table](../../security/task/t_EnableAuditingForATable.md)|admin|
|Experience a more enhanced way of defining and configuring the audit capability|[Configure auditing using Audit Management Console](../task/audit-mgmt-console.md)|admin|
|Automate and simplify the deletion of audit data|[Setup your audit retention](../task/setup-audit-retention.md)|security\_admin|

## What to explore next

To learn more about using Auditing, see:

-   [Configuring auditing for a table](../../security/task/t_EnableAuditingForATable.md)
-   [Configure auditing using Audit Management Console](../task/audit-mgmt-console.md)
-   [Viewing Sys Audit and Audit Relationship Change tables](../../security/concept/c_UnderstandingTheSysAuditTable.md#)
-   [Knowing about History sets](../../security/concept/c_HistorySets.md)

