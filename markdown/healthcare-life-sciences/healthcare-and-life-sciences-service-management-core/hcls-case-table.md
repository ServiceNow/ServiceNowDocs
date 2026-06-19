---
title: Healthcare case table
description: The Healthcare case \[sn\_hcls\_case\] table is an abstract table and is extendable that stores healthcare-related cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/healthcare-life-sciences/healthcare-and-life-sciences-service-management-core/hcls-case-table.html
release: zurich
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Healthcare case table

The Healthcare case \[sn\_hcls\_case\] table is an abstract table and is extendable that stores healthcare-related cases.

## Key features

-   Extends the Case \[sn\_customerservice\_case\] table to store all healthcare cases associated with a patient. For more information, see, Tables installed with Customer Service Management.
-   Includes the **Patient** field as an optional field anda reference to the Patient \[sn\_hcls\_patient\] table. For more information, see [Patient table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/healthcare-and-life-sciences-service-management-core/hcls-patient-table.md).
-   Enables healthcare case types including drug program enrollment, clinical trial enrollment, billing inquiry, and patient appointment request.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown).

**Parent Topic:**[Healthcare and Life Sciences data model tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/healthcare-and-life-sciences-service-management-core/hcls-healthcare-data-tables.md)

