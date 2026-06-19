---
title: Mark as Solution button
description: The Mark as Solution button is added to the KB popup view and displayed when you search the knowledge base from a task record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/table-administration-and-data-management/c\_MarkAsSolutionButton.html
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Many-to-many task relations, Working with Task table, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Mark as Solution button

The **Mark as Solution** button is added to the KB popup view and displayed when you search the knowledge base from a task record.

Selecting **Mark as Solution** creates a record in the Task / KB Relationships `[task_rel_kb]` table to associate the KB article with a task. You can disable this button by marking the active field false on the 'solution\_button' UI macro.

**Parent Topic:**[Creating many-to-many task relations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_ManyToManyTaskRelations.md)

