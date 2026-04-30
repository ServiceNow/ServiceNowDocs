---
title: Resource Inventory Open API
description: The Resource Inventory Open API provides endpoints to create, retrieve, and delete resources.Deletes a specified resource record.Retrieves a list of all resource records.Retrieves a specified resource record.Updates a specified resource record.Creates a resource record.Creates a resource configuration item \(CI\) and related CI hierarchy based on a template.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 45
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Resource Inventory Open API

The Resource Inventory Open API provides endpoints to create, retrieve, and delete resources.

Use this API to manage resources in the following tables.

-   Cable \[cmdb\_ci\_cable\]
-   Equipment Holder \[cmdb\_ci\_equipment\_holder\]
-   Interface Card \[cmdb\_ci\_interface\_card\]
-   IP Address \[cmdb\_ci\_ip\_address\]
-   Logical Connection \[cmdb\_ci\_ni\_logical\_path\]
-   Network Interface \[cmdb\_ci\_ni\_interface\]
-   Network Site \[cmdb\_ci\_ni\_site\]
-   Physical Connection \[cmdb\_ci\_ni\_physical\_link\]
-   Strand \[cmdb\_ci\_strand\]
-   Topology \[cmdb\_ci\_topology\]
-   Tables specified by the **sn\_ni\_core.equipment\_tables** sys\_property, and any tables that extend the specified tables.
-   Tables that extend Equipment Holder \[cmdb\_ci\_equipment\_holder\].
-   Child tables that extend any of the following tables:
    -   Cable \[cmdb\_ci\_cable\]
    -   Equipment Holder \[cmdb\_ci\_equipment\_holder\]
    -   Strand \[cmdb\_ci\_strand\]

This API is included in the Network Inventory Core application, which is available on the ServiceNow Store.

This API is provided within the `sn_ni_core` namespace.

The calling user must have the sn\_ni\_core.inventory\_integrator role.

This API can be extended to make customizations around required parameters, request body validation, and field mappings. For more information, see the [Resource Inventory Open API Developer Guide](../../guides/telecom/concept/resource-inventory-dev-guide.md#).

The Resource Inventory Open API is a ServiceNow® implementation of the TM Forum Resource Inventory API REST specification. This implementation is based on the [TMF639 Resource Inventory API User Guide v4.0.1](https://www.tmforum.org/resources/standard/tmf639-resource-inventory-api-user-guide-v4-0/), July 2020.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Resource Inventory Open API - DELETE /sn\_ni\_core/resource/\{id\}

Deletes a specified resource record.

### URL format

Default URL: `/api/sn_ni_core/resource/{id}`

### Supported request parameters

<table id="table_tjw_q3s_g5b" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the resource. Located in one of the following tables depending on the type of resource.-   Interface Card \[cmdb\_ci\_interface\_card\]
-   Logical Connection \[cmdb\_ci\_ni\_logical\_path\]
-   Network Interface \[cmdb\_ci\_ni\_interface\]
-   Network Site \[cmdb\_ci\_ni\_site\]
-   Physical Connection \[cmdb\_ci\_ni\_physical\_link\]
-   Tables specified by the **sn\_ni\_core.equipment\_tables** sys\_property, and any tables that extend the specified tables.
-   Tables that extend Equipment Holder \[cmdb\_ci\_equipment\_holder\].

**Note:** Resources in the IP Address \[cmdb\_ci\_ip\_address\] table can't be deleted using this API.

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

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|215|Request successfully received for processing. The request will be completed asynchronously.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|403|Forbidden. Resource deletion failed. The resource might be required by its related resources.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON\)

|Name|Description|
|----|-----------|
|None| |

### cURL request

This example deletes a resource.

```
curl "https://instance.service-now.com/api/sn_ni_core/resource/54ada05e875c15109a9c0f65dabb3586" \
--request DELETE \
--header "Accept:application/json" \
--user 'username':'password'

```

Response body.

```
""
```

## Resource Inventory Open API - GET /sn\_ni\_core/resource

Retrieves a list of all resource records.

### URL format

Default URL: `/api/sn_ni_core/resource`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

Required. Table name of the type of resource to retrieve. You can only retrieve one type of resource per API call. Valid values:

-   `cmdb_ci_cable` \(Cable\)
-   `cmdb_ci_interface_card` \(Interface Card\)
-   `cmdb_ci_ip_address` \(IP Address\)
-   `cmdb_ci_ni_logical_path` \(Logical Connection\)
-   `cmdb_ci_ni_interface` \(Network Interface\)
-   `cmdb_ci_ni_site` \(Network Site\)
-   `cmdb_ci_ni_physical_link` \(Physical Connection\)
-   `cmdb_ci_strand` \(Strand\)
-   `cmdb_ci_topology` \(Topology\)
-   Name of a table specified by the **sn\_ni\_core.equipment\_tables** sys\_property, or name of a table that extends the specified tables.
-   Name of a table that extends Equipment Holder \[cmdb\_ci\_equipment\_holder\].

 Data type: String

</td></tr><tr><td>

description

</td><td>

Description to use to filter resources. Only resources with the specified description are returned in the response. Data type: String

</td></tr><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. Valid values:

-   description
-   href
-   id
-   name
-   note
-   place
-   relatedParty
-   resourceCharacteristic
-   resourceRelationship
-   resourceSpecification
-   startOperatingDate

Data type: String

Default: Returns all fields.

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval. Default: 20

 Data type: Number

</td></tr><tr><td>

name

</td><td>

Name to use to filter resources. Only resources with the specified name are returned in the response.Data type: String

</td></tr><tr id="tmf-offset"><td>

offset

</td><td>

Starting index at which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks.Default: 0

 Data type: Number

</td></tr><tr><td>

resourceSpecification.id

</td><td>

Resource specification sys\_id to use to filter resources. The sys\_id must be from a model in one of the following tables.-   Equipment Holder Models \[sn\_ni\_core\_equipment\_holder\_product\_model\]
-   Equipment Models \[sn\_ni\_core\_equipment\_product\_model\]
-   Interface Card Models \[sn\_ni\_core\_interface\_card\_product\_model\]
-   Logical Connection Models \[sn\_ni\_core\_logical\_connection\_product\_model\]
-   Network Interface Models \[sn\_ni\_core\_network\_interface\_product\_model\]
-   Physical Connection Models \[sn\_ni\_core\_physical\_connection\_product\_model\]

Only resources with a model matching the specified sys\_id are returned in the response.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

<table id="table_lpj_dh1_vxb"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Range

</td><td>

Range of content returned in a paginated call. For example, if `offset=2` and `limit=3`, the value of the **Content-Range** header is `items 3-5`.

</td></tr><tr><td>

Content-Type

</td><td>

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Link

</td><td>

Contains the following links to navigate through query results.-   first
-   last
-   next
-   previous

</td></tr><tr><td>

X-Total-Count

</td><td>

For paginated queries, this header specifies the total number of records available on the server.**Note:** If the total number of records is more than 100,000 this header always returns 100,000.

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|206|Partial content. The request was successfully processed and returned a partial range of content specified by a paginated call.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|

### Response body parameters \(JSON\)

<table id="table_okb_1rw_f5b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td id="type-entry">

@type

</td><td id="type-descr-entry">

Type of resource.Valid values:

-   `cmdb_ci_cable` \(Cable\)
-   `cmdb_ci_interface_card` \(Interface Card\)
-   `cmdb_ci_ip_address` \(IP Address\)
-   `cmdb_ci_ni_logical_path` \(Logical Connection\)
-   `cmdb_ci_ni_interface` \(Network Interface\)
-   `cmdb_ci_ni_site` \(Network Site\)
-   `cmdb_ci_ni_physical_link` \(Physical Connection\)
-   `cmdb_ci_strand` \(Strand\)
-   `cmdb_ci_topology` \(Topology\)
-   Name of a table specified by the **sn\_ni\_core.equipment\_tables** sys\_property, or name of a table that extends the specified tables.
-   Name of a table that extends Equipment Holder \[cmdb\_ci\_equipment\_holder\].

Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the resource.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the resource. Located in one of the following tables depending on the type of resource.-   Cable \[cmdb\_ci\_cable\]
-   Equipment Holder \[cmdb\_ci\_equipment\_holder\]
-   Interface Card \[cmdb\_ci\_interface\_card\]
-   IP Address \[cmdb\_ci\_ip\_address\]
-   Logical Connection \[cmdb\_ci\_ni\_logical\_path\]
-   Network Interface \[cmdb\_ci\_ni\_interface\]
-   Network Site \[cmdb\_ci\_ni\_site\]
-   Physical Connection \[cmdb\_ci\_ni\_physical\_link\]
-   Strand \[cmdb\_ci\_strand\]
-   Topology \[cmdb\_ci\_topology\]
-   Tables specified by the **sn\_ni\_core.equipment\_tables** sys\_property, and any tables that extend the specified tables.
-   Tables that extend Equipment Holder \[cmdb\_ci\_equipment\_holder\].
-   Child tables that extend any of the following tables:
    -   Cable \[cmdb\_ci\_cable\]
    -   Equipment Holder \[cmdb\_ci\_equipment\_holder\]
    -   Strand \[cmdb\_ci\_strand\]

Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the resource.

Data type: String

</td></tr><tr><td>

note

</td><td>

List of notes about the resource. Data type: Array of Objects

```
"note": [
   {
      "text": "String"
   }
]
```

</td></tr><tr><td>

note.text

</td><td>

The note text.

Data type: String

</td></tr><tr><td>

place

</td><td>

Network site for the resource.

This parameter is not supported for Network Site, Physical Connection, or Logical Connection resources.

Data type: Object

```
"place": {
   "@referredType": "String",
   "href": "String",
   "id": "String"
}
```

</td></tr><tr><td>

place.@referredType

</td><td>

Type of place. This value is always `GeographicAddress`.Data type: String

</td></tr><tr><td>

place.href

</td><td>

Relative link to the place record.Data type: String

</td></tr><tr><td>

place.id

</td><td>

Sys\_id of the place record.

Data type: String

Table: Network Site \[cmdb\_ci\_ni\_site\]

</td></tr><tr><td id="related-party-parm">

relatedParty

</td><td>

Details about contacts for the resource.

Data type: Array of Objects

```
"relatedParty": [
   {
      "@referredType": "String",
      "href": "String",
      "id": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of related party. Located in the in the **Type** field.Data type: String

Table: In the type field of Group \[sys\_user\_group\] table.

</td></tr><tr><td>

relatedParty.href

</td><td>

Relative link to the related party record.Data type: String

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the related party record.

Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

relatedParty.role

</td><td>

Role of the related party. Data type: String

Table: In the Group type field of the Teams \[cmdb\_rel\_team\] table.

</td></tr><tr><td>

resourceCharacteristic

</td><td>

List of characteristics of the resource. The following resource types require specific resource characteristics. -   For Physical Connection and Logical Connection resources, a `Port A` or `Port Z` characteristic is required. If the Lifecycle Stage Status of the resource is In Use, both `Port A` and `Port Z` are required.
-   For Equipment Holder resources, a `Container Type` characteristic is required.

Data type: Array of Objects

```
"resourceCharacteristic": [
   {
      "name": "String",
      "value": "String",
      "valueType": "String"
   }
]
```

</td></tr><tr><td>

resourceCharacteristic.name

</td><td>

Field name from the resource table specified by the **@type** parameter. You can't use the fields model\_id, name, network\_site, operation\_notes, operational\_status, short\_description, start\_date, or any sys\_ prefixed fields such as sys\_id.

Data type: String

</td></tr><tr><td>

resourceCharacteristic.value

</td><td>

The value of the characteristic.

Data type: String

</td></tr><tr><td>

resourceCharacteristic.valueType

</td><td>

Type of value.Valid values:

-   boolean
-   datetime
-   float
-   integer
-   ph\_number
-   reference
-   string

Data type: String

</td></tr><tr><td>

resourceRelationship

</td><td>

List of related resources. The following resource types require specific related resources. -   For Interface Card resources, a relationship to an Equipment Holder resource where Container Type is Slot or Sub Slot is required.
-   For Network Interface resources, a relationship to an Equipment or Interface Card resource is required.
-   For Equipment Holder resources where Container Type is Slot or Sub Slot, a relationship to an Equipment or Interface Card resource is required.

Data type: Array

```
"resourceRelationship": [
  {
    "relationshipType": "String",
    "resource": {Object}
  }
]
```

</td></tr><tr><td>

resourceRelationship.relationshipType

</td><td>

Type of relationship between the two resources in the format `[this resource descriptor]::[related resource descriptor]`. For example, `Contains::Contained by` indicates that the related resource is the child of this resource.

Valid values for the descriptors are located in the CI Relationship Type \[cmdb\_rel\_type\] table in the **Parent descriptor** and **Child descriptor** columns.

Data type: String

</td></tr><tr><td>

resourceRelationship.resource

</td><td>

Details about the related resource. The related resource must be one of the following resource types.

-   Cable
-   Equipment
-   Equipment Holder
-   Interface Card
-   Logical Connection
-   Network Interface
-   Network Site
-   Physical Connection
-   Strand
-   Topology

Data type: Object

```
"resource": {
   "id": "String",
   "href": "String"
}
```

</td></tr><tr><td>

resourceRelationship.resource.id

</td><td>

Sys\_id of the related resource. Located in one of the following tables depending on the type of related resource.

-   Interface Card \[cmdb\_ci\_interface\_card\]
-   Logical Connection \[cmdb\_ci\_ni\_logical\_path\]
-   Network Interface \[cmdb\_ci\_ni\_interface\]
-   Network Site \[cmdb\_ci\_ni\_site\]
-   Physical Connection \[cmdb\_ci\_ni\_physical\_link\]
-   Tables specified by the **sn\_ni\_core.equipment\_tables** sys\_property, and any tables that extend the specified tables.
-   Tables that extend Equipment Holder \[cmdb\_ci\_equipment\_holder\]

Data type: String

</td></tr><tr><td>

resourceRelationship.resource.href

</td><td>

Relative link to the related resource record.Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

Resource specification. Data type: Object

```
"resourceSpecification": {
   "id": "String"
}
```

</td></tr><tr><td>

resourceSpecification.id

</td><td>

Sys\_id of the associated model for the resource. Located in one of the following tables depending on the type of model.

-   Cable Models \[sn\_ent\_cable\_model\]
-   Equipment Holder Models \[sn\_ent\_nw\_holder\_model\]
-   Equipment Models \[sn\_ent\_nw\_equipment\_model\]
-   Interface Card Models \[sn\_ent\_nw\_interface\_model\]
-   Logical Connection Models \[sn\_ent\_logical\_nw\_connection\_model\]
-   Network Interface Models \[sn\_ent\_nw\_interface\_model\]
-   Physical Connection Models \[sn\_ent\_physical\_nw\_connection\_model\]
-   Strand Models \[sn\_ent\_strand\_model\]
-   Topology Models \[sn\_ent\_network\_topology\_model\]

Data type: String

</td></tr><tr><td>

startOperatingDate

</td><td>

Date and time that the resource first started operating.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves the **name**, **id**, and **href** fields for the first five Network Site resource records.

```
curl "https://instance.service-now.com/api/sn_ni_core/resource?@type=cmdb_ci_ni_site&fields=name%2Cid%2Chref&limit=5" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body.

```
[
   {
      "name": "DALLAS TX CO/HUB",
      "id": "c23683c54051c910f8772175cacd725c",
      "href": "/api/sn_ni_core/resource/c23683c54051c910f8772175cacd725c"
   },
   {
      "name": "PFP LOC F-800",
      "id": "0ac19bc54051c910f8772175cacd724b",
      "href": "/api/sn_ni_core/resource/0ac19bc54051c910f8772175cacd724b"
   },
   {
      "name": "FIBER SERVICE TERMINAL 003",
      "id": "d0541fcd4051c910f8772175cacd72c8",
      "href": "/api/sn_ni_core/resource/d0541fcd4051c910f8772175cacd72c8"
   },
   {
      "name": "270 RUMWOOD MAIN",
      "id": "e6f6df8d4051c910f8772175cacd72b2",
      "href": "/api/sn_ni_core/resource/e6f6df8d4051c910f8772175cacd72b2"
   },
   {
      "name": "3620 CHESTER ROMI48073",
      "id": "917dd8f6870e851079c40f2d0ebb353d",
      "href": "/api/sn_ni_core/resource/917dd8f6870e851079c40f2d0ebb353d"
   }
]
```

## Resource Inventory Open API - GET /sn\_ni\_core/resource/\{id\}

Retrieves a specified resource record.

### URL format

Default URL: `/api/sn_ni_core/resource/{id}`

### Supported request parameters

<table id="table_tjw_q3s_g5b" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the resource. Located in one of the following tables depending on the type of resource.-   Cable \[cmdb\_ci\_cable\]
-   Equipment Holder \[cmdb\_ci\_equipment\_holder\]
-   Interface Card \[cmdb\_ci\_interface\_card\]
-   IP Address \[cmdb\_ci\_ip\_address\]
-   Logical Connection \[cmdb\_ci\_ni\_logical\_path\]
-   Network Interface \[cmdb\_ci\_ni\_interface\]
-   Network Site \[cmdb\_ci\_ni\_site\]
-   Physical Connection \[cmdb\_ci\_ni\_physical\_link\]
-   Strand \[cmdb\_ci\_strand\]
-   Topology \[cmdb\_ci\_topology\]
-   Tables specified by the **sn\_ni\_core.equipment\_tables** sys\_property, and any tables that extend the specified tables.
-   Tables that extend Equipment Holder \[cmdb\_ci\_equipment\_holder\].
-   Child tables that extend any of the following tables:
    -   Cable \[cmdb\_ci\_cable\]
    -   Equipment Holder \[cmdb\_ci\_equipment\_holder\]
    -   Strand \[cmdb\_ci\_strand\]

Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. Valid values:

-   description
-   href
-   id
-   name
-   note
-   place
-   relatedParty
-   resourceCharacteristic
-   resourceRelationship
-   resourceSpecification
-   startOperatingDate

Data type: String

Default: Returns all fields.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON\)

