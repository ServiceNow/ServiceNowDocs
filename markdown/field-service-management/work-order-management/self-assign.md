---
title: Accept or reject a work order task on a mobile device
description: Accept or reject a work order task assigned to you through the Field Service Contractor for mobile application.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Field Service Contractor for mobile, Complete work orders on Mobile Agent, Using Field Service Management, Field Service Management]
---

# Accept or reject a work order task on a mobile device

Accept or reject a work order task assigned to you through the Field Service Contractor for mobile application.

## Before you begin

Role required: wm\_ext\_agent or wm\_ext\_manager

## Procedure

1.  Access your instance using the ServiceNow Agent mobile application.

2.  On the **My work** navigation tab, tap **All open tasks**

3.  Select the work order task from the list.

4.  On the work order task form, either accept or reject the task.

    -   To reject the task, tap **Reject**, select the reason for the rejection, and enter details.

        The following confirmation message appears at the top of the screen: `Task rejected successfully. Click here to view open tasks`.

    -   To work on the task yourself, tap **Accept**.
    **Note:** If the contractor agent or manager is unavailable, the following message is displayed: `Warning: WOTXXXXXX has been scheduled for a time you may not be available.`


## Result

The task is either accepted or rejected. If the task is rejected, it is reassigned depending on the role of the person who accepted or rejected it.

-   If a manager rejects the task, the state of the task changes to Pending dispatch or Pending assignment. The rejected task is assigned to the manager of next appropriate group. If the system cannot identify another qualified group, the task remains in the Pending dispatch state so the dispatcher can manually assign the task.

-   If an agent rejects the task, it is reassigned to the agent's manager.

**Parent Topic:**[Field Service Contractor for mobile](../concept/wot-fsc.md)

