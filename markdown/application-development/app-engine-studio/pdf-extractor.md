---
title: Use a PDF to create data tables
description: Create tables from a PDF form using the PDF extractor tool in App Engine Studio.Add data tables to your application by uploading a PDF in App Engine Studio.Add field columns to your data table using the PDF extractor in App Engine Studio.Move fields into a new referenced data table using the PDF extractor in App Engine Studio.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Create a data model, Enhance your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Use a PDF to create data tables

Create tables from a PDF form using the PDF extractor tool in App Engine Studio.

**Note:** This feature is only available if your licensing entitles you to "exclusive low code capability" and you have Table Builder for App Engine installed. Contact your Solutions consultant for more information.

## Overview of creating tables from PDFs

The PDF extractor in App Engine Studio allows you to upload a PDF and then extract table fields for use in a custom app. This streamlines the process of building application data tables from pre-existing PDF forms because you no longer need to manually type in field labels.

**Note:** Ensure that you are mindful about recreating any tables that may already exist on the ServiceNow AI Platform. For example, with a PDF containing user demographic data, determine whether you want to reference existing user data tables rather than creating new tables from the PDF.

## General navigation

The following table contains a list of some of the other basic navigational elements within the PDF extractor tool.

<table id="id_e5n_j24_hvb"><thead><tr><th>

Navigational element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Collapse / expand icons\(![Collapse or expand pane icons.](../image/pdf-collapse-pdf-pane.png)\)

</td><td>

Select these icons to toggle between collapsing or expanding the PDF and table panes.

</td></tr><tr><td>

Page controls\(![PDF page controls icon.](../image/pdf-page-controls-icon.png)\)

</td><td>

Use the arrows at the bottom of the PDF to page through the document one page at a time or navigate directly to the beginning or end of the document.

</td></tr><tr><td>

Zoom controls\(![PDF zoom controls.](../image/pdf-zoom-controls.png)\)

</td><td>

Use the zoom controls to zoom in or out in the PDF.

</td></tr><tr><td>

Add new field icon\(![Add new field icon.](../image/pdf-add-new-field.png)\)

</td><td id="entry_pdf-add-new-field">

Add a field column to your table manually by selecting **+Add new field**, and then enter details directly. This is similar to how you add fields on the **Data** tab of Table Builder.

</td></tr><tr><td>

Add reference table icon\(![Add reference table icon.](../image/pdf-add-reference-table.png)\)

</td><td>

Select **Add reference table** in the right side panel to add a reference field in your table that points to a new table.

</td></tr><tr><td>

Open data table and form icon\(![Open data table and form icon.](../image/pdf-open-table-and-form.png)\)

</td><td>

Select **Open data table and form** to open the selected table within Table Builder.

</td></tr><tr><td>

Table additional actions list \(![Additional actions menu](../image/pdf-ellipsis-menu.png)\)

</td><td id="entry_pdf-table-addl-actions">

Use the table additional actions menu to edit basic properties for your table, or if you have added a reference table, select **Delete** to delete the table.

</td></tr><tr><td>

Trash icon\(![Trash icon.](../image/pdf-trash-icon.png)\)

</td><td>

Select the **Trash icon** \( ![Trash icon.](../image/pdf-trash-icon.png)\) to delete fields from a table.

</td></tr></tbody>
</table>## PDF parsing limitations

The following limitations currently exist when uploading a PDF using this tool:

-   PDF cannot be converted from an image.
-   PDF cannot be longer than 25 pages.
-   PDF file size cannot exceed 5 MB.
-   Languages other than English and French are not currently supported.

**Parent Topic:**[Create a data model for your application](add-data.md)

## Create a table from a PDF form

Add data tables to your application by uploading a PDF in App Engine Studio.

### Before you begin

**Note:** This feature is only available if your licensing entitles you to "exclusive low code capability" and you have Table Builder for App Engine installed. Contact your Solutions consultant for more information.

Verify that the PDF meets the following requirements:

-   PDF cannot be converted from an image.
-   PDF cannot be longer than 25 pages.
-   PDF file size cannot exceed 5 MB.
-   Languages other than English and French are not currently supported.

Role required: admin, sn\_app\_eng\_studio.user, or delegated\_developer

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Next to the Data heading, select the Add icon \(![Add icon](../image/plus-icon.png)\).

4.  Select **Create a blank table**, and then select **Continue**.

5.  Select **Upload a PDF** and then select **Continue**.

6.  Select and upload the PDF.

    You can drag the PDF file onto App Engine Studio or browse your computer.

    **Note:** It may take a moment for the PDF to load. Select the trash icon \(![Trash icon.](../image/pdf-trash-icon.png)\) to clear the PDF selection.

    ![Choose the PDF you want to upload.](../image/pdf-to-table-upload.png "Choose the PDF you want to upload")

7.  Select **Continue**.

    **Note:** It may take up to a minute for the PDF to be parsed.

