---
title: lead API
description: The lead API provides endpoints that enable you to create, update, and query/retrieve marketing leads and their associated lead line items from an instance.Retrieves all leads and associated lead line items based on the filter criteria passed in the query parameters.Returns the lead record and all associated lead line items for the specified sys\_id.Updates the specified lead record and its associated lead line items. You can also use this endpoint to associate new lead line items to the specified lead.Creates a lead record and its associated lead line items using the specified parameters.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 64
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# lead API

The lead API provides endpoints that enable you to create, update, and query/retrieve marketing leads and their associated lead line items from an instance.

Use this API to integrate your instance with external websites and systems such as automated lead capture systems, or to provide lead information to external reporting systems.

This API is provided within the `sn_lead_mgmt_core` namespace. To access the API, the Lead Management Data Model \(sn\_lead\_mgmt\_core\) plugin must be activated on the instance, and the calling user must have the sn\_lead\_mgmt\_core.lead\_integrator role.

For additional information on Lead Management, see [Using Lead Management](https://www.servicenow.com/docs/access?context=lead-management-using&version=australia&pubname=australia-order-management&ft:locale=en-US).

## Extending the Lead API

You can extend the lead API by overriding the methods in its associated script includes. The default API functionality is located in script includes ending in "OOB", such as LeadAPIProcessUtilOOB. To override this functionality, create methods with identical names and parameters in the script include that has the same file name, but doesn't end in "OOB", such as LeadAPIProcessUtil.

The following is a list of the script includes that you can override to change the behavior of the lead API:

-   [LeadAPIProcessUtilOOB](../../../app-store/dev_portal/API_reference/LeadAPIProcessUtilOOB/concept/LeadAPIProcessUtilOOBAPI.md#): Contains methods that handle the retrieval and creation of lead and lead line item records.
-   [LeadApiValidationUtilOOB](../../../app-store/dev_portal/API_reference/LeadAPIValidationUtilOOB/concept/LeadAPIValidationUtilOOBAPI.md#): Contains methods that validate the JSON request object for the POST and PATCH endpoints.
-   [LeadAPIHelperOOB](../../../app-store/dev_portal/API_reference/LeadAPIHelperOOB/concept/LeadAPIHelperOOBAPI.md#): Contains API helper methods that:
    -   Return an array of leads and related lead line items.
    -   Return a JSON object from the associated GlideRecord.
    -   Remove all ignored fields from a JSON object and perform other transformations.
-   LeadAPIConstantsOOB: Contains constants, status codes, and messages for all API operations. It also includes the list of fields that are ignored by the POST and PATCH endpoints.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## lead - GET /sn\_lead\_mgmt\_core/lead

Retrieves all leads and associated lead line items based on the filter criteria passed in the query parameters.

This endpoint returns a paginated response as per the specified limit and offset. It retrieves information from the following tables:

-   Lead \[sn\_lead\_mgmt\_core\_lead\]
-   Lead Line Item \[sn\_lead\_mgmt\_core\_lead\_line\_item\]

### URL format

Versioned URL: `/api/sn_lead_mgmt_core/{api_version}/lead`

Default URL: `/api/sn_lead_mgmt_core/{api_version}/lead`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_fields

</td><td id="sysparm_fields_entry-RESTAPI">

Comma-separated list of fields to return in the response. Invalid fields are ignored.Data type: String

Default: Return all fields.

</td></tr><tr><td>

sysparm\_limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. This limit is applied before ACL evaluation. If no records return, including records you have access to, rearrange the record order so records you have access to return first.

**Note:** Unusually large **sysparm\_limit** values can impact system performance.

Data type: Number

Default: 10000

</td></tr><tr id="row_sysparm_offset"><td>

sysparm\_offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

Default: 0

</td></tr><tr><td>

sysparm\_query

</td><td>

Encoded query used to filter the result set.For example:

`(sysparm_query=caller_id=javascript:gs.getUserID()^active=true)`

The encoded query supports order by. To sort responses based on certain fields, use the ORDERBY and ORDERBYDESC clauses in **sysparm\_query**. For example, `sysparm_query=active=true^ORDERBYnumber^ORDERBYDESCcategory` filters all active records and orders the results in ascending order by number first, and then in descending order by category.

If part of the query is invalid, such as by specifying an invalid field name, the instance ignores the invalid part. It then returns rows using only the valid portion of the query. You can control this behavior using the property **glide.invalid\_query.returns\_no\_rows**. Set this property to true to return no rows on an invalid query.

**Note:** The **glide.invalid\_query.returns\_no\_rows** property controls the behavior of all queries across the instance, such as in lists, scripts \(GlideRecord.query\(\)\), and web service APIs.

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Content-Type|Data format of the request body. Only supports **application/json**.|

<table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Content-Range

</td><td>

Range of content returned in a paginated call. For example, if offset=2 and limit=3, the value of the Content-Range header is items 3-5.

</td></tr><tr><td>

Links

</td><td>

Links through which to navigate the query results: -   first
-   last
-   next
-   previous
-   self

</td></tr><tr><td>

Total-Count

</td><td>

Total number of filtered records.

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Request was successfully processed. All responses returned \(no pagination\).

</td></tr><tr><td>

206

</td><td>

Request successfully processed. Partial resource returned in response \(with pagination\).

</td></tr><tr><td>

400

</td><td>

Error. Possible reasons:-   Invalid limit/limit greater than maximum allowed.
-   Invalid offset.

</td></tr><tr><td>

403

</td><td>

Record denied access. Insufficient permission to query the record.

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request.

</td></tr></tbody>
</table>### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td id="lead-account-entry">

Account linked to the lead.Data type: Object

```
"account": { 
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

account.name

</td><td id="lead-account.name-entry">

Name of the account.Data type: String

</td></tr><tr><td>

account.sys\_id

</td><td id="lead-account.sys_id-entry">

Sys\_id of the associated account record.

Data type: String

 Table: Account \[customer\_account\]

</td></tr><tr><td>

business\_phone

</td><td id="lead-business_phone-entry">

Lead's business phone number.Data type: String

</td></tr><tr><td>

city

</td><td id="lead-city-entry">

City in which the lead resides.Data type: String

</td></tr><tr><td>

closed\_date

</td><td id="lead-closed_date-entry">

Date and time when the lead was closed.Data type: Object

```
"closed_date": {
  "display_value": "String", 
  "value": "String"
} 
```

</td></tr><tr><td>

closed\_date.​display\_value

</td><td id="lead-closed_date.display_value-entry">

Date and time as displayed in the UI. Data type: String

Format: User's format and time zone.

</td></tr><tr><td>

closed\_date.value

</td><td id="lead-closed_date.value-entry">

Date and time that the lead closed as defined in the associated record.Data type: String

Format: UTC

</td></tr><tr><td>

company

</td><td id="lead-company-entry">

Lead's company name.Data type: String

</td></tr><tr><td>

consumer

</td><td id="lead-consumer-entry">

Consumer associated with the lead.Data type: Object

```
"consumer": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

consumer.name

</td><td id="lead-consumer.name-entry">

Name of the associated consumer.Data type: String

</td></tr><tr><td>

consumer.sys\_id

</td><td id="lead-consumer.sys_id-entry">

Sys\_id of the associated consumer record.

Data type: String

 Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

contact

</td><td id="lead-contact-entry">

Contact associated with the lead account.Data type: Object

```
"contact": {
  "name": "String",
  "sys_id": "String" 
} 
```

</td></tr><tr><td>

contact.name

</td><td id="lead-contact.name-entry">

Contact's name.Data type: String

</td></tr><tr><td>

contact.sys\_id

</td><td id="lead-contact.sys_id-entry">

Sys\_id of the associated contact record.

Data type: String

 Table: Contact \[customer\_contact\]

</td></tr><tr><td>

country

</td><td id="lead-country-entry">

Country in which the lead resides.Data type: String

</td></tr><tr><td>

do\_not\_call

</td><td id="lead-do_not_call-entry">

Flag that indicates whether the mode of communication is by phone.

Valid values:

-   true: Can call contact.
-   false: Don't call contact.

Data type: Boolean

</td></tr><tr><td>

do\_not\_email

</td><td id="lead-do_not_email-entry">

Flag that indicates whether the mode of communication is by email.

Valid values:

-   true: Can email contact.
-   false: Don't email contact.

Data type: Boolean

</td></tr><tr><td>

do\_not\_share

</td><td id="lead-do_not_share-entry">

Flag that indicates whether the lead details can be shared.

Valid values:

-   true: Lead details can be shared.
-   false: Lead details can't be shared.

Data type: Boolean

</td></tr><tr><td>

email

</td><td id="lead-email-entry">

Lead's email address.Data type: String

</td></tr><tr><td>

external\_id

</td><td id="lead-external_id-entry">

ID used by the system that generated the lead to identify the lead in the associated system.Data type: String

</td></tr><tr><td>

external\_system

</td><td id="lead-external_system-entry">

Name of the external system associated with the lead, such as HubSpot or pipedrive.Data type: String

</td></tr><tr><td>

first\_name

</td><td id="lead-first_name-entry">

First name of the contact associated with the lead.Data type: String

</td></tr><tr><td>

industry

</td><td id="lead-industry-entry">

Industry to which the lead belongs.Data type: String

Table: Located in the **industry** field of the Account \[customer\_account\] table.

</td></tr><tr><td>

last\_name

</td><td id="lead-last_name-entry">

Last name of the contact associated with the lead.

Data type: String

</td></tr><tr><td>

lead\_group

</td><td id="lead-lead_group-entry">

Group to which the lead belongs.

Data type: Object

 ```
"lead_group": {
  "name: "String",
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_group.name

</td><td id="lead-lead_group.name-entry">

Lead group's name.Data type: String

</td></tr><tr><td>

lead\_group.sys\_id

</td><td id="lead-lead_group.sys_id-entry">

Sys\_id of the lead group record.Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

lead\_line\_items

</td><td id="lead-lead_line_items-entry">

Details of the lead line items associated with the lead.Data type: Array of Objects

```
"lead_line_items": [ 
  { 
    "external_id": "String", 
    "external_system": "String",
    "lead": {Object},
    "number": "String",
    "product_offering": {Object},
    "quantity": Number,
    "sys_created_by”: "String",
    "sys_created_on {Object},
    "sys_domain": "String",
    "sys_domain_path": "String",
    "sys_id": "String",
    "sys_mod_count": Number,
    "sys_tags": [Array],
    "sys_updated_by: "String",
    "sys_updated_on: {Object},
    "unit_of_measurement": {Object}, 
    "work_notes": [Array]
  } 
] 
```

</td></tr><tr><td>

lead\_line\_items.​external\_id

</td><td id="lead-lead_line_items.external_id-entry">

ID used by the system that generated the lead line item to identify the line item in the associated system.Data type: String

</td></tr><tr><td>

lead\_line\_items.​external\_system

</td><td id="lead-lead_line_items.external_system-entry">

Name of the external system associated with the lead line item, such as HubSpot or pipedrive.Data type: String

</td></tr><tr><td>

lead\_line\_items.​lead

</td><td id="lead-lead_line_items.lead-entry">

Details about the lead associated with the line item.Data type: Object

```
"lead: {
  "name": "String",
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​lead.name

</td><td id="lead-lead_line_items.lead.name-entry">

Associated lead's name.Data type: String

</td></tr><tr><td>

lead\_line\_items.​lead.sys\_id

</td><td id="lead-lead_line_items.lead.sys_id-entry">

Sys\_id of the associated lead record.Data type: String

</td></tr><tr><td>

lead\_line\_items.​number

</td><td id="lead-lead_line_items.number-entry">

Unique system-generated number of the lead line item record.Data type: String

</td></tr><tr><td>

lead\_line\_items.​product\_offering

</td><td id="lead-lead_line_items.product_offering-entry">

Information about the product offering associated with the lead line item.Data type: Object

```
"product_offering": {
  "code": " String",
  "name": "String",
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​product\_offering.code

</td><td id="lead-lead_line_items.product_offering.code-entry">

Code linked to the product offering. **Note:** This is a system-generated alphanumeric number based on the product name. Although system generated, you can edit the code to represent a SKU or any other industry specific product codes.

Data type: String

</td></tr><tr><td>

lead\_line\_items.​product\_offering.name

</td><td id="lead-lead_line_items.product_offering.name-entry">

Product offering's name.Data type: String

</td></tr><tr><td>

lead\_line\_items.​product\_offering.sys\_id

</td><td id="lead-lead_line_items.product_offering.sys_id-entry">

Sys\_id of the product offering record associated with the lead line item.

Data type: String

 Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

lead\_line\_items.​quantity

</td><td id="lead-lead_line_items.quantity-entry">

Quantity of items the lead wants to purchase of the associated product offering.

Data type: Number \(Integer\)

</td></tr><tr><td>

lead\_line\_items.​sys\_created\_by

</td><td id="lead-lead_line_items.sys_created_by-entry">

User name of the person that created the lead line item.Data type: String

</td></tr><tr><td>

lead\_line\_items.​sys\_created\_on

</td><td id="lead-lead_line_items.sys_created_on-entry">

System-generated date and time that the lead line item was created.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "value": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​sys\_created\_on.display\_value

</td><td id="lead-lead_line_items.sys_created_on.display_value-entry">

Date and time that the lead line item was created.Data type: String

Format: Default instance format and time zone

</td></tr><tr><td>

lead\_line\_items.​sys\_created\_on.value

</td><td id="lead-lead_line_items.sys_created_on.value-entry">

Date and time that the lead line item was created.Data type: String

Format: UTC

</td></tr><tr><td>

lead\_line\_items.​sys\_domain

</td><td id="lead-lead_line_items.sys_domain-entry">

Sys\_id of the domain record to which the lead line item belongs. **Note:** This parameter is only returned in the response if domain separation is enabled.

Data type: String

</td></tr><tr><td>

lead\_line\_items.sys\_domain\_path

</td><td id="lead-lead_line_items.sys_domain_path-entry">

Path of the domain to which the lead line item belongs. **Note:** This parameter is only returned in the response if domain separation is enabled.

Data type: String

</td></tr><tr><td>

lead\_line\_items.​sys\_id

</td><td id="lead-lead_line_items.sys_id-entry">

Sys\_id of the lead line item record.Data type: String

</td></tr><tr><td>

lead\_line\_items.​sys\_mod\_count

</td><td id="lead-lead_line_items.sys_mod_count-entry">

Number of times the associated lead line item record has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

lead\_line\_items.​sys\_tags

</td><td id="lead-lead_line_items.sys_tags-entry">

List of system tags associated with the lead line item.Data type: Array

</td></tr><tr><td>

lead\_line\_items.​sys\_updated\_by

</td><td id="lead-lead_line_items.sys_updated_by-entry">

User name of the person that last updated the associated lead line item.Data type: String

</td></tr><tr><td>

lead\_line\_items.​sys\_updated\_on

</td><td id="lead-lead_line_items.sys_updated_on-entry">

System-generated date and time when the lead line item was last updated.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "value": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​sys\_updated\_on.​display\_value

</td><td id="lead-lead_line_items.sys_updated_on.display_value-entry">

Date and time that the lead line item was last updated.Data type: String

Format: Default instance format and time zone

</td></tr><tr><td>

lead\_line\_items.​sys\_updated\_on.​value

</td><td id="lead-lead_line_items.sys_updated_on.value-entry">

Date and time that the lead line item was last updated.Data type: String

Format: UTC

</td></tr><tr><td>

lead\_line\_items.​unit\_of\_measurement

</td><td id="lead-lead_line_items.unit_of_measurement-entry">

Details of the measuring unit of lead line item.

Data type: Object

 ```
"unit_of_measurement": {
  "name": "String",
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​unit\_of\_measurement.​name

</td><td id="lead-lead_line_items.unit_of_measurement.name-entry">

Name of the measuring unit such as, each or cubic foot.Data type: String

</td></tr><tr><td>

lead\_line\_items.​unit\_of\_measurement.​sys\_id

</td><td id="lead-lead_line_items.unit_of_measurement.sys_id-entry">

Sys\_id of the record that describes the measuring unit.Data type: String

Table: Unit of Measure \[sn\_prd\_pm\_uom\]

</td></tr><tr><td>

lead\_line\_items.​work\_notes

</td><td id="lead-lead_line_items.work_notes-entry">

List that describes the work notes created for the lead line item.

Data type: Array of Objects

 ```
"work_notes": [
  {
    "author": "String",
    "date": "String",
    "text": "String"
  }
]
```

</td></tr><tr><td>

lead\_line\_items.​work\_notes.​author

</td><td id="lead-lead_line_items.work_notes.author-entry">

User name of the person that authored the associated work note.Data type: String

</td></tr><tr><td>

lead\_line\_items.​work\_notes.​date

</td><td id="lead-lead_line_items.work_notes.date-entry">

Date that the note was created.Data type: String

</td></tr><tr><td>

lead\_line\_items.​work\_notes.​text

</td><td id="lead-lead_line_items.work_notes.text-entry">

Text of the note made by the author.Data type: String

</td></tr><tr><td>

lead\_rating

</td><td id="lead-lead_rating-entry">

Rating for the lead such as, 100\_cold, 200\_warm, 300\_hot, or 400\_super\_hot.**Note:** This is a choice field. It must contain one of the choice items defined in the lead\_rating field of the Leads table.

Data type: String

</td></tr><tr><td>

lead\_score

</td><td id="lead-lead_score-entry">

Score for the lead.Data type: Decimal

Range: 1 to 100

</td></tr><tr><td>

lead\_source

</td><td id="lead-lead_source-entry">

Originator of the lead.**Note:** This is a choice field. It must contain one of the choice items defined in the lead\_source field of the Leads table.

Data type: String

</td></tr><tr><td>

lead\_type

</td><td id="lead-lead_type-entry">

Type of lead, such as New Business or Existing Business.

 **Note:** This is a choice field. It must contain one of the choice items defined in the lead\_type field of the Leads table.

 Data type: String

</td></tr><tr><td>

middle\_name

</td><td id="lead-middle_name-entry">

Middle name of the contact for the lead.Data type: String

</td></tr><tr><td>

mobile\_phone

</td><td id="lead-mobile_phone-entry">

Phone number of the contact for the lead.Data type: String

</td></tr><tr><td>

number

</td><td id="lead-number-entry">

Unique system-generated number of the lead record.Data type: String

</td></tr><tr><td>

other\_reason

</td><td id="lead-other_reason-entry">

Additional reason for the lead disqualification.Data type: String

Max length: 160 characters

</td></tr><tr><td>

owner

</td><td id="lead-owner-entry">

Details of the person associated with the lead.

Data type: Object

 ```
"owner": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

owner.name

</td><td id="lead-owner.name-entry">

Name of the person that owns the lead.Data type: String

</td></tr><tr><td>

owner.sys\_id

</td><td id="lead-owner.sys_id-entry">

Sys\_id of the user record of the person that owns the lead.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

reason

</td><td id="lead-reason-entry">

Reason for the lead disqualification such as, Disqualify.Data type: String

Max length: 40 characters

</td></tr><tr><td>

short\_description

</td><td id="lead-short_description-entry">

Short description of the lead.Data type: String

Max length: 160 characters

</td></tr><tr><td>

similar\_lead

</td><td id="lead-similar_lead-entry">

Details on any similar lead. Use this for possible lead disqualification.

Data type: Object

 ```
"similar_lead": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

similar\_lead.name

</td><td id="lead-similar_lead.name-entry">

Name of the duplicate lead.Data type: String

</td></tr><tr><td>

similar\_lead.sys\_id

</td><td id="lead-similar_lead.sys_id-entry">

Sys\_id of the lead record that is a possible duplicate lead.Data type: String

Table: Lead \[sn\_lead\_mgmt\_core\_lead\]

</td></tr><tr><td>

stage

</td><td id="lead-stage-entry">

Stage of the lead such as, 100\_new.

**Note:** This is a choice field. It must contain one of the choice items defined in the stage field of the Leads table.

Data type: String

</td></tr><tr><td>

state

</td><td id="lead-state-entry">

State in which the lead resides.Data type: String

</td></tr><tr><td>

street

</td><td id="lead-street-entry">

Street on which the lead resides.Data type: String

</td></tr><tr><td>

sys\_class\_name

</td><td id="lead-sys_class_name-entry">

System-generated class name of the Lead table.Data type: String

</td></tr><tr><td>

sys\_created\_by

</td><td id="lead-sys_created_by-entry">

User name of the person that created the lead.Data type: String

</td></tr><tr><td>

sys\_created\_on

</td><td id="lead-sys_created_on-entry">

System-generated date and time that the lead was created.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "value": "String"
} 
```

</td></tr><tr><td>

sys\_created\_on.​display\_value

</td><td id="lead-sys_created_on.display_value-entry">

Date and time when the lead was created.Data type: String

Format: Default instance format and time zone

</td></tr><tr><td>

sys\_created\_on.​value

</td><td id="lead-sys_created_on.value-entry">

Date and time when the lead was created.Data type: String

Format: UTC

</td></tr><tr><td>

sys\_domain

</td><td id="lead-sys_domain-entry">

Sys\_id of the domain record to which the lead belongs. **Note:** This parameter is only returned in the response if domain separation is enabled.

Data type: String

</td></tr><tr><td>

sys\_domain\_path

</td><td id="lead-sys_domain_path-entry">

Path of the domain to which the lead belongs. **Note:** This parameter is only returned in the response if domain separation is enabled.

Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="lead-sys_id-entry">

Sys\_id of the lead record.Data type: String

Table: Lead \[sn\_lead\_mgmt\_core\_lead\]

</td></tr><tr><td>

sys\_mod\_count

</td><td id="lead-sys_mod_count-entry">

Number of times the associated lead record has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

sys\_tags

</td><td id="lead-sys_tags-entry">

List of system tags associated with the lead. You can use these tags to categorize leads.Data type: Array

</td></tr><tr><td>

sys\_updated\_by

</td><td id="lead-sys_updated_by-entry">

User name of the person that last updated the lead record.Data type: String

</td></tr><tr><td>

sys\_updated\_on

</td><td id="lead-sys_updated_on-entry">

System-generated date and time when the lead was last updated.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "value": "String"
} 
```

</td></tr><tr><td>

sys\_updated\_on.​display\_value

</td><td id="lead-sys_updated_on.display_value-entry">

Date and time that the lead was last updated.Data type: String

Format: Instance's default format and time zone

</td></tr><tr><td>

sys\_updated\_on.​value

</td><td id="lead-sys_updated_on.value-entry">

Date and time that the lead was last updated.Data type: String

Format: UTC

</td></tr><tr><td>

title

</td><td id="lead-title-entry">

Lead's title.Data type: String

</td></tr><tr><td>

website

</td><td id="lead-website-entry">

Lead's website URL.Data type: String

</td></tr><tr><td>

work\_notes

</td><td id="lead-work_notes-entry">

List of work notes created for the lead.

Data type: Array of Objects

 ```
"work_notes": [
  {
    "author": "String",
    "date": "String",
    "text": "String"
  }
]
```

</td></tr><tr><td>

work\_notes.​author

</td><td id="lead-work_notes.author-entry">

User name of the person that authored the associated work note.Data type: String

</td></tr><tr><td>

work\_notes.​date

</td><td id="lead-work_notes.date-entry">

Date that the note was created.Data type: String

</td></tr><tr><td>

work\_notes.​text

</td><td id="lead-work_notes.text-entry">

Text of the note made by the author.Data type: String

</td></tr><tr><td>

zip

</td><td id="lead-zip-entry">

Zip code of the associated lead.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to pass query parameters to specify the leads to return.

```
curl "https://instance.service-now.com/api/sn_lead_mgmt_core/lead?sysparm_query=stage%3D400_closed_won&sysparm_fields=sys_id%2Cfirst_name%2Clast_name%2Cshort_description%2Cstage%2Clead_line_items&sysparm_offset=2" \ 
--request GET \ 
--header "Accept:application/json" \ 
--user "username":"password"
```

Leads are return in an array of objects:

```
[
  {
    "short_description": "Looking for a quote on preventative maintenance plans for their corporate office building elevators.",
    "reason": null,
    "country": "USA",
    "closed_date": null,
    "city": "San Francisco",
    "lead_source": "inbound_phone",
    "external_id": null,
    "industry": "manufacturing",
    "sys_updated_on": {
      "value": "2024-05-31 11:01:55",
      "display_value": "2024-05-31 04:01:55"
    },
    "title": "Director of Building operations",
    "sys_class_name": "Lead",
    "number": "LEAD0000001",
    "sys_id": "856b6a95ffde8210b85dffffffffffd7",
    "business_phone": "+1 (555) 123-4567",
    "similar_lead": null,
    "sys_updated_by": "admin",
    "mobile_phone": null,
    "street": "789, Industrial drive",
    "sys_created_on": {
      "value": "2024-05-20 10:32:41",
      "display_value": "2024-05-20 03:32:41"
    },
    "contact": null,
    "company": "Lee Manufacturing Inc",
    "state": "CA",
    "first_name": "James",
    "email": "james.wilson@email.com",
    "consumer": null,
    "sys_created_by": "admin",
    "zip": "94016",
    "owner": {
      "sys_id": "60058fe943fe3110d6c6cd60afb8f203",
      "name": "Max Blaze"
    },
    "website": null,
    "lead_group": null,
    "sys_mod_count": 1,
    "last_name": "Wilson",
    "other_reason": null,
    "middle_name": null,
    "sys_tags": null,
    "do_not_share": false,
    "lead_score": 92,
    "stage": "300_nurturing",
    "do_not_email": false,
    "lead_type": null,
    "work_notes": [
      {
        "author": "Abel Tuter",
        "date": "2024-12-04 06:52:07",
        "text": "Work notes for lead"
      }
    ],
    "do_not_call": false,
    "lead_rating": "400_super_hot",
    "account": null,
    "external_system": null,
    "lead_line_items": [
      {
        "quantity": 6,
        "product_offering": {
          "sys_id": "32619d9fd0a63110f8770dbf976be1f9",
          "name": "Safety Test Coverage",
          "code": "SAFETSTCVG1"
        },
        "sys_mod_count": 0,
        "external_id": null,
        "sys_updated_on": {
          "value": "2024-05-20 10:38:41",
          "display_value": "2024-05-20 03:38:41"
        },
        "sys_tags": null,
        "lead": {
          "sys_id": "856b6a95ffde8210b85dffffffffffd7",
          "name": "LEAD0000001"
        },
        "number": "LEADL0000003",
        "sys_id": "013daa19ffde8210b85dffffffffff82",
        "unit_of_measurement": {
          "sys_id": "cb2795d553020110286eddeeff7b12ff",
          "name": "Each"
        },
        "sys_updated_by": "admin",
        "sys_created_on": {
          "value": "2024-05-20 10:38:41",
          "display_value": "2024-05-20 03:38:41"
        },
        "work_notes": null,
        "sys_created_by": "admin",
        "external_system": null
      }
    ]
  },
  {
    "short_description": "Partner referral for a company interested in a reliable internet bundle with strong security features for their office.",
    "reason": null,
    "country": "USA",
    "closed_date": null,
    "city": "San Francisco",
    "lead_source": "partner_referral",
    "external_id": null,
    "industry": "technology_services",
    "sys_updated_on": {
      "value": "2024-05-20 10:53:59",
      "display_value": "2024-05-20 03:53:59"
    },
    "title": "IT Director",
    "sys_class_name": "Lead",
    "number": "LEAD0000002",
    "sys_id": "e71fa6d9ffde8210b85dffffffffff51",
    "business_phone": "(626) 722-6969",
    "similar_lead": null,
    "sys_updated_by": "admin",
    "mobile_phone": null,
    "street": "747 Howard St",
    "sys_created_on": {
      "value": "2024-05-20 10:49:12",
      "display_value": "2024-05-20 03:49:12"
    },
    "contact": {
      "sys_id": "4d147a386f0331003b3c498f5d3ee437",
      "name": ""
    },
    "company": "Boxeo",
    "state": "CA",
    "first_name": "Julie",
    "email": "julie.lewis@example.com",
    "consumer": null,
    "sys_created_by": "admin",
    "zip": "94013",
    "owner": {
      "sys_id": "60058fe943fe3110d6c6cd60afb8f203",
      "name": "Max Blaze"
    },
    "website": null,
    "lead_group": null,
    "sys_mod_count": 0,
    "last_name": "Lewis",
    "other_reason": null,
    "middle_name": null,
    "sys_tags": null,
    "do_not_share": false,
    "lead_score": 78,
    "stage": "400_closed_won",
    "do_not_email": false,
    "lead_type": null,
    "work_notes": [
      {
        "author": "Abel Tuter",
        "date": "2024-12-03 03:52:51",
        "text": "Work noted for LEAD0000002"
      }
    ],
    "do_not_call": false,
    "lead_rating": "200_warm",
    "account": {
      "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
      "name": ""
    },
    "external_system": null,
    "lead_line_items": [
      {
        "quantity": 50,
        "product_offering": {
          "sys_id": "0b61dd9fd0a63110f8770dbf976be171",
          "name": "Solana Modem M Series",
          "code": "SOLANAMODE2"
        },
        "sys_mod_count": 0,
        "external_id": null,
        "sys_updated_on": { 
          "value": "2024-05-20 10:51:57",
          "display_value": "2024-05-20 03:51:57"
        },
        "sys_tags": null,
        "lead": {
          "sys_id": "e71fa6d9ffde8210b85dffffffffff51",
          "name": "LEAD0000002"
        },
        "number": "LEADL0000009",
        "sys_id": "2130fa1dffde8210b85dffffffffffff",
        "unit_of_measurement": {
          "sys_id": "cb2795d553020110286eddeeff7b12ff",
          "name": "Each"
        },
        "sys_updated_by": "admin",
        "sys_created_on": { 
          "value": "2024-05-20 10:51:25", 
          "display_value": "2024-05-20 03:51:25"
        },
        "work_notes": null,
        "sys_created_by": "admin",
        "external_system": null
      } 
    ]
  }
] 
```

## lead - GET /sn\_lead\_mgmt\_core/lead/\{sys\_id\}

Returns the lead record and all associated lead line items for the specified sys\_id.

This endpoint retrieves information from the following tables:

-   Lead \[sn\_lead\_mgmt\_core\_lead\]
-   Lead Line Item \[sn\_lead\_mgmt\_core\_lead\_line\_item\]

### URL format

Versioned URL: `/api/sn_lead_mgmt_core/{api_version}/lead/{sys_id}`

Default URL: `/api/sn_lead_mgmt_core/{api_version}/lead/{sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the lead to retrieve.Data type: String

Table: Lead \[sn\_lead\_mgmt\_core\_lead\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="table_h4v_1hp_sdc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td id="lead-account-entry">

Account linked to the lead.Data type: Object

```
"account": { 
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

account.name

</td><td id="lead-account.name-entry">

Name of the account.Data type: String

</td></tr><tr><td>

account.sys\_id

</td><td id="lead-account.sys_id-entry">

Sys\_id of the associated account record.

Data type: String

 Table: Account \[customer\_account\]

</td></tr><tr><td>

business\_phone

</td><td id="lead-business_phone-entry">

Lead's business phone number.Data type: String

</td></tr><tr><td>

city

</td><td id="lead-city-entry">

City in which the lead resides.Data type: String

</td></tr><tr><td>

closed\_date

</td><td id="lead-closed_date-entry">

Date and time when the lead was closed.Data type: Object

```
"closed_date": {
  "display_value": "String", 
  "value": "String"
} 
```

</td></tr><tr><td>

closed\_date.​display\_value

</td><td id="lead-closed_date.display_value-entry">

Date and time as displayed in the UI. Data type: String

Format: User's format and time zone.

</td></tr><tr><td>

closed\_date.value

</td><td id="lead-closed_date.value-entry">

Date and time that the lead closed as defined in the associated record.Data type: String

Format: UTC

</td></tr><tr><td>

company

</td><td id="lead-company-entry">

Lead's company name.Data type: String

</td></tr><tr><td>

consumer

</td><td id="lead-consumer-entry">

Consumer associated with the lead.Data type: Object

```
"consumer": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

consumer.name

</td><td id="lead-consumer.name-entry">

Name of the associated consumer.Data type: String

</td></tr><tr><td>

consumer.sys\_id

</td><td id="lead-consumer.sys_id-entry">

Sys\_id of the associated consumer record.

Data type: String

 Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

contact

</td><td id="lead-contact-entry">

Contact associated with the lead account.Data type: Object

```
"contact": {
  "name": "String",
  "sys_id": "String" 
} 
```

</td></tr><tr><td>

contact.name

</td><td id="lead-contact.name-entry">

Contact's name.Data type: String

</td></tr><tr><td>

contact.sys\_id

</td><td id="lead-contact.sys_id-entry">

Sys\_id of the associated contact record.

Data type: String

 Table: Contact \[customer\_contact\]

</td></tr><tr><td>

country

</td><td id="lead-country-entry">

Country in which the lead resides.Data type: String

</td></tr><tr><td>

do\_not\_call

</td><td id="lead-do_not_call-entry">

Flag that indicates whether the mode of communication is by phone.

Valid values:

-   true: Can call contact.
-   false: Don't call contact.

Data type: Boolean

</td></tr><tr><td>

do\_not\_email

</td><td id="lead-do_not_email-entry">

Flag that indicates whether the mode of communication is by email.

Valid values:

-   true: Can email contact.
-   false: Don't email contact.

Data type: Boolean

</td></tr><tr><td>

do\_not\_share

</td><td id="lead-do_not_share-entry">

Flag that indicates whether the lead details can be shared.

Valid values:

-   true: Lead details can be shared.
-   false: Lead details can't be shared.

Data type: Boolean

</td></tr><tr><td>

email

</td><td id="lead-email-entry">

Lead's email address.Data type: String

</td></tr><tr><td>

external\_id

</td><td id="lead-external_id-entry">

ID used by the system that generated the lead to identify the lead in the associated system.Data type: String

</td></tr><tr><td>

external\_system

</td><td id="lead-external_system-entry">

Name of the external system associated with the lead, such as HubSpot or pipedrive.Data type: String

</td></tr><tr><td>

first\_name

</td><td id="lead-first_name-entry">

First name of the contact associated with the lead.Data type: String

</td></tr><tr><td>

industry

</td><td id="lead-industry-entry">

Industry to which the lead belongs.Data type: String

Table: Located in the **industry** field of the Account \[customer\_account\] table.

</td></tr><tr><td>

last\_name

</td><td id="lead-last_name-entry">

Last name of the contact associated with the lead.

Data type: String

</td></tr><tr><td>

lead\_group

</td><td id="lead-lead_group-entry">

Group to which the lead belongs.

Data type: Object

 ```
"lead_group": {
  "name: "String",
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_group.name

</td><td id="lead-lead_group.name-entry">

Lead group's name.Data type: String

</td></tr><tr><td>

lead\_group.sys\_id

</td><td id="lead-lead_group.sys_id-entry">

Sys\_id of the lead group record.Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

lead\_line\_items

</td><td id="lead-lead_line_items-entry">

Details of the lead line items associated with the lead.Data type: Array of Objects

```
"lead_line_items": [ 
  { 
    "external_id": "String", 
    "external_system": "String",
    "lead": {Object},
    "number": "String",
    "product_offering": {Object},
    "quantity": Number,
    "sys_created_by”: "String",
    "sys_created_on {Object},
    "sys_domain": "String",
    "sys_domain_path": "String",
    "sys_id": "String",
    "sys_mod_count": Number,
    "sys_tags": [Array],
    "sys_updated_by: "String",
    "sys_updated_on: {Object},
    "unit_of_measurement": {Object}, 
    "work_notes": [Array]
  } 
] 
```

</td></tr><tr><td>

lead\_line\_items.​external\_id

</td><td id="lead-lead_line_items.external_id-entry">

ID used by the system that generated the lead line item to identify the line item in the associated system.Data type: String

</td></tr><tr><td>

lead\_line\_items.​external\_system

</td><td id="lead-lead_line_items.external_system-entry">

Name of the external system associated with the lead line item, such as HubSpot or pipedrive.Data type: String

</td></tr><tr><td>

lead\_line\_items.​lead

</td><td id="lead-lead_line_items.lead-entry">

Details about the lead associated with the line item.Data type: Object

```
"lead: {
  "name": "String",
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​lead.name

</td><td id="lead-lead_line_items.lead.name-entry">

Associated lead's name.Data type: String

</td></tr><tr><td>

lead\_line\_items.​lead.sys\_id

</td><td id="lead-lead_line_items.lead.sys_id-entry">

Sys\_id of the associated lead record.Data type: String

</td></tr><tr><td>

lead\_line\_items.​number

</td><td id="lead-lead_line_items.number-entry">

Unique system-generated number of the lead line item record.Data type: String

</td></tr><tr><td>

lead\_line\_items.​product\_offering

</td><td id="lead-lead_line_items.product_offering-entry">

Information about the product offering associated with the lead line item.Data type: Object

```
"product_offering": {
  "code": " String",
  "name": "String",
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​product\_offering.code

</td><td id="lead-lead_line_items.product_offering.code-entry">

Code linked to the product offering. **Note:** This is a system-generated alphanumeric number based on the product name. Although system generated, you can edit the code to represent a SKU or any other industry specific product codes.

Data type: String

</td></tr><tr><td>

lead\_line\_items.​product\_offering.name

</td><td id="lead-lead_line_items.product_offering.name-entry">

Product offering's name.Data type: String

</td></tr><tr><td>

lead\_line\_items.​product\_offering.sys\_id

</td><td id="lead-lead_line_items.product_offering.sys_id-entry">

Sys\_id of the product offering record associated with the lead line item.

Data type: String

 Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

lead\_line\_items.​quantity

</td><td id="lead-lead_line_items.quantity-entry">

Quantity of items the lead wants to purchase of the associated product offering.

Data type: Number \(Integer\)

</td></tr><tr><td>

lead\_line\_items.​sys\_created\_by

</td><td id="lead-lead_line_items.sys_created_by-entry">

User name of the person that created the lead line item.Data type: String

</td></tr><tr><td>

lead\_line\_items.​sys\_created\_on

</td><td id="lead-lead_line_items.sys_created_on-entry">

System-generated date and time that the lead line item was created.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "value": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​sys\_created\_on.display\_value

</td><td id="lead-lead_line_items.sys_created_on.display_value-entry">

Date and time that the lead line item was created.Data type: String

Format: Default instance format and time zone

</td></tr><tr><td>

lead\_line\_items.​sys\_created\_on.value

</td><td id="lead-lead_line_items.sys_created_on.value-entry">

Date and time that the lead line item was created.Data type: String

Format: UTC

</td></tr><tr><td>

lead\_line\_items.​sys\_domain

</td><td id="lead-lead_line_items.sys_domain-entry">

Sys\_id of the domain record to which the lead line item belongs. **Note:** This parameter is only returned in the response if domain separation is enabled.

Data type: String

</td></tr><tr><td>

lead\_line\_items.sys\_domain\_path

</td><td id="lead-lead_line_items.sys_domain_path-entry">

Path of the domain to which the lead line item belongs. **Note:** This parameter is only returned in the response if domain separation is enabled.

Data type: String

</td></tr><tr><td>

lead\_line\_items.​sys\_id

</td><td id="lead-lead_line_items.sys_id-entry">

Sys\_id of the lead line item record.Data type: String

</td></tr><tr><td>

lead\_line\_items.​sys\_mod\_count

</td><td id="lead-lead_line_items.sys_mod_count-entry">

Number of times the associated lead line item record has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

lead\_line\_items.​sys\_tags

</td><td id="lead-lead_line_items.sys_tags-entry">

List of system tags associated with the lead line item.Data type: Array

</td></tr><tr><td>

lead\_line\_items.​sys\_updated\_by

</td><td id="lead-lead_line_items.sys_updated_by-entry">

User name of the person that last updated the associated lead line item.Data type: String

</td></tr><tr><td>

lead\_line\_items.​sys\_updated\_on

</td><td id="lead-lead_line_items.sys_updated_on-entry">

System-generated date and time when the lead line item was last updated.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "value": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​sys\_updated\_on.​display\_value

</td><td id="lead-lead_line_items.sys_updated_on.display_value-entry">

Date and time that the lead line item was last updated.Data type: String

Format: Default instance format and time zone

</td></tr><tr><td>

lead\_line\_items.​sys\_updated\_on.​value

</td><td id="lead-lead_line_items.sys_updated_on.value-entry">

Date and time that the lead line item was last updated.Data type: String

Format: UTC

</td></tr><tr><td>

lead\_line\_items.​unit\_of\_measurement

</td><td id="lead-lead_line_items.unit_of_measurement-entry">

Details of the measuring unit of lead line item.

Data type: Object

 ```
"unit_of_measurement": {
  "name": "String",
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​unit\_of\_measurement.​name

</td><td id="lead-lead_line_items.unit_of_measurement.name-entry">

Name of the measuring unit such as, each or cubic foot.Data type: String

</td></tr><tr><td>

lead\_line\_items.​unit\_of\_measurement.​sys\_id

</td><td id="lead-lead_line_items.unit_of_measurement.sys_id-entry">

Sys\_id of the record that describes the measuring unit.Data type: String

Table: Unit of Measure \[sn\_prd\_pm\_uom\]

</td></tr><tr><td>

lead\_line\_items.​work\_notes

</td><td id="lead-lead_line_items.work_notes-entry">

List that describes the work notes created for the lead line item.

Data type: Array of Objects

 ```
"work_notes": [
  {
    "author": "String",
    "date": "String",
    "text": "String"
  }
]
```

</td></tr><tr><td>

lead\_line\_items.​work\_notes.​author

</td><td id="lead-lead_line_items.work_notes.author-entry">

User name of the person that authored the associated work note.Data type: String

</td></tr><tr><td>

lead\_line\_items.​work\_notes.​date

</td><td id="lead-lead_line_items.work_notes.date-entry">

Date that the note was created.Data type: String

</td></tr><tr><td>

lead\_line\_items.​work\_notes.​text

</td><td id="lead-lead_line_items.work_notes.text-entry">

Text of the note made by the author.Data type: String

</td></tr><tr><td>

lead\_rating

</td><td id="lead-lead_rating-entry">

Rating for the lead such as, 100\_cold, 200\_warm, 300\_hot, or 400\_super\_hot.**Note:** This is a choice field. It must contain one of the choice items defined in the lead\_rating field of the Leads table.

Data type: String

</td></tr><tr><td>

lead\_score

</td><td id="lead-lead_score-entry">

Score for the lead.Data type: Decimal

Range: 1 to 100

</td></tr><tr><td>

lead\_source

</td><td id="lead-lead_source-entry">

Originator of the lead.**Note:** This is a choice field. It must contain one of the choice items defined in the lead\_source field of the Leads table.

Data type: String

</td></tr><tr><td>

lead\_type

</td><td id="lead-lead_type-entry">

Type of lead, such as New Business or Existing Business.

 **Note:** This is a choice field. It must contain one of the choice items defined in the lead\_type field of the Leads table.

 Data type: String

</td></tr><tr><td>

middle\_name

</td><td id="lead-middle_name-entry">

Middle name of the contact for the lead.Data type: String

</td></tr><tr><td>

mobile\_phone

</td><td id="lead-mobile_phone-entry">

Phone number of the contact for the lead.Data type: String

</td></tr><tr><td>

number

</td><td id="lead-number-entry">

Unique system-generated number of the lead record.Data type: String

</td></tr><tr><td>

other\_reason

</td><td id="lead-other_reason-entry">

Additional reason for the lead disqualification.Data type: String

Max length: 160 characters

</td></tr><tr><td>

owner

</td><td id="lead-owner-entry">

Details of the person associated with the lead.

Data type: Object

 ```
"owner": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

owner.name

</td><td id="lead-owner.name-entry">

Name of the person that owns the lead.Data type: String

</td></tr><tr><td>

owner.sys\_id

</td><td id="lead-owner.sys_id-entry">

Sys\_id of the user record of the person that owns the lead.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

reason

</td><td id="lead-reason-entry">

Reason for the lead disqualification such as, Disqualify.Data type: String

Max length: 40 characters

</td></tr><tr><td>

short\_description

</td><td id="lead-short_description-entry">

Short description of the lead.Data type: String

Max length: 160 characters

</td></tr><tr><td>

similar\_lead

</td><td id="lead-similar_lead-entry">

Details on any similar lead. Use this for possible lead disqualification.

Data type: Object

 ```
"similar_lead": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

similar\_lead.name

</td><td id="lead-similar_lead.name-entry">

Name of the duplicate lead.Data type: String

</td></tr><tr><td>

similar\_lead.sys\_id

</td><td id="lead-similar_lead.sys_id-entry">

Sys\_id of the lead record that is a possible duplicate lead.Data type: String

Table: Lead \[sn\_lead\_mgmt\_core\_lead\]

</td></tr><tr><td>

stage

</td><td id="lead-stage-entry">

Stage of the lead such as, 100\_new.

**Note:** This is a choice field. It must contain one of the choice items defined in the stage field of the Leads table.

Data type: String

</td></tr><tr><td>

state

</td><td id="lead-state-entry">

State in which the lead resides.Data type: String

</td></tr><tr><td>

street

</td><td id="lead-street-entry">

Street on which the lead resides.Data type: String

</td></tr><tr><td>

sys\_class\_name

</td><td id="lead-sys_class_name-entry">

System-generated class name of the Lead table.Data type: String

</td></tr><tr><td>

sys\_created\_by

</td><td id="lead-sys_created_by-entry">

User name of the person that created the lead.Data type: String

</td></tr><tr><td>

sys\_created\_on

</td><td id="lead-sys_created_on-entry">

System-generated date and time that the lead was created.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "value": "String"
} 
```

</td></tr><tr><td>

sys\_created\_on.​display\_value

</td><td id="lead-sys_created_on.display_value-entry">

Date and time when the lead was created.Data type: String

Format: Default instance format and time zone

</td></tr><tr><td>

sys\_created\_on.​value

</td><td id="lead-sys_created_on.value-entry">

Date and time when the lead was created.Data type: String

Format: UTC

</td></tr><tr><td>

sys\_domain

</td><td id="lead-sys_domain-entry">

Sys\_id of the domain record to which the lead belongs. **Note:** This parameter is only returned in the response if domain separation is enabled.

Data type: String

</td></tr><tr><td>

sys\_domain\_path

</td><td id="lead-sys_domain_path-entry">

Path of the domain to which the lead belongs. **Note:** This parameter is only returned in the response if domain separation is enabled.

Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="lead-sys_id-entry">

Sys\_id of the lead record.Data type: String

Table: Lead \[sn\_lead\_mgmt\_core\_lead\]

</td></tr><tr><td>

sys\_mod\_count

</td><td id="lead-sys_mod_count-entry">

Number of times the associated lead record has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

sys\_tags

</td><td id="lead-sys_tags-entry">

List of system tags associated with the lead. You can use these tags to categorize leads.Data type: Array

</td></tr><tr><td>

sys\_updated\_by

</td><td id="lead-sys_updated_by-entry">

User name of the person that last updated the lead record.Data type: String

</td></tr><tr><td>

sys\_updated\_on

</td><td id="lead-sys_updated_on-entry">

System-generated date and time when the lead was last updated.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "value": "String"
} 
```

</td></tr><tr><td>

sys\_updated\_on.​display\_value

</td><td id="lead-sys_updated_on.display_value-entry">

Date and time that the lead was last updated.Data type: String

Format: Instance's default format and time zone

</td></tr><tr><td>

sys\_updated\_on.​value

</td><td id="lead-sys_updated_on.value-entry">

Date and time that the lead was last updated.Data type: String

Format: UTC

</td></tr><tr><td>

title

</td><td id="lead-title-entry">

Lead's title.Data type: String

</td></tr><tr><td>

website

</td><td id="lead-website-entry">

Lead's website URL.Data type: String

</td></tr><tr><td>

work\_notes

</td><td id="lead-work_notes-entry">

List of work notes created for the lead.

Data type: Array of Objects

 ```
"work_notes": [
  {
    "author": "String",
    "date": "String",
    "text": "String"
  }
]
```

</td></tr><tr><td>

work\_notes.​author

</td><td id="lead-work_notes.author-entry">

User name of the person that authored the associated work note.Data type: String

</td></tr><tr><td>

work\_notes.​date

</td><td id="lead-work_notes.date-entry">

Date that the note was created.Data type: String

</td></tr><tr><td>

work\_notes.​text

</td><td id="lead-work_notes.text-entry">

Text of the note made by the author.Data type: String

</td></tr><tr><td>

zip

</td><td id="lead-zip-entry">

Zip code of the associated lead.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to retrieve the lead record with the sys\_id of 856b6a95ffde8210b85dffffffffffd7.

```
curl "https://instance.service-now.com /api/sn_lead_mgmt_core/lead/856b6a95ffde8210b85dffffffffffd7" \ 
--request GET \ 
--header "Accept:application/json" \ 
--user "username":"password" 
```

The following are the return results:

```
{ 
  "short_description": "Looking for a quote on preventative maintenance plans for their corporate office building elevators.",
  "reason": null,
  "country": "USA",
  "closed_date": null,
  "city": "San Francisco",
  "lead_source": "inbound_phone",
  "external_id": null,
  "industry": "manufacturing",
  "sys_updated_on": {
    "value": "2024-05-31 11:01:55",
    "display_value": "2024-05-31 04:01:55"
  },
  "title": "Director of Building operations",
  "sys_class_name": "Lead",
  "number": "LEAD0000001",
  "sys_id": "856b6a95ffde8210b85dffffffffffd7",
  "business_phone": "+1 (555) 123-4567",
  "similar_lead": null,
  "sys_updated_by": "abel.tuter",
  "mobile_phone": null,
  "street": "789, Industrial drive",
  "sys_created_on": {
    "value": "2024-05-20 10:32:41",
    "display_value": "2024-05-20 03:32:41"
  },
  "contact": null,
  "company": "Lee Manufacturing Inc",
  "state": "CA",
  "first_name": "James",
  "email": "james.wilson@email.com",
  "consumer": null,
  "sys_created_by": "abel.tuter",
  "zip": "94016",
  "owner": {
    "sys_id": "60058fe943fe3110d6c6cd60afb8f203",
    "name": "Max Blaze"
  },
  "website": null,
  "lead_group": null,
  "sys_mod_count": 1,
  "last_name": "Wilson",
  "other_reason": null,
  "middle_name": null,
  "sys_tags": null,
  "do_not_share": false,
  "lead_score": 92,
  "stage": "300_nurturing",
  "do_not_email": false,
  "lead_type": null,
  "work_notes": [
    {
      "author": "Abel Tuter",
      "date": "2024-12-04 06:52:07",
      "text": "Work notes for lead" 
    }
  ],
  "do_not_call": false,
  "lead_rating": "400_super_hot",
  "account": null,
  "external_system": null, 
  "lead_line_items": [
    {
      "quantity": 6,
      "product_offering": {
        "sys_id": "32619d9fd0a63110f8770dbf976be1f9",
        "name": "Safety Test Coverage",
        "code": "SAFETSTCVG1"
      },
      "sys_mod_count": 0,
      "external_id": null,
      "sys_updated_on": {
        "value": "2024-05-20 10:38:41",
        "display_value": "2024-05-20 03:38:41" 
      },
      "sys_tags": null,
      "lead": {
        "sys_id": "856b6a95ffde8210b85dffffffffffd7",
        "name": "LEAD0000001"
      },
      "number": "LEADL0000003", 
      "sys_id": "013daa19ffde8210b85dffffffffff82",
      "unit_of_measurement": { 
        "sys_id": "cb2795d553020110286eddeeff7b12ff",
        "name": "Each"
      },
      "sys_updated_by": "abel.tuter",
      "sys_created_on": {
        "value": "2024-05-20 10:38:41",
        "display_value": "2024-05-20 03:38:41"
      },
      "work_notes": null,
      "sys_created_by": "abel.tuter",
      "external_system": null
    }
  ]
} 
```

## lead - PATCH /sn\_lead\_mgmt\_core/lead/\{sys\_id\}

Updates the specified lead record and its associated lead line items. You can also use this endpoint to associate new lead line items to the specified lead.

This endpoint updates information in the following tables:

-   Lead \[sn\_lead\_mgmt\_core\_lead\]
-   Lead Line Item \[sn\_lead\_mgmt\_core\_lead\_line\_item\]

Rules for passed-in parameters:

-   Invalid parameter names are ignored.
-   Invalid values for non-mandatory choice and reference fields are ignored.
-   If field WRITE access is denied for one or more fields, the restricted fields are ignored.
-   You can't insert system field values using this API. Any provided values are ignored. System fields are a part of the ignored fields list, which is configurable.
-   The values of the parameters **account**, **contact**, and **consumer** are ignored if both the **account** and **consumer** parameters are non-empty.
-   Unless otherwise specified, the default value for all non-passed parameters is 'null'.

**Note:** This endpoint only modifies the specified parameters. If a parameter that exists in the current lead or lead line item record is not specified in the call, its contents remain unchanged.

### URL format

Versioned URL: `/api/sn_lead_mgmt_core/{api_version}/lead/{sys_id}`

Default URL: `/api/sn_lead_mgmt_core/{api_version}/lead/{sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the lead record to update.Data type: String

Table: Lead \[sn\_lead\_mgmt\_core\_lead\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="lead-account-row"><td>

account

</td><td id="lead-account-entry">

Details of the account associated with the lead.Data type: Object

```
"account": {
  "sys_id": "String"
}
```

</td></tr><tr><td>

account.sys\_id

</td><td id="lead-account.sys_id-entry">

Sys\_id of the associated account record.

Data type: String

 Table: Account \[customer\_account\]

</td></tr><tr><td>

business\_phone

</td><td id="lead-business_phone-entry">

Lead's business phone number.Data type: String

</td></tr><tr><td>

city

</td><td id="lead-city-entry">

City in which the lead resides.Data type: String

</td></tr><tr><td>

company

</td><td id="lead-company-entry">

Lead's company name.Data type: String

</td></tr><tr><td>

consumer

</td><td>

Consumer associated with the lead.Data type: Object

```
"consumer": { 
  "sys_id": "String" 
} 
```

</td></tr><tr><td>

consumer.sys\_id

</td><td id="lead-consumer.sys_id-entry">

Sys\_id of the associated consumer record.

Data type: String

 Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

contact

</td><td>

Contact associated with the lead account.Data type: Object

```
"contact": { 
  "sys_id": "String" 
} 
```

</td></tr><tr><td>

contact.sys\_id

</td><td id="lead-contact.sys_id-entry">

Sys\_id of the associated contact record.

Data type: String

 Table: Contact \[customer\_contact\]

</td></tr><tr><td>

country

</td><td id="lead-country-entry">

Country in which the lead resides.Data type: String

</td></tr><tr><td>

do\_not\_call

</td><td id="lead-do_not_call-entry">

Flag that indicates whether the mode of communication is by phone.

Valid values:

-   true: Can call contact.
-   false: Don't call contact.

Data type: Boolean

</td></tr><tr><td>

do\_not\_email

</td><td id="lead-do_not_email-entry">

Flag that indicates whether the mode of communication is by email.

Valid values:

-   true: Can email contact.
-   false: Don't email contact.

Data type: Boolean

</td></tr><tr><td>

do\_not\_share

</td><td id="lead-do_not_share-entry">

Flag that indicates whether the lead details can be shared.

Valid values:

-   true: Lead details can be shared.
-   false: Lead details can't be shared.

Data type: Boolean

</td></tr><tr><td>

email

</td><td id="lead-email-entry">

Lead's email address.Data type: String

</td></tr><tr><td>

external\_id

</td><td id="lead-external_id-entry">

ID used by the system that generated the lead to identify the lead in the associated system.Data type: String

</td></tr><tr><td>

external\_system

</td><td id="lead-external_system-entry">

Name of the external system associated with the lead, such as HubSpot or pipedrive.Data type: String

</td></tr><tr><td>

first\_name

</td><td id="lead-first_name-entry">

First name of the contact associated with the lead.Data type: String

</td></tr><tr><td>

industry

</td><td id="lead-industry-entry">

Industry to which the lead belongs.Data type: String

Table: Located in the **industry** field of the Account \[customer\_account\] table.

</td></tr><tr><td>

last\_name

</td><td>

Required. Last name of the contact associated with the lead.

Data type: String

</td></tr><tr><td>

lead\_group

</td><td>

Group to which the lead belongs.

Data type: Object

 ```
"lead_group": {
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_group.sys\_id

</td><td id="lead-lead_group.sys_id-entry">

Sys\_id of the lead group record.Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

lead\_line\_items

</td><td>

List of lead line items to associated with the lead.Group to which the lead belongs.

Data type: Object

```
"lead_line_items": [ 
  { 
    "external_id": "String",
    "external_system": "String",
    "product_offering": {Object},
    "quantity": Number, 
    "work_notes": [Array],
    "unit_of_measurement": {Object} 
  } 
] 
```

Maximum line items: 100 - any over that are ignored

</td></tr><tr><td>

lead\_line\_items.​external\_id

</td><td id="lead-lead_line_items.external_id-entry">

ID used by the system that generated the lead line item to identify the line item in the associated system.Data type: String

</td></tr><tr><td>

lead\_line\_items.​external\_system

</td><td id="lead-lead_line_items.external_system-entry">

Name of the external system associated with the lead line item, such as HubSpot or pipedrive.Data type: String

</td></tr><tr><td>

lead\_line\_items.product\_offering

</td><td>

Required. Information about the product offering associated with the lead line item.Data type: Object

```
"product_offering": {
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.product\_offering.sys\_id

</td><td>

Required. Sys\_id of the product offering record associated with the lead line item.

Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

lead\_line\_items.quantity

</td><td>

Quantity of items the lead wants to purchase of the associated product offering.

Data type: Number \(Integer\)

</td></tr><tr><td>

lead\_line\_items.​unit\_of\_measurement

</td><td>

Details of the measuring unit of lead line item.

Data type: Object

 ```
"unit_of_measurement": {
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​unit\_of\_measurement​.sys\_id

</td><td>

Sys\_id of the record that describes the measuring unit.Data type: String

Table: Unit of Measure \[sn\_prd\_pm\_uom\]

</td></tr><tr><td>

lead\_line\_items.work\_notes

</td><td>

List that describes the work notes created for the lead line item.

Data type: Array of Objects

 ```
"work_notes": [
    "text": "String"
  }
]
```

</td></tr><tr><td>

lead\_line\_items.​work\_notes.​text

</td><td id="lead-lead_line_items.work_notes.text-entry">

Text of the note made by the author.Data type: String

</td></tr><tr><td>

lead\_rating

</td><td id="lead-lead_rating-entry">

Rating for the lead such as, 100\_cold, 200\_warm, 300\_hot, or 400\_super\_hot.**Note:** This is a choice field. It must contain one of the choice items defined in the lead\_rating field of the Leads table.

Data type: String

</td></tr><tr><td>

lead\_score

</td><td id="lead-lead_score-entry">

Score for the lead.Data type: Decimal

Range: 1 to 100

</td></tr><tr><td>

lead\_source

</td><td id="lead-lead_source-entry">

Originator of the lead.**Note:** This is a choice field. It must contain one of the choice items defined in the lead\_source field of the Leads table.

Data type: String

</td></tr><tr><td>

lead\_type

</td><td id="lead-lead_type-entry">

Type of lead, such as New Business or Existing Business.

 **Note:** This is a choice field. It must contain one of the choice items defined in the lead\_type field of the Leads table.

 Data type: String

</td></tr><tr><td>

middle\_name

</td><td id="lead-middle_name-entry">

Middle name of the contact for the lead.Data type: String

</td></tr><tr><td>

mobile\_phone

</td><td id="lead-mobile_phone-entry">

Phone number of the contact for the lead.Data type: String

</td></tr><tr><td>

other\_reason

</td><td id="lead-other_reason-entry">

Additional reason for the lead disqualification.Data type: String

Max length: 160 characters

</td></tr><tr><td>

owner

</td><td>

Details of the person associated with the lead.

Data type: Object

 ```
"owner": {
  "sys_id": "String"
}
```

</td></tr><tr><td>

owner.sys\_id

</td><td id="lead-owner.sys_id-entry">

Sys\_id of the user record of the person that owns the lead.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

reason

</td><td id="lead-reason-entry">

Reason for the lead disqualification such as, Disqualify.Data type: String

Max length: 40 characters

</td></tr><tr><td>

short\_description

</td><td id="lead-short_description-entry">

Short description of the lead.Data type: String

Max length: 160 characters

</td></tr><tr><td>

similar\_lead

</td><td>

Details on any similar lead. Use this for possible lead disqualification.

Data type: Object

 ```
"similar_lead": {
  "sys_id": "String"
}
```

</td></tr><tr><td>

similar\_lead.sys\_id

</td><td id="lead-similar_lead.sys_id-entry">

Sys\_id of the lead record that is a possible duplicate lead.Data type: String

Table: Lead \[sn\_lead\_mgmt\_core\_lead\]

</td></tr><tr><td>

stage

</td><td id="lead-stage-entry">

Stage of the lead such as, 100\_new.

**Note:** This is a choice field. It must contain one of the choice items defined in the stage field of the Leads table.

Data type: String

</td></tr><tr><td>

state

</td><td id="lead-state-entry">

State in which the lead resides.Data type: String

</td></tr><tr><td>

street

</td><td id="lead-street-entry">

Street on which the lead resides.Data type: String

</td></tr><tr><td>

title

</td><td id="lead-title-entry">

Lead's title.Data type: String

</td></tr><tr><td>

website

</td><td id="lead-website-entry">

Lead's website URL.Data type: String

</td></tr><tr><td>

work\_notes

</td><td>

List of work notes created for the lead.

Data type: Array of Objects

 ```
"work_notes": [
  {
    "text": "String"
  }
]
```

 **Note:** An array of work notes in the request is inserted as a single text. This text is generated by combining the content from all work note objects in the request, with each entry separated by a comma \(,\).

</td></tr><tr><td>

work\_notes.​text

</td><td id="lead-work_notes.text-entry">

Text of the note made by the author.Data type: String

</td></tr><tr><td>

zip

</td><td id="lead-zip-entry">

Zip code of the associated lead.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Successful. Lead and lead line items records were successfully updated.

</td></tr><tr><td>

400

</td><td id="lead-400-status_code-entry">

Error. Possible reasons: -   Invalid payload: Invalid/empty request body.
-   Invalid payload: Invalid field value for email/phone number fields.
-   Invalid payload: Mandatory field is absent, or its value is empty.
-   Invalid payload: Stage is ‘400\_closed\_won’. Qualifying lead is not supported using the API.
-   If the stage of the lead to be updated is already in the closed state and you are trying to update it.

</td></tr><tr><td>

403

</td><td id="entry-403-status-code">

Forbidden. The user doesn't have access rights to the specified record.

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td id="d3360e67">

Account linked to the lead.Data type: Object

```
"account": { 
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

account.name

</td><td id="lead-account.name-entry">

Name of the account.Data type: String

</td></tr><tr><td>

account.sys\_id

</td><td id="d3360e91">

Sys\_id of the associated account record.

Data type: String

 Table: Account \[customer\_account\]

</td></tr><tr><td>

business\_phone

</td><td id="d3360e108">

Lead's business phone number.Data type: String

</td></tr><tr><td>

city

</td><td id="d3360e119">

City in which the lead resides.Data type: String

</td></tr><tr><td>

closed\_date

</td><td id="lead-closed_date-entry">

Date and time when the lead was closed.Data type: Object

```
"closed_date": {
  "display_value": "String", 
  "value": "String"
} 
```

</td></tr><tr><td>

closed\_date.​display\_value

</td><td id="lead-closed_date.display_value-entry">

Date and time as displayed in the UI. Data type: String

Format: User's format and time zone.

</td></tr><tr><td>

closed\_date.value

</td><td id="lead-closed_date.value-entry">

Date and time that the lead closed as defined in the associated record.Data type: String

Format: UTC

</td></tr><tr><td>

company

</td><td id="d3360e171">

Lead's company name.Data type: String

</td></tr><tr><td>

consumer

</td><td id="lead-consumer-entry">

Consumer associated with the lead.Data type: Object

```
"consumer": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

consumer.name

</td><td id="lead-consumer.name-entry">

Name of the associated consumer.Data type: String

</td></tr><tr><td>

consumer.sys\_id

</td><td id="d3360e208">

Sys\_id of the associated consumer record.

Data type: String

 Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

contact

</td><td id="lead-contact-entry">

Contact associated with the lead account.Data type: Object

```
"contact": {
  "name": "String",
  "sys_id": "String" 
} 
```

</td></tr><tr><td>

contact.name

</td><td id="lead-contact.name-entry">

Contact's name.Data type: String

</td></tr><tr><td>

contact.sys\_id

</td><td id="d3360e250">

Sys\_id of the associated contact record.

Data type: String

 Table: Contact \[customer\_contact\]

</td></tr><tr><td>

country

</td><td id="d3360e267">

Country in which the lead resides.Data type: String

</td></tr><tr><td>

do\_not\_call

</td><td id="d3360e278">

Flag that indicates whether the mode of communication is by phone.

Valid values:

-   true: Can call contact.
-   false: Don't call contact.

Data type: Boolean

</td></tr><tr><td>

do\_not\_email

</td><td id="d3360e303">

Flag that indicates whether the mode of communication is by email.

Valid values:

-   true: Can email contact.
-   false: Don't email contact.

Data type: Boolean

</td></tr><tr><td>

do\_not\_share

</td><td id="d3360e327">

Flag that indicates whether the lead details can be shared.

Valid values:

-   true: Lead details can be shared.
-   false: Lead details can't be shared.

Data type: Boolean

</td></tr><tr><td>

email

</td><td id="d3360e351">

Lead's email address.Data type: String

</td></tr><tr><td>

external\_id

</td><td id="d3360e362">

ID used by the system that generated the lead to identify the lead in the associated system.Data type: String

</td></tr><tr><td>

external\_system

</td><td id="d3360e373">

Name of the external system associated with the lead, such as HubSpot or pipedrive.Data type: String

</td></tr><tr><td>

first\_name

</td><td id="d3360e384">

First name of the contact associated with the lead.Data type: String

</td></tr><tr><td>

industry

</td><td id="d3360e396">

Industry to which the lead belongs.Data type: String

Table: Located in the **industry** field of the Account \[customer\_account\] table.

</td></tr><tr><td>

last\_name

</td><td id="lead-last_name-entry">

Last name of the contact associated with the lead.

Data type: String

</td></tr><tr><td>

lead\_group

</td><td id="lead-lead_group-entry">

Group to which the lead belongs.

Data type: Object

 ```
"lead_group": {
  "name: "String",
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_group.name

</td><td id="lead-lead_group.name-entry">

Lead group's name.Data type: String

</td></tr><tr><td>

lead\_group.sys\_id

</td><td id="d3360e454">

Sys\_id of the lead group record.Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

lead\_line\_items

</td><td id="lead-lead_line_items-entry">

Details of the lead line items associated with the lead.Data type: Array of Objects

```
"lead_line_items": [ 
  { 
    "external_id": "String", 
    "external_system": "String",
    "lead": {Object},
    "number": "String",
    "product_offering": {Object},
    "quantity": Number,
    "sys_created_by”: "String",
    "sys_created_on {Object},
    "sys_domain": "String",
    "sys_domain_path": "String",
    "sys_id": "String",
    "sys_mod_count": Number,
    "sys_tags": [Array],
    "sys_updated_by: "String",
    "sys_updated_on: {Object},
    "unit_of_measurement": {Object}, 
    "work_notes": [Array]
  } 
] 
```

</td></tr><tr><td>

lead\_line\_items.​external\_id

</td><td id="d3360e481">

ID used by the system that generated the lead line item to identify the line item in the associated system.Data type: String

</td></tr><tr><td>

lead\_line\_items.​external\_system

</td><td id="d3360e492">

Name of the external system associated with the lead line item, such as HubSpot or pipedrive.Data type: String

</td></tr><tr><td>

lead\_line\_items.​lead

</td><td id="lead-lead_line_items.lead-entry">

Details about the lead associated with the line item.Data type: Object

```
"lead: {
  "name": "String",
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​lead.name

</td><td id="lead-lead_line_items.lead.name-entry">

Associated lead's name.Data type: String

</td></tr><tr><td>

lead\_line\_items.​lead.sys\_id

</td><td id="lead-lead_line_items.lead.sys_id-entry">

Sys\_id of the associated lead record.Data type: String

</td></tr><tr><td>

lead\_line\_items.​number

</td><td id="lead-lead_line_items.number-entry">

Unique system-generated number of the lead line item record.Data type: String

</td></tr><tr><td>

lead\_line\_items.​product\_offering

</td><td id="lead-lead_line_items.product_offering-entry">

Information about the product offering associated with the lead line item.Data type: Object

```
"product_offering": {
  "code": " String",
  "name": "String",
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​product\_offering.code

</td><td id="lead-lead_line_items.product_offering.code-entry">

Code linked to the product offering. **Note:** This is a system-generated alphanumeric number based on the product name. Although system generated, you can edit the code to represent a SKU or any other industry specific product codes.

Data type: String

</td></tr><tr><td>

lead\_line\_items.​product\_offering.name

</td><td id="lead-lead_line_items.product_offering.name-entry">

Product offering's name.Data type: String

</td></tr><tr><td>

lead\_line\_items.​product\_offering.sys\_id

</td><td id="lead-lead_line_items.product_offering.sys_id-entry">

Sys\_id of the product offering record associated with the lead line item.

Data type: String

 Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

lead\_line\_items.​quantity

</td><td id="lead-lead_line_items.quantity-entry">

Quantity of items the lead wants to purchase of the associated product offering.

Data type: Number \(Integer\)

</td></tr><tr><td>

lead\_line\_items.​sys\_created\_by

</td><td id="lead-lead_line_items.sys_created_by-entry">

User name of the person that created the lead line item.Data type: String

</td></tr><tr><td>

lead\_line\_items.​sys\_created\_on

</td><td id="lead-lead_line_items.sys_created_on-entry">

System-generated date and time that the lead line item was created.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "value": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​sys\_created\_on.display\_value

</td><td id="lead-lead_line_items.sys_created_on.display_value-entry">

Date and time that the lead line item was created.Data type: String

Format: Default instance format and time zone

</td></tr><tr><td>

lead\_line\_items.​sys\_created\_on.value

</td><td id="lead-lead_line_items.sys_created_on.value-entry">

Date and time that the lead line item was created.Data type: String

Format: UTC

</td></tr><tr><td>

lead\_line\_items.​sys\_domain

</td><td id="lead-lead_line_items.sys_domain-entry">

Sys\_id of the domain record to which the lead line item belongs. **Note:** This parameter is only returned in the response if domain separation is enabled.

Data type: String

</td></tr><tr><td>

lead\_line\_items.sys\_domain\_path

</td><td id="lead-lead_line_items.sys_domain_path-entry">

Path of the domain to which the lead line item belongs. **Note:** This parameter is only returned in the response if domain separation is enabled.

Data type: String

</td></tr><tr><td>

lead\_line\_items.​sys\_id

</td><td id="lead-lead_line_items.sys_id-entry">

Sys\_id of the lead line item record.Data type: String

</td></tr><tr><td>

lead\_line\_items.​sys\_mod\_count

</td><td id="lead-lead_line_items.sys_mod_count-entry">

Number of times the associated lead line item record has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

lead\_line\_items.​sys\_tags

</td><td id="lead-lead_line_items.sys_tags-entry">

List of system tags associated with the lead line item.Data type: Array

</td></tr><tr><td>

lead\_line\_items.​sys\_updated\_by

</td><td id="lead-lead_line_items.sys_updated_by-entry">

User name of the person that last updated the associated lead line item.Data type: String

</td></tr><tr><td>

lead\_line\_items.​sys\_updated\_on

</td><td id="lead-lead_line_items.sys_updated_on-entry">

System-generated date and time when the lead line item was last updated.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "value": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​sys\_updated\_on.​display\_value

</td><td id="lead-lead_line_items.sys_updated_on.display_value-entry">

Date and time that the lead line item was last updated.Data type: String

Format: Default instance format and time zone

</td></tr><tr><td>

lead\_line\_items.​sys\_updated\_on.​value

</td><td id="lead-lead_line_items.sys_updated_on.value-entry">

Date and time that the lead line item was last updated.Data type: String

Format: UTC

</td></tr><tr><td>

lead\_line\_items.​unit\_of\_measurement

</td><td id="lead-lead_line_items.unit_of_measurement-entry">

Details of the measuring unit of lead line item.

Data type: Object

 ```
"unit_of_measurement": {
  "name": "String",
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​unit\_of\_measurement.​name

</td><td id="lead-lead_line_items.unit_of_measurement.name-entry">

Name of the measuring unit such as, each or cubic foot.Data type: String

</td></tr><tr><td>

lead\_line\_items.​unit\_of\_measurement.​sys\_id

</td><td id="lead-lead_line_items.unit_of_measurement.sys_id-entry">

Sys\_id of the record that describes the measuring unit.Data type: String

Table: Unit of Measure \[sn\_prd\_pm\_uom\]

</td></tr><tr><td>

lead\_line\_items.​work\_notes

</td><td id="lead-lead_line_items.work_notes-entry">

List that describes the work notes created for the lead line item.

Data type: Array of Objects

 ```
"work_notes": [
  {
    "author": "String",
    "date": "String",
    "text": "String"
  }
]
```

</td></tr><tr><td>

lead\_line\_items.​work\_notes.​author

</td><td id="lead-lead_line_items.work_notes.author-entry">

User name of the person that authored the associated work note.Data type: String

</td></tr><tr><td>

lead\_line\_items.​work\_notes.​date

</td><td id="lead-lead_line_items.work_notes.date-entry">

Date that the note was created.Data type: String

</td></tr><tr><td>

lead\_line\_items.​work\_notes.​text

</td><td id="d3360e862">

Text of the note made by the author.Data type: String

</td></tr><tr><td>

lead\_rating

</td><td id="d3360e873">

Rating for the lead such as, 100\_cold, 200\_warm, 300\_hot, or 400\_super\_hot.**Note:** This is a choice field. It must contain one of the choice items defined in the lead\_rating field of the Leads table.

Data type: String

</td></tr><tr><td>

lead\_score

</td><td id="d3360e886">

Score for the lead.Data type: Decimal

Range: 1 to 100

</td></tr><tr><td>

lead\_source

</td><td id="d3360e899">

Originator of the lead.**Note:** This is a choice field. It must contain one of the choice items defined in the lead\_source field of the Leads table.

Data type: String

</td></tr><tr><td>

lead\_type

</td><td id="d3360e912">

Type of lead, such as New Business or Existing Business.

 **Note:** This is a choice field. It must contain one of the choice items defined in the lead\_type field of the Leads table.

 Data type: String

</td></tr><tr><td>

middle\_name

</td><td id="d3360e930">

Middle name of the contact for the lead.Data type: String

</td></tr><tr><td>

mobile\_phone

</td><td id="d3360e942">

Phone number of the contact for the lead.Data type: String

</td></tr><tr><td>

number

</td><td id="lead-number-entry">

Unique system-generated number of the lead record.Data type: String

</td></tr><tr><td>

other\_reason

</td><td id="d3360e964">

Additional reason for the lead disqualification.Data type: String

Max length: 160 characters

</td></tr><tr><td>

owner

</td><td id="lead-owner-entry">

Details of the person associated with the lead.

Data type: Object

 ```
"owner": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

owner.name

</td><td id="lead-owner.name-entry">

Name of the person that owns the lead.Data type: String

</td></tr><tr><td>

owner.sys\_id

</td><td id="d3360e1005">

Sys\_id of the user record of the person that owns the lead.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

reason

</td><td id="d3360e1019">

Reason for the lead disqualification such as, Disqualify.Data type: String

Max length: 40 characters

</td></tr><tr><td>

short\_description

</td><td id="d3360e1032">

Short description of the lead.Data type: String

Max length: 160 characters

</td></tr><tr><td>

similar\_lead

</td><td id="lead-similar_lead-entry">

Details on any similar lead. Use this for possible lead disqualification.

Data type: Object

 ```
"similar_lead": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

similar\_lead.name

</td><td id="lead-similar_lead.name-entry">

Name of the duplicate lead.Data type: String

</td></tr><tr><td>

similar\_lead.sys\_id

</td><td id="d3360e1073">

Sys\_id of the lead record that is a possible duplicate lead.Data type: String

Table: Lead \[sn\_lead\_mgmt\_core\_lead\]

</td></tr><tr><td>

stage

</td><td id="d3360e1086">

Stage of the lead such as, 100\_new.

**Note:** This is a choice field. It must contain one of the choice items defined in the stage field of the Leads table.

Data type: String

</td></tr><tr><td>

state

</td><td id="d3360e1103">

State in which the lead resides.Data type: String

</td></tr><tr><td>

street

</td><td id="d3360e1114">

Street on which the lead resides.Data type: String

</td></tr><tr><td>

sys\_class\_name

</td><td id="lead-sys_class_name-entry">

System-generated class name of the Lead table.Data type: String

</td></tr><tr><td>

sys\_created\_by

</td><td id="lead-sys_created_by-entry">

User name of the person that created the lead.Data type: String

</td></tr><tr><td>

sys\_created\_on

</td><td id="lead-sys_created_on-entry">

System-generated date and time that the lead was created.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "value": "String"
} 
```

</td></tr><tr><td>

sys\_created\_on.​display\_value

</td><td id="lead-sys_created_on.display_value-entry">

Date and time when the lead was created.Data type: String

Format: Default instance format and time zone

</td></tr><tr><td>

sys\_created\_on.​value

</td><td id="lead-sys_created_on.value-entry">

Date and time when the lead was created.Data type: String

Format: UTC

</td></tr><tr><td>

sys\_domain

</td><td id="lead-sys_domain-entry">

Sys\_id of the domain record to which the lead belongs. **Note:** This parameter is only returned in the response if domain separation is enabled.

Data type: String

</td></tr><tr><td>

sys\_domain\_path

</td><td id="lead-sys_domain_path-entry">

Path of the domain to which the lead belongs. **Note:** This parameter is only returned in the response if domain separation is enabled.

Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="lead-sys_id-entry">

Sys\_id of the lead record.Data type: String

Table: Lead \[sn\_lead\_mgmt\_core\_lead\]

</td></tr><tr><td>

sys\_mod\_count

</td><td id="lead-sys_mod_count-entry">

Number of times the associated lead record has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

sys\_tags

</td><td id="lead-sys_tags-entry">

List of system tags associated with the lead. You can use these tags to categorize leads.Data type: Array

</td></tr><tr><td>

sys\_updated\_by

</td><td id="lead-sys_updated_by-entry">

User name of the person that last updated the lead record.Data type: String

</td></tr><tr><td>

sys\_updated\_on

</td><td id="lead-sys_updated_on-entry">

System-generated date and time when the lead was last updated.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "value": "String"
} 
```

</td></tr><tr><td>

sys\_updated\_on.​display\_value

</td><td id="lead-sys_updated_on.display_value-entry">

Date and time that the lead was last updated.Data type: String

Format: Instance's default format and time zone

</td></tr><tr><td>

sys\_updated\_on.​value

</td><td id="lead-sys_updated_on.value-entry">

Date and time that the lead was last updated.Data type: String

Format: UTC

</td></tr><tr><td>

title

</td><td id="d3360e1299">

Lead's title.Data type: String

</td></tr><tr><td>

website

</td><td id="d3360e1310">

Lead's website URL.Data type: String

</td></tr><tr><td>

work\_notes

</td><td id="lead-work_notes-entry">

List of work notes created for the lead.

Data type: Array of Objects

 ```
"work_notes": [
  {
    "author": "String",
    "date": "String",
    "text": "String"
  }
]
```

</td></tr><tr><td>

work\_notes.​author

</td><td id="lead-work_notes.author-entry">

User name of the person that authored the associated work note.Data type: String

</td></tr><tr><td>

work\_notes.​date

</td><td id="lead-work_notes.date-entry">

Date that the note was created.Data type: String

</td></tr><tr><td>

work\_notes.​text

</td><td id="d3360e1361">

Text of the note made by the author.Data type: String

</td></tr><tr><td>

zip

</td><td id="d3360e1372">

Zip code of the associated lead.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to update the lead record with the sys\_id 856b6a95ffde8210b85dffffffffffd7.

```
curl " https://instance.service-now.com/api/sn_lead_mgmt_core/v1/lead/856b6a95ffde8210b85dffffffffffd7" \ 
--request PATCH \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data " {
  "lead_source": "inbount_web",
  "business_phone": "+1 (555) 123-4567",
  "do_not_share": true,
  "lead_score": 40,
  "stage": "300_nurturning",
  "do_not_email": false,
  "lead_type": "new_business",
  "work_notes": [
    {
      "text": "Work notes for lead"
    }
  ],
  "lead_rating": "200_warm",
  "lead_line_items": [
    {
      "sys_id" : "013daa19ffde8210b85dffffffffff82",
      "quantity": 10
    },
    {
      "product_offering": {
        "sys_id": "0b61dd9fd0a63110f8770dbf976be171"
      }
    }
  ]
}"
```

The response contains all lead record fields.

```
{ 
  "short_description": "Looking for a quote on preventative maintenance plans for their corporate office building elevators.",
  "reason": null,
  "country": "USA",
  "closed_date": null,
  "city": "San Francisco",
  "lead_source": "inbount_web",
  "external_id": null,
  "industry": "manufacturing",
  "sys_updated_on": {
    "value": "2024-12-11 08:45:52",
    "display_value": "2024-12-11 00:45:52"
  },
  "title": "Director of Building operations",
  "sys_class_name": "Lead",
  "number": "LEAD0000001",
  "sys_id": "856b6a95ffde8210b85dffffffffffd7",
  "business_phone": "+1 (555) 123-4567",
  "similar_lead": null,
  "sys_updated_by": "abel.tuter",
  "mobile_phone": null,
  "street": "789, Industrial drive",
  "sys_created_on": {
    "value": "2024-05-20 10:32:41",
    "display_value": "2024-05-20 03:32:41"
  },
  "contact": null,
  "company": "Lee Manufacturing Inc",
  "state": "CA",
  "first_name": "James",
  "email": "james.wilson@email.com",
  "consumer": null,
  "sys_created_by": "abel.tuter",
  "zip": "94016",
  "owner": {
    "sys_id": "60058fe943fe3110d6c6cd60afb8f203",
    "name": "Max Blaze"
  },
  "website": null,
  "lead_group": null,
  "sys_mod_count": 4,
  "last_name": "Wilson",
  "other_reason": null,
  "middle_name": null,
  "sys_tags": null,
  "do_not_share": true,
  "lead_score": 40,
  "stage": "300_nurturing",
  "do_not_email": false,
  "lead_type": "new_business",
  "work_notes": [
    {
      "author": "Abel Tuter",
      "date": "2024-12-11 00:45:52",
      "text": "Lead Line Item [code]<a href='/sn_lead_mgmt_core_lead_line_item.do?sys_id=013daa19ffde8210b85dffffffffff82'>LEADL0000003</a>[/code] has been updated  [code] <b> Quantity </b> [/code] 10 [code] <i>was</i> [/code] 6"
    },
    {
      "author": "Abel Tuter",
      "date": "2024-12-11 00:45:52",
      "text": "Lead Line Item [code]<a href='/sn_lead_mgmt_core_lead_line_item.do?sys_id=37610e1780925210f877983fa0be6725'>LEADL0001002</a>[/code] has been created  [code] <b> Product Offering </b> [/code] Solana Modem M Series [code] <b> Quantity </b> [/code] 1"
    },
    {
      "author": "Abel Tuter",
      "date": "2024-12-11 00:45:51",
      "text": "Work notes for lead"
    }
  ],
  "do_not_call": false,
  "lead_rating": "200_warm",
  "account": null,
  "external_system": null,
  "lead_line_items": [
    {
      "quantity": 10,
      "product_offering": {
        "sys_id": "32619d9fd0a63110f8770dbf976be1f9",
        "name": "Safety Test Coverage",
        "code": "SAFETSTCVG1"
      },
      "sys_mod_count": 1,
      "external_id": null,
      "sys_updated_on": {
        "value": "2024-12-11 08:45:52",
        "display_value": "2024-12-11 00:45:52"
      },
      "sys_tags": null,
      "lead": {
        "sys_id": "856b6a95ffde8210b85dffffffffffd7",
        "name": "LEAD0000001"
      },
      "number": "LEADL0000003",
      "sys_id": "013daa19ffde8210b85dffffffffff82",
      "unit_of_measurement": {
        "sys_id": "cb2795d553020110286eddeeff7b12ff",
        "name": "Each"
      },
      "sys_updated_by": "abel.tuter",
      "sys_created_on": {
        "value": "2024-05-20 10:38:41",
        "display_value": "2024-05-20 03:38:41"
      },
      "work_notes": null,
      "sys_created_by": "abel.tuter",
      "external_system": null
    },
    {
      "quantity": 1,
      "product_offering": {
        "sys_id": "0b61dd9fd0a63110f8770dbf976be171",
        "name": "Solana Modem M Series",
        "code": "SOLANAMODE2"
      },
      "sys_mod_count": 0,
      "external_id": null,
      "sys_updated_on": {
        "value": "2024-12-11 08:45:52",
        "display_value": "2024-12-11 00:45:52"
      },
      "sys_tags": null,
      "lead": {
        "sys_id": "856b6a95ffde8210b85dffffffffffd7",
        "name": "LEAD0000001"
      },
      "number": "LEADL0001002",
      "sys_id": "37610e1780925210f877983fa0be6725",
      "unit_of_measurement": null,
      "sys_updated_by": "abel.tuter",
      "sys_created_on": {
        "value": "2024-12-11 08:45:52",
        "display_value": "2024-12-11 00:45:52"
      },
      "work_notes": null,
      "sys_created_by": "abel.tuter",
      "external_system": null
    }
  ]
}
```

## lead - POST /sn\_lead\_mgmt\_core/lead

Creates a lead record and its associated lead line items using the specified parameters.

Once processed, records are created in the following tables:

-   Lead \[sn\_lead\_mgmt\_core\_lead\]
-   Lead Line Item \[sn\_lead\_mgmt\_core\_lead\_line\_item\]

Rules for passed-in parameters:

-   Invalid parameter names are ignored.
-   Invalid values for non-mandatory choice and reference fields are ignored.
-   If field WRITE access is denied for one or more fields, the restricted fields are ignored.
-   You can't insert system field values using this API. Any provided values are ignored. System fields are a part of the ignored fields list, which is configurable.
-   The values of the parameters **account**, **contact**, and **consumer** are ignored if both the **account** and **consumer** parameters are non-empty.
-   Unless otherwise specified, the default value for all non-passed parameters is 'null'.

### URL format

Versioned URL: `/api/sn_lead_mgmt_core/{api_version}/lead`

Default URL: `/api/sn_lead_mgmt_core/{api_version}/lead`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="lead-account-row"><td>

account

</td><td id="lead-account-entry">

Details on the account associated with the lead.Data type: Object

```
"account": {
  "sys_id": "String"
}
```

</td></tr><tr><td>

account.sys\_id

</td><td id="lead-account.sys_id-entry">

Sys\_id of the associated account record.

Data type: String

 Table: Account \[customer\_account\]

</td></tr><tr><td>

business\_phone

</td><td id="lead-business_phone-entry">

Lead's business phone number.Data type: String

</td></tr><tr><td>

city

</td><td id="lead-city-entry">

City in which the lead resides.Data type: String

</td></tr><tr><td>

company

</td><td id="lead-company-entry">

Lead's company name.Data type: String

</td></tr><tr><td>

consumer

</td><td>

Consumer associated with the lead.Data type: Object

```
"consumer": { 
  "sys_id": "String" 
} 
```

</td></tr><tr><td>

consumer.sys\_id

</td><td id="lead-consumer.sys_id-entry">

Sys\_id of the associated consumer record.

Data type: String

 Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

contact

</td><td>

Contact associated with the lead account.Data type: Object

```
"contact": { 
  "sys_id": "String" 
} 
```

</td></tr><tr><td>

contact.sys\_id

</td><td id="lead-contact.sys_id-entry">

Sys\_id of the associated contact record.

Data type: String

 Table: Contact \[customer\_contact\]

</td></tr><tr><td>

country

</td><td id="lead-country-entry">

Country in which the lead resides.Data type: String

</td></tr><tr><td>

do\_not\_call

</td><td>

Flag that indicates whether the mode of communication is by phone.

Valid values:

-   true: Can call contact.
-   false: Don't call contact.

Data type: Boolean

 Default: false

</td></tr><tr><td>

do\_not\_email

</td><td>

Flag that indicates whether the mode of communication is by email.

Valid values:

-   true: Can email contact.
-   false: Don't email contact.

Data type: Boolean

 Default: false

</td></tr><tr><td>

do\_not\_share

</td><td>

Flag that indicates whether the lead details can be shared.

Valid values:

-   true: Lead details can be shared.
-   false: Lead details can't be shared.

Data type: Boolean

 Default: false

</td></tr><tr><td>

email

</td><td id="lead-email-entry">

Lead's email address.Data type: String

</td></tr><tr><td>

external\_id

</td><td id="lead-external_id-entry">

ID used by the system that generated the lead to identify the lead in the associated system.Data type: String

</td></tr><tr><td>

external\_system

</td><td id="lead-external_system-entry">

Name of the external system associated with the lead, such as HubSpot or pipedrive.Data type: String

</td></tr><tr><td>

first\_name

</td><td id="lead-first_name-entry">

First name of the contact associated with the lead.Data type: String

</td></tr><tr><td>

industry

</td><td id="lead-industry-entry">

Industry to which the lead belongs.Data type: String

Table: Located in the **industry** field of the Account \[customer\_account\] table.

</td></tr><tr><td>

last\_name

</td><td>

Required. Last name of the contact associated with the lead.

Data type: String

</td></tr><tr><td>

lead\_group

</td><td>

Group to which the lead belongs.

Data type: Object

 ```
"lead_group": {
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_group.sys\_id

</td><td id="lead-lead_group.sys_id-entry">

Sys\_id of the lead group record.Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

lead\_line\_items

</td><td>

List of lead line items to associated with the lead.Group to which the lead belongs.

Data type: Object

```
"lead_line_items": [ 
  { 
    "external_id": "String",
    "external_system": "String",
    "product_offering": {Object},
    "quantity": Number, 
    "work_notes": [Array],
    "unit_of_measurement": {Object} 
  } 
] 
```

Maximum line items: 100 - any over that are ignored

</td></tr><tr><td>

lead\_line\_items.​external\_id

</td><td id="lead-lead_line_items.external_id-entry">

ID used by the system that generated the lead line item to identify the line item in the associated system.Data type: String

</td></tr><tr><td>

lead\_line\_items.​external\_system

</td><td id="lead-lead_line_items.external_system-entry">

Name of the external system associated with the lead line item, such as HubSpot or pipedrive.Data type: String

</td></tr><tr><td>

lead\_line\_items.product\_offering

</td><td>

Required. Information about the product offering associated with the lead line item.Data type: Object

```
"product_offering": {
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.product\_offering.sys\_id

</td><td>

Required. Sys\_id of the product offering record associated with the lead line item.

Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

lead\_line\_items.quantity

</td><td>

Quantity of items the lead wants to purchase of the associated product offering.

Data type: Number \(Integer\)

 Default: 1

</td></tr><tr><td>

lead\_line\_items.unit\_of\_measurement

</td><td>

Details of the measuring unit of lead line item.

Data type: Object

 ```
"unit_of_measurement": {
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​unit\_of\_measurement.​sys\_id

</td><td id="lead-lead_line_items.unit_of_measurement.sys_id-entry">

Sys\_id of the record that describes the measuring unit.Data type: String

Table: Unit of Measure \[sn\_prd\_pm\_uom\]

</td></tr><tr><td>

lead\_line\_items.work\_notes

</td><td>

List that describes the work notes created for the lead line item.

Data type: Array of Objects

```
"work_notes": [
    "text": "String"
  }
]
```

Default: Empty array

</td></tr><tr><td>

lead\_line\_items.​work\_notes.​text

</td><td id="lead-lead_line_items.work_notes.text-entry">

Text of the note made by the author.Data type: String

</td></tr><tr><td>

lead\_rating

</td><td id="lead-lead_rating-entry">

Rating for the lead such as, 100\_cold, 200\_warm, 300\_hot, or 400\_super\_hot.**Note:** This is a choice field. It must contain one of the choice items defined in the lead\_rating field of the Leads table.

Data type: String

</td></tr><tr><td>

lead\_score

</td><td id="lead-lead_score-entry">

Score for the lead.Data type: Decimal

Range: 1 to 100

</td></tr><tr><td>

lead\_source

</td><td id="lead-lead_source-entry">

Originator of the lead.**Note:** This is a choice field. It must contain one of the choice items defined in the lead\_source field of the Leads table.

Data type: String

</td></tr><tr><td>

lead\_type

</td><td id="lead-lead_type-entry">

Type of lead, such as New Business or Existing Business.

 **Note:** This is a choice field. It must contain one of the choice items defined in the lead\_type field of the Leads table.

 Data type: String

</td></tr><tr><td>

middle\_name

</td><td id="lead-middle_name-entry">

Middle name of the contact for the lead.Data type: String

</td></tr><tr><td>

mobile\_phone

</td><td id="lead-mobile_phone-entry">

Phone number of the contact for the lead.Data type: String

</td></tr><tr><td>

other\_reason

</td><td id="lead-other_reason-entry">

Additional reason for the lead disqualification.Data type: String

Max length: 160 characters

</td></tr><tr><td>

owner

</td><td>

Details of the person associated with the lead.

Data type: Object

 ```
"owner": {
  "sys_id": "String"
}
```

</td></tr><tr><td>

owner.sys\_id

</td><td id="lead-owner.sys_id-entry">

Sys\_id of the user record of the person that owns the lead.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

reason

</td><td id="lead-reason-entry">

Reason for the lead disqualification such as, Disqualify.Data type: String

Max length: 40 characters

</td></tr><tr><td>

short\_description

</td><td id="lead-short_description-entry">

Short description of the lead.Data type: String

Max length: 160 characters

</td></tr><tr><td>

similar\_lead

</td><td>

Details on any similar lead. Use this for possible lead disqualification.

Data type: Object

 ```
"similar_lead": {
  "sys_id": "String"
}
```

</td></tr><tr><td>

similar\_lead.sys\_id

</td><td id="lead-similar_lead.sys_id-entry">

Sys\_id of the lead record that is a possible duplicate lead.Data type: String

Table: Lead \[sn\_lead\_mgmt\_core\_lead\]

</td></tr><tr><td>

stage

</td><td>

Stage of the lead such as, 100\_new.

**Note:** This is a choice field. It must contain one of the choice items defined in the stage field of the Leads table.

Data type: String

 Default: 100\_new

</td></tr><tr><td>

state

</td><td id="lead-state-entry">

State in which the lead resides.Data type: String

</td></tr><tr><td>

street

</td><td id="lead-street-entry">

Street on which the lead resides.Data type: String

</td></tr><tr><td>

title

</td><td id="lead-title-entry">

Lead's title.Data type: String

</td></tr><tr><td>

website

</td><td id="lead-website-entry">

Lead's website URL.Data type: String

</td></tr><tr><td>

work\_notes

</td><td>

List of work notes created for the lead.

Data type: Array of Objects

 ```
"work_notes": [
  {
    "text": "String"
  }
]
```

 **Note:** An array of work notes in the request is inserted as a single text. This text is generated by combining the content from all work note objects in the request, with each entry separated by a comma \(,\).

 Default: Empty array

</td></tr><tr><td>

work\_notes.​text

</td><td id="lead-work_notes.text-entry">

Text of the note made by the author.Data type: String

</td></tr><tr><td>

zip

</td><td id="lead-zip-entry">

Zip code of the associated lead.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

201

</td><td>

Successful. Lead and its associated line items are inserted successfully.

</td></tr><tr><td>

400

</td><td id="lead-400-status_code-entry">

Error. Possible reasons: -   Invalid payload: Invalid/empty request body.
-   Invalid payload: Invalid field value for email/phone number fields.
-   Invalid payload: Mandatory field is absent, or its value is empty.
-   Business rule/data policy violation.

</td></tr><tr><td>

403

</td><td id="entry-403-status-code">

Forbidden. The user doesn't have access rights to the specified record.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td id="d3360e67">

Account linked to the lead.Data type: Object

```
"account": { 
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

account.name

</td><td id="lead-account.name-entry">

Name of the account.Data type: String

</td></tr><tr><td>

account.sys\_id

</td><td id="d3360e91">

Sys\_id of the associated account record.

Data type: String

 Table: Account \[customer\_account\]

</td></tr><tr><td>

business\_phone

</td><td id="d3360e108">

Lead's business phone number.Data type: String

</td></tr><tr><td>

city

</td><td id="d3360e119">

City in which the lead resides.Data type: String

</td></tr><tr><td>

closed\_date

</td><td id="lead-closed_date-entry">

Date and time when the lead was closed.Data type: Object

```
"closed_date": {
  "display_value": "String", 
  "value": "String"
} 
```

</td></tr><tr><td>

closed\_date.​display\_value

</td><td id="lead-closed_date.display_value-entry">

Date and time as displayed in the UI. Data type: String

Format: User's format and time zone.

</td></tr><tr><td>

closed\_date.value

</td><td id="lead-closed_date.value-entry">

Date and time that the lead closed as defined in the associated record.Data type: String

Format: UTC

</td></tr><tr><td>

company

</td><td id="d3360e171">

Lead's company name.Data type: String

</td></tr><tr><td>

consumer

</td><td id="lead-consumer-entry">

Consumer associated with the lead.Data type: Object

```
"consumer": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

consumer.name

</td><td id="lead-consumer.name-entry">

Name of the associated consumer.Data type: String

</td></tr><tr><td>

consumer.sys\_id

</td><td id="d3360e208">

Sys\_id of the associated consumer record.

Data type: String

 Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

contact

</td><td id="lead-contact-entry">

Contact associated with the lead account.Data type: Object

```
"contact": {
  "name": "String",
  "sys_id": "String" 
} 
```

</td></tr><tr><td>

contact.name

</td><td id="lead-contact.name-entry">

Contact's name.Data type: String

</td></tr><tr><td>

contact.sys\_id

</td><td id="d3360e250">

Sys\_id of the associated contact record.

Data type: String

 Table: Contact \[customer\_contact\]

</td></tr><tr><td>

country

</td><td id="d3360e267">

Country in which the lead resides.Data type: String

</td></tr><tr><td>

do\_not\_call

</td><td id="lead-do_not_call-entry">

Flag that indicates whether the mode of communication is by phone.

Valid values:

-   true: Can call contact.
-   false: Don't call contact.

Data type: Boolean

</td></tr><tr><td>

do\_not\_email

</td><td id="lead-do_not_email-entry">

Flag that indicates whether the mode of communication is by email.

Valid values:

-   true: Can email contact.
-   false: Don't email contact.

Data type: Boolean

</td></tr><tr><td>

do\_not\_share

</td><td id="lead-do_not_share-entry">

Flag that indicates whether the lead details can be shared.

Valid values:

-   true: Lead details can be shared.
-   false: Lead details can't be shared.

Data type: Boolean

</td></tr><tr><td>

email

</td><td id="d3360e351">

Lead's email address.Data type: String

</td></tr><tr><td>

external\_id

</td><td id="d3360e362">

ID used by the system that generated the lead to identify the lead in the associated system.Data type: String

</td></tr><tr><td>

external\_system

</td><td id="d3360e373">

Name of the external system associated with the lead, such as HubSpot or pipedrive.Data type: String

</td></tr><tr><td>

first\_name

</td><td id="d3360e384">

First name of the contact associated with the lead.Data type: String

</td></tr><tr><td>

industry

</td><td id="d3360e396">

Industry to which the lead belongs.Data type: String

Table: Located in the **industry** field of the Account \[customer\_account\] table.

</td></tr><tr><td>

last\_name

</td><td id="lead-last_name-entry">

Last name of the contact associated with the lead.

Data type: String

</td></tr><tr><td>

lead\_group

</td><td id="lead-lead_group-entry">

Group to which the lead belongs.

Data type: Object

 ```
"lead_group": {
  "name: "String",
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_group.name

</td><td id="lead-lead_group.name-entry">

Lead group's name.Data type: String

</td></tr><tr><td>

lead\_group.sys\_id

</td><td id="d3360e454">

Sys\_id of the lead group record.Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

lead\_line\_items

</td><td id="lead-lead_line_items-entry">

Details of the lead line items associated with the lead.Data type: Array of Objects

```
"lead_line_items": [ 
  { 
    "external_id": "String", 
    "external_system": "String",
    "lead": {Object},
    "number": "String",
    "product_offering": {Object},
    "quantity": Number,
    "sys_created_by”: "String",
    "sys_created_on {Object},
    "sys_domain": "String",
    "sys_domain_path": "String",
    "sys_id": "String",
    "sys_mod_count": Number,
    "sys_tags": [Array],
    "sys_updated_by: "String",
    "sys_updated_on: {Object},
    "unit_of_measurement": {Object}, 
    "work_notes": [Array]
  } 
] 
```

</td></tr><tr><td>

lead\_line\_items.​external\_id

</td><td id="d3360e481">

ID used by the system that generated the lead line item to identify the line item in the associated system.Data type: String

</td></tr><tr><td>

lead\_line\_items.​external\_system

</td><td id="d3360e492">

Name of the external system associated with the lead line item, such as HubSpot or pipedrive.Data type: String

</td></tr><tr><td>

lead\_line\_items.​lead

</td><td id="lead-lead_line_items.lead-entry">

Details about the lead associated with the line item.Data type: Object

```
"lead: {
  "name": "String",
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​lead.name

</td><td id="lead-lead_line_items.lead.name-entry">

Associated lead's name.Data type: String

</td></tr><tr><td>

lead\_line\_items.​lead.sys\_id

</td><td id="lead-lead_line_items.lead.sys_id-entry">

Sys\_id of the associated lead record.Data type: String

</td></tr><tr><td>

lead\_line\_items.​number

</td><td id="lead-lead_line_items.number-entry">

Unique system-generated number of the lead line item record.Data type: String

</td></tr><tr><td>

lead\_line\_items.​product\_offering

</td><td id="lead-lead_line_items.product_offering-entry">

Information about the product offering associated with the lead line item.Data type: Object

```
"product_offering": {
  "code": " String",
  "name": "String",
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​product\_offering.code

</td><td id="lead-lead_line_items.product_offering.code-entry">

Code linked to the product offering. **Note:** This is a system-generated alphanumeric number based on the product name. Although system generated, you can edit the code to represent a SKU or any other industry specific product codes.

Data type: String

</td></tr><tr><td>

lead\_line\_items.​product\_offering.name

</td><td id="lead-lead_line_items.product_offering.name-entry">

Product offering's name.Data type: String

</td></tr><tr><td>

lead\_line\_items.​product\_offering.sys\_id

</td><td id="lead-lead_line_items.product_offering.sys_id-entry">

Sys\_id of the product offering record associated with the lead line item.

Data type: String

 Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

lead\_line\_items.​quantity

</td><td id="lead-lead_line_items.quantity-entry">

Quantity of items the lead wants to purchase of the associated product offering.

Data type: Number \(Integer\)

</td></tr><tr><td>

lead\_line\_items.​sys\_created\_by

</td><td id="lead-lead_line_items.sys_created_by-entry">

User name of the person that created the lead line item.Data type: String

</td></tr><tr><td>

lead\_line\_items.​sys\_created\_on

</td><td id="lead-lead_line_items.sys_created_on-entry">

System-generated date and time that the lead line item was created.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "value": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​sys\_created\_on.display\_value

</td><td id="lead-lead_line_items.sys_created_on.display_value-entry">

Date and time that the lead line item was created.Data type: String

Format: Default instance format and time zone

</td></tr><tr><td>

lead\_line\_items.​sys\_created\_on.value

</td><td id="lead-lead_line_items.sys_created_on.value-entry">

Date and time that the lead line item was created.Data type: String

Format: UTC

</td></tr><tr><td>

lead\_line\_items.​sys\_domain

</td><td id="lead-lead_line_items.sys_domain-entry">

Sys\_id of the domain record to which the lead line item belongs. **Note:** This parameter is only returned in the response if domain separation is enabled.

Data type: String

</td></tr><tr><td>

lead\_line\_items.sys\_domain\_path

</td><td id="lead-lead_line_items.sys_domain_path-entry">

Path of the domain to which the lead line item belongs. **Note:** This parameter is only returned in the response if domain separation is enabled.

Data type: String

</td></tr><tr><td>

lead\_line\_items.​sys\_id

</td><td id="lead-lead_line_items.sys_id-entry">

Sys\_id of the lead line item record.Data type: String

</td></tr><tr><td>

lead\_line\_items.​sys\_mod\_count

</td><td id="lead-lead_line_items.sys_mod_count-entry">

Number of times the associated lead line item record has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

lead\_line\_items.​sys\_tags

</td><td id="lead-lead_line_items.sys_tags-entry">

List of system tags associated with the lead line item.Data type: Array

</td></tr><tr><td>

lead\_line\_items.​sys\_updated\_by

</td><td id="lead-lead_line_items.sys_updated_by-entry">

User name of the person that last updated the associated lead line item.Data type: String

</td></tr><tr><td>

lead\_line\_items.​sys\_updated\_on

</td><td id="lead-lead_line_items.sys_updated_on-entry">

System-generated date and time when the lead line item was last updated.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "value": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​sys\_updated\_on.​display\_value

</td><td id="lead-lead_line_items.sys_updated_on.display_value-entry">

Date and time that the lead line item was last updated.Data type: String

Format: Default instance format and time zone

</td></tr><tr><td>

lead\_line\_items.​sys\_updated\_on.​value

</td><td id="lead-lead_line_items.sys_updated_on.value-entry">

Date and time that the lead line item was last updated.Data type: String

Format: UTC

</td></tr><tr><td>

lead\_line\_items.​unit\_of\_measurement

</td><td id="lead-lead_line_items.unit_of_measurement-entry">

Details of the measuring unit of lead line item.

Data type: Object

 ```
"unit_of_measurement": {
  "name": "String",
  "sys_id": "String"
} 
```

</td></tr><tr><td>

lead\_line\_items.​unit\_of\_measurement.​name

</td><td id="lead-lead_line_items.unit_of_measurement.name-entry">

Name of the measuring unit such as, each or cubic foot.Data type: String

</td></tr><tr><td>

lead\_line\_items.​unit\_of\_measurement.​sys\_id

</td><td id="d3360e809">

Sys\_id of the record that describes the measuring unit.Data type: String

Table: Unit of Measure \[sn\_prd\_pm\_uom\]

</td></tr><tr><td>

lead\_line\_items.​work\_notes

</td><td id="lead-lead_line_items.work_notes-entry">

List that describes the work notes created for the lead line item.

Data type: Array of Objects

 ```
"work_notes": [
  {
    "author": "String",
    "date": "String",
    "text": "String"
  }
]
```

</td></tr><tr><td>

lead\_line\_items.​work\_notes.​author

</td><td id="lead-lead_line_items.work_notes.author-entry">

User name of the person that authored the associated work note.Data type: String

</td></tr><tr><td>

lead\_line\_items.​work\_notes.​date

</td><td id="lead-lead_line_items.work_notes.date-entry">

Date that the note was created.Data type: String

</td></tr><tr><td>

lead\_line\_items.​work\_notes.​text

</td><td id="d3360e862">

Text of the note made by the author.Data type: String

</td></tr><tr><td>

lead\_rating

</td><td id="d3360e873">

Rating for the lead such as, 100\_cold, 200\_warm, 300\_hot, or 400\_super\_hot.**Note:** This is a choice field. It must contain one of the choice items defined in the lead\_rating field of the Leads table.

Data type: String

</td></tr><tr><td>

lead\_score

</td><td id="d3360e886">

Score for the lead.Data type: Decimal

Range: 1 to 100

</td></tr><tr><td>

lead\_source

</td><td id="d3360e899">

Originator of the lead.**Note:** This is a choice field. It must contain one of the choice items defined in the lead\_source field of the Leads table.

Data type: String

</td></tr><tr><td>

lead\_type

</td><td id="d3360e912">

Type of lead, such as New Business or Existing Business.

 **Note:** This is a choice field. It must contain one of the choice items defined in the lead\_type field of the Leads table.

 Data type: String

</td></tr><tr><td>

middle\_name

</td><td id="d3360e930">

Middle name of the contact for the lead.Data type: String

</td></tr><tr><td>

mobile\_phone

</td><td id="d3360e942">

Phone number of the contact for the lead.Data type: String

</td></tr><tr><td>

number

</td><td id="lead-number-entry">

Unique system-generated number of the lead record.Data type: String

</td></tr><tr><td>

other\_reason

</td><td id="d3360e964">

Additional reason for the lead disqualification.Data type: String

Max length: 160 characters

</td></tr><tr><td>

owner

</td><td id="lead-owner-entry">

Details of the person associated with the lead.

Data type: Object

 ```
"owner": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

owner.name

</td><td id="lead-owner.name-entry">

Name of the person that owns the lead.Data type: String

</td></tr><tr><td>

owner.sys\_id

</td><td id="d3360e1005">

Sys\_id of the user record of the person that owns the lead.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

reason

</td><td id="d3360e1019">

Reason for the lead disqualification such as, Disqualify.Data type: String

Max length: 40 characters

</td></tr><tr><td>

short\_description

</td><td id="d3360e1032">

Short description of the lead.Data type: String

Max length: 160 characters

</td></tr><tr><td>

similar\_lead

</td><td id="lead-similar_lead-entry">

Details on any similar lead. Use this for possible lead disqualification.

Data type: Object

 ```
"similar_lead": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

similar\_lead.name

</td><td id="lead-similar_lead.name-entry">

Name of the duplicate lead.Data type: String

</td></tr><tr><td>

similar\_lead.sys\_id

</td><td id="d3360e1073">

Sys\_id of the lead record that is a possible duplicate lead.Data type: String

Table: Lead \[sn\_lead\_mgmt\_core\_lead\]

</td></tr><tr><td>

stage

</td><td id="lead-stage-entry">

Stage of the lead such as, 100\_new.

**Note:** This is a choice field. It must contain one of the choice items defined in the stage field of the Leads table.

Data type: String

</td></tr><tr><td>

state

</td><td id="d3360e1103">

State in which the lead resides.Data type: String

</td></tr><tr><td>

street

</td><td id="d3360e1114">

Street on which the lead resides.Data type: String

</td></tr><tr><td>

sys\_class\_name

</td><td id="lead-sys_class_name-entry">

System-generated class name of the Lead table.Data type: String

</td></tr><tr><td>

sys\_created\_by

</td><td id="lead-sys_created_by-entry">

User name of the person that created the lead.Data type: String

</td></tr><tr><td>

sys\_created\_on

</td><td id="lead-sys_created_on-entry">

System-generated date and time that the lead was created.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "value": "String"
} 
```

</td></tr><tr><td>

sys\_created\_on.​display\_value

</td><td id="lead-sys_created_on.display_value-entry">

Date and time when the lead was created.Data type: String

Format: Default instance format and time zone

</td></tr><tr><td>

sys\_created\_on.​value

</td><td id="lead-sys_created_on.value-entry">

Date and time when the lead was created.Data type: String

Format: UTC

</td></tr><tr><td>

sys\_domain

</td><td id="lead-sys_domain-entry">

Sys\_id of the domain record to which the lead belongs. **Note:** This parameter is only returned in the response if domain separation is enabled.

Data type: String

</td></tr><tr><td>

sys\_domain\_path

</td><td id="lead-sys_domain_path-entry">

Path of the domain to which the lead belongs. **Note:** This parameter is only returned in the response if domain separation is enabled.

Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="lead-sys_id-entry">

Sys\_id of the lead record.Data type: String

Table: Lead \[sn\_lead\_mgmt\_core\_lead\]

</td></tr><tr><td>

sys\_mod\_count

</td><td id="lead-sys_mod_count-entry">

Number of times the associated lead record has been modified.Data type: Number \(Integer\)

</td></tr><tr><td>

sys\_tags

</td><td id="lead-sys_tags-entry">

List of system tags associated with the lead. You can use these tags to categorize leads.Data type: Array

</td></tr><tr><td>

sys\_updated\_by

</td><td id="lead-sys_updated_by-entry">

User name of the person that last updated the lead record.Data type: String

</td></tr><tr><td>

sys\_updated\_on

</td><td id="lead-sys_updated_on-entry">

System-generated date and time when the lead was last updated.Data type: Object

```
"sys_created_on": {
  "display_value": "String",
  "value": "String"
} 
```

</td></tr><tr><td>

sys\_updated\_on.​display\_value

</td><td id="lead-sys_updated_on.display_value-entry">

Date and time that the lead was last updated.Data type: String

Format: Instance's default format and time zone

</td></tr><tr><td>

sys\_updated\_on.​value

</td><td id="lead-sys_updated_on.value-entry">

Date and time that the lead was last updated.Data type: String

Format: UTC

</td></tr><tr><td>

title

</td><td id="d3360e1299">

Lead's title.Data type: String

</td></tr><tr><td>

website

</td><td id="d3360e1310">

Lead's website URL.Data type: String

</td></tr><tr><td>

work\_notes

</td><td id="lead-work_notes-entry">

List of work notes created for the lead.

Data type: Array of Objects

 ```
"work_notes": [
  {
    "author": "String",
    "date": "String",
    "text": "String"
  }
]
```

</td></tr><tr><td>

work\_notes.​author

</td><td id="lead-work_notes.author-entry">

User name of the person that authored the associated work note.Data type: String

</td></tr><tr><td>

work\_notes.​date

</td><td id="lead-work_notes.date-entry">

Date that the note was created.Data type: String

</td></tr><tr><td>

work\_notes.​text

</td><td id="d3360e1361">

Text of the note made by the author.Data type: String

</td></tr><tr><td>

zip

</td><td id="d3360e1372">

Zip code of the associated lead.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to create a new lead record with one lead line item.

```
curl " https://instance.service-now.com/api/sn_lead_mgmt_core/v1/lead" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data " {
    "short_description": "Looking for a quote on preventative maintenance plans for their corporate office building elevators.",
    "country": "USA",
    "city": "San Francisco",
    "lead_source": "inbound_phone",
    "industry": "manufacturing",
    "title": "Director of Building operations",
    "business_phone": "+1 (555) 123-4567",
    "street": "789, Industrial drive",
    "company": "Lee Manufacturing Inc",
    "state": "CA",
    "first_name": "James",
    "email": "james.wilson@email.com",
    "consumer": {
      "sys_id": "46ce64ef99ca5210f8779c3cc41bb03c"
    },
    "zip": "94016",
    "website": "example.com",
    "last_name": "Wilson",
    "middle_name": null,
    "do_not_share": false,
    "lead_score": 92,
    "stage": "100_new",
    "do_not_email": false,
    "lead_type": "existing_business",
    "work_notes": [
      {
        "text": "Work notes for lead"
      }
    ],
    "do_not_call": true,
    "lead_rating": "200_warm",
    "lead_line_items": [
      {
        "quantity": 1,
        "product_offering": {
          "sys_id": "32619d9fd0a63110f8770dbf976be1f9"
        },
        "unit_of_measurement": { 
          "sys_id": "cb2795d553020110286eddeeff7b12ff"
        }
      }
  ]
}
```

The response contains the fields in the lead and lead line items records.

```
{
  "short_description": "Looking for a quote on preventative maintenance plans for their corporate office building elevators.",
  "reason": null,
  "country": "USA",
  "closed_date": null,
  "city": "San Francisco",
  "lead_source": "inbound_phone",
  "external_id": null,
  "industry": "manufacturing",
  "sys_updated_on": {
    "value": "2024-12-11 08:35:26",
    "display_value": "2024-12-11 00:35:26"
  },
  "title": "Director of Building operations",
  "sys_class_name": "Lead",
  "number": "LEAD0001001",
  "sys_id": "030f795380925210f877983fa0be67c0",
  "business_phone": "+1 (555) 123-4567",
  "similar_lead": null,
  "sys_updated_by": "abel.tuter",
  "mobile_phone": null,
  "street": "789, Industrial drive",
  "sys_created_on": {
    "value": "2024-12-11 08:35:26",
    "display_value": "2024-12-11 00:35:26"
  },
  "contact": null,
  "company": "Lee Manufacturing Inc",
  "state": "CA",
  "first_name": "James",
  "email": "james.wilson@email.com",
  "consumer": {
    "sys_id": "46ce64ef99ca5210f8779c3cc41bb03c",
    "name": "test"
  },
  "sys_created_by": "abel.tuter",
  "zip": "94016",
  "owner": {
    "sys_id": "62826bf03710200044e0bfc8bcbe5df1",
    "name": "Abel Tuter"
  },
  "website": "example.com",
  "lead_group": null,
  "sys_mod_count": 1,
  "last_name": "Wilson",
  "other_reason": null,
  "middle_name": null,
  "sys_tags": null,
  "do_not_share": false,
  "lead_score": 92,
  "stage": "100_new",
  "do_not_email": false,
  "lead_type": "existing_business",
  "work_notes": [
    {
      "author": "Abel Tuter",
      "date": "2024-12-11 00:35:26",
      "text": "Work notes for lead"
    },
    {
      "author": "Abel Tuter",
      "date": "2024-12-11 00:35:26",
      "text": "Lead Line Item [code]<a href='/sn_lead_mgmt_core_lead_line_item.do?sys_id=830f795380925210f877983fa0be67c5'>LEADL0001001</a>[/code] has been created  [code] <b> Product Offering </b> [/code] Safety Test Coverage [code] <b> Quantity </b> [/code] 1 [code] <b> Unit of Measure </b> [/code] Each"
    }
  ],
  "do_not_call": true,
  "lead_rating": "200_warm",
  "account": null,
  "external_system": null,
  "lead_line_items": [
    {
      "quantity": 1,
      "product_offering": {
        "sys_id": "32619d9fd0a63110f8770dbf976be1f9",
        "name": "Safety Test Coverage",
        "code": "SAFETSTCVG1"
      },
      "sys_mod_count": 0,
      "external_id": null,
      "sys_updated_on": {
        "value": "2024-12-11 08:35:26",
        "display_value": "2024-12-11 00:35:26"
      },
      "sys_tags": null,
      "lead": {
        "sys_id": "030f795380925210f877983fa0be67c0",
        "name": "LEAD0001001"
      },
      "number": "LEADL0001001",
      "sys_id": "830f795380925210f877983fa0be67c5",
      "unit_of_measurement": {
        "sys_id": "cb2795d553020110286eddeeff7b12ff",
        "name": "Each"
      },
      "sys_updated_by": "abel.tuter",
      "sys_created_on": {
        "value": "2024-12-11 08:35:26",
        "display_value": "2024-12-11 00:35:26"
      },
      "work_notes": null,
      "sys_created_by": "abel.tuter",
      "external_system": null
    }
  ]
}
```

