---
title: Example - Restrict a field with a script
description: This access control prevents everyone from editing an incident with a category of Software in a list. It is defined by a script.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-administration/list-administration/r\_ExampleRestrictAFieldWithAScript.html
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

\[Omitted image "RestrictSoftwareIncidents.png"\] Alt text:

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


**Parent Topic:**[Configuring contextual security for the list editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/list-administration/r_ConfigListEditorContextSecurity.md)

**Previous topic:**[Example - Restrict a field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/list-administration/r_ExampleRestrictAField.md)

**Next topic:**[Example - Restrict a field with a condition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/list-administration/r_ExRestrictAFieldWithACondition.md)

