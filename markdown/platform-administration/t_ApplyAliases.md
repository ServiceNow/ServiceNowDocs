---
title: Apply aliases
description: After testing, aliases can be normalized in all new records or in existing records when they are updated.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Normal values, Field normalization and transformation, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Apply aliases

After testing, aliases can be normalized in all new records or in existing records when they are updated.

## About this task

Each time an alias is created for a normal value, a data job is created. The alias is not applied to values in the entire database until its data job is started manually. Run each job separately or run the jobs together to apply all aliases at once.

## Procedure

1.  In a normalization record, ensure that the Mode is set to **Active**.

    Data jobs cannot run in the **Test** mode.

2.  Click the **Normal value** related list.

3.  Select a value from list.

4.  In the Normal Value record, select the **Data Jobs** related list.

    A data job is listed for each alias configured for this normal value.

5.  Run the extant data jobs to replace the aliases with the normal value in all existing records in the database.

    1.  Select the check box next to a job, and then select **Start** from the Actions menu.
    2.  To run all data jobs at once, select all the check boxes, and then select the **Start** action.
    3.  Refresh the list to check the progress of the data jobs to ensure that they complete normally.

**Parent Topic:**[Normal values](../concept/c_WhatFieldNormalizationDoes.md)

