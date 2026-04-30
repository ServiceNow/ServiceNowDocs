---
title: Create averages for product life cycles in Software Asset Management classic
description: Create averages to calculate software End of Life \(EOL\) and End of Support \(EOS\) life cycles in the Software Asset Management classic application.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# Create averages for product life cycles in Software Asset Management classic

Create averages to calculate software End of Life \(EOL\) and End of Support \(EOS\) life cycles in the Software Asset Management classic application.

## Before you begin

Role required: model\_manager

## About this task

You can create averages that can be used globally for all products and publishers or you can create averages specific to a product or a publisher. These averages are used to create calculated life cycles for products. For details on calculated life cycles, see [End of Life \(EOL\) and End of Support \(EOS\) life cycles](../concept/calculated-lifecycles.md).

## Procedure

1.  Navigate to **Software asset** &gt; **Software lifecycle averages**.

2.  Select **New** to open the Software lifecycle averages page.

3.  On the form, fill in the fields.

<table id="table_e4b_qcn_crb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

The type of option you select for creating life cycles. Choose from the following options:-   **Custom industry average**: Refers to the industry averages based on the GA dates.
-   **Product**: Refers to a specific product. This includes custom products too.
-   **Publisher**: Refers to a specific publisher. This includes custom publishers too.


</td></tr><tr><td>

Display name

</td><td>

A unique name for this life cycle average record.

</td></tr><tr><td>

Product

</td><td>

his field appears only if you select the value **Product** in the **Type** field

</td></tr><tr><td>

Publisher

</td><td>

This field is automatically populated once you select a product. If you selected the value **Publisher** in the **Type** field, then you select a publisher.

</td></tr><tr><td>

Domain

</td><td>

Indicates the domain in which your instance is located.

</td></tr><tr><td>

Average end of life period \(months\)

</td><td>

Specify the number of months for the EOL life cycle.

</td></tr><tr><td>

Average end of support period \(months\)

</td><td>

Specify the number of months for the EOS life cycle.

</td></tr><tr><td>

Active

</td><td>

Indicates that the life cycle average record will be used for creating software life cycles.

</td></tr></tbody>
</table>4.  Select **Submit**.

    The record is created and appears in the Software lifecycle averages list view.


**Parent Topic:**[Using Software Asset Management classic](../concept/using-sam-classic.md)

