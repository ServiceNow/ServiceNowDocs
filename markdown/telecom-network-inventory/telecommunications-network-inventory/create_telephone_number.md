---
title: Create a telephone number to an area or region
description: Created topic for STRY55294083 - DOC1071773Create a telephone number to add that number to an area or to a region by using the Telecommunications Network Inventory application. You can review, create, update, or delete a telephone number.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a telephone infrastructure, Inventory number allocation, Define inventory records, Use, Telecommunications Network Inventory]
---

# Create a telephone number to an area or region

Create a telephone number to add that number to an area or to a region by using the Telecommunications Network Inventory application. You can review, create, update, or delete a telephone number.

## Before you begin

-   Ensure that the Telecommunications Network Inventory application includes all the required components of your telephone number. Otherwise, see [Create the components of a telephone number](../concept/create_components_of_a_telephone_number.md).
-   Role required: sn\_inv\_num\_mgmt.inventory\_number\_manager

## About this task

Setting the Create telephone allocations and numbers checkbox as true, while creating a telephone block, creates individual numbers and telephone allocation. You can also add a telephone number to a telephone number allocation.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory Number Allocation** &gt; **Telephone Numbers**.

3.  Select **New**

4.  On the **Details** tab, in the telephone number section, fill in the fields.

<table id="table_v4g_qcq_mxb"><thead><tr><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Switch CLLI

</td><td>

A reference to any Configuration Item but is ideally recommended to telco equipment.

</td></tr><tr><td>

Line number

</td><td>

Portion of a telephone number that uniquely identifies an individual telephone line within an area. You can provide a series or individual line numbers in an xxxx-xxxx or xxxx, xxxx-xxxx format.

 **Note:** If the provided line number isn’t in a series of numbers, multiple number allocations are created.

</td></tr></tbody>
</table>    To learn about the other fields, see [Inventory number allocation fields](../reference/inventory-number-allocation-fields.md).

5.  Add the attachments, such as the graphics or documents, by selecting the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

6.  Select **Save**.

    A telephone number is created with an area code, central office code, status of the number, switch CLLI, line number, and telephone number.


## What to do next

You can review and update the fields, create a related tab record, or delete a record. To learn more, see [Update or delete a record of an inventory number allocation](update_and_delete_ip_address_space.md).

**Parent Topic:**[Create a telephone infrastructure](../concept/telephone_block_telephone_number_and_telephone_number.md)

