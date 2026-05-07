---
title: Matrix Loader CSV fields and field options upload and export
description: Use the Matrix Loader to bulk create, edit, and export fields, field options, and product pickers in CPQ. Define data in CSV files with supported columns and formats, then upload or download them for faster configuration management and environment migration.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Configure the Matrix Loader, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Matrix Loader CSV fields and field options upload and export

Use the Matrix Loader to bulk create, edit, and export fields, field options, and product pickers in CPQ. Define data in CSV files with supported columns and formats, then upload or download them for faster configuration management and environment migration.

## CSV fields upload

All field types can be added and edited via the Matrix Loader. This section assumes the reader will work in a spreadsheet file \(Google Sheets, Microsoft Excel, or similar\), then export the result to a CSV file for upload to the Matrix Loader. This topic outlines the columns and data that the Matrix Loader accepts in the field upload.

<table id="table_kzw_53y_mhc"><thead><tr><th>

Column name

</th><th>

Description

</th><th>

Valid values

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

field\_type

</td><td>

Defines the data type of the field

</td><td>

text \| textField boolean \| booleanField number \| numberField picklist \| pickListField

</td><td>

Required

</td></tr><tr><td>

name

</td><td>

The name that the admin sees on field list Admin page

</td><td>

Valid strings can be composed of up to 255 characters, including letters, numbers, spaces, and the following special characters: `{}[]()|\~`_^@?<=>;:/.-,+*ʼ&%$#”!`

</td><td>

Required

</td></tr><tr><td>

variableName

</td><td>

Distinct string used to reference the field

</td><td>

Valid field variable names consist of up to 128 letters, numbers, and underscores. The first and last character must be a letter or number.

</td><td>

Required; must be unique

</td></tr><tr><td>

required

</td><td>

Not currently used by the application

</td><td>

TRUE \| FALSE

 &lt;empty&gt;

</td><td>

Optional; not currently used by the application

</td></tr><tr><td>

defaultValue

</td><td>

Provide an initial value in field when config experience starts

</td><td>

\[See note\]

</td><td>

Optional; relevant to textField, booleanField, numberField, and single pickListField only. Multi pickListFields set defaults in the fieldOptions upload file.

</td></tr><tr><td>

minLength

</td><td>

Minimum number of characters accepted

</td><td>

&lt;number&gt;

</td><td>

Optional; relevant to textField only

</td></tr><tr><td>

maxLength

</td><td>

Maximum number of characters accepted

</td><td>

&lt;number&gt;

</td><td>

Optional; relevant to textField only

</td></tr><tr><td>

precision

</td><td>

Define digits of precision to the right of the decimal

</td><td>

&lt;number&gt;

</td><td>

Optional; relevant to numberField only

</td></tr><tr><td>

minValue

</td><td>

Minimum numeric value accepted

</td><td>

&lt;number&gt;

</td><td>

Optional; relevant to numberField only

</td></tr><tr><td>

maxValue

</td><td>

Maximum numeric value accepted

</td><td>

&lt;number&gt;

</td><td>

Optional; relevant to numberField only

</td></tr><tr><td>

selectType

</td><td>

Define whether pickListField is single-select or multi-select

</td><td>

single multi

 &lt;empty&gt;

</td><td>

Optional; relevant to pickListField only. If &lt;empty&gt;, assumes single

</td></tr></tbody>
</table>**Note:** When a field has defined values, the default value must conform to one of the defined values. For example:

-   Valid Boolean field default values are TRUE and FALSE.
-   If a number field has minValue or maxValue defined, the specified default value must conform to the definition.
-   The default value of a single pickListField must match an option value defined for the field. This option value can be defined in a field option CSV file that is processed by the Matrix Loader in the same batch as the field CSV file.
-   Text field values are limited to 2000 characters.

The order of columns is not fixed. For convenience, admins can rearrange the columns in their spreadsheet and the resulting CSV file.

The fields upload explainer file shows the variety of fields and field parameters accepted by the Matrix Loader. Cells with gray backgrounds denote that the cell is not relevant to the context of the row. To download the explainer file, in the Matrix Loader, click the Fields link in the Sample Files section.

**Note:** This fileʼs content is not intended to be uploaded to a environment as is. Instead, use the format examples to build an upload file that meets the requirements of your current project, export it to CSV format, and upload it to your environment by using the Matrix Loader.

Just as fields added via the Admin UI must be associated with one or more blueprints, so must fields that are added in bulk via the Matrix Loader. For instructions, see [Associate a field with a blueprint](cpq-associate-field-with-a-blueprint.md).

## CSV fields export

For convenience, admins can export a CSV file of fields and field options defined in the environment via the following steps:

1.  In the Admin navigation pane, click **Fields**.

    You see a list of all defined fields.

2.  \(Optional\) Enter a search string and press &lt;enter&gt; to narrow the list of fields.
3.  Click **Export**. A message temporarily appears at the bottom of the page.
4.  Click the notification center in the lower left corner.

    ![CSV fields export](../images/cpq-matrix-loader-csv-export-prepared.png)

