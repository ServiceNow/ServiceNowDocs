---
title: Use drop off lists
description: Agents use drop off lists to return items that are in their personal stockroom.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Updating task status in web interface, Complete work orders on the web interface, Using Field Service Management, Field Service Management]
---

# Use drop off lists

Agents use drop off lists to return items that are in their personal stockroom.

An item may need to be returned because it is defective or not needed to complete a work order task. Agents can create a drop off list of items to send the items to a different stockroom using a transfer order. Agents also have the option to physically drop items off at a stockroom and note the drop off in the Field Service Management application.

An asset must meet the following criteria to be added to an agent's drop off list:

-   Located in the agent's personal stockroom
-   **Drop Off** check box selected on the transfer order record
-   One of the following:
    -   Substate is **Defective**
    -   Asset was not used and the work order task is in **Closed Complete** state

-   **[Create a drop off list](../task/t_CreateADropOffList.md)**  
Agents can create a drop off list of assets at any time.
-   **[View a drop off list](../task/t_ViewADropOffList.md)**  
Agents can view a consolidated list, grouped by stockroom, of all items that have been added to drop off lists by all agents.
-   **[Drop off an asset](../task/t_DropOffAnAsset.md)**  
Agents can physically drop assets off at a stockroom.

**Parent Topic:**[Updating task status in web interface](../../field-service-management/concept/updating-task-status-in-web-interface.md)

