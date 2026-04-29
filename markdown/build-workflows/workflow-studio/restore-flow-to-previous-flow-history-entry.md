---
title: Restore a flow to a previous flow history entry
description: Restore a flow to a previous configuration. Create a new flow history entry for the restore operation.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Flow history, Build flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Restore a flow to a previous flow history entry

Restore a flow to a previous configuration. Create a new flow history entry for the restore operation.

## Before you begin

Role required: flow\_designer or admin

## About this task

You can restore a flow when you want to set the current configuration to that of a previous flow history entry configuration. A restored flow duplicates the actions, flow logic, subflows, and data configuration from a previous flow configuration. Restoring a flow also creates a new flow history entry item.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Flows**.

3.  Open the flow that you want to restore.

4.  Select **Edit flow**.

5.  From the sidebar view, select the **History** icon.

6.  From the list of flow history entries, select the entry whose configuration you want to restore.

    Workflow Studio displays the configuration of flow history entry in the Flow History view.

7.  From the Flow History view, select **Restore**.

    ![Flow history entry for 5th June. 3:37 AM with option to Restore](../images/flow-history-restore-01.png)

8.  From the Restore confirmation dialog box, select **Restore**.

    ![Restore past version dialog box. Proceeding will duplicate version "5th June, 3:37am" and make it the current version.](../images/flow-history-restore-02.png)


## Result

![The Flow history list has a new entry of type Restored.](../images/flow-history-restore-03.png)

Workflow Studio displays the restored flow configuration.

**Parent Topic:**[Flow history](../concept/flow-history.md)

