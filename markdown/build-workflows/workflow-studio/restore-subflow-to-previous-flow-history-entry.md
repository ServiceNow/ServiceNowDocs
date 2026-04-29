---
title: Restore a subflow to a previous flow history entry
description: Restore a subflow to a previous configuration. Create a new flow history entry for the restore operation.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Subflow history, Build subflows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Restore a subflow to a previous flow history entry

Restore a subflow to a previous configuration. Create a new flow history entry for the restore operation.

## Before you begin

Role required: flow\_designer or admin

## About this task

You can restore a subflow when you want to set the current configuration to that of a previous flow history entry configuration. A restored subflow duplicates the actions, flow logic, subflows, and data configuration from a previous flow configuration. Restoring a subflow also creates a new flow history entry item.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Subflows**.

3.  Open the subflow that you want to restore.

4.  Select **Edit subflow**.

5.  From the sidebar view, select the **History** icon.

6.  From the list of flow history entries, select the entry whose configuration you want to restore.

    Workflow Studio displays the configuration of flow history entry in the Flow History view.

7.  From the Flow History view, select **Restore**.

    ![Flow history entry for 5th June, 5:14 AM with option to Restore](../images/subflow-history-restore-01.png)

8.  From the Restore confirmation dialog box, select **Restore**.

    ![Restore past version dialog box. Proceeding will duplicate version "5th June, 5:14am" and make it the current version.](../images/subflow-history-restore-02.png)


## Result

![The Flow history list has a new entry of type Restored.](../images/subflow-history-restore-03.png)

Workflow Studio displays the restored subflow configuration.

**Parent Topic:**[Subflow history](../concept/subflow-history.md)

