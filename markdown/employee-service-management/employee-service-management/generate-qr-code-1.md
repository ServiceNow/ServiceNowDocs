---
title: Generate and print QR code for a space or room
description: Generate and print a QR code for a single space or room, or for multiple spaces or rooms. Employees can scan the QR code to view their reservation details using the Now Mobile app.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Generate and print QR code for a space or room

Generate and print a QR code for a single space or room, or for multiple spaces or rooms. Employees can scan the QR code to view their reservation details using the Now Mobile app.

## Before you begin

[Enable mobile universal linking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/universal-linking-enable.md)

Role required: sn\_wsd\_core.admin or sn\_wsd\_core.workplace\_manager

## Procedure

1.  Navigate to **Workplace Core** &gt; **QR code management** &gt; **Create QR codes**.

    If needed, other possible navigation options include the following:

    -   Navigate to **Workplace Core** &gt; **QR code management** &gt; **Manage QR codes** and click **New**.
    -   Navigate to **Workplace Core** &gt; **Administration** &gt; **Space type configuration**.

        Select a space type for which you want to generate and print QR code and click **Create QR codes**.

    -   For rooms, navigate to **Workplace Core** &gt; **Space Administration** &gt; **Rooms**.

        Select a room and click **Create QR code**.

    -   For spaces, navigate to **Workplace Core** &gt; **Space Administration** &gt; **Spaces**.

        Select a space and click **Create QR code**.

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
</table>3.  Click **Submit**.

4.  To print the QR code, click **Print QR codes**.

5.  In the Print QR codes dialog box, do the following:

    1.  Specify a file name for the printed QR code in the **Enter file name** field.

        All the QR codes of the selected spaces are in a single PDF file with the specified file name.

    2.  View the number of QR codes to be printed in the **Count** field.

    3.  Select the layout of the QR code in the **Label layout** field.

    4.  Preview the QR code print.

    5.  Click **Print**.

        The QR code generation runs in the background.


## Result

The QR codes are generated. The QR codes are printed in a single PDF file with the specified file name. You will receive an email notification after the QR code generation is completed with the QR code details.

## What to do next

After the QR code generation is completed, go to **Manage QR codes** to view the generated file. For more information, refer to [Manage QR codes](manage-qr-codes.md).

Click **download** to download the PDF file.

**Parent Topic:**[QR code management](../concept/qr-code-mgmt.md)