<table id="table_okb_1rw_f5b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td id="type-entry">

@type

</td><td id="type-descr-entry">

Type of resource.Valid values:

-   `cmdb_ci_cable` \(Cable\)
-   `cmdb_ci_interface_card` \(Interface Card\)
-   `cmdb_ci_ip_address` \(IP Address\)
-   `cmdb_ci_ni_logical_path` \(Logical Connection\)
-   `cmdb_ci_ni_interface` \(Network Interface\)
-   `cmdb_ci_ni_site` \(Network Site\)
-   `cmdb_ci_ni_physical_link` \(Physical Connection\)
-   `cmdb_ci_strand` \(Strand\)
-   `cmdb_ci_topology` \(Topology\)
-   Name of a table specified by the **sn\_ni\_core.equipment\_tables** sys\_property, or name of a table that extends the specified tables.
-   Name of a table that extends Equipment Holder \[cmdb\_ci\_equipment\_holder\].

Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the resource.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the resource. Located in one of the following tables depending on the type of resource.-   Cable \[cmdb\_ci\_cable\]
-   Equipment Holder \[cmdb\_ci\_equipment\_holder\]
-   Interface Card \[cmdb\_ci\_interface\_card\]
-   IP Address \[cmdb\_ci\_ip\_address\]
-   Logical Connection \[cmdb\_ci\_ni\_logical\_path\]
-   Network Interface \[cmdb\_ci\_ni\_interface\]
-   Network Site \[cmdb\_ci\_ni\_site\]
-   Physical Connection \[cmdb\_ci\_ni\_physical\_link\]
-   Strand \[cmdb\_ci\_strand\]
-   Topology \[cmdb\_ci\_topology\]
-   Tables specified by the **sn\_ni\_core.equipment\_tables** sys\_property, and any tables that extend the specified tables.
-   Tables that extend Equipment Holder \[cmdb\_ci\_equipment\_holder\].
-   Child tables that extend any of the following tables:
    -   Cable \[cmdb\_ci\_cable\]
    -   Equipment Holder \[cmdb\_ci\_equipment\_holder\]
    -   Strand \[cmdb\_ci\_strand\]

Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the resource.

Data type: String

</td></tr><tr><td>

note

</td><td>

List of notes about the resource. Data type: Array of Objects

```
"note": [
   {
      "text": "String"
   }
]
```

</td></tr><tr><td>

note.text

</td><td>

The note text.

Data type: String

</td></tr><tr><td>

place

</td><td>

Network site for the resource.

This parameter is not supported for Network Site, Physical Connection, or Logical Connection resources.

Data type: Object

```
"place": {
   "@referredType": "String",
   "href": "String",
   "id": "String"
}
```

</td></tr><tr><td>

place.@referredType

</td><td>

Type of place. This value is always `GeographicAddress`.Data type: String

</td></tr><tr><td>

place.href

</td><td>

