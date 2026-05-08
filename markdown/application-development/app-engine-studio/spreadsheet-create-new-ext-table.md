---
title: Create new table from extensible table and spreadsheet import
description: Create a new table by extending an existing table, and then using a Microsoft Excel spreadsheet import to update or customize it.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Use a spreadsheet, Create a data model, Enhance your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Create new table from extensible table and spreadsheet import

Create a new table by extending an existing table, and then using a Microsoft Excel spreadsheet import to update or customize it.

## Before you begin

-   Import a spreadsheet into App Engine Studio. See [Import a spreadsheet](spreadsheet-importing-spreadsheet.md).

Role required: admin, sn\_app\_eng\_studio.user, delegated developer permissions for "Integration" must be present to view data import and mapping options. For more information, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## Procedure

1.  After you have uploaded your spreadsheet as described in [Import a spreadsheet](spreadsheet-importing-spreadsheet.md), choose where to import your file in the displayed wizard.

    ![Import into a new data table.](../image/aes-spreadsheet-import-data.png "Import into a new data table")

    1.  Select **A new table**.

    2.  Choose **Create from an extensible table**.

2.  Select **Continue**.

3.  Search for an select an existing **Table** to add that table's data to your app and create an extension with branching logic.

    **Note:** Tables already in the app display first in the list and recommended ServiceNow AI Platform tables display next, along with a short description of the type of information the table stores.

4.  Select **Continue**.

5.  On the form, fill in the fields.

<table id="table_ac1_z5q_5mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table label

</td><td>

Unique label to identify the table.

</td></tr><tr><td>

Table name

</td><td>

Database name for the table. A table name is created automatically after you enter a table label. You can edit the name if needed.

</td></tr><tr><td>

Make extensible

</td><td>

