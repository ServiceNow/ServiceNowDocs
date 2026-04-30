---
title: Migrate existing goals data to Goal Framework tables
description: With the admin role, you can migrate the existing goals data to the Goal Framework tables by running the scheduled job.
locale: en-US
release: xanadu
product: Goal Framework
classification: goal-framework
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Migrate existing goals data to Goal Framework tables

With the admin role, you can migrate the existing goals data to the Goal Framework tables by running the scheduled job.

## Before you begin

Role required: admin

## About this task

**Note:** Migrating data to the Goal Framework tables is a one-time job, and not meant to be on a schedule.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for and click the **Migrate Goal, Strategy, and Work item data to the Goal Framework and related Planning item tables** scheduled job.

3.  On the Scheduled Script Execution form:

    1.  Ensure that the frequency is selected as **On Demand** in the **Run** field.

    2.  Set the value to **true** for the required parameters in the **Run this script** field.

        For parameters information, see [Migrate Goal, Strategy, and Work item data to the Goal Framework and related Planning item tables](../reference/scheduled-script-execution-form-gf-1.md#scheduled-job-to-migrate-goals-data).

4.  Click **Execute Now**.


