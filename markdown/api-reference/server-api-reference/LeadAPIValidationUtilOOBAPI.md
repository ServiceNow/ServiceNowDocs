---
title: LeadAPIValidationUtilOOB - Scoped
description: The LeadAPIValidationUtilOOB script include provides methods that are called by the lead REST API to validate lead records and associated lead line item records when they are created \(POST\) or updated \(PATCH\).Validates the passed fields for a specified lead and its associated line items when updating a lead record using the PATCH endpoint of the lead API.Validates the passed fields for a specified lead and its associated line items when creating a lead record using the POST endpoint of the lead API.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# LeadAPIValidationUtilOOB - Scoped

The LeadAPIValidationUtilOOB script include provides methods that are called by the lead REST API to validate lead records and associated lead line item records when they are created \(POST\) or updated \(PATCH\).

If you want to customize how lead records are validated when the [lead API](../../../../../integrate/inbound-rest/concept/lead-api.md#) methods are called, override the methods in this script include in the LeadAPIValidationUtil script include. The names of the methods that you are overriding in the LeadAPIValidationUtil script include must be the same as those in the LeadAPIValidationUtilOOB script include file.

This API is provided within the `sn_lead_mgmt_core` namespace. To access the API, the Lead Management Data Model \(sn\_lead\_mgmt\_core\) plugin must be activated on the instance, and the calling user must have the sn\_lead\_mgmt\_core.lead\_integrator role.

For additional information on Lead Management, see [Using Lead Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/lead-management-using.md).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## LeadAPIValidationUtilOOB - validateLeadObjectForPatchCall \(Object leadObject\)

Validates the passed fields for a specified lead and its associated line items when updating a lead record using the `PATCH` endpoint of the lead API.

This method is triggered by the processUpdateLead\(\) method in the LeadAPIValidationUtilOOB script include. This method performs various validations, such as:

-   Checks for mandatory fields
-   Checks that the phone number and email address have the proper format.
-   Checks choice and reference fields, ignoring any invalid values.
-   Validates the stage and throws an error if the user attempts to qualify a lead.

|Name|Type|Description|
|----|----|-----------|
|leadObject|Object|Fields to update in the specified lead record and associated lead line item records. For a list of the fields that can be passed and their associated requirements, see [lead - PATCH /sn\_lead\_mgmt\_core/lead/\{sys\_id\}](../../../../../integrate/inbound-rest/concept/lead-api.md#).|

<table id="table_h1v_qls_ydc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;JSON object&gt;

</td><td>

Results of the validation.```
{
  "errors": [Array],
  "indexesOfleadLineItemsForInsertion": [Array] 
} 
```

</td></tr><tr><td>

&lt;JSON object&gt;.errors

</td><td>

Details of the errors detected while validating the passed lead and lead line item object. Returns an empty array if no errors are detected.For example:

```
[
  {"email":"Invalid email address."},
  {"last_name":"Mandatory field is either missing or invalid."},
  {"lead_line_items[0]/product_offering":"Mandatory field is either missing or invalid."}
]
```

These error messages are located in the LeadAPIConstantsOOB script include.

Data type: Array of Objects

</td></tr><tr><td>

&lt;JSON object&gt;.indexesOfleadLineItemsForInsertion

</td><td>

Indexes of new lead line items that need to be inserted in the leadObject. Data type: Array of Integers

</td></tr></tbody>
</table>The following code example shows where to add your custom code for the validateLeadObjectForPatchCall\(\) method in the LeadAPIValidationUtil script include.

```
var LeadAPIValidationUtil = Class.create(); 

LeadAPIValidationUtil.prototype = Object.extendsObject(LeadAPIValidationUtilOOB, { 

// Define overriding functions here

validateLeadObjectForPatchCall: function(leadObject) { 
// Add your custom code here
}, 

type: 'LeadAPIValidationUtil' 

});
```

## LeadAPIValidationUtilOOB - validateLeadObjectForPostCall \(Object leadObject\)

Validates the passed fields for a specified lead and its associated line items when creating a lead record using the `POST` endpoint of the lead API.

This method is triggered by the processCreateLead\(\) method in the LeadAPIValidationUtilOOB script include. This method performs various validations, such as:

-   Checks for required fields.
-   Checks that the phone number and email address have the proper format.
-   Checks choice and reference fields, ignoring any invalid values.

|Name|Type|Description|
|----|----|-----------|
|leadObject|Object|Fields to insert in the new lead record and associated lead line item records. For a list of the fields that can be passed and their associated requirements, see [lead - POST /sn\_lead\_mgmt\_core/lead](../../../../../integrate/inbound-rest/concept/lead-api.md#).|

<table id="table_hgp_t1s_ydc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

Details of the errors detected while validating the passed lead and lead line item object. Returns an empty array if no errors are detected.For example:

```
[
  {"email":"Invalid email address."},
  {"last_name":"Mandatory field is either missing or invalid."},
  {"lead_line_items[0]/product_offering":"Mandatory field is either missing or invalid."}
]
```

These error messages are located in the LeadAPIConstantsOOB script include.

</td></tr></tbody>
</table>The following code example shows where to add your custom code for the validateLeadObjectForPostCall\(\) method in the LeadAPIValidationUtil script include.

```
var LeadAPIValidationUtil = Class.create(); 

LeadAPIValidationUtil.prototype = Object.extendsObject(LeadAPIValidationUtilOOB, { 

// Define overriding functions here 

validateLeadObjectForPostCall: function(leadObject) { 
// Add your custom code
}, 

type: 'LeadAPIValidationUtil' 

}); 
```

