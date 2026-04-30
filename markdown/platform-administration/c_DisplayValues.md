---
title: Display values
description: Reference fields store a sys\_id for each referenced record in the database, but the sys\_id is not shown.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference field type, Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Display values

Reference fields store a sys\_id for each referenced record in the database, but the sys\_id is not shown.

The reference field shows the display value. For example, an incident's **Assigned to** field stores the sys\_id of a particular user, but actually displays the user's name. The following example shows how **Charlie Witherspoon**, which is the display value of a user record, is shown in the **Assigned to** field.

![](../image/DisplayValueXml.png "Display value xml")

|Reference field|Value stored in database|Display value field of source table|Value displayed in UI|
|---------------|------------------------|-----------------------------------|---------------------|
|Assigned to \[task.assigned\_to\]|46b87022a9fe198101a78787e40d7547|Name \[sys\_user.name\]|Charlie Whitherspoon|

Reference fields show display values in:

-   [Lists](https://www.servicenow.com/docs/access?context=c_UseLists&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)
-   Forms
-   Reports
-   [Auto-complete suggestions](c_AutoCompleteForReferenceFields.md#)
-   Slushbuckets

-   **[Select a field as the table display value](../task/t_SelectTheDisplayValue.md)**  
Only one field can be defined as the display value for a table.

**Parent Topic:**[Reference field type](c_ReferenceField.md)

**Related topics**  


[Unique record identifier \(sys\_id\)](../../table-administration/concept/c_UniqueRecordIdentifier.md#)

