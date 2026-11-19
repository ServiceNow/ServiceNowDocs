---
title: Restore a flow to a previous flow history entry
description: Restore a flow to a previous configuration. Create a new flow history entry for the restore operation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/workflow-studio/restore-flow-to-previous-flow-history-entry.html
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Flow history, Building flows, Use, Workflow Studio, Build workflows]
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

    \[Omitted image "flow-history-restore-01.png"\] Alt text: Flow history entry for 5th June. 3:37 AM with option to Restore

8.  From the Restore confirmation dialog box, select **Restore**.

    \[Omitted image "flow-history-restore-02.png"\] Alt text: Restore past version dialog box. Proceeding will duplicate version "5th June, 3:37am" and make it the current version.


## Result

\[Omitted image "flow-history-restore-03.png"\] Alt text: The Flow history list has a new entry of type Restored.

Workflow Studio displays the restored flow configuration.

**Parent Topic:**[Flow history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/flow-history.md)

