---
title: Healthcare Task table
description: The Healthcare Task \[sn\_hcls\_task\] table is an abstract table and is extendable that stores the details of the task associated with a healthcare case or a patient in your healthcare organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/healthcare-life-sciences/healthcare-and-life-sciences-service-management-core/hcls-task-table.html
release: xanadu
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Healthcare and Life Sciences data model tables, Healthcare and Life Sciences Service Management Core reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Healthcare Task table

The Healthcare Task \[sn\_hcls\_task\] table is an abstract table and is extendable that stores the details of the task associated with a healthcare case or a patient in your healthcare organization.

## Key features

-   Extends the Task \[task\] table to store all healthcare tasks associated with a patient or a healthcare case. For more information, see Task table.
-   Includes the **Patient** field as a reference to the Patient \[sn\_hcls\_patient\] table. For more information, see [Patient table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/healthcare-life-sciences/healthcare-and-life-sciences-service-management-core/hcls-patient-table.md).
-   Enables healthcare task types including appointment booking and updating insurance information.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown).

**Parent Topic:**[Healthcare and Life Sciences data model tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/healthcare-life-sciences/healthcare-and-life-sciences-service-management-core/hcls-healthcare-data-tables.md)