Relative link to the place record.Data type: String

</td></tr><tr><td>

place.id

</td><td>

Sys\_id of the place record.

Data type: String

Table: Network Site \[cmdb\_ci\_ni\_site\]

</td></tr><tr><td id="related-party-parm">

relatedParty

</td><td>

Details about contacts for the resource.

Data type: Array of Objects

```
"relatedParty": [
   {
      "@referredType": "String",
      "href": "String",
      "id": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of related party. Located in the in the **Type** field.Data type: String

Table: In the type field of Group \[sys\_user\_group\] table.

</td></tr><tr><td>

relatedParty.href

</td><td>

Relative link to the related party record.Data type: String

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the related party record.

Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

resourceCharacteristic

</td><td>

List of characteristics of the resource. The following resource types require specific resource characteristics. -   For Physical Connection and Logical Connection resources, a `Port A` or `Port Z` characteristic is required. If the Lifecycle Stage Status of the resource is In Use, both `Port A` and `Port Z` are required.
-   For Equipment Holder resources, a `Container Type` characteristic is required.

Data type: Array of Objects

```
"resourceCharacteristic": [
   {
      "name": "String",
      "value": "String",
      "valueType": "String"
   }
]
```

</td></tr><tr><td>

resourceCharacteristic.name

</td><td>

Field name from the resource table specified by the **@type** parameter. You can't use the fields model\_id, name, network\_site, operation\_notes, operational\_status, short\_description, start\_date, or any sys\_ prefixed fields such as sys\_id.

Data type: String

</td></tr><tr><td>

resourceCharacteristic.value

</td><td>

The value of the characteristic.

Data type: String

</td></tr><tr><td>

resourceCharacteristic.valueType

</td><td>

Type of value.Valid values:

-   boolean
-   datetime
-   float
-   integer
-   ph\_number
-   reference
-   string

Data type: String

</td></tr><tr><td>

resourceRelationship

</td><td>

List of related resources. The following resource types require specific related resources. -   For Interface Card resources, a relationship to an Equipment Holder resource where Container Type is Slot or Sub Slot is required.
-   For Network Interface resources, a relationship to an Equipment or Interface Card resource is required.
-   For Equipment Holder resources where Container Type is Slot or Sub Slot, a relationship to an Equipment or Interface Card resource is required.

Data type: Array

```
"resourceRelationship": [
  {
    "relationshipType": "String",
    "resource": {Object}
  }
]
```

</td></tr><tr><td>

resourceRelationship.relationshipType

</td><td>

Type of relationship between the two resources in the format `[this resource descriptor]::[related resource descriptor]`. For example, `Contains::Contained by` indicates that the related resource is the child of this resource.

Valid values for the descriptors are located in the CI Relationship Type \[cmdb\_rel\_type\] table in the **Parent descriptor** and **Child descriptor** columns.

Data type: String

</td></tr><tr><td>

resourceRelationship.resource

</td><td>

Details about the related resource. The related resource must be one of the following resource types.

-   Cable
-   Equipment
-   Equipment Holder
-   Interface Card
-   Logical Connection
-   Network Interface
-   Network Site
-   Physical Connection
-   Strand
-   Topology

Data type: Object

```
"resource": {
   "id": "String",
   "href": "String"
}
```

</td></tr><tr><td>

resourceRelationship.resource.id

</td><td>

Sys\_id of the related resource. Located in one of the following tables depending on the type of related resource.

-   Interface Card \[cmdb\_ci\_interface\_card\]
-   Logical Connection \[cmdb\_ci\_ni\_logical\_path\]
-   Network Interface \[cmdb\_ci\_ni\_interface\]
-   Network Site \[cmdb\_ci\_ni\_site\]
-   Physical Connection \[cmdb\_ci\_ni\_physical\_link\]
-   Tables specified by the **sn\_ni\_core.equipment\_tables** sys\_property, and any tables that extend the specified tables.
-   Tables that extend Equipment Holder \[cmdb\_ci\_equipment\_holder\]

Data type: String

</td></tr><tr><td>

resourceRelationship.resource.href

</td><td>

Relative link to the related resource record.Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

Resource specification. Data type: Object

```
"resourceSpecification": {
   "id": "String"
}
```

</td></tr><tr><td>

resourceSpecification.id

</td><td>

Sys\_id of the associated model for the resource. Located in one of the following tables depending on the type of model.

-   Cable Models \[sn\_ent\_cable\_model\]
-   Equipment Holder Models \[sn\_ent\_nw\_holder\_model\]
-   Equipment Models \[sn\_ent\_nw\_equipment\_model\]
-   Interface Card Models \[sn\_ent\_nw\_interface\_model\]
-   Logical Connection Models \[sn\_ent\_logical\_nw\_connection\_model\]
-   Network Interface Models \[sn\_ent\_nw\_interface\_model\]
-   Physical Connection Models \[sn\_ent\_physical\_nw\_connection\_model\]
-   Strand Models \[sn\_ent\_strand\_model\]
-   Topology Models \[sn\_ent\_network\_topology\_model\]

Data type: String

</td></tr><tr><td>

startOperatingDate

</td><td>

Date and time that the resource first started operating.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves a specified resource record.

```
curl "https://instance.service-now.com/api/sn_ni_core/resource/915da8e140ddc910f8772175cacd72de" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body.

```
{
   "href": "/api/sn_ni_core/resource/915da8e140ddc910f8772175cacd72de",
   "id": "915da8e140ddc910f8772175cacd72de",
   "name": "DLLSTXMR/ESS7450/IOM-01/MDA-01/NI-01",
   "place": {
      "id": "c23683c54051c910f8772175cacd725c",
      "href": "/api/now/table/cmdb_ci_ni_site/c23683c54051c910f8772175cacd725c",
      "@referredType": "GeographicAddress"
   },
   "resourceCharacteristic": [
      {
         "name": "attested",
         "valueType": "boolean",
         "value": "false"
      },
      {
         "name": "availability",
         "valueType": "string",
         "value": "used"
      },
      {
         "name": "cabled",
         "valueType": "boolean",
         "value": "false"
      },
      {
         "name": "can_print",
         "valueType": "boolean",
         "value": "false"
      },
      {
         "name": "connector_type",
         "valueType": "string",
         "value": "sc"
      },
      {
         "name": "cost_cc",
         "valueType": "string",
         "value": "USD"
      },
      {
         "name": "equipment_clli",
         "valueType": "string",
         "value": "DLLSTXESS01"
      },
      {
         "name": "fault_count",
         "valueType": "integer",
         "value": "0"
      },
      {
         "name": "install_status",
         "valueType": "integer",
         "value": "1"
      },
      {
         "name": "life_cycle_stage",
         "valueType": "reference",
         "value": "Operational"
      },
      {
         "name": "life_cycle_stage_status",
         "valueType": "reference",
         "value": "In Use"
      },
      {
         "name": "manufacturer",
         "valueType": "reference",
         "value": "a2f6a4914055c910f8772175cacd723a"
      },
      {
         "name": "monitor",
         "valueType": "boolean",
         "value": "false"
      },
      {
         "name": "network_domain",
         "valueType": "string",
         "value": "core"
      },
      {
         "name": "ni_type",
         "valueType": "reference",
         "value": "646cf25fe42e0510f877e70ec9bcaca8"
      },
      {
         "name": "port_bandwidth",
         "valueType": "reference",
         "value": "ff39ae92eb900110700ca73bc152286d"
      },
      {
         "name": "replaceable",
         "valueType": "boolean",
         "value": "false"
      },
      {
         "name": "skip_sync",
         "valueType": "boolean",
         "value": "false"
      },
      {
         "name": "telco_equipment",
         "valueType": "reference",
         "value": "583e7b95405dc910f8772175cacd7292"
      },
      {
         "name": "unverified",
         "valueType": "boolean",
         "value": "false"
      },
      {
         "name": "virtual",
         "valueType": "boolean",
         "value": "false"
      }
   ],
   "resourceRelationship": [
      {
         "relationshipType": "Contained by::Contains",
         "resource": {
            "id": "81baac6140ddc910f8772175cacd728e",
            "href": "/api/sn_ni_core/resource/81baac6140ddc910f8772175cacd728e"
         }
      },
      {
         "relationshipType": "Contained by::Contains",
         "resource": {
            "id": "bf624bc640194d10f8772175cacd7225",
            "href": "/api/sn_ni_core/resource/bf624bc640194d10f8772175cacd7225"
         }
      }
   ],
   "resourceSpecification": {
      "id": "980416b0874e8110d28eb259dabb356b",
      "href": "/api/now/table/sn_ni_core_network_inventory_product_model/980416b0874e8110d28eb259dabb356b",
      "@referredType": "NetworkInterfaceModel"
   },
   "@type": "cmdb_ci_ni_interface"
}
```

## Resource Inventory Open API - PATCH /sn\_ni\_core/resource/\{id\}

Updates a specified resource record.

### URL format

