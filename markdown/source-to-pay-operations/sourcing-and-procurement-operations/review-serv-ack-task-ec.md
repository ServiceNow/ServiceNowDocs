---
title: Review your service acknowledgment task from Employee Center
description: Review and acknowledge the receipt status of your ordered service from your supplier from Employee Center.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Sourcing Procurement Operations integration Employee, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Review your service acknowledgment task from Employee Center

Review and acknowledge the receipt status of your ordered service from your supplier from Employee Center.

## Before you begin

Service acknowledgment tasks are auto-created the first time on purchase order creation, and are triggered on a monthly basis by the Create Service Acknowledgment Task scheduled job. This scheduled job automatically picks all purchase order lines that have started and are yet to reach their end dates, and have some remaining amount or percentage or quantity to be delivered.

To review your service acknowledgments, your service request should have been reviewed and approved by a Procurement Specialist and converted to a purchase order. Only then, this task is displayed to you on Employee Center.

Role required: sn\_shop.shopper

## About this task

The due date of your service acknowledgment task is set based on the due date defined by you when placing the order.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **My Tasks**.

2.  On the **Pending confirmation** tab, select the task that you want to work with.

3.  View details of the task, such as task number, due date, state, primary contact, purchase order number, supplier, order created, total amount, remaining amount, and so on.

    You can track the updates on the selected task from the **Activity** tab. You can also view and upload attachments associated with the task from the **Attachments** tab.

4.  Do one of these actions.

<table id="choicetable_drb_mxq_flb"><thead><tr><th align="left" id="d82649e121">

Action

</th><th align="left" id="d82649e124">

Description

</th></tr></thead><tbody><tr><td id="d82649e130">

**I didn't receive any services**

</td><td>

Displays the **Confirm you didn't receive any services** dialog box to record your confirmation for that particular month. On confirmation, the task is marked as Closed Complete and moved to the **Completed** tab. The scheduled job will run to create a new task for you the following month.

</td></tr><tr><td id="d82649e145">

**Mark as received**

</td><td>

Displays the **Specify the quantity you received** dialog box, where you can enter the received quantity for the selected purchase line for that particular month \(if the unit of the supplier product is individual unit\), or the received percentage \(if the unit of the supplier product is fixed fee\). This information is now displayed in the **Confirmed** tab.**Note:** If you select multiple purchase lines, you can't specify individual amounts or percentages for them, and the entire lines must be marked as received. Also, if the purchase order line has fixed fee as the unit, then it’s automatically set up for percentage.

</td></tr><tr><td id="d82649e162">

**Mark this task as complete**

</td><td>

Displays the **Confirm you didn't receive all services** dialog box to record your confirmation for that particular month. On confirmation, the task is marked as Closed Complete and moved to the **Completed** tab.

</td></tr></tbody>
</table>    **Note:** Every time you confirm receiving a percentage of your order, a receipt of type Services is automatically created. This receipt can be viewed by a Procurement Specialist against your purchase order on Source-to-Pay Workspace.


## What to do next

You can view the completed task in the **Completed** tab.

**Parent Topic:**[Sourcing and Procurement Operations integration with Employee Center](../concept/employee-center-integration-psm.md)

