---
title: Example - Restrict a field
description: This access control prevents everyone except an administrator from editing the Short Description field of an incident record in a list.
locale: en-US
release: xanadu
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring contextual security for the list editor, List editor administration, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Example - Restrict a field

This access control prevents everyone except an administrator from editing the Short Description field of an incident record in a list.

![](../image/RestrictTheIncidentShortDescription.png "Restrict the Incident Short Description")

-   **Type:** record
-   **Operation:** list\_edit
-   **Name:** Incident \[incident\], Short Description
-   **Admin overrides:** Select the check box.
-   **Script:** `answer = false;`

**Parent Topic:**[Configuring contextual security for the list editor](r_ConfigListEditorContextSecurity.md)

**Previous topic:**[Example - Restrict a table](r_ExampleRestrictATable.md)

**Next topic:**[Example - Restrict a field with a script](r_ExampleRestrictAFieldWithAScript.md)

