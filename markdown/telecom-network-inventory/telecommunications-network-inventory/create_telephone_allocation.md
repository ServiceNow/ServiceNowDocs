---
title: Create a telephone number allocation
description: Created topic for STRY55294083 - DOC1071773Create a telephone number allocation so that you can group a set of telephone numbers and apply the required conditions to it by using the Telecommunications Network Inventory application. You can also review, create, update, or delete a telephone number allocation.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a telephone infrastructure, Inventory number allocation, Defining inventory records, Use, Telecommunications Network Inventory]
---

# Create a telephone number allocation

Create a telephone number allocation so that you can group a set of telephone numbers and apply the required conditions to it by using the Telecommunications Network Inventory application. You can also review, create, update, or delete a telephone number allocation.

## Before you begin

-   Ensure that the Telecommunications Network Inventory application includes all the required components of your telephone number. Otherwise, see [Creating telephone number components](../concept/create_components_of_a_telephone_number.md).
-   Role required: sn\_inv\_num\_mgmt.inventory\_number\_manager

## About this task

Setting the Create telephone allocations and numbers checkbox as true, while creating a telephone block, creates individual numbers and telephone allocation. You can assign multiple telephone numbers to a telephone allocation. When you assign a single telephone number allocation to a telephone number block, you can assign a series of numbers to that block.

On completing this task, assigning a single telephone number allocation to a telephone number block results in assigning a series of numbers to that block.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory Number Allocation** &gt; **Telephone Number**.

3.  Select **New**.

4.  On the **Details** tab, on the IP address section form, fill in the fields.

<table id="table_mqw_wfq_mxb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for this allocation.

</td></tr><tr><td>

Telephone number block

</td><td>

Telephone number block that you want to add the numbers to.**Note:** For the port-in numbers or the numbers that you don’t want to assign a block to, you can create the telephone numbers and telephone allocation without referring to a block.

</td></tr><tr><td>

Availability

</td><td>

Availability of this block. If this block is available, set the availability as true. Also, you can specify how many numbers are under the unassigned status and are available.

</td></tr><tr><td>

Start number

</td><td>

Starting phone number of the series from where you can assign this block to.

</td></tr><tr><td>

End number

</td><td>

Ending phone number of the series that you can assign to this block to.

</td></tr></tbody>
</table>    To learn about the other fields, see [Inventory number allocation fields](../reference/inventory-number-allocation-fields.md).

5.  Add the attachments, such as the graphics or documents, by selecting the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

6.  Select **Save**.

    The related tabs appear on the form. You can view or change the related tab information. To learn more about the related tabs, see [Related tabs in the network inventory forms](../reference/inventory-related-tab.md).

    **Note:** Based on the assigned or allocated telephone numbers, the existing allocation divides into separate allocations. For example, in a series of 1-100, if 1-10 and 90–100 are assigned, then the 1–100 allocation divides into three allocations. The three allocations, 1–10 and 90–100 with availability as No and 11–89 as Yes are created.


**Parent Topic:**[Create a telephone infrastructure](../concept/telephone_block_telephone_number_and_telephone_number.md)

