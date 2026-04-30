---
title: Domain separation for Emergency Self Report
description: The following table lists the domain separation use cases for service providers \(SPs\) using this application.
locale: en-US
release: xanadu
product: Emergency Self Report
classification: emergency-self-report
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Emergency Self Report, Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Domain separation for Emergency Self Report

The following table lists the domain separation use cases for service providers \(SPs\) using this application.

|Use case|Functions|Limitations|
|--------|---------|-----------|
|SP Internal - SP uses the application for internal employees to self-report their status via a dedicated service portal or web page.|Yes|None|
|SP External - SP uses the application for tenant employees to self-report their status via a dedicated service portal or web page.|Yes|None|
|Tenant - Tenant uses the application for their sub-domain for their employees to self-report their status via a dedicated service portal or web page.|Yes|None|

Some modules in the Emergency Self Report application are affected by domain separation. These modules can be used by SPs and tenants.

-   **EMERGENCY SELF REPORT DASHBOARD module**
    -   A web page where users can self-report their current status. When they submit their status, a health record is created. \(Table: Crisis Task\)
    -   A knowledge base list of articles.
-   **ALL HEALTH RECORDS &amp; HR TASKS module \(Crisis Tasks\)**
    -   Domain column row protections exist.
    -   Extended from the Task table and therefore contains the necessary domain-separated business logic.
    -   Related list, Approvers \(Table: Approval\) is an established domain-separated table.
    -   Related list, Tasks \(Table: Task\) is an established domain-separated table.

**Parent Topic:**[Emergency Self Report](../concept/emergency-self-report.md)

