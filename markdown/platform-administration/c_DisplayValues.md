---
title: Display values
description: Reference fields store a sys\_id for each referenced record in the database, but the sys\_id is not shown.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Display values

Reference fields store a sys\_id for each referenced record in the database, but the sys\_id is not shown.

The reference field shows the display value. For example, an incident's **Assigned to** field stores the sys\_id of a particular user, but actually displays the user's name. The following example shows how **Charlie Witherspoon**, which is the display value of a user record, is shown in the **Assigned to** field.

![XML demonstrating an assigned_to element with a sys_id as the value and an assigned_to="Charlie WItherspoon" attribute.Charlie Witherspoon is displayed in the Assigned to form field instead of the sys_id.](../image/DisplayValueXml.png "Display value xml")

|Reference field|Value stored in database|Display value field of source table|Value displayed in UI|
|---------------|------------------------|-----------------------------------|---------------------|
|Assigned to \[task.assigned\_to\]|46b87022a9fe198101a78787e40d7547|Name \[sys\_user.name\]|Charlie Whitherspoon|

Reference fields show display values in:

-   [Lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_UseLists.md)
-   Forms
-   Reports
-   [Auto-complete suggestions](c_AutoCompleteForReferenceFields.md#)
-   Slushbuckets

**Related topics**  


[Unique record identifier \(sys\_id\)](../../table-administration/concept/c_UniqueRecordIdentifier.md#)

