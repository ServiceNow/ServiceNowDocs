---
title: System for Cross-domain Identity Management \(SCIM\) API
description: The System for Cross-domain Identity Management \(SCIM\) API provides endpoints to create, read, update, and delete operations on users and groups using the SCIM protocol.Deletes the specified group record from the Group \[sys\_user\_group\] table of a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Returns one or more group records from the Group \[sys\_user\_group\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Returns the specified group record from the Group \[sys\_user\_group\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Enables you to add, update, and delete specified fields in a group record in the Group \[sys\_user\_group\] table of a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Creates a group record in the Group \[sys\_user\_group\] table of a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Updates the specified group record in the Group \[sys\_user\_group\] table of a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Deletes the specified user record from the User \[sys\_user\] table of a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Returns one or more user records from the User \[sys\_user\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Returns the specified user record from the User \[sys\_user\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Enables you to add, replace, and remove specified fields in a user record in the User \[sys\_user\] table of a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Creates a user record in the User \[sys\_user\] table of a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Updates the specified user record in the User \[sys\_user\] table of a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Retrieves information about all System for Cross-domain Identity Management \(SCIM\) resource types supported by the associated ServiceNow instance.Retrieves information about the specified System for Cross-domain Identity Management \(SCIM\) resource type.Retrieves information about all System for Cross-domain Identity Management \(SCIM\) resource schemas supported by a ServiceNow instance. These schemas define the attributes available for each resource type.Retrieves information about the specified System for Cross-domain Identity Management \(SCIM\) resource schemas supported by a ServiceNow instance. These schemas define the attributes available for each resource type.Returns the configuration metadata to use to obtain information about the service capabilities, configurations, schemas, and resource types for the System for Cross-domain Identity Management \(SCIM\) endpoints available within a ServiceNow instance.Returns one or more company records from the Company \[core\_company\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Returns the specified company record from the Company \[core\_company\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Returns one or more cost center records from the Cost Center \[cmn\_cost\_center\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Returns the specified cost center record from the Cost Center \[cmn\_cost\_center\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Returns one or more department records from the Department \[cmn\_department\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Returns the specified department record from the Department \[cmn\_department\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Returns one or more location records from the Location \[cmn\_location\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.Returns the specified location record from the Location \[cmn\_location\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.
locale: en-US
release: xanadu
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 126
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# System for Cross-domain Identity Management \(SCIM\) API

The System for Cross-domain Identity Management \(SCIM\) API provides endpoints to create, read, update, and delete operations on users and groups using the SCIM protocol.

The SCIM protocol is an application-level HTTP-based protocol based on the HTTP \[[RFC7230](https://datatracker.ietf.org/doc/html/rfc7230)\] standard. Use this API for provisioning and managing identity data, such as users and groups, on the web and in cross-domain environments, such as enterprise-to-cloud service providers or inter-cloud scenarios.

To access this API, you must activate the SCIM v2 - ServiceNow® Cross-domain Identity Management \(com.snc.integration.scim2\) plugin.

## Resource mapping

The SCIM service has six resources:

-   User \(core and extension\)
-   Group \(core and extension\)
-   Company
-   CostCenter
-   Department
-   Location

Most of the attributes in these SCIM resources map to corresponding fields in an existing ServiceNow table. The following tables define these mappings. Attributes that do not correspond to fields in existing ServiceNow tables map to two SCIM-specific tables. For additional information on these tables, see [SCIM-specific tables](scim-api.md#).

The SCIM User resource has both core \(schema: urn:ietf:params:scim:schemas:core:2.0:User\) and extension \(urn:ietf:params:scim:schemas:extension:servicenow:2.0:User\) schemas. Most of the User core and extension schema attributes map to the User \[sys\_user\] table.

|SCIM attribute name|User field name|
|-------------------|---------------|
|active|active|
|addresses.country|country|
|addresses.default.country|country|
|addresses.home.country|country|
|addresses.locality|city|
|addresses.default.locality|city|
|addresses.home.locality|city|
|addresses.postalCode|zip|
|addresses.default.postalCode|zip|
|addresses.home.postalCode|zip|
|addresses.region|state|
|addresses.default.region|state|
|addresses.home.region|state|
|addresses.streetAddress|street|
|addresses.default.streetAddress|street|
|addresses.home.streetAddress|street|
|displayName|name|
|emails.value|email|
|emails.default.value|email|
|emails.work.value|email|
|id|sys\_id|
|meta.created|sys\_created\_on|
|meta.lastModified|sys\_updated\_on|
|name.familyName|last\_name|
|name.givenName|first\_name|
|name.honorificPrefix|introduction|
|name.middleName|middle\_name|
|phoneNumbers.value|phone|
|phoneNumbers.home.value|home\_phone|
|phoneNumbers.mobile.value|mobile\_phone|
|phoneNumbers.work.value|phone|
|preferredLanguage|preferred\_language|
|timezone|time\_zone|
|title|title|
|userName|user\_name|

|SCIM attribute name|Sys Scim User field name|
|-------------------|------------------------|
|externalId|external\_id|

The SCIM User extended schema \(urn:ietf:params:scim:schemas:extension:servicenow:2.0:User\) maps to the User \[sys\_user\] table.

|SCIM attribute name|User field name|
|-------------------|---------------|
|company.name|company.name|
|company.value|company.sys\_id|
|costCenter.name|cost\_center.name|
|costCenter.value|cost\_center.sys\_id|
|department.name|department.name|
|department.value|department.sys\_id|
|employeeNumber|employee\_number|
|gender|gender|
|location.name|location.name|
|location.value|location.sys\_id|
|manager.displayName|manager.name|
|manager.value|manager.sys\_id|

The SCIM Group resource schema \(urn:ietf:params:scim:schemas:core:2.0:Group\) maps to the Group \[sys\_user\_group\] table.

|SCIM attribute name|Group field name|
|-------------------|----------------|
|displayName|name|
|id|sys\_id|
|meta.created|sys\_created\_on|
|meta.lastModified|sys\_updated\_on|

The SCIM Group externalId parameter maps to the Sys Scim Group \[sys\_scim\_group\] table.

|SCIM attribute name|Sys Scim Group field name|
|-------------------|-------------------------|
|externalId|external\_id|

The SCIM Group ServiceNow extension schema \(urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group\) maps to the Group \[sys\_user\_group\] table.

|SCIM attribute name|Group field name|
|-------------------|----------------|
|company.value|company.sys\_id|
|company.name|company.name|

The SCIM Company resource schema \(urn:ietf:params:scim:schemas:custom:servicenow:2.0:Company\) maps to the Company \[core\_company\] table.

|SCIM attribute name|Company field name|
|-------------------|------------------|
|id|sys\_id|
|meta.created|sys\_created\_on|
|meta.lastModified|sys\_updated\_on|
|name|name|

The SCIM CostCenter resource schema \(urn:ietf:params:scim:schemas:custom:servicenow:2.0:CostCenter\) maps to the Cost Center \[cmn\_cost\_center\] table.

|SCIM attribute name|Cost Center field name|
|-------------------|----------------------|
|id|sys\_id|
|meta.created|sys\_created\_on|
|meta.lastModified|sys\_updated\_on|
|name|name|

The SCIM Department resource schema \(urn:ietf:params:scim:schemas:custom:servicenow:2.0:Department\) maps to the Department \[cmn\_department\] table.

|SCIM attribute name|Department field name|
|-------------------|---------------------|
|id|sys\_id|
|meta.created|sys\_created\_on|
|meta.lastModified|sys\_updated\_on|
|name|name|

The SCIM Location resource schema \(urn:ietf:params:scim:schemas:custom:servicenow:2.0:Location\) maps to the Location \[cmn\_location\] table.

|SCIM attribute name|Location field name|
|-------------------|-------------------|
|id|sys\_id|
|meta.created|sys\_created\_on|
|meta.lastModified|sys\_updated\_on|
|name|name|

## SCIM-specific tables

Two tables, Sys Scim User \[sys\_scim\_user\] and Sys Scim Group \[sys\_scim\_group\], contain the SCIM attributes that do not map to existing ServiceNow tables. The following define the contents of these tables.

<table id="table_w2h_nch_mrb"><thead><tr><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Created

</td><td>

Date and time that the associated record was created.Data type: String

 Maximum length: 40

</td></tr><tr><td>

Created by

</td><td>

Name of the entity that created the record.Data type: String

 Maximum length: 40

</td></tr><tr><td>

External ID

</td><td>

External ID used by the entity that created this user record to reference the user in their system.Data type: String

 Maximum length: 255

</td></tr><tr><td>

Sys ID

</td><td>

Unique identifier for the record within a ServiceNow instance.Data type: String

 Maximum length: 32

</td></tr><tr><td>

Updated

</td><td>

Date and time that the associated record was last updated.Data type: String

 Maximum length: 40

</td></tr><tr><td>

Updated by

</td><td>

Name of the entity that last updated the associated record.Data type: String

 Maximum length: 40

</td></tr><tr><td>

Updates

</td><td>

Number of times that the record has been updated.Data type: Integer

 Maximum length: 40

</td></tr><tr><td>

User

</td><td>

Reference to the user associated with this recordReference: User \[sys\_user\] table

 Maximum length: 32

</td></tr><tr><td>

User type

</td><td>

Type of user record. This value is used to identify the organization to user relationship.This can be any value, but typical values might include:

-   Contractor
-   Employee
-   External
-   Intern
-   Temp
-   Unknown

 Data type: String

 Maximum length: 40

</td></tr></tbody>
</table><table id="table_mpt_nch_mrb"><thead><tr><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Created

</td><td>

Date and time that the associated record was created.Data type: String

 Maximum length: 40

</td></tr><tr><td>

Created by

</td><td>

Name of the entity that created the record.Data type: String

 Maximum length: 40

</td></tr><tr><td>

External ID

</td><td>

External ID used by the entity that created this group record to reference the group in their system.Data type: String

 Maximum length: 255

</td></tr><tr><td>

Group

</td><td>

Reference to the group associated with this record.Reference: Group \[sys\_user\_group\] table

 Maximum length: 32

</td></tr><tr><td>

Sys ID

</td><td>

Unique identifier for the record within a ServiceNow instance.Data type: String

 Maximum length: 32

</td></tr><tr><td>

Updated

</td><td>

Date and time that the associated record was last updated.Data type: String

 Maximum length: 40

</td></tr><tr><td>

Updated by

</td><td>

Name of the entity that last updated the associated record.Data type: String

 Maximum length: 40

</td></tr><tr><td>

Updates

</td><td>

Number of times that the record has been updated.Data type: Integer

 Maximum length: 40

</td></tr></tbody>
</table>## Roles and access control lists

The scim\_admin role is required to access the SCIM-specific tables and the private SCIM endpoints and enables access to the User \[sys\_user\] and Group \[sys\_user\_group\] tables.

The SCIM service has four ACLs for accessing the Sys Scim User \[sys\_scim\_user\] table and the Sys Scim Group \[sys\_scim\_group\] table that enable create, delete, read, and write. These ACLs are only mapped to the scim\_admin role.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## SCIM - DELETE /scim/Groups/\{group\_id\}

Deletes the specified group record from the Group \[sys\_user\_group\] table of a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Groups/{group_id}`

Default URL: `/api/now/scim/Groups/{group_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

group\_id

</td><td>

Sys\_id of the group record to delete. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|204|No Content. The request was successfully processed.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

errors

</td><td id="errors-SCIM-entry">

Response that describes any errors that may have occurred during processing the request.Data type: Object

 ```
"errors": {
  "details": "String",
  "schemas": "String",
  "scimType": "String",
  "status": "String"
}
```

</td></tr><tr><td>

errors.detail

</td><td id="errors_details-SCIM-entry">

Detailed error message on why the request failed.Data type: String

</td></tr><tr><td>

errors.scimType

</td><td id="errors_scimType-SCIM-entry">

SCIM error detail keyword.Data type: String

</td></tr><tr><td>

errors.schemas

</td><td id="errors_schemas-SCIM-entry">

URI of the SCIM Schemas used to process the error response.Data type: Array of Strings

</td></tr><tr><td>

errors.status

</td><td id="errors_status-SCIM-entry">

HTTP status code for the error response.Data type: String

</td></tr></tbody>
</table>### cURL request to delete a group

This example shows how to delete a group record from the Group \[sys\_user\_group\] table.

```
curl "https://instance-servicenow.com/api/now/scim/Groups/a0a9e9fb1b7e3010593876a61a4bcbe0" \
--request DELETE \
--header "Accept:application/scim+json" \
```

## SCIM - GET /scim/Groups

Returns one or more group records from the Group \[sys\_user\_group\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

**Note:** A query that does not return any matches returns success \(HTTP status code 200\) with **totalResults** set to 0.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Groups`

Default URL: `/api/now/scim/Groups`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

count

</td><td id="count-SCIM-entry">

Number of records to return. A negative value is interpreted as zero.Data type: Number

 Maximum: 500 - A value greater than this results in a bad request error.

 Default: 10

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr><tr><td>

filter

</td><td id="group_filter-SCIM-entry">

Filter expression to apply to the return results. Field filters are expressed as `<field_name> <operator> <"value">`. Refer to [RFC7644](https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2) for a list of the valid operators. **Note:** The `NOT` operator is not supported by this method.

 For example, to filter for all groups whose name starts with "HR", enter `displayName SW "HR"`.

 To specify more than one field filter, concatenate the filters using the `AND` operand. For example, to filter for all groups whose name starts with "HR" and were last modified before October 3, 2021, enter `displayName SW "HR" AND meta.lastModified lt "2021-10-33T00:00:00Z"`. Use dot-walking to specify nested attributes.

 Only the following SCIM group fields are available for use in filters:

-   displayName
-   externalId: Only supports `EQ` operator.
-   id
-   meta.created
-   meta.lastModified

 Data type: String

 Default: No filtering

</td></tr><tr><td>

sortBy

</td><td id="group_sortBy-SCIM-entry">

Must be specified with the **sortOrder** parameter. Field by which to sort the return results. Sorting is case-insensitive. You can only use those parameters available for filtering for the **sortBy** parameter, except that **externalId** is not allowed.

 For values that are null:

-   sorted by ascending - Null values are sorted to the top.
-   sorted by descending - Null values are sorted to the bottom.

 Data type: String

 Default: No sort

</td></tr><tr><td>

sortOrder

</td><td id="sortOrder-SCIM-entry">

Must be specified with the **sortBy** parameter. Order in which the **sortBy** parameter is applied to the return results. Valid values:

-   ascending
-   descending

 Data type: String

 Default: ascending

</td></tr><tr><td>

startIndex

</td><td id="group_startIndex-SCIM-entry">

One-based index into the table at which to start retrieving records. For example, if you set this parameter to 100, and the **count** parameter to 20, the endpoint returns records 100 through 119. **Note:** Any value that is set to less than one is interpreted as one.

 Data type: String

 Default: 1

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td id="status_400-SCIM-entry">

Bad Request. A bad request type or malformed request was detected.-   Ensure that both the **attributes** and **excludedAttributes** query parameters have not been passed in the request.
-   Ensure that the **count** parameter is not greater than 500.
-   Ensure that all **filter** parameters are valid.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

itemsPerPage

</td><td id="itemsPerPage-SCIM-entry">

Number of records returned in the return results.Data type: Number

</td></tr><tr><td>

Resources

</td><td>

List of group records.Data type: Array of Objects

 ```
"Resources": [
  {
    "company": {Object},
    "displayName": "String",
    "externalId": "String",
    "id": "String",
    "meta": [Array]
  }
]
```

</td></tr><tr><td>

Resources.company

</td><td>

Details about the group's company or organization.Data type: Object

 ```
"company": {
  "display": "String",
  "$ref": "String",
  "value": "String"
}
```

</td></tr><tr><td>

Resources.company.display

</td><td>

Name of the company.Data type: String

</td></tr><tr><td>

Resources.company.$ref

</td><td>

Reference URI of the company.Format: `<host>/Companies/<company sys_id>`, such as: `http://instance-servicenow.com/api/now/scim/Companies/81fd65ecac1d55eb42a426568fc87a63`.

 Data type: String

</td></tr><tr><td>

Resources.company.value

</td><td>

Sys\_id of the associated company.Data type: String

</td></tr><tr><td>

Resources.displayName

</td><td>

Human-readable name of the group, such as HR Team.Data type: String

</td></tr><tr><td>

Resources.externalId

</td><td>

Unique identifier assigned to the group by the entity provisioning it.Data type: String

</td></tr><tr><td>

Resources.id

</td><td>

Sys\_id of the group.Data type: String

</td></tr><tr><td>

Resources.meta

</td><td>

Metadata pertaining to the group.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": String",
  "resourceType": String"
}
```

</td></tr><tr><td>

Resources.meta.created

</td><td>

Date and time when the group record was created.Data type: String

</td></tr><tr><td>

Resources.meta.lastModified

</td><td>

Date and time when the group record was last modified.Data type: String

</td></tr><tr><td>

Resources.meta.location

</td><td>

URI of the group being retrieved.Data type: String

</td></tr><tr><td>

Resources.meta.resourceType

</td><td>

SCIM Groups' resource type.Data type: String

</td></tr><tr><td>

Resources.members

</td><td>

List of the users and groups associated with the group.Data type: Array of Objects

```
"members": [
  {
    "display": "String",
    "value": "String",
    "$ref": "String"
  }
]
```

</td></tr><tr><td>

Resources.members.display

</td><td>

Name of the associated group member.Data type: String

</td></tr><tr><td>

Resources.members.value

</td><td>

Sys\_id of the associated user or group record.Data type: String

</td></tr><tr><td>

Resources.members.$ref

</td><td>

URI of the associated group member.Data type: String

</td></tr><tr><td>

Resources.schemas

</td><td>

List of URIs of the SCIM Group schemas used to process the request.

Supported group schemas:

-   urn:ietf:params:scim:schemas:core:2.0:Group - Core schema specified in the Internet Engineering Task Force System for Cross-domain Identity Management: Core Schema document \([https://datatracker.ietf.org/doc/html/rfc7643\#section-4.2](https://datatracker.ietf.org/doc/html/rfc7643#section-4.2)\)
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group - ServiceNow extension schema. This schema contains attributes that are present in the Groups \[sys\_user\_group\] table in a base ServiceNow system, but are not part of the core schema.
-   urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group” - Custom extension schema. This schema is part of “Group” resourceType in the sys\_scim\_schema\_extension table. If the schema is not active, the schema URN is not returned in the response.

Data type: Array of Strings

</td></tr><tr><td>

schemas

</td><td>

List of URIs of the SCIM List Response schemas used to process the request.Data type: Array

</td></tr><tr><td>

startIndex

</td><td>

One-based index into the Group \[sys\_user\_group\] table at which the endpoint started retrieving records.Data type: Number

</td></tr><tr><td>

totalResults

</td><td id="totalResults-SCIM-entry">

Total number of records that match the request.Data type: Number

</td></tr></tbody>
</table>### cURL request for multiple groups

This example shows how to request multiple groups \(four in this case\), using the **count** parameter.

```
curl "https://instance-sevicenow.com/api/now/scim/Groups?count=4" \
--request GET \
--header "Accept:application/scim+json" \
```

Response:

```
{"schemas":
  ["urn:ietf:params:scim:api:messages:2.0:ListResponse"],
  "totalResults":44,
  "Resources":[
    {"schemas":
      [
        "urn:ietf:params:scim:schemas:core:2.0:Group"",
        “urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group”,
        “urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group”
      ],
      "id":"019ad92ec7230010393d265c95c260dd",
      "meta":{
        "resourceType":"Group",
        "created":"2020-03-17T11:39:14Z",
        "lastModified":"2020-03-17T11:39:14Z",
        "location":"https://instance-sevicenow.com/api/now/scim/Groups/019ad92ec7230010393d265c95c260dd"
      },
      "displayName":"Analytics Settings Managers"
    },
    {"schemas":
      [
        "urn:ietf:params:scim:schemas:core:2.0:Group"",
        “urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group”,
        “urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group”
      ],
      "id":"0a52d3dcd7011200f2d224837e6103f2",
      "meta":{
        "resourceType":"Group",
        "created":"2021-09-29T16:42:02Z",
        "lastModified":"2021-09-29T16:42:02Z",
        "location":"https://instance-sevicenow.com/api/now/scim/Groups/0a52d3dcd7011200f2d224837e6103f2"
      },
      "displayName":"Application Development",
      "members":[
        {
          "value":"dc6053dcd7011200f2d224837e6103e0",
          "display":"John Doe",
          "$ref": "http://instance-sevicenow.com/api/now/scim/Users/dc6053dcd7011200f2d224837e6103e0"
        },
        {
          "value":"443193dcd7011200f2d224837e61037d",
          "display":"Abel Tutor",
          "$ref": "http://instance-sevicenow.com/api/now/scim/Users/443193dcd7011200f2d224837e61037d"
        }
      ],
      "urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group": {
        "company": {
          "value": "81fd65ecac1d55eb42a426568fc87a63",
          "name": "ACME Japan",
          "$ref": "http://instance-sevicenow.com/api/now/scim/Companies/81fd65ecac1d55eb42a426568fc87a63"
        }
      }
    },
    {"schemas":
      [
        "urn:ietf:params:scim:schemas:core:2.0:Group"",
        “urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group”,
        “urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group”
      ],
      "id":"0c4e7b573b331300ad3cc9bb34efc461",
      "meta":{
        "resourceType":"Group",
        "created":"2021-09-29T05:11:33Z",
        "lastModified":"2021-09-29T05:11:33Z",
        "location":"instance-sevicenow.com/api/now/scim/Groups/0c4e7b573b331300ad3cc9bb34efc461"
      },
      "displayName":"Problem Analyzers",
      "members":[
        {
          "value":"d3dbbf173b331300ad3cc9bb34efc466",
          "display":"Problem Manager",
          "$ref": "http://instance-sevicenow.com/api/now/scim/Users/babb4639b76233004fbc2089ee11a97f"
        },
        {
          "value":"38cb3f173b331300ad3cc9bb34efc4d6",
          "display":"Problem Coordinator B",
          "$ref": "http://instance-sevicenow.com/api/now/scim/Users/cbcc4639b76233004fbc2089ee111047"
        },
        {
          "value":"26fbff173b331300ad3cc9bb34efc4bd",
          "display":"Problem Administrator",
          "$ref": "http://instance-sevicenow.com/api/now/scim/Users/45324639b76232189fbc2089ee11bc34"
        }
      ],
      "urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group": {
        "company": {
          "value": "913465ecac1d569b42a426568fc88af3",
          "name": "ACME London",
          "$ref": "http://instance-sevicenow.com/api/now/scim/Companies/913465ecac1d569b42a426568fc88af3"
        }
      }
    },
    {"schemas":
      [
        "urn:ietf:params:scim:schemas:core:2.0:Group"",
        "urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group",
        "urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group"
      ],
      "id":"0c5e2a7ce4001410f877ce457cda6b98",
      "meta":{
        "resourceType":"Group",
        "created":"2020-04-06T03:47:08Z",
        "lastModified":"2020-07-29T04:02:26Z",
        "location":"instance-sevicenow.com/api/now/scim/Groups/0c5e2a7ce4001410f877ce457cda6b98"
      },
      "displayName":"Business Application Registration Approval Group"
    }
  ],
  "startIndex":1,
  "itemsPerPage":4
}
```

### cURL request for multiple groups using excludedAttributes

This example shows how to request multiple groups \(four in this case\), using the **count** parameter and excluding the meta and members fields.

```
curl "https://instance-sevicenow.com/api/now/scim/Groups?excludedAttributes=meta%2C%20members&count=4" \
--request GET \
--header "Accept:application/scim+json" \
```

Response:

```
{"schemas":
  ["urn:ietf:params:scim:api:messages:2.0:ListResponse"],
  "totalResults":44,
  "Resources":[
    {"schemas":
      [
        "urn:ietf:params:scim:schemas:core:2.0:Group"",
        “urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group”,
        “urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group”
      ],
      "id":"019ad92ec7230010393d265c95c260dd",
      "displayName":"Analytics Settings Managers",
      "urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group": {
        "company": {
          "value": "913465ecac1d569b42a426568fc88af3",
          "name": "ACME London",
          "$ref": "http://instance-sevicenow.com/api/now/scim/Companies/913465ecac1d569b42a426568fc88af3"
        }
      }
    },
    {"schemas":
      [
        "urn:ietf:params:scim:schemas:core:2.0:Group"",
        “urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group”,
        “urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group”
      ],
      "id":"0a52d3dcd7011200f2d224837e6103f2",
      "displayName":"Application Development"
    },
    {"schemas":
      [
        "urn:ietf:params:scim:schemas:core:2.0:Group"",
        “urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group”,
        “urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group”
      ],
      "id":"0c4e7b573b331300ad3cc9bb34efc461",
      "displayName":"Problem Analyzers"
    },
    {"schemas":
      [
        "urn:ietf:params:scim:schemas:core:2.0:Group"",
        “urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group”,
        “urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group”
      ],
      "id":"0c5e2a7ce4001410f877ce457cda6b98",
      "displayName":"Business Application Registration Approval Group",
      "urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group": {
        "company": {
          "value": "81fd65ecac1d55eb42a426568fc87a63",
          "name": "ACME Japan",
          "$ref": "http://instance-sevicenow.com/api/now/scim/Companies/81fd65ecac1d55eb42a426568fc87a63"
        }
      }
    }
  ],
  "startIndex":1,
  "itemsPerPage":4
}
```

## SCIM - GET /scim/Groups/\{group\_id\}

Returns the specified group record from the Group \[sys\_user\_group\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Groups/{group_id}`

Default URL: `/api/now/scim/Groups/{group_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

group\_id

</td><td>

Sys\_id of the group record to return.

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td id="status_400-SCIM-entry">

Bad Request. A bad request type or malformed request was detected.-   Ensure that both the **attributes** and **excludedAttributes** query parameters have not been passed in the request.
-   Ensure that the **count** parameter is not greater than 500.
-   Ensure that all **filter** parameters are valid.

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="id_uwk_c5c_grb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="group_company-SCIM-row"><td>

company

</td><td id="group_company-SCIM-entry">

Details about the group's company or organization.Data type: Object

 ```
"company": {
  "display": "String",
  "$ref": "String",
  "value": "String"
}
```

</td></tr><tr id="group_company_display-SCIM-row"><td>

company.display

</td><td id="group_company_display-SCIM-entry">

Name of the company.Data type: String

</td></tr><tr id="group_company_ref-SCIM-row"><td>

company.$ref

</td><td id="group_company_ref-SCIM-entry">

Reference URI of the company.Format: `<host>/Companies/<company sys_id>`, such as: `http://instance-servicenow.com/api/now/scim/Companies/81fd65ecac1d55eb42a426568fc87a63`.

 Data type: String

</td></tr><tr id="group_company_value-SCIM-row"><td>

company.value

</td><td id="group_company_value-SCIM-entry">

Sys\_id of the associated company.Data type: String

</td></tr><tr id="group_displayName-SCIM-row"><td>

displayName

</td><td id="group_displayName-SCIM-entry">

Human-readable name of the group, such as HR Team.Data type: String

</td></tr><tr id="group_externalId-SCIM-row"><td>

externalId

</td><td id="group_externalId-SCIM-entry">

Unique identifier assigned to the group by the entity provisioning it.Data type: String

</td></tr><tr id="group_id-SCIM-row"><td>

id

</td><td id="group_id-SCIM-entry">

Sys\_id of the group.Data type: String

</td></tr><tr id="group_meta-SCIM-row"><td>

meta

</td><td id="group_meta-SCIM-entry">

Metadata pertaining to the group.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": String",
  "resourceType": String"
}
```

</td></tr><tr id="group_meta_created-SCIM-row"><td>

meta.created

</td><td id="group_meta_created-SCIM-entry">

Date and time when the group record was created.Data type: String

</td></tr><tr id="group_meta_lastModified-SCIM-row"><td>

meta.lastModified

</td><td id="group_meta_lastModified-SCIM-entry">

Date and time when the group record was last modified.Data type: String

</td></tr><tr id="group_meta_location-SCIM-row"><td>

meta.location

</td><td id="group_meta_location-SCIM-entry">

URI of the group being retrieved.Data type: String

</td></tr><tr id="group_meta_resourceType-SCIM-row"><td>

meta.resourceType

</td><td id="group_meta_resourceType-SCIM-entry">

SCIM Groups' resource type.Data type: String

</td></tr><tr id="group_members-SCIM-row"><td>

members

</td><td id="group_members-SCIM-entry">

List of the users and groups associated with the group.Data type: Array of Objects

```
"members": [
  {
    "display": "String",
    "value": "String",
    "$ref": "String"
  }
]
```

</td></tr><tr id="group_members_display-SCIM-row"><td>

members.display

</td><td id="group_members_display-SCIM-entry">

Name of the associated group member.Data type: String

</td></tr><tr id="group_members_value-SCIM-row"><td>

members.value

</td><td id="group_members_value-SCIM-entry">

Sys\_id of the associated user or group record.Data type: String

</td></tr><tr id="group_members_ref-SCIM-row"><td>

members.$ref

</td><td id="group_members_ref-SCIM-entry">

URI of the associated group member.Data type: String

</td></tr><tr id="group_schemas-SCIM-row"><td>

schemas

</td><td id="group_schemas-SCIM-entry">

List of URIs of the SCIM Group schemas used to process the request.

Supported group schemas:

-   urn:ietf:params:scim:schemas:core:2.0:Group - Core schema specified in the Internet Engineering Task Force System for Cross-domain Identity Management: Core Schema document \([https://datatracker.ietf.org/doc/html/rfc7643\#section-4.2](https://datatracker.ietf.org/doc/html/rfc7643#section-4.2)\)
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group - ServiceNow extension schema. This schema contains attributes that are present in the Groups \[sys\_user\_group\] table in a base ServiceNow system, but are not part of the core schema.
-   urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group” - Custom extension schema. This schema is part of “Group” resourceType in the sys\_scim\_schema\_extension table. If the schema is not active, the schema URN is not returned in the response.

Data type: Array of Strings

</td></tr></tbody>
</table>### cURL request for specific group

This example shows how to retrieve a specific group record.

```
curl "https://instance-servicenow.com/api/now/scim/Groups/e0140d671bbe3010593876a61a4bcb11" \
--request GET \
--header "Accept:application/scim+json" \
```

Response:

```
{"schemas":
  [
    "urn:ietf:params:scim:schemas:core:2.0:Group",
    "urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group",
    "urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group"
  ],
  "id":"e0140d671bbe3010593876a61a4bcb11",
  "externalId":"8ae5dc9e-c7ad-4d3d-a152-35a6b6222b83",
  "meta":{
    "resourceType":"Group",
    "created":"2021-09-30T18:20:43Z",
    "lastModified":"2021-09-30T18:20:43Z",
    "location":"https://instance-servicenow.com/api/now/scim/Groups/e0140d671bbe3010593876a61a4bcb11"},
    "displayName":"HR Group",
    "members":[
      {
        "value":"62826bf03710200044e0bfc8bcbe5df1",
        "display":"Abel Tuter",
        "$ref": "http://instance-servicenow.com/api/now/scim/Users/62826bf03710200044e0bfc8bcbe5df1"
      }
    ], 
    "urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group": {
      "company": {
        "value": "81fd65ecac1d55eb42a426568fc87a63",
        "name": "ACME Japan",
        "$ref": "http://111.111.1.11:8080/api/now/scim/Companies/81fd65ecac1d55eb42a426568fc87a63"
      }
    }
  }
}
```

## SCIM - PATCH /scim/Groups/\{group\_id\}

Enables you to add, update, and delete specified fields in a group record in the Group \[sys\_user\_group\] table of a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

For additional information, refer to the [Modifying with PATCH](https://datatracker.ietf.org/doc/html/rfc7644#section-3.5.2) section of RFC 7644.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Groups/{group_id}`

Default URL: `/api/now/scim/Groups/{group_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

group\_id

</td><td>

Sys\_id of the group record to update.

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Operations

</td><td>

Required. List of operation objects to patch the specified Group record with.Data type: Array of Objects

 ```
"Operations": [
  {
    "op": "String",
    "path": "String",
    "value": Any
  }
]
```

</td></tr><tr><td>

Operations.op

</td><td>

Required. Operation to perform.Valid values:

-   add: Add the specified field and value to the Group record.
-   remove: Remove the value from the specified field. Replaced with data type "null".
-   replace: Replace the value of the specified field.

 Data type: String

</td></tr><tr><td>

Operations.path

</td><td>

Required for `remove` operations, optional for others. Name/path of the field to modify.The **path** parameter can have one of the following formats:

-   A direct field, such as `displayName`
-   In case of complex array, a pointer to a specific element with a filter, such as: `emails[type eq "work"]`

```
{
  "schemas": [
    "urn:ietf:params:scim:api:messages:2.0:PatchOp"
  ],
  "Operations": [
    {
      "op": "add",
      "path": "displayName",
      "value": "HR Group"
    },
    {
      "op": "replace", 
      "path": "members[value eq \"sysid1\"]", 
      "value": {
        "value": "sysid2"
      }
    } 
  ]
}
```

 Data type: String

 Default: Considers the field to be a resource.

</td></tr><tr><td>

Operations.value

</td><td>

Value of the field specified in the **Operations.path** parameter. The format of this parameter depends on the data-type of the associated field. For example, if updating a simple string, such as the title, the **value** field is expressed as a string.

 ```
 "Operations": [
  {
    "op": "add",
    "path": "displayName",
    "value": "HR Group"
  }
]
```

 You can also declare simple string values without a **path** parameters, such as:

```
 "Operations": [
  {
    "op": "add",
    "value": {
      "displayName": "HR Group"
    }
  }
]
```

 The following shows how to add a member to the group:

```
{
  "op": "add",
  "value": {
    "members": {
      "value": "62826bf03710200044e0bfc8bcbe5df1",
    }
  }
}
```

 If the field being updated is not in the base-schema, you must enclose the name-value pair in an object that specifies the URN of the associated schema.

 ```
"value": {
  "<schema_urn>": {
    "<field_name>": "<new_value>"
  },
}
```

 For example:

 ```
"value": {
  "urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group": {
    "groupNumber": "13454"
  },
}
```

Data type: Any

</td></tr><tr><td>

Operations.value.type

</td><td>

Name of the field to update.Data type: String

</td></tr><tr><td>

Operations.value.value

</td><td>

Value to update the field with. Data type: String

</td></tr><tr><td>

schemas

</td><td id="group_schemas-SCIM-entry">

Required. SCIM Schema URI of the Patch Operation: "urn:ietf:params:scim:api:messages:2.0:PatchOp”Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="Content_Type-SCIM-entry">

Data format of the request body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

204

</td><td>

`Successful. No Content (Applicable only for SCIM Group Patch API)` - This 204 status is dependent on the state of the SCIM UI property, `Enable Group Patch API response with No Content`, and is subject to the attribute parameter passed as per RFC: [https://www.rfc-editor.org/rfc/rfc7644\#page-35](https://www.rfc-editor.org/rfc/rfc7644#page-35).

 Default property value: false

 The `Enable Group Patch API response with No Content` property can be used to get additional response execution performance gains if the client does not plan to consume any response resources.

</td></tr><tr><td>

400

</td><td>

Bad Request. A bad request type or malformed request was detected.-   Check for invalid values:
    -   Malformed request body.
    -   Required field is not provided or empty.
    -   Invalid user or group sys\_id is provided.
-   Check if a read-only or immutable field is trying to be modified.
-   Ensure that both the **attributes** and **excludedAttributes** query parameters have not been passed in the request or that the request does not exceed the maximum number of members.

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr><tr><td>

409

</td><td>

Group already exists. The **displayName** parameter must be unique.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

company

</td><td id="group_company-SCIM-entry">

Details about the group's company or organization.Data type: Object

 ```
"company": {
  "display": "String",
  "$ref": "String",
  "value": "String"
}
```

</td></tr><tr><td>

company.display

</td><td id="group_company_display-SCIM-entry">

Name of the company.Data type: String

</td></tr><tr><td>

company.$ref

</td><td id="group_company_ref-SCIM-entry">

Reference URI of the company.Format: `<host>/Companies/<company sys_id>`, such as: `http://instance-servicenow.com/api/now/scim/Companies/81fd65ecac1d55eb42a426568fc87a63`.

 Data type: String

</td></tr><tr><td>

company.value

</td><td id="group_company_value-SCIM-entry">

Sys\_id of the associated company.Data type: String

</td></tr><tr><td>

displayName

</td><td id="group_displayName-SCIM-entry">

Human-readable name of the group, such as HR Team.Data type: String

</td></tr><tr><td>

externalId

</td><td id="group_externalId-SCIM-entry">

Unique identifier assigned to the group by the entity provisioning it.Data type: String

</td></tr><tr><td>

errors

</td><td id="errors-SCIM-entry">

Response that describes any errors that may have occurred during processing the request.Data type: Object

 ```
"errors": {
  "details": "String",
  "schemas": "String",
  "scimType": "String",
  "status": "String"
}
```

</td></tr><tr><td>

errors.detail

</td><td id="errors_details-SCIM-entry">

Detailed error message on why the request failed.Data type: String

</td></tr><tr><td>

errors.scimType

</td><td id="errors_scimType-SCIM-entry">

SCIM error detail keyword.Data type: String

</td></tr><tr><td>

errors.schemas

</td><td id="errors_schemas-SCIM-entry">

URI of the SCIM Schemas used to process the error response.Data type: Array of Strings

</td></tr><tr><td>

errors.status

</td><td id="errors_status-SCIM-entry">

HTTP status code for the error response.Data type: String

</td></tr><tr><td>

displayName

</td><td id="d3411e890">

Human-readable name of the group, such as HR Team.Data type: String

</td></tr><tr><td>

externalId

</td><td id="d3411e902">

Unique identifier assigned to the group by the entity provisioning it.Data type: String

</td></tr><tr><td>

id

</td><td id="group_id-SCIM-entry">

Sys\_id of the group.Data type: String

</td></tr><tr><td>

members

</td><td id="group_members-SCIM-entry">

List of the users and groups associated with the group.Data type: Array of Objects

```
"members": [
  {
    "display": "String",
    "value": "String",
    "$ref": "String"
  }
]
```

</td></tr><tr><td>

members.display

</td><td id="group_members_display-SCIM-entry">

Name of the associated group member.Data type: String

</td></tr><tr><td>

members.value

</td><td id="group_members_value-SCIM-entry">

Sys\_id of the associated user or group record.Data type: String

</td></tr><tr><td>

members.$ref

</td><td id="group_members_ref-SCIM-entry">

URI of the associated group member.Data type: String

</td></tr><tr><td>

meta

</td><td id="group_meta-SCIM-entry">

Metadata pertaining to the group.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": String",
  "resourceType": String"
}
```

</td></tr><tr><td>

meta.created

</td><td id="group_meta_created-SCIM-entry">

Date and time when the group record was created.Data type: String

</td></tr><tr><td>

meta.lastModified

</td><td id="group_meta_lastModified-SCIM-entry">

Date and time when the group record was last modified.Data type: String

</td></tr><tr><td>

meta.location

</td><td id="group_meta_location-SCIM-entry">

URI of the group being retrieved.Data type: String

</td></tr><tr><td>

meta.resourceType

</td><td id="group_meta_resourceType-SCIM-entry">

SCIM Groups' resource type.Data type: String

</td></tr><tr><td>

schemas

</td><td id="d3411e1029">

List of URIs of the SCIM Group schemas used to process the request.

Supported group schemas:

-   urn:ietf:params:scim:schemas:core:2.0:Group - Core schema specified in the Internet Engineering Task Force System for Cross-domain Identity Management: Core Schema document \([https://datatracker.ietf.org/doc/html/rfc7643\#section-4.2](https://datatracker.ietf.org/doc/html/rfc7643#section-4.2)\)
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group - ServiceNow extension schema. This schema contains attributes that are present in the Groups \[sys\_user\_group\] table in a base ServiceNow system, but are not part of the core schema.
-   urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group” - Custom extension schema. This schema is part of “Group” resourceType in the sys\_scim\_schema\_extension table. If the schema is not active, the schema URN is not returned in the response.

Data type: Array of Strings

</td></tr></tbody>
</table>### cURL request

This example shows how to add an external ID to a group record and replace the current list of associated members \(users\).

```
curl "https://instance-servicenow.com/api/now/scim/Groups/a92b84f96b073010638c83eece44af4e" \
--request PATCH \
--header "Accept:application/scim+json" \
--header "Content-Type:application/scim+json" \
--data "{
  "schemas": [
    "urn:ietf:params:scim:api:messages:2.0:PatchOp"
  ],
  "Operations": [
    {
      "op": "add",
      "path": "externalId",
      "value": "278fdc2e-a6aa-4140-bd23-9ba4987a2938"
    },
    {
      "op": "replace",
      "path": "members",
      "value": [
        {
          "value": "62826bf03710200044e0bfc8bcbe5df1"
        },
        {
          "value": "a8f98bb0eb32010045e1a5115206fe3a"
        }
      ]
    }
  ]
}"
```

Response:

```
{
  "schemas": [
    "urn:ietf:params:scim:schemas:core:2.0:Group",
    "urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group",
    'urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group'
  ],
  "id": "a92b84f96b073010638c83eece44af4e",
  "externalId": "278fdc2e-a6aa-4140-bd23-9ba4987a2938",
  "meta": {
    "resourceType": "Group",
    "created": "2021-10-07T13:58:22Z",
    "lastModified": "2021-10-07T15:48:44Z",
    "location":
      "https://instance-sevicenow/api/now/scim/Groups/a92b84f96b073010638c83eece44af4e"
  },
  "displayName": "HR Team",
  "members": [
    {
      "value": "62826bf03710200044e0bfc8bcbe5df1",
      "display": "Abel Tuter",
      "$ref":
        "https://instance-sevicenow/api/now/scim/Users/62826bf03710200044e0bfc8bcbe5df1"
    },
    {
      "value": "a8f98bb0eb32010045e1a5115206fe3a",
      "display": "Abraham Lincoln",
      "$ref":
        "https://instance-sevicenow/api/now/scim/Users/a8f98bb0eb32010045e1a5115206fe3a"
    }
  ],
  "urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group": {
    "company": {
      "value": "81fd65ecac1d55eb42a426568fc87a63",
      "name": "ACME Japan",
      "$ref": "http://instance-sevicenow/api/now/scim/Companies/81fd65ecac1d55eb42a426568fc87a63"
    }
  }
}
```

## SCIM - POST /scim/Groups

Creates a group record in the Group \[sys\_user\_group\] table of a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

You can define the display name of the group, an external ID used to correlate this group to an external system, and add members \(users/groups\) to the group.

**Note:** The search and bulk modifications functionality as noted in the RFC7643 specification are not supported by this endpoint.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Groups`

Default URL: `/api/now/scim/Groups`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

company

</td><td id="group_company-SCIM-entry">

Details about the group's company or organization.Data type: Object

 ```
"company": {
  "display": "String",
  "$ref": "String",
  "value": "String"
}
```

</td></tr><tr><td>

company.display

</td><td id="group_company_display-SCIM-entry">

Name of the company.Data type: String

</td></tr><tr><td>

company.$ref

</td><td id="group_company_ref-SCIM-entry">

Reference URI of the company.Format: `<host>/Companies/<company sys_id>`, such as: `http://instance-servicenow.com/api/now/scim/Companies/81fd65ecac1d55eb42a426568fc87a63`.

 Data type: String

</td></tr><tr><td>

company.value

</td><td id="group_company_value-SCIM-entry">

Sys\_id of the associated company.Data type: String

</td></tr><tr><td>

displayName

</td><td id="group_request_displayName-SCIM-entry">

Required. Human-readable name of the group, such as HR Team.Data type: String

</td></tr><tr><td>

externalId

</td><td id="group_externalId-SCIM-entry">

Unique identifier assigned to the group by the entity provisioning it.Data type: String

</td></tr><tr><td>

members

</td><td>

List of users or other groups to associate with the group.Data type: Array of Objects

 ```
"members:" [
  {
    "value": "String"
  }
]
```

 Maximum size: 100 - You can modify this maximum size by updating the system property com.snc.interation.scim2.max.member.count.

</td></tr><tr><td>

members.value

</td><td>

Sys\_id of the associated user or group record.Data type: String

</td></tr><tr><td>

schemas

</td><td id="group_request_schema-SCIM-entry">

Required.List of URIs of the SCIM Group schemas used to process the request.

Supported group schemas:

-   urn:ietf:params:scim:schemas:core:2.0:Group - Core schema specified in the Internet Engineering Task Force System for Cross-domain Identity Management: Core Schema document \([https://datatracker.ietf.org/doc/html/rfc7643\#section-4.2](https://datatracker.ietf.org/doc/html/rfc7643#section-4.2)\)
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group - ServiceNow extension schema. This schema contains attributes that are present in the Groups \[sys\_user\_group\] table in a base ServiceNow system, but are not part of the core schema.
-   urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group” - Custom extension schema. This schema is part of “Group” resourceType in the sys\_scim\_schema\_extension table. If the schema is not active, the schema URN is not returned in the response.

Data type: Array of Strings

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="Content_Type-SCIM-entry">

Data format of the request body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. A bad request type or malformed request was detected.-   Check for invalid values:
    -   Malformed request body.
    -   Required field is not provided or empty.
    -   Invalid user or group sys\_id is provided.
-   Check if a read-only or immutable field is trying to be modified.
-   Ensure that both the **attributes** and **excludedAttributes** query parameters have not been passed in the request or that the request does not exceed the maximum number of members.

</td></tr><tr><td>

409

</td><td id="status_409-SCIM-entry">

Group already exists. The **displayName** parameter must be unique.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="id_uwk_c5c_grb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="group_company-SCIM-row"><td>

company

</td><td id="d3411e834">

Details about the group's company or organization.Data type: Object

 ```
"company": {
  "display": "String",
  "$ref": "String",
  "value": "String"
}
```

</td></tr><tr id="group_company_display-SCIM-row"><td>

company.display

</td><td id="d3411e848">

Name of the company.Data type: String

</td></tr><tr id="group_company_ref-SCIM-row"><td>

company.$ref

</td><td id="d3411e859">

Reference URI of the company.Format: `<host>/Companies/<company sys_id>`, such as: `http://instance-servicenow.com/api/now/scim/Companies/81fd65ecac1d55eb42a426568fc87a63`.

 Data type: String

</td></tr><tr id="group_company_value-SCIM-row"><td>

company.value

</td><td id="d3411e879">

Sys\_id of the associated company.Data type: String

</td></tr><tr id="group_displayName-SCIM-row"><td>

displayName

</td><td id="group_displayName-SCIM-entry">

Human-readable name of the group, such as HR Team.Data type: String

</td></tr><tr id="group_externalId-SCIM-row"><td>

externalId

</td><td id="d3411e902">

Unique identifier assigned to the group by the entity provisioning it.Data type: String

</td></tr><tr id="group_id-SCIM-row"><td>

id

</td><td id="group_id-SCIM-entry">

Sys\_id of the group.Data type: String

</td></tr><tr id="group_meta-SCIM-row"><td>

meta

</td><td id="group_meta-SCIM-entry">

Metadata pertaining to the group.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": String",
  "resourceType": String"
}
```

</td></tr><tr id="group_meta_created-SCIM-row"><td>

meta.created

</td><td id="group_meta_created-SCIM-entry">

Date and time when the group record was created.Data type: String

</td></tr><tr id="group_meta_lastModified-SCIM-row"><td>

meta.lastModified

</td><td id="group_meta_lastModified-SCIM-entry">

Date and time when the group record was last modified.Data type: String

</td></tr><tr id="group_meta_location-SCIM-row"><td>

meta.location

</td><td id="group_meta_location-SCIM-entry">

URI of the group being retrieved.Data type: String

</td></tr><tr id="group_meta_resourceType-SCIM-row"><td>

meta.resourceType

</td><td id="group_meta_resourceType-SCIM-entry">

SCIM Groups' resource type.Data type: String

</td></tr><tr id="group_members-SCIM-row"><td>

members

</td><td id="group_members-SCIM-entry">

List of the users and groups associated with the group.Data type: Array of Objects

```
"members": [
  {
    "display": "String",
    "value": "String",
    "$ref": "String"
  }
]
```

</td></tr><tr id="group_members_display-SCIM-row"><td>

members.display

</td><td id="group_members_display-SCIM-entry">

Name of the associated group member.Data type: String

</td></tr><tr id="group_members_value-SCIM-row"><td>

members.value

</td><td id="group_members_value-SCIM-entry">

Sys\_id of the associated user or group record.Data type: String

</td></tr><tr id="group_members_ref-SCIM-row"><td>

members.$ref

</td><td id="group_members_ref-SCIM-entry">

URI of the associated group member.Data type: String

</td></tr><tr id="group_schemas-SCIM-row"><td>

schemas

</td><td id="group_schemas-SCIM-entry">

List of URIs of the SCIM Group schemas used to process the request.

Supported group schemas:

-   urn:ietf:params:scim:schemas:core:2.0:Group - Core schema specified in the Internet Engineering Task Force System for Cross-domain Identity Management: Core Schema document \([https://datatracker.ietf.org/doc/html/rfc7643\#section-4.2](https://datatracker.ietf.org/doc/html/rfc7643#section-4.2)\)
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group - ServiceNow extension schema. This schema contains attributes that are present in the Groups \[sys\_user\_group\] table in a base ServiceNow system, but are not part of the core schema.
-   urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group” - Custom extension schema. This schema is part of “Group” resourceType in the sys\_scim\_schema\_extension table. If the schema is not active, the schema URN is not returned in the response.

Data type: Array of Strings

</td></tr></tbody>
</table>### cURL request POST a new group and add member

This example creates group51 and adds the user Abel Tutor as a member.

```
curl "https://instance-servicenow.com/api/now/scim/Groups" \
--request POST \
--header "Accept:application/scim+json" \
--header "Content-Type:application/scim+json" \
--data "{
  \"schemas\": ["urn:ietf:params:scim:schemas:core:2.0:Group",
    “urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group”, 
    “urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group”],
  \"displayName\": \"HR Team\",
  \"externalId\": \"8ae5dc9e-c7ad-4d3d-a152-35a6b6222b83\",
  \"members\": [
    {
      \"value\": \"62826bf03710200044e0bfc8bcbe5df1\",
      \"$ref\": \"Users/62826bf03710200044e0bfc8bcbe5df1\"
    }
  ]
}"
```

Response:

```
{"schemas":
  [
    "urn:ietf:params:scim:schemas:core:2.0:Group",
    "urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group",
    'urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group'
  ],
  "id":"e0140d671bbe3010593876a61a4bcb11",
  "externalId":"8ae5dc9e-c7ad-4d3d-a152-35a6b6222b83",
  "meta":{
    "resourceType":"Group",
    "created":"2021-09-30T18:20:43Z",
    "lastModified":"2021-09-30T18:20:43Z",
    "location":"https://instance-servicenow.com/api/now/scim/Groups/e0140d671bbe3010593876a61a4bcb11"},
    "displayName":"HR Team",
    "members":[
      {
        "value":"62826bf03710200044e0bfc8bcbe5df1",
        "display":"Abel Tuter",
        "$ref": "http://instance-servicenow.com/api/now/scim/Users/62826bf03710200044e0bfc8bcbe5df1"
      }
    ],
    "urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group": {
      "company": {
        "value": "81fd65ecac1d55eb42a426568fc87a63",
        "name": "ACME Japan",
        "$ref": http://instance-servicenow.com/api/now/scim/Companies/81fd65ecac1d55eb42a426568fc87a63
      }
    }
  }
}
```

## SCIM - PUT /scim/Groups/\{group\_id\}

Updates the specified group record in the Group \[sys\_user\_group\] table of a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

Fields that are omitted in the request are not updated. You can explicitly clear a field by setting its value to null for a single valued field and to an empty array for array type fields such as **members**.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Groups/{group_id}`

Default URL: `/api/now/scim/Groups/{group_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

group\_id

</td><td>

Sys\_id of the group record to update.

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

company

</td><td id="group_company-SCIM-entry">

Details about the group's company or organization.Data type: Object

 ```
"company": {
  "display": "String",
  "$ref": "String",
  "value": "String"
}
```

</td></tr><tr><td>

company.display

</td><td id="group_company_display-SCIM-entry">

Name of the company.Data type: String

</td></tr><tr><td>

company.$ref

</td><td id="group_company_ref-SCIM-entry">

Reference URI of the company.Format: `<host>/Companies/<company sys_id>`, such as: `http://instance-servicenow.com/api/now/scim/Companies/81fd65ecac1d55eb42a426568fc87a63`.

 Data type: String

</td></tr><tr><td>

company.value

</td><td id="group_company_value-SCIM-entry">

Sys\_id of the associated company.Data type: String

</td></tr><tr><td>

displayName

</td><td id="group_displayName-SCIM-entry">

Human-readable name of the group, such as HR Team.Data type: String

</td></tr><tr><td>

externalId

</td><td id="group_externalId-SCIM-entry">

Unique identifier assigned to the group by the entity provisioning it.Data type: String

</td></tr><tr><td>

members

</td><td>

List of users to replace the current list of members with.Data type: Array of Objects

 ```
"members:" [
  {
    "value": "String"
  }
]
```

 Maximum size: 100 - You can modify this maximum size by updating the system property com.snc.interation.scim2.max.member.count.

</td></tr><tr><td>

members.value

</td><td>

Sys\_id of the associated user or group record.Data type: String

</td></tr><tr><td>

schemas

</td><td id="group_request_schema-SCIM-entry">

Required.List of URIs of the SCIM Group schemas used to process the request.

Supported group schemas:

-   urn:ietf:params:scim:schemas:core:2.0:Group - Core schema specified in the Internet Engineering Task Force System for Cross-domain Identity Management: Core Schema document \([https://datatracker.ietf.org/doc/html/rfc7643\#section-4.2](https://datatracker.ietf.org/doc/html/rfc7643#section-4.2)\)
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group - ServiceNow extension schema. This schema contains attributes that are present in the Groups \[sys\_user\_group\] table in a base ServiceNow system, but are not part of the core schema.
-   urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group” - Custom extension schema. This schema is part of “Group” resourceType in the sys\_scim\_schema\_extension table. If the schema is not active, the schema URN is not returned in the response.

Data type: Array of Strings

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="Content_Type-SCIM-entry">

Data format of the request body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. A bad request type or malformed request was detected.-   Check for invalid values:
    -   Malformed request body.
    -   Required field is not provided or empty.
    -   Invalid user or group sys\_id is provided.
-   Check if a read-only or immutable field is trying to be modified.
-   Ensure that both the **attributes** and **excludedAttributes** query parameters have not been passed in the request or that the request does not exceed the maximum number of members.

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr><tr><td>

409

</td><td id="status_409-SCIM-entry">

Group already exists. The **displayName** parameter must be unique.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

company

</td><td id="d3411e834">

Details about the group's company or organization.Data type: Object

 ```
"company": {
  "display": "String",
  "$ref": "String",
  "value": "String"
}
```

</td></tr><tr><td>

company.display

</td><td id="d3411e848">

Name of the company.Data type: String

</td></tr><tr><td>

company.$ref

</td><td id="d3411e859">

Reference URI of the company.Format: `<host>/Companies/<company sys_id>`, such as: `http://instance-servicenow.com/api/now/scim/Companies/81fd65ecac1d55eb42a426568fc87a63`.

 Data type: String

</td></tr><tr><td>

company.value

</td><td id="d3411e879">

Sys\_id of the associated company.Data type: String

</td></tr><tr><td>

displayName

</td><td id="d3411e890">

Human-readable name of the group, such as HR Team.Data type: String

</td></tr><tr><td>

errors

</td><td id="errors-SCIM-entry">

Response that describes any errors that may have occurred during processing the request.Data type: Object

 ```
"errors": {
  "details": "String",
  "schemas": "String",
  "scimType": "String",
  "status": "String"
}
```

</td></tr><tr><td>

errors.detail

</td><td id="errors_details-SCIM-entry">

Detailed error message on why the request failed.Data type: String

</td></tr><tr><td>

errors.scimType

</td><td id="errors_scimType-SCIM-entry">

SCIM error detail keyword.Data type: String

</td></tr><tr><td>

errors.schemas

</td><td id="errors_schemas-SCIM-entry">

URI of the SCIM Schemas used to process the error response.Data type: Array of Strings

</td></tr><tr><td>

errors.status

</td><td id="errors_status-SCIM-entry">

HTTP status code for the error response.Data type: String

</td></tr><tr><td>

externalId

</td><td id="d3411e902">

Unique identifier assigned to the group by the entity provisioning it.Data type: String

</td></tr><tr><td>

id

</td><td id="group_id-SCIM-entry">

Sys\_id of the group.Data type: String

</td></tr><tr><td>

members

</td><td id="group_members-SCIM-entry">

List of the users and groups associated with the group.Data type: Array of Objects

```
"members": [
  {
    "display": "String",
    "value": "String",
    "$ref": "String"
  }
]
```

</td></tr><tr><td>

members.display

</td><td id="group_members_display-SCIM-entry">

Name of the associated group member.Data type: String

</td></tr><tr><td>

members.value

</td><td id="group_members_value-SCIM-entry">

Sys\_id of the associated user or group record.Data type: String

</td></tr><tr><td>

members.$ref

</td><td id="group_members_ref-SCIM-entry">

URI of the associated group member.Data type: String

</td></tr><tr><td>

meta

</td><td id="group_meta-SCIM-entry">

Metadata pertaining to the group.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": String",
  "resourceType": String"
}
```

</td></tr><tr><td>

meta.created

</td><td id="group_meta_created-SCIM-entry">

Date and time when the group record was created.Data type: String

</td></tr><tr><td>

meta.lastModified

</td><td id="group_meta_lastModified-SCIM-entry">

Date and time when the group record was last modified.Data type: String

</td></tr><tr><td>

meta.location

</td><td id="group_meta_location-SCIM-entry">

URI of the group being retrieved.Data type: String

</td></tr><tr><td>

meta.resourceType

</td><td id="group_meta_resourceType-SCIM-entry">

SCIM Groups' resource type.Data type: String

</td></tr><tr><td>

schemas

</td><td id="group_schemas-SCIM-entry">

List of URIs of the SCIM Group schemas used to process the request.

Supported group schemas:

-   urn:ietf:params:scim:schemas:core:2.0:Group - Core schema specified in the Internet Engineering Task Force System for Cross-domain Identity Management: Core Schema document \([https://datatracker.ietf.org/doc/html/rfc7643\#section-4.2](https://datatracker.ietf.org/doc/html/rfc7643#section-4.2)\)
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group - ServiceNow extension schema. This schema contains attributes that are present in the Groups \[sys\_user\_group\] table in a base ServiceNow system, but are not part of the core schema.
-   urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group” - Custom extension schema. This schema is part of “Group” resourceType in the sys\_scim\_schema\_extension table. If the schema is not active, the schema URN is not returned in the response.

Data type: Array of Strings

</td></tr></tbody>
</table>### cURL request updating group members using PUT

The following example changes the member associated with the group to Abraham Lincoln instead of Abel Tutor and changes the name of the group to HR Team.

```
curl "https://instance-servicenow.com/api/now/scim/Groups/e0140d671bbe3010593876a61a4bcb11" \
--request PUT \
--header "Accept:application/scim+json" \
--header "Content-Type:application/scim+json" \
--data "{
  \"schemas\": ["urn:ietf:params:scim:schemas:core:2.0:Group",
    “urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group”, 
    “urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group”],
  \"displayName\": \"HR Team\",
  \"externalId\": \"8ae5dc9e-c7ad-4d3d-a152-35a6b6222b83\",
  \"members\": [
    {
      \"value\": \"a8f98bb0eb32010045e1a5115206fe3a\",
      \"$ref\": \"Users\"
    }
  ]
}" 
```

Response:

```
{"schemas":
  [
    "urn:ietf:params:scim:schemas:core:2.0:Group",
    "urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group",
    'urn:ietf:params:scim:schemas:extension:servicenow:custom:2.0:Group'
  ],
  "id":"e0140d671bbe3010593876a61a4bcb11",
  "externalId":"8ae5dc9e-c7ad-4d3d-a152-35a6b6222b83",
  "meta":{
    "resourceType":"Group",
    "created":"2021-09-30T18:20:43Z",
    "lastModified":"2021-09-30T21:19:40Z",
    "location":"https://instance-servicenow.com/api/now/scim/Groups/e0140d671bbe3010593876a61a4bcb11"
  },
  "displayName":"HR Team",
  "members":[
    {
      "value":"a8f98bb0eb32010045e1a5115206fe3a",
      "display":"Abraham Lincoln",
      "$ref": "http://instance-servicenow.com/api/now/scim/Users/62826bf03710200044e0bfc8bcbe5df1"
    }
  ],
  "urn:ietf:params:scim:schemas:extension:servicenow:2.0:Group": {
    "company": {
      "value": "81fd65ecac1d55eb42a426568fc87a63",
      "name": "ACME Japan",
      "$ref": "http://192.168.1.25:8080/api/now/scim/Companies/81fd65ecac1d55eb42a426568fc87a63"
    }
  }
}
```

## SCIM - DELETE /scim/Users/\{user\_id\}

Deletes the specified user record from the User \[sys\_user\] table of a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Users/{user_id}`

Default URL: `/api/now/scim/Users/{user_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

user\_id

</td><td>

Sys\_id of the user record to delete.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|204|No Content. The request was successfully processed.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

errors

</td><td id="errors-SCIM-entry">

Response that describes any errors that may have occurred during processing the request.Data type: Object

 ```
"errors": {
  "details": "String",
  "schemas": "String",
  "scimType": "String",
  "status": "String"
}
```

</td></tr><tr><td>

errors.detail

</td><td id="errors_details-SCIM-entry">

Detailed error message on why the request failed.Data type: String

</td></tr><tr><td>

errors.scimType

</td><td id="errors_scimType-SCIM-entry">

SCIM error detail keyword.Data type: String

</td></tr><tr><td>

errors.schemas

</td><td id="errors_schemas-SCIM-entry">

URI of the SCIM Schemas used to process the error response.Data type: Array of Strings

</td></tr><tr><td>

errors.status

</td><td id="errors_status-SCIM-entry">

HTTP status code for the error response.Data type: String

</td></tr></tbody>
</table>### cURL request

This example shows how to delete a user record from the User \[sys\_user\] table.

```
curl "https://instance-servicenow.com/api/now/scim/Users/b7c5015f778330102e8cc5179e5a9992" \
--request DELETE \
--header "Accept:application/scim+json"  \
```

## SCIM - GET /scim/Users

Returns one or more user records from the User \[sys\_user\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

**Note:** A query that does not return any matches returns success \(HTTP status code 200\) with **totalResults** set to 0.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Users`

Default URL: `/api/now/scim/Users`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

count

</td><td id="count-SCIM-entry">

Number of records to return. A negative value is interpreted as zero.Data type: Number

 Maximum: 500 - A value greater than this results in a bad request error.

 Default: 10

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr><tr><td>

filter

</td><td id="user_filter-SCIM-entry">

Filter expression to apply to the return results. Field filters are expressed as `<field_name> <operator> <"value">`. Refer to [RFC7644](https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2) for a list of the valid operators. **Note:** The `NOT` operator is not supported.

 For example, to filter for all users whose name starts with "Jo", enter `userName SW "jo"` \(case-insensitive\).

 To specify more than one field filter, concatenate the filters using the `AND` operand. For example, to filter for all users whose name starts with "Jo" and whose last name contains "smi", enter `userName SW "john" AND name.familyName CO "smi"`. Use dot-walking to specify nested attributes.

 Only the following SCIM user fields are available for use in filters and some, as noted, only support fixed format:

-   active
-   addresses - Fixed format only, such as:
    -   \[type eq "home" and streetAddress eq "xxxx"\]
    -   \[type eq "home" and locality eq "xxxx"\]
    -   \[type eq "home" and region eq "xxxx"\]
    -   \[type eq "home" and postalCode eq "xxxx"\]
    -   \[type eq "home" and country eq "xxxx"\]
-   displayName
-   emails - Fixed format only, such as: \[type eq "work" and value eq "emailValue"\]
-   externalId - Only `EQ` operator is supported.
-   id
-   meta.created
-   meta.lastModified
-   name.familyName
-   name.givenName
-   name.middleName
-   preferredLanguage
-   phoneNumbers - Fixed format only, such as:
    -   \[type eq “work” and value eq “xxxx”\]
    -   \[type eq “mobile” and value eq “xxxx”\]
    -   \[type eq “home” and value eq “xxxx”\]
-   timezone
-   title
-   userName
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:User:employeeNumber
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:User:gender
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:User:department.name
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:User:department.value
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:User:manager.displayName
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:User:manager.value
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:User:costCenter.name
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:User:costCenter.value
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:User:company.name
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:User:company.value
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:User:location.name
-   urn:ietf:params:scim:schemas:extension:servicenow:2.0:User:location.value

 Data type: String

 Default: No filtering

</td></tr><tr><td>

sortBy

</td><td id="user_sortBy-SCIM-entry">

Must be specified with the **sortOrder** parameter. Field by which to sort the return results. Sorting is case-insensitive. You can only use the parameters available for filtering for the **sortBy** parameter, with the exception of **externalId**, which is not allowed.

 Also, only the following dot-walked parameters are supported:

-   **addressess** - Only the following values are allowed:
    -   **addresses.streetAddress** - Maps to home street address.
    -   **addresses.home.streetAddress**
    -   **addresses.locality** - Maps to home locality.
    -   **addresses.home.locality**
    -   **addresses.region** - Maps to home region.
    -   **addresses.home.region**
    -   **addresses.postalCode** - Maps to home postal code.
    -   **addresses.home.postalCode**
    -   **addresses.country** - Maps to home country.
    -   **addresses.home.country**
-   **emails** - Only the following values are allowed:
    -   **emails.value** - Maps to the email type work.
    -   **emails.work.value**
-   **phoneNumbers** - Only the following values are allowed:
    -   **phoneNumbers.value** - Maps to the phone number type work.
    -   **phoneNumbers.home.value**
    -   **phoneNumbers.mobile.value**
    -   **phoneNumbers.work.value**

 For values that are null:

-   sorted by ascending - Null values are sorted to the top.
-   sorted by descending - Null values are sorted to the bottom.

 Data type: String

 Default: No sort performed

</td></tr><tr><td>

sortOrder

</td><td id="sortOrder-SCIM-entry">

Must be specified with the **sortBy** parameter. Order in which the **sortBy** parameter is applied to the return results. Valid values:

-   ascending
-   descending

 Data type: String

 Default: ascending

</td></tr><tr><td>

startIndex

</td><td id="user_startIndex-SCIM-entry">

One-based index into the User \[sys\_user\] table at which to start retrieving records. For example, if you set this parameter to 100, and the **count** parameter to 20, the endpoint returns records 100 through 119. **Note:** Any value that is set to less than one is interpreted as one.

 Not valid with the **id** path parameter.

 Data type: String

 Default: 1

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td id="status_400-SCIM-entry">

Bad Request. A bad request type or malformed request was detected.-   Ensure that both the **attributes** and **excludedAttributes** query parameters have not been passed in the request.
-   Ensure that the **count** parameter is not greater than 500.
-   Ensure that all **filter** parameters are valid.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

itemsPerPage

</td><td id="itemsPerPage-SCIM-entry">

Number of records returned in the return results.Data type: Number

</td></tr><tr><td>

Resources

</td><td>

List of user records.Data type: Array of Objects

 ```
"Resources": [
  {
    "active": Boolean,
    "addresses": {Object},
    "displayName": "String",
    "emails": [Array],
    "externalId": "String",
    "groups": [Array],
    "id": "String",
    "meta": {Object},
    "name": {Object},
    "phoneNumbers": [Array],
    "preferredLanguage": "String",
    "schemas": [Array],
    "timezone": "String",
    "title": "String",
    "userName": "String",
    "userType": "String"
  }
]
```

</td></tr><tr><td>

Resources.active

</td><td>

Flag that indicates whether the associated user is active within the ServiceNow instance.Possible values:

-   true: User is active.
-   false: User is inactive.

 Data type: Boolean

</td></tr><tr><td>

Resources.adresses

</td><td>

Details of the user's current mailing address.Data type: Object

 ```
"addresses": {
  "country": "String",
  "locality": "String",
  "postalCode": "String",
  "region": "String",
  "streetAddress": "String",
  "type": "String"
}
```

</td></tr><tr><td>

Resources.addresses.country

</td><td>

Country name.Data type: String

</td></tr><tr><td>

Resources.addresses.locality

</td><td>

City or locality name.Data type: String

</td></tr><tr><td>

Resources.addresses.postalCode

</td><td>

Zip or postal code.Data type: String

</td></tr><tr><td>

Resources.addresses.region

</td><td>

State or region.Data type: String

</td></tr><tr><td>

Resources.addresses.streetAddress

</td><td>

Full street address. This can include the house number, street name, PO Box, and multi-line extended street address information.Data type: String

</td></tr><tr><td>

Resources.addresses.type

</td><td>

Type of address. Currently only supports `home`.Data type: String

</td></tr><tr><td>

Resources.displayName

</td><td>

User display name. This value is auto-generated by concatenating the **name** fields. Data type: String

</td></tr><tr><td>

Resources.emails

</td><td>

List of email accounts associated with the user.Data type: Array of Objects

 ```
"emails:" [
  {
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

Resources.emails.type

</td><td>

User email type. Currently only supports type of "work".Data type: String

</td></tr><tr><td>

Resources.emails.value

</td><td>

User's email address. This is a unique key for the associated user.Data type: String

</td></tr><tr><td>

Resources.externalId

</td><td>

Unique identifier assigned to the user by the entity provisioning it.Data type: String

</td></tr><tr><td>

Resources.groups

</td><td>

List of groups to which the user belongs, either through direct membership, nested groups, or dynamically calculated.Data type: Array of Objects

 ```
"groups": [
  {
    "display": "String",
    "type": "String",
    "value": "String",
    "$ref": "String"
  }
]
```

</td></tr><tr><td>

Resources.groups.display

</td><td>

Name of the associated group.Data type: String

</td></tr><tr><td>

Resources.groups.type

</td><td>

Type of group association, such as direct or indirect.Data type: String

</td></tr><tr><td>

Resources.groups.value

</td><td>

Sys\_id of an associated group record.Data type: String

</td></tr><tr><td>

Resources.groups.ref

</td><td>

URI of the associated group.Data type: String

</td></tr><tr><td>

Resources.id

</td><td>

Sys\_id of the associated User record.Data type: String

</td></tr><tr><td>

Resources.meta

</td><td>

Metadata pertaining to the user.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": String",
  "resourceType": String"
}
```

</td></tr><tr><td>

Resources.meta.created

</td><td>

Date and time when the user record was created.Data type: String

</td></tr><tr><td>

Resources.meta.lastModified

</td><td>

Date and time when the user record was last modified.Data type: String

</td></tr><tr><td>

Resources.meta.location

</td><td>

URI of the user being retrieved.Data type: String

</td></tr><tr><td>

Resources.meta.resourceType

</td><td>

SCIM Users' resource type.Data type: String

</td></tr><tr><td>

Resources.name

</td><td>

User's name information.Data type: Object

 ```
"name": {
  "familyName": "String",
  "givenName": "String",
  "honorificPrefix": "String",
  "middleName": "String"
}
```

</td></tr><tr><td>

Resources.name.familyName

</td><td>

User's family or last name.Data type: String

</td></tr><tr><td>

Resources.name.givenName

</td><td>

User's given or first name.Data type: String

</td></tr><tr><td>

Resources.name.honorificPrefix

</td><td>

User's honorific name or title, such as Dr., Bishop, or Baron.Data type: String

</td></tr><tr><td>

Resources.name.middle

</td><td>

User's middle name.Data type: String

</td></tr><tr><td>

Resources.phoneNumbers

</td><td>

List of phone numbers associated with the user.Data type: Array of Objects

 ```
"phoneNumbers": [
  {
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

Resources.phoneNumbers.type

</td><td>

Type of phone number.Possible values:

 -   home
-   mobile
-   work

 Data type: String

</td></tr><tr><td>

Resources.phoneNumbers.value

</td><td>

User's phone number.Data type: String

</td></tr><tr><td>

Resources.preferredLanguage

</td><td>

User's preferred spoken and written language.Data type: String

</td></tr><tr><td>

Resources.schemas

</td><td>

List of URIs of the SCIM User schemas used to process the request.Data type: Array of Strings

</td></tr><tr><td>

Resources.timezone

</td><td>

User's time zone.Data type: String

</td></tr><tr><td>

Resources.title

</td><td>

User's title, such as CEO or President.Data type: String

</td></tr><tr><td>

Resources.userName

</td><td>

Unique user name for the associated user. Data type: String

</td></tr><tr><td>

Resources.userType

</td><td>

User type. This value is used to identify the organization to user relationship.This can be any value, but typical values might include:

-   Contractor
-   Employee
-   Intern
-   Temp
-   External
-   Unknown

 Data type: String

</td></tr><tr><td>

schemas

</td><td id="user_schemas-SCIM-entry">

List of URIs of the SCIM ListResponse schemas used to process the request.Data type: Array of Strings

</td></tr><tr><td>

startIndex

</td><td>

One-based index into the User \[sys\_user\] table at which the records were returned.Data type: String

</td></tr><tr><td>

totalResults

</td><td id="totalResults-SCIM-entry">

Total number of records that match the request.Data type: Number

</td></tr></tbody>
</table>### Extension parameters returned

<table id="id_hmw_fjk_grb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="user_company-SCIM-row"><td>

company

</td><td id="user_company-SCIM-entry">

Details about the user's associated company.Data type: Object

 ```
"company": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_company_display-SCIM-row"><td>

company.display

</td><td id="user_company_display-SCIM-entry">

Name of the company.Data type: String

</td></tr><tr id="user_company_value-SCIM-row"><td>

company.value

</td><td id="user_company_value-SCIM-entry">

Sys\_id of the company record. Data type: String

</td></tr><tr id="user_company_ref-SCIM-row"><td>

company.$ref

</td><td id="user_company_ref-SCIM-entry">

Reference URI for the company.Data type: String

</td></tr><tr id="user_costCenter-SCIM-row"><td>

costCenter

</td><td id="user_costCenter-SCIM-entry">

Details about the user's associated cost center.Data type: Object

 ```
"costCenter": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_costCenter_display-SCIM-row"><td>

costCenter.display

</td><td id="user_costCenter_display-SCIM-entry">

Name of the cost center.Data type: String

</td></tr><tr id="user_costCenter_value-SCIM-row"><td>

costCenter.value

</td><td id="user_costCenter_value-SCIM-entry">

Sys\_id of the cost center record. Data type: String

</td></tr><tr id="user_costCenter_ref-SCIM-row"><td>

costCenter.$ref

</td><td id="user_costCenter_ref-SCIM-entry">

Reference URI for the cost center.Data type: String

</td></tr><tr id="user_department-SCIM-row"><td>

department

</td><td id="user_department-SCIM-entry">

Details about the user's associated department.Data type: Object

 ```
"department": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_department_display-SCIM-row"><td>

department.display

</td><td id="user_department_display-SCIM-entry">

Name of the department.Data type: String

</td></tr><tr id="user_department_value-SCIM-row"><td>

department.value

</td><td id="user_department_value-SCIM-entry">

Sys\_id of the department record. Data type: String

</td></tr><tr id="user_department_ref-SCIM-row"><td>

department.$ref

</td><td id="user_department_ref-SCIM-entry">

Reference URI for the department.Data type: String

</td></tr><tr id="user_employeeNumber-SCIM-row"><td>

employeeNumber

</td><td id="user_employeeNumber-SCIM-entry">

Numeric or alphanumeric employee number.Data type: String

</td></tr><tr id="user_gender-SCIM-row"><td>

gender

</td><td id="user_gender-SCIM-entry">

Gender of the user, such as male or female.Data type: String

</td></tr><tr id="user_location-SCIM-row"><td>

location

</td><td id="user_location-SCIM-entry">

Details about the user's associated location.Data type: Object

 ```
"location": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_location_display-SCIM-row"><td>

location.display

</td><td id="user_location_display-SCIM-entry">

Name of the location.Data type: String

</td></tr><tr id="user_location_value-SCIM-row"><td>

location.value

</td><td id="user_location_value-SCIM-entry">

Sys\_id of the location record. Data type: String

</td></tr><tr id="user_location_ref-SCIM-row"><td>

location.$ref

</td><td id="user_location_ref-SCIM-entry">

Reference URI for the location.Data type: String

</td></tr><tr id="user_manager-SCIM-row"><td>

manager

</td><td id="user_manager-SCIM-entry">

Details about the user's associated manager.Data type: Object

 ```
"manager": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_manager_display-SCIM-row"><td>

manager.display

</td><td id="user_manager_display-SCIM-entry">

Name of the manager.Data type: String

</td></tr><tr id="user_manager_value-SCIM-row"><td>

manager.value

</td><td id="user_manager_value-SCIM-entry">

Sys\_id of the manager record. Data type: String

</td></tr><tr id="user_manager_ref-SCIM-row"><td>

manager.$ref

</td><td id="user_manager_ref-SCIM-entry">

Reference URI for the manager.Data type: String

</td></tr></tbody>
</table>### cURL request using attributes

The following example shows how to obtain two users starting at the sixth record and only returning the display name.

```
curl "https://instance-servicenow.com/api/now/scim/Users?attributes=displayName&startIndex=6&count=2" \
--request GET \
--header "Accept:application/scim+json" \
```

Response:

```
{"schemas":
  ["urn:ietf:params:scim:api:messages:2.0:ListResponse"],
  "totalResults":619,
  "Resources":
    [
      {
        "schemas":
          [
            "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User",
            "urn:ietf:params:scim:schemas:core:2.0:User"
          ],
        "id":"02826bf03710200044e0bfc8bcbe5d6d",
        "displayName":"Sean Bonnet"
      },
      {
        "schemas":
          [
            "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User",
            "urn:ietf:params:scim:schemas:core:2.0:User"
           ],
         "id":"02826bf03710200044e0bfc8bcbe5d76",
         "displayName":"Jacinto Gawron"
      }
    ],
  "startIndex":6,
  "itemsPerPage":2
}
```

### cURL request using a filter

The following example shows how to use the **filter** parameter to return the first two user records whose given name starts with "a".

```
curl "https://instance-servicenow.com/api/now/scim/Users?filter=name.givenName%20SW%20%22a%22&count=2" \
--request GET \
--header "Accept:application/scim+json" \
```

Response:

```
{"schemas":
  ["urn:ietf:params:scim:api:messages:2.0:ListResponse"],
  "totalResults":42,
  "Resources":
    [
      {
        "schemas":
          [
            "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User",
            "urn:ietf:params:scim:schemas:core:2.0:User"
          ],
        "id":"06826bf03710200044e0bfc8bcbe5d8a",
        "meta":
          {
            "resourceType":"User",
            "created":"2012-02-18T03:04:50Z",
            "lastModified":"2021-10-01T14:23:32Z",
            "location":"https://instance-servicenow.com/api/now/scim/Users/06826bf03710200044e0bfc8bcbe5d8a"
          },
          "userName":"allyson.gillispie",
          "name":
            {
              "familyName":"Gillispie",
              "givenName":"Allyson"
            },
          "displayName":"Allyson Gillispie",
          "active":true,
          "emails":
            [
              {
                "value":"allyson.gillispie@example.com",
                "type":"work"
              }
            ],
          "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User":
            {
              "gender":"Female",
              "costCenter":
                {
                  "value":"d9d07bddc0a80a647cf932056ed24652",
                  "name":"Engineering"
                },
              "company":
                {
                  "value":"31bea3d53790200044e0bfc8bcbe5dec",
                  "name":"ACME North America"
                },
              "department":
                {
                  "value":"221f3db5c6112284009f4becd3039cc9",
                  "name":"Development"
                },
              "location":
                {
                  "value":"f9084ba00a0a0b910060ba2ce83f882b",
                  "name":"946 Donax Avenue, Imperial Beach,CA"
                }
            }
         },
      {
        "schemas":
          [
            "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User",
            "urn:ietf:params:scim:schemas:core:2.0:User"
          ],
        "id":"0a826bf03710200044e0bfc8bcbe5d7a"
        "meta":
          {
            "resourceType":"User",
            "created":"2012-02-18T03:04:50Z",
            "lastModified":"2021-10-01T14:23:32Z",
            "location":"https://instance-servicenow.com/api/now/scim/Users/0a826bf03710200044e0bfc8bcbe5d7a"
          },
        "userName":"adela.cervantsz",
        "name":
          {
            "familyName":"Cervantsz",
            "givenName":"Adela"
          },
        "displayName":"Adela Cervantsz",
        "active":true,
        "emails":
          [
            {
              "value":"adela.cervantsz@example.com",
              "type":"work"
            }
          ],
        "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User":
          {
            "gender":"Female",
            "costCenter":
              {
                "value":"91e8bbf43710200044e0bfc8bcbe5daa",
                "name":"Customer Support"
              },
            "company":
              {
                "value":"31bea3d53790200044e0bfc8bcbe5dec",
                "name":"ACME North America"
              },
            "department":
              {
                "value":"5d7f17f03710200044e0bfc8bcbe5d43",
                "name":"Customer Support"
              },
            "location":
              {
                "value":"25ab93750a0a0bb30067bd2ef3d4a5c9",
                "name":"8306 Mills Drive, Miami,FL"
              }
          }
    }
  ],
  "startIndex":1,
  "itemsPerPage":2
}
```

## SCIM - GET /scim/Users/\{user\_id\}

Returns the specified user record from the User \[sys\_user\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Users/{user_id}`

Default URL: `/api/now/scim/Users/{user_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

user\_id

</td><td>

Sys\_id of the user record to return.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td id="status_400-SCIM-entry">

Bad Request. A bad request type or malformed request was detected.-   Ensure that both the **attributes** and **excludedAttributes** query parameters have not been passed in the request.
-   Ensure that the **count** parameter is not greater than 500.
-   Ensure that all **filter** parameters are valid.

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="id_x11_hyj_grb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="user_active-SCIM-row"><td>

active

</td><td id="user_active-SCIM-entry">

Flag that indicates whether the associated user is active within the ServiceNow instance.Possible values:

-   true: User is active.
-   false: User is inactive.

 Data type: Boolean

</td></tr><tr id="user_addresses-SCIM-row"><td>

addresses

</td><td id="user_addresses-SCIM-entry">

Details of the user's current mailing address.Data type: Object

 ```
"addresses": {
  "country": "String",
  "locality": "String",
  "postalCode": "String",
  "region": "String",
  "streetAddress": "String",
  "type": "String"
}
```

</td></tr><tr id="user_addresses_country-SCIM-row"><td>

addresses.country

</td><td id="user_addresses_country-SCIM-entry">

Country name.Data type: String

</td></tr><tr id="user_addresses_locality-SCIM-row"><td>

addresses.locality

</td><td id="user_addresses_locality-SCIM-entry">

City or locality name.Data type: String

</td></tr><tr id="user_addresses_postalCode-SCIM-row"><td>

addresses.postalCode

</td><td id="user_addresses_postalCode-SCIM-entry">

Zip or postal code.Data type: String

</td></tr><tr id="user_addresses_region-SCIM-row"><td>

addresses.region

</td><td id="user_addresses_region-SCIM-entry">

State or region.Data type: String

</td></tr><tr id="user_addresses_streetAddress-SCIM-row"><td>

addresses.streetAddress

</td><td id="user_addresses_streetAddress-SCIM-entry">

Full street address. This can include the house number, street name, PO Box, and multi-line extended street address information.Data type: String

</td></tr><tr id="user_addresses_type-SCIM-row"><td>

addresses.type

</td><td id="user_addresses_type-SCIM-entry">

Type of address. Currently only supports `home`.Data type: String

</td></tr><tr id="user_displayName-SCIM-row"><td>

displayName

</td><td id="user_displayName-SCIM-entry">

User display name. This value is auto-generated by concatenating the **name** fields. Data type: String

</td></tr><tr id="user_emails-SCIM-row"><td>

emails

</td><td id="user_emails-SCIM-entry">

List of email accounts associated with the user.Data type: Array of Objects

 ```
"emails:" [
  {
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr id="user_emails_type-SCIM-row"><td>

emails.type

</td><td id="user_emails_type-SCIM-entry">

User email type. Currently only supports type of "work".Data type: String

</td></tr><tr id="user_emails_value-SCIM-row"><td>

emails.value

</td><td id="user_emails_value-SCIM-entry">

User's email address. This is a unique key for the associated user.Data type: String

</td></tr><tr id="user_emails_externalId-SCIM-row"><td>

externalId

</td><td id="user_emails_externalId-SCIM-entry">

Unique identifier assigned to the user by the entity provisioning it.Data type: String

</td></tr><tr id="user_groups-SCIM-row"><td>

groups

</td><td id="user_groups-SCIM-entry">

List of groups to which the user belongs, either through direct membership, nested groups, or dynamically calculated.Data type: Array of Objects

 ```
"groups": [
  {
    "display": "String",
    "type": "String",
    "value": "String",
    "$ref": "String"
  }
]
```

</td></tr><tr id="user_groups_display-SCIM-row"><td>

groups.display

</td><td id="user_groups_display-SCIM-entry">

Name of the associated group.Data type: String

</td></tr><tr id="user_groups_type-SCIM-row"><td>

groups.type

</td><td id="user_groups_type-SCIM-entry">

Type of group association, such as direct or indirect.Data type: String

</td></tr><tr id="user_groups_value-SCIM-row"><td>

groups.value

</td><td id="user_groups_value-SCIM-entry">

Sys\_id of an associated group record.Data type: String

</td></tr><tr id="user_groups_ref-SCIM-row"><td>

groups.$ref

</td><td id="user_groups_ref-SCIM-entry">

URI of the associated group.Data type: String

</td></tr><tr id="user_id-SCIM-row"><td>

id

</td><td id="user_id-SCIM-entry">

Sys\_id of the associated User record.Data type: String

</td></tr><tr id="user_meta-SCIM-row"><td>

meta

</td><td id="user_meta-SCIM-entry">

Metadata pertaining to the user.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": String",
  "resourceType": String"
}
```

</td></tr><tr id="user_meta_created-SCIM-row"><td>

meta.created

</td><td id="user_meta_created-SCIM-entry">

Date and time when the user record was created.Data type: String

</td></tr><tr id="user_meta_lastModified-SCIM-row"><td>

meta.lastModified

</td><td id="user_meta_lastModified-SCIM-entry">

Date and time when the user record was last modified.Data type: String

</td></tr><tr id="user_meta_location-SCIM-row"><td>

meta.location

</td><td id="user_meta_location-SCIM-entry">

URI of the user being retrieved.Data type: String

</td></tr><tr id="user_meta_resourceType-SCIM-row"><td>

meta.resourceType

</td><td id="user_meta_resourceType-SCIM-entry">

SCIM Users' resource type.Data type: String

</td></tr><tr id="user_name-SCIM-row"><td>

name

</td><td id="user_name-SCIM-entry">

User's name information.Data type: Object

 ```
"name": {
  "familyName": "String",
  "givenName": "String",
  "honorificPrefix": "String",
  "middleName": "String"
}
```

</td></tr><tr id="user_name_familyName-SCIM-row"><td>

name.familyName

</td><td id="user_name_familyName-SCIM-entry">

User's family or last name.Data type: String

</td></tr><tr id="user_name_givenName-SCIM-row"><td>

name.givenName

</td><td id="user_name_givenName-SCIM-entry">

User's given or first name.Data type: String

</td></tr><tr id="user_name_honorificPrefix-SCIM-row"><td>

name.honorificPrefix

</td><td id="user_name_honorificPrefix-SCIM-entry">

User's honorific name or title, such as Dr., Bishop, or Baron.Data type: String

</td></tr><tr id="user_name_middle-SCIM-row"><td>

name.middle

</td><td id="user_name_middle-SCIM-entry">

User's middle name.Data type: String

</td></tr><tr id="user_phoneNumbers-SCIM-row"><td>

phoneNumbers

</td><td id="user_phoneNumbers-SCIM-entry">

List of phone numbers associated with the user.Data type: Array of Objects

 ```
"phoneNumbers": [
  {
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr id="user_phoneNumbers_type-SCIM-row"><td>

phoneNumbers.type

</td><td id="user_phoneNumbers_type-SCIM-entry">

Type of phone number.Possible values:

 -   home
-   mobile
-   work

 Data type: String

</td></tr><tr id="user_phoneNumbers_value-SCIM-row"><td>

phoneNumbers.value

</td><td id="user_phoneNumbers_value-SCIM-entry">

User's phone number.Data type: String

</td></tr><tr id="user_preferredLanguage-SCIM-row"><td>

preferredLanguage

</td><td id="user_preferredLanguage-SCIM-entry">

User's preferred spoken and written language.Data type: String

</td></tr><tr id="user_schemas-SCIM-row"><td>

schemas

</td><td id="user_schemas-SCIM-entry">

List of URIs of the SCIM User schemas used to process the request.Data type: Array of Strings

</td></tr><tr id="user_timezone-SCIM-row"><td>

timezone

</td><td id="user_timezone-SCIM-entry">

User's time zone.Data type: String

</td></tr><tr id="user_title-SCIM-row"><td>

title

</td><td id="user_title-SCIM-entry">

User's title, such as CEO or President.Data type: String

</td></tr><tr id="user_userName-SCIM-row"><td>

userName

</td><td id="user_userName-SCIM-entry">

Unique user name for the associated user. Data type: String

</td></tr><tr id="user_userType-SCIM-row"><td>

userType

</td><td id="user_userType-SCIM-entry">

User type. This value is used to identify the organization to user relationship.This can be any value, but typical values might include:

-   Contractor
-   Employee
-   Intern
-   Temp
-   External
-   Unknown

 Data type: String

</td></tr></tbody>
</table>### Extension parameters returned

<table id="id_hmw_fjk_grb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="user_company-SCIM-row"><td>

company

</td><td id="user_company-SCIM-entry">

Details about the user's associated company.Data type: Object

 ```
"company": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_company_display-SCIM-row"><td>

company.display

</td><td id="user_company_display-SCIM-entry">

Name of the company.Data type: String

</td></tr><tr id="user_company_value-SCIM-row"><td>

company.value

</td><td id="user_company_value-SCIM-entry">

Sys\_id of the company record. Data type: String

</td></tr><tr id="user_company_ref-SCIM-row"><td>

company.$ref

</td><td id="user_company_ref-SCIM-entry">

Reference URI for the company.Data type: String

</td></tr><tr id="user_costCenter-SCIM-row"><td>

costCenter

</td><td id="user_costCenter-SCIM-entry">

Details about the user's associated cost center.Data type: Object

 ```
"costCenter": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_costCenter_display-SCIM-row"><td>

costCenter.display

</td><td id="user_costCenter_display-SCIM-entry">

Name of the cost center.Data type: String

</td></tr><tr id="user_costCenter_value-SCIM-row"><td>

costCenter.value

</td><td id="user_costCenter_value-SCIM-entry">

Sys\_id of the cost center record. Data type: String

</td></tr><tr id="user_costCenter_ref-SCIM-row"><td>

costCenter.$ref

</td><td id="user_costCenter_ref-SCIM-entry">

Reference URI for the cost center.Data type: String

</td></tr><tr id="user_department-SCIM-row"><td>

department

</td><td id="user_department-SCIM-entry">

Details about the user's associated department.Data type: Object

 ```
"department": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_department_display-SCIM-row"><td>

department.display

</td><td id="user_department_display-SCIM-entry">

Name of the department.Data type: String

</td></tr><tr id="user_department_value-SCIM-row"><td>

department.value

</td><td id="user_department_value-SCIM-entry">

Sys\_id of the department record. Data type: String

</td></tr><tr id="user_department_ref-SCIM-row"><td>

department.$ref

</td><td id="user_department_ref-SCIM-entry">

Reference URI for the department.Data type: String

</td></tr><tr id="user_employeeNumber-SCIM-row"><td>

employeeNumber

</td><td id="user_employeeNumber-SCIM-entry">

Numeric or alphanumeric employee number.Data type: String

</td></tr><tr id="user_gender-SCIM-row"><td>

gender

</td><td id="user_gender-SCIM-entry">

Gender of the user, such as male or female.Data type: String

</td></tr><tr id="user_location-SCIM-row"><td>

location

</td><td id="user_location-SCIM-entry">

Details about the user's associated location.Data type: Object

 ```
"location": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_location_display-SCIM-row"><td>

location.display

</td><td id="user_location_display-SCIM-entry">

Name of the location.Data type: String

</td></tr><tr id="user_location_value-SCIM-row"><td>

location.value

</td><td id="user_location_value-SCIM-entry">

Sys\_id of the location record. Data type: String

</td></tr><tr id="user_location_ref-SCIM-row"><td>

location.$ref

</td><td id="user_location_ref-SCIM-entry">

Reference URI for the location.Data type: String

</td></tr><tr id="user_manager-SCIM-row"><td>

manager

</td><td id="user_manager-SCIM-entry">

Details about the user's associated manager.Data type: Object

 ```
"manager": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_manager_display-SCIM-row"><td>

manager.display

</td><td id="user_manager_display-SCIM-entry">

Name of the manager.Data type: String

</td></tr><tr id="user_manager_value-SCIM-row"><td>

manager.value

</td><td id="user_manager_value-SCIM-entry">

Sys\_id of the manager record. Data type: String

</td></tr><tr id="user_manager_ref-SCIM-row"><td>

manager.$ref

</td><td id="user_manager_ref-SCIM-entry">

Reference URI for the manager.Data type: String

</td></tr></tbody>
</table>### cURL request using user sys\_id

The following example shows how to obtain a specific user record by passing their sys\_id.

```
curl "https://instance-servicenow.com/api/now/scim/Users/62826bf03710200044e0bfc8bcbe5df1" \
--request GET \
--header "Accept:application/scim+json" \
```

Response:

```
{"schemas":
  [
    "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User",
    "urn:ietf:params:scim:schemas:core:2.0:User"
  ],
    "id":"62826bf03710200044e0bfc8bcbe5df1",
    "meta":
      {
        "resourceType":"User",
        "created":"2012-02-18T03:04:52Z",
        "lastModified":"2021-10-01T14:23:34Z",
        "location":"https://instance-servicenow.com/api/now/scim/Users/62826bf03710200044e0bfc8bcbe5df1"
      },
    "userName":"abel.tuter",
    "name":
      {
        "familyName":"Tuter",
        "givenName":"Abel"
      },
    "displayName":"Abel Tuter",
    "active":true,
    "emails":[
      {
        "value":"abel.tuter@example.com",
        "type":"work"
      }
    ],
    "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User":
      {
        "gender":"Male",
        "costCenter":
          {
            "value":"d9d07bddc0a80a647cf932056ed24652",
            "name":"Engineering"
          },
        "company":
          {
            "value":"227cdfb03710200044e0bfc8bcbe5d6b",
            "name":"ACME South America"
          },
        "department":
          {
            "value":"9a7ed3f03710200044e0bfc8bcbe5db7",
            "name":"Product Management"
           },
        "location":
          {
            "value":"25b3d04b0a0a0bb300176b546c22db27",
            "name":"SHS quadra 5, Bloco E., Brasilia"}
          }
      }

```

## SCIM - PATCH /scim/Users/\{user\_id\}

Enables you to add, replace, and remove specified fields in a user record in the User \[sys\_user\] table of a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Users/{user_id}`

Default URL: `/api/now/scim/Users/{user_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

user\_id

</td><td>

Sys\_id of the user record to modify.

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Operations

</td><td>

Required. List of operation objects to patch the specified user record with.Data type: Array

 ```
"Operations": [
  {
    "op": "String",
    "path": "String",
    "value": Any
  }
]
```

</td></tr><tr><td>

Operations.op

</td><td>

Required. Operation to perform.Valid values:

-   add: Add the specified field and value to the user record.
-   remove: Remove the value from the specified field.
-   replace: Replace the value of the specified field.

 Data type: String

</td></tr><tr><td>

Operations.path

</td><td>

Required for `remove` operations. Name/path of the field to modify.The **path** parameter can have one of the following formats:

-   A direct field, such as `title`
-   A nested fields, such as `name.givenName`
-   In case of complex array, it can point to a specific element with a filter, such as: `emails[type eq "work"]`

```
{
  "schemas": [
    "urn:ietf:params:scim:api:messages:2.0:PatchOp"
  ],
  "Operations": [
    {
      "op": "add",
      "path": "title",
      "value": "xyz"
    },
    {  
      "op": "replace",
      "path": "name.givenName",
      "value": "Jennifer"
    },
    {
      "op": "replace",
      "path": "emails[type eq \"work\"]",
      "value": "xyz@test.com"
    }
  ]
}
```

 Data type: String

 Default: Considers the field to be a user resource.

</td></tr><tr><td>

Operations.value

</td><td>

Value of the field specified in the **Operations.path** parameter. The format of this parameter depends on the data-type of the associated field. For example, if updating a simple string, such as the title, the **value** field is expressed as a string.

 ```
 "Operations": [
  {
    "op": "add",
    "path": "title",
    "value": "xyz"
  }
]
```

 You can also declare simple string values without using **value** or **path** parameters, such as:

```
 "Operations": [
  {
    "op": "add",
    "title": "xyz"
  }
]
```

 However, when updating a phone number, which is an array that contains objects that define additional fields to add to the user record and their associated values, the **value** field is expressed as an array of objects.

 ```
 "Operations": [
  {
    "op": "add",
    "path": "phoneNumbers",
    "value": [
      {
        "type": "work",
        "value": "9876543210"
      },
      {
        "type": "home",
        "value": "9876783216"
      }
    ]
  }
]
```

 When specifying attribute nodes, the entry can include the nesting as follows:

```
{
  "op": "replace",
  "value": {
    "name": {
      "familyName": "Jones",
      "givenName": "Jennifer"
    }
  }
}
```

Or you can specify the nesting in the **Operations.path**:

 ```
{
  "op": "replace",
  "path": "name.givenName",
  "value": "Jennifer"
}
```

 If the field being updated is not in the base-schema, you must enclose the name-value pair in an object that specifies the URN of the associated schema.

 ```
"value": {
  "<schema_urn>": {
    "<field_name>": "<new_value>"
  },
}
```

 For example:

 ```
"value": {
  "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User": {
    "employeeNumber": "13454"
  },
}
```

Data type: Any

</td></tr><tr><td>

Operations.value.type

</td><td>

Name of the field to update.Data type: String

</td></tr><tr><td>

Operations.value.value

</td><td>

Value to update the field with. Data type: String

</td></tr><tr><td>

schemas

</td><td>

Required. SCIM Schema URI of Patch Operation `urn:ietf:params:scim:api:messages:2.0:PatchOp`.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="Content_Type-SCIM-entry">

Data format of the request body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. A bad request type or malformed request was detected.-   Check for invalid values:
    -   Malformed request body.
    -   Required field is not provided or empty.
    -   Invalid user or group sys\_id is provided.
-   Check if a read-only or immutable field is trying to be modified.
-   Ensure that both the **attributes** and **excludedAttributes** query parameters have not been passed in the request or that the request does not exceed the maximum number of members.

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr><tr><td>

409

</td><td>

User already exists. The **userName** parameter must be unique.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_mjy_k1l_grb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td id="user_active-SCIM-entry">

Flag that indicates whether the associated user is active within the ServiceNow instance.Possible values:

-   true: User is active.
-   false: User is inactive.

 Data type: Boolean

</td></tr><tr><td>

addresses

</td><td id="user_addresses-SCIM-entry">

Details of the user's current mailing address.Data type: Object

 ```
"addresses": {
  "country": "String",
  "locality": "String",
  "postalCode": "String",
  "region": "String",
  "streetAddress": "String",
  "type": "String"
}
```

</td></tr><tr><td>

addresses.country

</td><td id="user_addresses_country-SCIM-entry">

Country name.Data type: String

</td></tr><tr><td>

addresses.locality

</td><td id="user_addresses_locality-SCIM-entry">

City or locality name.Data type: String

</td></tr><tr><td>

addresses.postalCode

</td><td id="user_addresses_postalCode-SCIM-entry">

Zip or postal code.Data type: String

</td></tr><tr><td>

addresses.region

</td><td id="user_addresses_region-SCIM-entry">

State or region.Data type: String

</td></tr><tr><td>

addresses.streetAddress

</td><td id="user_addresses_streetAddress-SCIM-entry">

Full street address. This can include the house number, street name, PO Box, and multi-line extended street address information.Data type: String

</td></tr><tr><td>

addresses.type

</td><td id="user_addresses_type-SCIM-entry">

Type of address. Currently only supports `home`.Data type: String

</td></tr><tr><td>

displayName

</td><td id="user_displayName-SCIM-entry">

User display name. This value is auto-generated by concatenating the **name** fields. Data type: String

</td></tr><tr><td>

emails

</td><td id="user_emails-SCIM-entry">

List of email accounts associated with the user.Data type: Array of Objects

 ```
"emails:" [
  {
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

emails.type

</td><td id="user_emails_type-SCIM-entry">

User email type. Currently only supports type of "work".Data type: String

</td></tr><tr><td>

emails.value

</td><td id="user_emails_value-SCIM-entry">

User's email address. This is a unique key for the associated user.Data type: String

</td></tr><tr><td>

errors

</td><td id="errors-SCIM-entry">

Response that describes any errors that may have occurred during processing the request.Data type: Object

 ```
"errors": {
  "details": "String",
  "schemas": "String",
  "scimType": "String",
  "status": "String"
}
```

</td></tr><tr><td>

errors.detail

</td><td id="errors_details-SCIM-entry">

Detailed error message on why the request failed.Data type: String

</td></tr><tr><td>

errors.scimType

</td><td id="errors_scimType-SCIM-entry">

SCIM error detail keyword.Data type: String

</td></tr><tr><td>

errors.schemas

</td><td id="errors_schemas-SCIM-entry">

URI of the SCIM Schemas used to process the error response.Data type: Array of Strings

</td></tr><tr><td>

errors.status

</td><td id="errors_status-SCIM-entry">

HTTP status code for the error response.Data type: String

</td></tr><tr><td>

externalId

</td><td id="user_emails_externalId-SCIM-entry">

Unique identifier assigned to the user by the entity provisioning it.Data type: String

</td></tr><tr><td>

groups

</td><td id="user_groups-SCIM-entry">

List of groups to which the user belongs, either through direct membership, nested groups, or dynamically calculated.Data type: Array of Objects

 ```
"groups": [
  {
    "display": "String",
    "type": "String",
    "value": "String",
    "$ref": "String"
  }
]
```

</td></tr><tr><td>

groups.display

</td><td id="user_groups_display-SCIM-entry">

Name of the associated group.Data type: String

</td></tr><tr><td>

groups.type

</td><td id="user_groups_type-SCIM-entry">

Type of group association, such as direct or indirect.Data type: String

</td></tr><tr><td>

groups.value

</td><td id="user_groups_value-SCIM-entry">

Sys\_id of an associated group record.Data type: String

</td></tr><tr><td>

groups.$ref

</td><td id="user_groups_ref-SCIM-entry">

URI of the associated group.Data type: String

</td></tr><tr><td>

id

</td><td id="user_id-SCIM-entry">

Sys\_id of the associated User record.Data type: String

</td></tr><tr><td>

meta

</td><td id="user_meta-SCIM-entry">

Metadata pertaining to the user.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": String",
  "resourceType": String"
}
```

</td></tr><tr><td>

meta.created

</td><td id="user_meta_created-SCIM-entry">

Date and time when the user record was created.Data type: String

</td></tr><tr><td>

meta.lastModified

</td><td id="user_meta_lastModified-SCIM-entry">

Date and time when the user record was last modified.Data type: String

</td></tr><tr><td>

meta.location

</td><td id="user_meta_location-SCIM-entry">

URI of the user being retrieved.Data type: String

</td></tr><tr><td>

meta.resourceType

</td><td id="user_meta_resourceType-SCIM-entry">

SCIM Users' resource type.Data type: String

</td></tr><tr><td>

name

</td><td id="user_name-SCIM-entry">

User's name information.Data type: Object

 ```
"name": {
  "familyName": "String",
  "givenName": "String",
  "honorificPrefix": "String",
  "middleName": "String"
}
```

</td></tr><tr><td>

name.familyName

</td><td id="user_name_familyName-SCIM-entry">

User's family or last name.Data type: String

</td></tr><tr><td>

name.givenName

</td><td id="user_name_givenName-SCIM-entry">

User's given or first name.Data type: String

</td></tr><tr><td>

name.honorificPrefix

</td><td id="user_name_honorificPrefix-SCIM-entry">

User's honorific name or title, such as Dr., Bishop, or Baron.Data type: String

</td></tr><tr><td>

name.middle

</td><td id="user_name_middle-SCIM-entry">

User's middle name.Data type: String

</td></tr><tr><td>

phoneNumbers

</td><td id="user_phoneNumbers-SCIM-entry">

List of phone numbers associated with the user.Data type: Array of Objects

 ```
"phoneNumbers": [
  {
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

phoneNumbers.type

</td><td id="user_phoneNumbers_type-SCIM-entry">

Type of phone number.Possible values:

 -   home
-   mobile
-   work

 Data type: String

</td></tr><tr><td>

phoneNumbers.value

</td><td id="user_phoneNumbers_value-SCIM-entry">

User's phone number.Data type: String

</td></tr><tr><td>

preferredLanguage

</td><td id="user_preferredLanguage-SCIM-entry">

User's preferred spoken and written language.Data type: String

</td></tr><tr><td>

schemas

</td><td id="user_schemas-SCIM-entry">

List of URIs of the SCIM User schemas used to process the request.Data type: Array of Strings

</td></tr><tr><td>

timezone

</td><td id="user_timezone-SCIM-entry">

User's time zone.Data type: String

</td></tr><tr><td>

title

</td><td id="user_title-SCIM-entry">

User's title, such as CEO or President.Data type: String

</td></tr><tr><td>

userName

</td><td id="user_userName-SCIM-entry">

Unique user name for the associated user. Data type: String

</td></tr><tr><td>

userType

</td><td id="user_userType-SCIM-entry">

User type. This value is used to identify the organization to user relationship.This can be any value, but typical values might include:

-   Contractor
-   Employee
-   Intern
-   Temp
-   External
-   Unknown

 Data type: String

</td></tr></tbody>
</table>### Extension parameters returned

<table id="id_hmw_fjk_grb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="user_company-SCIM-row"><td>

company

</td><td id="user_company-SCIM-entry">

Details about the user's associated company.Data type: Object

 ```
"company": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_company_display-SCIM-row"><td>

company.display

</td><td id="user_company_display-SCIM-entry">

Name of the company.Data type: String

</td></tr><tr id="user_company_value-SCIM-row"><td>

company.value

</td><td id="user_company_value-SCIM-entry">

Sys\_id of the company record. Data type: String

</td></tr><tr id="user_company_ref-SCIM-row"><td>

company.$ref

</td><td id="user_company_ref-SCIM-entry">

Reference URI for the company.Data type: String

</td></tr><tr id="user_costCenter-SCIM-row"><td>

costCenter

</td><td id="user_costCenter-SCIM-entry">

Details about the user's associated cost center.Data type: Object

 ```
"costCenter": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_costCenter_display-SCIM-row"><td>

costCenter.display

</td><td id="user_costCenter_display-SCIM-entry">

Name of the cost center.Data type: String

</td></tr><tr id="user_costCenter_value-SCIM-row"><td>

costCenter.value

</td><td id="user_costCenter_value-SCIM-entry">

Sys\_id of the cost center record. Data type: String

</td></tr><tr id="user_costCenter_ref-SCIM-row"><td>

costCenter.$ref

</td><td id="user_costCenter_ref-SCIM-entry">

Reference URI for the cost center.Data type: String

</td></tr><tr id="user_department-SCIM-row"><td>

department

</td><td id="user_department-SCIM-entry">

Details about the user's associated department.Data type: Object

 ```
"department": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_department_display-SCIM-row"><td>

department.display

</td><td id="user_department_display-SCIM-entry">

Name of the department.Data type: String

</td></tr><tr id="user_department_value-SCIM-row"><td>

department.value

</td><td id="user_department_value-SCIM-entry">

Sys\_id of the department record. Data type: String

</td></tr><tr id="user_department_ref-SCIM-row"><td>

department.$ref

</td><td id="user_department_ref-SCIM-entry">

Reference URI for the department.Data type: String

</td></tr><tr id="user_employeeNumber-SCIM-row"><td>

employeeNumber

</td><td id="user_employeeNumber-SCIM-entry">

Numeric or alphanumeric employee number.Data type: String

</td></tr><tr id="user_gender-SCIM-row"><td>

gender

</td><td id="user_gender-SCIM-entry">

Gender of the user, such as male or female.Data type: String

</td></tr><tr id="user_location-SCIM-row"><td>

location

</td><td id="user_location-SCIM-entry">

Details about the user's associated location.Data type: Object

 ```
"location": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_location_display-SCIM-row"><td>

location.display

</td><td id="user_location_display-SCIM-entry">

Name of the location.Data type: String

</td></tr><tr id="user_location_value-SCIM-row"><td>

location.value

</td><td id="user_location_value-SCIM-entry">

Sys\_id of the location record. Data type: String

</td></tr><tr id="user_location_ref-SCIM-row"><td>

location.$ref

</td><td id="user_location_ref-SCIM-entry">

Reference URI for the location.Data type: String

</td></tr><tr id="user_manager-SCIM-row"><td>

manager

</td><td id="user_manager-SCIM-entry">

Details about the user's associated manager.Data type: Object

 ```
"manager": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_manager_display-SCIM-row"><td>

manager.display

</td><td id="user_manager_display-SCIM-entry">

Name of the manager.Data type: String

</td></tr><tr id="user_manager_value-SCIM-row"><td>

manager.value

</td><td id="user_manager_value-SCIM-entry">

Sys\_id of the manager record. Data type: String

</td></tr><tr id="user_manager_ref-SCIM-row"><td>

manager.$ref

</td><td id="user_manager_ref-SCIM-entry">

Reference URI for the manager.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to add, remove, and replace values within a user record.

```
curl -X PATCH \
  https://instance-servicenow.com/api/now/scim/Users/005d500b536073005e0addeeff7b12f4 \
  -d '{
  "schemas": [
    "urn:ietf:params:scim:api:messages:2.0:PatchOp"
  ],
  "Operations": [
    {
      "op" : "remove",
      "path" : "title" 
    },
    {
      "op" : "add",
      "path" : "phoneNumbers",
      "value" : [
        {
          "type" : "work",
          "value" : "9876543210"
        }
      ]
    },
    {
      "op": "replace",
      "value": {
        "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User": {
            "employeeNumber": "13454"
        },
        "name": {
            "familyName": "John",
            "givenName": "Smith"
        }
      }
    }
  ]
}'
```

Response:

```
{
  "schemas":[
    "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User",
    "urn:ietf:params:scim:schemas:core:2.0:User"
  ],
  "id":"005d500b536073005e0addeeff7b12f4",
  "meta":{
    "resourceType":"User",
    "created":"2019-04-05T21:09:12Z",
    "lastModified":"2021-10-12T18:29:27Z",
    "location":"https://instance-servicenow.com/api/now/scim/Users/005d500b536073005e0addeeff7b12f4"
  },
  "userName":"survey.user",
  "name":{
    "familyName":"John",
    "givenName":"Smith"
  },
  "displayName":"Smith John",
  "active":true,
  "emails":[
    {
      "value":"survey.user@email.com",
      "type":"work"
    }
  ],
  "phoneNumbers":[
    {
      "value":"9876543210",
      "type":"work"
    }
  ],
  "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User":{
    "employeeNumber":"13454"
  }
}

```

## SCIM - POST /scim/Users

Creates a user record in the User \[sys\_user\] table of a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

**Note:** The search and bulk modifications functionality as noted in the RFC7643 specification are not supported by this endpoint.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Users`

Default URL: `/api/now/scim/Users`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td id="user_active-SCIM-entry">

Flag that indicates whether the associated user is active within the ServiceNow instance.Possible values:

-   true: User is active.
-   false: User is inactive.

 Data type: Boolean

</td></tr><tr><td>

addresses

</td><td id="user_addresses-SCIM-entry">

Details of the user's current mailing address.Data type: Object

 ```
"addresses": {
  "country": "String",
  "locality": "String",
  "postalCode": "String",
  "region": "String",
  "streetAddress": "String",
  "type": "String"
}
```

</td></tr><tr><td>

addresses.country

</td><td id="user_addresses_country-SCIM-entry">

Country name.Data type: String

</td></tr><tr><td>

addresses.locality

</td><td id="user_addresses_locality-SCIM-entry">

City or locality name.Data type: String

</td></tr><tr><td>

addresses.postalCode

</td><td id="user_addresses_postalCode-SCIM-entry">

Zip or postal code.Data type: String

</td></tr><tr><td>

addresses.region

</td><td id="user_addresses_region-SCIM-entry">

State or region.Data type: String

</td></tr><tr><td>

addresses.streetAddress

</td><td id="user_addresses_streetAddress-SCIM-entry">

Full street address. This can include the house number, street name, PO Box, and multi-line extended street address information.Data type: String

</td></tr><tr><td>

addresses.type

</td><td id="user_addresses_type-SCIM-entry">

Type of address. Currently only supports `home`.Data type: String

</td></tr><tr><td>

displayName

</td><td id="user_displayName-SCIM-entry">

User display name. This value is auto-generated by concatenating the **name** fields. Data type: String

</td></tr><tr><td>

emails

</td><td id="user_emails-SCIM-entry">

List of email accounts associated with the user.Data type: Array of Objects

 ```
"emails:" [
  {
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

emails.type

</td><td id="user_emails_type-SCIM-entry">

User email type. Currently only supports type of "work".Data type: String

</td></tr><tr><td>

emails.value

</td><td id="user_emails_value-SCIM-entry">

User's email address. This is a unique key for the associated user.Data type: String

</td></tr><tr><td>

externalId

</td><td id="user_emails_externalId-SCIM-entry">

Unique identifier assigned to the user by the entity provisioning it.Data type: String

</td></tr><tr><td>

name

</td><td id="user_name-SCIM-entry">

User's name information.Data type: Object

 ```
"name": {
  "familyName": "String",
  "givenName": "String",
  "honorificPrefix": "String",
  "middleName": "String"
}
```

</td></tr><tr><td>

name.familyName

</td><td id="user_name_familyName-SCIM-entry">

User's family or last name.Data type: String

</td></tr><tr><td>

name.givenName

</td><td id="user_name_givenName-SCIM-entry">

User's given or first name.Data type: String

</td></tr><tr><td>

name.honorificPrefix

</td><td id="user_name_honorificPrefix-SCIM-entry">

User's honorific name or title, such as Dr., Bishop, or Baron.Data type: String

</td></tr><tr><td>

name.middle

</td><td id="user_name_middle-SCIM-entry">

User's middle name.Data type: String

</td></tr><tr><td>

phoneNumbers

</td><td id="user_phoneNumbers-SCIM-entry">

List of phone numbers associated with the user.Data type: Array of Objects

 ```
"phoneNumbers": [
  {
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

phoneNumbers.type

</td><td id="user_phoneNumbers_type-SCIM-entry">

Type of phone number.Possible values:

 -   home
-   mobile
-   work

 Data type: String

</td></tr><tr><td>

phoneNumbers.value

</td><td id="user_phoneNumbers_value-SCIM-entry">

User's phone number.Data type: String

</td></tr><tr><td>

preferredLanguage

</td><td id="user_preferredLanguage-SCIM-entry">

User's preferred spoken and written language.Data type: String

</td></tr><tr><td>

timezone

</td><td id="user_timezone-SCIM-entry">

User's time zone.Data type: String

</td></tr><tr><td>

title

</td><td id="user_title-SCIM-entry">

User's title, such as CEO or President.Data type: String

</td></tr><tr><td>

userName

</td><td>

Required. Unique user name for the associated user. Data type: String

</td></tr><tr><td>

userType

</td><td id="user_userType-SCIM-entry">

User type. This value is used to identify the organization to user relationship.This can be any value, but typical values might include:

-   Contractor
-   Employee
-   Intern
-   Temp
-   External
-   Unknown

 Data type: String

</td></tr><tr><td>

Extended Schema

</td><td>

 

</td></tr><tr><td>

company

</td><td>

Details about the user's associated company.Data type: Object

 ```
"company": {
  "value": "String"
}
```

</td></tr><tr><td>

company.value

</td><td>

Required if company is included in post. Sys\_id of the company record. Data type: String

</td></tr><tr><td>

costCenter

</td><td>

Details about the user's associated cost center.Data type: Object

 ```
"costCenter": {
  "value": "String"
}
```

</td></tr><tr><td>

costCenter.value

</td><td>

Required if costCenter is included in post. Sys\_id of the cost center record. Data type: String

</td></tr><tr><td>

department

</td><td>

Details about the user's associated department.Data type: Object

 ```
"department": {
  "value": "String"
}
```

</td></tr><tr><td>

department.value

</td><td>

Required if department is included in post. Sys\_id of the department record. Data type: String

</td></tr><tr><td>

employeeNumber

</td><td id="user_employeeNumber-SCIM-entry">

Numeric or alphanumeric employee number.Data type: String

</td></tr><tr><td>

gender

</td><td id="user_gender-SCIM-entry">

Gender of the user, such as male or female.Data type: String

</td></tr><tr><td>

location

</td><td>

Details about the user's associated location.Data type: Object

 ```
"location": {
  "value": "String"
}
```

</td></tr><tr><td>

location.value

</td><td>

Required if location is included in post. Sys\_id of the location record. Data type: String

</td></tr><tr><td>

manager

</td><td>

Details about the user's associated manager.Data type: Object

 ```
"manager": {
  "value": "String"
}
```

</td></tr><tr><td>

manager.value

</td><td>

Required if manager is included in post. Sys\_id of the manager record. Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="Content_Type-SCIM-entry">

Data format of the request body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|201|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|409|User already exists. The **userName** parameter must be unique.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td id="d3411e1089">

Flag that indicates whether the associated user is active within the ServiceNow instance.Possible values:

-   true: User is active.
-   false: User is inactive.

 Data type: Boolean

</td></tr><tr><td>

addresses

</td><td id="d3411e1114">

Details of the user's current mailing address.Data type: Object

 ```
"addresses": {
  "country": "String",
  "locality": "String",
  "postalCode": "String",
  "region": "String",
  "streetAddress": "String",
  "type": "String"
}
```

</td></tr><tr><td>

addresses.country

</td><td id="d3411e1128">

Country name.Data type: String

</td></tr><tr><td>

addresses.locality

</td><td id="d3411e1139">

City or locality name.Data type: String

</td></tr><tr><td>

addresses.postalCode

</td><td id="d3411e1150">

Zip or postal code.Data type: String

</td></tr><tr><td>

addresses.region

</td><td id="d3411e1162">

State or region.Data type: String

</td></tr><tr><td>

addresses.streetAddress

</td><td id="d3411e1173">

Full street address. This can include the house number, street name, PO Box, and multi-line extended street address information.Data type: String

</td></tr><tr><td>

addresses.type

</td><td id="d3411e1184">

Type of address. Currently only supports `home`.Data type: String

</td></tr><tr><td>

displayName

</td><td id="d3411e1198">

User display name. This value is auto-generated by concatenating the **name** fields. Data type: String

</td></tr><tr><td>

emails

</td><td id="d3411e1212">

List of email accounts associated with the user.Data type: Array of Objects

 ```
"emails:" [
  {
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

emails.type

</td><td id="d3411e1226">

User email type. Currently only supports type of "work".Data type: String

</td></tr><tr><td>

emails.value

</td><td id="d3411e1238">

User's email address. This is a unique key for the associated user.Data type: String

</td></tr><tr><td>

errors

</td><td id="errors-SCIM-entry">

Response that describes any errors that may have occurred during processing the request.Data type: Object

 ```
"errors": {
  "details": "String",
  "schemas": "String",
  "scimType": "String",
  "status": "String"
}
```

</td></tr><tr><td>

errors.detail

</td><td id="errors_details-SCIM-entry">

Detailed error message on why the request failed.Data type: String

</td></tr><tr><td>

errors.scimType

</td><td id="errors_scimType-SCIM-entry">

SCIM error detail keyword.Data type: String

</td></tr><tr><td>

errors.schemas

</td><td id="errors_schemas-SCIM-entry">

URI of the SCIM Schemas used to process the error response.Data type: Array of Strings

</td></tr><tr><td>

errors.status

</td><td id="errors_status-SCIM-entry">

HTTP status code for the error response.Data type: String

</td></tr><tr><td>

externalId

</td><td id="d3411e1249">

Unique identifier assigned to the user by the entity provisioning it.Data type: String

</td></tr><tr><td>

groups

</td><td id="user_groups-SCIM-entry">

List of groups to which the user belongs, either through direct membership, nested groups, or dynamically calculated.Data type: Array of Objects

 ```
"groups": [
  {
    "display": "String",
    "type": "String",
    "value": "String",
    "$ref": "String"
  }
]
```

</td></tr><tr><td>

groups.display

</td><td id="user_groups_display-SCIM-entry">

Name of the associated group.Data type: String

</td></tr><tr><td>

groups.type

</td><td id="user_groups_type-SCIM-entry">

Type of group association, such as direct or indirect.Data type: String

</td></tr><tr><td>

groups.value

</td><td id="user_groups_value-SCIM-entry">

Sys\_id of an associated group record.Data type: String

</td></tr><tr><td>

groups.$ref

</td><td id="user_groups_ref-SCIM-entry">

URI of the associated group.Data type: String

</td></tr><tr><td>

id

</td><td id="user_id-SCIM-entry">

Sys\_id of the associated User record.Data type: String

</td></tr><tr><td>

meta

</td><td id="user_meta-SCIM-entry">

Metadata pertaining to the user.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": String",
  "resourceType": String"
}
```

</td></tr><tr><td>

meta.created

</td><td id="user_meta_created-SCIM-entry">

Date and time when the user record was created.Data type: String

</td></tr><tr><td>

meta.lastModified

</td><td id="user_meta_lastModified-SCIM-entry">

Date and time when the user record was last modified.Data type: String

</td></tr><tr><td>

meta.location

</td><td id="user_meta_location-SCIM-entry">

URI of the user being retrieved.Data type: String

</td></tr><tr><td>

meta.resourceType

</td><td id="user_meta_resourceType-SCIM-entry">

SCIM Users' resource type.Data type: String

</td></tr><tr><td>

name

</td><td id="d3411e1389">

User's name information.Data type: Object

 ```
"name": {
  "familyName": "String",
  "givenName": "String",
  "honorificPrefix": "String",
  "middleName": "String"
}
```

</td></tr><tr><td>

name.familyName

</td><td id="d3411e1403">

User's family or last name.Data type: String

</td></tr><tr><td>

name.givenName

</td><td id="d3411e1414">

User's given or first name.Data type: String

</td></tr><tr><td>

name.honorificPrefix

</td><td id="d3411e1425">

User's honorific name or title, such as Dr., Bishop, or Baron.Data type: String

</td></tr><tr><td>

name.middle

</td><td id="d3411e1436">

User's middle name.Data type: String

</td></tr><tr><td>

phoneNumbers

</td><td id="d3411e1448">

List of phone numbers associated with the user.Data type: Array of Objects

 ```
"phoneNumbers": [
  {
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

phoneNumbers.type

</td><td id="d3411e1462">

Type of phone number.Possible values:

 -   home
-   mobile
-   work

 Data type: String

</td></tr><tr><td>

phoneNumbers.value

</td><td id="d3411e1488">

User's phone number.Data type: String

</td></tr><tr><td>

preferredLanguage

</td><td id="d3411e1499">

User's preferred spoken and written language.Data type: String

</td></tr><tr><td>

schemas

</td><td id="user_schemas-SCIM-entry">

List of URIs of the SCIM User schemas used to process the request.Data type: Array of Strings

</td></tr><tr><td>

timezone

</td><td id="d3411e1521">

User's time zone.Data type: String

</td></tr><tr><td>

title

</td><td id="d3411e1533">

User's title, such as CEO or President.Data type: String

</td></tr><tr><td>

userName

</td><td id="user_userName-SCIM-entry">

Unique user name for the associated user. Data type: String

</td></tr><tr><td>

userType

</td><td id="d3411e1557">

User type. This value is used to identify the organization to user relationship.This can be any value, but typical values might include:

-   Contractor
-   Employee
-   Intern
-   Temp
-   External
-   Unknown

 Data type: String

</td></tr></tbody>
</table>### cURL request to POST user

This example shows how to POST the user Jack Sparrow to the User \[sys\_user\] table.

```
curl -X POST \
  https://instance-servicenow.com/api/now/scim/Users \
  -d '{
    "schemas": [
        "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User",
        "urn:ietf:params:scim:schemas:core:2.0:User"
    ],
    "externalId": "123456",
    "userName": "jack.sparrow",
    "name": {
        "familyName": "Sparrow",
        "givenName": "Jack"
    },
    "title": "Senior Developer",
    "preferredLanguage": "en",
    "timezone": "ET",
    "active": true,
    "emails": [
      {
        "value": "jack.sparrow@abc.com",
        "display": null,
        "type": "work",
        "primary": true
      }
    ],
    "phoneNumbers": [
      {
        "value": "9977553312",
        "type": "mobile",
        "primary": true
      }
    ]
}'
```

Response

```
{"schemas":
  [
    "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User",
    "urn:ietf:params:scim:schemas:core:2.0:User"
  ],
  "id":"d6287d7b1bbe3010593876a61a4bcbc3",
  "externalId":"123456",
  "meta":{
    "resourceType":"User",
    "created":"2021-10-01T16:46:48Z",
    "lastModified":"2021-10-01T16:46:48Z",
    "location":"https://instance-servicenow.com/api/now/scim/Users/d6287d7b1bbe3010593876a61a4bcbc3"
  },
  "userName":"jack.sparrow",
  "name":{
    "familyName":"Sparrow",
    "givenName":"Jack"
  },
  "displayName":"Jack Sparrow",
  "title":"Senior Developer",
  "preferredLanguage":"en",
  "timezone":"ET",
  "active":true,
  "emails":[
    {
      "value":"jack.sparrow@abc.com",
      "type":"work"
    }
  ],
  "phoneNumbers":[
    {
      "value":"9977553312",
      "type":"mobile"
    }
  ]
}
```

## SCIM - PUT /scim/Users/\{user\_id\}

Updates the specified user record in the User \[sys\_user\] table of a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Users/{user_id}`

Default URL: `/api/now/scim/Users/{user_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

user\_id

</td><td>

Sys\_id of the user record to update.

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td id="user_active-SCIM-entry">

Flag that indicates whether the associated user is active within the ServiceNow instance.Possible values:

-   true: User is active.
-   false: User is inactive.

 Data type: Boolean

</td></tr><tr><td>

addresses

</td><td id="user_addresses-SCIM-entry">

Details of the user's current mailing address.Data type: Object

 ```
"addresses": {
  "country": "String",
  "locality": "String",
  "postalCode": "String",
  "region": "String",
  "streetAddress": "String",
  "type": "String"
}
```

</td></tr><tr><td>

addresses.country

</td><td id="user_addresses_country-SCIM-entry">

Country name.Data type: String

</td></tr><tr><td>

addresses.locality

</td><td id="user_addresses_locality-SCIM-entry">

City or locality name.Data type: String

</td></tr><tr><td>

addresses.postalCode

</td><td id="user_addresses_postalCode-SCIM-entry">

Zip or postal code.Data type: String

</td></tr><tr><td>

addresses.region

</td><td id="user_addresses_region-SCIM-entry">

State or region.Data type: String

</td></tr><tr><td>

addresses.streetAddress

</td><td id="user_addresses_streetAddress-SCIM-entry">

Full street address. This can include the house number, street name, PO Box, and multi-line extended street address information.Data type: String

</td></tr><tr><td>

addresses.type

</td><td id="user_addresses_type-SCIM-entry">

Type of address. Currently only supports `home`.Data type: String

</td></tr><tr><td>

displayName

</td><td id="user_displayName-SCIM-entry">

User display name. This value is auto-generated by concatenating the **name** fields. Data type: String

</td></tr><tr><td>

emails

</td><td id="user_emails-SCIM-entry">

List of email accounts associated with the user.Data type: Array of Objects

 ```
"emails:" [
  {
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

emails.type

</td><td id="user_emails_type-SCIM-entry">

User email type. Currently only supports type of "work".Data type: String

</td></tr><tr><td>

emails.value

</td><td id="user_emails_value-SCIM-entry">

User's email address. This is a unique key for the associated user.Data type: String

</td></tr><tr><td>

externalId

</td><td id="user_emails_externalId-SCIM-entry">

Unique identifier assigned to the user by the entity provisioning it.Data type: String

</td></tr><tr><td>

name

</td><td id="user_name-SCIM-entry">

User's name information.Data type: Object

 ```
"name": {
  "familyName": "String",
  "givenName": "String",
  "honorificPrefix": "String",
  "middleName": "String"
}
```

</td></tr><tr><td>

name.familyName

</td><td id="user_name_familyName-SCIM-entry">

User's family or last name.Data type: String

</td></tr><tr><td>

name.givenName

</td><td id="user_name_givenName-SCIM-entry">

User's given or first name.Data type: String

</td></tr><tr><td>

name.honorificPrefix

</td><td id="user_name_honorificPrefix-SCIM-entry">

User's honorific name or title, such as Dr., Bishop, or Baron.Data type: String

</td></tr><tr><td>

name.middle

</td><td id="user_name_middle-SCIM-entry">

User's middle name.Data type: String

</td></tr><tr><td>

phoneNumbers

</td><td id="user_phoneNumbers-SCIM-entry">

List of phone numbers associated with the user.Data type: Array of Objects

 ```
"phoneNumbers": [
  {
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

phoneNumbers.type

</td><td id="user_phoneNumbers_type-SCIM-entry">

Type of phone number.Possible values:

 -   home
-   mobile
-   work

 Data type: String

</td></tr><tr><td>

phoneNumbers.value

</td><td id="user_phoneNumbers_value-SCIM-entry">

User's phone number.Data type: String

</td></tr><tr><td>

preferredLanguage

</td><td id="user_preferredLanguage-SCIM-entry">

User's preferred spoken and written language.Data type: String

</td></tr><tr><td>

timezone

</td><td id="user_timezone-SCIM-entry">

User's time zone.Data type: String

</td></tr><tr><td>

title

</td><td id="user_title-SCIM-entry">

User's title, such as CEO or President.Data type: String

</td></tr><tr><td>

userName

</td><td>

Required. Unique user name for the associated user. Data type: String

</td></tr><tr><td>

userType

</td><td id="user_userType-SCIM-entry">

User type. This value is used to identify the organization to user relationship.This can be any value, but typical values might include:

-   Contractor
-   Employee
-   Intern
-   Temp
-   External
-   Unknown

 Data type: String

</td></tr><tr><td>

Extended Schema

</td><td>

 

</td></tr><tr><td>

company

</td><td>

Details about the user's associated company.Data type: Object

 ```
"company": {
  "value": "String"
}
```

</td></tr><tr><td>

company.value

</td><td>

Required if company is included in post. Sys\_id of the company record. Data type: String

</td></tr><tr><td>

costCenter

</td><td>

Details about the user's associated cost center.Data type: Object

 ```
"costCenter": {
  "value": "String"
}
```

</td></tr><tr><td>

costCenter.value

</td><td>

Required if costCenter is included in post. Sys\_id of the cost center record. Data type: String

</td></tr><tr><td>

department

</td><td>

Details about the user's associated department.Data type: Object

 ```
"department": {
  "value": "String"
}
```

</td></tr><tr><td>

department.value

</td><td>

Required if department is included in post. Sys\_id of the department record. Data type: String

</td></tr><tr><td>

employeeNumber

</td><td id="user_employeeNumber-SCIM-entry">

Numeric or alphanumeric employee number.Data type: String

</td></tr><tr><td>

gender

</td><td id="user_gender-SCIM-entry">

Gender of the user, such as male or female.Data type: String

</td></tr><tr><td>

location

</td><td>

Details about the user's associated location.Data type: Object

 ```
"location": {
  "value": "String"
}
```

</td></tr><tr><td>

location.value

</td><td>

Required if location is included in post. Sys\_id of the location record. Data type: String

</td></tr><tr><td>

manager

</td><td>

Details about the user's associated manager.Data type: Object

 ```
"manager": {
  "value": "String"
}
```

</td></tr><tr><td>

manager.value

</td><td>

Required if manager is included in post. Sys\_id of the manager record. Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="Content_Type-SCIM-entry">

Data format of the request body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|404|Not found. The requested item wasn't found.|
|409|User already exists. The **userName** parameter must be unique.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_mjy_k1l_grb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td id="d3411e1089">

Flag that indicates whether the associated user is active within the ServiceNow instance.Possible values:

-   true: User is active.
-   false: User is inactive.

 Data type: Boolean

</td></tr><tr><td>

addresses

</td><td id="d3411e1114">

Details of the user's current mailing address.Data type: Object

 ```
"addresses": {
  "country": "String",
  "locality": "String",
  "postalCode": "String",
  "region": "String",
  "streetAddress": "String",
  "type": "String"
}
```

</td></tr><tr><td>

addresses.country

</td><td id="d3411e1128">

Country name.Data type: String

</td></tr><tr><td>

addresses.locality

</td><td id="d3411e1139">

City or locality name.Data type: String

</td></tr><tr><td>

addresses.postalCode

</td><td id="d3411e1150">

Zip or postal code.Data type: String

</td></tr><tr><td>

addresses.region

</td><td id="d3411e1162">

State or region.Data type: String

</td></tr><tr><td>

addresses.streetAddress

</td><td id="d3411e1173">

Full street address. This can include the house number, street name, PO Box, and multi-line extended street address information.Data type: String

</td></tr><tr><td>

addresses.type

</td><td id="d3411e1184">

Type of address. Currently only supports `home`.Data type: String

</td></tr><tr><td>

displayName

</td><td id="d3411e1198">

User display name. This value is auto-generated by concatenating the **name** fields. Data type: String

</td></tr><tr><td>

emails

</td><td id="d3411e1212">

List of email accounts associated with the user.Data type: Array of Objects

 ```
"emails:" [
  {
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

emails.type

</td><td id="d3411e1226">

User email type. Currently only supports type of "work".Data type: String

</td></tr><tr><td>

emails.value

</td><td id="d3411e1238">

User's email address. This is a unique key for the associated user.Data type: String

</td></tr><tr><td>

errors

</td><td id="errors-SCIM-entry">

Response that describes any errors that may have occurred during processing the request.Data type: Object

 ```
"errors": {
  "details": "String",
  "schemas": "String",
  "scimType": "String",
  "status": "String"
}
```

</td></tr><tr><td>

errors.detail

</td><td id="errors_details-SCIM-entry">

Detailed error message on why the request failed.Data type: String

</td></tr><tr><td>

errors.scimType

</td><td id="errors_scimType-SCIM-entry">

SCIM error detail keyword.Data type: String

</td></tr><tr><td>

errors.schemas

</td><td id="errors_schemas-SCIM-entry">

URI of the SCIM Schemas used to process the error response.Data type: Array of Strings

</td></tr><tr><td>

errors.status

</td><td id="errors_status-SCIM-entry">

HTTP status code for the error response.Data type: String

</td></tr><tr><td>

externalId

</td><td id="d3411e1249">

Unique identifier assigned to the user by the entity provisioning it.Data type: String

</td></tr><tr><td>

groups

</td><td id="user_groups-SCIM-entry">

List of groups to which the user belongs, either through direct membership, nested groups, or dynamically calculated.Data type: Array of Objects

 ```
"groups": [
  {
    "display": "String",
    "type": "String",
    "value": "String",
    "$ref": "String"
  }
]
```

</td></tr><tr><td>

groups.display

</td><td id="user_groups_display-SCIM-entry">

Name of the associated group.Data type: String

</td></tr><tr><td>

groups.type

</td><td id="user_groups_type-SCIM-entry">

Type of group association, such as direct or indirect.Data type: String

</td></tr><tr><td>

groups.value

</td><td id="user_groups_value-SCIM-entry">

Sys\_id of an associated group record.Data type: String

</td></tr><tr><td>

groups.$ref

</td><td id="user_groups_ref-SCIM-entry">

URI of the associated group.Data type: String

</td></tr><tr><td>

id

</td><td id="user_id-SCIM-entry">

Sys\_id of the associated User record.Data type: String

</td></tr><tr><td>

meta

</td><td id="user_meta-SCIM-entry">

Metadata pertaining to the user.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": String",
  "resourceType": String"
}
```

</td></tr><tr><td>

meta.created

</td><td id="user_meta_created-SCIM-entry">

Date and time when the user record was created.Data type: String

</td></tr><tr><td>

meta.lastModified

</td><td id="user_meta_lastModified-SCIM-entry">

Date and time when the user record was last modified.Data type: String

</td></tr><tr><td>

meta.location

</td><td id="user_meta_location-SCIM-entry">

URI of the user being retrieved.Data type: String

</td></tr><tr><td>

meta.resourceType

</td><td id="user_meta_resourceType-SCIM-entry">

SCIM Users' resource type.Data type: String

</td></tr><tr><td>

name

</td><td id="d3411e1389">

User's name information.Data type: Object

 ```
"name": {
  "familyName": "String",
  "givenName": "String",
  "honorificPrefix": "String",
  "middleName": "String"
}
```

</td></tr><tr><td>

name.familyName

</td><td id="d3411e1403">

User's family or last name.Data type: String

</td></tr><tr><td>

name.givenName

</td><td id="d3411e1414">

User's given or first name.Data type: String

</td></tr><tr><td>

name.honorificPrefix

</td><td id="d3411e1425">

User's honorific name or title, such as Dr., Bishop, or Baron.Data type: String

</td></tr><tr><td>

name.middle

</td><td id="d3411e1436">

User's middle name.Data type: String

</td></tr><tr><td>

phoneNumbers

</td><td id="d3411e1448">

List of phone numbers associated with the user.Data type: Array of Objects

 ```
"phoneNumbers": [
  {
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

phoneNumbers.type

</td><td id="d3411e1462">

Type of phone number.Possible values:

 -   home
-   mobile
-   work

 Data type: String

</td></tr><tr><td>

phoneNumbers.value

</td><td id="d3411e1488">

User's phone number.Data type: String

</td></tr><tr><td>

preferredLanguage

</td><td id="d3411e1499">

User's preferred spoken and written language.Data type: String

</td></tr><tr><td>

schemas

</td><td id="user_schemas-SCIM-entry">

List of URIs of the SCIM User schemas used to process the request.Data type: Array of Strings

</td></tr><tr><td>

timezone

</td><td id="d3411e1521">

User's time zone.Data type: String

</td></tr><tr><td>

title

</td><td id="d3411e1533">

User's title, such as CEO or President.Data type: String

</td></tr><tr><td>

userName

</td><td id="user_userName-SCIM-entry">

Unique user name for the associated user. Data type: String

</td></tr><tr><td>

userType

</td><td id="d3411e1557">

User type. This value is used to identify the organization to user relationship.This can be any value, but typical values might include:

-   Contractor
-   Employee
-   Intern
-   Temp
-   External
-   Unknown

 Data type: String

</td></tr></tbody>
</table>### Extension parameters returned

<table id="id_hmw_fjk_grb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="user_company-SCIM-row"><td>

company

</td><td id="user_company-SCIM-entry">

Details about the user's associated company.Data type: Object

 ```
"company": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_company_display-SCIM-row"><td>

company.display

</td><td id="user_company_display-SCIM-entry">

Name of the company.Data type: String

</td></tr><tr id="user_company_value-SCIM-row"><td>

company.value

</td><td id="user_company_value-SCIM-entry">

Sys\_id of the company record. Data type: String

</td></tr><tr id="user_company_ref-SCIM-row"><td>

company.$ref

</td><td id="user_company_ref-SCIM-entry">

Reference URI for the company.Data type: String

</td></tr><tr id="user_costCenter-SCIM-row"><td>

costCenter

</td><td id="user_costCenter-SCIM-entry">

Details about the user's associated cost center.Data type: Object

 ```
"costCenter": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_costCenter_display-SCIM-row"><td>

costCenter.display

</td><td id="user_costCenter_display-SCIM-entry">

Name of the cost center.Data type: String

</td></tr><tr id="user_costCenter_value-SCIM-row"><td>

costCenter.value

</td><td id="user_costCenter_value-SCIM-entry">

Sys\_id of the cost center record. Data type: String

</td></tr><tr id="user_costCenter_ref-SCIM-row"><td>

costCenter.$ref

</td><td id="user_costCenter_ref-SCIM-entry">

Reference URI for the cost center.Data type: String

</td></tr><tr id="user_department-SCIM-row"><td>

department

</td><td id="user_department-SCIM-entry">

Details about the user's associated department.Data type: Object

 ```
"department": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_department_display-SCIM-row"><td>

department.display

</td><td id="user_department_display-SCIM-entry">

Name of the department.Data type: String

</td></tr><tr id="user_department_value-SCIM-row"><td>

department.value

</td><td id="user_department_value-SCIM-entry">

Sys\_id of the department record. Data type: String

</td></tr><tr id="user_department_ref-SCIM-row"><td>

department.$ref

</td><td id="user_department_ref-SCIM-entry">

Reference URI for the department.Data type: String

</td></tr><tr id="user_employeeNumber-SCIM-row"><td>

employeeNumber

</td><td id="d3411e1767">

Numeric or alphanumeric employee number.Data type: String

</td></tr><tr id="user_gender-SCIM-row"><td>

gender

</td><td id="d3411e1778">

Gender of the user, such as male or female.Data type: String

</td></tr><tr id="user_location-SCIM-row"><td>

location

</td><td id="user_location-SCIM-entry">

Details about the user's associated location.Data type: Object

 ```
"location": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_location_display-SCIM-row"><td>

location.display

</td><td id="user_location_display-SCIM-entry">

Name of the location.Data type: String

</td></tr><tr id="user_location_value-SCIM-row"><td>

location.value

</td><td id="user_location_value-SCIM-entry">

Sys\_id of the location record. Data type: String

</td></tr><tr id="user_location_ref-SCIM-row"><td>

location.$ref

</td><td id="user_location_ref-SCIM-entry">

Reference URI for the location.Data type: String

</td></tr><tr id="user_manager-SCIM-row"><td>

manager

</td><td id="user_manager-SCIM-entry">

Details about the user's associated manager.Data type: Object

 ```
"manager": {
  "display": "String",
  "value": "String",
  "$ref": "String"
}
```

</td></tr><tr id="user_manager_display-SCIM-row"><td>

manager.display

</td><td id="user_manager_display-SCIM-entry">

Name of the manager.Data type: String

</td></tr><tr id="user_manager_value-SCIM-row"><td>

manager.value

</td><td id="user_manager_value-SCIM-entry">

Sys\_id of the manager record. Data type: String

</td></tr><tr id="user_manager_ref-SCIM-row"><td>

manager.$ref

</td><td id="user_manager_ref-SCIM-entry">

Reference URI for the manager.Data type: String

</td></tr></tbody>
</table>### cURL request to update user information using PUT

This example shows how to update the information of an existing user using the PUT endpoint.

```
curl -X PUT \
  https://instance-servicenow.com/api/now/scim/Users/cdfef423e0423010f8778ac6d674f5ae \
  -d '{
  "schemas": [
    "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User",
    "urn:ietf:params:scim:schemas:core:2.0:User"
  ],
  "externalId": "123457",
  "userName": "john.Doe",
  "name": {
    "familyName": "Doe",
    "givenName": "John"
  },
  "title": "Sir",
  "preferredLanguage": "en",
  "timezone": "ET",
  "active": true,
  "emails": [
    {
      "value": "john.doe@abc.com",
      "display": null,
      "type": "work",
      "primary": true
    }
  ],
  "phoneNumbers": [
    {
      "value": "9977553312",
      "type": "mobile",
      "primary": true
    }
  ],
  "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User": {
    "gender": "Male",
    "employeeNumber" : "13453",
    "location" : {
      "value" : "0002c0a93790200044e0bfc8bcbe5df5"
    },
    "company" : {
      "value" : "81fd65ecac1d55eb42a426568fc87a63"
    },
    "costCenter" : {
      "value" : "7fb1cc99c0a80a6d30c04574d14c0acf"
    },
    "department" : {
      "value":"221db0edc611228401760aec06c9d929"
    }
  }
}'
```

Response

```
{
  "schemas": [
    "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User",
    "urn:ietf:params:scim:schemas:core:2.0:User"
  ],
  "id": "b7c5015f778330102e8cc5179e5a9992",
  "externalId": "123457",
  "meta": {
    "resourceType": "User",
    "created": "2021-10-12T10:05:32Z",
    "lastModified": "2021-10-12T10:08:04Z",
    "location":
      "http://instance-servicenow.com/api/now/scim/Users/b7c5015f778330102e8cc5179e5a9992"
  },
  "userName": "john.doe",
  "name": {
    "familyName": "Doe",
    "givenName": "John"
  },
  "displayName": "John Doe",
  "title": "Sir",
  "preferredLanguage": "en",
  "timezone": "ET",
  "active": true,
  "emails": [
    {
      "value": "tony.stark@abc.com",
      "type": "work"
    }
  ],
  "phoneNumbers": [
    {
      "value": "9977553312",
      "type": "mobile"
    }
  ],
  "urn:ietf:params:scim:schemas:extension:servicenow:2.0:User": {
    "employeeNumber": "13453",
    "gender": "Male",
    "costCenter": {
      "value": "7fb1cc99c0a80a6d30c04574d14c0acf",
      "name": "Sales",
      "$ref":
       "http://instance-servicenow.com/api/now/scim/CostCenters/7fb1cc99c0a80a6d30c04574d14c0acf"
    },
    "company": {
      "value": "81fd65ecac1d55eb42a426568fc87a63",
      "name": "ACME Japan",
      "$ref":
       "http://instance-servicenow.com/api/now/scim/Companies/81fd65ecac1d55eb42a426568fc87a63"
    },
    "department": {
      "value": "221db0edc611228401760aec06c9d929",
      "name": "Sales",
      "$ref":
        "http://instance-servicenow.com/api/now/scim/Departments/221db0edc611228401760aec06c9d929"
    },
    "manager": {
      "value": "7027fda8773230102e8cc5179e5a99ea",
      "displayName": "Jack Sparrow",
      "$ref":
        "http://instance-servicenow.com/api/now/scim/Users/7027fda8773230102e8cc5179e5a99ea"
    },
    "location": {
      "value": "0002c0a93790200044e0bfc8bcbe5df5",
      "name": "2-10-1 Yurakucho, Chiyoda-ku, Tokyo",
      "$ref":
        "http://instance-servicenow.com/api/now/scim/Locations/0002c0a93790200044e0bfc8bcbe5df5"
    }
  }
}
```

## SCIM - GET /scim/ResourceTypes

Retrieves information about all System for Cross-domain Identity Management \(SCIM\) resource types supported by the associated ServiceNow instance.

This is a public endpoint and does not require any roles to access.

### URL format

Versioned URL: `/api/now/{api_version}/scim/ResourceTypes`

Default URL: `/api/now/scim/ResourceTypes`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON\)

<table id="id_avz_rp3_3rb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

itemsPerPage

</td><td id="itemsPerPage-SCIM-entry">

Number of records returned in the return results.Data type: Number

</td></tr><tr><td>

Resources

</td><td>

List of available resource types.Data type: Array of Objects

 ```
"Resources": [
  {
    "description": "String",
    "endpoint": "String",
    "id": "String",
    "meta": {Object},
    "name": "String",
    "schema": "String"
    "schemas": [Array],
    "schemaExtensions": [Array]
  }
]
```

</td></tr><tr><td>

Resources.description

</td><td id="description-SCIM-entry">

Brief description of the resource type.Data type: String

</td></tr><tr><td>

Resources.endpoint

</td><td id="endpoint-SCIM-entry">

Name of the HTTP-addressable endpoint relative to the Base URL of the service provider, for example "Users".Data type: String

</td></tr><tr><td>

Resources.id

</td><td id="id-SCIM-entry">

Unique identifier for the resource. Use this attribute when calling GET /scim/ResourceType/\{resource\_id\} endpoint.Data type: String

</td></tr><tr><td>

Resources.meta

</td><td id="meta-SCIM-entry">

Information that further describes the associated resource.Data type: Object

 ```
"metadata": {
  "location": "String",
  "resourceType": "String"
}
```

</td></tr><tr><td>

Resources.meta.location

</td><td id="meta_location-SCIM-entry">

URI of the associated resource type on the associated ServiceNow instance.Data type: String

</td></tr><tr><td>

Resources.meta.resourceType

</td><td id="meta_resourceType-SCIM-entry">

Always "ResourceType".Data type: String

</td></tr><tr><td>

Resources.name

</td><td id="name-SCIM-entry">

Name of the resource type, such as User or Group.Data type: String

</td></tr><tr><td>

Resources.schema

</td><td id="schema-SCIM-entry">

Resource type's primary/base schema URI. For example: `"urn:ietf:params:scim:schemas:core:2.0:User"`.Data type: String

</td></tr><tr><td>

Resources.schemas

</td><td id="schemas-SCIM-entry">

Schema used to process the `/ResourceType` request. For example: `"urn:ietf:params:scim:schemas:core:2.0:ResourceType"`.Data type: String

</td></tr><tr><td>

Resources.schemaExtensions

</td><td id="schemaExtensions-SCIM-entry">

List of schema extensions that apply to the associated resource type. For example: `"urn:ietf:params:scim:schemas:extension: servicenow:2.0:User"`.Data type: Array of Object

 ```
"schemaExtensions": {
  "required": Boolean,
  "schema": "String"
}
```

</td></tr><tr><td>

Resources.schemaExtensions.required

</td><td id="schemaExtensions_required-SCIM-entry">

Flag that indicates whether the schema extension is required for the resource type.Possible values:

-   true: A resource of this type must include this schema extension and also include any attributes declared as required in this schema extension.
-   false: A resource of this type may omit this schema extension.

 Data type: Boolean

</td></tr><tr><td>

Resources.schemaExtensions.schema

</td><td id="schemaExtensions_schema-SCIM-entry">

URI of an extended schema. For example: `"urn:ietf:params:scim:schemas:extension:servicenow: 2.0:User"`.Data type: String

</td></tr><tr><td>

schemas

</td><td id="schemas2-SCIM-entry">

Schema used to process the list response to the request. For example: `"urn:ietf:params:scim:api:messages:2.0:ListResponse"` Data type: String

</td></tr><tr><td>

startIndex

</td><td id="startIndex-SCIM-entry">

One-based index into the Resource table at which records were retrieved. Data type: String

</td></tr><tr><td>

totalResults

</td><td id="totalResults-SCIM-entry">

Total number of records that match the request.Data type: Number

</td></tr></tbody>
</table>### cURL request

The following example shows how to obtain the SCIM resource types supported by a ServiceNow instance.

```
curl "https://instance-servicenow.com/api/now/scim/ResourceTypes \
--request GET \
--header "Accept:application/scim+json" \
```

Response

```
{
  "schemas":[
    "urn:ietf:params:scim:api:messages:2.0:ListResponse"
  ],
  "totalResults":6,
  "Resources":[
    {
      "schemas":[
        "urn:ietf:params:scim:schemas:core:2.0:ResourceType"
      ],
      "id":"User",
      "name":"User",
      "description":"User Account",
      "endpoint":"/Users",
      "schema":"urn:ietf:params:scim:schemas:core:2.0:User",
      "schemaExtensions":[
        {
          "schema":"urn:ietf:params:scim:schemas:extension:enterprise:2.0:User",
          "required":false
        },
        {
          "schema":"urn:ietf:params:scim:schemas:extension:servicenow:2.0:User",
          "required":false
        }
      ],
      "meta":{
        "resourceType":"ResourceType",
        "location":"https://instance-servicenow.com/api/now/scim/ResourceTypes/User"
      }
    },
    {
      "schemas":[
        "urn:ietf:params:scim:schemas:core:2.0:ResourceType"
      ],
      "id":"Group",
      "name":"Group",
      "description":"Group",
      "endpoint":"/Groups",
      "schema":"urn:ietf:params:scim:schemas:core:2.0:Group",
      "meta":{
        "resourceType":"ResourceType",
        "location":"https://instance-servicenow.service-now.com/api/now/scim/ResourceTypes/Group"
      }
    },
    {
      "schemas":[
        "urn:ietf:params:scim:schemas:core:2.0:ResourceType"
      ],
      "id":"Company",
      "name":"Company",
      "description":"Company",
      "endpoint":"/Companies",
      "schema":"urn:ietf:params:scim:schemas:custom:servicenow:2.0:Company",
      "meta":{
        "resourceType":"ResourceType",
        "location":"https://instance-servicenow.com/api/now/scim/ResourceTypes/Company"
      }
    },
    {
      "schemas":[
        "urn:ietf:params:scim:schemas:core:2.0:ResourceType"
      ],
      "id":"Department",
      "name":"Department",
      "description":"Department",
      "endpoint":"/Departments",
      "schema":"urn:ietf:params:scim:schemas:custom:servicenow:2.0:Department",
      "meta":{
        "resourceType":"ResourceType",
        "location":"https://instance-servicenow.com/api/now/scim/ResourceTypes/Department"
      }
    },
    {
      "schemas":[
        "urn:ietf:params:scim:schemas:core:2.0:ResourceType"
      ],
      "id":"CostCenter",
      "name":"CostCenter",
      "description":"CostCenter",
      "endpoint":"/CostCenters",
      "schema":"urn:ietf:params:scim:schemas:custom:servicenow:2.0:CostCenter",
      "meta":{
        "resourceType":"ResourceType",
        "location":"https://instance-servicenow.com/api/now/scim/ResourceTypes/CostCenter"
      }
    },
    {
      "schemas":[
        "urn:ietf:params:scim:schemas:core:2.0:ResourceType"
      ],
      "id":"Location",
      "name":"Location",
      "description":"Location",
      "endpoint":"/Locations",
      "schema":"urn:ietf:params:scim:schemas:custom:servicenow:2.0:Location",
      "meta":{
        "resourceType":"ResourceType",
        "location":"https://instance-servicenow.com/api/now/scim/ResourceTypes/Location"
      }
    }
  ],
  "startIndex":1,
  "itemsPerPage":6
}
```

## SCIM - GET /scim/ResourceTypes/\{ResourceName\}

Retrieves information about the specified System for Cross-domain Identity Management \(SCIM\) resource type.

This is a public endpoint and does not require any roles to access.

### URL format

Versioned URL: `/api/now/{api_version}/scim/ResourceTypes/{ResourceName}`

Default URL: `/api/now/scim/ResourceTypes/{ResourceName}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

ResourceName

</td><td>

Unique ID of the resource type to retrieve.Valid values:

-   Company
-   CostCenter
-   Department
-   Group
-   Location
-   User

 Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON\)

<table id="id_avz_rp3_3rb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Brief description of the resource type.Data type: String

</td></tr><tr><td>

endpoint

</td><td>

Name of the HTTP-addressable endpoint relative to the Base URL of the service provider, for example "Companies".Data type: String

</td></tr><tr><td>

id

</td><td>

Unique identifier for the resource. Use this attribute when calling GET /scim/ResourceType/\{resource\_id\} endpoint.Data type: String

</td></tr><tr><td>

meta

</td><td>

Information that further describes the associated resource.Data type: Object

 ```
"metadata": {
  "location": "String",
  "resourceType": "String"
}
```

</td></tr><tr><td>

meta.location

</td><td>

URI of the associated resource type on the associated ServiceNow instance.Data type: String

</td></tr><tr><td>

meta.resourceType

</td><td>

Always "ResourceType".Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the resource type, such as User or Group.Data type: String

</td></tr><tr><td>

schema

</td><td>

Resource type's primary/base schema URI. For example: `"urn:ietf:params:scim:schemas:core:2.0:User"`.Data type: String

</td></tr><tr><td>

schemas

</td><td>

Schema used to process the `/ResourceType` request. For example: `"urn:ietf:params:scim:schemas:core:2.0:ResourceType"`.Data type: String

</td></tr><tr><td>

schemaExtensions

</td><td>

List of schema extensions that apply to the associated resource type. For example: `"urn:ietf:params:scim:schemas:extension: servicenow:2.0:User"`.Data type: Array of Object

 ```
"schemaExtensions": {
  "required": Boolean,
  "schema": "String"
}
```

</td></tr><tr><td>

schemaExtensions.required

</td><td>

Flag that indicates whether the schema extension is required for the resource type.Possible values:

-   true: A resource of this type must include this schema extension and also include any attributes declared as required in this schema extension.
-   false: A resource of this type may omit this schema extension.

 Data type: Boolean

</td></tr><tr><td>

schemaExtensions.schema

</td><td>

URI of an extended schema. For example: `"urn:ietf:params:scim:schemas:extension:servicenow: 2.0:User"`.Data type: String

</td></tr><tr><td>

schemas

</td><td>

Schema used to process the list response to the request. For example: `"urn:ietf:params:scim:api:messages:2.0:ListResponse"` Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to obtain the User SCIM resource type from a ServiceNow instance.

```
curl "https://instance-servicenow.com/api/now/scim/ResourceTypes/"User" \
--request GET \
--header "Accept:application/scim+json" \
```

Response

```
{
  "schemas":[
    "urn:ietf:params:scim:schemas:core:2.0:ResourceType"
  ],
  "id":"User",
  "name":"User",
  "description":"User Account",
  "endpoint":"/Users",
  "schema":"urn:ietf:params:scim:schemas:core:2.0:User",
  "schemaExtensions":[
    {
      "schema":"urn:ietf:params:scim:schemas:extension:servicenow:2.0:User",
      "required":false
    },
    {
      "schema":"urn:ietf:params:scim:schemas:extension:enterprise:2.0:User",
      "required":false
    }
  ],
  "meta":{
    "resourceType":"ResourceType",
    "location":"https://instance-servicenow.com/api/now/scim/ResourceTypes/User"
  }
}
```

## SCIM - GET /scim/Schemas

Retrieves information about all System for Cross-domain Identity Management \(SCIM\) resource schemas supported by a ServiceNow instance. These schemas define the attributes available for each resource type.

This is a public endpoint and does not require any roles to access.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Schemas`

Default URL: `/api/now/scim/Schemas`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON\)

|Name|Description|
|----|-----------|
|Standard RFC7643 return results|Method returns results in compliance with the RFC7643 standard. For details see [Schema Definition](https://datatracker.ietf.org/doc/html/rfc7643#section-7) in the RFC7643 specification.|

### cURL request

The following example shows how to obtain the SCIM schemas supported by a ServiceNow instance.

```
curl "https://instance-servicenow.com/api/now/scim/Schemas \
--request GET \
--header "Accept:application/scim+json" \
```

Response

```
{
  "schemas":[
    "urn:ietf:params:scim:api:messages:2.0:ListResponse"
  ],
  "totalResults":8,
  "Resources":[
    {
      "schemas":[
        "urn:ietf:params:scim:schemas:core:2.0:Schema"
      ],
      "id":"urn:ietf:params:scim:schemas:core:2.0:User",
      "name":"User",
      "description":"User Account",
      "attributes":[
        {
          "name":"active",
          "type":"boolean",
          "multiValued":false,
          "description":"A Boolean value indicating the User's administrative status.",
          "required":false,
          "caseExact":true,
          "mutability":"readWrite",
          "returned":"default",
          "uniqueness":"none"
        },
        {
          "name":"addresses",
          "type":"complex",
          "subAttributes":[
            {
              "name":"country",
              "type":"string",
              "multiValued":false,
              "description":"The country name component.",
              "required":false,
              "caseExact":false,
              "mutability":"readWrite",
              "returned":"default",
              "uniqueness":"none"
            },
            {
              "name":"formatted",
              "type":"string",
              "multiValued":false,
              "description":"The full mailing address, formatted for display or use with a mailing label. This attribute MAY contain newlines.",
              "required":false,
              "caseExact":false,
              "mutability":"readWrite",
              "returned":"default",
              "uniqueness":"none"
            },
            {
              "name":"locality",
              "type":"string",
              "multiValued":false,
              "description":"The city or locality component.",
              "required":false,
              "caseExact":false,
              "mutability":"readWrite",
              "returned":"default",
              "uniqueness":"none"
            },
            {
              "name":"postalCode",
              "type":"string",
              "multiValued":false,
              "description":"The zipcode or postal code component.",
              "required":false,
              "caseExact":false,
              "mutability":"readWrite",
              "returned":"default",
              "uniqueness":"none"
            },
            {
              "name":"primary",
              "type":"boolean",
              "multiValued":false,
              "description":"A Boolean value indicating the 'primary' or 
                preferred attribute value for this attribute, e.g., the preferred address. 
                The primary attribute value 'true' MUST appear no more than once.",
              "required":false,
              "caseExact":true,
              "mutability":"readWrite",
              "returned":"default",
              "uniqueness":"none"
            },
            {
              "name":"region",
              "type":"string",
              "multiValued":false,
              "description":"The state or region component.",
              "required":false,
              "caseExact":false,
              "mutability":"readWrite",
              "returned":"default",
              "uniqueness":"none"
            },
            {
              "name":"streetAddress",
              "type":"string",
              "multiValued":false,
              "description":"The full street address component, which may include house number, 
                street name, PO BOX, and multi-line extended street address information. This 
                attribute MAY contain newlines.",
              "required":false,
              "caseExact":false,
              "mutability":"readWrite",
              "returned":"default",
              "uniqueness":"none"
            },
            {
              "name":"type",
              "type":"string",
              "multiValued":false,
              "description":"A label indicating the attribute's function; e.g., 'work' or 'home'.",
              "required":false,
              "canonicalValues":["other","work","home"],
              "caseExact":false,
              "mutability":"readWrite",
              "returned":"default",
              "uniqueness":"none"
            }
          ],
          "multiValued":true,
          "description":"Physical mailing addresses for this User.",
          "required":false,
          "caseExact":true,
          "mutability":"readWrite",
          "returned":"default",
          "uniqueness":"none"
        },
.
.
.
      {
        "schemas":[
          "urn:ietf:params:scim:schemas:core:2.0:Schema"
        ],
        "id":"urn:ietf:params:scim:schemas:custom:servicenow:2.0:Department",
        "name":"Department",
        "description":"Department",
        "attributes":[
          {
            "name":"name",
            "type":"string",
            "multiValued":false,
            "description":"The name of the department.",
            "required":false,
            "caseExact":false,
            "mutability":"readOnly",
            "returned":"default",
            "uniqueness":"none"
          }
        ],
        "meta":{
          "resourceType":"Schema",
          "location":"https://instance-servicenow.com/api/now/scim/Schemas/urn:ietf:params:scim:schemas:custom:servicenow:2.0:Department"
        }
      },
      {
        "schemas":[
          "urn:ietf:params:scim:schemas:core:2.0:Schema"
        ],
        "id":"urn:ietf:params:scim:schemas:custom:servicenow:2.0:CostCenter",
        "name":"CostCenter",
        "description":"CostCenter",
        "attributes":[
          {
            "name":"name",
            "type":"string",
            "multiValued":false,
            "description":"The name of the cost center.",
            "required":false,
            "caseExact":false,
            "mutability":"readOnly",
            "returned":"default",
            "uniqueness":"none"
          }
        ],
        "meta":
          {
            "resourceType":"Schema",
            "location":"https://instance.servicenow.com/api/now/scim/Schemas/urn:ietf:params:scim:schemas:custom:servicenow:2.0:CostCenter"
         }
        },
        {
          "schemas":[
            "urn:ietf:params:scim:schemas:core:2.0:Schema"
          ],
        "id":"urn:ietf:params:scim:schemas:custom:servicenow:2.0:Location",
        "name":"Location",
        "description":"Location",
        "attributes":[
          {
            "name":"name",
            "type":"string",
            "multiValued":false,
            "description":"The location name.",
            "required":false,
            "caseExact":false,
            "mutability":"readOnly",
            "returned":"default",
            "uniqueness":"none"
          }
        ],
        "meta":{
          "resourceType":"Schema",
          "location":"https://instance.servicenow.com/api/now/scim/Schemas/urn:ietf:params:scim:schemas:custom:servicenow:2.0:Location"
        }
      }
    ],
    "startIndex":1,
  "itemsPerPage":8
}
```

## SCIM - GET /scim/Schemas/\{SchemaName\}

Retrieves information about the specified System for Cross-domain Identity Management \(SCIM\) resource schemas supported by a ServiceNow instance. These schemas define the attributes available for each resource type.

This is a public endpoint and does not require any roles to access.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Schemas/{SchemaName}`

Default URL: `/api/now/scim/Schemas/{SchemaName}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

SchemaName

</td><td>

URI of the resource schema to return.Valid values:

-   urn:ietf:params:scim:schemas:core:2.0:User
-   urn:ietf:params:scim:schemas:extension: enterprise:2.0:User
-   urn:ietf:params:scim:schemas:extension: servicenow:2.0:User
-   urn:ietf:params:scim:schemas:core:2.0:Group
-   urn:ietf:params:scim:schemas:custom: servicenow:2.0:Company
-   urn:ietf:params:scim:schemas:custom: servicenow:2.0:Department
-   urn:ietf:params:scim:schemas:custom: servicenow:2.0:CostCenter
-   urn:ietf:params:scim:schemas:custom: servicenow:2.0:Location

 Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON\)

|Name|Description|
|----|-----------|
|Standard RFC7643 return results|Method returns results in compliance with the RFC7643 standard. For details see [Schema Definition](https://datatracker.ietf.org/doc/html/rfc7643#section-7) in the RFC7643 specification.|

### cURL request

The following example shows how to obtain the core Group SCIM schema from a ServiceNow instance.

```
curl "https://instance-servicenow.com/api/now/scim/Schemas/"urn:ietf:params:scim:schemas:core:2.0:Group" \
--request GET \
--header "Accept:application/scim+json" \
```

Response

```
{
  "schemas":[
    "urn:ietf:params:scim:schemas:core:2.0:Schema"
  ],
  "id":"urn:ietf:params:scim:schemas:core:2.0:Group",
  "name":"Group",
  "description":"Group",
  "attributes":[
    {
      "name":"displayName",
      "type":"string",
      "multiValued":false,
      "description":"A human-readable name for the Group.",
      "required":true,
      "caseExact":false,
      "mutability":"readWrite",
      "returned":"default",
      "uniqueness":"none"
    },
    {
      "name":"members",
      "type":"complex",
      "subAttributes":[
        {
          "name":"display",
          "type":"string",
          "multiValued":false,
          "description":"A human readable name, primarily used for display purposes.",
          "required":false,
          "caseExact":false,
          "mutability":"immutable",
          "returned":"default",
          "uniqueness":"none"
        },
        {
          "name":"value",
          "type":"string",
          "multiValued":false,
          "description":"The identifier of a group member.",
          "required":true,
          "caseExact":false,
          "mutability":"immutable",
          "returned":"default",
          "uniqueness":"none"
        },
        {
          "name":"$ref",
          "type":"reference",
          "multiValued":false,
          "description":"The URI of the member resource.",
          "required":false,
          "caseExact":true,
          "mutability":"immutable",
          "returned":"default",
          "uniqueness":"none",
          "referenceTypes":["Group","User"]
        }
      ],
      "multiValued":true,
      "description":"A list of members of the Group.",
      "required":false,
      "caseExact":true,
      "mutability":"readWrite",
      "returned":"default",
      "uniqueness":"none"
    }
  ],
  "meta":{
    "resourceType":"Schema",
    "location":"https://instance-servicenow.com/api/now/scim/Schemas/urn:ietf:params:scim:schemas:core:2.0:Group"
  }
}
```

## SCIM - GET /scim/ServiceProviderConfig

Returns the configuration metadata to use to obtain information about the service capabilities, configurations, schemas, and resource types for the System for Cross-domain Identity Management \(SCIM\) endpoints available within a ServiceNow instance.

This is a public endpoint and does not require any roles to access.

### URL format

Versioned URL: `/api/now/{api_version}/scim/ServiceProviderConfig`

Default URL: `/api/now/scim/ServiceProviderConfig`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON\)

|Name|Description|
|----|-----------|
|Standard RFC7643 return results|Method returns results in compliance with the RFC7643 standard. For details see [Service Provider Configuration Schema](https://datatracker.ietf.org/doc/html/rfc7643#section-5) in the RFC7643 specification.|

### cURL request

The following example shows how to obtain the SCIM configuration metadata for a ServiceNow instance.

```
curl "https://instance-servicenow.com/api/now/scim/ServiceProviderConfig \
--request GET \
--header "Accept:application/scim+json" \
```

Response

```
{
  "schemas": [
    "urn:ietf:params:scim:schemas:core:2.0:ServiceProviderConfig"
  ],
  "patch": {
    "supported": true
  },
  "bulk": {
    "supported": false,
    "maxOperations": 0,
    "maxPayloadSize": 1000000
  },
  "filter": {
    "supported": true,
    "maxResults": 500
  },
  "changePassword": {
    "supported": false
  },
  "sort": {
    "supported": false
  },
  "etag": {
    "supported": false
  },
  "authenticationSchemes": [
    {
      "name": "OAuth 2.0 Bearer Token",
      "description": "The OAuth 2.0 Bearer Token Authentication scheme. OAuth
        enables clients to access protected resources by obtaining an access token, which is
        defined in RFC 6750 as \"a string representing an access authorization issued to the
        client\", rather than using the resource owner's credentials directly.",
      "specUri": "http://tools.ietf.org/html/rfc6750",
      "type": "oauthbearertoken",
      "primary": true
    }
  ]
}
```

## SCIM - GET /scim/Companies

Returns one or more company records from the Company \[core\_company\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

**Note:** A query that does not return any matches returns success \(HTTP status code 200\) with **totalResults** set to 0.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Companies`

Default URL: `/api/now/scim/Companies`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

count

</td><td id="count-SCIM-entry">

Number of records to return. A negative value is interpreted as zero.Data type: Number

 Maximum: 500 - A value greater than this results in a bad request error.

 Default: 10

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr><tr><td>

filter

</td><td>

Filter expression to apply to the return results. Field filters are expressed as `<field_name> <operator> <"value">`. Refer to [RFC7644](https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2) for a list of the valid operators. **Note:** The `NOT` operator is not supported by this method.

 For example, to filter for all companies whose name starts with "Acme", enter `displayName SW "Acme"`.

 To specify more than one field filter, concatenate the filters using the `AND` operand. For example, to filter for all companies whose name starts with "Acme" and were last modified before October 3, 2021, enter `displayName SW "Acme" AND meta.lastModified lt "2021-10-03T00:00:00Z"`. Use dot-walking to specify nested attributes.

 Data type: String

 Default: No filtering

</td></tr><tr><td>

sortBy

</td><td id="group_sortBy-SCIM-entry">

Must be specified with the **sortOrder** parameter. Field by which to sort the return results. Sorting is case-insensitive. You can only use those parameters available for filtering for the **sortBy** parameter, except that **externalId** is not allowed.

 For values that are null:

-   sorted by ascending - Null values are sorted to the top.
-   sorted by descending - Null values are sorted to the bottom.

 Data type: String

 Default: No sort

</td></tr><tr><td>

sortOrder

</td><td id="sortOrder-SCIM-entry">

Must be specified with the **sortBy** parameter. Order in which the **sortBy** parameter is applied to the return results. Valid values:

-   ascending
-   descending

 Data type: String

 Default: ascending

</td></tr><tr><td>

startIndex

</td><td id="group_startIndex-SCIM-entry">

One-based index into the table at which to start retrieving records. For example, if you set this parameter to 100, and the **count** parameter to 20, the endpoint returns records 100 through 119. **Note:** Any value that is set to less than one is interpreted as one.

 Data type: String

 Default: 1

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td id="status_400-SCIM-entry">

Bad Request. A bad request type or malformed request was detected.-   Ensure that both the **attributes** and **excludedAttributes** query parameters have not been passed in the request.
-   Ensure that the **count** parameter is not greater than 500.
-   Ensure that all **filter** parameters are valid.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="id_uwg_55q_3rb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

itemsPerPage

</td><td id="itemsPerPage-SCIM-entry">

Number of records returned in the return results.Data type: Number

</td></tr><tr><td>

Resources

</td><td>

List of returned cost center records.Data type: Object

 ```
"Resources": {
  "id": "String",
  "meta": {Object},
  "name": "String",
  "schemas": "String"
}
```

</td></tr><tr><td>

Resources.id

</td><td>

Sys\_id of the company record.Data type: String

</td></tr><tr><td>

Resources.meta

</td><td>

Information pertaining to the company record.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": "String",
  "resourcType": "String"
}
```

</td></tr><tr><td>

Resources.meta.created

</td><td>

Date and time the associated company record was created.Data type: String

</td></tr><tr><td>

Resources.meta.lastModified

</td><td>

Date and time the associated company record was last modified.Data type: String

</td></tr><tr><td>

Resources.meta.location

</td><td>

URI of the associated company record.Data type: String

</td></tr><tr><td>

Resources.meta.resourceType

</td><td>

SCIM resource type; always Company.Data type: String

</td></tr><tr><td>

Resources.name

</td><td>

Company name.Data type: String

</td></tr><tr><td>

Resources.schemas

</td><td>

Schema used when processing the request.Data type: String

</td></tr><tr><td>

schemas

</td><td>

Schema used to process the list response to the request. For example: `"urn:ietf:params:scim:api:messages:2.0:ListResponse"` Data type: String

</td></tr><tr><td>

startIndex

</td><td>

One-based index into the Company \[core\_company\] table at which the records were returned.Data type: String

</td></tr><tr><td>

totalResults

</td><td id="totalResults-SCIM-entry">

Total number of records that match the request.Data type: Number

</td></tr></tbody>
</table>### cURL request

This example shows how to retrieve the first two company records.

```
curl "https://instance-servicenow.com/api/now/scim/Companies?count=2" \
--request GET \
--header "Accept:application/scim+json" \
```

Response:

```
{
  "schemas":[
    "urn:ietf:params:scim:api:messages:2.0:ListResponse"
  ],
  "totalResults":182,
  "Resources":[
    {
      "schemas":[
        "urn:ietf:params:scim:schemas:custom:servicenow:2.0:Company"
      ],
      "id":"0c43af40c6112275011a4bd4c0143fbf",
      "meta":{
        "resourceType":"Company",
        "created":"2005-05-24T01:14:19Z",
        "lastModified":"2013-05-06T23:44:48Z",
        "location":"https://instance-servicenow.com/api/now/scim/Companies/0c43af40c6112275011a4bd4c0143fbf"
      },
      "name":"ABC Company"
    },
    {
      "schemas":[
        "urn:ietf:params:scim:schemas:custom:servicenow:2.0:Company"
      ],
      "id":"0c43b088c6112275011a4bd46a4e6cc4",
      "meta":{
        "resourceType":"Company",
        "created":"2005-05-24T01:14:19Z",
        "lastModified":"2013-06-05T17:53:26Z",
        "location":"https://instance-servicenow.com/api/now/scim/Companies/0c43b088c6112275011a4bd46a4e6cc4"
      },
      "name":"Acme Co"
    }
  ],
  "startIndex":1,
  "itemsPerPage":2
}
```

## SCIM - GET /scim/Companies/\{company\_id\}

Returns the specified company record from the Company \[core\_company\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Companies/{company_id}`

Default URL: `/api/now/scim/Groups/{company_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

company\_id

</td><td>

Sys\_id of the company record to return.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td id="status_400-SCIM-entry">

Bad Request. A bad request type or malformed request was detected.-   Ensure that both the **attributes** and **excludedAttributes** query parameters have not been passed in the request.
-   Ensure that the **count** parameter is not greater than 500.
-   Ensure that all **filter** parameters are valid.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="id_mvt_mbq_3rb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td id="id-company-SCIM-entry">

Sys\_id of the company record.Data type: String

</td></tr><tr><td>

meta

</td><td id="meta-company-SCIM-entry">

Information pertaining to the company record.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": "String",
  "resourcType": "String"
}
```

</td></tr><tr><td>

meta.created

</td><td id="meta_created-company-SCIM-entry">

Date and time the associated company record was created.Data type: String

</td></tr><tr><td>

meta.lastModified

</td><td id="meta_lastModified-company-SCIM-entry">

Date and time the associated company record was last modified.Data type: String

</td></tr><tr><td>

meta.location

</td><td id="meta_location-company-SCIM-entry">

URI of the associated company record.Data type: String

</td></tr><tr><td>

meta.resourceType

</td><td id="meta_resourceType-company-SCIM-entry">

SCIM resource type; always Company.Data type: String

</td></tr><tr><td>

name

</td><td id="name-company-SCIM-entry">

Company name.Data type: String

</td></tr><tr><td>

schemas

</td><td id="schemas-company-SCIM-entry">

Schema used when processing the request.Data type: String

</td></tr></tbody>
</table>### cURL request

This example shows how to retrieve a specific company record.

```
curl "https://instance-servicenow.com/api/now/scim/Companies/0c43af40c6112275011a4bd4c0143fbf" \
--request GET \
--header "Accept:application/scim+json" \
```

Response

```
{
  "schemas":[
    "urn:ietf:params:scim:schemas:custom:servicenow:2.0:Company"
  ],
  "id":"0c43af40c6112275011a4bd4c0143fbf",
  "meta":{
    "resourceType":"Company",
    "created":"2005-05-24T01:14:19Z",
    "lastModified":"2013-05-06T23:44:48Z",
    "location":"https://instance-servicenow.com/api/now/scim/Companies/0c43af40c6112275011a4bd4c0143fbf"
  },
  "name":"ABC Company"
}
```

## SCIM - GET /scim/CostCenters

Returns one or more cost center records from the Cost Center \[cmn\_cost\_center\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

**Note:** A query that does not return any matches returns success \(HTTP status code 200\) with **totalResults** set to 0.

### URL format

Versioned URL: `/api/now/{api_version}/scim/CostCenters`

Default URL: `/api/now/scim/CostCenters`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

count

</td><td id="count-SCIM-entry">

Number of records to return. A negative value is interpreted as zero.Data type: Number

 Maximum: 500 - A value greater than this results in a bad request error.

 Default: 10

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr><tr><td>

filter

</td><td>

Filter expression to apply to the return results. Field filters are expressed as `<field_name> <operator> <"value">`. Refer to [RFC7644](https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2) for a list of the valid operators. **Note:** The `NOT` operator is not supported by this method.

 For example, to filter for all cost center whose name starts with "HR", enter `displayName SW "HR"`.

 To specify more than one field filter, concatenate the filters using the `AND` operand. For example, to filter for all cost center whose name starts with "HR" and were last modified before October 3, 2021, enter `displayName SW "HR" AND meta.lastModified lt "2021-10-03T00:00:00Z"`. Use dot-walking to specify nested attributes.

 Data type: String

 Default: No filtering

</td></tr><tr><td>

sortBy

</td><td id="group_sortBy-SCIM-entry">

Must be specified with the **sortOrder** parameter. Field by which to sort the return results. Sorting is case-insensitive. You can only use those parameters available for filtering for the **sortBy** parameter, except that **externalId** is not allowed.

 For values that are null:

-   sorted by ascending - Null values are sorted to the top.
-   sorted by descending - Null values are sorted to the bottom.

 Data type: String

 Default: No sort

</td></tr><tr><td>

sortOrder

</td><td id="sortOrder-SCIM-entry">

Must be specified with the **sortBy** parameter. Order in which the **sortBy** parameter is applied to the return results. Valid values:

-   ascending
-   descending

 Data type: String

 Default: ascending

</td></tr><tr><td>

startIndex

</td><td id="group_startIndex-SCIM-entry">

One-based index into the table at which to start retrieving records. For example, if you set this parameter to 100, and the **count** parameter to 20, the endpoint returns records 100 through 119. **Note:** Any value that is set to less than one is interpreted as one.

 Data type: String

 Default: 1

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td id="status_400-SCIM-entry">

Bad Request. A bad request type or malformed request was detected.-   Ensure that both the **attributes** and **excludedAttributes** query parameters have not been passed in the request.
-   Ensure that the **count** parameter is not greater than 500.
-   Ensure that all **filter** parameters are valid.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="id_tld_hxq_3rb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

itemsPerPage

</td><td id="itemsPerPage-SCIM-entry">

Number of records returned in the return results.Data type: Number

</td></tr><tr><td>

Resources

</td><td>

List of returned cost center records.Data type: Object

 ```
"Resources": {
  "id": "String",
  "meta": {Object},
  "name": "String",
  "schemas": "String"
}
```

</td></tr><tr><td>

Resources.id

</td><td>

Sys\_id of the cost center record.Data type: String

</td></tr><tr><td>

Resources.meta

</td><td>

Information pertaining to the cost center record.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": "String",
  "resourcType": "String"
}
```

</td></tr><tr><td>

Resources.meta.created

</td><td>

Date and time the associated cost center record was created.Data type: String

</td></tr><tr><td>

Resources.meta.lastModified

</td><td>

Date and time the associated cost center record was last modified.Data type: String

</td></tr><tr><td>

Resources.meta.location

</td><td>

URI of the associated cost center record.Data type: String

</td></tr><tr><td>

Resources.meta.resourceType

</td><td>

SCIM resource type; always CostCenter.Data type: String

</td></tr><tr><td>

Resources.name

</td><td>

Cost center name.Data type: String

</td></tr><tr><td>

Resources.schemas

</td><td>

Schema used when processing the request.Data type: String

</td></tr><tr><td>

schemas

</td><td>

Schema used to process the list response to the request. For example: `"urn:ietf:params:scim:api:messages:2.0:ListResponse"` Data type: String

</td></tr><tr><td>

startIndex

</td><td>

One-based index into the Cost Center \[cmn\_cost\_center\] table at which the records were returned.Data type: String

</td></tr><tr><td>

totalResults

</td><td id="totalResults-SCIM-entry">

Total number of records that match the request.Data type: Number

</td></tr></tbody>
</table>### cURL request

This example shows how to retrieve the first two cost center records.

```
curl "https://instance-servicenow.com/api/now/scim/CostCenters?count=2" \
--request GET \
--header "Accept:application/scim+json" \
```

Response

```
{
  "schemas":[
    "urn:ietf:params:scim:api:messages:2.0:ListResponse"
  ],
  "totalResults":8,
  "Resources":[
    {
      "schemas":[
        "urn:ietf:params:scim:schemas:custom:servicenow:2.0:CostCenter"
      ],
      "id":"7fb1cc99c0a80a6d30c04574d14c0acf",
      "meta":{
        "resourceType":"CostCenter",
        "created":"2012-01-19T21:02:39Z",
        "lastModified":"2012-02-25T23:06:36Z",
        "location":"https://instance-servicenow.com/api/now/scim/CostCenters/7fb1cc99c0a80a6d30c04574d14c0acf"
      },
      "name":"Sales"
    },
    {
      "schemas":[
        "urn:ietf:params:scim:schemas:custom:servicenow:2.0:CostCenter"
      ],
      "id":"91e8bbf43710200044e0bfc8bcbe5daa",
      "meta":{
        "resourceType":"CostCenter",
        "created":"2012-02-18T04:40:24Z",
        "lastModified":"2012-02-25T23:05:58Z",
        "location":"https://instance-servicenow.com/api/now/scim/CostCenters/91e8bbf43710200044e0bfc8bcbe5daa"
      },
      "name":"Customer Support"
    }
  ],
  "startIndex":1,
  "itemsPerPage":2
}
```

## SCIM - GET /scim/CostCenters/\{cost\_center\_id\}

Returns the specified cost center record from the Cost Center \[cmn\_cost\_center\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

**Note:** A query that does not return any matches returns success \(HTTP status code 200\) with **totalResults** set to 0.

### URL format

Versioned URL: `/api/now/{api_version}/scim/CostCenters/{cost_center_id}`

Default URL: `/api/now/scim/CoostCenters/{cost_center_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

cost\_center\_id

</td><td>

Sys\_id of the cost center record to return.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td id="status_400-SCIM-entry">

Bad Request. A bad request type or malformed request was detected.-   Ensure that both the **attributes** and **excludedAttributes** query parameters have not been passed in the request.
-   Ensure that the **count** parameter is not greater than 500.
-   Ensure that all **filter** parameters are valid.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="id_tld_hxq_3rb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td id="id-costcenter-SCIM-entry">

Sys\_id of the cost center record.Data type: String

</td></tr><tr><td>

meta

</td><td id="meta-costcenter-SCIM-entry">

Information pertaining to the cost center record.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": "String",
  "resourcType": "String"
}
```

</td></tr><tr><td>

meta.created

</td><td id="meta_created-costcenter-SCIM-entry">

Date and time the associated cost center record was created.Data type: String

</td></tr><tr><td>

meta.lastModified

</td><td id="meta_lastModified-costcenter-SCIM-entry">

Date and time the associated cost center record was last modified.Data type: String

</td></tr><tr><td>

meta.location

</td><td id="meta_location-costcenter-SCIM-entry">

URI of the associated cost center record.Data type: String

</td></tr><tr><td>

meta.resourceType

</td><td id="meta_resourceType-costcenter-SCIM-entry">

SCIM resource type; always CostCenter.Data type: String

</td></tr><tr><td>

name

</td><td id="name-costcenter-SCIM-entry">

Cost center name.Data type: String

</td></tr><tr><td>

schemas

</td><td id="schemas-costcenter-SCIM-entry">

Schema used when processing the request.Data type: String

</td></tr></tbody>
</table>### cURL request

This example shows how to retrieve a specific cost center record.

```
curl "https://instance-servicenow.com/api/now/scim/CostCenters/7fb1cc99c0a80a6d30c04574d14c0acf" \
--request GET \
--header "Accept:application/scim+json" \
```

Response

```
{
  "schemas":[
    "urn:ietf:params:scim:schemas:custom:servicenow:2.0:CostCenter"
  ],
  "id":"7fb1cc99c0a80a6d30c04574d14c0acf",
  "meta":{
    "resourceType":"CostCenter",
    "created":"2012-01-19T21:02:39Z",
    "lastModified":"2012-02-25T23:06:36Z",
    "location":"https://instance-servicenow.com/api/now/scim/CostCenters/7fb1cc99c0a80a6d30c04574d14c0acf"
  },
  "name":"Sales"
}
```

## SCIM - GET /scim/Departments

Returns one or more department records from the Department \[cmn\_department\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

**Note:** A query that does not return any matches returns success \(HTTP status code 200\) with **totalResults** set to 0.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Departments`

Default URL: `/api/now/scim/Departments`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

count

</td><td id="count-SCIM-entry">

Number of records to return. A negative value is interpreted as zero.Data type: Number

 Maximum: 500 - A value greater than this results in a bad request error.

 Default: 10

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr><tr><td>

filter

</td><td>

Filter expression to apply to the return results. Field filters are expressed as `<field_name> <operator> <"value">`. Refer to [RFC7644](https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2) for a list of the valid operators. **Note:** The `NOT` operator is not supported by this method.

 For example, to filter for all departments whose name starts with "Engineer", enter `displayName SW "Engineer"`.

 To specify more than one field filter, concatenate the filters using the `AND` operand. For example, to filter for all departments whose name starts with "Engineer" and were last modified before October 3, 2021, enter `displayName SW "Engineer" AND meta.lastModified lt "2021-10-03T00:00:00Z"`. Use dot-walking to specify nested attributes.

 Data type: String

 Default: No filtering

</td></tr><tr><td>

sortBy

</td><td id="group_sortBy-SCIM-entry">

Must be specified with the **sortOrder** parameter. Field by which to sort the return results. Sorting is case-insensitive. You can only use those parameters available for filtering for the **sortBy** parameter, except that **externalId** is not allowed.

 For values that are null:

-   sorted by ascending - Null values are sorted to the top.
-   sorted by descending - Null values are sorted to the bottom.

 Data type: String

 Default: No sort

</td></tr><tr><td>

sortOrder

</td><td id="sortOrder-SCIM-entry">

Must be specified with the **sortBy** parameter. Order in which the **sortBy** parameter is applied to the return results. Valid values:

-   ascending
-   descending

 Data type: String

 Default: ascending

</td></tr><tr><td>

startIndex

</td><td id="group_startIndex-SCIM-entry">

One-based index into the table at which to start retrieving records. For example, if you set this parameter to 100, and the **count** parameter to 20, the endpoint returns records 100 through 119. **Note:** Any value that is set to less than one is interpreted as one.

 Data type: String

 Default: 1

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td id="status_400-SCIM-entry">

Bad Request. A bad request type or malformed request was detected.-   Ensure that both the **attributes** and **excludedAttributes** query parameters have not been passed in the request.
-   Ensure that the **count** parameter is not greater than 500.
-   Ensure that all **filter** parameters are valid.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="id_sqc_3br_3rb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

itemsPerPage

</td><td id="itemsPerPage-SCIM-entry">

Number of records returned in the return results.Data type: Number

</td></tr><tr><td>

Resources

</td><td>

List of returned department records.Data type: Object

 ```
"Resources": {
  "id": "String",
  "meta": {Object},
  "name": "String",
  "schemas": "String"
}
```

</td></tr><tr><td>

Resources.id

</td><td>

Sys\_id of the department record.Data type: String

</td></tr><tr><td>

Resources.meta

</td><td>

Information pertaining to the department record.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": "String",
  "resourcType": "String"
}
```

</td></tr><tr><td>

Resources.meta.created

</td><td>

Date and time the associated department record was created.Data type: String

</td></tr><tr><td>

Resources.meta.lastModified

</td><td>

Date and time the associated department record was last modified.Data type: String

</td></tr><tr><td>

Resources.meta.location

</td><td>

URI of the associated department record.Data type: String

</td></tr><tr><td>

Resources.meta.resourceType

</td><td>

SCIM resource type; always Department.Data type: String

</td></tr><tr><td>

Resources.name

</td><td>

Department name.Data type: String

</td></tr><tr><td>

Resources.schemas

</td><td>

 

</td></tr><tr><td>

schemas

</td><td>

 

</td></tr><tr><td>

startIndex

</td><td>

One-based index into the Department \[cmn\_department\] table at which the records were returned.Data type: String

</td></tr><tr><td>

totalResults

</td><td id="totalResults-SCIM-entry">

Total number of records that match the request.Data type: Number

</td></tr></tbody>
</table>### cURL request

This example shows how to retrieve the first two department records.

```
curl "https://instance-servicenow.com/api/now/scim/Departments?count=2" \
--request GET \
--header "Accept:application/scim+json" \
```

Response

```
{
  "schemas":[
    "urn:ietf:params:scim:api:messages:2.0:ListResponse"
  ],
  "totalResults":7,
  "Resources":[
    {
      "schemas":[
        "urn:ietf:params:scim:schemas:custom:servicenow:2.0:Department"
      ],
      "id":"221db0edc611228401760aec06c9d929",
      "meta":{
        "resourceType":"Department",
        "created":"2006-01-31T20:18:24Z",
        "lastModified":"2012-02-18T07:01:40Z",
        "location":"https://instance-servicenow.com/api/now/scim/Departments/221db0edc611228401760aec06c9d929"
      },
      "name":"Sales"
    },
    {
      "schemas":[
        "urn:ietf:params:scim:schemas:custom:servicenow:2.0:Department"
      ],
      "id":"221f3db5c6112284009f4becd3039cc9",
      "meta":{
        "resourceType":"Department",
        "created":"2008-03-20T20:20:06Z",
        "lastModified":"2012-02-18T07:01:22Z",
        "location":"https://instance-servicenow.com/api/now/scim/Departments/221f3db5c6112284009f4becd3039cc9"
      },
      "name":"Development"
    }
  ],
  "startIndex":1,
  "itemsPerPage":2
}
```

## SCIM - GET /scim/Departments/\{deparment\_id\}

Returns the specified department record from the Department \[cmn\_department\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Departments/{department_id}`

Default URL: `/api/now/scim/Departments/{department_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

department\_id

</td><td>

Sys\_id of the department record to return.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td id="status_400-SCIM-entry">

Bad Request. A bad request type or malformed request was detected.-   Ensure that both the **attributes** and **excludedAttributes** query parameters have not been passed in the request.
-   Ensure that the **count** parameter is not greater than 500.
-   Ensure that all **filter** parameters are valid.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="id_g3b_jdr_3rb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td id="id-dept-SCIM-entry">

Sys\_id of the department record.Data type: String

</td></tr><tr><td>

meta

</td><td id="meta-dept-SCIM-entry">

Information pertaining to the department record.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": "String",
  "resourcType": "String"
}
```

</td></tr><tr><td>

meta.created

</td><td id="meta_created-dept-SCIM-entry">

Date and time the associated department record was created.Data type: String

</td></tr><tr><td>

meta.lastModified

</td><td id="meta_lastModified-dept-SCIM-entry">

Date and time the associated department record was last modified.Data type: String

</td></tr><tr><td>

meta.location

</td><td id="meta_location-dept-SCIM-entry">

URI of the associated department record.Data type: String

</td></tr><tr><td>

meta.resourceType

</td><td id="meta_resourceType-dept-SCIM-entry">

SCIM resource type; always Department.Data type: String

</td></tr><tr><td>

name

</td><td id="name-dept-SCIM-entry">

Department name.Data type: String

</td></tr><tr><td>

schemas

</td><td id="schemas-dept-SCIM-entry">

Schema used when processing the request.Data type: String

</td></tr></tbody>
</table>### cURL request

This example shows how to retrieve a specific department record.

```
curl "https://instance-servicenow.com/api/now/scim/Departments/221db0edc611228401760aec06c9d929" \
--request GET \
--header "Accept:application/scim+json" \
```

Response:

```
{
  "schemas":[
    "urn:ietf:params:scim:schemas:custom:servicenow:2.0:Department"
  ],
  "id":"221db0edc611228401760aec06c9d929",
  "meta":{
    "resourceType":"Department",
    "created":"2006-01-31T20:18:24Z",
    "lastModified":"2012-02-18T07:01:40Z",
    "location":"https://instance-servicenow.com/api/now/scim/Departments/221db0edc611228401760aec06c9d929"
  },
  "name":"Sales"
}
```

## SCIM - GET /scim/Locations

Returns one or more location records from the Location \[cmn\_location\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

**Note:** A query that does not return any matches returns success \(HTTP status code 200\) with **totalResults** set to 0.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Locations`

Default URL: `/api/now/scim/Locations`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

count

</td><td id="count-SCIM-entry">

Number of records to return. A negative value is interpreted as zero.Data type: Number

 Maximum: 500 - A value greater than this results in a bad request error.

 Default: 10

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr><tr><td>

filter

</td><td>

Filter expression to apply to the return results. Field filters are expressed as `<field_name> <operator> <"value">`. Refer to [RFC7644](https://datatracker.ietf.org/doc/html/rfc7644#section-3.4.2) for a list of the valid operators. **Note:** The `NOT` operator is not supported by this method.

 For example, to filter for all locations whose name starts with "Ch", enter `displayName SW "Ch"`.

 To specify more than one field filter, concatenate the filters using the `AND` operand. For example, to filter for all locations whose name starts with "Ch" and were last modified before October 3, 2021, enter `displayName SW "Ch" AND meta.lastModified lt "2021-10-03T00:00:00Z"`. Use dot-walking to specify nested attributes.

 Data type: String

 Default: No filtering

</td></tr><tr><td>

sortBy

</td><td id="group_sortBy-SCIM-entry">

Must be specified with the **sortOrder** parameter. Field by which to sort the return results. Sorting is case-insensitive. You can only use those parameters available for filtering for the **sortBy** parameter, except that **externalId** is not allowed.

 For values that are null:

-   sorted by ascending - Null values are sorted to the top.
-   sorted by descending - Null values are sorted to the bottom.

 Data type: String

 Default: No sort

</td></tr><tr><td>

sortOrder

</td><td id="sortOrder-SCIM-entry">

Must be specified with the **sortBy** parameter. Order in which the **sortBy** parameter is applied to the return results. Valid values:

-   ascending
-   descending

 Data type: String

 Default: ascending

</td></tr><tr><td>

startIndex

</td><td id="group_startIndex-SCIM-entry">

One-based index into the table at which to start retrieving records. For example, if you set this parameter to 100, and the **count** parameter to 20, the endpoint returns records 100 through 119. **Note:** Any value that is set to less than one is interpreted as one.

 Data type: String

 Default: 1

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td id="status_400-SCIM-entry">

Bad Request. A bad request type or malformed request was detected.-   Ensure that both the **attributes** and **excludedAttributes** query parameters have not been passed in the request.
-   Ensure that the **count** parameter is not greater than 500.
-   Ensure that all **filter** parameters are valid.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="id_qt1_xfr_3rb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

itemsPerPage

</td><td id="itemsPerPage-SCIM-entry">

Number of records returned in the return results.Data type: Number

</td></tr><tr><td>

Resources

</td><td>

List of returned location records.Data type: Object

 ```
"Resources": {
  "id": "String",
  "meta": {Object},
  "name": "String",
  "schemas": "String"
}
```

</td></tr><tr><td>

Resources.id

</td><td>

Sys\_id of the location record.Data type: String

</td></tr><tr><td>

Resources.meta

</td><td>

Information pertaining to the location record.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": "String",
  "resourceType": "String"
}
```

</td></tr><tr><td>

Resources.meta.created

</td><td>

Date and time the associated location record was created.Data type: String

</td></tr><tr><td>

Resources.meta.lastModified

</td><td>

Date and time the associated location record was last modified.Data type: String

</td></tr><tr><td>

Resources.meta.location

</td><td>

URI of the associated location record.Data type: String

</td></tr><tr><td>

Resources.meta.resourceType

</td><td>

SCIM resource type; always Location.Data type: String

</td></tr><tr><td>

Resources.name

</td><td>

Location name.Data type: String

</td></tr><tr><td>

Resources.schemas

</td><td>

Schema used when processing the request.Data type: String

</td></tr><tr><td>

schemas

</td><td>

Schema used to process the list response to the request. For example: `"urn:ietf:params:scim:api:messages:2.0:ListResponse"` Data type: String

</td></tr><tr><td>

startIndex

</td><td>

One-based index into the Location \[cmn\_location\] table at which the records were returned.Data type: String

</td></tr><tr><td>

totalResults

</td><td id="totalResults-SCIM-entry">

Total number of records that match the request.Data type: Number

</td></tr></tbody>
</table>### cURL request

This example shows how to retrieve a the first two company records.

```
curl "https://instance-servicenow.com/api/now/scim/Locations?count=2" \
--request GET \
--header "Accept:application/scim+json" \
```

Response

```
{
  "schemas":[
    "urn:ietf:params:scim:api:messages:2.0:ListResponse"
  ],
  "totalResults":426,
  "Resources":[
    {
      "schemas":["urn:ietf:params:scim:schemas:custom:servicenow:2.0:Location"],
      "id":"0002c0a93790200044e0bfc8bcbe5df5",
      "meta":{
        "resourceType":"Location",
        "created":"2012-02-19T18:39:00Z",
        "lastModified":"2012-02-19T18:39:00Z",
        "location":"https://instance-servicenow.com/api/now/scim/Locations/0002c0a93790200044e0bfc8bcbe5df5"
      },
      "name":"2-10-1 Yurakucho, Chiyoda-ku, Tokyo"
    },
    {
      "schemas":["urn:ietf:params:scim:schemas:custom:servicenow:2.0:Location"],
      "id":"0594ed7437d0200044e0bfc8bcbe5df0",
      "meta":{
        "resourceType":"Location",
        "created":"2012-02-17T17:54:15Z",
        "lastModified":"2021-08-31T14:13:11Z",
        "location":"https://instance-servicenow.com/api/now/scim/Locations/0594ed7437d0200044e0bfc8bcbe5df0"
      },
      "name":"Colombia"
    }
  ],
  "startIndex":1,
  "itemsPerPage":2
}
```

## SCIM - GET /scim/Locations/\{location\_id\}

Returns the specified location record from the Location \[cmn\_location\] table within a ServiceNow instance using the System for Cross-domain Identity Management \(SCIM\) protocol.

### URL format

Versioned URL: `/api/now/{api_version}/scim/Locations/{location_id}`

Default URL: `/api/now/scim/Locations/{location_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

location\_id

</td><td>

Sys\_id of the location record to return.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="attributes-SCIM-entry">

Comma-separated list of fields to return in the response. No other fields are returned.Cannot be used with the **excludedAttributes** parameter.

 Data type: String

 Default: Return all fields unless **excludedAttributes** is specified.

</td></tr><tr><td>

excludedAttributes

</td><td id="excludedAttributes-SCIM-entry">

Comma-separated list of fields to exclude from the records returned in the response. All other fields are returned.Cannot be used with the **attributes** parameter.

 Data type: String

 Default: Do not exclude any fields.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="Accept-SCIM-entry">

Data format of the response body. Supported types: **application/json** or **application/scim+json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td id="status_400-SCIM-entry">

Bad Request. A bad request type or malformed request was detected.-   Ensure that both the **attributes** and **excludedAttributes** query parameters have not been passed in the request.
-   Ensure that the **count** parameter is not greater than 500.
-   Ensure that all **filter** parameters are valid.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="id_s2d_33r_3rb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td id="id-location-SCIM-entry">

Sys\_id of the location record.Data type: String

</td></tr><tr><td>

meta

</td><td id="meta-location-SCIM-entry">

Information pertaining to the location record.Data type: Object

 ```
"meta": {
  "created": "String",
  "lastModified": "String",
  "location": "String",
  "resourceType": "String"
}
```

</td></tr><tr><td>

meta.created

</td><td id="meta_created-location-SCIM-entry">

Date and time the associated location record was created.Data type: String

</td></tr><tr><td>

meta.lastModified

</td><td id="meta_lastModified-location-SCIM-entry">

Date and time the associated location record was last modified.Data type: String

</td></tr><tr><td>

meta.location

</td><td id="meta_location-location-SCIM-entry">

URI of the associated location record.Data type: String

</td></tr><tr><td>

meta.resourceType

</td><td id="meta_resourceType-location-SCIM-entry">

SCIM resource type; always Location.Data type: String

</td></tr><tr><td>

name

</td><td id="name-location-SCIM-entry">

Location name.Data type: String

</td></tr><tr><td>

schemas

</td><td id="schemas-location-SCIM-entry">

Schema used when processing the request.Data type: String

</td></tr></tbody>
</table>### cURL request

This example shows how to retrieve a specific location record.

```
curl "https://instance-servicenow.com/api/now/scim/Locations/0c43af40c6112275011a4bd4c0143fbf" \
--request GET \
--header "Accept:application/scim+json" \
```

Response

```
{
  "schemas":["urn:ietf:params:scim:schemas:custom:servicenow:2.0:Location"],
  "id":"0594ed7437d0200044e0bfc8bcbe5df0",
  "meta":{
    "resourceType":"Location",
    "created":"2012-02-17T17:54:15Z",
    "lastModified":"2021-08-31T14:13:11Z",
    "location":"https://instance-servicenow.com/api/now/scim/Locations/0594ed7437d0200044e0bfc8bcbe5df0"
  },
  "name":"Colombia"
}
```

