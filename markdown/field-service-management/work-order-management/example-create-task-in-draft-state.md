---
title: Example - Create task without qualifying a work order
description: Create work order tasks and part requirements for a work order without qualifying a work order, when it is in the draft state.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage work orders, Prepare work orders, Using Field Service Management, Field Service Management]
---

# Example - Create task without qualifying a work order

Create work order tasks and part requirements for a work order without qualifying a work order, when it is in the draft state.

## Before you begin

-   You must enable **Apply Work Order template in draft status** to automatically create work order tasks based on the templates without the need for qualifying a work order. You can find this option by navigating to **Field Service** &gt; **Administration** &gt; **Configuration**.
-   To create or edit the work order template, work order task, or part requirements, you must ensure that the work order is in the draft state.

Role required: wm\_task\_initiator

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Work Order** &gt; **Draft Work Orders**.

2.  Open work order to which you want to apply template to create work order tasks.

3.  In the work order **Template** field, select a template for the work order and save the form.

    The work order tasks are created based on the selected template.

4.  Edit the work order template to create customized tasks.

    1.  In the Work Order Tasks related list, select all the existing tasks.

    2.  From the **Actions on selected rows** list, select **Delete**.

    3.  Go to the Template field and click **Preview this record** to edit the work order template.

        For more information about editing work order template, see [Create a work order template](../../it-services/task/t_CreateAWorkOrderTemplate.md).

5.  Create adhoc work order tasks.

    1.  In the Work Order Tasks related list, click **New**.

    2.  Fill in the required fields.

        For more information, see [Create a work order task](../../planning-and-policy/task/t_CreateAWorkOrderTask.md).

    3.  Click **Submit**.


**Parent Topic:**[Manage work orders](../../planning-and-policy/concept/c_ManageWorkOrders.md)

