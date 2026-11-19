---
title: Table restriction example
description: This access control prevents everyone from editing all fields in the Incident table in a list.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/list-administration/r\_ExampleRestrictATable.html
release: brazil
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Contextual security, List editor, Administer, List administration, Forms, fields, and lists, Configure core features, ServiceNow AI Platform]
---

# Table restriction example

This access control prevents everyone from editing all fields in the Incident table in a list.

\[Omitted image "RestrictTheIncidentTable.png"\] Alt text:

-   **Type:** record
-   **Operation:** list\_edit
-   **Name:** Incident \[incident\]
-   **Admin overrides:** Clear the check box.
-   **Script:** `answer = false;`

