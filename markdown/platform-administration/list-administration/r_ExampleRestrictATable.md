---
title: Example - Restrict a table
description: This access control prevents everyone from editing all fields in the Incident table in a list.
locale: en-US
release: yokohama
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring contextual security for the list editor, List editor administration, Administering lists, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Example - Restrict a table

This access control prevents everyone from editing all fields in the Incident table in a list.

![](../image/RestrictTheIncidentTable.png "Restrict the Incident Table")

-   **Type:** record
-   **Operation:** list\_edit
-   **Name Incident:**\[incident\]
-   **Admin overrides:** Clear the check box.
-   **Script:** `answer = false;`