5.  Click **Download** to download the CSV file.

    ![Notifications screen](../images/cpq-matrix-loader-csv-export-ready.png)


The resulting ZIP file contains the fields CSV file and the field options CSV file.

## CSV field options upload

The field options upload defines pickListField options and attribution. This section assumes the reader will work in a spreadsheet file \(Google Sheets, Microsoft Excel, or similar\), then download/export the result to a CSV file for upload to the Matrix Loader. The following outlines the columns and data the Matrix Loader accepts in the field option upload.

<table id="table_w2l_hjy_mhc"><thead><tr><th>

Column name

</th><th>

Description

</th><th>

Valid values

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

variableName

</td><td>

The variable name of the field for which this rowʼs option will be added

</td><td>

&lt;field variableName&gt;

</td><td>

Required

</td></tr><tr><td>

name

</td><td>

Option name visible to end- user

</td><td>

Valid strings can be composed of up to 255 characters, including letters, numbers, spaces, and the following special characters: `{}[]()|\~`_^@?<=>;:/.-,+*ʼ&%$#”!`

</td><td>

Required

</td></tr><tr><td>

value

</td><td>

Distinct string will use to reference the field option

</td><td>

Valid field option variable names consist of up to 128 letters, numbers, and underscores. The first and last character must be a letter or number. Field option variable names must be unique in the scope of the same field.

</td><td>

Required

</td></tr><tr><td>

defaultValue

</td><td>

Provide an initial value in field when config experience starts

</td><td>

TRUE FALSE

 &lt;empty&gt;

</td><td>

Optional; relevant to multi pickListFields only

</td></tr><tr><td>

extendedDescri ption

</td><td>

Contextual description for Admin reference

</td><td>

Valid strings can be composed of up to 255 characters, including letters, numbers, spaces, and the following special characters: `{}[]()|\~`_^@?<=>;:/.-,+*ʼ&%$#”!`

</td><td>

Optional

</td></tr><tr><td>

imageUrl

</td><td>

Image will show end-user for this pickListField option

</td><td>

&lt;URL&gt;

</td><td>

Optional; for use with pickListField.

 Display type is defined as VisualPicker or MultiSelectVisua lPicker in layout

</td></tr></tbody>
</table>The fields upload explainer file shows the variety of field options and field option parameters accepted by the Matrix Loader. Cells with gray backgrounds denote that the cell is not relevant to the context of the row. To download the explainer file, in the Matrix Loader, click the Fields link in the Sample Files section.

**Note:** This fileʼs content is not intended to be uploaded to a environment as is. Instead, use the format examples to build an upload file that meets the requirements of your current project, export it to CSV format, and upload it to your environment by using the Matrix Loader.

## Field options CSV export

Field options are exported in the same motion used to export fields from CPQ. For instructions, see the "CSV fields Export" section above.

## CSV upload: product picker

This section outlines the steps to create a product picker named "My product picker", which will include the following products/options:

-   Option1/Product1 - Product One
-   Option2/Product2 - Product Two
-   Option3/Product3 - Product Three

To create a product picker, follow these steps.

1.  Extract a sample CSV file for fields from the Matrix Loader.

    This CSV file should contain the field information required for creating a product picker. Ensure that you add an extra line at the top of the sample file specifying the field type as product picker \(this field type may not be present in the sample file\).

    ![CSV file](../images/cpq-matrix-loader-csv-upload-fields-sample.png)

2.  Extract a sample CSV file for field options from the Matrix Loader.

    This CSV file should contain the product names that will be displayed in the end-user UI for the fields created in the previous step.

    ![CSV file](../images/cpq-matrix-loader-csv-export-field-options-sample.png)

3.  Create a new .yaml file.

    This file should include the fields contained in the product picker, as defined in the CSV file in Step 1. The .yaml file will be used to link the two CSV files during the upload process in the Matrix Loader. Without it, the product picker will not be created.

    Example .yaml Syntax:

    ```
    ---
    - variableName: myProductPicker
    	fields:
    	- variableName: myProductPicker.value
    		target: ProductId
    	- variableName: myProductPicker.select
    	- variableName: myProductPicker.quantity
    		target: ProductQuantity
    ```

4.  Upload files to the Matrix Loader: Compress the two .csv files and the .yaml file from the previous steps into a zipped folder. Then, go to the Matrix Loader, upload the zipped folder, click **Import**, and then click **Continue**.

    ![Matrix Loader](../images/cpq-matrix-loader-import-files-dialog.png)

5.  Validate in UI: The newly created product picker should be available in the CPQ Admin fields as shown below.

    ![Product Picker](../images/cpq-matrix-loader-product-picker-setup.png)


## CSV export: product picker

To export a product picker, click fields in CPQ Admin. Click **Product Pickers**, select the product picker to export, and then click **Export**.

**Related topics**  


[Matrix Loader: CSV rules upload](matrix_loader_csv_rules_upload.md)

[Matrix Loader: CSV table upload](../task/cpq-matrix-loader-csv-table-upload.md)

