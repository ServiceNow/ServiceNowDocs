---
title: Table restriction example
description: This access control prevents everyone except admins from editing all fields in the Incident table in a list.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/list-administration/r\_ExampleRestrictATable.html
release: australia
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2026-11-09"
reading_time_minutes: 1
breadcrumb: [Contextual security, List editor, Administer, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Table restriction example

This access control prevents everyone except admins from editing all fields in the Incident table in a list.

\[Omitted image "RestrictTheIncidentTable.png"\] Alt text: Access control that restricts list editing on the Incident table to admins.

-   **Type:** record
-   **Operation:** list\_edit
-   **Name:** Incident \[incident\]
-   **Decision Type:** Allow If
-   **Role:** admin

