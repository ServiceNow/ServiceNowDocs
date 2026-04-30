---
title: Create a legal contract template of type HTML
description: Create a document template of type HTML.
locale: en-US
release: yokohama
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure legal contract of type HTML, Legal contract templates, Configure Legal Simple Contracts, Setting up Legal Simple Contracts, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Employee Service Management]
---

# Create a legal contract template of type HTML

Create a document template of type HTML.

## Before you begin

Role required: admin

## About this task

Legal contract templates help you to create and organize standard contract templates along with fillable metadata placeholders. You can create templates of HTML, PDF and Microsoft Word types. In an HTML document template type, you can map the inputs provided in the intake form to the fillable metadata placeholders.

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Simple Contracts Admin** &gt; **Contract Templates**.

2.  Select **New**.

3.  Select **HTML Document Template**

4.  On the form, fill in the fields.

<table id="table_nbm_c44_bhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the template.

</td></tr><tr><td>

Table

</td><td>

Name of the table that contains the fields to include in the document template.Select **General Contract Support \[sn\_lg\_ops\_general\_contract\_support\]**.

**Note:** Tables are shown depending on the selected application scope.

</td></tr><tr><td>

Contract type

</td><td>

Contract type to which the template is associated.

</td></tr><tr><td>

User criteria

</td><td>

User criteria to control which users can use the document.

</td></tr><tr><td>

Body

</td><td>

Content to include in the generated legal contract document.Insert columns from the selected table to the document template:

1.  Point the cursor to the desired location in the text editor.
2.  In **Select variables**, click the plus icon \(![Plus icon.](../image/plus_icon.png)\) beside **Fields**.
3.  From the fields list, select a column name.
 The selected column is added at the cursor position.

 **Note:** The variables from the legal intake form must be mapped to a column so that they can be used to populate the template.

</td></tr><tr><td>

Select variables

</td><td>

List of variables that can be used in the body of the template.Variables pull information from the selected table to customize the template.

</td></tr><tr><td class="sub-head" colspan="2">

Header tab

</td></tr><tr><td>

Header Image

</td><td>

Image file to use in the document header.

</td></tr><tr><td>

Header image height

</td><td>

Maximum height of the header image.

</td></tr><tr><td>

Header Position

</td><td>

Position of the image within the header.

</td></tr><tr><td class="sub-head" colspan="2">

Footer tab

</td></tr><tr><td>

Footer image

</td><td>

Image file to use in the document footer.

</td></tr><tr><td>

Footer image height

</td><td>

Maximum height of the footer image.

</td></tr><tr><td>

Footer image position

</td><td>

Position of the image within the footer.

</td></tr><tr><td>

Footer text

</td><td>

Text such as privacy and confidential statement to appear in the footer.

</td></tr><tr><td>

Footer text position

</td><td>

Position of the footer text within the footer.

</td></tr><tr><td>

Vertical alignment

</td><td>

Placement of the footer text relative to the footer image.

</td></tr><tr><td class="sub-head" colspan="2">

Page tab

</td></tr><tr><td>

Page size

</td><td>

Page size of the document.

</td></tr><tr><td>

Custom font

</td><td>

Font of the text on the page.

</td></tr><tr><td>

Top/Bottom margin

</td><td>

Margin to leave on the top and bottom sides of the page.

</td></tr><tr><td>

Left/Right margin

</td><td>

Margin to leave on the left and right sides of the page.

</td></tr></tbody>
</table>5.  Click **Insert Date** to insert a date at the cursor location in the template.

    You can insert multiple date types mapped to different date columns from the selected table such as start date, end date, or current date.

6.  Add a document template block to insert condition-based content on the generated document.

    1.  Point the cursor to the desired location in the text editor and click the **Add Blocks** button.

    2.  In the Add Blocks pane, search for a document template block.

    3.  Select a block to add to the template and click **Insert to Template**.

        The selected block is inserted at the selected point in the template.

    4.  Drag the inserted block to place it to another location in the template.

7.  Save the contract template.

    -   Save a contract template by clicking **Submit**.
    -   Save the changes to an existing contract template by clicking **Update**.
    The contract template is saved in the Draft state. The Participants related list appears.

8.  Add participants in the contract template.

    1.  In the Participants related list, click **New**.

    2.  In the **Name** field, enter the display name for the participant.

        For example, for an internal signatory, you could enter `Internal Signer 1`.

    3.  In the **Order** field, enter the order in which the signature request will be initiated for the participant.

    4.  In the **Signer** field, select a user field from the list of fields populated from the selected table.

        The user in the mapped field is automatically added as a signatory in the document.

    5.  In the **User** field, select the same field as in the **Signer** field.

    6.  Click **Submit**.

9.  Insert signatures in the contract template.

    1.  Place the cursor in the desired location in the **Body** field.

    2.  Select **Insert Signature** to insert signature variable for a participant.

    3.  In the Add a signature window, select a participant.

    4.  Click **OK**.

10. Insert signature date in the contract template.

    1.  Place the cursor in the desired location in the **Body** field.

    2.  Enter the code `${sign_date:<Participant Name>}` to insert signature date variable for a participant.

        For example: To capture the signature date for the participant Abel in the contract template, enter `${sign_date:Abel}`.

11. To make the template available for usage, click **Publish**.


