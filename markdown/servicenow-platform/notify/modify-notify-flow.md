---
title: Create a custom Notify subflow
description: Create your own custom flows to use in Notify using Workflow Studio.
locale: en-US
release: australia
product: Notify
classification: notify
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Notify flows, Notify reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a custom Notify subflow

Create your own custom flows to use in Notify using Workflow Studio.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **Subflows**.

3.  Select **New** &gt; **Subflow**.

4.  Provide the details in the new subflow section, and then select **Build subflow**.

5.  Select **Action** under **ACTIONS**.

6.  Select **Global**, and then select a Notify action.

7.  Enter the details in Action Inputs based on the Notify action chosen.

    For example, if you select **Say**, you must enter the details as shown below:

    -   **Text to say**: Provide the text in this field that must be read.
    -   **Language**: Select the language.
    -   **Notify Call**: Select the Notify call.
8.  Select **Done**.

9.  Select **Publish**.

    A pop-up window appears to confirm the publication of the subflow.

10. Select **Publish**.


## What to do next

In order to use your workflow, you can test and map the subflow to a Notify number group. To map the subflow, you must navigate to **All** &gt; **Notify** &gt; **Number Groups**. Select a Notify group, and then map the created subflow.

**Parent Topic:**[Notify flows](../concept/notify-flow-designer.md)

