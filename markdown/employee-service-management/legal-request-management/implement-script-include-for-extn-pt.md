---
title: Use the script include for Scripted Extension Point
description: Use the script include for Scripted Extension Point to update the custom fields on the iManage storage based on the mapping provided in the functions.
locale: en-US
release: australia
product: Legal Request Management
classification: legal-request-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create implementation in Scripted Extension Point, Configure legal storage system, Configure, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Use the script include for Scripted Extension Point

Use the script include for Scripted Extension Point to update the custom fields on the iManage storage based on the mapping provided in the functions.

The processes below explain how to implement the script include for Scripted Extension Point.

-   On the script include form, the script field is auto populated with the structure of expected function definitions. For more information on script include form, see [Script includes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_ScriptIncludes.md).
-   In the script include, the function have inputs that is available when the implementation is called.
-   In case of iManage Extension Point \(sn\_lg\_ops.iManageCustomFieldHelperExtension\), following are the function definition, expectation and possible outputs:

<table id="table_ctv_jqb_1yb"><thead><tr><th>

Function Name

</th><th>

Usage Information

</th><th>

Output

</th></tr></thead><tbody><tr><td>

canHandle

</td><td>

Input:TableName: Name of the table of which the current record is being processed.

Use: This function is used to identify whether this implementation should be executed if the TableName you are passing is using the same condition that is defined in the function.

Example: In Legal Request Management, you have the input as tableName to identify if this implementation is for the same table.

The possible script would be as follows:

`canHandle: function(tableName) { return tableName == "The target table of implementation "; },`

</td><td>

True/FalseTrue: The current execution should be executed.

False: The current execution shouldn’t be executed.

</td></tr><tr><td>

Process

</td><td>

Input:requestRecord: GlideRecord object of the current legal record which is being processed.

Use: This function is used to create mapping between the iManage Fields and the fields of the legal record.

Example: In Legal Request Management, you have the GlideRecord object of the current legal table record in concern, which is used to get the values of the record fields and map to the custom fields in the process function.

The possible script would be as follows:

`process: function(requestRecord) { return { custom1: requestRecord.getDisplayValue("practice_area"), custom2: data, custom4: requestRecord.requested_for.country, description: requestRecord.description }; },`

</td><td>

`{ custom1: requestRecord.getDisplayValue(“practice_area”). custom2: requestRecord.getValue("description”) }`

</td></tr></tbody>
</table>
**Parent Topic:**[Create implementation in Scripted Extension Point](../task/create-scripted-extension-point.md)

