---
title: Dictionary entry form
description: The Dictionary Entry form was redesigned to provide an Advanced view and additional fields. You might need to configure the form to see all fields.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 15
breadcrumb: [Modify dictionary entries, Managing tables and indexes, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Dictionary entry form

The Dictionary Entry form was redesigned to provide an Advanced view and additional fields. You might need to configure the form to see all fields.

<table id="table_qpd_swr_lq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Defines the table in which the element is created.**Note:** This list shows only the tables that meet the scope protections for adding fields.

</td></tr><tr><td>

Type

</td><td>

Defines the field type of the column or, if the **Type** is **Collection**, indicates that the dictionary entry represents the table. For more information, see [Field administration](../../reference-pages/concept/c_IntroductionToFields.md).You can change the type of a field. To preserve existing data, only change between logical types that map to the same physical type on the database. For example, Choice and String.

</td></tr><tr><td>

Active

</td><td>

Enables or disables the field. When this check box is cleared, the field is hidden in lists and forms in the Classic Environment. However, inactive fields are still available for queries. Additionally, disabling a field by clearing this option doesn't remove it from a configured list. Inactive fields display in admin-configured lists until an admin updates the list layout to remove them. See below for additional behavior notes.

-   Forms: Deactivated fields are removed from forms.
-   Lists: Inactive fields continue to display in admin-configured lists until an admin updates the list layout to remove them. If an inactive field is removed from an admin-configured default view, any personal lists will reset to follow the default view, thus removing the inactive field from the personal list.
-   Reports: Existing reports that include inactive fields will continue to work, because the data still exists in the records. However, deactivated fields are not available when creating new reports or list layouts if they are not present in admin-configured lists.
-   Condition Builder: Deactivated fields are not available in the Condition Builder, unless a you are using an existing URL with filters containing the inactive field. **Show Matching**, **Filter Out**, and **Group By** can also be used on an inactive field if the column is present in the list view.
-   ServiceNow API: The ServiceNow API does not check whether a column is active or inactive. The old values for the field remain in the records and cannot be undone.
-   Scripts: Inactive fields may still be referenced in scripts. \(Server side scripts that use GlideRecord can read and write to inactive fields\).

</td></tr><tr><td>

Function field

</td><td>

If selected, creates a field that displays the results of a database function, such as a mathematical operation, field length computation, or day of the week calculation.Once the new function record is saved, you cannot clear the check box to make the field a regular field.

</td></tr><tr><td>

Read only

</td><td>

Determines whether users can change the field value in the user interface. When this check box is selected, it gets grayed out. The system calculates and displays the data for the field.**Note:** You can [override this option](../concept/c_DictionaryOverrides.md) for extended tables.

</td></tr><tr><td>

Audit

</td><td>

Enables or disables auditing for a table. Turning on Auditing \(History\) for a Table.**Note:** This option only applies to tables.

</td></tr><tr><td>

Text index

</td><td>

Determines whether searches index the text in a table.**Note:** This option only applies to tables. To exclude fields from indexing, see [Remove an index for a specific field](../../search-administration/task/t_RemoveAnIndexForASpecificField.md).

</td></tr><tr><td>

Column label

</td><td>

Defines a unique label for the column. The label appears on list headers and form fields for the column.-   Updating the **Column label** field also updates the label in the language file \(for the current language\).
-   When you create a new column, the column name is populated automatically based on the label, which is prefixed with u\_ to indicate that it is custom. For example, if you enter **Activity Description** as the column label, the column name defaults to **u\_activity\_description**.

</td></tr><tr><td>

Column name

</td><td>

Defines the field name of the column. When you create a new field, this name is populated automatically based on the label and a prefix as follows:-   For a field on a table in a different scope, the name is prefixed with the scope to indicate that it is custom and not part of that application.
-   For a field on a table in the same scoped application, the name does not have a prefix, which indicates that it is part of the application.
-   For a field in a global application, the name is prefixed with u\_ to indicate that it is custom.

 You cannot modify the prefix; however, you can modify the rest of the name. The name can contain only lowercase, alphanumeric ASCII characters and underscores \(\_\). You cannot change the name of an existing dictionary record.

**Note:** You cannot enter consecutive \(double\) underscores in a column name. For example if you enter `my__sample_name` as the column name, it is automatically changed to `my_sample_name` when you save the dictionary entry.

\]

