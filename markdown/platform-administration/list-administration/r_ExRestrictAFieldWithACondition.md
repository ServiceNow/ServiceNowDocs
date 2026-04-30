---
title: Example - Restrict a field with a condition
description: This access control prevents everyone from editing a Critical Incident in a list. It is defined by a condition.
locale: en-US
release: zurich
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring contextual security, List editor, Administer, List administration, Forms, fields, and lists, Configure core features, Administer]
---

# Example - Restrict a field with a condition

This access control prevents everyone from editing a Critical Incident in a list. It is defined by a condition.

![](../image/RestrictCriticalEvents.png "Restrict Critical Incidents")

-   **Type:** record
-   **Operation:** list\_edit
-   **Name Incident:**\[incident\]
-   **Admin overrides:** Clear the check box.
-   **Condition:** Priority is not 1 - Critical