8.  Define the properties for your new table.

<table id="table_wkw_fpn_hvb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table label

</td><td>

Unique label to identify the table.

</td></tr><tr><td>

Table name

</td><td>

Database name for the table. A table name is created automatically after you enter a table label. Once this is created, this field is read only.

</td></tr><tr><td>

Make extensible

</td><td>

Option to allow other tables to share data from this table. For more information on table extension, see [Table extension](add-data.md#section_ebj_sdb_d5b).

</td></tr><tr><td>

Auto number

</td><td>

Option to track table records with a unique number. If you select this option, define the **Prefix**, **Starting number**, and **Number of digits**.

</td></tr><tr><td>

Prefix

</td><td>

Abbreviated name of the table to append to the beginning of the record number. For example, if you are creating a "Laptop" table, then your prefix may be "LPTP" or "LT."

</td></tr></tbody>
</table>9.  Select **Continue**.

    You may now configure permissions for your new data table.

10. Control who has access to create, read, write, and delete content from this table by adding new roles and/or defining the desired Create, Read, Write, Delete permissions for existing roles.

    Roles that you create in the table persist throughout the application and can be further defined in other tables you add. See [Add application security](add-security.md) for more information on how security permissions work.

    **Note:** At least one role must have read access for you to be able to preview the table.

11. Select **Continue** after you have configured table permissions.

12. Select **Go to PDF extractor** to open up the PDF in the PDF extractor.


### What to do next

Next, you will add fields from the uploaded PDF. Follow the steps in [Add new fields from a PDF form](pdf-extractor.md#) to populate your new data table with field columns.

## Add new fields from a PDF form

Add field columns to your data table using the PDF extractor in App Engine Studio.

### Before you begin

**Note:** This feature is only available if your licensing entitles you to "exclusive low code capability" and you have Table Builder for App Engine installed. Contact your Solutions consultant for more information.

Role required: admin, sn\_app\_eng\_studio.user, or delegated\_developer

### Procedure

1.  Choose one of the following options:

    -   Follow the steps outlined in the previous procedure to upload a PDF \(see [Create a table from a PDF form](pdf-extractor.md#)\).
    -   If you have already uploaded the PDF, select the **Open pdf extractor** element on the **Forms** or **Table** tab in Table Builder to launch the PDF extractor tool.
    The PDF form displays.

2.  Review the PDF.

    Use any of the navigational controls in the PDF pane to navigate to where you'd like to begin adding fields. See [General navigation](pdf-extractor.md#section_wkf_twk_gvb).

3.  Click **Select** to enter text selection mode.

4.  In the PDF, click on a field or text phrase to highlight it to use it as the basis for a new field.

    ![Add fields from PDF](../image/pdf-to-table-add-fields.png "Add fields from PDF")

5.  Edit the extracted text in the **Field Label** as needed for the new field you are going to add.

6.  Choose a **Field type**.

    Field type refers to the type of data that the new column will store. For example, to store plain text in the column, select **String**. To understand the basic field properties, see [Add and customize a field in a table](https://www.servicenow.com/docs/access?context=t_CreatingNewFields&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

    Depending on the type that you select, you may need to fill in additional fields to further define the table column. For example, with Reference field types, search for and select the appropriate data table to reference.

    1.  If you have chosen to create a choice field, perform the following actions to populate options for the choice field.

        1.  Choose a **Choice Type** from the menu. This controls whether or not the list will have None as an option.
        2.  Click in the **Choices** field, and then enter text manually or select text on the PDF to automatically extract it.
        3.  Click **Add** to add your choice to the list.
        ![Adding a choice field.](../image/pdf-add-choice-field.png "Adding a choice field")

    2.  Repeat the previous steps until all choices have been added for your choice field.

7.  Select the **Table** where you want to add the new field.

    Multiple options may appear if you have added reference tables. The original table is selected by default.

8.  Select **Add field** to add the field to the list of fields in the table on the right.

    **Note:** Any fields you add to the table on the right remain highlighted in green in the PDF to remind you that you have created a related field from them. If you delete a field from the tables on the right, the extracted text will no longer be highlighted.

9.  Repeat the steps above until you have added all the fields you want to add from the PDF.

    **Note:** You can also add fields manually by clicking **+Add new field** in the table on the right and entering details directly similar to how you add fields on the **Table** tab of Table Builder.

10. Review the fields in your table and edit as necessary.

<table id="id_lx3_xg4_hvb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Move fields between tables

</td><td>

To move a field between tables within the PDF extractor, change the selected **Table Name** to the desired table location.

</td></tr><tr><td>

Delete reference table

</td><td>

Delete any additional reference tables that you add by selecting **Delete** from the Additional actions list in the top right corner of the table \( ![Additional actions list.](../image/pdf-ellipsis-menu.png)\)

</td></tr><tr><td>

Add a new field

</td><td>

Add a field column to your table manually by selecting **+Add new field**, and then enter details directly. This is similar to how you add fields on the **Data** tab of Table Builder.

</td></tr><tr><td>

Edit a field

</td><td>

To edit field properties \(e.g., Field type\), click on the field property to select it, and then make your edits.

</td></tr><tr><td>

Delete a field

</td><td>

Select the **Trash icon** \( ![Trash icon.](../image/pdf-trash-icon.png)\) to delete fields from a table.

</td></tr><tr><td>

Open table within Table Builder

</td><td>

Select **Open data table and form** to open the selected table within Table Builder.

</td></tr></tbody>
</table>11. Select **Save**.


### What to do next

To open your data table in Table Builder, select **Open data table and form** above the displayed tables. For more information on editing your data tables in Table Builder, see [Table Builder](../../../administer/form-builder/concept/tb-landing-page.md).

To add a reference table, see [Add a reference table from a PDF form](pdf-extractor.md#).

## Add a reference table from a PDF form

Move fields into a new referenced data table using the PDF extractor in App Engine Studio.

### Before you begin

**Note:** This feature is only available if your licensing entitles you to "exclusive low code capability" and you have Table Builder for App Engine installed. Contact your Solutions consultant for more information.

Role required: admin, sn\_app\_eng\_studio.user, or delegated\_developer

### About this task

You may decide that you want to add some of the form information into separate tables that are referenced from the original table and can be referenced by other tables. For example, if you work for an insurance company, you may want to create separate data tables for bills, claims, and policies that can be referenced as separate data tables even though the information is extracted from a single PDF form.

You can add a reference field, and then create the corresponding reference data table directly from the PDF extractor in App Engine Studio.

**Note:** Before you create any new reference tables for your app, it's a good practice to verify that you are not accidentally recreating any tables that already exist on the ServiceNow AI Platform.

### Procedure

1.  Choose one of the following options:

    -   Follow the steps outlined in the previous procedure to upload a PDF \(see [Create a table from a PDF form](pdf-extractor.md#)\).
    -   If you have already uploaded the PDF, select the **Open pdf extractor** element on the **Forms** or **Table** tab in Table Builder to launch the PDF extractor tool.
    The PDF form displays.

2.  Select **Add reference table** in the right side panel to add a reference table to your table.

3.  Enter the following properties for your reference table.

    |Column header property|Description|
    |----------------------|-----------|
    |Table label|Unique label for the reference table.|
    |Table name|Database name for the reference table.|
    |Make extensible|Option to allow other tables to share data from this table. For more information on table extension, see [Table extension](add-data.md#section_ebj_sdb_d5b).|
    |Auto number|Option to track table records with a unique number. If you select this option, define the **Prefix**, **Starting number**, and **Number of digits**.|

    Next, you will add a reference field to the original table you are editing. This creates the connection between the tables \(e.g., "Seller info"\).

4.  Select the **Table label** of the table where you want to add your reference field in \(the original table is selected by default\).

    The original table should be selected by default in the **Table label** field.

5.  Enter a **Reference field label** for this new reference field \(e.g., "Seller information"\).

6.  Select fields from your original table to add them to your new reference table.

    These fields are related to the reference field you added to the current table.

    ![Add a reference table.](../image/pdf-to-table-add-reference-table.png "Add a reference table")

7.  Select **Add reference table**.

    The reference table appears below and contains the fields that you selected that were in the original table.

8.  Review and edit the fields and table properties as necessary.

<table id="id_lx3_xg4_hvb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Move fields between tables

</td><td>

To move a field between tables within the PDF extractor, change the selected **Table Name** to the desired table location.

</td></tr><tr><td>

Delete reference table

</td><td>

Delete any additional reference tables that you add by selecting **Delete** from the Additional actions list in the top right corner of the table \( ![Additional actions list.](../image/pdf-ellipsis-menu.png)\)

</td></tr><tr><td>

Add a new field

</td><td>

Add a field column to your table manually by selecting **+Add new field**, and then enter details directly. This is similar to how you add fields on the **Data** tab of Table Builder.

</td></tr><tr><td>

Edit a field

</td><td>

To edit field properties \(e.g., Field type\), click on the field property to select it, and then make your edits.

</td></tr><tr><td>

Delete a field

</td><td>

Select the **Trash icon** \( ![Trash icon.](../image/pdf-trash-icon.png)\) to delete fields from a table.

</td></tr><tr><td>

Open table within Table Builder

</td><td>

Select **Open data table and form** to open the selected table within Table Builder.

</td></tr></tbody>
</table>    See [General navigation](pdf-extractor.md#section_wkf_twk_gvb) for more information on additional navigational controls in the table pane.

9.  Select **Save**.


### What to do next

To open your data table in Table Builder, select **Open data table and form** above the displayed tables. For more information on editing your data tables in Table Builder, see [Table Builder](../../../administer/form-builder/concept/tb-landing-page.md).

