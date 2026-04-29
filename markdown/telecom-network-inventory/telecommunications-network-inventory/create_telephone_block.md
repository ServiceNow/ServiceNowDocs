---
title: Create a telephone block
description: Created topic for STRY55294083 - DOC1071773Create a telephone block to organize and categorize all sequential telephone numbers that are within an area by using the Telecommunications Network Inventory application.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a telephone infrastructure, Inventory number allocation, Define inventory records, Use, Telecommunications Network Inventory]
---

# Create a telephone block

Create a telephone block to organize and categorize all sequential telephone numbers that are within an area by using the Telecommunications Network Inventory application.

## Before you begin

-   Ensure that the Telecommunications Network Inventory application includes all the required components of your telephone number. To learn more, see [Create the components of a telephone number](../concept/create_components_of_a_telephone_number.md).
-   Role required: sn\_inv\_num\_mgmt.inventory\_number\_manager

## About this task

You can create multiple telephone number allocations and telephone numbers for one telephone block. Also, you can also review, create, update, or delete a telephone block.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory Number Allocation** &gt; **Telephone Blocks**.

3.  Select **New**.

    **Note:** You can create and allocate telephone numbers without using a block for the port-in numbers or for the numbers that don’t want a block.

4.  On the form, fill in the fields.

<table id="table_mzv_1nt_mxb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create telephone allocation and numbers

</td><td>

By default, the field is set as true. The result is that the individual telephone numbers and telephone number allocations are created using the provided from and to number. When you clear this check box, only a telephone block is created.**Note:**

1.  The created number of allocations and the telephone numbers are shown as available to allocate.
2.  By default, the status of the created numbers is set as new.


</td></tr><tr><td>

From number

</td><td>

Starting number of the series from where you want to start adding numbers to this block.

</td></tr><tr><td>

To number

</td><td>

Last number of the series where you want to stop adding numbers to this block.**Note:** The same or overlapping series of numbers aren’t enabled to include in a block. For example, if a block 100–200 exists, then the new block of 150-200 or 100–200 can’t be enabled.

</td></tr></tbody>
</table>    To learn about the other fields, see [Inventory number allocation fields](../reference/inventory-number-allocation-fields.md).

5.  Add the attachments, such as the graphics or documents, by selecting the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

6.  Select **Submit**.

    Depending on the details that you provided, a telephone block is created.

7.  On the **Details** tab, under telephone block form, fill in the additional fields.

<table id="table_ufm_mbt_vxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Quantity

</td><td>

Number of telephone numbers that are in the selected telephone number blocks.**Note:** This field is auto-populated after creating a telephone block. However, you can always update this field as required.

</td></tr><tr><td>

Available quantity

</td><td>

Number of telephone numbers that aren’t assigned or available.**Note:** This field is auto-populated after creating a telephone block. However, you can always update this field as required.

</td></tr></tbody>
</table>    To learn about the remaining identification fields that are common to most of the Inventory and Inventory number allocation menu forms, see [Commonly used network asset instance identification fields](../reference/commonly-used-tni-identification-fields.md).

8.  Select **Save**.

9.  On the related tabs, view or update the related tab information.

    To learn more about the related tabs, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).

10. View the related network inventories by selecting the brick icon \(![Infrastructure relationship icon.](../image/infrastructure-relashionship.png)\).

    The Infrastructure Relationships section shows all the related network inventories that are grouped by the network instances.


## What to do next

You can review and update the fields, create a related tab record, or delete a record. To learn more, see [Update or delete a record of an inventory number allocation](update_and_delete_ip_address_space.md).

**Parent Topic:**[Create a telephone infrastructure](../concept/telephone_block_telephone_number_and_telephone_number.md)

