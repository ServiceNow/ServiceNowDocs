---
title: Example - Restrict a field with a condition
description: This access control prevents everyone from editing a Critical Incident in a list. It is defined by a condition.
locale: en-US
release: xanadu
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring contextual security for the list editor, List editor administration, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Example - Restrict a field with a condition

This access control prevents everyone from editing a Critical Incident in a list. It is defined by a condition.

![](../image/RestrictCriticalEvents.png "Restrict Critical Incidents")

-   **Type:** record
-   **Operation:** list\_edit
-   **Name Incident:**\[incident\]
-   **Admin overrides:** Clear the check box.
-   **Condition:** Priority is not 1 - Critical

**Parent Topic:**[Configuring contextual security for the list editor](r_ConfigListEditorContextSecurity.md)

**Previous topic:**[Example - Restrict a field with a script](r_ExampleRestrictAFieldWithAScript.md)

**Next topic:**[User preferences for list editing](r_ManagingUserPreferences.md)

