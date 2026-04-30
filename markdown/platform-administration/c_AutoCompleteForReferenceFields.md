---
title: Auto-complete for reference fields
description: By default, a reference field auto-completes as the user types in the field.A field inherits and uses the reference table's auto-complete attributes unless the field has its own value for the same attributes. You can define the attributes for references to a table, and it affects every form that references that table.You can remove the display value column from a reference field by setting the ref\_ac\_display\_value attribute to false.By default, all reference fields use a starts with query to search for matching text in the reference table. This prevents auto-complete from executing inefficient contains queries every time a user searches a reference field. You can require all reference fields to use a starts with query.By default, auto-complete only matches text in the display value column. You can configure a reference field to match text from any additional column the reference field displays.By default, the reference auto-complete uses a starts with search. A user preference can be created to implement a contains search.Wildcard searches use the auto-complete functionality.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Reference field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Auto-complete for reference fields

By default, a reference field auto-completes as the user types in the field.

Administrators can configure additional auto-complete options. A user must have table-level read permission on the referenced table for auto-complete to display any options.

![A user types in joe, and autocomplete suggests Joe Employee for the field.](../image/RefAutoComplete.png "Auto complete")

## Dictionary attributes for auto-completion of reference fields

There are dictionary attributes that are specific to reference fields and that determine auto-complete behavior.

<table id="table_r5y_s13_rt"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ref\_auto\_completer

</td><td>

Specifies the name of the client-side JavaScript class that creates the drop-down auto completion choices. Valid class values include: -   **AJAXReferenceCompleter**: Displays matching auto-complete choices as a drop-down choice list. The list only displays the reference table's display value column. Reference fields automatically use this class if there is no other auto-completion class specified.
-   **AJAXTableCompleter**: Displays matching auto-complete choices as rows in a table. The table displays the reference table's display value column and any columns listed in the **ref\_ac\_columns** attribute.
-   **AJAXReferenceChoice**: Displays matching auto-complete choices as a drop-down choice-list. The list only displays the reference table's display value column. Furthermore, the list only displays up to 25 matching choices. If there are more than 25 auto-complete choices, the reference field instead displays the choices with the AJAXTableCompleter class.

</td></tr><tr><td>

ref\_ac\_columns

</td><td>

Specifies the list of reference table columns to display. Separate column names with a semi-colon. For example, **ref\_ac\_columns=user\_name;email;sys\_created\_on** allows auto-complete to match text from the user\_name, email, and sys\_created\_on columns.

</td></tr><tr><td>

ref\_ac\_order\_by

</td><td>

Specifies the reference table column that sorts the auto-completion choices. For example, **ref\_ac\_order\_by=name** sorts the auto-completion choices alphabetically by name.

</td></tr></tbody>
</table>## Auto-complete UI features

The AJAX table completer class has a number of UI improvements.

-   The table completer always displays the number of records the auto-complete query finds.
-   The table completer highlights the entire selected row by changing the color of the background and text.
-   The table completer lists a value for every column.
    -   The first time a value appears in a column, the table completer displays it in black text.
    -   The table completer displays subsequent duplicate values in grey text. Previously, the table completer displayed an empty cell in a column containing a duplicate value.

![](../image/Autocomplete_highlighting.png "Selected row highlight")

Set the **ref\_auto\_completer=AJAXTableCompleter** dictionary attribute to use these improvements.

## Define auto-complete attributes for all references to a table

A field inherits and uses the reference table's auto-complete attributes unless the field has its own value for the same attributes. You can define the attributes for references to a table, and it affects every form that references that table.

### Before you begin

Role required: personalize\_dictionary

### About this task

A field-level attribute overrides a table-level attribute of the same name. If a field uses different reference attributes from those that are defined for the reference table, then the field uses both sets of attributes.

Use these steps to define auto-complete attributes for all fields in a table that do not already have their own auto-complete attributes. This example describes how to define auto-complete attributes for all references to the User \[sys\_user\] table.

**Note:** A field's auto-complete attribute value supersedes a table's auto-complete attribute value. This means that any existing field-level value for an auto-complete attribute supersedes any value the administrator applies to the auto-complete attribute from the reference table.

### Procedure

1.  Navigate to a list of the target table, such as **All** &gt; **User Administration** &gt; **Users**.

2.  Perform the appropriate action for your list version.

    |Version|Action|
    |-------|------|
    |**List v2**|Right-click the column header and click **Configure** &gt; **Dictionary**.|
    |**List v3**|Open the list title menu and click **Configure**, and then click **Dictionary**.|

3.  Select the row that does not list a column name.

    This row is typically the first row in the list. For example, select the first **sys\_user** link.

4.  Under **Related Links**, click **Advanced view**.

5.  In the **Attributes** field, enter a comma-separated list of auto-complete attributes you want to apply to all fields in the table.

    For example, to display the user's department with all references to the sys\_user table, enter:

    ```
    ref_auto_completer=AJAXTableCompleter,ref_ac_columns=department,ref_ac_order_by=department
    ```

6.  Click **Update**.


### What to do next

To test the new auto-complete attributes, open a form that references the User \[sys\_user\] table, such as an open incident. Enter a single character in the **Assigned to** field. The auto-complete options now include both the user name and department.

![Auto-complete list](../image/AutocompleteTableAttributes2.png)

## Remove the display value column

You can remove the display value column from a reference field by setting the **ref\_ac\_display\_value** attribute to false.

### Before you begin

Role required: personalize\_dictionary

### About this task

This causes the reference field to remove the display value column and only display the columns listed in the **ref\_ac\_columns** attribute. This feature requires the use of the AJAXTableCompleter class and the **ref\_ac\_columns**, **ref\_ac\_columns\_search**, and **ref\_ac\_display\_value** attributes.

