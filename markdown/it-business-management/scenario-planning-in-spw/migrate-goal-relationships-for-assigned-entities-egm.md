---
title: Migrate goal relationships for assigned entities
description: Migrate the existing goal relationship data from the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table by running the scheduled job.
locale: en-US
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring goals in Strategic Planning, Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Migrate goal relationships for assigned entities

Migrate the existing goal relationship data from the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table by running the scheduled job.

## Before you begin

Role required: admin

## About this task

-   If you’ve upgraded from Alignment Planner Workspace v4.1.1 or v5.0.1 to Strategic Planning v2.0.1 and have created m2m relationship with lens entities other than **Company**, **Business Unit**, **Department**, and **Portfolio**, you can migrate those lens entities from the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table to the Goals table to access and manage the goals for those lens entities in the respective portfolio plans.
-   Migrating goal relationships data for assigned entities is a one-time job, and not meant to be on a schedule.
-   Running the job populates the **Assigned entity type** and **Assigned entity** fields on the [Goal form](../reference/goal-form-egm.md) based on the data in the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table if you have any customized lenses other than the lens entity types, **Company**, **Business Unit**, **Department**, and **Portfolio**.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for and click the **Migrate goal relationships for assigned entities** scheduled job.

3.  On the Scheduled Script Execution form:

    1.  Ensure that the frequency is selected as **On Demand** in the **Run** field.

    2.  In the **Run this script** field, list the entities configured in the Goal Assigned Entity Configuration \[sn\_gf\_assigned\_entity\_config\] table that you want to migrate the goal relationship data for.

        For parameters information, see [Scheduled Script Execution form](../../alignment-planner-workspace/reference/scheduled-script-execution-form-egm.md).

4.  Click **Execute Now**.


**Parent Topic:**[Configuring goals in Strategic Planning](../concept/configuring-goal-framework-apw.md)

