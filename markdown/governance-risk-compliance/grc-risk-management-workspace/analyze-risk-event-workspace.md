---
title: Analyze a risk event in the Risk Workspace
description: Analyze user-submitted risk events. You can add additional details to the risk event, request more information from the submitter, or reject the risk event if the event is not valid.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Analyze a risk event in the Risk Workspace

Analyze user-submitted risk events. You can add additional details to the risk event, request more information from the submitter, or reject the risk event if the event is not valid.

## Before you begin

Role required: sn\_risk.manager

## About this task

When you a risk event is submitted, it contains basic or little information. As a risk manager, you must add additional details to it when the event is in the **Analyze** state. These additional details consist of the following:

-   Approvers of the risk event.
-   Root cause of the event.
-   Preventative and remedial action for the event.
-   Additional entries for the event to break up the event losses.
-   Citations
-   Tasks
-   Impacted controls
-   Issues

If you need more information about the risk event, you can ask the submitter to provide you additional information. If you think that the event does not merit attention or is invalid, then you can reject the event.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace** &gt; **Risk events** &gt; **All events**.

2.  Open the event to analyze and click **Analyze**.

3.  Click the Details related list and modify any information that you may need.

    If the risk event occurred but the losses were quickly recovered, the**Full rapid recovery** option is selected. If the risk event resulted in a gain, instead of a loss, the **Financial gain** option is selected. To understand how a risk event can result in a gain, see [Manage risk events](../../grc-risk/reference/manage-risk-events.md#)

4.  Click **Save**

5.  At this stage, you can do one of the following.

    |Task|Action|
    |----|------|
    |**Request approval from the approvers identified.**|Click **Request approval**.|
    |**If further details are required from the submitter, request more information.**|Click **Request more information**.|
    |**If the risk event is not valid, reject the event.**|Click **Reject**.|

6.  To add more information to the risk event, click the appropriate related list and add the necessary details.


## What to do next

If the risk event is of subtype **Actual**, create risk event entries. For more information see [Create a risk event entry in the Risk Workspace](create-risk-event-entry-ws.md).

**Parent Topic:**[Using the Risk Workspace](../concept/using-risk-workspace.md)

