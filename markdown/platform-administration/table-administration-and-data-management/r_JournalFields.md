---
title: Journal fields
description: Journal fields work together to create a log of changes and comments as tasks are worked on.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Task table structure, Working with the Task table, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Journal fields

Journal fields work together to create a log of changes and comments as tasks are worked on.

**Note:** Journal fields are shown regardless of the table audit enabled/disabled setting.

Fields of the journal\_input type are multi-line text boxes which, upon save, add the comments into the Activity field with a notation.

|Field|Description|
|-----|-----------|
|Additional comments|Any user can update.|
|Work notes|ITIL users can update.|

These comments, as well as any changes to the record or email notifications sent out because of the record, are displayed in the activity formatter, which can be added to the form like a field.

![](../image/ActivityFormatterForJournalFields.png "Activity formatter for journal fields")

**Parent Topic:**[Task table structure](../../table-administration/concept/task-table-structure.md)

