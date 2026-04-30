---
title: Mark records for updating
description: Mark records for updating according to one or more criteria by creating an update job.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Update records safely, Data Management, Tables and data, Configure core features, Administer]
---

# Mark records for updating

Mark records for updating according to one or more criteria by creating an update job.

## Before you begin

Role required: admin

## Procedure

1.  Either choose to mark specific records for updating or mark all records in a list for updating.

    -   To mark only specific records for updating, navigate to **All** &gt; **System Data Management** &gt; **Update Jobs**.
    -   To mark all records in a list for updating, in any list of records, right-click a column heading, and then select **Data Management** &gt; **Update All with preview**.
2.  Select the table that contains the records you want to update.

3.  Limit the number of records in the update job by adding a condition or conditions that records must meet.

    1.  Select a field, operator, and field value.

        For example, **\[Category\] \[is\] \[Software\]**.

    2.  Use the OR and AND operators to add conditions.

    3.  Select **New Criteria** to add another set of conditions.

    **Note:** Limiting the number of records that are added to the update job can help prevent the table from being locked when the job is executed.

4.  View the number of records that match the conditions.

    1.  Select **Preview**.

    2.  Select the link with the number of matching records.

5.  In the Fields &amp; values lists, select the field that you want to update and a new value.

6.  Select additional fields and values to update more fields.

7.  Select **Continue**.


## Result

The job is saved and the form provides options to schedule the job or execute it now.

## What to do next

[Schedule or execute a job to update records](schedule-execute-job-update-records.md)

**Parent Topic:**[Updating records safely](../concept/updating-records-safely.md)

