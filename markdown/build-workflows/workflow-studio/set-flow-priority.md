---
title: Set flow priority
description: Determine the order in which worker threads run background flows. Use a mix of flow priorities to distinguish between flows to defer and flows to run first.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Flow priority, Flow administration, Configure flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Set flow priority

Determine the order in which worker threads run background flows. Use a mix of flow priorities to distinguish between flows to defer and flows to run first.

## Before you begin

-   Role required: flow\_designer or admin
-   [Show flow priority field](show-flow-priority-field.md)

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select the **Flow** data pill filter.

3.  Open the flow whose priority you want to set.

4.  Select **Edit flow**.

5.  From the More Actions menu, select **Properties**.

6.  From the Flow properties window, expand **Advanced Options**.

7.  From **Flow Priority Default**, select the priority value you want for the flow.

    You can set background flows to have one of these priority values.

    -   High
    -   Medium
    -   Low
    By default, background flows run with medium priority.

    **Note:** Flows that run in the foreground run with an elevated priority above background flows.

8.  Select **Update**.


## Result

The flow runs at the priority you specify as long as it does not pause or get delegated to another node to run.

## What to do next

Use the FDIH dashboard to review the flow executions and verify that your flows are running as expected.

**Parent Topic:**[Flow priority](../concept/flow-priority.md)

