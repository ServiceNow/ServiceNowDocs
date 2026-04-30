---
title: Fields view in Table Builder
description: Modify the table properties and manage the table fields by using the default Fields view on the Data tab in Table Builder.Store more information in a table record by adding a table column.Delete a column from your table using Table Builder.Modify the label that uniquely identifies the data that is stored in it to users.Change the database name for the column. You may opt to change the column name manually if a reviewer finds that the column name in the database was causing issues in testing.Change the type of field that will store information for rows in a table column. For example, if your table is tracking dates, you would want to select the Date column type.Edit field properties such as the field label, type, and default values in Table Builder.Define the default value to populate a table column automatically after a user creates a record.Select a column value that will be displayed in the reference fields of other tables. For example, the Opened by column of the task table could refer to a specific column in the user table so it can display a user name.
locale: en-US
release: yokohama
product: Form Builder
classification: form-builder
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Data in Table Builder, Using Table Builder, Table Builder, Builder library, Developing your application, Building applications]
---

# Fields view in Table Builder

Modify the table properties and manage the table fields by using the default Fields view on the **Data** tab in Table Builder.

## Before you begin

-   Launch Table Builder. For more information, see [Accessing Table Builder](../concept/accessing-form-builder.md).
-   \(Optional\) Choose a domain to work within \(if not global\). For more information, see [Domain separation and Table Builder](../concept/form-builder-domain-separation.md).
-   \(Optional\) Choose an application scope to work within \(if not global\). For more information, see [Using an application scope with Table Builder](../concept/fb-application-scope.md).

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

## Procedure

-   Use the following procedures to edit tables using **Fields** view in Table Builder.


**Parent Topic:**[Data in Table Builder](../concept/table-builder.md)

## Add a table column in Table Builder

Store more information in a table record by adding a table column.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Fields view displays by default. You can also access the Fields view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Select **+ Add new field**.

3.  On the resulting blank row, fill in the desired properties for the new data table column.

    ![Adding a new field to a table.](../image/tb-add-new-field.png "Adding a new field to a table")

<table id="choicetable_wqj_vdz_5wb"><thead><tr><th align="left" id="d188421e267">

Field

</th><th align="left" id="d188421e270">

Description

</th></tr></thead><tbody><tr><td id="d188421e276">

**Column label**

</td><td>

Unique label for the column.

</td></tr><tr><td id="d188421e285">

**Column name**

</td><td>

Database name for the column.

</td></tr><tr><td id="d188421e294">

**Type**

</td><td id="chdesc_fieldtype">

