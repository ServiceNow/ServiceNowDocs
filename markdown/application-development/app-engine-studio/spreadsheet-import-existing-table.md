---
title: Modify existing table using spreadsheet import
description: Use a Microsoft Excel spreadsheet import to update an existing application table.
locale: en-US
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Use a spreadsheet, Create a data model, Enhance your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Modify existing table using spreadsheet import

Use a Microsoft Excel spreadsheet import to update an existing application table.

## Before you begin

-   Import a spreadsheet into App Engine Studio. See [Import a spreadsheet](spreadsheet-importing-spreadsheet.md).

Role required: admin, sn\_app\_eng\_studio.user, sn\_app\_eng\_studio.admin, or delegated developer permissions. For more information, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## Procedure

1.  After you have uploaded your spreadsheet as described in [Import a spreadsheet](spreadsheet-importing-spreadsheet.md), choose where to import your file in the displayed wizard.

    ![Import into an existing application table.](../image/aes-spreadsheet-import-data-existing.png "Import into an existing application table")

    1.  Select **An existing table**.

    2.  Select an existing application table from the list that displays.

2.  Select **Continue**.

    A screen displays where you can map field columns from your source spreadsheet on the left to field columns in your existing target application table on the right.

    **Note:** You will have the opportunity to adjust mapping or create new fields from your import in it.

    ![Map imported fields.](../image/spreadsheet-map-fields.png "Map imported fields")

3.  You have the following actions available to you during this step.

<table id="choicetable_importchoices"><tbody><tr><td id="d252246e172">

**Batch map fields using Automap**

</td><td>

Select **Automap** to automatically map your spreadsheet fields to displayed fields in the selected target table. Automap maps source entities to similarly named target entities. For a target entity that has already been mapped, selecting **Automap** doesn't change its value. An automapped field has a wand icon on its data pill.

</td></tr><tr><td id="d252246e187">

**Map fields by dragging and dropping**

</td><td>

Map fields from your import to your target table by dragging data pills representing columns in the imported spreadsheet to the **Value** column in the target table. You can also map fields by using the pill picker to the right of each target table field.

</td></tr><tr><td id="d252246e202">

**Map fields using the data picker**

</td><td>

Map data by using the pill picker \(![Pill picker.](../../../administer/integrationhub/images/pill-picker-green.png)\) on the right side of the target table. You can enter more than one value in the **Value** column, you can also enter text.

</td></tr><tr><td id="d252246e223">

**Add transform options**

</td><td>

Add transform options for each of the individual mapped spreadsheet fields by clicking the FX icon \( ![FX icon.](../../../administer/flow-designer/images/fx-icon.png)\) on the right side pane. For example, you can use the Uppercase transform function to change an input string to all uppercase characters. See [Transform functions](https://www.servicenow.com/docs/access?context=transform-functions&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) for information on how to use these to trim data for your imported spreadsheet fields.

**Note:** Not all the transform functions available in Flow Designer are available.

</td></tr><tr><td id="d252246e247">

**Activate data record matching**

</td><td>

Specify fields where the system should check for matching data and, if found, update existing records instead of creating new ones by enabling the **Match** toggle in your target table. For example, if a target table has an **Order number** field and a record with an order number of 743, there are two options for handling potential matches.

-   If the **Match** toggle switch for the **Order number** field is on, the system checks for matching data. If the source data has a record with the same order number, the system updates the existing record in the target table.
-   If the **Match** toggle switch for the **Order number** field is off, the system doesn't check for matching data. If the source data has a record with the same order number, the system creates a new record in the target table. In this case, the target table will have two records, both with an order number of 743.


</td></tr><tr><td id="d252246e286">

**Configure reference and choice field behavior**

</td><td>

Configure behavior for **Choice** and **Reference** field types.1.  Click the gear icon \(![Gear icon.](../../../administer/ui-builder/image/gear-icon.png)\).
2.  In **Field**, select the field column to match the incoming record value against in the target table.
3.  In **If no matching record exists then do the following**, specify what to do if that record isn't found in the target table.
    -   **Create a new choice/record:** Creates the choice or record in the target table's matching field column from the data imported for the field.
    -   **Ignore this field:** Ignores the field in the target table and leaves it null.
    -   **Skip this record:** Skips adding the entire record \(row\) in the target table.
4.  Click **Done**.


</td></tr><tr><td id="d252246e348">

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
</table>4.  Select **Continue** to create the data import mapping and update your target table.

    **Note:** You will be prompted if there are any unmapped fields remaining in your spreadsheet. You can map those fields or continue without mapping them.

5.  Convert any remaining worksheets if your file contained multiple worksheet tabs.

    -   **Note:** For each sheet that you want to convert, you will need to select **Convert to table**, and then repeat steps in this procedure or choose a different pathway for the additional worksheet \(see [Create new table from spreadsheet import](spreadsheet-create-new-table.md) or [Create new table from extensible table and spreadsheet import](spreadsheet-create-new-ext-table.md) for steps\).

    -   If you do not have multiple worksheets, proceed to the next step.
6.  Select **Done** on the summary screen.

    Alternatively, to view your table in Table Builder, you can select **Edit table\(s\)** on the summary screen.


## What to do next

For more information on editing your data tables in Table Builder, see [Table Builder](../../../administer/form-builder/concept/tb-landing-page.md).

**Parent Topic:**[Use a spreadsheet to add data](upload-multi-sheets.md)

