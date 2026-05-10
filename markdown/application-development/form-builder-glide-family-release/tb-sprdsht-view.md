---
title: Spreadsheet view in Table Builder
description: Use Spreadsheet view in Table Builder to work with your application data records and data structure in a spreadsheet format.Add a new data record within Table Builder Spreadsheet view.Edit individual data records within Table Builder Spreadsheet view.Sort your data records by a specific field column within Table Builder Spreadsheet view.Show a filtered list of data records that contain matching data for a selected field within Table Builder Spreadsheet view.Display only the data records you want to see in your list by setting up a conditional query within Table Builder Spreadsheet view.Edit field properties such as the field label, type, attributes, and default values within Table Builder Spreadsheet view.Add new field columns to a selected table within Table Builder Spreadsheet view.Duplicate an existing field column within a table shown in Table Builder Spreadsheet view.Change the order in which your columns are displayed within Table Builder Spreadsheet view.Choose whether to hide or show specific field columns within Table Builder Spreadsheet view.Pin specific columns to always display on the left when you scroll to the right in a table with a large number of field columns within Table Builder Spreadsheet view. Pinned columns are saved for each individual user, not globally. The next time a user logs in, any columns they pinned will be shown.Delete a field column for a selected table within Table Builder Spreadsheet view.
locale: en-US
release: australia
product: Form Builder \(Glide Family Release\)
classification: form-builder-glide-family-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Data in Table Builder, Using Table Builder, Table Builder, Builder library, Developing your application, Building applications]
---

# Spreadsheet view in Table Builder

Use **Spreadsheet** view in Table Builder to work with your application data records and data structure in a spreadsheet format.

## Overview of the Spreadsheet view

**Spreadsheet** view in Table Builder, enables you to review your application tables and their accompanying data in a familiar spreadsheet format. You can add columns, delete columns, and change column properties as well as review and update individual data records within those columns from a single screen.

## Saving data records in Spreadsheet view

Sometimes errors occur when trying to save data records \( data conflicting with applicable policies or business rules\). When this happens, a warning popup displays along with a filtered list of erroneous data records.

Correct the data in each record individually, or select **Revert record changes** to revert any changes you made to the erroneous records.

![Errors in Spreadsheet view.](../image/scr-us2-spreadsheet-error.png "Errors in Spreadsheet view")

Use the following procedures to edit table field structure and any imported data records for a selected table using **Spreadsheet** view in Table Builder

**Parent Topic:**[Data in Table Builder](../concept/table-builder.md)

## Add a new data record

Add a new data record within Table Builder **Spreadsheet** view.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Spreadsheet view displays by default. You can also access Spreadsheet view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Select the **Add new record** icon \(![Add new record icon.](../image/icn-us2-add-data-record.png)\).

    ![Add new record.](../image/scr-us2-add-record.png "Add new record")

3.  Make your changes to the data record.

