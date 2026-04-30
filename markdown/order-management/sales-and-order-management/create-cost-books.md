---
title: Create and publish a cost book
description: Create a cost book that defines the unit costs for products and services in Sales Customer Relationship Management.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Pricing Management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create and publish a cost book

Create a cost book that defines the unit costs for products and services in Sales Customer Relationship Management.

## Before you begin

Role required: sn\_csm\_pricing\_pricelist\_administrator, sn\_csm\_pricing\_pricelist\_manager

## About this task

You can create cost books that define the unit costs for a set of products and a specified currency. However, only one cost book per given currency is allowed.

You can create multiple cost books for a given currency, but the first cost book that you create for a particular currency is automatically set as the default cost book. If you don’t want the first cost book as the default, deselect the **Default** option. When you're creating a default cost book, the start date must be either the current date or a date earlier than the current date.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![image.Lists] view.

2.  Navigate to **Prices** &gt; **Cost Books**.

3.  In the Prices - Cost Books list, select **New**.

4.  In the Details tab, fill in the fields.

<table id="table_xvx_p4x_w1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique system-assigned number that identifies the cost book.

</td></tr><tr><td>

Name

</td><td>

Name of the cost book, for example Standard Cost Book.

</td></tr><tr><td>

Code

</td><td>

System-generated alphanumeric number based on the cost book name. Although the code is system-generated, you can edit it to represent an industry-specific code.

</td></tr><tr><td>

Currency

</td><td>

Currency of the cost book, for example USD for US dollars.

</td></tr><tr><td>

Default

</td><td>

Option for setting this cost book as the default cost book with the specified **Currency**.

</td></tr><tr><td>

Description

</td><td>

Brief description of the cost book.

</td></tr><tr><td>

State

</td><td>

Stage of the cost book:-   Draft: Initial state of the cost book. Information is still being added to the cost book and hasn’t been published to the catalog yet.
-   Published: Cost book has been published to the catalog. After a cost book is published, you can update, delete, retire, or archive it.
-   Retired: Cost book has been retired and is no longer active. The cost book and its cost book lines can't be updated.
-   Archived: Cost book has been archived and is no longer available for use.
**Note:** A default cost book can’t be deleted, retired, or archived.

</td></tr><tr><td>

Start date

</td><td>

Starting date and time that the cost book is effective. Select the Calendar icon ![](../image/field-calendar.png) to choose the start date and time, then select **OK**. **Note:** If this date is for a default cost book, the start date must be either the current date or a date that is earlier than the current date.

</td></tr><tr><td>

End date

</td><td>

Ending date and time of the cost book. After the ending time, the cost book is no longer active. Select the Calendar ![](../image/field-calendar.png) icon to choose the end date and time, then select **OK**.**Note:** If this date is for a default cost book, the end date is ignored.

</td></tr></tbody>
</table>5.  Select **Save**.

    The cost book is in the Draft state.

    **Note:** You can continue by defining cost book lines when the cost book is in Draft state. However, you must publish the cost book to apply the cost book and its cost book lines.

6.  Select **Publish**.

    The state changes to Published. The Cost Book Lines tab opens for creating a cost book list line.


## What to do next

[Create a cost book line](create-cost-book-lines.md).

