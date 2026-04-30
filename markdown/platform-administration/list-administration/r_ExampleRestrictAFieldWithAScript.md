---
title: Example - Restrict a field with a script
description: This access control prevents everyone from editing an incident with a category of Software in a list. It is defined by a script.
locale: en-US
release: xanadu
product: List Administration
classification: list-administration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring contextual security for the list editor, List editor administration, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
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


**Parent Topic:**[Configuring contextual security for the list editor](r_ConfigListEditorContextSecurity.md)

**Previous topic:**[Example - Restrict a field](r_ExampleRestrictAField.md)

**Next topic:**[Example - Restrict a field with a condition](r_ExRestrictAFieldWithACondition.md)

