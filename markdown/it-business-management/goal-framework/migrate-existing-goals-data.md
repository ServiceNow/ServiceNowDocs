---
title: Migrate existing goals data to Goal Framework tables
description: If your organization uses the legacy goal and strategy tables \(Goal, Enterprise Strategy, Business Unit Strategy, and Strategic Objective\), you can migrate the existing data to the Goal Framework tables by running the scheduled job.
locale: en-US
release: australia
product: Goal Framework
classification: goal-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Migrate existing goals data to Goal Framework tables

If your organization uses the legacy goal and strategy tables \(Goal, Enterprise Strategy, Business Unit Strategy, and Strategic Objective\), you can migrate the existing data to the Goal Framework tables by running the scheduled job.

## Before you begin

Role required: admin

## About this task

Use the scheduled job to migrate legacy goals and strategy data to the Goal Framework tables. The migration includes the following:

-   Migrates all existing goal records from the Goal \[goal\] table to the Goal \[sn\_gf\_goal\] table. Corresponding target records are automatically created in the Target \[sn\_gf\_goal\_target\] table.
-   Migrates all existing strategy records from the Enterprise Strategy \[enterprise\_strategy\], Business Unit Strategy \[business\_unit\_strategy\], and Strategic Objective \[strategic\_objective\] tables to the Strategic Priority \[sn\_gf\_strategy\] table.

**Note:** Migrating data to the Goal Framework tables is a one-time job, and not meant to be on a schedule.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for and click the **Migrate Goal, Strategy, and Work item data to the Goal Framework and related Planning item tables** scheduled job.

3.  On the Scheduled Script Execution form:

    1.  Ensure that the frequency is selected as **On Demand** in the **Run** field.

    2.  Set the value to **true** for the required parameters in the **Run this script** field.

        For parameters information, see [Migrate Goal, Strategy, and Work item data to the Goal Framework and related Planning item tables](../reference/scheduled-script-execution-form-gf-1.md#scheduled-job-to-migrate-goals-data).

4.  Click **Execute Now**.


