---
title: LeadAPIProcessUtilOOB - Scoped
description: The LeadAPIProcessUtilOOB script include provides methods that are called by the lead REST API to retrieve lead records and their associated lead line item records.Processes the request body and creates a lead and all its associated line items, based on the passed parameters.Retrieves all lead records and associated line item records based on the passed-in filter criteria. This method returns all fields within the associated records.Retrieves the specified lead record and its associated line item records. This method returns all fields within the associated records.Processes the request body and updates the specified lead and all its associated line items, based on the passed parameters.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# LeadAPIProcessUtilOOB- Scoped

The LeadAPIProcessUtilOOB script include provides methods that are called by the lead REST API to retrieve lead records and their associated lead line item records.

If you want to customize how lead records are retrieved when the [lead API](../../../../../integrate/inbound-rest/concept/lead-api.md#) methods are called, override the methods in this script include in the LeadAPIProcessUtil script include. The names of the methods that you are overriding in the LeadAPIProcessUtil script include must be the same as those in the LeadAPIProcessUtilOOB script include file.

This API is provided within the `sn_lead_mgmt_core` namespace. To access the API, the Lead Management Data Model \(sn\_lead\_mgmt\_core\) plugin must be activated on the instance, and the calling user must have the sn\_lead\_mgmt\_core.lead\_integrator role.

For additional information on Lead Management, see [Using Lead Management](https://www.servicenow.com/docs/access?context=lead-management-using&version=australia&pubname=australia-order-management&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## LeadAPIProcessUtilOOB - processCreateLead \(Object requestBody\)

Processes the request body and creates a lead and all its associated line items, based on the passed parameters.

Records are inserted in the following tables:

-   Lead \[sn\_lead\_mgmt\_core\_lead\]
-   Lead Line Item \[sn\_lead\_mgmt\_core\_lead\_line\_item\]

<table id="table_sxx_crr_ydc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

requestBody

</td><td>

Object

</td><td>

Request body of the lead and its related lead line items to create.For details on the contents of this object, see [lead - POST /sn\_lead\_mgmt\_core/lead](../../../../../integrate/inbound-rest/concept/lead-api.md#).

</td></tr></tbody>
</table><table id="table_txx_crr_ydc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

JSON object

</td><td>

Details of the saved lead and lead line item records.Data type: Object

```
{
  "body": {Object},
  "status": "String"
}
```

</td></tr><tr><td>

&lt;JSONobject&gt;.body

</td><td>

Response body.Successful response: All fields within the requested lead record and all fields in the associated lead line item records. For a description of the fields returned, refer to [lead - POST /sn\_lead\_mgmt\_core/lead](../../../../../integrate/inbound-rest/concept/lead-api.md#).

Error response: List of errors detected when trying to process the request. These error messages are defined in the LeadAPIConstants script include.

Data type: Object

</td></tr><tr><td>

&lt;JSONobject&gt;.status

</td><td>

Response status code.These status codes are defined in the LeadAPIConstants script include.

Data type: String

</td></tr></tbody>
</table>The following code example shows where to add your custom code for the processCreateLead\(\) method in the LeadAPIProcessUtil script include.

```
var LeadAPIProcessUtil = Class.create(); 

LeadAPIProcessUtil.prototype = Object.extendsObject(LeadAPIProcessUtilOOB, { 

// Define overriding functions here 

processCreateLead: function(requestBody) { 
// Add your custom code 
}, 

type: 'LeadAPIProcessUtil' 

}); 
```

## LeadAPIProcessUtilOOB - processGetAllLeads \(Object queryParams, String requestUrl\)

Retrieves all lead records and associated line item records based on the passed-in filter criteria. This method returns all fields within the associated records.

Record details are fetched from the following tables:

-   Lead \[sn\_lead\_mgmt\_core\_lead\]
-   Lead Line Item \[sn\_lead\_mgmt\_core\_lead\_line\_item\]

<table id="table_igt_klr_ydc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

queryParams

</td><td>

Object

</td><td>

Object containing the query parameters to apply when retrieving the lead records. These are the query parameters passed in the [lead - GET /sn\_lead\_mgmt\_core/lead](../../../../../integrate/inbound-rest/concept/lead-api.md#) endpoint.For example:

```
{
  "sysparm_fields":["first_name,last_name,sys_id,lead_line_items"],
  "sysparm_query":["lead_type=new_business"],
  "sysparm_offset":["2"],"sysparm_limit":["25"]
}
```

</td></tr><tr><td>

requestUrl

</td><td>

String

</td><td>

Request URL. Pass this URL when you are processing a paginated response so that the method has the links to all of the pages in the response.

</td></tr></tbody>
</table><table id="table_jgt_klr_ydc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

JSON object

</td><td>

Details of the requested lead and lead line item records.Data type: Object

```
{
  "body": [Array],
  "contentRange": "String",
  "links": "String", 
  "status": "String",
  "totalCount": "Number" 
}
```

If an errors occur while processing the request, the JSON object only contains the `body` and `status` parameters.

</td></tr><tr><td>

&lt;JSONobject&gt;.body

</td><td>

Response body.Successful response: An array of objects with each object containing a lead record and all associated lead line item records. All fields within the requested lead record and all fields in the associated lead line item records are returned. For a description of the fields returned, refer to [lead - GET /sn\_lead\_mgmt\_core/lead](../../../../../integrate/inbound-rest/concept/lead-api.md#).

Error response: List of errors detected when trying to process the request. These error messages are defined in the LeadAPIConstants script include.

Data type: Array of Objects

</td></tr><tr><td>

&lt;JSONobject&gt;.contentRange

</td><td>

Range of the content returned in a paginated call. For example: If offset=2 and limit=3, the value of this parameter is items 3-5.

Data type: String

</td></tr><tr><td>

&lt;JSONobject&gt;.links

</td><td>

In the case of a paginated response, comma-separated links to each page contained in the response.For example:

```
<https://servicenow-instance/api/sn_lead_mgmt_core/lead?sysparm_offset=0&sysparm_limit=20>;rel="self",
<https://servicenow-instance/api/sn_lead_mgmt_core/lead?sysparm_offset=20&sysparm_limit=20>;rel="last",
<https://servicenow-instance/api/sn_lead_mgmt_core/lead?sysparm_offset=20&sysparm_limit=20>;rel="next"
```

Data type: String

</td></tr><tr><td>

&lt;JSONobject&gt;.status

</td><td>

Response status code.These status codes are defined in the LeadAPIConstants script include.

Data type: String

</td></tr><tr><td>

&lt;JSONobject&gt;.totalCount

</td><td>

Total number of lead records returned by the method.Data type: Number \(Integer\)

</td></tr></tbody>
</table>The following code example shows where to add your custom code for the processGetAllLeads\(\) method in the LeadAPIProcessUtil script include.

```
var LeadAPIProcessUtil = Class.create(); 

LeadAPIProcessUtil.prototype = Object.extendsObject(LeadAPIProcessUtilOOB, { 

// Define overriding functions here 

processGetAllLeads: function(queryParams, requestUrl) { 
// Add your custom code here 
}, 

type: 'LeadAPIProcessUtil' 
}); 
```

## LeadAPIProcessUtilOOB - processGetLeadById \(String id\)

Retrieves the specified lead record and its associated line item records. This method returns all fields within the associated records.

Record details are fetched from the following tables:

-   Lead \[sn\_lead\_mgmt\_core\_lead\]
-   Lead Line Item \[sn\_lead\_mgmt\_core\_lead\_line\_item\]

<table id="table_fvz_qcl_ydc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

String

</td><td>

Sys\_id of the lead record to retrieve.Table: Lead \[sn\_lead\_mgmt\_core\_lead\]

</td></tr></tbody>
</table><table id="table_gvz_qcl_ydc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

JSON object

</td><td>

Details of the requested lead and lead line item records.Data type: Object

```
{
  "body": {Object},
  "status": "String"
}
```

</td></tr><tr><td>

&lt;JSONobject&gt;.body

</td><td>

Response body.Successful response: All fields within the requested lead record and all fields in the associated lead line item records. For a description of the fields returned, refer to [lead - GET /sn\_lead\_mgmt\_core/lead/\{sys\_id\}](../../../../../integrate/inbound-rest/concept/lead-api.md#).

Error response: List of errors detected when trying to process the request. These error messages are defined in the LeadAPIConstants script include.

Data type: Object

</td></tr><tr><td>

&lt;JSONobject&gt;.status

</td><td>

Response status code.These status codes are defined in the LeadAPIConstants script include.

Data type: String

</td></tr></tbody>
</table>The following code example shows where to add your custom code for the processGetLeadById\(\) method in the LeadAPIProcessUtil script include.

```
var LeadAPIProcessUtil = Class.create(); 

LeadAPIProcessUtil.prototype = Object.extendsObject(LeadAPIProcessUtilOOB, { 

// Define overriding functions here

processGetLeadById: function(id) { 
  // Add your custom code here
}, 

type: 'LeadAPIProcessUtil' 

}); 
```

## LeadAPIProcessUtilOOB - processUpdateLead \(Object requestBody, String id\)

Processes the request body and updates the specified lead and all its associated line items, based on the passed parameters.

Records are updated in the following tables:

-   Lead \[sn\_lead\_mgmt\_core\_lead\]
-   Lead Line Item \[sn\_lead\_mgmt\_core\_lead\_line\_item\]

<table id="table_n24_k5r_ydc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

requestBody

</td><td>

Object

</td><td>

Request body of the lead and its related lead line item fields to update.For details on the contents of this object, see [lead - PATCH /sn\_lead\_mgmt\_core/lead/\{sys\_id\}](../../../../../integrate/inbound-rest/concept/lead-api.md#).

</td></tr><tr><td>

id

</td><td>

String

</td><td>

Sys\_id of the lead record to update.Table: Lead \[sn\_lead\_mgmt\_core\_lead\]

</td></tr></tbody>
</table><table id="table_o24_k5r_ydc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

JSON object

</td><td>

Details of the saved lead and lead line item records.Data type: Object

```
{
  "body": {Object},
  "status": "String"
}
```

</td></tr><tr><td>

&lt;JSONobject&gt;.body

</td><td>

Response body.Successful response: All fields of the updated lead record and all fields in the associated lead line item records \(updated or not\). For a description of the fields returned, refer to [lead - PATCH /sn\_lead\_mgmt\_core/lead/\{sys\_id\}](../../../../../integrate/inbound-rest/concept/lead-api.md#).

Error response: List of errors detected when trying to process the request. These error messages are defined in the LeadAPIConstants script include.

Data type: Object

</td></tr><tr><td>

&lt;JSONobject&gt;.status

</td><td>

Response status code.These status codes are defined in the LeadAPIConstants script include.

Data type: String

</td></tr></tbody>
</table>The following code example shows where to add your custom code for the processUpdateLead\(\) method in the LeadAPIProcessUtil script include.

```
var LeadAPIProcessUtil = Class.create();

LeadAPIProcessUtil.prototype = Object.extendsObject(LeadAPIProcessUtilOOB, {

// Define overriding functions here 

processUpdateLead: function(requestBody, id) { 
// Add your custom code here
},

type: 'LeadAPIProcessUtil' 

}); 
```

