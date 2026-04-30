---
title: Data Certification planning
description: Initial planning can make the certification process more successful.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data Certification on Core UI, Data Certification, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data Certification planning

Initial planning can make the certification process more successful.

By defining certification schedules and certification audit definitions, users with the certification\_admin role establish when certifications are performed, who performs it, and what data must be certified.

## Required Roles

Users with the certification\_admin role can view filter versions. These users can create, update, and delete filters, if they have the proper access to necessary tables. In the base ServiceNow system, certification\_admin users have limited system rights and do not have access to all the tables required for creating a filter. When assigning compliance resources, make sure to grant additional roles to the certification\_admin user as needed. For example, this user requires roles that grant access to these tables:

-   Company `[core_company]`
-   Cost Center `[cmn_cost_center]`
-   Schedule `[cmn_schedule]`

## Planning Data Certification

Planning the data certification process requires defining:

-   The certification schedule defines certification for a particular set of information on a particular table. It also generates certification tasks to perform that certification. One certification task is generated per task owner and a certification instance record groups the tasks.
-   The optional certification audit definition groups some certification schedules to be performed together and generates certification audit instances to perform them.

The following questions require answers for each certification schedule:

-   What information requires certification?
-   When is the due date for certification?
-   Who must perform the certification?

