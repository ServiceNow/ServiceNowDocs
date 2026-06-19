---
title: Example - Restrict a table
description: This access control prevents everyone from editing all fields in the Incident table in a list.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/list-administration/r\_ExampleRestrictATable.html
release: australia
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring contextual security, List editor, Administer, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Example - Restrict a table

This access control prevents everyone from editing all fields in the Incident table in a list.

\[Omitted image "RestrictTheIncidentTable.png"\] Alt text:

-   **Type:** record
-   **Operation:** list\_edit
-   **Name Incident:**\[incident\]
-   **Admin overrides:** Clear the check box.
-   **Script:** `answer = false;`

