---
title: Time zones in SLAs
description: You can specify the geographical time zone that is used for schedule calculation.
locale: en-US
release: zurich
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Service Level Management, IT Service Management]
---

# Time zones in SLAs

You can specify the geographical time zone that is used for schedule calculation.

Specify the time zone source to be used when creating task SLAs. You can select one of the following options:

-   **The caller's timezone**: If this option is selected and the caller has not selected a time zone, then the system time zone is used.
-   **The SLA definition's timezone**: If the **The SLA definition's timezone** option is selected, the **Timezone** list appears.

**Timezone**: Specify a time zone for the SLA. The time zone can be the system time zone or active standard geographical time zones.

-   **The CI location's timezone**
-   **The task location's timezone**
-   **The callers' location's timezone**

**Note:** If you select a time zone source other than the **The SLA definition's timezone** and the time zone derived from the time zone source is empty, the system time zone is used.

**Parent Topic:**[Service Level Management reference](service-level-management-reference.md)

