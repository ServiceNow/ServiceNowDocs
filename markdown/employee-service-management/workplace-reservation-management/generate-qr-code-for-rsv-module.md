---
title: Generate and print a QR code for a reservable module
description: Generate and print a QR code for an entire reservable module. Place the QR codes at reservable workplace locations so that employees can scan the code, make a reservation, or perform reservation-related actions.
locale: en-US
release: zurich
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure a reservable module, Configure, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Generate and print a QR code for a reservable module

Generate and print a QR code for an entire reservable module. Place the QR codes at reservable workplace locations so that employees can scan the code, make a reservation, or perform reservation-related actions.

## Before you begin

Role required: sn\_wsd\_core.workplace\_manager, sn\_wsd\_rsv.admin, or sn\_wsd\_rsv.manager

## About this task

Generate and print QR code for a reservable module such as Desks, Meeting rooms, Parking and more. For example, when you generate and print a QR code for Parking reservable module, then the generated QR code can be used for all the locations that are assigned to Parking reservable module. You can download the QR code, print and place it at all the locations that belong to the Parking reservable module.

## Procedure

1.  To generate a QR code, do the following:

    1.  Generate QR code using the following navigation paths:

        You can generate QR code using any of the following navigation paths:

        -   Navigate to **Workplace Core** &gt; **QR code management** &gt; **Create QR codes**.
        -   Navigate to **Workplace Core** &gt; **Space Administration** &gt; **Rooms**. Select a room and click **Create QR code**.
        -   Navigate to **Workplace Core** &gt; **Space Administration** &gt; **Spaces**. Select a space and click **Create QR code**.
2.  On the form, fill in the fields.

<table id="table_ln1_ftl_prb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number of the QR code.

</td></tr><tr><td>

Table

</td><td>

Table for which you want to add a QR code. By default, the table is set a as **Space \[sn\_wsd\_core\_space\]**.

</td></tr><tr><td>

State

</td><td>

Status of the QR code generation.

</td></tr><tr><td>

Short description

</td><td>

Description about the QR code.

</td></tr><tr><td>

Conditions

</td><td>

Filter conditions based on which the QR code must be generated.-   To add a condition, select**Add Filter Condition**.
-   To add an OR condition, select **Add "OR" Clause**.


</td></tr></tbody>
</table>3.  To print the QR code, click **Print QR codes**.

4.  In the Print QR codes dialog box, do the following:

    1.  Specify a file name for the printed QR code in the **Enter file name** field.

        All the QR codes of the selected spaces are in a single PDF file with the specified file name.

    2.  View the number of QR codes to be printed in the **Count** field.

    3.  Select the layout of the QR code in the **Label layout** field.

    4.  Preview the QR code print.

    5.  Click **Print**.

        The QR code generation runs in the background.


## What to do next

The QR codes are generated. The QR codes are printed in a single PDF file with the specified file name. You will receive an email notification after the QR code generation is completed with the QR code details.

After the QR code generation is completed, go to **Manage QR codes** to view the generated file. For more information, refer to [Manage QR codes](../../workplace-service-delivery/task/manage-qr-codes.md).

Click **download** to download the PDF file.

**Parent Topic:**[Configure a reservable module](config-reservable-module.md)

