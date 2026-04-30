---
title: Reference field type
description: A reference field stores a reference to a field on another table. For example, the Caller field on the Incident table is a reference to the User \[sys\_user\] table.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Reference field type

A reference field stores a reference to a field on another table. For example, the **Caller** field on the Incident table is a reference to the User \[sys\_user\] table.

When you define a reference field, the system creates a relationship between the two tables. Adding a reference field to a form makes the other fields in the referenced table available to the form.

**Note:** A reference field can refer only to records from one other table. To add a field that can refer to records on any table, use the Document ID element type.

Administrators can create new reference fields and configure several options for reference fields.

|Option|Description|
|------|-----------|
|Display values|Each reference field stores a sys\_id for each referenced record in the database, but the sys\_id is not shown. The reference field shows the specified display value.|
|Decorations|A reference decoration is an icon that appears next to a reference field.|
|Reference styles|Reference styles are specialized field styles that control the appearance of reference fields.|
|Reference qualifiers|Reference qualifiers restrict the records that are available for reference fields.|
|Cascade delete rules|Cascade delete rules specify what should happen to records that reference a record that is deleted.|
|Auto-complete|By default, a reference field auto-completes as the user types in the field. Administrators can configure auto-complete settings.|
|Reference key|A reference key saves a field other than sys\_id as the unique identifier for a reference field.|
|Enable dynamic creation|When dynamic creation is enabled, entering a nonexistent value in a reference field creates a new record on the referenced table instead of returning an error.|

**Tip:** For troubleshooting information, see the [Reference field is not showing the expected display value when selected or it appears blank \[KB0693859\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0693859) article in the Now Support Knowledge Base.

