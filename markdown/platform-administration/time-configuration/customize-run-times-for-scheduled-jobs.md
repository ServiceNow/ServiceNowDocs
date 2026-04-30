---
title: Enable run types for scheduled job child tables
description: The run types; Day and Month in Year, Day in Week in Month in Year, and Week in Month, require the fields; Day, Month, and Year to be visible. Child tables which don’t display those fields can't create jobs with that run type selected.Identify child tables in scheduled jobs to promote consistent configuration across all related tables. This helps maintain data integrity and uniform processing logic throughout the table hierarchy.
locale: en-US
release: zurich
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a scheduled job, Scheduled jobs, System scheduler, Explore, Time configuration, Configure core features, Administer]
---

# Enable run types for scheduled job child tables

The run types; **Day and Month in Year**, **Day in Week in Month in Year**, and **Week in Month**, require the fields; **Day**, **Month**, and **Year** to be visible. Child tables which don’t display those fields can't create jobs with that run type selected.

## Before you begin

Identify the child table for which you’re configuring new run times. To find child tables, follow the instructions in [Find child tables for scheduled jobs](customize-run-times-for-scheduled-jobs.md#).

Role required: admin

## Procedure

1.  Configure **Run** time options:
2.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

3.  Select **New**.

4.  Select **Automatically run a script of your choosing**.

5.  Select the **Run** menu to display available choices.

    If the choices for the **Run** menu have been previously modified, the new run types won’t be visible. To add them:

    1.  Select and hold \(or right-click\) **Run** and select **Configure Choices**.

    2.  Select the choices for **Run** that you want to add and select **Add**.


**Parent Topic:**[Create a scheduled job](t_CreateAScheduledJob.md)

## Find child tables for scheduled jobs

Identify child tables in scheduled jobs to promote consistent configuration across all related tables. This helps maintain data integrity and uniform processing logic throughout the table hierarchy.

### Before you begin

Role required: admin

### About this task

There are two ways to locate child tables of a scheduled job; either by running a script or using search parameters.

### Procedure

1.  Run a background script such as: `gs.info(GlideDBObjectManager.get().getAllExtensions('sysauto'));`

    The script is an efficient and thorough way to gather the names of all child tables to a parent table.

2.  Search the **sys\_db\_object\_list** table, using the search parameters: **Extends table label starts with Scheduled Job or Extends table Extends table label starts with scheduled Job or Extends table Extends table Extends table label starts with scheduled jobs.**

    Depending on the depth of the table hierarchy, additional parameters might be needed to find all child tables.


**Related topics**  


[Scheduled jobs](../../reference-pages/concept/c_ScheduledJobs.md)

[Create a scheduled job](t_CreateAScheduledJob.md)

[Advanced options for scheduled jobs](advanced-options-for-scheduled-jobs.md)

[Enable run types for scheduled job child tables](customize-run-times-for-scheduled-jobs.md#)