4.  Select **Save**.

    See [Saving data records in Spreadsheet view](tb-sprdsht-view.md#section_bgw_pjc_dxb)for details on troubleshooting errors.


## Edit individual data records

Edit individual data records within Table Builder **Spreadsheet** view.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Spreadsheet view displays by default. You can also access Spreadsheet view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Click into any editable data record field to launch the data for editing.

    ![Edit a field on the record](../image/edit-data-record-tb.png "Edit a field")

3.  Make your changes to the data.

4.  Select **Save**.

    See [Saving data records in Spreadsheet view](tb-sprdsht-view.md#section_bgw_pjc_dxb)for details on troubleshooting errors.


## Sort your data records

Sort your data records by a specific field column within Table Builder **Spreadsheet** view.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Spreadsheet view displays by default. You can also access Spreadsheet view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Hover over a column header that contains the data by which you would like to sort the list of records, and then select the **Additional actions** icon \(![Additional actions icon.](../image/icn-us2-ellipsis-column.png)\) to launch a column-specific list of actions \(e.g., sort records by Approval Date in ascending order\).

3.  Select from the following options to choose whether to sort the data for the column in ascending or descending order.

    -   Sort A to Z or Sort Oldest to Newest \(ascending order\)
    -   Sort Z to A or Sort Newest to Oldest \(descending order\)
    ![Sort by a to z.](../image/scr-us2-sort-data.png "Sort A to Z")

    The list of records will then display in the order you chose.


## Show matching data records

Show a filtered list of data records that contain matching data for a selected field within Table Builder **Spreadsheet** view.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Spreadsheet view displays by default. You can also access Spreadsheet view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Select and hold \(or right-click\) the data record in a cell to create a filtered list of records that contain the matching data, \(e.g., show all records where **Short description** is "Can't read email".\).

    ![Show matching data records.](../image/scr-vs2-show-matching.png "Show matching data records")

    A filtered list of records with matching data displays and a new filter query is added and accessible when you click the **Filter** button at the top of the grid.

    **Note:** To remove the filtering you just added, select the **Filter** button, and then delete the new filter condition from the list. See [Filter your data records](tb-sprdsht-view.md#).


## Filter your data records

Display only the data records you want to see in your list by setting up a conditional query within Table Builder **Spreadsheet** view.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Spreadsheet view displays by default. You can also access Spreadsheet view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Select **Filter** above the spreadsheet to launch a filter query.

    You can also select **Filter by value** from a specific column's **Additional actions** menu \(![Additional actions icon.](../image/icn-us2-ellipsis-column.png)\) to pre-select that column's data for your query.

    **Note:** When a number appears to the right of the **Filter** button, it means that there are existing filters set for the view.

    The Filter window displays \(along with any filter criteria that has already been set\). In this case, an existing filter is set to display records where **Age** is 35.

    ![Filter data.](../image/scr-us2-filter-data.png "Filter data")

3.  Enter your filtering query to specify which data records you want to display.

    -   Select the **New condition set** button to enter a new filter condition which is connected by an OR statement.
    -   Select the **or** or **and** buttons to extend the existing filter set with the desired boolean.
    -   Select the **Delete** icon to remove a filter condition row.
4.  Select **Apply** to apply the filter condition to your view.

    The filtered list of records will then display based on the criteria you chose.


## Edit column field properties

Edit field properties such as the field label, type, attributes, and default values within Table Builder **Spreadsheet** view.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Spreadsheet view displays by default. You can also access Spreadsheet view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Hover over the desired column header, and then select the **Additional actions** icon \(![Additional actions icon.](../image/icn-us2-ellipsis-column.png)\) to launch a column-specific list of actions.

3.  Select **Column properties**.

    The Properties pane displays for the selected field column.

    ![Column properties displayed](../image/scr-us2-field-properties-pane.png "Properties pane")

4.  Edit the desired field property for the column.

    See [Field configuration in Table Builder](../reference/field-parameters.md) for more information on field properties.

5.  Select **Save**.


## Add new columns

Add new field columns to a selected table within Table Builder **Spreadsheet** view.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Spreadsheet view displays by default. You can also access Spreadsheet view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Select the **+ Add field** button.

    **Note:** You can also select the **Additional actions** icon \(![Additional actions icon.](../image/icn-us2-ellipsis-column.png)\) to launch a column-specific list of actions, and then select **Insert column left** or **Insert column right** to insert the new column in a specific place within the table.

    The Add a new column window displays.

    ![Add new column.](../image/scr-us2-add-column.png "Add new column")

3.  Enter the following information for your new field column.

<table id="choicetable_bs2_1yy_5wb"><thead><tr><th align="left" id="d267433e1148">

Field

</th><th align="left" id="d267433e1151">

Description

</th></tr></thead><tbody><tr><td id="d267433e1157">

**Column label**

</td><td>

Unique label for the column.

</td></tr><tr><td id="d267433e1166">

**Column name**

</td><td>

Database name for the column.

</td></tr><tr><td id="d267433e1175">

**Type**

</td><td>

Type of information that the column contains. For example, to contain plain text in the column, select **String**.

 Depending on the type that you select, fill in the additional fields to further define the table column. For example, if you select **String**, define the character limit of the string input. Or, if you select **Choice**, define the choices that users can choose from.

 See [Field types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_FieldTypes.md).

</td></tr></tbody>
</table>4.  Select **Advanced settings** to expand it and enter any additional properties for your new field column.

<table id="choicetable_mjz_hbz_5wb"><thead><tr><th align="left" id="d267433e1218">

Field

</th><th align="left" id="d267433e1221">

Description

</th></tr></thead><tbody><tr><td id="d267433e1227">

**Function field**

</td><td>

A function field generates a value based on simple computations of other fields and constants. The **Function definition** field then displays, where you define a function.

</td></tr><tr><td id="d267433e1242">

**Mandatory**

</td><td>

Option that you can select so that the data that your users enter in the field is required before they can save their changes to the form.

</td></tr><tr><td id="d267433e1254">

**Read only**

</td><td>

Option that you can select so that the field is not editable by the form users.

</td></tr><tr><td id="d267433e1266">

**Default value**

</td><td>

String or number that represents the default value of the field. This will be auto-populated in all rows of your column once it is created.

</td></tr></tbody>
</table>5.  Select **Add** to add the new field column to your table.


## Duplicate an existing column

Duplicate an existing field column within a table shown in Table Builder **Spreadsheet** view.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Spreadsheet view displays by default. You can also access Spreadsheet view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Hover over the header for the column to duplicate, and then select the **Additional actions** icon \(![Additional actions icon.](../image/icn-us2-ellipsis-column.png)\) to launch a column-specific list of actions.

3.  Select **Duplicate column**from the menu.

    The text "copy" is automatically appended to the existing column label.

    ![Duplicate column.](../image/scr-us2-duplicate-column.png "Duplicate column")

4.  Edit the **Column label** to the desired display name for the duplicated field column.

5.  Edit the **Type** for the field column as desired.

    See [Field types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_FieldTypes.md).

6.  Select **Duplicate**.

    A new column displays in the view.


## Reorder columns

Change the order in which your columns are displayed within Table Builder **Spreadsheet** view.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Spreadsheet view displays by default. You can also access Spreadsheet view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Click to select the **Column handle** icon \(![Column handle icon.](../image/icn-us2-column-handle.png)\) for a column and then drag the column to the desired locations in the table.

    ![Drag and drop column.](../image/scr-us2-drag-column.png "Drag and drop columns")

    **Note:** If your table contains many table columns, select the **Manage columns** menu to view a compact list of column names, and then visually drag and drop within this list to order your table columns.


## Set column visibility

Choose whether to hide or show specific field columns within Table Builder **Spreadsheet** view.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Spreadsheet view displays by default. You can also access Spreadsheet view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Choose one of the following options.

<table id="choicetable_tm2_b3j_twb"><thead><tr><th align="left" id="d267433e1682">

Action

</th><th align="left" id="d267433e1685">

Steps

</th></tr></thead><tbody><tr><td id="d267433e1691">

**Hide a column**

</td><td>

Using the **Manage columns** button:

1.  Select the **Manage columns** button to launch a window that displays the list of available columns.
2.  Deselect the column you wish to hide. Only selected columns will display in your view.
 Using the column's context menu:

1.  Hover over the column header to hide, and then select the **Additional actions** icon \(![Additional actions icon.](../image/icn-us2-ellipsis-column.png)\).
2.  Select **Hide** from the menu to hide the column from view.


</td></tr><tr><td id="d267433e1740">

**Unhide a column**

</td><td>

Using the **Manage columns** menu:

1.  Select the **Manage columns** button to launch a window that displays the list of available columns.
2.  Select the checkbox to the left of the column you wish to unhide. Only selected columns are displayed in your view.


</td></tr></tbody>
</table>    **Note:** A number displays to the right of the **Manage columns** button to show how many columns are active in the view.


## Pin columns

Pin specific columns to always display on the left when you scroll to the right in a table with a large number of field columns within Table Builder **Spreadsheet** view. Pinned columns are saved for each individual user, not globally. The next time a user logs in, any columns they pinned will be shown.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Spreadsheet view displays by default. You can also access Spreadsheet view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Choose one of the following options to pin or unpin a field column.

<table id="choicetable_br1_bkj_twb"><thead><tr><th align="left" id="d267433e1875">

Action

</th><th align="left" id="d267433e1878">

Steps

</th></tr></thead><tbody><tr><td id="d267433e1884">

**Pin a column**

</td><td>

1.  Hover over the column header to pin, and then select the **Additional actions** icon \(![Additional actions icon.](../image/icn-us2-ellipsis-column.png)\).
2.  Select **Pin** from the menu to pin the column to the left side of your view.


</td></tr><tr><td id="d267433e1915">

**Unpin a column**

</td><td>

1.  Hover over the column header to unpin, and then select the **Additional actions** icon \(![Additional actions icon.](../image/icn-us2-ellipsis-column.png)\).

**Note:** Pinned columns have a checkmark to the left of the column in the list.

2.  Toggle **Pin** off to unpin the pinned column.


</td></tr></tbody>
</table>    **Note:** You can also view which columns are pinned in the view by clicking the **Manage columns** button. Pinned columns will have a pin icon displayed next to the right of the listed column.


## Delete columns

Delete a field column for a selected table within Table Builder **Spreadsheet** view.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Spreadsheet view displays by default. You can also access Spreadsheet view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Hover over a column header you want to delete, and then select the **Additional actions** icon \(![Additional actions icon.](../image/icn-us2-ellipsis-column.png)\) to launch a column-specific list of actions \(e.g., sort records by Approval Date in ascending order\).

3.  Select **Delete column**.

    A confirmation window displays.

4.  Select **Delete** to delete the field column from your table.

    **Note:** If there are data records stored for the column you want to delete, you will not be able to delete the column until you have removed the records stored for this field.


