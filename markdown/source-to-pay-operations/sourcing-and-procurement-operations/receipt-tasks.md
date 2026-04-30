---
title: Receipt tasks
description: Receipt tasks are created when goods receipt is required for the purchase line.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [receipt tasks, goods receipt]
breadcrumb: [Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Receipt tasks

Receipt tasks are created when goods receipt is required for the purchase line.

A receipt task references a purchase order and is grouped by the recipient and the calendar month of the product's expected delivery date. A receipt task is created only during the month of the expected delivery date, irrespective of the purchase order creation date, and remains open until all the expected deliveries for the recipient in a calendar month are confirmed. This is done using the \[PSM\] Create Receiving Task scheduled job.

Consider the following example:

The current month is September 2020, and for a purchase order, there are five purchase order lines:

|Purchase order line|Expected delivery date|Recipient|
|-------------------|----------------------|---------|
|1|September 10, 2020|John|
|2|September 20, 2020|John|
|3|October 22, 2020|John|
|4|September 12, 2020|Peter|
|5|October 5, 2020|John|

On the purchase order, three receipt tasks are created as follows:

-   Receipt task 1, associated to purchase order line 1 and 2, is created on September 1, 2020, with the state **Open**.
-   Receipt task 2, associated to purchase order line 3 and 5, is created on October 1, 2020, with the state **Open**.
-   Receipt task 3, associated to purchase order line 4, is created on September 1, 2020, with the state **Open**.

You can view all receipt tasks from the **Receipt Acknowledgment** sub-module under the Sourcing and Purchasing Automation module. The following are the key fields of a receipt task:

<table id="table_icy_vyy_hlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier of the receipt task.

</td></tr><tr><td>

Assigned to

</td><td>

Person primarily responsible for this receipt task.

</td></tr><tr><td>

Primary contact

</td><td>

Person within the procurement team who can be contacted with questions about receipts, milestones, invoices, or other activities related to acknowledgment. This field is populated or updated with the same user in the **Assigned to** field of the parent task record, as follows: For a receipt or acknowledgment task, from the referenced purchase order.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the receipt task. This description is dynamically populated based on whether there are one or multiple products to be received from the supplier.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the receipt task.

</td></tr><tr><td>

State

</td><td>

Status of the receipt task. For example, **Open**, **Shipped**, **Partially Complete**, and so on.

</td></tr><tr><td>

Due date

</td><td>

Expected due date from the person to whom this task is assigned.

</td></tr><tr><td class="sub-head" colspan="2">

Summary Details

</td></tr><tr><td>

Expected start

</td><td>

Expected start date of the receipt task.

</td></tr><tr><td>

Actual start

</td><td>

Actual start date of the receipt task.

</td></tr><tr><td>

Actual end

</td><td>

Actual end date of the receipt task.

</td></tr><tr><td>

Duration

</td><td>

Duration to complete this receipt task.

</td></tr></tbody>
</table>The following are the related lists of a receipt task:

<table id="table_ovd_sbz_hlb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Purchase order lines

</td><td>

List of all the related purchase order lines for this receipt task.

</td></tr><tr><td>

Receipts

</td><td>

List of all the receipts for this task.This list is populated when the shipment of the product is partially or fully complete.

 For more details, see [Receipts](receipts.md)

</td></tr><tr><td>

Shipment details

</td><td>

List of all the shipment tracking numbers for this receipt task.For more details, see [Shipment details](shipment-details.md).

</td></tr></tbody>
</table>**Parent Topic:**[Sourcing and Purchasing Automation](purchase-experience-workflow.md)

