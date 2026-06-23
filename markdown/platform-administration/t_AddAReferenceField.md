---
title: Add a reference field
description: Add reference fields to a table using the same method as for any other field.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-administration/t\_AddAReferenceField.html
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference field type, Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Add a reference field

Add reference fields to a table using the same method as for any other field.

## Before you begin

Role required: personalize\_form

## About this task

The related table also appears in the Available Tables list for future form customizations.

## Procedure

1.  Open the desired form.

2.  Right-click the header and select **Configure** &gt; **Form Layout**.

3.  Use [dot-walking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-user-interface/configure-user-experiences/c_DotWalking.md) to locate and select the field in the referenced table that you want to add.

    It appears as **Table name.Field**. For example, the caller's email address appears as **Caller.Email**.

4.  Click **Save**.


-   **[Enable dynamic creation for reference fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/t_EnableDynCreationForRefFields.md)**  
When dynamic creation is enabled, entering a nonexistent value in a reference field creates a new record on the referenced table instead of returning an error.
-   **[Configure cascade delete rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/t_CascadeDeleteRules.md)**  
When a record is deleted, there are different options for how the deletion will affect records that reference the deleted record. You can configure what happens to records that reference a record when that record is deleted.
-   **[Define the reference key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/t_DefineTheReferenceKey.md)**  
By default, reference fields store the sys\_id of the record in the database.
-   **[Display a reference field as a choice list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/t_DisplayTheRefFieldAsAChoiceList.md)**  
You can display a reference field as a choice list instead of opening a lookup window.

**Parent Topic:**[Reference field type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/c_ReferenceField.md)

