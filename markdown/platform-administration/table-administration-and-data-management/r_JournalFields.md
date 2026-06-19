---
title: Journal fields
description: Journal fields work together to create a log of changes and comments as tasks are worked on.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/table-administration-and-data-management/r\_JournalFields.html
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Task table structure, Working with Task table, Table admin, Tables and data, Configure core features, Administer]
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

\[Omitted image "ActivityFormatterForJournalFields.png"\] Alt text:

**Parent Topic:**[Task table structure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/table-administration-and-data-management/task-table-structure.md)

