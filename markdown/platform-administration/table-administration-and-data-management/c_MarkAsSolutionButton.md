---
title: Mark as Solution button
description: The Mark as Solution button is added to the KB popup view and displayed when you search the knowledge base from a task record.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Creating many-to-many task relations, Working with the Task table, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Mark as Solution button

The **Mark as Solution** button is added to the KB popup view and displayed when you search the knowledge base from a task record.

Selecting **Mark as Solution** creates a record in the Task / KB Relationships `[task_rel_kb]` table to associate the KB article with a task. You can disable this button by marking the active field false on the 'solution\_button' UI macro.

**Parent Topic:**[Creating many-to-many task relations](c_ManyToManyTaskRelations.md)

