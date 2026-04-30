---
title: Source parts in Dispatcher Workspace
description: Source parts from your preferred stockrooms or assignment groups to complete the work order task promptly.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing part requirements in Dispatcher Workspace, Working in Dispatcher Workspace, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Source parts in Dispatcher Workspace

Source parts from your preferred stockrooms or assignment groups to complete the work order task promptly.

## Before you begin

Role required: wm\_dispatcher

Ensure that the part you are sourcing is not requested before.

## About this task

Parts sourcing is a process of reserving and obtaining parts described in a part requirement record. You can source the necessary parts to complete the work order task.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Select **Dispatcher Workspace**.

3.  Click the work order task for which you want to source the parts from the task panel.

4.  Click the **Part Requirements** tab, view a list of required parts for the task.

5.  Select the part that you want to source.

    **Note:** The Source Part option is enabled only if you select a part that is not previously sourced or marked false as requested.

6.  Click **Source Part**.

7.  On the form, fill in appropriate option based on the desired sourcing criteria.

8.  <table id="table_ksd_1wx_xzb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

To stockroom

</td><td>

Location of the stockroom where the item is to be shipped.This field is auto-populated with a default personal stockroom location of the agent.

</td></tr><tr><td>

Stockroom selection criteria

</td><td>

Choice of a stockroom from where you want to source the part. For example, preferred stockrooms, all stockrooms, and assignment group stockrooms.

</td></tr><tr><td>

Search radius

</td><td>

Radius in selected distance unit \(miles or kilometers\).

</td></tr></tbody>
</table>    The stockroom locations appear in the Source part form and as cards in the map screen.

    **Note:** Only stockrooms that have the specified part are included in the list.

9.  If there are no stockrooms available that match the selected search criteria, you can either change the sourcing criteria or click **Place a part request** to source the part from assignment groups or other stockrooms.

    -   A part request \(REQ\) is created for the specified part requirement with the state as **Pending Approval** and the part request line with the state as **Requested**.
    -   A temporary part request \(RITM\) record is created for the requested parts and sent to your agents as a mobile notification.
10. Select a stockroom from the list of available stockrooms.

11. Enter the total quantity of the parts required to complete the task in the**Reserve quantity** field.

12. Click **Submit**.


## Result

The transfer order and transfer order line is created for the sourced part.

## What to do next

Complete the transfer orders: If the agent sources parts from other stockrooms or assignment groups, a transfer order line is created automatically. You can then complete the transfer order, ensuring the parts are moved to the designated location.