</td></tr><tr><td>

Max length

</td><td>

Provides a logical limit for the size of string fields to determine how the system displays them in the user interface and how to map them to physical database data types.String fields with a length under 255 characters appear as a single-line text fields. String fields with a length over 254 characters appear as a multi-line text box.

 The system maps the field length to the closest physical data type available on the database. Sometimes, this results in more available length than originally specified. For example, entering a length of 50 maps to the closest physical data type of VARCHAR\(100\), which provides up to a 100 character limit or double the requested field length. Likewise, entering a length of 1000 maps to the closest physical data type of MEDIUMTEXT, which provides up to a 4000 character limit or four times the requested field length.

 **Note:**

-   You can only change this value for a **String** field. Changes for any other type of field are ignored.
-   Users on an Oracle instance cannot increase the maximum length of a string field to anything greater than 4000 through the application UI as this requires the CLOB datatype in Oracle. To increase beyond this size, log an incident with technical support to request the change.
-   To prevent data from being lost, only decrease the length of a string field when you are developing a new application and not when a field contains data. A warning appears if a change to a custom field results in data loss. For a base system field, you cannot make a change that results in data loss.

</td></tr><tr><td>

Mandatory

</td><td>

Determines whether this field must contain a value to save a record. For more information, see [Make a field mandatory](../../field-administration/task/t_MakingAFieldMandatory.md).**Note:** You can override this option for extended tables.

</td></tr><tr><td>

Display

</td><td>

Indicates that this field is the [Display values](../../field-administration/concept/c_DisplayValues.md) for reference fields. Set this to true for the one field whose value you want to use as the text displayed in links to this table on lists and forms. By default, the **Number** field is the display value for all task tables.**Note:**

-   This option does not control whether a list or form displays this field as part of the layout. Instead, see [List configuration](../../list-administration/concept/c_ListConfiguration.md) and Personalizing Forms.
-   The display value becomes part of the form title when viewing an individual record from a table.
-   You can set a different display value on an extended table than the display value on a parent table by using a [dictionary override](../concept/c_DictionaryOverrides.md).

</td></tr><tr><td>

Function definition

</td><td>

Defines the function that the field performs.Starts with `glidefunction:`, followed by the operation to be performed \(for example, `concat`\), followed by function parameters. Constants must be enclosed in single quotes.

For example, the following function definition creates a field that shows the short description, followed by a space, followed by the caller name:

`glidefunction:concat(short_description, ' ', caller_id.name)`

