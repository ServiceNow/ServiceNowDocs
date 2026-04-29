---
title: Worker profile synchronization limitations
description: Limitations to the data that is synchronized from Workday to ServiceNow.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference - HR Service Delivery Integration with Workday, HR Service Delivery Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Worker profile synchronization limitations

Limitations to the data that is synchronized from Workday to ServiceNow.

-   Partial pull is not supported for Department and Location. It is only supported for HR profile and Job Profile.
-   When an organization, a location, and a job profile is made inactive in Workday, it does not become inactive in ServiceNow. This is because the Department table, Location table, and Job profiles table in ServiceNow do not have the **Active** field to record the status information.
-   The following fields are not mapped while synchronizing HR profiles:
    -   Under Employee Information: Leave status, Location type, Notice period, Probation end date, Probation period, Social Security number, and Business.
    -   Under Jobs: Location type and Work email.

**Parent Topic:**[Reference - HR Service Delivery Integration with Workday](hrsd-int-workday-reference.md)

**Related topics**  


[Components installed with HR Service Delivery Integration with Workday](installed-with-wd.md)