Option to allow other tables to share data from this table. For more information on table extension, see [Table extension](../concept/add-data.md#section_ebj_sdb_d5b).

</td></tr><tr><td>

Auto number

</td><td>

Option to track table records with a unique number. If you select this option, define the **Prefix**, **Starting number**, and **Number of digits**.

</td></tr><tr><td>

Prefix

</td><td>

Abbreviated name of the table to append to the beginning of the record number. For example, if you are creating a "Laptop" table, then your prefix may be "LPTP" or "LT."

</td></tr><tr><td>

Starting number

</td><td>

Number to identify the first record created for your table.

</td></tr><tr><td>

Number of digits

</td><td>

Maximum number of digits to allow in the record number. This value determines the highest possible record number. For example, if you enter `7`, then the highest possible number is 9999999.

</td></tr></tbody>
</table>6.  Select **Continue**.

7.  Control who has access to create, read, write, and delete content from this table by adding new roles and/or defining the desired Create, Read, Write, Delete permissions for existing roles.

    Roles that you create in the table persist throughout the application and can be further defined in other tables you add. See [Add application security](../concept/add-security.md) for more information on how security permissions work.

    **Note:** At least one role must have read access for you to be able to preview the table.

8.  Select **Continue**.

    **Note:** Now your table is ready for data. In the next step, fields from your import are matched with fields on your newly extended table. You will have an opportunity to adjust mapping or create new fields from your import in it.

9.  Select **Continue** to proceed to mapping fields.

    A screen displays where you can map field columns from your source spreadsheet on the left to field columns in your newly extended target table that you just created on the right.

    ![Map imported fields.](../image/spreadsheet-map-fields.png "Map imported fields")

10. You have the following choices available to you during this step.

<table id="choicetable_ats_cqp_vvb"><tbody><tr><td id="d48292e379">

**Batch map fields using Automap**

</td><td>

Select **Automap** to automatically map your spreadsheet fields to displayed fields in the selected target table. Automap maps source entities to similarly named target entities. For a target entity that has already been mapped, selecting **Automap** doesn't change its value. An automapped field has a wand icon on its data pill.

</td></tr><tr><td id="d48292e394">

**Map fields by dragging and dropping**

</td><td>

Map fields from your import to your target table by dragging data pills representing columns in the imported spreadsheet to the **Value** column in the target table. You can also map fields by using the pill picker to the right of each target table field.

</td></tr><tr><td id="d48292e409">

**Map fields using the data picker**

</td><td>

Map data by using the pill picker \(![Pill picker.](../../../administer/integrationhub/images/pill-picker-green.png)\) on the right side of the target table. You can enter more than one value in the **Value** column, you can also enter text.

</td></tr><tr><td id="d48292e430">

**Add transform options**

</td><td>

Add transform options for each of the individual mapped spreadsheet fields by clicking the FX icon \( ![FX icon.](../../../administer/flow-designer/images/fx-icon.png)\) on the right side pane. For example, you can use the Uppercase transform function to change an input string to all uppercase characters. See [Transform functions](https://www.servicenow.com/docs/access?context=transform-functions&version=australia&pubname=australia-build-workflows&ft:locale=en-US) for information on how to use these to trim data for your imported spreadsheet fields.

**Note:** Not all the transform functions available in Flow Designer are available.

</td></tr><tr><td id="d48292e454">

**Activate data record matching**

</td><td>

Specify fields where the system should check for matching data and, if found, update existing records instead of creating new ones by enabling the **Match** toggle in your target table. For example, if a target table has an **Order number** field and a record with an order number of 743, there are two options for handling potential matches.

-   If the **Match** toggle switch for the **Order number** field is on, the system checks for matching data. If the source data has a record with the same order number, the system updates the existing record in the target table.
-   If the **Match** toggle switch for the **Order number** field is off, the system doesn't check for matching data. If the source data has a record with the same order number, the system creates a new record in the target table. In this case, the target table will have two records, both with an order number of 743.


</td></tr><tr><td id="d48292e493">

**Configure reference and choice field behavior**

</td><td>

Configure behavior for **Choice** and **Reference** field types.1.  Click the gear icon \(![Gear icon.](../../../administer/ui-builder/image/gear-icon.png)\).
2.  In **Field**, select the field column to match the incoming record value against in the target table.
3.  In **If no matching record exists then do the following**, specify what to do if that record isn't found in the target table.
    -   **Create a new choice/record:** Creates the choice or record in the target table's matching field column from the data imported for the field.
    -   **Ignore this field:** Ignores the field in the target table and leaves it null.
    -   **Skip this record:** Skips adding the entire record \(row\) in the target table.
4.  Click **Done**.


</td></tr><tr><td id="d48292e555">

**Add new field columns to target table**

</td><td>

Add unmapped field columns from your import to your target table or create new fields in your target table. 1.  Select **Add fields** above the target table on the right.
2.  Choose which fields to add to your target table by selecting the checkbox on the left or select **All** to choose all of them.
3.  You can also perform the following functions:
    -   Edit the **Field Label** for the imported field.
    -   Edit field properties for the imported field by selecting the **Edit icon** \(![Edit target table field properties.](../image/aes-add-field-edit-properties.png)\).
    -   Create a new field by clicking **Create a new field** in the top right corner of the window.
4.  Select **Add fields** to add the selected fields to your target table.


</td></tr></tbody>
</table>11. Select **Continue** to create the data import mapping and update your target table.

12. Convert any remaining worksheets if your file contained multiple worksheet tabs.

    -   **Note:** For each sheet that you want to convert, you will need to select **Convert to table**, and then repeat steps in this procedure or choose a different pathway for the additional worksheet \(see [Create new table from spreadsheet import](spreadsheet-create-new-table.md) or [Modify existing table using spreadsheet import](spreadsheet-import-existing-table.md) for steps\).

    -   If you do not have multiple worksheets, proceed to the next step.
13. Select **Done** on the summary screen.

    Alternatively, to view your table in Table Builder, you can select **Edit table\(s\)** on the summary screen.


## What to do next

For more information on editing your data tables in Table Builder, see [Table Builder](../../../administer/form-builder/concept/tb-landing-page.md).

**Parent Topic:**[Use a spreadsheet to add data](upload-multi-sheets.md)

