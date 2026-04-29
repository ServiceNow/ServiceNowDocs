---
title: Define a task relationship allowed from the task relationship type record
description: Define the Task Relationships Allowed from the Task Relationship Type record.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Many-to-many task relations, Working with Task table, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Define a task relationship allowed from the task relationship type record

Define the Task Relationships Allowed from the Task Relationship Type record.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Task Relationships** &gt; **Relationship Types**.

2.  Select a Task Relationship Type record.

3.  In the Task Relationship Allowed related list, select **New**.

4.  Populate the parent and child tables to define which tables are able to accept the relationship.

5.  Define scripts to run in the Parent and Child script fields.

    These scripts are run when a parent or child record is run to automatically generate the other task \(child or parent\). These scripts use the current value of the new record, as opposed to the source record which triggered the script.

6.  Select **Submit**.


**Parent Topic:**[Creating many-to-many task relations](../concept/c_ManyToManyTaskRelations.md)