Default URL: `/api/sn_ni_core/resource/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the resource. Located in one of the following tables depending on the type of resource.-   Cable \[cmdb\_ci\_cable\]
-   Equipment Holder \[cmdb\_ci\_equipment\_holder\]
-   Interface Card \[cmdb\_ci\_interface\_card\]
-   IP Address \[cmdb\_ci\_ip\_address\]
-   Logical Connection \[cmdb\_ci\_ni\_logical\_path\]
-   Network Interface \[cmdb\_ci\_ni\_interface\]
-   Network Site \[cmdb\_ci\_ni\_site\]
-   Physical Connection \[cmdb\_ci\_ni\_physical\_link\]
-   Strand \[cmdb\_ci\_strand\]
-   Topology \[cmdb\_ci\_topology\]
-   Tables specified by the **sn\_ni\_core.equipment\_tables** sys\_property, and any tables that extend the specified tables.
-   Tables that extend Equipment Holder \[cmdb\_ci\_equipment\_holder\].
-   Child tables that extend any of the following tables:
    -   Cable \[cmdb\_ci\_cable\]
    -   Equipment Holder \[cmdb\_ci\_equipment\_holder\]
    -   Strand \[cmdb\_ci\_strand\]

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td id="type-entry">

@type

</td><td id="type-descr-entry">

Type of resource.Valid values:

-   `cmdb_ci_cable` \(Cable\)
-   `cmdb_ci_interface_card` \(Interface Card\)
-   `cmdb_ci_ip_address` \(IP Address\)
-   `cmdb_ci_ni_logical_path` \(Logical Connection\)
-   `cmdb_ci_ni_interface` \(Network Interface\)
-   `cmdb_ci_ni_site` \(Network Site\)
-   `cmdb_ci_ni_physical_link` \(Physical Connection\)
-   `cmdb_ci_strand` \(Strand\)
-   `cmdb_ci_topology` \(Topology\)
-   Name of a table specified by the **sn\_ni\_core.equipment\_tables** sys\_property, or name of a table that extends the specified tables.
-   Name of a table that extends Equipment Holder \[cmdb\_ci\_equipment\_holder\].

Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the resource.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the resource.

Data type: String

</td></tr><tr><td>

note

</td><td>

List of notes about the resource. Data type: Array of Objects

```
"note": [
   {
      "text": "String"
   }
]
```

</td></tr><tr><td id="note-text-entry">

note.text

</td><td>

Required if the **note** parameter is used.The note text.

Data type: String

</td></tr><tr><td>

place

</td><td>

Network site for the resource.

This parameter is not supported for Network Site, Physical Connection, or Logical Connection resources.

Data type: Object

```
"place": {
   "@referredType": "String",
   "href": "String",
   "id": "String"
}
```

</td></tr><tr><td>

place.@referredType

</td><td>

Type of place. This value is always `GeographicAddress`.Data type: String

</td></tr><tr><td>

place.href

</td><td>

Relative link to the place record.Data type: String

</td></tr><tr><td id="place-id-entry">

place.id

</td><td>

Required if the **place** parameter is used.Sys\_id of the place record.

Data type: String

Table: Network Site \[cmdb\_ci\_ni\_site\]

</td></tr><tr><td>

relatedParty

</td><td>

Details about contacts for the resource.

Data type: Array of Objects

```
"relatedParty": [
   {
      "@referredType": "String",
      "href": "String",
      "id": "String",
      "role": "String"
   }
]
```

 **Note:** Removing relatedParty records from a resource is not supported by this endpoint. Records can be manually deleted from the Teams \[cmdb\_rel\_team\] table.

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of related party. Located in the in the **Type** field.Data type: String

Table: In the type field of Group \[sys\_user\_group\] table.

</td></tr><tr><td>

relatedParty.href

</td><td>

Relative link to the related party record.Data type: String

</td></tr><tr><td id="rel-party-id-parm">

relatedParty.id

</td><td>

Required if the **relatedParty** parameter is used.Sys\_id of the related party record.

Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

relatedParty.role

</td><td>

Role of the related party. Data type: String

Table: In the Group type field of the Teams \[cmdb\_rel\_team\] table.

</td></tr><tr><td>

resourceCharacteristic

</td><td>

List of characteristics of the resource. The following resource types require specific resource characteristics. -   For Physical Connection and Logical Connection resources, a `Port A` or `Port Z` characteristic is required. If the Lifecycle Stage Status of the resource is In Use, both `Port A` and `Port Z` are required.
-   For Equipment Holder resources, a `Container Type` characteristic is required.

Data type: Array of Objects

```
"resourceCharacteristic": [
   {
      "name": "String",
      "value": "String",
      "valueType": "String"
   }
]
```

</td></tr><tr><td id="res-char-name-parm">

resourceCharacteristic.name

</td><td>

Required if the **resourceCharacteristic** parameter is used.Field name from the resource table specified by the **@type** parameter. You can't use the fields model\_id, name, network\_site, operation\_notes, operational\_status, short\_description, start\_date, or any sys\_ prefixed fields such as sys\_id.

Data type: String

</td></tr><tr><td id="res-char-value-parm">

resourceCharacteristic.value

</td><td>

Required if the **resourceCharacteristic** parameter is used.The value of the characteristic.

Data type: String

</td></tr><tr><td>

resourceCharacteristic.valueType

</td><td>

Type of value.Valid values:

-   boolean
-   datetime
-   float
-   integer
-   ph\_number
-   reference
-   string

Data type: String

</td></tr><tr><td>

resourceRelationship

</td><td>

List of related resources. The following resource types require specific related resources. -   For Interface Card resources, a relationship to an Equipment Holder resource where Container Type is Slot or Sub Slot is required.
-   For Network Interface resources, a relationship to an Equipment or Interface Card resource is required.
-   For Equipment Holder resources where Container Type is Slot or Sub Slot, a relationship to an Equipment or Interface Card resource is required.

Data type: Array

```
"resourceRelationship": [
  {
    "relationshipType": "String",
    "resource": {Object}
  }
]
```

</td></tr><tr><td id="rel-type-parm">

resourceRelationship.relationshipType

</td><td>

Required if the **resourceRelationship** parameter is used.Type of relationship between the two resources in the format `[this resource descriptor]::[related resource descriptor]`. For example, `Contains::Contained by` indicates that the related resource is the child of this resource.

Valid values for the descriptors are located in the CI Relationship Type \[cmdb\_rel\_type\] table in the **Parent descriptor** and **Child descriptor** columns.

Data type: String

</td></tr><tr><td id="rel-resource-parm">

resourceRelationship.resource

</td><td>

Required if the **resourceRelationship** parameter is used.Details about the related resource. The related resource must be one of the following resource types.

-   Cable
-   Equipment
-   Equipment Holder
-   Interface Card
-   Logical Connection
-   Network Interface
-   Network Site
-   Physical Connection
-   Strand
-   Topology

Data type: Object

```
"resource": {
   "id": "String",
   "href": "String"
}
```

</td></tr><tr><td id="rel-resource-id-parm">

resourceRelationship.resource.id

</td><td>

Required if the **resourceRelationship** parameter is used.Sys\_id of the related resource. Located in one of the following tables depending on the type of related resource.

-   Interface Card \[cmdb\_ci\_interface\_card\]
-   Logical Connection \[cmdb\_ci\_ni\_logical\_path\]
-   Network Interface \[cmdb\_ci\_ni\_interface\]
-   Network Site \[cmdb\_ci\_ni\_site\]
-   Physical Connection \[cmdb\_ci\_ni\_physical\_link\]
-   Tables specified by the **sn\_ni\_core.equipment\_tables** sys\_property, and any tables that extend the specified tables.
-   Tables that extend Equipment Holder \[cmdb\_ci\_equipment\_holder\]

Data type: String

</td></tr><tr><td>

resourceRelationship.resource.href

</td><td>

Relative link to the related resource record.Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

Resource specification. Data type: Object

```
"resourceSpecification": {
   "id": "String"
}
```

</td></tr><tr><td id="res-spec-id-parm">

resourceSpecification.id

</td><td>

Required if the **resourceSpecification** parameter is used.Sys\_id of the associated model for the resource. Located in one of the following tables depending on the type of model.

-   Cable Models \[sn\_ent\_cable\_model\]
-   Equipment Holder Models \[sn\_ent\_nw\_holder\_model\]
-   Equipment Models \[sn\_ent\_nw\_equipment\_model\]
-   Interface Card Models \[sn\_ent\_nw\_interface\_model\]
-   Logical Connection Models \[sn\_ent\_logical\_nw\_connection\_model\]
-   Network Interface Models \[sn\_ent\_nw\_interface\_model\]
-   Physical Connection Models \[sn\_ent\_physical\_nw\_connection\_model\]
-   Strand Models \[sn\_ent\_strand\_model\]
-   Topology Models \[sn\_ent\_network\_topology\_model\]

Data type: String

</td></tr><tr><td>

startOperatingDate

</td><td>

Date and time that the resource first started operating.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/merge-patch+json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|415|The request body is in an unsupported format or the Content-Type request header is set incorrectly.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td id="d4470e138">

@type

</td><td id="d4470e141">

Type of resource.Valid values:

-   `cmdb_ci_cable` \(Cable\)
-   `cmdb_ci_interface_card` \(Interface Card\)
-   `cmdb_ci_ip_address` \(IP Address\)
-   `cmdb_ci_ni_logical_path` \(Logical Connection\)
-   `cmdb_ci_ni_interface` \(Network Interface\)
-   `cmdb_ci_ni_site` \(Network Site\)
-   `cmdb_ci_ni_physical_link` \(Physical Connection\)
-   `cmdb_ci_strand` \(Strand\)
-   `cmdb_ci_topology` \(Topology\)
-   Name of a table specified by the **sn\_ni\_core.equipment\_tables** sys\_property, or name of a table that extends the specified tables.
-   Name of a table that extends Equipment Holder \[cmdb\_ci\_equipment\_holder\].

Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the resource.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the resource. Located in one of the following tables depending on the type of resource.-   Cable \[cmdb\_ci\_cable\]
-   Equipment Holder \[cmdb\_ci\_equipment\_holder\]
-   Interface Card \[cmdb\_ci\_interface\_card\]
-   IP Address \[cmdb\_ci\_ip\_address\]
-   Logical Connection \[cmdb\_ci\_ni\_logical\_path\]
-   Network Interface \[cmdb\_ci\_ni\_interface\]
-   Network Site \[cmdb\_ci\_ni\_site\]
-   Physical Connection \[cmdb\_ci\_ni\_physical\_link\]
-   Strand \[cmdb\_ci\_strand\]
-   Topology \[cmdb\_ci\_topology\]
-   Tables specified by the **sn\_ni\_core.equipment\_tables** sys\_property, and any tables that extend the specified tables.
-   Tables that extend Equipment Holder \[cmdb\_ci\_equipment\_holder\].
-   Child tables that extend any of the following tables:
    -   Cable \[cmdb\_ci\_cable\]
    -   Equipment Holder \[cmdb\_ci\_equipment\_holder\]
    -   Strand \[cmdb\_ci\_strand\]

Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the resource.

Data type: String

</td></tr><tr><td>

note

</td><td>

List of notes about the resource. Data type: Array of Objects

```
"note": [
   {
      "text": "String"
   }
]
```

</td></tr><tr><td>

note.text

</td><td>

The note text.

Data type: String

</td></tr><tr><td>

place

</td><td>

Network site for the resource.

This parameter is not supported for Network Site, Physical Connection, or Logical Connection resources.

Data type: Object

```
"place": {
   "@referredType": "String",
   "href": "String",
   "id": "String"
}
```

</td></tr><tr><td>

place.@referredType

</td><td>

Type of place. This value is always `GeographicAddress`.Data type: String

</td></tr><tr><td>

place.href

</td><td>

Relative link to the place record.Data type: String

</td></tr><tr><td>

place.id

</td><td>

Sys\_id of the place record.

Data type: String

Table: Network Site \[cmdb\_ci\_ni\_site\]

</td></tr><tr><td id="related-party-parm">

relatedParty

</td><td>

Details about contacts for the resource.

Data type: Array of Objects

```
"relatedParty": [
   {
      "@referredType": "String",
      "href": "String",
      "id": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of related party. Located in the in the **Type** field.Data type: String

Table: In the type field of Group \[sys\_user\_group\] table.

</td></tr><tr><td>

relatedParty.href

</td><td>

Relative link to the related party record.Data type: String

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the related party record.

Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

relatedParty.role

</td><td>

Role of the related party. Data type: String

Table: In the Group type field of the Teams \[cmdb\_rel\_team\] table.

</td></tr><tr><td>

resourceCharacteristic

</td><td>

List of characteristics of the resource. The following resource types require specific resource characteristics. -   For Physical Connection and Logical Connection resources, a `Port A` or `Port Z` characteristic is required. If the Lifecycle Stage Status of the resource is In Use, both `Port A` and `Port Z` are required.
-   For Equipment Holder resources, a `Container Type` characteristic is required.

Data type: Array of Objects

```
"resourceCharacteristic": [
   {
      "name": "String",
      "value": "String",
      "valueType": "String"
   }
]
```

</td></tr><tr><td>

resourceCharacteristic.name

</td><td>

Field name from the resource table specified by the **@type** parameter. You can't use the fields model\_id, name, network\_site, operation\_notes, operational\_status, short\_description, start\_date, or any sys\_ prefixed fields such as sys\_id.

Data type: String

</td></tr><tr><td>

resourceCharacteristic.value

</td><td>

The value of the characteristic.

Data type: String

</td></tr><tr><td>

resourceCharacteristic.valueType

</td><td>

Type of value.Valid values:

-   boolean
-   datetime
-   float
-   integer
-   ph\_number
-   reference
-   string

Data type: String

</td></tr><tr><td>

resourceRelationship

</td><td>

List of related resources. The following resource types require specific related resources. -   For Interface Card resources, a relationship to an Equipment Holder resource where Container Type is Slot or Sub Slot is required.
-   For Network Interface resources, a relationship to an Equipment or Interface Card resource is required.
-   For Equipment Holder resources where Container Type is Slot or Sub Slot, a relationship to an Equipment or Interface Card resource is required.

Data type: Array

```
"resourceRelationship": [
  {
    "relationshipType": "String",
    "resource": {Object}
  }
]
```

</td></tr><tr><td>

resourceRelationship.relationshipType

</td><td>

Type of relationship between the two resources in the format `[this resource descriptor]::[related resource descriptor]`. For example, `Contains::Contained by` indicates that the related resource is the child of this resource.

Valid values for the descriptors are located in the CI Relationship Type \[cmdb\_rel\_type\] table in the **Parent descriptor** and **Child descriptor** columns.

Data type: String

</td></tr><tr><td>

resourceRelationship.resource

</td><td>

Details about the related resource. The related resource must be one of the following resource types.

-   Cable
-   Equipment
-   Equipment Holder
-   Interface Card
-   Logical Connection
-   Network Interface
-   Network Site
-   Physical Connection
-   Strand
-   Topology

Data type: Object

```
"resource": {
   "id": "String",
   "href": "String"
}
```

</td></tr><tr><td>

resourceRelationship.resource.id

</td><td>

Sys\_id of the related resource. Located in one of the following tables depending on the type of related resource.

-   Interface Card \[cmdb\_ci\_interface\_card\]
-   Logical Connection \[cmdb\_ci\_ni\_logical\_path\]
-   Network Interface \[cmdb\_ci\_ni\_interface\]
-   Network Site \[cmdb\_ci\_ni\_site\]
-   Physical Connection \[cmdb\_ci\_ni\_physical\_link\]
-   Tables specified by the **sn\_ni\_core.equipment\_tables** sys\_property, and any tables that extend the specified tables.
-   Tables that extend Equipment Holder \[cmdb\_ci\_equipment\_holder\]

Data type: String

</td></tr><tr><td>

resourceRelationship.resource.href

</td><td>

Relative link to the related resource record.Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

Resource specification. Data type: Object

```
"resourceSpecification": {
   "id": "String"
}
```

</td></tr><tr><td>

resourceSpecification.id

</td><td>

Sys\_id of the associated model for the resource. Located in one of the following tables depending on the type of model.

-   Cable Models \[sn\_ent\_cable\_model\]
-   Equipment Holder Models \[sn\_ent\_nw\_holder\_model\]
-   Equipment Models \[sn\_ent\_nw\_equipment\_model\]
-   Interface Card Models \[sn\_ent\_nw\_interface\_model\]
-   Logical Connection Models \[sn\_ent\_logical\_nw\_connection\_model\]
-   Network Interface Models \[sn\_ent\_nw\_interface\_model\]
-   Physical Connection Models \[sn\_ent\_physical\_nw\_connection\_model\]
-   Strand Models \[sn\_ent\_strand\_model\]
-   Topology Models \[sn\_ent\_network\_topology\_model\]

Data type: String

</td></tr><tr><td>

startOperatingDate

</td><td>

Date and time that the resource first started operating.Data type: String

</td></tr></tbody>
</table>### cURL request

This example updates the name of a resource.

```
curl "http://instance.servicenow.com/api/sn_ni_core/resource/583e7b95405dc910f8772175cacd7292" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type: application/merge-patch+json" \
--user 'username':'password' \
--data '{"name": "new name"}'
```

Response body.

```
{
  "href": "/api/sn_ni_core/resource/583e7b95405dc910f8772175cacd7292",
  "id": "583e7b95405dc910f8772175cacd7292",
  "name": "new name",
  "note": [
    {
      "text": "TECHNICIAN SCHECULED TO BE ONSITE THE WEEK OF APRIL 4, 2022."
    }
  ],
  "place": {
    "id": "c23683c54051c910f8772175cacd725c",
    "href": "/api/now/table/cmdb_ci_ni_site/c23683c54051c910f8772175cacd725c",
    "@referredType": "GeographicAddress"
  },
  "resourceCharacteristic": [
    {
      "name": "alarmable",
      "valueType": "boolean",
      "value": "true"
    },
    {
      "name": "attested",
      "valueType": "boolean",
      "value": "false"
    },
    {
      "name": "can_hub",
      "valueType": "boolean",
      "value": "false"
    },
    {
      "name": "can_partitionvlans",
      "valueType": "boolean",
      "value": "false"
    },
    {
      "name": "can_print",
      "valueType": "boolean",
      "value": "false"
    },
    {
      "name": "can_route",
      "valueType": "boolean",
      "value": "false"
    },
    {
      "name": "can_switch",
      "valueType": "boolean",
      "value": "false"
    },
    {
      "name": "comments",
      "valueType": "string",
      "value": "ETHERNET SWITCH"
    },
    {
      "name": "cost_cc",
      "valueType": "string",
      "value": "USD"
    },
    {
      "name": "cpu_count",
      "valueType": "integer",
      "value": "1"
    },
    {
      "name": "equipment_clli",
      "valueType": "string",
      "value": "DLLSTXESS01"
    },
    {
      "name": "fault_count",
      "valueType": "integer",
      "value": "0"
    },
    {
      "name": "firmware_manufacturer",
      "valueType": "reference",
      "value": "0c441abbc6112275000025157c651c89"
    },
    {
      "name": "firmware_version",
      "valueType": "string",
      "value": "A09DX887"
    },
    {
      "name": "hardware_status",
      "valueType": "string",
      "value": "installed"
    },
    {
      "name": "install_status",
      "valueType": "integer",
      "value": "1"
    },
    {
      "name": "internet_facing",
      "valueType": "boolean",
      "value": "true"
    },
    {
      "name": "inventory_category",
      "valueType": "string",
      "value": "equipment"
    },
    {
      "name": "last_service_date",
      "valueType": "datetime",
      "value": "2022-02-18T16:36:54.000Z"
    },
    {
      "name": "life_cycle_stage",
      "valueType": "reference",
      "value": "Deploy"
    },
    {
      "name": "life_cycle_stage_status",
      "valueType": "reference",
      "value": "Reserved"
    },
    {
      "name": "managed_by",
      "valueType": "reference",
      "value": "46c9e158a9fe198101d44d0d22cb640d"
    },
    {
      "name": "manufacturer",
      "valueType": "reference",
      "value": "b7e831bdc0a80169015ae101f3c4d6cd"
    },
    {
      "name": "model_number",
      "valueType": "string",
      "value": "7450ESS-1"
    },
    {
      "name": "monitor",
      "valueType": "boolean",
      "value": "false"
    },
    {
      "name": "network_domain",
      "valueType": "string",
      "value": "core"
    },
    {
      "name": "ni_function",
      "valueType": "reference",
      "value": "2d22153940990d10f8772175cacd728b"
    },
    {
      "name": "ni_role",
      "valueType": "reference",
      "value": "c68e3f15405dc910f8772175cacd72f1"
    },
    {
      "name": "ni_type",
      "valueType": "reference",
      "value": "3772e8d54015c910f8772175cacd721c"
    },
    {
      "name": "ram",
      "valueType": "integer",
      "value": "3000"
    },
    {
      "name": "replaceable",
      "valueType": "boolean",
      "value": "true"
    },
    {
      "name": "serial_number",
      "valueType": "string",
      "value": "7894564568225"
    },
    {
      "name": "skip_sync",
      "valueType": "boolean",
      "value": "false"
    },
    {
      "name": "spare",
      "valueType": "boolean",
      "value": "true"
    },
    {
      "name": "template_id",
      "valueType": "reference",
      "value": "49433535e5d28110f877657a33339131"
    },
    {
      "name": "unit_position",
      "valueType": "integer",
      "value": "2"
    },
    {
      "name": "unverified",
      "valueType": "boolean",
      "value": "false"
    }
  ],
  "resourceRelationship": [
    {
      "relationshipType": "Contains::Contained by",
      "resource": {
        "id": "f5d1c429405dc910f8772175cacd723f",
        "href": "/api/sn_ni_core/resource/f5d1c429405dc910f8772175cacd723f"
      }
    },
    {
      "relationshipType": "Contains::Contained by",
      "resource": {
        "id": "d6e100e5405dc910f8772175cacd72e9",
        "href": "/api/sn_ni_core/resource/d6e100e5405dc910f8772175cacd72e9"
      }
    },
    {
      "relationshipType": "Contained by::Contains",
      "resource": {
        "id": "5b10e8154015c910f8772175cacd724d",
        "href": "/api/sn_ni_core/resource/5b10e8154015c910f8772175cacd724d"
      }
    }
  ],
  "resourceSpecification": {
    "id": "0ae34df1e5528110f877657a33339119",
    "href": "/api/now/table/cmdb_model/0ae34df1e5528110f877657a33339119",
    "@referredType": "EquipmentModel"
  },
  "@type": "cmdb_ci_ni_telco_equipment"
}
```

## Resource Inventory Open API - POST /sn\_ni\_core/resource

Creates a resource record.

### URL format

Default URL: `/api/sn_ni_core/resource`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td id="type-entry">

@type

</td><td id="type-descr-entry">

Type of resource.Valid values:

-   `cmdb_ci_cable` \(Cable\)
-   `cmdb_ci_interface_card` \(Interface Card\)
-   `cmdb_ci_ip_address` \(IP Address\)
-   `cmdb_ci_ni_logical_path` \(Logical Connection\)
-   `cmdb_ci_ni_interface` \(Network Interface\)
-   `cmdb_ci_ni_site` \(Network Site\)
-   `cmdb_ci_ni_physical_link` \(Physical Connection\)
-   `cmdb_ci_strand` \(Strand\)
-   `cmdb_ci_topology` \(Topology\)
-   Name of a table specified by the **sn\_ni\_core.equipment\_tables** sys\_property, or name of a table that extends the specified tables.
-   Name of a table that extends Equipment Holder \[cmdb\_ci\_equipment\_holder\].

Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the resource.Data type: String

</td></tr><tr><td id="name-entry">

name

</td><td>

Required.Name of the resource.

Data type: String

</td></tr><tr><td>

note

</td><td>

List of notes about the resource. Data type: Array of Objects

```
"note": [
   {
      "text": "String"
   }
]
```

</td></tr><tr><td id="note-text-entry">

note.text

</td><td>

Required if the **note** parameter is used.The note text.

Data type: String

</td></tr><tr><td id="place-entry">

place

</td><td>

Required for Equipment Holder resources where Container Type is Cage, Bay, Cabinet, Rack, Line Up, or Inventory Model Bundle. Required for all Equipment resources.Network site for the resource.

This parameter is not supported for Network Site, Physical Connection, or Logical Connection resources.

Data type: Object

```
"place": {
   "@referredType": "String",
   "href": "String",
   "id": "String"
}
```

</td></tr><tr><td>

place.@referredType

</td><td>

Type of place. This value is always `GeographicAddress`.Data type: String

</td></tr><tr><td>

place.href

</td><td>

Relative link to the place record.Data type: String

</td></tr><tr><td id="place-id-entry">

place.id

</td><td>

Required if the **place** parameter is used.Sys\_id of the place record.

Data type: String

Table: Network Site \[cmdb\_ci\_ni\_site\]

</td></tr><tr><td id="related-party-parm">

relatedParty

</td><td>

Details about contacts for the resource.

Data type: Array of Objects

```
"relatedParty": [
   {
      "@referredType": "String",
      "href": "String",
      "id": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of related party. Located in the in the **Type** field.Data type: String

Table: In the type field of Group \[sys\_user\_group\] table.

</td></tr><tr><td>

relatedParty.href

</td><td>

Relative link to the related party record.Data type: String

</td></tr><tr><td id="rel-party-id-parm">

relatedParty.id

</td><td>

Required if the **relatedParty** parameter is used.Sys\_id of the related party record.

Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

resourceCharacteristic

</td><td>

List of characteristics of the resource. The following resource types require specific resource characteristics. -   For Physical Connection and Logical Connection resources, a `Port A` or `Port Z` characteristic is required. If the Lifecycle Stage Status of the resource is In Use, both `Port A` and `Port Z` are required.
-   For Equipment Holder resources, a `Container Type` characteristic is required.

Data type: Array of Objects

```
"resourceCharacteristic": [
   {
      "name": "String",
      "value": "String",
      "valueType": "String"
   }
]
```

</td></tr><tr><td id="res-char-name-parm">

resourceCharacteristic.name

</td><td>

Required if the **resourceCharacteristic** parameter is used.Field name from the resource table specified by the **@type** parameter. You can't use the fields model\_id, name, network\_site, operation\_notes, operational\_status, short\_description, start\_date, or any sys\_ prefixed fields such as sys\_id.

Data type: String

</td></tr><tr><td id="res-char-value-parm">

resourceCharacteristic.value

</td><td>

Required if the **resourceCharacteristic** parameter is used.The value of the characteristic.

Data type: String

</td></tr><tr><td>

resourceCharacteristic.valueType

</td><td>

Type of value.Valid values:

-   boolean
-   datetime
-   float
-   integer
-   ph\_number
-   reference
-   string

Data type: String

</td></tr><tr><td>

resourceRelationship

</td><td>

List of related resources. The following resource types require specific related resources. -   For Interface Card resources, a relationship to an Equipment Holder resource where Container Type is Slot or Sub Slot is required.
-   For Network Interface resources, a relationship to an Equipment or Interface Card resource is required.
-   For Equipment Holder resources where Container Type is Slot or Sub Slot, a relationship to an Equipment or Interface Card resource is required.

Data type: Array

```
"resourceRelationship": [
  {
    "relationshipType": "String",
    "resource": {Object}
  }
]
```

</td></tr><tr><td id="rel-type-parm">

resourceRelationship.relationshipType

</td><td>

Required if the **resourceRelationship** parameter is used.Type of relationship between the two resources in the format `[this resource descriptor]::[related resource descriptor]`. For example, `Contains::Contained by` indicates that the related resource is the child of this resource.

Valid values for the descriptors are located in the CI Relationship Type \[cmdb\_rel\_type\] table in the **Parent descriptor** and **Child descriptor** columns.

Data type: String

</td></tr><tr><td id="rel-resource-parm">

resourceRelationship.resource

</td><td>

Required if the **resourceRelationship** parameter is used.Details about the related resource. The related resource must be one of the following resource types.

-   Cable
-   Equipment
-   Equipment Holder
-   Interface Card
-   Logical Connection
-   Network Interface
-   Network Site
-   Physical Connection
-   Strand
-   Topology

Data type: Object

```
"resource": {
   "id": "String",
   "href": "String"
}
```

</td></tr><tr><td id="rel-resource-id-parm">

resourceRelationship.resource.id

</td><td>

Required if the **resourceRelationship** parameter is used.Sys\_id of the related resource. Located in one of the following tables depending on the type of related resource.

-   Interface Card \[cmdb\_ci\_interface\_card\]
-   Logical Connection \[cmdb\_ci\_ni\_logical\_path\]
-   Network Interface \[cmdb\_ci\_ni\_interface\]
-   Network Site \[cmdb\_ci\_ni\_site\]
-   Physical Connection \[cmdb\_ci\_ni\_physical\_link\]
-   Tables specified by the **sn\_ni\_core.equipment\_tables** sys\_property, and any tables that extend the specified tables.
-   Tables that extend Equipment Holder \[cmdb\_ci\_equipment\_holder\]

Data type: String

</td></tr><tr><td>

resourceRelationship.resource.href

</td><td>

Relative link to the related resource record.Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

Resource specification. Data type: Object

```
"resourceSpecification": {
   "id": "String"
}
```

</td></tr><tr><td id="res-spec-id-parm">

resourceSpecification.id

</td><td>

Required if the **resourceSpecification** parameter is used.Sys\_id of the associated model for the resource. Located in one of the following tables depending on the type of model.

-   Cable Models \[sn\_ent\_cable\_model\]
-   Equipment Holder Models \[sn\_ent\_nw\_holder\_model\]
-   Equipment Models \[sn\_ent\_nw\_equipment\_model\]
-   Interface Card Models \[sn\_ent\_nw\_interface\_model\]
-   Logical Connection Models \[sn\_ent\_logical\_nw\_connection\_model\]
-   Network Interface Models \[sn\_ent\_nw\_interface\_model\]
-   Physical Connection Models \[sn\_ent\_physical\_nw\_connection\_model\]
-   Strand Models \[sn\_ent\_strand\_model\]
-   Topology Models \[sn\_ent\_network\_topology\_model\]

Data type: String

</td></tr><tr><td>

startOperatingDate

</td><td>

Date and time that the resource first started operating.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|
|Location|URL of the created resource.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|215|Request successfully received for processing. The request will be completed asynchronously.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|

### Response body parameters \(JSON\)

<table id="table_okb_1rw_f5b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td id="d4470e138">

@type

</td><td id="d4470e141">

Type of resource.Valid values:

-   `cmdb_ci_cable` \(Cable\)
-   `cmdb_ci_interface_card` \(Interface Card\)
-   `cmdb_ci_ip_address` \(IP Address\)
-   `cmdb_ci_ni_logical_path` \(Logical Connection\)
-   `cmdb_ci_ni_interface` \(Network Interface\)
-   `cmdb_ci_ni_site` \(Network Site\)
-   `cmdb_ci_ni_physical_link` \(Physical Connection\)
-   `cmdb_ci_strand` \(Strand\)
-   `cmdb_ci_topology` \(Topology\)
-   Name of a table specified by the **sn\_ni\_core.equipment\_tables** sys\_property, or name of a table that extends the specified tables.
-   Name of a table that extends Equipment Holder \[cmdb\_ci\_equipment\_holder\].

Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the resource.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the resource. Located in one of the following tables depending on the type of resource.-   Cable \[cmdb\_ci\_cable\]
-   Equipment Holder \[cmdb\_ci\_equipment\_holder\]
-   Interface Card \[cmdb\_ci\_interface\_card\]
-   IP Address \[cmdb\_ci\_ip\_address\]
-   Logical Connection \[cmdb\_ci\_ni\_logical\_path\]
-   Network Interface \[cmdb\_ci\_ni\_interface\]
-   Network Site \[cmdb\_ci\_ni\_site\]
-   Physical Connection \[cmdb\_ci\_ni\_physical\_link\]
-   Strand \[cmdb\_ci\_strand\]
-   Topology \[cmdb\_ci\_topology\]
-   Tables specified by the **sn\_ni\_core.equipment\_tables** sys\_property, and any tables that extend the specified tables.
-   Tables that extend Equipment Holder \[cmdb\_ci\_equipment\_holder\].
-   Child tables that extend any of the following tables:
    -   Cable \[cmdb\_ci\_cable\]
    -   Equipment Holder \[cmdb\_ci\_equipment\_holder\]
    -   Strand \[cmdb\_ci\_strand\]

Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the resource.

Data type: String

</td></tr><tr><td>

note

</td><td>

List of notes about the resource. Data type: Array of Objects

```
"note": [
   {
      "text": "String"
   }
]
```

</td></tr><tr><td>

note.text

</td><td>

The note text.

Data type: String

</td></tr><tr><td>

place

</td><td>

Network site for the resource.

This parameter is not supported for Network Site, Physical Connection, or Logical Connection resources.

Data type: Object

```
"place": {
   "@referredType": "String",
   "href": "String",
   "id": "String"
}
```

</td></tr><tr><td>

place.@referredType

</td><td>

Type of place. This value is always `GeographicAddress`.Data type: String

</td></tr><tr><td>

place.href

</td><td>

Relative link to the place record.Data type: String

</td></tr><tr><td>

place.id

</td><td>

Sys\_id of the place record.

Data type: String

Table: Network Site \[cmdb\_ci\_ni\_site\]

</td></tr><tr><td id="d4470e405">

relatedParty

</td><td>

Details about contacts for the resource.

Data type: Array of Objects

```
"relatedParty": [
   {
      "@referredType": "String",
      "href": "String",
      "id": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of related party. Located in the in the **Type** field.Data type: String

Table: In the type field of Group \[sys\_user\_group\] table.

</td></tr><tr><td>

relatedParty.href

</td><td>

Relative link to the related party record.Data type: String

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the related party record.

Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

resourceCharacteristic

</td><td>

List of characteristics of the resource. The following resource types require specific resource characteristics. -   For Physical Connection and Logical Connection resources, a `Port A` or `Port Z` characteristic is required. If the Lifecycle Stage Status of the resource is In Use, both `Port A` and `Port Z` are required.
-   For Equipment Holder resources, a `Container Type` characteristic is required.

Data type: Array of Objects

```
"resourceCharacteristic": [
   {
      "name": "String",
      "value": "String",
      "valueType": "String"
   }
]
```

</td></tr><tr><td>

resourceCharacteristic.name

</td><td>

Field name from the resource table specified by the **@type** parameter. You can't use the fields model\_id, name, network\_site, operation\_notes, operational\_status, short\_description, start\_date, or any sys\_ prefixed fields such as sys\_id.

Data type: String

</td></tr><tr><td>

resourceCharacteristic.value

</td><td>

The value of the characteristic.

Data type: String

</td></tr><tr><td>

resourceCharacteristic.valueType

</td><td>

Type of value.Valid values:

-   boolean
-   datetime
-   float
-   integer
-   ph\_number
-   reference
-   string

Data type: String

</td></tr><tr><td>

resourceRelationship

</td><td>

List of related resources. The following resource types require specific related resources. -   For Interface Card resources, a relationship to an Equipment Holder resource where Container Type is Slot or Sub Slot is required.
-   For Network Interface resources, a relationship to an Equipment or Interface Card resource is required.
-   For Equipment Holder resources where Container Type is Slot or Sub Slot, a relationship to an Equipment or Interface Card resource is required.

Data type: Array

```
"resourceRelationship": [
  {
    "relationshipType": "String",
    "resource": {Object}
  }
]
```

</td></tr><tr><td>

resourceRelationship.relationshipType

</td><td>

Type of relationship between the two resources in the format `[this resource descriptor]::[related resource descriptor]`. For example, `Contains::Contained by` indicates that the related resource is the child of this resource.

Valid values for the descriptors are located in the CI Relationship Type \[cmdb\_rel\_type\] table in the **Parent descriptor** and **Child descriptor** columns.

Data type: String

</td></tr><tr><td>

resourceRelationship.resource

</td><td>

Details about the related resource. The related resource must be one of the following resource types.

-   Cable
-   Equipment
-   Equipment Holder
-   Interface Card
-   Logical Connection
-   Network Interface
-   Network Site
-   Physical Connection
-   Strand
-   Topology

Data type: Object

```
"resource": {
   "id": "String",
   "href": "String"
}
```

</td></tr><tr><td>

resourceRelationship.resource.id

</td><td>

Sys\_id of the related resource. Located in one of the following tables depending on the type of related resource.

-   Interface Card \[cmdb\_ci\_interface\_card\]
-   Logical Connection \[cmdb\_ci\_ni\_logical\_path\]
-   Network Interface \[cmdb\_ci\_ni\_interface\]
-   Network Site \[cmdb\_ci\_ni\_site\]
-   Physical Connection \[cmdb\_ci\_ni\_physical\_link\]
-   Tables specified by the **sn\_ni\_core.equipment\_tables** sys\_property, and any tables that extend the specified tables.
-   Tables that extend Equipment Holder \[cmdb\_ci\_equipment\_holder\]

Data type: String

</td></tr><tr><td>

resourceRelationship.resource.href

</td><td>

Relative link to the related resource record.Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

Resource specification. Data type: Object

```
"resourceSpecification": {
   "id": "String"
}
```

</td></tr><tr><td>

resourceSpecification.id

</td><td>

Sys\_id of the associated model for the resource. Located in one of the following tables depending on the type of model.

-   Cable Models \[sn\_ent\_cable\_model\]
-   Equipment Holder Models \[sn\_ent\_nw\_holder\_model\]
-   Equipment Models \[sn\_ent\_nw\_equipment\_model\]
-   Interface Card Models \[sn\_ent\_nw\_interface\_model\]
-   Logical Connection Models \[sn\_ent\_logical\_nw\_connection\_model\]
-   Network Interface Models \[sn\_ent\_nw\_interface\_model\]
-   Physical Connection Models \[sn\_ent\_physical\_nw\_connection\_model\]
-   Strand Models \[sn\_ent\_strand\_model\]
-   Topology Models \[sn\_ent\_network\_topology\_model\]

Data type: String

</td></tr><tr><td>

startOperatingDate

</td><td>

Date and time that the resource first started operating.Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates a network site in Denver, Colorado.

```
curl "https://instance.service-now.com/api/sn_ni_core/resource" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"name\": \"DENVER CO CO/HUB\",
  \"note\": [
    {
      \"text\": \"Cisco maintenance team onsite June 22, 2022.\"
    }
  ],
  \"resourceCharacteristic\": [
    {
      \"name\": \"attested\",
      \"valueType\": \"boolean\",
      \"value\": \"false\"
    },
    {
      \"name\": \"can_print\",
      \"valueType\": \"boolean\",
      \"value\": \"false\"
    },
    {
      \"name\": \"clli_code\",
      \"valueType\": \"string\",
      \"value\": \"DNVRCOMR02T\"
    },
    {
      \"name\": \"comments\",
      \"valueType\": \"string\",
      \"value\": \"Site is scheduled for diesel generator test July 13, 2022 at 9am CST.\"
    },
    {
      \"name\": \"cost_cc\",
      \"valueType\": \"string\",
      \"value\": \"USD\"
    },
    {
      \"name\": \"county\",
      \"valueType\": \"string\",
      \"value\": \"DENVER\"
    },
    {
      \"name\": \"data_center_code\",
      \"valueType\": \"string\",
      \"value\": \"DNVR00564\"
    },
    {
      \"name\": \"fault_count\",
      \"valueType\": \"integer\",
      \"value\": \"0\"
    },
    {
      \"name\": \"install_status\",
      \"valueType\": \"integer\",
      \"value\": \"1\"
    },
    {
      \"name\": \"life_cycle_stage\",
      \"valueType\": \"reference\",
      \"value\": \"Operational\"
    },
    {
      \"name\": \"life_cycle_stage_status\",
      \"valueType\": \"reference\",
      \"value\": \"In Use\"
    },
    {
      \"name\": \"location\",
      \"valueType\": \"reference\",
      \"value\": \"25ab8f300a0a0bb300d99f69c3ac24cd\"
    },
    {
      \"name\": \"managed_by\",
      \"valueType\": \"reference\",
      \"value\": \"b0f31e5673500010c2e7660c4cf6a711\"
    },
    {
      \"name\": \"monitor\",
      \"valueType\": \"boolean\",
      \"value\": \"false\"
    },
    {
      \"name\": \"network_domain\",
      \"valueType\": \"string\",
      \"value\": \"core\"
    },
    {
      \"name\": \"ni_type\",
      \"valueType\": \"reference\",
      \"value\": \"8e8f3770404d0110f8772175cacd7204\"
    },
    {
      \"name\": \"pots_number\",
      \"valueType\": \"ph_number\",
      \"value\": \"(214) 555-1234\"
    },
    {
      \"name\": \"skip_sync\",
      \"valueType\": \"boolean\",
      \"value\": \"false\"
    },
    {
      \"name\": \"third_party_ownership\",
      \"valueType\": \"boolean\",
      \"value\": \"false\"
    },
    {
      \"name\": \"unverified\",
      \"valueType\": \"boolean\",
      \"value\": \"false\"
    }
  ],
  \"resourceRelationship\": [
    {
      \"relationshipType\": \"Connects to::Connected by\",
      \"resource\": {
        \"id\": \"e6f6df8d4051c910f8772175cacd72b2\",
        \"href\": \"/api/sn_ni_core/resource/e6f6df8d4051c910f8772175cacd72b2\"
      }
    },
    {
      \"relationshipType\": \"Connects to::Connected by\",
      \"resource\": {
        \"id\": \"0ac19bc54051c910f8772175cacd724b\",
        \"href\": \"/api/sn_ni_core/resource/0ac19bc54051c910f8772175cacd724b\"
      }
    },
    {
      \"relationshipType\": \"Connects to::Connected by\",
      \"resource\": {
        \"id\": \"997e5c11875851109a9c0f65dabb35ac\",
        \"href\": \"/api/sn_ni_core/resource/997e5c11875851109a9c0f65dabb35ac\"
      }
    },
    {
      \"relationshipType\": \"Contains::Contained by\",
      \"resource\": {
        \"id\": \"5b10e8154015c910f8772175cacd724d\",
        \"href\": \"/api/sn_ni_core/resource/5b10e8154015c910f8772175cacd724d\"
      }
    },
    {
      \"relationshipType\": \"Contains::Contained by\",
      \"resource\": {
        \"id\": \"57e73b51405dc910f8772175cacd726e\",
        \"href\": \"/api/sn_ni_core/resource/57e73b51405dc910f8772175cacd726e\"
      }
    },
    {
      \"relationshipType\": \"Contains::Contained by\",
      \"resource\": {
        \"id\": \"bf58f751405dc910f8772175cacd72e8\",
        \"href\": \"/api/sn_ni_core/resource/bf58f751405dc910f8772175cacd72e8\"
      }
    },
    {
      \"relationshipType\": \"Contains::Contained by\",
      \"resource\": {
        \"id\": \"b5711e31405d0d10f8772175cacd7232\",
        \"href\": \"/api/sn_ni_core/resource/b5711e31405d0d10f8772175cacd7232\"
      }
    },
    {
      \"relationshipType\": \"Contains::Contained by\",
      \"resource\": {
        \"id\": \"ed811e31405d0d10f8772175cacd72d3\",
        \"href\": \"/api/sn_ni_core/resource/ed811e31405d0d10f8772175cacd72d3\"
      }
    },
    {
      \"relationshipType\": \"Contains::Contained by\",
      \"resource\": {
        \"id\": \"d74937d1405dc910f8772175cacd7288\",
        \"href\": \"/api/sn_ni_core/resource/d74937d1405dc910f8772175cacd7288\"
      }
    },
    {
      \"relationshipType\": \"Contains::Contained by\",
      \"resource\": {
        \"id\": \"da0df2e3e4e64510f877e70ec9bcacc6\",
        \"href\": \"/api/sn_ni_core/resource/da0df2e3e4e64510f877e70ec9bcacc6\"
      }
    }
  ],
  \"@type\": \"cmdb_ci_ni_site\"
}" \
--user 'username':'password'
```

Response body.

```
{
   "href": "/api/sn_ni_core/resource/00399f0aed349150f877305f29f832b2",
   "id": "00399f0aed349150f877305f29f832b2",
   "name": "DENVER CO CO/HUB",
   "note": [
      {
         "text": "Cisco maintenance team onsite June 22, 2022."
      }
   ],
   "resourceCharacteristic": [
      {
         "name": "altitude_units",
         "valueType": "string",
         "value": "feet"
      },
      {
         "name": "attestation_status",
         "valueType": "string",
         "value": "Not Yet Reviewed"
      },
      {
         "name": "attested",
         "valueType": "boolean",
         "value": "false"
      },
      {
         "name": "can_print",
         "valueType": "boolean",
         "value": "false"
      },
      {
         "name": "clli_code",
         "valueType": "string",
         "value": "DNVRCOMR02T"
      },
      {
         "name": "comments",
         "valueType": "string",
         "value": "Site is scheduled for diesel generator test July 13, 2022 at 9am CST."
      },
      {
         "name": "cost_cc",
         "valueType": "string",
         "value": "USD"
      },
      {
         "name": "county",
         "valueType": "string",
         "value": "DENVER"
      },
      {
         "name": "data_center_code",
         "valueType": "string",
         "value": "DNVR00564"
      },
      {
         "name": "discovery_source",
         "valueType": "string",
         "value": "Resource Inventory Open API"
      },
      {
         "name": "fault_count",
         "valueType": "integer",
         "value": "0"
      },
      {
         "name": "first_discovered",
         "valueType": "datetime",
         "value": "2022-07-21T19:38:04.000Z"
      },
      {
         "name": "install_status",
         "valueType": "integer",
         "value": "1"
      },
      {
         "name": "last_discovered",
         "valueType": "datetime",
         "value": "2022-07-21T19:38:04.000Z"
      },
      {
         "name": "life_cycle_stage",
         "valueType": "reference",
         "value": "Operational"
      },
      {
         "name": "life_cycle_stage_status",
         "valueType": "reference",
         "value": "In Use"
      },
      {
         "name": "location",
         "valueType": "reference",
         "value": "25ab8f300a0a0bb300d99f69c3ac24cd"
      },
      {
         "name": "managed_by",
         "valueType": "reference",
         "value": "b0f31e5673500010c2e7660c4cf6a711"
      },
      {
         "name": "monitor",
         "valueType": "boolean",
         "value": "false"
      },
      {
         "name": "network_domain",
         "valueType": "string",
         "value": "core"
      },
      {
         "name": "ni_type",
         "valueType": "reference",
         "value": "8e8f3770404d0110f8772175cacd7204"
      },
      {
         "name": "pots_number",
         "valueType": "ph_number",
         "value": "(214) 555-1234"
      },
      {
         "name": "skip_sync",
         "valueType": "boolean",
         "value": "false"
      },
      {
         "name": "third_party_ownership",
         "valueType": "boolean",
         "value": "false"
      },
      {
         "name": "unverified",
         "valueType": "boolean",
         "value": "false"
      }
   ],
   "resourceRelationship": [
      {
         "relationshipType": "Connects to::Connected by",
         "resource": {
            "id": "e6f6df8d4051c910f8772175cacd72b2",
            "href": "/api/sn_ni_core/resource/e6f6df8d4051c910f8772175cacd72b2"
         }
      },
      {
         "relationshipType": "Connects to::Connected by",
         "resource": {
            "id": "0ac19bc54051c910f8772175cacd724b",
            "href": "/api/sn_ni_core/resource/0ac19bc54051c910f8772175cacd724b"
         }
      },
      {
         "relationshipType": "Connects to::Connected by",
         "resource": {
            "id": "997e5c11875851109a9c0f65dabb35ac",
            "href": "/api/sn_ni_core/resource/997e5c11875851109a9c0f65dabb35ac"
         }
      },
      {
         "relationshipType": "Contains::Contained by",
         "resource": {
            "id": "5b10e8154015c910f8772175cacd724d",
            "href": "/api/sn_ni_core/resource/5b10e8154015c910f8772175cacd724d"
         }
      },
      {
         "relationshipType": "Contains::Contained by",
         "resource": {
            "id": "57e73b51405dc910f8772175cacd726e",
            "href": "/api/sn_ni_core/resource/57e73b51405dc910f8772175cacd726e"
         }
      },
      {
         "relationshipType": "Contains::Contained by",
         "resource": {
            "id": "bf58f751405dc910f8772175cacd72e8",
            "href": "/api/sn_ni_core/resource/bf58f751405dc910f8772175cacd72e8"
         }
      },
      {
         "relationshipType": "Contains::Contained by",
         "resource": {
            "id": "b5711e31405d0d10f8772175cacd7232",
            "href": "/api/sn_ni_core/resource/b5711e31405d0d10f8772175cacd7232"
         }
      },
      {
         "relationshipType": "Contains::Contained by",
         "resource": {
            "id": "ed811e31405d0d10f8772175cacd72d3",
            "href": "/api/sn_ni_core/resource/ed811e31405d0d10f8772175cacd72d3"
         }
      },
      {
         "relationshipType": "Contains::Contained by",
         "resource": {
            "id": "d74937d1405dc910f8772175cacd7288",
            "href": "/api/sn_ni_core/resource/d74937d1405dc910f8772175cacd7288"
         }
      },
      {
         "relationshipType": "Contains::Contained by",
         "resource": {
            "id": "da0df2e3e4e64510f877e70ec9bcacc6",
            "href": "/api/sn_ni_core/resource/da0df2e3e4e64510f877e70ec9bcacc6"
         }
      }
   ],
   "@type": "cmdb_ci_ni_site"
}
```

## Resource Inventory Open API - POST /sn\_ni\_core/resourceinventoryviatemplate

Creates a resource configuration item \(CI\) and related CI hierarchy based on a template.

Before calling this endpoint, you must create an inventory template in the Inventory Template \[sn\_ni\_core\_inventory\_template\] table. You can define the entire hierarchy of related CIs in an inventory template. You can then create all of the CIs and relationships via a single API request.

### URL format

Default URL: `/api/sn_ni_core/resourceinventoryviatemplate`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

overrides

</td><td>

List of columns to override and the values to use.Data type: Object

```
"overrides": {
  "column_name": "String"
}
```

</td></tr><tr><td>

overrides.column\_name

</td><td>

Required if the **overrides** parameter is used. Column name and value.Data type: String

</td></tr><tr><td>

parentId

</td><td>

Required. Sys\_id of the parent CI. Located in one of the following tables depending on the type of parent CI. -   Cable \[cmdb\_ci\_cable\]
-   Equipment Holder \[cmdb\_ci\_equipment\_holder\]
-   Interface Card \[cmdb\_ci\_interface\_card\]
-   IP Address \[cmdb\_ci\_ip\_address\]
-   Logical Connection \[cmdb\_ci\_ni\_logical\_path\]
-   Network Interface \[cmdb\_ci\_ni\_interface\]
-   Network Site \[cmdb\_ci\_ni\_site\]
-   Physical Connection \[cmdb\_ci\_ni\_physical\_link\]
-   Strand \[cmdb\_ci\_strand\]
-   Topology \[cmdb\_ci\_topology\]
-   Tables specified by the **sn\_ni\_core.equipment\_tables** sys\_property, and any tables that extend the specified tables.
-   Tables that extend Equipment Holder \[cmdb\_ci\_equipment\_holder\].
-   Child tables that extend any of the following tables:
    -   Cable \[cmdb\_ci\_cable\]
    -   Equipment Holder \[cmdb\_ci\_equipment\_holder\]
    -   Strand \[cmdb\_ci\_strand\]

Data type: String

</td></tr><tr><td>

templateId

</td><td>

Required. Sys\_id of the template. Data type: String

Table: Inventory Template \[sn\_ni\_core\_inventory\_template\]

</td></tr><tr><td>

templateOverrides

</td><td>

List of template overrides.Data type: Array of Objects

```
"templateOverrides": [
  {
    "overrideTemplateId": "String",
    "templateId": "String"     
  }
]
```

</td></tr><tr><td>

templateOverrides.overrideTemplateId

</td><td>

Required if the **templateOverrides** parameter is used. Available template sys\_id.Data type: String

</td></tr><tr><td>

templateOverrides.templateId

</td><td>

Required if the **templateOverrides** parameter is used. Related template sys\_id.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|
|Location|URL of the created CI at the top of the hierarchy.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|201|Resource created.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Error. An error occurred with the request. For example, the request failed validation checks.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Result object with information about the created CIs.Data type: Object

```
"result": {
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the created CI at the top of the hierarchy.Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates a CI hierarchy using a template.

```
curl "https://instance.service-now.com/api/sn_ni_core/resourceinventoryviatemplate" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   "templateId": "90475711ed6ec110f877d2f57b8accda",
   "parentId": "917dd8f6870e851079c40f2d0ebb353d",
   "overrides": {
      "equipment_clli": "test"
   },
   "templateOverrides": [
      {
         "templateId": "ac3b679ded6ec110f877d2f57b8acc29",
         "overrideTemplateId": "f9604efb54e18110f87749bbc4ad38d8"
      },
      {
         "templateId": "171c23dded6ec110f877d2f57b8acc33",
         "overrideTemplateId": "0f38e59187424110e14f64e73cbb35b4"
      }
   ]
}" \
--user 'username':'password'
```

Response body.

```
"result": {
   "sys_id": "00598f0aed346259f388105f29f892c4"
}
```

