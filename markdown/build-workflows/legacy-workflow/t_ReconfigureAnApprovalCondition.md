---
title: Reconfigure an approval condition
description: Approval activities react differently to script errors than the other activities.
locale: en-US
release: yokohama
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Workflow error handling, Workflow administration, Classic Workflow, Build workflows]
---

# Reconfigure an approval condition

Approval activities react differently to script errors than the other activities.

## About this task

Approval activity script errors can prevent an approval from being processed successfully. This, in turn, can cause the approval to complete as **Skipped**, which can appear to be an **Approved** state. To prevent this from happening, reconfigure the **Approved** exit as follows:

## Procedure

1.  Open an approval workflow and make sure it is checked out.

2.  On an approval activity, double-click the **Approved** exit.

3.  Add the following script to the **Condition** field:

    `&& activity.state != 'faulted'`

    This prevents the activity from continuing down the normal path in an error state and ensures that **Skipped** or **Approved** is the desired state.

4.  Click **Update**.


**Parent Topic:**[Workflow error handling](../concept/c_WorkflowErrorHandling.md)

