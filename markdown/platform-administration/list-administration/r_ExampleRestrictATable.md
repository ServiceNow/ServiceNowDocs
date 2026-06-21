---
title: Example - Restrict a table
description: This access control prevents everyone from editing all fields in the Incident table in a list.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-administration/list-administration/r\_ExampleRestrictATable.html
release: xanadu
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring contextual security for the list editor, List editor administration, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Example - Restrict a table

This access control prevents everyone from editing all fields in the Incident table in a list.

\[Omitted image "RestrictTheIncidentTable.png"\] Alt text:

-   **Type:** record
-   **Operation:** list\_edit
-   **Name Incident:**\[incident\]
-   **Admin overrides:** Clear the check box.
-   **Script:** `answer = false;`

**Parent Topic:**[Configuring contextual security for the list editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/list-administration/r_ConfigListEditorContextSecurity.md)

**Previous topic:**[Configuring contextual security for the list editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/list-administration/r_ConfigListEditorContextSecurity.md)

**Next topic:**[Example - Restrict a field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/list-administration/r_ExampleRestrictAField.md)

