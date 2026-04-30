---
title: Track part pickups on the Field Service Contractor Portal
description: You can see which parts are ready to be picked up by viewing a consolidated list of assets grouped by stockroom and waiting to be picked up. After picking up the part, you can close the transfer order line task.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Requesting and receiving required parts, Field Service Contractor Portal, Using Field Service Management, Field Service Management]
---

# Track part pickups on the Field Service Contractor Portal

You can see which parts are ready to be picked up by viewing a consolidated list of assets grouped by stockroom and waiting to be picked up. After picking up the part, you can close the transfer order line task.

## Before you begin

Role required: wm\_ext\_agent

## About this task

The agents can physically pick up the assets and then record them as delivered. The list contains transfer order lines in the Received or In Transit stage with a work order task that meets the following criteria:

-   Assigned to the agent
-   In the Accepted or Work in Progress state

## Procedure

1.  Navigate to **All** &gt; **Field Service Contractor Portal** &gt; **My Lists** &gt; **Pickup Parts**.

2.  From the **Transfer Order Line** list, select a transfer order line.

3.  From the **Transfer Order Line Tasks** list, select a transfer order line task that has the short description text "Receive" and the state Open.

4.  After physically picking up the items, click **Close Task**.

    The **Transfer Order Line Tasks** list displays a newly created transfer order line task that is ready to be delivered.

5.  Review the transfer order line task that has the short description text "Deliver" and the state Open.

6.  Click **Close Task**.


## Result

The part is delivered successfully to the agent.

**Parent Topic:**[Requesting and receiving required parts](../concept/requesting-and-receiving-parts.md)

