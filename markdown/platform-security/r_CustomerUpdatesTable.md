---
title: Customer Updates table
description: Changes made in the system are recorded on the Customer Updates \[sys\_update\_xml\] table chronologically. There are a few exceptions, as noted below.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [System logs, Logs, Platform Security]
---

# Customer Updates table

Changes made in the system are recorded on the Customer Updates `[sys_update_xml]` table chronologically. There are a few exceptions, as noted below.

To navigate to this table, enter `sys_update_xml.list` into the navigation filter. For information about update sets, see [System update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/system-update-sets.md).

The following information is stored about each update:

|Field|Description|
|-----|-----------|
|Name|A name that identifies the updated record.|
|Created|The date and time the Customer Update record was created.|
|Created By|The user who performed the change.|
|Type|The type of the update.|
|Updated|The date and time the Customer Update record was updated.|
|Updated By|The user who performed the update.|
|Updates|The number of times the record has been updated.|
|Target Name|The name of the element that was altered.|
|View|The view of the form that was altered if it was a form layout change.|
|Payload|The XML contents of the record after the change.|
|Remote Update Set|A reference to that update set if the change was performed by a remote update set.|
|Local Update Set|The update set the change is associated with.|

**Note:** Some application changes are not represented by Customer Update records \(sys\_update\_xml\)​ Examples:​

-   Types of metadata where updateSynch = false
-   Cascading changes to tables and fields such as display name changes
-   Unresolved metadata references from other applications \(resulting in no “display value” on the element\)
-   sys\_id changes for coalescing files​
-   Changes to Flow/Flow Actions that may generate sys\_documentation
-   ua\_table\_license\_config records generated on table creation​
-   Jobs running in the background such as natural language processing
-   Cases where sys\_update\_xml is manually modified or removed

To learn more, see [Commit changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/t_CommitChanges.md).

​ ​ ​

