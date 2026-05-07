---
title: Time zones in SLAs
description: You can specify the geographical time zone that is used for schedule calculation.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Level Management reference, Service Level Management, IT Service Management]
---

# Time zones in SLAs

You can specify the geographical time zone that is used for schedule calculation.

Specify the time zone source to be used when creating task SLAs. The time zone selected is dependent on the requirements of the organization, making sure that teams are working to address a task or incident per the regular working hours or specified schedules defined for SLA.

The time zone addresses the requirements of the contractual requirements for the SLA.

You can select one of the following options:

-   **The caller's time zone**: If this option is selected, then the geographical time zone configured for the caller who has initiated the incident or task record is used. If the caller has not selected a time zone, then the system time zone is used.
-   **The SLA definition's time zone**: If the **The SLA definition's timezone** option is selected, the **Timezone** list appears. You can select from available time zone options.

**Timezone**: Specify a time zone for the SLA. The time zone can be the system time zone or active standard geographical time zones.

-   **The CI location's time zone**: If this time zone is specified, the time zone relevant to the CI associated with the incident or task is used. For example, if the team supporting the servers associated with a task is located in a specific location, their geographical time zone is used.
-   **The task location's time zone**: If this time zone is selected, the time zone of the assignment group associated with the task is used.
-   **The callers' location's time zone**: If this option is selected, then the time zone for the geographical location of the caller who has initiated the incident or task record is used. If the caller has not selected a time zone, then the system time zone is used.

**Note:** If you select a time zone source other than the **The SLA definition's timezone** and the time zone derived from the time zone source is empty, the system time zone is used.

**Parent Topic:**[Service Level Management reference](service-level-management-reference.md)

