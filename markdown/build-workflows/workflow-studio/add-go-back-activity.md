---
title: Add a Go back activity to a playbook
description: Add a Go back activity to a decision branch in your playbook and configure where the playbook returns to when the activity runs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/add-go-back-activity.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 2
breadcrumb: [Go back activity, Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Add a Go back activity to a playbook

Add a Go back activity to a decision branch in your playbook and configure where the playbook returns to when the activity runs.

## Before you begin

Role required: pd\_author

## About this task

A Go back activity must be placed inside a decision branch. The decision must have at least one branch that moves forward in the playbook. For information about the Go back activity and design considerations, see [Go back activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/go-back-activity.md).

**Note:** If restart is not configured for the target, the playbook does not continue from that point. For information about configuring restart, see [Configure restart for Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/enable-define-restart.md).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the **Playbooks** tab, open the playbook you want to edit.

3.  Insert a Go back activity on an existing decision branch or between two stages in the Diagram view.

    1.  Select the \(+\) icon.

    2.  From the mini-picker, select **Add a Go back**.

    If you insert the Go back activity between two stages or activities without a decision node, Workflow Studio automatically inserts a decision node and places the next stage or activity and the Go back in parallel branches.

4.  Select the **Go back** activity.

5.  On the Go back properties panel, under the **Configuration** tab, configure the Go back target.

    |Go back to|Description|
    |----------|-----------|
    |**Activity**|The playbook returns to the start of a specific activity. Select the target activity from the list of activities earlier in the playbook.|
    |**Stage**|The playbook returns to the start of a specific stage. Select the target stage from the list.|
    |**Start of Playbook**|The playbook returns to the beginning. No additional selection is required.|

6.  Verify that your configuration is valid.

    Workflow Studio highlights errors in real-time. Correct any errors before activating.

7.  Complete the playbook by adding the stages and activities required for the process.


## What to do next

After the playbook is complete, test and activate it.

**Parent Topic:**[Go back activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/go-back-activity.md)

