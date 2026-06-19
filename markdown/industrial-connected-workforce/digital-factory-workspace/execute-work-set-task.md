---
title: Execute a work set task
description: Run a work set task to complete all sub-activities of the underlying work set standard as part of one guided flow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/industrial-connected-workforce/digital-factory-workspace/execute-work-set-task.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-05-25"
reading_time_minutes: 1
keywords: [execute work set, run work set task]
breadcrumb: [Standard and task life cycles, Industrial Standards, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Execute a work set task

Run a work set task to complete all sub-activities of the underlying work set standard as part of one guided flow.

## Before you begin

The parent work set standard is in the **Published** state and has at least one sub-activity.

Role required: sn\_icw\_std.work\_set\_user

## About this task

When a work set task is created, the system generates a child record for each sub-activity of the parent standard. Standard sub-activities create Industrial Guided Tasks records, and action sub-activities create industrial action records. The work set task tracks the overall progress of these child records.

## Procedure

1.  From the Digital Factory Workspace task list, select the work set task according to their requirement.

2.  Select **Set to Work in Progress**.

    The work set task also moves to **Work in Progress** automatically when any child task starts or when a child action closes.

3.  Open and complete each child task or action from the related lists on the work set task form.

    You can also pause the progress by selecting **Set on hold** from the overflow menu and resume by selecting **Set to Work in Progress**.

4.  Select **Create Deviation** or **Create Safety Incident** to capture an issue that you find while running the task.

    **Create Safety Incident** is available only when the health and safety integration is installed.

5.  When all child records are submitted or closed, select **Submit**.

    **Note:** If any child task is still active, the work set task can't close. You must complete or cancel the remaining child records first.


## Result

The work set task moves to the **Closed Complete** state. The system records the actual start time when the task moves to **Work in Progress** and the actual end time when the task is submitted.

If a work set task is canceled or expires \(**Closed Skipped**\), any active child tasks move to the same end state. Active child actions are canceled.

**Parent Topic:**[Work set standard and task life cycles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/work-set-standard-task-life-cycle.md)

