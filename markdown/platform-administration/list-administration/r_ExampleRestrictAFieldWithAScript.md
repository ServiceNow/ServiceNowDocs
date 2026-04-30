---
title: Example - Restrict a field with a script
description: This access control prevents everyone from editing an incident with a category of Software in a list. It is defined by a script.
locale: en-US
release: yokohama
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring contextual security for the list editor, List editor administration, Administering lists, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Example - Restrict a field with a script

This access control prevents everyone from editing an incident with a category of Software in a list. It is defined by a script.

![](../image/RestrictSoftwareIncidents.png "Restrict Software Incidents")

-   **Type:** record
-   **Operation:** list\_edit
-   **Name Incident:**\[incident\]
-   **Admin overrides:** Clear the check box.
-   **Script:**

    ```
    if (current.category == 'software')
    answer = false;
    else
    answer = true;
    ```


