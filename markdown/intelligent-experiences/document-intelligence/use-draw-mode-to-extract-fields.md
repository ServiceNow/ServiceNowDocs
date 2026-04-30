---
title: Extract fields using the draw tool
description: Use the draw tool to extract information directly from text and tables on the document image.Use the draw tool to extract a single field directly from the document image.Use the draw tool to extract a table directly from the document image.Adjust the draw tool grid to better fit the information that you want to extract from the document image.Use the draw tool to review auto-filled fields directly from the document image panel.Edit the fields on the document image to make sure that the correct information is extracted.
locale: en-US
release: xanadu
product: Document Intelligence
classification: document-intelligence
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Complete a document task, Using Document Intelligence, Document Intelligence, Enable AI experiences]
---

# Extract fields using the draw tool

Use the draw tool to extract information directly from text andtables on the document image.

## Overview of the draw tool

When viewing a processed document in the Document Intelligence workspace, you can use the draw tool to extract and review fields from the document image.

Especially in cases when there are no recommendations yet or incorrect recommendations, the draw tool is useful for selecting the specific area on the document you want to extract.

Any extracted table fields should already appear in a grid over the table. An extracted single field appears as a labeled box over the text.You can review the extracted fields right from the grid or boxand make adjustments as needed. If the table fields are empty or there is no grid, you can create one or more grids over the table to extract the fields.

![Draw tool creates a grid over the table on the document image.](../image/docintel-drawtool-overview2.gif)

## Extract a single field using the draw tool

Use the draw tool to extract a single field directly from the document image.

### Before you begin

Role required: sn\_docintel.extraction\_agent

### About this task

Use the following steps to extract a single field from a document using the draw tool. The extracted data is used to fill the related field in the document fields panel.

If the field is auto-filled, a box already appears over the extracted text. You can adjust the field as needed.

### Procedure

1.  In the document fields panel, expand **Fields**.

2.  Select a field.

    The Draw Tool icon \(![Draw Tool icon.](../image/icon-docintel-draw-mode2.png)\) is enabled in the document controls toolbar.

    If the field is already auto-filled and the box appears over the field, or if you’ve already drawn a box, proceed to step 5.

3.  Select the Draw Tool icon \(![Draw Tool icon.](../image/icon-docintel-draw-mode2.png)\).

4.  Draw a box over the area on the document image that you want to extract.

    An editable box appears over the text. The field name is displayed next to the box. The extracted text in the box appears highlighted.

    ![Box drawn on the document to extract the date field value.](../image/docintel-dm-single-field-example.png "Box drawn on a single field")

    The extracted text fills the related field in the document fields panel.

    **Tip:** Press **Enter** or **Return** in the filled field to move to the next field and draw a new box.

5.  Adjust the box as needed.

<table id="choicetable_kws_nrj_4bc"><thead><tr><th align="left" id="d70773e210">

Option

</th><th align="left" id="d70773e213">

Description

</th></tr></thead><tbody><tr><td id="d70773e219">

**Resize the box**

</td><td>

Select the box. Drag the box edge or corner to the desired position.

 The updated text in the box is extracted and fills the related field in the document fields panel.

</td></tr><tr><td id="d70773e234">

**Remove the box**

</td><td>

Select the Remove the box icon \(![Remove the box icon](../image/icon-docintel-delete-grid.png)\).

 The box is deleted and the extracted value is removed from the field.

</td></tr><tr><td id="d70773e255">

**Extract to a different field**

</td><td>

Select the field name next to the box and choose another option from the list.

</td></tr></tbody>
</table>6.  Edit the extracted text by entering the changes in the field.

    DocIntel may not detect all the text within the selected area. In this case, you may need to enter the information directly in the field.


## Extract a table using the draw tool

Use the draw tool to extract a table directly from the document image.

### Before you begin

Role required: sn\_docintel.extraction\_agent

### About this task

