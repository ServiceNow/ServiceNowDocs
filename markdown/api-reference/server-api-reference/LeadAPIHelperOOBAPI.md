---
title: LeadAPIHelperOOB - Scoped
description: The LeadAPIHelperOOB script include provides helper methods called by the lead REST API to perform various functions, such as converting a set of lead records from a GlideRecord object into a JSON array or JSON object and transforming fields within a lead object.Converts a GlideRecord object into a JSON object. This method iterates over the fields of the GlideRecord, checks their types, and appropriately formats their values into a JSON-compatible structure.Converts a set of lead records from a GlideRecord object to a JSON array. You must specify the lead record fields that you want included in the JSON array.Transforms the specified lead object.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# LeadAPIHelperOOB- Scoped

The LeadAPIHelperOOB script include provides helper methods called by the lead REST API to perform various functions, such as converting a set of lead records from a GlideRecord object into a JSON array or JSON object and transforming fields within a lead object.

If you want to customize these helper functions, override the methods in this script include in the LeadAPIHelper script include. The names of the methods that you are overriding in the LeadAPIHelper script include must be the same as those in the LeadAPIHelperOOB script include file.

This API is provided within the `sn_lead_mgmt_core` namespace. To access the API, the Lead Management Data Model \(sn\_lead\_mgmt\_core\) plugin must be activated on the instance, and the calling user must have the sn\_lead\_mgmt\_core.lead\_integrator role.

For additional information on Lead Management, see [Using Lead Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/lead-management-using.md).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## LeadAPIHelperOOB - getJSONFromGR\(GlideRecord gr, Array fields\)

Converts a GlideRecord object into a JSON object. This method iterates over the fields of the GlideRecord, checks their types, and appropriately formats their values into a JSON-compatible structure.

<table id="table_wfp_p1z_ydc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

gr

</td><td>

GlideRecord

</td><td>

GlideRecord object to convert to a JSON object.

</td></tr><tr><td>

fields

</td><td>

Array

</td><td>

Optional. Comma-separated field names to include in the JSON object. These names must exactly match the names in the lead record.For example:  `["account", "first_name", "do_not_call", "lead_line_items"]`

**Note:**

If the **fields** parameter is null or contains the value `"lead_line_items"`, the method fetches each associated line item record, including all fields of the line item.

This method only supports converting individual fields from the Lead \[sn\_lead\_mgmt\_core\_lead\] table, not the Lead Line Item \[sn\_lead\_mgmt\_core\_lead\_line\_item\] table. If you specify a specific field from the Lead Line Item table, it is ignored.

Default: All lead record fields are included in the JSON object.

</td></tr></tbody>
</table><table id="table_xfp_p1z_ydc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

JSON object

</td><td>

JSON object that contains the fields from the specified GlideRecord. Each field in the GlideRecord is converted to a key-value pair. Special handling is applied for reference fields, choice fields, date-time fields, and other specific data types to ensure they are correctly formatted.

</td></tr></tbody>
</table>The following code example shows where to add your custom code for the getJsonFromGR\(\) method in the LeadAPIHelper script include.

```
var LeadAPIHelper = Class.create(); 
LeadAPIHelper.prototype = Object.extendsObject(LeadAPIHelperOOB, {

// Define overriding functions here
getJSONFromGR: function(gr, fields) {

// Add your custom code here
},

type: 'LeadAPIHelper'
});
```

## LeadAPIHelperOOB - getLeadsJSON\(GlideRecord leadsGr, Array fields\)

Converts a set of lead records from a GlideRecord object to a JSON array. You must specify the lead record fields that you want included in the JSON array.

<table id="table_d41_qvy_ydc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

leadsGr

</td><td>

GlideRecord

</td><td>

GlideRecord object containing the lead records to convert to JSON.Table: Lead \[sn\_lead\_mgmt-core\_lead\]

</td></tr><tr><td>

fields

</td><td>

Array

</td><td>

Comma-separated field names to include in the JSON object. These names must exactly match the names in the lead record.For example:  `["account", "first_name", "do_not_call", "lead_line_items"]`

**Note:**

If the **fields** parameter is null or contains the value `"lead_line_items"`, the method fetches each associated line item record, including all fields of the line item.

This method only supports converting individual fields from the Lead \[sn\_lead\_mgmt\_core\_lead\] table, not the Lead Line Item \[sn\_lead\_mgmt\_core\_lead\_line\_item\] table. If you specify a specific field from the Lead Line Item table, it is ignored.

</td></tr></tbody>
</table><table id="table_e41_qvy_ydc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array of JSON objects

</td><td>

Each object represents a lead containing the specified fields. If applicable, it also includes an array of lead line item objects for every lead.Each field in the GlideRecord is converted to a key-value pair. Special handling is applied for reference fields, choice fields, date-time fields, and other specific data types to ensure they are correctly formatted.

</td></tr></tbody>
</table>The following code example shows where to add your custom code for the getLeadsJson\(\) method in the LeadAPIHelper script include.

```
var LeadAPIHelper = Class.create();
LeadAPIHelper.prototype = Object.extendsObject(LeadAPIHelperOOB, { 

// Define overriding functions here 
getLeadsJson: function(leadsGR, fields) {

// Add your custom code here
}, 

type: 'LeadAPIHelper' 
}); 
```

## LeadAPIHelperOOB - getTransformedLeadObject\(Object leadObject\)

Transforms the specified lead object.

This transformation includes:

-   Removing ignored fields.
-   Converting reference fields to their  associated values, such as a sys\_id.
-   Combining work notes texts into a comma-separated string.
-   Validating the account, contact, and consumer fields. The values of account, contact, and consumer are ignored if both account and consumer contain values.

|Name|Type|Description|
|----|----|-----------|
|leadObject|Object|Lead object to transform. This object contains details of the lead and its related lead line items.|

|Type|Description|
|----|-----------|
|Object|Transformed lead object.|

The following code example shows where to add your custom code for the getTransformedLeadObject\(\) method in the LeadAPIHelper script include.

```
var LeadAPIHelper = Class.create();

LeadAPIHelper.prototype = Object.extendsObject(LeadAPIHelperOOB, {

// Define overriding functions here 
getTransformedLeadObject: function(leadObject) { 

// Add your custom code here
}, 

type: 'LeadAPIHelper'
}); 
```

