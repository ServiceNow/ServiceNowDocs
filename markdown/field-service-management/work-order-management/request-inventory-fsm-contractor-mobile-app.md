---
title: Request inventory using the Field Service Contractor for mobile application
description: Request inventory to receive parts when your stock gets low or you need a part for a particular work order.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Field Service Contractor for mobile, Complete work orders on Mobile Agent, Using Field Service Management, Field Service Management]
---

# Request inventory using the Field Service Contractor for mobile application

Request inventory to receive parts when your stock gets low or you need a part for a particular work order.

## Before you begin

Role required: wm\_ext\_agent, wm\_ext\_manager

## About this task

You can request the required parts from your group or personal stockroom. If you request parts from the group stockroom, the transfer orders are automatically generated.

## Procedure

1.  Access your instance using the ServiceNow Agent mobile application.

2.  On the **My work** navigation tab, tap **My Tasks**.

3.  Select the work order task that needs parts.

4.  Tap on the **Parts** tab.

5.  Under part requirements, tap **Create Part Requirement**.

6.  Tap **Model**.

7.  Select a part model.

8.  In the **Required quantity** field, enter the total quantity of the parts required to complete the task.

9.  In the **Required by date** field, enter the date by which all parts should be delivered.

10. Enable the **Mandatory** option to specify the parts required to perform the work order task.

11. Tap **Submit**.

    A message appears as the part requirement is created.

12. Navigate back to the part requirements list screen and tap the part requirement card.

13. Tap **Find part** to locate the specific part.

    The stockroom locations appear on the screen.

14. Tap the stockroom from which you want to receive the parts and then tap **Source part**.

15. Select the stockroom to which the sourced parts will be transferred.

    For example, if you need to receive parts to your stockroom then select your personal stockroom.

16. In the **Quantity** field, enter the quantity of the parts required to complete the task.

17. Tap the **Next** icon.

18. Navigate back to the **Inventory** screen.


## Result

The Part Requirements and Transfer Orders related lists are updated automatically in the work order task form.

**Parent Topic:**[Field Service Contractor for mobile](../concept/wot-fsc.md)