Use the following steps to extract a table from a document using the draw tool. The extracted data is used to fill the related table fields.

If the table fields are auto-filled, a draw tool grid is already available based on the extracted fields. You can adjust the fields as needed. For more information, see [Adjust the draw tool grid](use-draw-mode-to-extract-fields.md#).

You can select multiple sections of a table throughout the pages of a document.

### Procedure

1.  In the document fields panel, expand the Tables section.

    The Tables section only displays fields assigned to a table [field group](../task/manage-keys.md).

2.  Select a table in the Tables section.

    The table panel is displayed, and the Draw Toolicon \(![Draw Tool icon.](../image/icon-docintel-draw-mode2.png)\) is enabled in the document controls toolbar.

    If the table fields are already auto-filled and the grid appears over the table, or if you’ve already drawn a grid, proceed to step 5.

    **Tip:** Collapse the Table panel using the Collapse table panel icon \(![Collapse table panel icon](../image/icon-docintel-collapse-table.png)\), if needed.

3.  Select the Draw Toolicon \(![Draw Tool icon.](../image/icon-docintel-draw-mode2.png)\).

4.  Draw a box over the area on the document image that you want to extract.

    **Tip:** Include the header row of the table in the selection area.

    An editable grid appears over the table. The grid defines the table cells in the area that you selected. The row numbers in the grid correspond to the rows in the Table panel.

    The text in the cell appears surrounded by a dotted-line box before it is extracted to the table fields. After it is extracted, it appears in a solid-line box.

    ![Draw tool grid displayed over a table on the document image.](../image/docintel-drawmode-grid.png)

5.  Adjust the grid as needed.

    For more information, see [Adjust the draw tool grid](use-draw-mode-to-extract-fields.md#).

6.  To select another section of the table on the same or a different page of the document:

    1.  Select the Draw Toolicon \(![Draw Tool icon.](../image/icon-docintel-draw-mode2.png)\).

    2.  Draw a box over the other area on the document image that you want to extract.

        **Note:** It isn’t possible to draw a new grid over an existing one.

        The grid number beside the table name shows the updated grid number. For example, “Line items \(2/2\)” shows you are in the second out of two grids used to extract the Line items table fields.

    3.  Adjust the grid as needed.

7.  To hide the grid\(s\), select the Hide/show the grid\(s\) icon \(![Hide/show the grids icon.](../image/icon-docintel-hide-grids.png)\).

    A partly-transparent box shows where a hidden grid is located on the document.

    Select the hidden grid or the Hide/show the grid\(s\) icon to show the grid.

8.  Extract the data.

    -   Select **Extract data**.

        This button displays if no data has been extracted yet.

    -   Select **Update fields**.

        This button displays if the table fields are already filled and you have made changes that will overwrite some of them.

        The **Update fields** button shows the number of fields to be updated.

    The data in the grid\(s\) are extracted and used to fill the related table fields.

    If there are any empty cells or missing columns in the grid\(s\), the related table fields are set to **Missing in the document**.


## Adjust the draw tool grid

Adjust the draw tool grid to better fit the information that you want to extract from the document image.

### Before you begin

-   These steps apply to tables that have a draw tool grid on the document image. For more information, see [Extract a table using the draw tool](use-draw-mode-to-extract-fields.md#).
-   Role required: sn\_docintel.extraction\_agent

### About this task

Use the following steps to make changes to a grid. You can then extract the updates to the related table fields.

### Procedure

1.  On the document image, select the grid that you want to change.

    If you have more than one grid on the document, only one displays editing tools. The other grid appears as an overlay until you select it for editing.

    ![Tools to adjust the draw-mode grid.](../image/docintel-drawtool-adjustments.png)

2.  Adjust the grid as needed.

    Adjustments are auto-saved.

    Any adjustments that produce a change to previous extractions are indicated in the cell corner.

    The text in the cell appears surrounded by a solid-line box if it’s already extracted. It appears in a dotted-line box if it isn’t extracted yet.

<table id="choicetable_jmr_csy_11c"><thead><tr><th align="left" id="d70773e675">

Option

</th><th align="left" id="d70773e678">

Description

</th></tr></thead><tbody><tr><td id="d70773e684">

**Move the grid**

</td><td>

Drag the Move icon \(![Move icon.](../image/icon-docintel-dm-move-table.png)\) to the desired position.

</td></tr><tr><td id="d70773e702">

**Change a column header**

</td><td>

Select the column header and select the column where the data will be extracted to in the table fields.

</td></tr><tr><td id="d70773e714">

**Make the first row a header row**

</td><td>

Select the row header and check the **This is a header row** check box.

</td></tr><tr><td id="d70773e729">

**Move a column or row border**

</td><td>

Drag the border to the desired position.

</td></tr><tr><td id="d70773e742">

**Add a new column or row**

</td><td>

Go to the outside border of the grid and select the Add a line icon \(![Add a line icon.](../image/icon-docintel-add-grid-line.png)\).

 Adding a line splits the affected cells so they can be extracted to separate fields.

</td></tr><tr><td id="d70773e763">

**Remove a column or row border**

</td><td>

Select the Remove a line icon \(![Remove a line icon.](../image/icon-docintel-delete-grid-line.png)\) at the end of the border outside the grid.

 Removing a line merges the affected cells so they can be extracted to the same fields.

</td></tr><tr><td id="d70773e784">

**Remove the grid**

</td><td>

Select the Remove the grid icon \(![Remove the grid icon](../image/icon-docintel-delete-grid.png)\).

 This action only removes the grid, not the extracted data.

</td></tr><tr><td id="d70773e805">

**Ignore a table column or row**

</td><td>

1.  Select the column or row heading.
2.  Select the **Do not extract this column/row** check box.
3.  Select **Save**.


</td></tr></tbody>
</table>
## Review a field on the document image

Use the draw tool to review auto-filled fields directly from the document image panel.

### Before you begin

-   These steps apply to tables that have a draw tool grid or single fields that have a draw tool boxon the document. For more information, see [Extract a table using the draw tool](use-draw-mode-to-extract-fields.md#)or [Extract a single field using the draw tool](use-draw-mode-to-extract-fields.md#).
-   Role required: sn\_docintel.extraction\_agent

### Procedure

1.  On the document image, point to a grid cell or field boxyou want to review.

    For a single field, an editable box appears over the text. The field name is displayed next to the box.

    ![Single field on the document image.](../image/docintel-dm-single-field.png)

    For a table field, the text in the grid cell appears surrounded by a box if the value is extracted.

    ![Tooltip showing the extracted field value.](../image/docintel-drawtool-cell-tooltip.png)

2.  Verify the value that appears in the field’s tooltip.

    -   If the value is accurate, move on to review the next field.
    -   If the value must be changed, edit the field.

        See [Edit a field on the document image](use-draw-mode-to-extract-fields.md#).

3.  Repeat steps 1 and 2 for each field that you want to review.


## Edit a field on the document image

Edit the fields on the document image to make sure that the correct information is extracted.

### Before you begin

-   These steps apply to tables that have a draw tool grid or single fields that have a draw tool boxon the document. For more information, see [Extract a table using the draw tool](use-draw-mode-to-extract-fields.md#)or [Extract a single field using the draw tool](use-draw-mode-to-extract-fields.md#).
-   Role required: sn\_docintel.extraction\_agent

### About this task

Use the following steps to change to a field by editing the recommendation on the document image. The text detected by DocIntel appears surrounded by a box.

### Procedure

1.  On the document image, select the text box or thegrid cell that you want to edit.

    A dialog box appears, showing the related field.

2.  Enter a value in the text box or select another recommendation from the list.

    ![Dialog box for the table field opened from the document image.](../image/docintel-edit-dm-field-in-doc2.png)

3.  Select **Save**.


