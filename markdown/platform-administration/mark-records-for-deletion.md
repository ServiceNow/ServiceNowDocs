---
title: Mark records for deletion
description: Mark records for deletion according to one or more criteria by creating a delete job.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Delete records safely, Data Management, Tables and data, Configure core features, Administer]
---

# Mark records for deletion

Mark records for deletion according to one or more criteria by creating a delete job.

## Before you begin

Role required: admin

## Procedure

1.  Either choose to mark specific records for deletion or mark all records in a list for deletion.

    -   To mark only specific records for deletion, navigate to **All** &gt; **System Data Management** &gt; **Delete Jobs**.
    -   To mark all records in a list for deletion, in any list of records, right-click a column heading, and then select **Data Management** &gt; **Delete All with preview**.
2.  Select the table that contains the records you want to delete.

3.  Limit the number of records in the delete job by adding one or more conditions that records must meet.

    1.  Select a field, operator, and field value.

        For example, **\[Category\] \[is\] \[Software\]**.

    2.  Use the OR and AND operators to add conditions.

    3.  Select **New Criteria** to add another set of conditions.

    **Note:** Limiting the number of records that are added to the delete job can help prevent the table from being locked when the job is executed.

4.  View the records that match the conditions.

    1.  Select **Preview**.

    2.  Select the link with the number of matching records.

    The list of records appears in a new browser tab.

5.  Return to the Delete Job tab.

6.  Select **Continue** to save the current job information.


## Result

The job is saved and the form displays options to schedule the job or execute it now.

## What to do next

[Preview affected records for deletion](preview-affected-records-for-deletion.md).

**Parent Topic:**[Deleting records safely](../concept/deleting-records-safely.md)

