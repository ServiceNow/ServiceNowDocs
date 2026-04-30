---
title: Access control
description: When generating or sharing a project, Process Mining honors the access control rules \(ACLs\) for the table.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Process Mining, Process Mining, Platform Analytics]
---

# Access control

When generating or sharing a project, Process Mining honors the access control rules \(ACLs\) for the table.

When generating a project, Process Mining honors the ACLs on the table that a project reports on, and ignores ACLs on the audit table. Users with the promin\_viewer role have read-only access.

When sharing a project:

-   All visible data in Analyst workbench is visible to any user who has access to the project.
-   All mining operations are performed as per the project creator's \[sys\_created\_by\] access. This includes mining performed by roles with higher permission levels, which can result in less data being mined.

Summary and insights page:

-   KPIs are visible to any user who has the required permission to access related KPIs.
-   Insights are visible to any user who has access to the project.

**Parent Topic:**[Configuring Process Mining](setting-up-process-mining.md)