**Note:** Auto-complete cannot match text from additional columns when the reference field is a product of the **ui\_reference** UI macro. This means any auto-complete action against a selector, such as the Impersonate User list, can only match text against the display value.

This example describes how to remove the display value column from references to the User \[sys\_user\] table and replace it with references to the first\_name and last\_name columns.

### Procedure

1.  Navigate to a list of the target table, such as **All** &gt; **User Administration** &gt; **Users**.

2.  Perform the appropriate action for your list version.

    |Version|Action|
    |-------|------|
    |**List v2**|Right-click the column header and click **Configure** &gt; **Dictionary**.|
    |**List v3**|Open the list title menu and click **Configure**, and then click **Dictionary**.|

3.  Select the row that does not list a column name.

    This row is typically the first row in the list. For example, select the first **sys\_user** link.

4.  Under **Related Links**, click **Advanced view**.

5.  In the **Attributes** field, add the **ref\_auto\_completer**, **ref\_ac\_columns**,**ref\_ac\_columns\_search**, and **ref\_ac\_display\_value** attributes.

    For example, to hide the display value column and only display the user's first and last names enter the following.

    ```
    ref_auto_completer=AJAXTableCompleter,ref_ac_columns=first_name;last_name,ref_ac_columns_search=true,ref_ac_display_value=false
    ```

6.  Click **Update**.


### What to do next

To test the new auto-complete attributes, open a form that references the User \[sys\_user\] table, such as an open incident. Enter a single character in the **Assigned to** field. The auto-complete options now hide the display value column \(user\_name\) and only display the first\_name and last\_name columns.

![Auto-complete no display value](../image/AutocompleteNoDisplayValue.png)

## Improve auto-complete queries

By default, all reference fields use a **starts with** query to search for matching text in the reference table. This prevents auto-complete from executing inefficient **contains** queries every time a user searches a reference field. You can require all reference fields to use a **starts with** query.

### Before you begin

Role required: admin

### About this task

The following example illustrates a **contains** query. Note that the letter "d" appears anywhere in the user's first or last name.

![Auto-complete contains query](../image/AutocompleteContains.png)

This procedure describes how to change the **glide.ui.ref\_ac.startswith** system property to always use a **starts with** query.

### Procedure

1.  In the navigation filter, enter `sys_properties.list` and press the Enter key.

2.  Select the **glide.ui.ref\_ac.startswith** property.

    To search for the property, enter `*startswith` in the **Go to** search filter for the **Name** column.

3.  In the **Value** field, replace **false** with **true**.

    **Note:** Setting the **glide.ui.ref\_ac.startswith** system property to **true** overrides any existing **autocomplete.contains** settings in both user and system level preferences. This property changes the autocomplete query method for all users regardless of preferences.

4.  Click **Update**.

5.  Test the change by opening a record with a reference field and entering a character in it, as illustrated in the example below.

    ![Auto-complete starts with query](../image/AutocompleteStartswith.png)


## Configure auto-complete to match text from any reference field

By default, auto-complete only matches text in the display value column. You can configure a reference field to match text from any additional column the reference field displays.

### Before you begin

Role required: personalize\_dictionary

### About this task

You can add the **ref\_ac\_columns\_search** attribute to enable auto-complete to match text in any column listed in the **ref\_ac\_columns** attribute. Set the **ref\_ac\_columns\_search** attribute to **true** to match text from all reference field columns. By default \(or when this attribute is **false**\) auto-complete only matches text in the display value column.

### Procedure

1.  Right-click the label of a reference field.

2.  Select **Configure Dictionary** from the choice list.

3.  Under **Related Links**, click **Advanced view**.

4.  In the **Attributes** field, add the desired auto-completion attributes.

    For example, these attributes add the department field to the caller list and sort callers by their department:

    ```
    ref_auto_completer=AJAXTableCompleter,ref_ac_columns=department,ref_ac_order_by=department,ref_ac_columns_search=true 
    ```

    ![Caller list with name and department](../image/AutoCompleteAttribute.png "Auto-complete attribute")

5.  Click **Update**.


### Example

The following example describes how to set the **Configuration Item** field display the CI class names from auto-complete choices for the Configuration item \[cmdb\_ci\] table.

```
ref_auto_completer=AJAXTableCompleter ,ref_ac_columns =sys_class_name ,ref_ac_order_by =sys_class_name ,ref_contributions =task_show_ci_map ;ci_show_incidents
```

**Note:** The **ref\_contributions** attribute controls the icons that appear next to the reference field.

![Additional CI attributes](../image/AdditionalCiAttributes.png)

## Enable contains auto-complete searches

By default, the reference auto-complete uses a **starts with** search. A user preference can be created to implement a **contains** search.

### Before you begin

Role required: admin

### Procedure

1.  Disable the **glide.ui.ref\_ac.startswith** system property.

    For more information, see [Improve auto-complete queries](c_AutoCompleteForReferenceFields.md#).

    **Note:** Setting the **glide.ui.ref\_ac.startswith** system property to **true** overrides any existing "autocomplete.contains" settings in both user and system level preferences. This property changes the auto-complete query method for all users regardless of preferences.

2.  Navigate to **User Administration** &gt; **User Preferences**.

3.  Select the preference **"'&lt;referenced table&gt;.autocomplete.contains"'**.

4.  Set the **value** field to **true**.

    ![Autocomplete user preference set to true](../image/AutocompleteContains1.png)

5.  Click **Update**.


### What to do next

Log out and log back in to display the updated search.

## Wildcards in reference auto-completes

Wildcard searches use the auto-complete functionality.

Use an asterisk in the reference field for wildcard searches.

If two asterisks are entered, a list of available records display in the auto-complete suggestions.

