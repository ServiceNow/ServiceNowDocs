---
title: Detach a saved trigger from a flow
description: View a list of flows that are associated with a saved trigger, and detach it from any of the flows. Detach a saved trigger before you specify different start conditions for your flow or before you delete the trigger.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a flow in Workflow Studio, Building flows, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Detach a saved trigger from a flow

View a list of flows that are associated with a saved trigger, and detach it from any of the flows. Detach a saved trigger before you specify different start conditions for your flow or before you delete the trigger.

## Before you begin

Role required: trigger\_designer, flow\_designer, or admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **Triggers**.

3.  From the list of triggers, select the trigger that you want to detach from a flow.

4.  Select the More Actions menu icon, then select **Associated objects**.

    ![Option to view the flows that are using the trigger.](../images/detach-a-trgger.png)

5.  From the list of flows that are using the trigger, select the flow that you want to detach.

6.  In the **Trigger** drop-down list, select the trigger name.

7.  Select the **Detach saved trigger** icon.

    ![Detach saved trigger from a flow.](../images/detach-flow-trigger.png)

8.  On the confirmation window, select **Detach**.

    Workflow Studio detaches the trigger and copies the start conditions from the saved trigger to the flow.

9.  Select **Done**.

10. Save the flow by clicking the save icon.


**Parent Topic:**[Create a flow in Workflow Studio](create-flow.md)

