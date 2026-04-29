---
title: Add a table to an HTML editor
description: Add and format an example table to a knowledge article using HTML field controls.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Table functions in HTML field editor, Configure the HTML toolbar, Configure a field editor for the HTML field, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Add a table to an HTML editor

Add and format an example table to a knowledge article using HTML field controls.

## Before you begin

Role required: admin

## About this task

In this task, you create and format a table in either htmlArea or TinyMCE v6.8.3. The resulting tables should look similar to one of the following images.

![Table example html](../image/TableExampleHTML.png "Table example in htmlArea")

![TinyMCE v6.8.3 Table example](../image/TinyMCEV6-table-example.png "Table example in TinyMCE v6.8.3")

If you enter alternative values for aspects such as width, cell spacing, cell padding, border, and alignment, the resulting table varies from the examples given.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Edit** and select the knowledge article that you want to edit.

2.  In the HTML field, position the cursor at the location where you want to add the table.

3.  Select the table icon, select **Insert table**, and then select the number of rows and columns.

4.  Edit the table properties.

    1.  Position your cursor in the table, select the table icon, and select **Table properties**.

    2.  Enter the following values on the **General** tab.

        -   Width: 75%
        -   Cell spacing: 3
        -   Cell padding: 3
        -   Border: 1
        -   Alignment: Left
    3.  On the **Advanced** tab, select the text field next to **Border color** and enter `Gray`.

        The color picker box turns gray to indicate the color that you entered. You can also select the box and select the colors in the palette.

    4.  Select **Ok**.

5.  Update the header table row.

    1.  Select the cells in the first table row, select the table icon, and select **Row** &gt; **Row properties**.

    2.  Enter the following values on the **General** tab.

        -   Row type: Header
        -   Alignment: Center
    3.  On the **Advanced tab**, enter `#87cefa` in the text box beside **Background color** to set it to a light blue.

    4.  Select **Ok**.

6.  Set the table cell properties.

    1.  Select all table cells in the first column except the cells in the header row.

    2.  Select the table icon and select **Cell** &gt; **Cell properties**.

    3.  Enter the following values on the **General** tab:

        -   H Align: Left
        -   V Align: Top
    4.  Select **Ok**.

    5.  Repeat these steps for the table cells in the second column.

7.  Set the background color of the middle row.

    1.  Position your cursor in the middle table row, select the table icon, and select **Row** &gt; **Row properties**.

    2.  On the **Advanced tab**, enter `Silver` in the text box beside **Background color** to set it to color \#c0c0c0.

    3.  Select **Ok**.

    4.  Repeat this procedure for every other table row.

8.  Set the width of the columns.

    1.  Select the first column of the table, select the table icon, and select **Cell** &gt; **Cell properties**.

    2.  On the **General** tab, enter `30%` in the **Width** text field.

    3.  Select **Ok**.

9.  Select and hold \(or right-click\) the form header and select **Save**.

10. Enter data in the table cells and then save the article.


