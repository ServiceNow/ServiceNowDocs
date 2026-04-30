---
title: Example - Restrict a field
description: This access control prevents everyone except an administrator from editing the Short Description field of an incident record in a list.
locale: en-US
release: yokohama
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring contextual security for the list editor, List editor administration, Administering lists, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Example - Restrict a field

This access control prevents everyone except an administrator from editing the Short Description field of an incident record in a list.

![](../image/RestrictTheIncidentShortDescription.png "Restrict the Incident Short Description")

-   **Type:** record
-   **Operation:** list\_edit
-   **Name:** Incident \[incident\], Short Description
-   **Admin overrides:** Select the check box.
-   **Script:** `answer = false;`

