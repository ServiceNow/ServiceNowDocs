---
title: Add a reference field
description: Add reference fields to a table using the same method as for any other field.
locale: en-US
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

3.  Use [dot-walking](https://www.servicenow.com/docs/access?context=c_DotWalking&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) to locate and select the field in the referenced table that you want to add.

    It appears as **Table name.Field**. For example, the caller's email address appears as **Caller.Email**.

4.  Click **Save**.


-   **[Enable dynamic creation for reference fields](t_EnableDynCreationForRefFields.md)**  
When dynamic creation is enabled, entering a nonexistent value in a reference field creates a new record on the referenced table instead of returning an error.
-   **[Configure cascade delete rules](t_CascadeDeleteRules.md)**  
When a record is deleted, there are different options for how the deletion will affect records that reference the deleted record. You can configure what happens to records that reference a record when that record is deleted.
-   **[Define the reference key](t_DefineTheReferenceKey.md)**  
By default, reference fields store the sys\_id of the record in the database.
-   **[Display a reference field as a choice list](t_DisplayTheRefFieldAsAChoiceList.md)**  
You can display a reference field as a choice list instead of opening a lookup window.

**Parent Topic:**[Reference field type](../concept/c_ReferenceField.md)

