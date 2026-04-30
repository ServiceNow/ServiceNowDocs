---
title: Integration with Healthcare and Life Sciences Service Management Core
description: Vaccine Administration Management is integrated with the ServiceNow Healthcare and Life Sciences Service Management Core application, enabling capabilities such as synchronization of some records across applications and services, and vaccination history that patient users can view.
locale: en-US
release: yokohama
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Vaccine Administration Management reference, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Integration with Healthcare and Life Sciences Service Management Core

Vaccine Administration Management is integrated with the ServiceNow® Healthcare and Life Sciences Service Management Core application, enabling capabilities such as synchronization of some records across applications and services, and vaccination history that patient users can view.

Vaccine Administration Management relies on the Healthcare and Life Sciences Service Management Core application to create or link to existing patient, consumer, and immunization records. Integration with Healthcare and Life Sciences Service Management Core uses the following tables:

-   Patient \[sn\_hcls\_patient\] table-Stores patient details, and links to a user's personal information, user, and consumer records.
-   Immunization \[sn\_hcls\_immunization\] table-Stores a record of immunization data that an associated user can see as their vaccination history from the vaccine portal.

Integration with Healthcare and Life Sciences Service Management Core also adds the sn\_hcls.patient role to the Vaccine Administration Management self-service portal user \[sn\_vaccine\_sm.user\] role.

**Related topics**  


[Healthcare and Life Sciences Service Management Core](../../healthcare-life-sciences/concept/hcls-core-app.md)

[Patient table](../../healthcare-life-sciences/reference/hcls-patient-table.md)

[Immunization table](../../healthcare-life-sciences/reference/hcls-immunization-table.md)

