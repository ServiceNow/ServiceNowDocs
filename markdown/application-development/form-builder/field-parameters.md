---
title: Field configuration in Table Builder
description: You can configure the basic field properties for any field within Table Builder.
locale: en-US
release: xanadu
product: Form Builder
classification: form-builder
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Table Builder reference, Table Builder, Builder library, Developing your application, Building applications]
---

# Field configuration in Table Builder

You can configure the basic field properties for any field within Table Builder.

## Field details

The Field details section lets you configure the basic field elements for the selected field in the form editor.

To see field type descriptions and learn more about what field types you can use, see [Field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

To understand the basic field properties and learn more about adding and customizing a field in a table, see [Add and customize a field in a table](https://www.servicenow.com/docs/access?context=t_CreatingNewFields&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

The following table shows field descriptions for the Field details section.

<table id="table_dwm_l2b_fsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Name of the field that is displayed for form users.

</td></tr><tr><td>

Active

</td><td>

Option that you can select to make a field active so that form users can view it.

 Deselecting **Active** inactivates a field. When **Active** is not selected, the field will not display in the form editor.

 To reactivate a field, hover to the left of the field column in the **Data** tab and select the Open side panel icon \[![Open side panel icon.](../image/field-config-icon.png)\]. Select **Active** and save changes.

</td></tr><tr><td>

Read only

</td><td>

Option that you can select so that the field is not editable by the form users.

</td></tr><tr><td>

Mandatory

</td><td>

Option that you can select so that the data that your users enter in the field is required before they can save their changes to the form.

</td></tr><tr><td>

Configure Label details menu \( ![Configure label details.](../image/fb-configure-label.png)\)

</td><td>

Properties for a field label:-   **Tooltip** property that is displayed when a user points to the field.
-   **Plural** property that indicates if multiple instances of a field exist, your user should enter the plural form of the label \(for example, the plural of cat is cats\)
-   **URL** property that indicates if the field label links to some other location, your user should enter the URL here.

</td></tr></tbody>
</table>## Default value

The default value automatically fills in the field on the empty form for a new record, or fills in the field later \(if the field is empty\) when your user submits the new record. You can specify the default values as either a constant or use a script to generate them.

To learn how to define a default value for the fields, see [Specify a default field value](https://www.servicenow.com/docs/access?context=t_SpecifyingADefaultValue&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

The following table shows field descriptions for the Default value section.

|Field|Description|
|-----|-----------|
|Use dynamic default|Property that displays the **Dynamic default value** field where you can set the default value that is displayed for the field.|
|Default value|String or number that represents the default value of the field.|
|Dynamic default value|Keywords that can be entered in the search field. Your user can then select a field that contains the desired default value for the field.|

## Function definition

A function field generates a value that is based on the simple computations of other fields and constants.

This section is displayed in the editor when you are creating a field and you select **Function field** in the Advanced properties section.

For information on defining function fields, see [Function field](https://www.servicenow.com/docs/access?context=platform-support-functions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

The following table shows field descriptions for the Function definition section.

|Field|Description|
|-----|-----------|
|Function Definition|Function expression that generates the desired value for the field.|

## Reference

A reference qualifier restricts the records that are available for reference fields.

For information on defining reference fields, see [Reference field type](https://www.servicenow.com/docs/access?context=c_ReferenceField&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

The following table shows field descriptions for the Reference section.

<table id="table_frs_n2b_fsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reference

</td><td>

Data table that the selected field references.

</td></tr><tr><td>

Use reference qualifier

</td><td>

Qualifier options:-   **Simple** option that enables your users to build a simple conditional expression. Your user can select the **Edit Conditions** button below the **Reference qualifier** field.
-   **Advanced** option that enables your user to build an advanced conditional expression by using the **Reference qualifier** field. The advanced reference qualifiers enable your user to define an inline encrypted query string or JavaScript \(actual code or the name of an existing script include or business rule\) filter in the **Reference qualifier** field.
-   **Dynamic** option that enables your users to build a conditional expression for the selected reference field by using the **Reference qualifier** field. Dynamic reference qualifiers enable your users to use a dynamic filter to run a query against a reference field to filter the returned data set.

</td></tr><tr><td>

Reference qualifier

</td><td>

Referenced qualifier that is based on your user's selection for the **Use reference qualifier** field.

</td></tr><tr><td>

Edit conditions

</td><td>

Hyperlink to launch a pop-up window where your user can enter a simple conditional expression for the **Reference qualifier** field.

</td></tr></tbody>
</table>## Dependent field

A choice or reference field can be declared dependent on another field on the same table. Dependent fields limit their available values based on the value in the dependent field.

Using dependent fields turns on choices. The available choices for your field rely on the value that a user chooses for the dependent field.

For information on defining field dependencies, see [Make a field dependent](https://www.servicenow.com/docs/access?context=t_MakingAFieldDependent&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

The following table shows field descriptions for the Dependent fields section.

|Field|Description|
|-----|-----------|
|Use dependent field|Field dependency that you can activate for the selected field.|
|Select dependent field|List where you select a different field on the form that can then be used to control which choices that are displayed to users in the form field you are configuring.|

## Choices

A choice list is a type of field that lets the user select from a pre-defined set of choices. You can define the available choices and customize the behavior and appearance of your choice lists. For information about the choice list configuration, see [Choice list field type](https://www.servicenow.com/docs/access?context=c_ChoiceLists&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

In the Choices section of the Config panel, select **Use choices**, and then select **Edit** or the **+Add** icon to customize the available choices for the selected field.

The following table shows field descriptions in the Choices section.

<table id="table_l3b_jdx_fsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Text that is displayed to your users for the choice in the list.

</td></tr><tr><td>

Value

</td><td>

Value for the choice field.

</td></tr><tr><td>

Dependent value

</td><td>

Value that you map in the selected Dependent field to the entered choice.

</td></tr><tr><td>

Domain

</td><td>

Domain that the choice resides in.

</td></tr><tr><td>

Active

</td><td>

Option to display the choice as a selection. Inactive choices do not display for users.

</td></tr><tr><td>

Options

</td><td>

Option that enables you to select **Use the choices from another field** to duplicate the displayed choices for this field from the choices in another selected field.

</td></tr><tr><td>

Show choices as

</td><td>

Options that control how a list of choices displays for users of your form.

-   **Dropdown** option. You must set a default value for the field.

**Note:** If no default is set, then **None** automatically becomes the default value and is shown in the choice list to users.

-   **Dropdown with --None-- choice** option. **None** becomes the default value.
-   **Suggestions \(Core UI only\)** option. Choices are displayed as suggestions.

</td></tr><tr><td>

Filter

</td><td>

Option to filter the choice list. Select **Show inactive choices** to view all choices \(including inactive ones\).

</td></tr></tbody>
</table>## Attributes

A dictionary attribute alters the behavior of the table or element that the dictionary record describes. You can add or modify the dictionary attributes. For information about dictionary attributes, see [Dictionary attributes](https://www.servicenow.com/docs/access?context=c_DictionaryAttributes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

In the Attributes section of the Config panel, select **Edit** or **+Add** to customize the available attributes for the selected field.

The following table shows field descriptions for the Attributes section.

<table id="table_bf2_q2b_fsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attribute

</td><td>

Option list of available attributes. Select an option from the list of available attributes.

 To review the list of available attributes, see [Dictionary attributes](https://www.servicenow.com/docs/access?context=c_DictionaryAttributes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Value

</td><td>

Attribute value that you can set to alter the field behavior that is described by the dictionary record.

</td></tr></tbody>
</table>## Formula

A formula allows you to calculate the value of a column without writing a script. You can use one of the predefined formulas or combine two are more formulas to calculate the column value. For information on the predefined formulas and examples, see [Formulas](formulas-columns-table-builder.md#).

In the Formula section, select **Edit** or **+ Add** to edit or add a formula.

|Field|Description|
|-----|-----------|
|Formula editor|A text-editor like interface that allows you to enter and edit formulas.|

-   **[Formulas for column values in Table Builder](formulas-columns-table-builder.md#)**  
You can use a predefined function and create a formula to calculate the value of a column without writing a script. Use a predefined function or create a nested formula by using the existing predefined functions to calculate the column value type.
-   **[Add a formula to a column in Table Builder](../task/add-formula-column-table-builder.md)**  
Use a predefined function or create a formula to calculate a value for a column without writing a script in Table Builder. You can use two or more functions to create a formula according to your requirements.

**Parent Topic:**[Table Builder reference](../concept/fb-reference.md)

