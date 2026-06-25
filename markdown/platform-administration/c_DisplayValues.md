---
title: Display values
description: Reference fields store a sys\_id for each referenced record in the database, but the sys\_id is not shown.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/c\_DisplayValues.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Display values

Reference fields store a sys\_id for each referenced record in the database, but the sys\_id is not shown.

The reference field shows the display value. For example, an incident's **Assigned to** field stores the sys\_id of a particular user, but actually displays the user's name. The following example shows how **Charlie Witherspoon**, which is the display value of a user record, is shown in the **Assigned to** field.

\[Omitted image "DisplayValueXml.png"\] Alt text: XML demonstrating an assigned\_to element with a sys\_id as the value and an assigned\_to="Charlie WItherspoon" attribute.Charlie Witherspoon is displayed in the Assigned to form field instead of the sys\_id.

|Reference field|Value stored in database|Display value field of source table|Value displayed in UI|
|---------------|------------------------|-----------------------------------|---------------------|
|Assigned to \[task.assigned\_to\]|46b87022a9fe198101a78787e40d7547|Name \[sys\_user.name\]|Charlie Whitherspoon|

Reference fields show display values in:

-   [Lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_UseLists.md)
-   Forms
-   Reports
-   [Auto-complete suggestions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_AutoCompleteForReferenceFields.md)
-   Slushbuckets

**Related topics**  


[Unique record identifier \(sys\_id\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_UniqueRecordIdentifier.md)