**Note:** Function parameters support dot-walking. See [Dot-walking to data in related tables](https://www.servicenow.com/docs/access?context=c_DotWalking&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Attributes \[Advanced view\]

</td><td>

Alters the behavior of a field or functionality that depends on the field. For more information, see [Dictionary Attributes](../../reference-pages/concept/c_DictionaryAttributes.md). Attributes can be overridden for extended tables with [dictionary overrides](../concept/c_DictionaryOverrides.md). You can also configure attributes for this dictionary entry through the **Attributes** related list.

</td></tr><tr><td class="sub-head" colspan="2">

Default Value

</td></tr><tr><td>

Use dynamic default \[Advanced view\]

</td><td>

Allows you to specify a default value that is generated dynamically based on a dynamic filter.

</td></tr><tr><td>

Dynamic filter value \[Advanced view\]

</td><td>

Specifies the [Create a dynamic filter option](https://www.servicenow.com/docs/access?context=t_DynamicFilterOptions&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) that determines the default value if the **Use dynamic default** option is selected.

</td></tr><tr><td>

Default value

</td><td>

Specifies the default value of the field for any new record. Ensure that this value uses the correct field type. For example, an integer field uses a default value of 2 but cannot use a default value of two. These values can be overridden with [dictionary overrides](../concept/c_DictionaryOverrides.md).

</td></tr><tr><td class="sub-head" colspan="2">

Reference Specification

</td></tr><tr><td>

Reference

</td><td>

Makes the field into a [Reference field type](../../field-administration/concept/c_ReferenceField.md).If you enter a name that does not match an existing table, a new table is created when you save your changes to the dictionary record. If the current table has a module in the application navigator, a module for the new table is automatically created in the same application menu.

</td></tr><tr><td>

Use reference qualifier \[Advanced view\]

</td><td>

Specifies the type of qualifier to use:-   Simple: A set of choice lists where you can specify a reference qualifier condition.
-   Dynamic: A [Create a dynamic filter option](https://www.servicenow.com/docs/access?context=t_DynamicFilterOptions&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) that you can use to build the qualifier.
-   Advanced: A static encoded query string or JavaScript code that you can use to build the qualifier.

</td></tr><tr><td>

Reference qual condition

</td><td>

Specifies a condition when the reference qualifier runs if the **Simple** qualifier type is selected.

</td></tr><tr><td>

Dynamic ref qual \[Advanced view\]

</td><td>

Specifies the [Create a dynamic filter option](https://www.servicenow.com/docs/access?context=t_DynamicFilterOptions&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) that determines the reference qualifier when the **Dynamic** qualifier type is selected.

</td></tr><tr><td>

Reference qual \[Advanced view\]

</td><td>

Filters the records available for a reference field if the **Advanced** qualifier type is selected. Reference qualifiers can be overridden with [dictionary overrides](../concept/c_DictionaryOverrides.md).

</td></tr><tr><td>

Reference key \[Advanced view\]

</td><td>

Identifies a field other than sys\_id to use as the unique identifier for reference fields.

</td></tr><tr><td>

Reference cascade rule \[Advanced view\]

</td><td>

Defines what happens to a record if the record it references is deleted. Select one of the following options:-   Clear: Clears the references \(default\).
-   Delete: Deletes all referencing records.
-   Restrict: Prevents record deletion if there is a referencing record.
-   None: Does not change referencing records.

</td></tr><tr><td>

Reference floats \[Advanced view\]

</td><td>

Enables the **Edit** button on related lists for one-to-many relationships.

</td></tr><tr><td>

Dynamic creation \[Advanced view\]

</td><td>

For reference fields, determines whether entering a value that does not match an existing record creates a record on the referenced table. If selected, use the **Dynamic creation script** field to define how to create the record.

</td></tr><tr><td>

Dynamic creation script \[Advanced view\]

</td><td>

When the **Dynamic creation field** is selected, allows you to enter a script for creating a record on the referenced table.

</td></tr><tr><td class="sub-head" colspan="2">

Dependent Field

</td></tr><tr><td>

Dependent on field \[Advanced view\]

</td><td>

Specifies a field on which the current field depends. For more information, see [Make a field dependent](../../field-administration/task/t_MakingAFieldDependent.md) **Note:** You can override this value for extended tables.

.

</td></tr><tr><td class="sub-head" colspan="2">

Choice List Specification

</td></tr><tr><td>

Choice

</td><td>

Allows users to see a list of suggested values in one of the following ways:-   List menu without -- None --
-   List menu with -- None --
-   [Suggestion field type](../../field-administration/task/t_AddingASuggestionField.md)

 If a choice is used, either define a [Choice list field type](../../field-administration/concept/c_ChoiceLists.md) or use the fields **Choice** table and **Choice** field to copy choices from another field elsewhere in the dictionary.

</td></tr><tr><td>

Choice table \[Advanced view\]

</td><td>

Populates the field choices with the same values as another choice field. If the **Choice** field is set to anything besides **None**, select a table to draw choice values from. The field **Choice field** must also be populated.For example, if **Choice table** is set to the Incident \[incident\] table, this field has the same choice list as one of the choice fields on Incident. **Choice field** \(see below\) determines which field.

</td></tr><tr><td>

Choice field \[Advanced view\]

</td><td>

Populates the field choices with the same values as another choice field. If the **Choice** field is set to anything besides **None**, select a field from the table you selected for **Choice table**. For example, if the **Choice table** field is set to the Incident \[incident\] table, and **Choice Field** is set to **Priority**, this field has the same choices as the **Priority** field on Incident, even if those choices change.**Note:** This field must be a choice field.

</td></tr><tr><td class="sub-head" colspan="2">

Calculated Value

</td></tr><tr><td>

Calculated \[Advanced view\]

</td><td>

Determines whether the value of the field is calculated from other values. If selected, use the **Calculation** field to define how the calculation is performed. The **Calculation Type** field allows you to select script or formula based calculation for the column value. When filtering, sorting or grouping by a calculated field, the sort order is based on the stored field value from the last time the field was updated, not the last time the field appeared. **Note:** In relation to business rules, calculated fields are populated first before any business rule, even a before business rule, is run. Calculated fields are then populated again if necessary after any before business rules run.

</td></tr><tr><td>

Calculation Type \[Advanced view\]

</td><td>

Allows you to select script based calculation or formula based calculation for a column. For more information about predefined functions and example formulas, see [Formulas for column values in Table Builder](https://www.servicenow.com/docs/access?context=formulas-columns-table-builder&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

</td></tr><tr><td>

Calculation \[Advanced view\]

</td><td>

Allows you to enter a script or formula based on the selected Calculation Type. When the **Calculation Type** is **Formula**, you can enter a predefined function or formula for calculating the value of the field. You can use a predefined formula or combine other formulas to create a formula according to your requirements.

 When the **Calculation Type** is **Script**, you can enter a script for calculating the value of the field. These can be overridden for extended tables with [dictionary overrides](../concept/c_DictionaryOverrides.md). You can use the current object in this script. As with access control rules, the script can:

-   Evaluate to true or false.
-   Return an answer variable set to true or false.
-   Set a field value directly, such as: `current.display_name="name"`.

**Note:** Fields display as read-only when calculated scripts are applied. For example, by adding a script to the calculated field on a dictionary record that is set to Active, the Active field is made read-only on the form. Inline editing of the Active field from the list view is also disabled.

</td></tr><tr><td class="sub-head" colspan="2">

Additional fields

</td></tr><tr><td>

Class

</td><td>

Identifies the table that the current table extends. Tables that do not extend other tables specify their own name in this field. For more information, see .

</td></tr><tr><td>

Defaultsort

</td><td>

Obsolete.

</td></tr><tr><td>

Size class

</td><td>

Determines whether the platform handles this table as a large table by reducing the amount of memory stored for each row during queries. There is a scheduled job which runs and sets the value of this field.

</td></tr><tr><td>

Spell check

</td><td>

Enables or disables spell check on the field.

</td></tr><tr><td>

Unique

</td><td>

Requires the field value to be unique.**Warning:** Making a field unique when the corresponding table already has different values for that field causes data loss. Before you enforce uniqueness on a field, verify that no records in the table for the field have values, or that they all have the same value.

</td></tr><tr><td class="sub-head" colspan="2">

UI action

</td></tr><tr><td>

Default view or Advanced view

</td><td>

Changes the form view to the default or advanced view. The fields change based on the view. If you are using the default view, you must write a script to accomplish the same tasks that advanced view fields provided.

</td></tr><tr><td class="sub-head" colspan="2">

Related Lists

</td></tr><tr><td>

Access Controls

</td><td>

Provides access to the access controls that permit or limit access to the data in the table.

</td></tr><tr><td>

Choices

</td><td>

Provides access to the options in the choice list field you are editing.

</td></tr><tr><td>

Dictionary overrides

</td><td>

Provides access to the dictionary overrides for this field.

</td></tr><tr><td>

Attributes

</td><td>

Provides access to the dictionary attributes for this entry.

</td></tr><tr><td>

Labels

</td><td>

Provides access to the labels used for the table or field you are editing.

</td></tr></tbody>
</table>**Parent Topic:**[Modify dictionary entries](../task/t_ModifyADictionaryEntryFromAForm.md)

