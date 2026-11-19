---
title: Access control
description: When generating or sharing a project, Process Mining honors the access control rules \(ACLs\) for the table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/process-mining/access-control.html
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

When generating a project, Process Mining honors the ACLs on the table that a project reports on, and ignores ACLs on the audit table.

When sharing a project:

-   All visible data in Analyst workbench is visible to any user who has access to the project.
-   All mining operations are performed as per the project creator's \[sys\_created\_by\] access. This includes mining performed by roles with higher permission levels, which can result in less data being mined.

Summary and insights page:

-   KPIs are visible to any user who has the required permission to access related KPIs.
-   Insights are visible to any user who has access to the project.

**Parent Topic:**[Configuring Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/setting-up-process-mining.md)

