---
title: Data source script examples
description: Use data source scripts to map input values, descriptive elements, and input actions. Alternatively create a dedicated data source for each of these elements.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-03-05"
reading_time_minutes: 5
breadcrumb: [Configure data sources, Data sources, Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Data source script examples

Use data source scripts to map input values, descriptive elements, and input actions. Alternatively create a dedicated data source for each of these elements.

The data source script accepts two parameters: *valuesMapper* and *context*. The context parameter refers to the input form that the user is interacting with. The *valuesMapper* parameter is responsible for linking element identifiers to specific table columns via the *addRecordMapping* method. For example, the method call could look like this:

```
valuesMapper.addRecordMapping(UNIQUE_ELEMENT_IDENTIFIER, GLIDE_RECORD_INSTANCE, COLUMN_NAME);
```

**Note:** All the scripts listed in this topic are configured within the data source record. For more information, see [Configure data sources](../task/data-sources-config.md).

## Default sample script

The following is the sample script provided within the Mobile App Builder. The script provides a template showing how to filter an existing table and to map specific fields to UI elements.

```
(function DataSource(valuesMapper, context) {
var gr = new GlideRecord(TABLE_NAME); // Could be any table within the Instance, including custom tables
gr.addQuery('sys_id',context.getUniqueValue());
gr.query();
if (gr.next()) { // Could also be itetaring muliple records from the same table using the 'while' iterator

    valuesMapper.addRecordMapping('short_description',gr,'short_description'); // Map the field short_description to a UI element that has element identifier of "short_description". The element identifier could be any String, it's easier to map the column's name as the element identifer.

    valuesMapper.addRecordMapping('priority',gr,'priority'); // Map the field priority to a UI element that has element identifier of "priority". The element identifier could be any String, it's easier to map the column's name as the element identifier.

}
})(valuesMapper, context);

```

This sample script contains:

-   The following parameters that define the data source:
    -   *valuesMapper*: This parameter is used to map the values from the data source to the UI elements.
    -   *Context*: This parameter specifies the context in which the data source is being used, such as an incident, change request, or any other table.
-   The *addRecordMapping* method is used to map the fields and consists of the following parameters:
    -   Element identifier: The unique name you defined for the field you're mapping. In the example, this is `<short description>` and `<priority>`.
    -   Glide record `<gr>`: This is used to reference any table within the instance, including custom tables.
    -   Field name: This is the name of the field within the glide record. In the example, this is `<short description>` and `<priority>`.

        **Note:** A general guideline is to name the element identifier the same as the field name, to make the code easier to maintain and understand.


## Script to map inputs configured in the input form

The following is an example script demonstrating how the *ElementIdentifier* attribute of inputs configured in the Attributes \[sys\_sg\_input\_attribute\] table is processed. The script contains examples of mapping an input value to a column in the incident table of five inputs named *input\_1*, *input\_2*, *input\_3*, *input\_4*, *input\_5*.

```
(function DataSource(valuesMapper, context) {
var gr = new GlideRecord('incident');
gr.addQuery('sys_id',context.getUniqueValue());
gr.query();
if (gr.next()) {
// Map the column short_description from the incident table to the elementIdentifier "input_1_short_description".
valuesMapper.addRecordMapping('input_1_short_description', gr,'short_description'); 

// Map the column start_time from the incident table to the elementIdentifier "input_2_start_time".
valuesMapper.addRecordMapping('input_2_start_time',gr,'start_time'); 

// Map the column score from the incident table to the elementIdentifier "input_3_score".
valuesMapper.addRecordMapping('input_3_score', gr,'score'); 

// Map the column assigned_to from the incident table to the elementIdentifier "input_4_assigned_to".
valuesMapper.addRecordMapping('input_4_assigned_to',gr,'assigned_to');

// Map the attachment from the record in the incident table to the elementIdentifier "input_5_attachment_1" (The column name must be “sys_id”).
valuesMapper.addRecordMapping('input_5_attachment_1',gr,'sys_id');

 }
})(valuesMapper, context);

```

This code defines the function *DataSource* that maps specific columns from the Incident \[incident\] table record to corresponding element identifiers. The following process occurs:

-   Creates a *GlideRecord* object for the incident \[incident\] table.
-   Queries the table for a record with a specific *sys\_id* using a unique value from the *context*.
-   If a record is found, it maps the following columns to their correlated unique element identifier:
    -   *short\_description* to *input\_1\_short\_description*
    -   *start\_time* to *input\_2\_start\_time*
    -   *score* to *input\_3\_score*
    -   *assigned\_to* to *input\_4\_assigned\_to*
    -   *sys\_id* to *input\_5\_attachment\_1*

## Script to map descriptive elements associated with inputs or input sections in the input form

The following is an example script demonstrating how to handle the *ElementIdentifier* attribute of a descriptive element, configured in the descriptive element \[ sys\_sg\_descriptive\_element\] table.

```
(function DataSource (valuesMapper, context) {
var gr = new GlideRecord('incident');
gr.addQuery('sys_id',context.getUniqueValue());
gr.query();
if (gr.next()) {
// Handle descriptive element of type Rich Text. Map to a column named "rich_text_1_col" in the incident table to the elementIdentifier "input_1_rich_text_descriptive_element_id". The col type in the "incident" should be "HTML"
valuesMapper.addRecordMapping('input_1_rich_text_descriptive_element_id',gr,'rich_text_1_col'); 

// Handle descriptive element of type Text. Map to a column named "plain_text_1_col" in the incident table to the elementIdentifier "input_1_text_descriptive_element_id". The col type in the "incident" should be "String"/"String (Full UTF-8)"
valuesMapper.addRecordMapping('input_1_text_descriptive_element_id',gr,'plain_text_1_col'); 

// Handle descriptive element of type Image. Map to a column named "image_1_col" in the incident table to the elementIdentifier "input_1_image_descriptive_element_id". The col type in the "incident" should be "Image"
valuesMapper.addRecordMapping('input_1_image_descriptive_element_id',gr,'image_1_col'); 
}
})(valuesMapper, context);

```

This code defines the function *DataSource* that maps specific columns from the Incident \[incident\] table record to corresponding element identifiers. The following process occurs:

-   Creates a *GlideRecord* object for the incident \[incident\] table.
-   Queries the table for a record with a specific *sys\_id* using a unique value from the *context*.
-   If a record is found, it maps the following columns to their correlated unique element identifier:
    -   *rich\_text\_1\_col* \(HTML type\) to *input\_1\_rich\_text\_descriptive\_element\_id*
    -   *plain\_text\_1\_col*\(String type\) to *input\_1\_text\_descriptive\_element\_id*
    -   *image\_1\_col* \(Image type\) to *input\_1\_image\_descriptive\_element\_id*

## Script to map input actions associated with inputs in the input form

The following is an example script demonstrating how to handle the *ElementIdentifier* attribute of input actions configured in the Input form action \[sys\_sg\_parameter\_action\] table.

```
(function DataSource(valuesMapper, context) {
var gr = new GlideRecord('incident');
gr.addQuery('sys_id',context.getUniqueValue());
gr.query();
if (gr.next()) {
// Handle an attachment type input action. Map the elementIdentifier "input_1_action_attachments" to a record in the incident table by specifying the sys_id as the column in the table.
valuesMapper.addRecordMapping('input_1_action_attachments',gr,'sys_id'); 

// Handle a comment type input action. Map the elementIdentifier "input_1_action_comment" to a column in the incident table where the comment is stored. In this example, the comment is stored in the //"comment_by_agent" column.
valuesMapper.addRecordMapping('input_1_action_comment',gr,'comment_by_agent'); 

//Handle a navigation type input action with a record context.
Map the elementIdentifier "input_1_navigation" to a record in the incident table by specifying the sys_id as the column in the table.
valuesMapper.addRecordMapping('input_1_navigation',gr,'sys_id'); 
}
})(valuesMapper, context);

```

This code defines the function *DataSource* that maps specific columns from an Incident \[incident\] table record to corresponding element identifiers. The following process occurs:

-   Creates a GlideRecord object for the 'incident' table.
-   Queries the table for a record with a specific *sys\_id* using a unique value from the *context*.
-   If a record is found, it maps the following columns to their correlated unique element identifier:
    -   *sys\_id* to *input\_1\_action\_attachments* for handling attachment type input actions.
    -   *comment\_by\_agent*to *input\_1\_action\_comment*for handling comment type input actions.
    -   *sys\_id* to *input\_1\_navigation* for handling navigation type input actions with a record context.