Type of information that the column contains. For example, to contain plain text in the column, select **String**.

 Depending on the type that you select, fill in the additional fields to further define the table column. For example, if you select **String**, define the character limit of the string input. Or, if you select **Choice**, define the choices that users can choose from.

 See [Field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td id="d188421e325">

**Reference**

</td><td>

Table that is associated with the column. This field applies only if the column type is **Reference**.

</td></tr><tr><td id="d188421e338">

**Max length**

</td><td>

Maximum number of characters that users can enter in the field.

</td></tr><tr><td id="d188421e347">

**Default value**

</td><td>

Value that populates the field automatically after a new record is created.

</td></tr><tr><td id="d188421e356">

**Display**

</td><td>

Option to set the column as the display value for the table. A reference field shows the display value of the table to which it is referring. For example, the **Opened by** column of the task table refers to the user table. Because the display value of the user table is the user name, the **Opened by** field shows something like **Beth Anglin** or **Joe Employee**. When you select a display value, choose the table column that would act as an appropriate title for individual records.

 Only one column can act as the display value for a table.

</td></tr><tr><td id="d188421e386">

**Updated**

</td><td>

Information about when the table was last updated.

</td></tr></tbody>
</table>4.  Select **Save**.


### Result

If you preview the table, you can see the new column that was added to your table. For more information on previewing a table, see [Preview your data in Table Builder](preview-table-fb.md).

## Delete a table column in Table Builder

Delete a column from your table using Table Builder.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Fields view displays by default. You can also access the Fields view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Next to the table field row you want to delete, hover over the leftmost column, and select the Open side panel icon \(![Open side panel icon](../image/side-panel-icon.png)\).

3.  At the top right corner of the side panel, select the trash icon \(![Trash icon.](../../../build/app-engine-studio/image/trash-icon.png)\) to delete the field.

    **Note:** Your table includes several default columns \(including Created and Updated\), that you can't delete. Also, you can't delete columns that are extended from another table or columns where data records are already present. To delete the column, you must first delete the existing data.

4.  Select **Delete** in the confirmation dialog.


### Result

If you preview the table, you can see that the table column is no longer used in the table. For more information on previewing a table, see [Preview your data in Table Builder](preview-table-fb.md).

## Change a column label in Table Builder

Modify the label that uniquely identifies the data that is stored in it to users.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### About this task

A column label is the text that's visible to your users when they're reading or updating application data. For example, if you create a form for requesters to fill in, each column label appears as a form field label.

Use a column label that describes the specific information that you expect users to enter. For example, to prompt a user to add comments, you would use the column label "Comments" instead of "Text".

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Fields view displays by default. You can also access the Fields view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Change a column label in the Column label column, by updating the text in the corresponding row.

    For example, to change the label of the "Office location" column, you would select the cell that says "Office location" and enter a different label.

    The column label updates automatically after you select another cell.

3.  Select **Save**.


## Changing a table column name in Table Builder

Change the database name for the column. You may opt to change the column name manually if a reviewer finds that the column name in the database was causing issues in testing.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### About this task

**Note:** You can't change the column name for existing fields that have information in them saved already.

A column name is the text that an administrator uses to track column data in the database. A column name is created automatically after you enter a column label. In Table Builder, if you change the column label, the column name also changes automatically.

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Fields view displays by default. You can also access the Fields view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Change the column name in the Column name column by updating the text in the corresponding row.

    For example, to change the name of the "Office location" column, you would select the cell that says u\_office\_location and enter a different name.

    The column name updates automatically after you select another cell.

3.  Select **Save**.


## Change a column type in Table Builder

Change the type of field that will store information for rows in a table column. For example, if your table is tracking dates, you would want to select the Date column type.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Fields view displays by default. You can also access the Fields view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Select a cell and clear the text from the **Type** column.

3.  From the list, select a column type.

    You can search the list by entering new text. For example, to find all the string types, you would enter `string`.

4.  If required, define the column type with more information.

    For example, if you select **Choice**, define the list of choices that users can select from.

    The column type updates automatically after you select another cell.

5.  Select **Save**.


## Edit field properties in Table Builder

Edit field properties such as the field label, type, and default values in Table Builder.

### Before you begin

Launch Table Builder. For more information, see [Accessing Table Builder](../concept/accessing-form-builder.md).

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Fields view displays by default. You can also access the Fields view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Select a field you want to modify in the table.

    For information about basic field properties, see [Field Configuration.](../reference/field-parameters.md)

3.  Next to the field you want to edit, hover over the leftmost column, and select the Open side panel icon \(![Open side panel icon](../image/side-panel-icon.png)\).

4.  Make your changes to the field properties.

    For information about modifying a field's UI policies, see [Modify a UI policy in Table Builder](../concept/form-builder-policies-rules.md#).

    **Note:** The **Config** tab on the right stays open even if you switch between the **Data** and **Forms** tabs.

5.  Select **Save**.


## Add a default value to a table column in Table Builder

Define the default value to populate a table column automatically after a user creates a record.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Fields view displays by default. You can also access the Fields view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Add the default value of a column in the **Default value** column by updating the content in the corresponding row.

    You define the default value by selecting a cell and then entering the value. The value that you enter depends on the column type. For example, if the column requires a choice, you would select one of the choices that you defined in the Type column.

    The column name updates automatically after you select another cell.

3.  Select **Save**.


## Select a column as the table display value in Table Builder

Select a column value that will be displayed in the reference fields of other tables. For example, the Opened by column of the task table could refer to a specific column in the user table so it can display a user name.

### Before you begin

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

### About this task

A reference field shows the display value of the table to which it is referring. For example, the Opened by column of the task table refers to the user table. Because the display value of the user table is the user name, the **Opened by** field shows something like "Beth Anglin" or "Joe Employee". When you select a display value, choose the table column that would act as an appropriate title for individual records.

Only one column can act as the display value for a table.

### Procedure

1.  Navigate to the **Data** tab.

    **Note:** Fields view displays by default. You can also access the Fields view from the Additional actions menu \(![Additional actions menu.](../image/tb-data-addl-actions-menu.png)\).

2.  Check that all selections are cleared from the **Display** column.

    To clear a selection, toggle off the switch as shown in the following example.

    ![Toggle off.](../image/toggle-off.png "Toggle off")

3.  From the Display column, select one row to act as the table display value.

    To select a row, toggle on the switch as shown in the following example.

    ![Toggle on.](../image/toggle-on.png "Toggle on")

4.  Select **Save**.


