---
title: Trouble Ticket Open API
description: The Trouble Ticket Open API provides endpoints to create, update, and retrieve data from the Case \[sn\_customerservice\_case\], Incident \[incident\], and Service Problem Case \[sn\_sprb\_mgmt\_case\] tables.Retrieves a list of all trouble ticket records from the Case \[sn\_customerservice\_case\], Incident \[incident\], and Service Problem Case \[sn\_sprb\_mgmt\_case\] tables.Retrieves a specified record from the Case \[sn\_customerservice\_case\], Incident \[incident\], or Service Problem Case \[sn\_sprb\_mgmt\_case\] table.Updates a specified record in the Case \[sn\_customerservice\_case\], Incident \[incident\], or Service Problem Case \[sn\_sprb\_mgmt\_case\] table.Creates a record in the Case \[sn\_customerservice\_case\], Incident \[incident\], or Service Problem Case \[sn\_sprb\_mgmt\_case\] table.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 28
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Trouble Ticket Open API

The Trouble Ticket Open API provides endpoints to create, update, and retrieve data from the Case \[sn\_customerservice\_case\], Incident \[incident\], and Service Problem Case \[sn\_sprb\_mgmt\_case\] tables.

Use this API to manage ticket information between external ticketing systems and the ServiceNow AI Platform.

This API is included in the [Proactive Service Experience Workflows](https://store.servicenow.com/sn_appstore_store.do#!/store/application/9e07323d5b2110100206cb837b81c773) application, which is available on the ServiceNow Store. The Customer Service \(com.sn\_customerservice\) and Customer Service Install Base Management \(com.snc.install\_base\) applications are required to use this API with the Case \[sn\_customerservice\_case\] table.

This API is provided within the `sn_ind_tsm_sdwan` namespace.

The calling user must have the ticket\_integrator role.

This API can be extended to make customizations around required parameters, request body validation, additional REST operations, and field mappings. For more information, see the [Trouble Ticket Open API Developer Guide](../../guides/telecom/concept/trouble-ticket_dev-guide.md#).

The Trouble Ticket Open API is a ServiceNow® implementation of the TM Forum Trouble Ticket Management API REST specification. This implementation is based on the [TMF621 Trouble Ticket Management API User Guide v5.0.0](https://www.tmforum.org/resources/specifications/tmf621-trouble-ticket-management-api-user-guide-v5-0-0/), September 2024. The Trouble Ticket Open API is conformance certified by TM Forum.

![TMF conformance logo](../image/tmf-conformance.png)

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Trouble Ticket - GET /sn\_ind\_tsm\_sdwan/ticket/troubleTicket 

Retrieves a list of all trouble ticket records from the Case \[sn\_customerservice\_case\], Incident \[incident\], and Service Problem Case \[sn\_sprb\_mgmt\_case\] tables.

### URL format

Default URL: `/api/sn_ind_tsm_sdwan/ticket/troubleTicket`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored.Valid fields:

-   channel
-   creationDate
-   description
-   href
-   id
-   lastUpdate
-   name
-   note
-   relatedEntity
-   relatedParty
-   severity
-   status
-   ticketType
-   @type

Default: Returns all fields.

Data type: String

</td></tr><tr><td>

id

</td><td>

Filter trouble tickets by sys\_id. Only tickets with the specified sys\_id are returned in the response.Data type: String

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval. Default: 25

Maximum: 100

You can change the default and maximum values by updating the **sn\_ind\_tsm\_sdwan.pagination.set\_limit** and **sn\_ind\_tsm\_sdwan.pagination.max\_limit** system properties.

Data type: Number

</td></tr><tr><td>

offset

</td><td>

Starting index at which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks.Data type: Number

Default: 0

</td></tr><tr><td>

severity

</td><td>

Filter trouble tickets by severity. Only tickets with the specified severity are returned in the response.Data type: String

</td></tr><tr><td>

status

</td><td>

Filter trouble tickets by status. Only tickets with the specified status are returned in the response.Data type: String

</td></tr><tr><td>

ticketType

</td><td>

Filter trouble tickets by ticket type. Only tickets of the specified type are returned in the response.Valid values:

-   Case
-   Incident
-   Service Problem Case

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

<table id="table_c2r_4gm_lsb" class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr id="content-range-row"><td>

Content-Range

</td><td>

Range of content returned in a paginated call. For example, if `offset=2` and `limit=3`, the value of the **Content-Range** header is `items 3-5`.

</td></tr><tr id="content-type-row"><td>

Content-Type

</td><td>

Data format of the response body. Only supports **application/json**.

</td></tr><tr id="links-pagination-row"><td>

Link

</td><td>

Contains the following links to navigate through query results.-   first
-   last
-   next
-   previous

</td></tr><tr id="x-total-count-row"><td id="x-total-count">

X-Total-Count

</td><td>

For paginated queries, this header specifies the total number of records available on the server.

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_qbg_4cm_lsb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="tmf-get-status-200-entry">

Request successfully processed. Full resource returned in response \(no pagination\).

</td></tr><tr><td>

206

</td><td id="tmf-get-status-206-entry">

Partial resource returned in response \(with pagination\).

</td></tr><tr><td>

400

</td><td id="tmf-get-status-400-entry">

Bad request. Possible reasons:

-   Invalid path parameter
-   Invalid URI

</td></tr><tr><td>

404

</td><td id="tmf-get-status-404-entry">

Record not found. No records matching the query parameters are found in the table.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_n4d_yvm_5pb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channel

</td><td>

Method of contact that the ticket was created through.Data type: Object

```
"channel":{
  "name": "String"
}
```

</td></tr><tr><td>

channel.name

</td><td>

The name of the contact method. Maps to the **Channel** \[contact\_type\] field for cases and the **Contact type** \[contact\_type\] field for incidents.Data type: String

</td></tr><tr><td>

creationDate

</td><td>

The date that the case or incident record was created. Maps to the **Created** field.Data type: String

</td></tr><tr><td>

description

</td><td>

The description of the issue from the ticket. Maps to the **Description** field.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the case or incident record.Data type: String

</td></tr><tr><td>

id

</td><td>

The sys\_id of the case or incident record.Data type: String

</td></tr><tr><td>

lastUpdate

</td><td>

The date the record was last updated. Maps to the **Updated** field.Data type: String

</td></tr><tr><td>

name

</td><td>

The name of the trouble ticket, typically a short description of the issue. Maps to the **Short description** field.Data type: String

</td></tr><tr><td>

note

</td><td>

A list of all comments on the ticket. This list does not include work notes.Data type: Array

 ```
"note":[
  {
    "author": "String",
    "date": "String",
    "text": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

note.@type

</td><td>

The type of note. Only comments are returned \(not work notes\) so this value is always `comments`.Data type: String

</td></tr><tr><td>

note.author

</td><td>

The name of the ServiceNow integration user who made the POST or PATCH request that created the comment.Data type: String

</td></tr><tr><td>

note.date

</td><td>

The date the comment was created in the ServiceNow instance.Data type: String

</td></tr><tr><td>

note.text

</td><td>

The comment text.Data type: String

</td></tr><tr><td>

relatedEntity

</td><td>

List of impacted assets, products, sold products \(product inventory\), configuration items, or services.Data type: Array of Objects

```
"relatedEntity": [
  {
    "id": "String",
    "href": "String",
    "name": "String",
    "role": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

relatedEntity.id

</td><td>

Sys\_id of the impacted item or service.For cases, this value is from one of the following tables:

-   Asset \[alm\_asset\]
-   Product Inventory \[sn\_prd\_invt\_product\_inventory\], which extends the Sold Product \[sn\_install\_base\_sold\_product\] table
-   Product Model \[cmdb\_model\]
-   Sold Product \[sn\_install\_base\_sold\_product\]

For incidents, this value is from one of the following tables:

-   Configuration Item \[cmdb\_ci\]
-   Service \[cmdb\_ci\_service\]

Data type: String

</td></tr><tr><td>

relatedEntity.href

</td><td>

Returns an empty string.Data type: String

</td></tr><tr><td>

relatedEntity.name

</td><td>

Name of the impacted item or service.Data type: String

</td></tr><tr><td>

relatedEntity.role

</td><td>

Description of the impacted item or service.Data type: String

</td></tr><tr><td>

relatedEntity.@referredType

</td><td>

Type of item or service.Valid values for case tickets:

-   asset
-   product
-   product\_inventory

Valid values for incident tickets:

-   cmdb\_ci
-   cmdb\_ci\_service

Data type: String

</td></tr><tr><td>

relatedEntity.@type

</td><td>

This value is always `relatedEntity`.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

Details about contacts for the ticket.Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the related party. The sys\_id can be from the following tables depending on the ticket type and the related party type.Case:

-   Account \[customer\_account\]; Related party type is `customer`
-   Contact \[customer\_contact\]; Related party type is `customer_contact`

Incident:

-   Company \[core\_company\]; Related party type is `customer`
-   User \[sys\_user\]; Related party type is `customer_contact`

Case or incident:

-   Group \[sys\_user\_group\]; Related party type is `assignment_group`
-   User \[sys\_user\]; Related party type is `assigned_to`

Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of related party.Possible values:

-   `assigned_to`: User assigned to work on the ticket.
-   `assignment_group`: Group assigned to work on the ticket.
-   `customer`: Company or account for the ticket.
-   `customer_contact`: Caller or contact for the ticket.

Data type: String

</td></tr><tr><td>

severity

</td><td>

The severity of the issue described by the trouble ticket. Maps to the **Priority** field.Data type: String

</td></tr><tr><td>

status

</td><td>

The current status of the trouble ticket. Maps to the **State** field.Data type: String

</td></tr><tr><td>

ticketType

</td><td>

The type of ticket.Possible values:

-   Case
-   Incident
-   Service Problem Case

Data type: String

</td></tr><tr><td>

@type

</td><td>

This value is always `TroubleTicket`.Data type: String

</td></tr></tbody>
</table>### cURL request

This example returns specified fields for the first five trouble ticket case records.

```
curl "https://instance.servicenow.com/api/sn_ind_tsm_sdwan/ticket/troubleTicket?limit=5&fields=id%2Cname%2Cdescription%2Cstatus%2Cseverity%2CticketType&ticketType=case" \
--request GET \
--user 'username':'password'
```

Response body.

```
[
   {
      "id": "0004609eb9830110f877b3758cd21d37",
      "name": "Compliant Over 2796",
      "description": "checkNo2796",
      "status": "New",
      "severity": "3 - Moderate",
      "ticketType": "Case"
   },
   {
      "id": "000560d2b9c30110f877b3758cd21d36",
      "name": "Compliant Over 4696",
      "description": "checkNo4696",
      "status": "New",
      "severity": "3 - Moderate",
      "ticketType": "Case"
   },
   {
      "id": "0007ac5eb9c30110f877b3758cd21d34",
      "name": "Compliant Over 8817",
      "description": "checkNo8817",
      "status": "New",
      "severity": "3 - Moderate",
      "ticketType": "Case"
   },
   {
      "id": "0007ac5eb9c30110f877b3758cd21d39",
      "name": "Compliant Over 8819",
      "description": "checkNo8819",
      "status": "New",
      "severity": "3 - Moderate",
      "ticketType": "Case"
   },
   {
      "id": "0007ac5eb9c30110f877b3758cd21d3e",
      "name": "Compliant Over 8821",
      "description": "checkNo8821",
      "status": "New",
      "severity": "3 - Moderate",
      "ticketType": "Case"
   }
]
```

## Trouble Ticket - GET /sn\_ind\_tsm\_sdwan/ticket/troubleTicket/\{id\}

Retrieves a specified record from the Case \[sn\_customerservice\_case\], Incident \[incident\], or Service Problem Case \[sn\_sprb\_mgmt\_case\] table.

### URL format

Default URL: `/api/sn_ind_tsm_sdwan/ticket/troubleTicket/{id}`

### Supported request parameters

<table id="table_ufw_yqm_5pb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the case or incident record to retrieve. Data type: String

Table: Case \[sn\_customerservice\_case\] or Incident \[incident\]

</td></tr></tbody>
</table><table id="table_cn5_zqm_5pb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored.Valid values:

-   channel
-   creationDate
-   description
-   href
-   id
-   lastUpdate
-   name
-   note
-   relatedEntity
-   relatedParty
-   severity
-   status
-   ticketType
-   @type

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

Bad Request. A bad request type or malformed request was detected for one or more of the following reasons.-   Invalid path parameter.
-   Invalid URI.

</td></tr><tr><td>

404

</td><td>

Record not found. A record associated with the ID is not found in the Case \[sn\_customerservice\_case\] or Incident \[incident\] table.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_n4d_yvm_5pb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channel

</td><td>

Method of contact that the ticket was created through.Data type: Object

```
"channel":{
  "name": "String"
}
```

</td></tr><tr><td>

channel.name

</td><td>

Name of the contact method. Maps to the Channel \[contact\_type\] field for cases and the Contact type \[contact\_type\] field for incidents.Data type: String

</td></tr><tr><td>

creationDate

</td><td>

Date that the case or incident record was created. Maps to the Created field.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the issue from the ticket. Maps to the Description field.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the case or incident record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the case or incident record.Data type: String

</td></tr><tr><td>

lastUpdate

</td><td>

Date the record was last updated. Maps to the Updated field.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the trouble ticket, typically a short description of the issue. Maps to the Short description field.Data type: String

</td></tr><tr><td>

note

</td><td>

List of all comments on the ticket. This list does not include work notes.Data type: Array of Objects

```
"note":[
  {
    "author": "String",
    "date": "String",
    "text": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

note.@type

</td><td>

Type of note. Only comments are returned \(not work notes\) so this value is always `comments`.Data type: String

</td></tr><tr><td>

note.author

</td><td>

Name of the user who wrote the comment.Data type: String

</td></tr><tr><td>

note.date

</td><td>

Date the comment was created in the ServiceNow instance.Data type: String

</td></tr><tr><td>

note.text

</td><td>

Comment text.Data type: String

</td></tr><tr><td>

relatedEntity

</td><td>

List of impacted assets, products, sold products \(product inventory\), configuration items, or services.Data type: Array of Objects

```
"relatedEntity": [
  {
    "id": "String",
    "href": "String",
    "name": "String",
    "role": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

relatedEntity.id

</td><td>

Sys\_id of the impacted item or service.For cases, this value is from one of the following tables:

-   Asset \[alm\_asset\]
-   Product Inventory \[sn\_prd\_invt\_product\_inventory\], which extends the Sold Product \[sn\_install\_base\_sold\_product\] table
-   Product Model \[cmdb\_model\]
-   Sold Product \[sn\_install\_base\_sold\_product\]

For incidents, this value is from one of the following tables:

-   Configuration Item \[cmdb\_ci\]
-   Service \[cmdb\_ci\_service\]

Data type: String

</td></tr><tr><td>

relatedEntity.href

</td><td>

Returns an empty string.Data type: String

</td></tr><tr><td>

relatedEntity.name

</td><td>

Name of the impacted item or service.Data type: String

</td></tr><tr><td>

relatedEntity.role

</td><td>

Description of the impacted item or service.Data type: String

</td></tr><tr><td>

relatedEntity.@referredType

</td><td>

Type of item or service.Valid values for case tickets:

-   asset
-   product
-   product\_inventory

Valid values for incident tickets:

-   cmdb\_ci
-   cmdb\_ci\_service

Data type: String

</td></tr><tr><td>

relatedEntity.@type

</td><td>

This value is always `relatedEntity`.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

Details about contacts for the ticket.Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the related party. The sys\_id can be from the following tables depending on the ticket type and the related party type.Case:

-   Account \[customer\_account\]; Related party type is `customer`
-   Contact \[customer\_contact\]; Related party type is `customer_contact`

Incident:

-   Company \[core\_company\]; Related party type is `customer`
-   User \[sys\_user\]; Related party type is `customer_contact`

Case or incident:

-   Group \[sys\_user\_group\]; Related party type is `assignment_group`
-   User \[sys\_user\]; Related party type is `assigned_to`

Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of related party.Possible values:

-   `assigned_to`: User assigned to work on the ticket.
-   `assignment_group`: Group assigned to work on the ticket.
-   `customer`: Company or account for the ticket.
-   `customer_contact`: Caller or contact for the ticket.

Data type: String

</td></tr><tr><td>

severity

</td><td>

Severity of the issue described by the trouble ticket. Maps to the Priority field.Data type: String

</td></tr><tr><td>

status

</td><td>

Current status of the trouble ticket. Maps to the State field.Data type: String

</td></tr><tr><td>

ticketType

</td><td>

Type of ticket.Possible values:

-   Case
-   Incident
-   Service Problem Case

Data type: String

</td></tr><tr><td>

@type

</td><td>

This value is always `TroubleTicket`.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves a trouble ticket record from the Case \[sn\_customerservice\_case\] table.

```
curl "https://instance.servicenow.com/api/sn_ind_tsm_sdwan/ticket/troubleTicket/6467508d47e345508761b955d36d43f6" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body.

```
{
    "id": "370415f03c20e910f8772f1bc332b31b",
    "href": "/api/sn_ind_tsm_sdwan/ticket/troubleTicket/370415f03c20e910f8772f1bc332b31b",
    "creationDate": "2023-01-19 22:39:28",
    "lastUpdate": "2023-01-19 22:41:39",
    "description": "Router is not working, my devices cannot detect any signals from the router. First button from the left is flashing red, all others are black. Resetting the router does not solve the problem, I need urgent assistance.",
    "severity": "2 - High",
    "ticketType": "Case",
    "name": "My router is not working properly",
    "status": "Open",
    "channel": {
        "name": "e_bonding"
    },
    "relatedParty": [
        {
            "id": "ffc68911c35420105252716b7d40dd55",
            "name": "Funco Intl",
            "@referredType": "customer"
        },
        {
            "id": "eaf68911c35420105252716b7d40ddde",
            "name": "Sally Thomas",
            "@referredType": "customer_contact"
        },
        {
            "id": "",
            "name": "",
            "@referredType": "assignment_group"
        },
        {
            "id": "",
            "name": "",
            "@referredType": "assigned_to"
        }
    ],
    "relatedEntity": [
        {
            "id": "b7fa12c7532520103b6bddeeff7b123b",
            "href": "",
            "name": "Deduplication and Compression PRD00001965",
            "role": "This is the product associated with the case.",
            "@type": "relatedEntity",
            "@referredType": "product"
        },
        {
            "id": "71e73d87c3e23010ff00ed23a140dde8",
            "href": "",
            "name": "",
            "role": "This is the asset associated with the case.",
            "@type": "relatedEntity",
            "@referredType": "asset"
        },
        {
            "id": "a1913c3577b301108e191e599a5a99e8",
            "href": "",
            "name": "Deduplication and Compression PI0000037",
            "role": "This is the product inventory associated with the case.",
            "@type": "relatedEntity",
            "@referredType": "product_inventory"
        }
    ],
    "note": [
        {
            "text": "This is a testing comment<script>gs.info('Hello World')</script>",
            "date": "2023-01-19 14:41:39",
            "author": "System Administrator",
            "@type": "comments"
        },
        {
            "text": "This is a testing comment<script>gs.info('Hello World')</script>",
            "date": "2023-01-19 14:39:28",
            "author": "System Administrator",
            "@type": "comments"
        }
    ],
    "@type": "TroubleTicket"
}
```

## Trouble Ticket - PATCH /sn\_ind\_tsm\_sdwan/ticket/troubleTicket/\{id\}

Updates a specified record in the Case \[sn\_customerservice\_case\], Incident \[incident\], or Service Problem Case \[sn\_sprb\_mgmt\_case\] table.

### URL format

Default URL: `/api/sn_ind_tsm_sdwan/ticket/troubleTicket/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the case or incident record to update.Data type: String

Table: Case \[sn\_customerservice\_case\] or Incident \[incident\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channel

</td><td>

Method of contact that the ticket was created through.Data type: Object

```
"channel":{
  "name": "String"
}
```

</td></tr><tr><td>

channel.name

</td><td>

Name of the contact method. Maps to the Channel \[contact\_type\] field for cases and the Contact type \[contact\_type\] field for incidents.Valid values are the choices for the contact\_type field. You can provide the choice label or value. For example, `Virtual Agent` or `virtual_agent`.

Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the issue. Maps to the **Description** field.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the trouble ticket, typically a short description of the issue. Maps to the Short description field.Data type: String

</td></tr><tr><td>

note

</td><td>

List of work notes and comments to add to the ticket.Data type: Array of Objects

```
"note":[
  {
    "text": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

note.@type

</td><td>

Type of note. This value determines whether the note is recorded in the Work notes or Additional comments field.Valid values:

-   comments
-   work\_notes

Data type: String

</td></tr><tr><td>

note.text

</td><td>

Note text. Maps to the Work notes or Additional comments field.Data type: String

</td></tr><tr><td>

relatedEntity

</td><td>

List of impacted assets, products, sold products \(product inventory\), configuration items, or services.Data type: Array of Objects

```
"relatedEntity": [
  {
    "id": "String",
    "@referredType": "String"
  }
]
```

</td></tr><tr><td>

relatedEntity.id

</td><td>

Sys\_id of the impacted item or service.For cases, this value is from one of the following tables:

-   Asset \[alm\_asset\]
-   Product Inventory \[sn\_prd\_invt\_product\_inventory\], which extends the Sold Product \[sn\_install\_base\_sold\_product\] table
-   Product Model \[cmdb\_model\]
-   Sold Product \[sn\_install\_base\_sold\_product\]

For incidents, this value is from one of the following tables:

-   Configuration Item \[cmdb\_ci\]
-   Service \[cmdb\_ci\_service\]

Data type: String

</td></tr><tr><td>

relatedEntity.@referredType

</td><td>

Type of item or service.Valid values for case tickets:

-   asset
-   product
-   product\_inventory

Valid values for incident tickets:

-   cmdb\_ci
-   cmdb\_ci\_service

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

Details about contacts for the ticket. For cases, this parameter populates the Contact or Account field. For incidents, this parameter populates the Caller or Company field.Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "@referredType": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the related party. If you provide a contact or a user \(caller\), their account or company is automatically populated on the ticket. Data type: String

Table: For cases, the sys\_id is from the Contact \[customer\_contact\] or Account \[customer\_account\] tables. For incidents, the sys\_id is from the User \[sys\_user\] or Company \[core\_company\] tables.

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of related party.Valid values:

-   customer: Company or account for the ticket.
-   customer\_contact: Caller or contact for the ticket.

Data type: String

</td></tr><tr><td>

severity

</td><td>

Severity of the issue described by the trouble ticket. Maps to the **Priority** field.Valid values:

-   1: Critical
-   2: High
-   3: Moderate
-   4: Low
-   5: Planning. Incident only.

Valid values are the choices for the Priority field. You must provide the choice value only. For example, `1`. If an invalid value is provided, the severity is set to Low.

Data type: String

</td></tr><tr><td>

status

</td><td>

Current status of the trouble ticket. Maps to the **State** field.Valid values are the choices for the **State** field. You can provide the choice label or value. For example, `New` or `1`.

Data type: String

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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. A bad request type or malformed request was detected for one or more of the following reasons.-   Invalid path parameter.
-   Invalid URI.

</td></tr><tr><td>

404

</td><td>

Record not found. A record associated with the ID is not found in the Case \[sn\_customerservice\_case\] or Incident \[incident\] table.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channel

</td><td>

Method of contact that the ticket was created through.Data type: Object

```
"channel":{
  "name": "String"
}
```

</td></tr><tr><td>

channel.name

</td><td>

Name of the contact method.Data type: String

</td></tr><tr><td>

creationDate

</td><td>

Date the record was created.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the issue from the ticket.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the case or incident record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the case or incident record.Data type: String

</td></tr><tr><td>

lastUpdate

</td><td>

Date the record was last updated.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the trouble ticket, typically a short description of the issue.Data type: String

</td></tr><tr><td>

note

</td><td>

List of all comments on the ticket. This list does not include work notes.Data type: Array of Objects

```
"note":[
  {
    "author": "String",
    "date": "String",
    "text": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

note.@type

</td><td>

Type of note. Only comments are returned \(not work notes\) so this value is always `comments`.Data type: String

</td></tr><tr><td>

note.author

</td><td>

Name of the user who wrote the comment.Data type: String

</td></tr><tr><td>

note.date

</td><td>

Date the comment was created in the ServiceNow instance.Data type: String

</td></tr><tr><td>

note.text

</td><td>

Comment text.Data type: String

</td></tr><tr><td>

relatedEntity

</td><td>

List of impacted assets, products, sold products \(product inventory\), configuration items, or services.Data type: Array of Objects

```
"relatedEntity": [
  {
    "id": "String",
    "href": "String",
    "name": "String",
    "role": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

relatedEntity.id

</td><td>

Sys\_id of the impacted item or service.For cases, this value is from one of the following tables:

-   Asset \[alm\_asset\]
-   Product Inventory \[sn\_prd\_invt\_product\_inventory\], which extends the Sold Product \[sn\_install\_base\_sold\_product\] table
-   Product Model \[cmdb\_model\]
-   Sold Product \[sn\_install\_base\_sold\_product\]

For incidents, this value is from one of the following tables:

-   Configuration Item \[cmdb\_ci\]
-   Service \[cmdb\_ci\_service\]

Data type: String

</td></tr><tr><td>

relatedEntity.href

</td><td>

Returns an empty string.Data type: String

</td></tr><tr><td>

relatedEntity.name

</td><td>

Name of the impacted item or service.Data type: String

</td></tr><tr><td>

relatedEntity.role

</td><td>

Description of the impacted item or service.Data type: String

</td></tr><tr><td>

relatedEntity.@referredType

</td><td>

Type of item or service.Valid values for case tickets:

-   asset
-   product
-   product\_inventory

Valid values for incident tickets:

-   cmdb\_ci
-   cmdb\_ci\_service

Data type: String

</td></tr><tr><td>

relatedEntity.@type

</td><td>

This value is always `relatedEntity`.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

Details about contacts for the ticket.Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the related party. The sys\_id can be from the following tables depending on the ticket type and the related party type.Case:

-   Account \[customer\_account\]; Related party type is `customer`
-   Contact \[customer\_contact\]; Related party type is `customer_contact`

Incident:

-   Company \[core\_company\]; Related party type is `customer`
-   User \[sys\_user\]; Related party type is `customer_contact`

Case or incident:

-   Group \[sys\_user\_group\]; Related party type is `assignment_group`
-   User \[sys\_user\]; Related party type is `assigned_to`

Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of related party.Possible values:

-   `assigned_to`: User assigned to work on the ticket.
-   `assignment_group`: Group assigned to work on the ticket.
-   `customer`: Company or account for the ticket.
-   `customer_contact`: Caller or contact for the ticket.

Data type: String

</td></tr><tr><td>

severity

</td><td>

Severity of the issue described by the trouble ticket.Data type: String

</td></tr><tr><td>

status

</td><td>

Current status of the trouble ticket.Data type: String

</td></tr><tr><td>

ticketType

</td><td>

Type of ticket.Possible values:

-   Case
-   Incident
-   Service Problem Case

Data type: String

</td></tr><tr><td>

@type

</td><td>

This value is always `TroubleTicket`.Data type: String

</td></tr></tbody>
</table>### cURL request

This example updates a case record.

```
curl "https://instance.servicenow.com/api/sn_ind_tsm_sdwan/ticket/troubleTicket/6467508d47e345508761b955d36d43f6" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   description: "Updated description",
   "note": [
      {
         "text": "Adding another comment",
         "@type": "comments"
      }
   ]
}" \
--user 'username':'password'
```

Response body.

```
{
   "id": "6467508d47e345508761b955d36d43f6",
   "href": "/api/sn_ind_tsm_sdwan/ticket/troubleTicket/6467508d47e345508761b955d36d43f6",
   "creationDate": "2022-05-16 23:38:55",
   "lastUpdate": "2022-05-16 23:48:42",
   "description": "Updated description",
   "severity": "2 - High",
   "ticketType": "Case",
   "name": "Laptop problem",
   "status": "New",
   "channel": {
      "name": "web"
   },
   "relatedParty": [
      {
         "id": "",
         "name": "",
         "@referredType": "customer"
      },
      {
         "id": "62826bf03710200044e0bfc8bcbe5df1",
         "name": "",
         "@referredType": "customer_contact"
      },
      {
         "id": "",
         "name": "",
         "@referredType": "assignment_group"
      },
      {
         "id": "",
         "name": "",
         "@referredType": "assigned_to"
      }
   ],
   "relatedEntity": [
      {
         "id": "",
         "href": "",
         "name": "",
         "role": "This is the product associated with the case",
         "@type": "relatedEntity",
         "@referredType": "product"
      },
      {
         "id": "74a9ec0d3790200044e0bfc8bcbe5d7f",
         "href": "",
         "name": "P1000597 - Apple MacBook Pro 15\"",
         "role": "This is the asset associated with the case",
         "@type": "relatedEntity",
         "@referredType": "asset"
      }
      {
         "id": "a1913c3577b301108e191e599a5a99e8",
         "href": "",
         "name": "Deduplication and Compression PI0000037",
         "role": "This is the product inventory associated with the case.",
         "@type": "relatedEntity",
         "@referredType": "product_inventory"
      }
   ],
   "note": [
      {
         "text": "Adding another comment",
         "date": "2022-05-16 16:48:42",
         "author": "admin",
         "@type": "comments"
      },
      {
         "text": "Comment about this case",
         "date": "2022-05-16 16:38:55",
         "author": "admin",
         "@type": "comments"
      }
   ],
   "@type": "TroubleTicket"
}
```

## Trouble Ticket - POST /sn\_ind\_tsm\_sdwan/ticket/troubleTicket 

Creates a record in the Case \[sn\_customerservice\_case\], Incident \[incident\], or Service Problem Case \[sn\_sprb\_mgmt\_case\] table.

### URL format

Default URL: `/api/sn_ind_tsm_sdwan/ticket/troubleTicket`

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

channel

</td><td>

Method of contact that the ticket was created through.Data type: Object

```
"channel":{
  "name": "String"
}
```

</td></tr><tr><td>

channel.name

</td><td>

Name of the contact method. Maps to the Channel \[contact\_type\] field for cases and the Contact type \[contact\_type\] field for incidents.Valid values are the choices for the contact\_type field. You can provide the choice label or value. For example, `Virtual Agent` or `virtual_agent`.

Data type: String

</td></tr><tr><td>

description

</td><td>

Required. A description of the issue. Maps to the **Description** field.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the trouble ticket, typically a short description of the issue. Maps to the Short description field.Data type: String

</td></tr><tr><td>

note

</td><td>

List of work notes and comments to add to the ticket.Data type: Array of Objects

```
"note":[
  {
    "text": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

note.@type

</td><td>

Type of note. This value determines whether the note is recorded in the Work notes or Additional comments field.Valid values:

-   comments
-   work\_notes

Data type: String

</td></tr><tr><td>

note.text

</td><td>

Note text. Maps to the Work notes or Additional comments field.Data type: String

</td></tr><tr><td>

relatedEntity

</td><td>

List of impacted assets, products, sold products \(product inventory\), configuration items, or services.Data type: Array of Objects

```
"relatedEntity": [
  {
    "id": "String",
    "@referredType": "String"
  }
]
```

</td></tr><tr><td>

relatedEntity.id

</td><td>

Sys\_id of the impacted item or service.For cases, this value is from one of the following tables:

-   Asset \[alm\_asset\]
-   Product Inventory \[sn\_prd\_invt\_product\_inventory\], which extends the Sold Product \[sn\_install\_base\_sold\_product\] table
-   Product Model \[cmdb\_model\]
-   Sold Product \[sn\_install\_base\_sold\_product\]

For incidents, this value is from one of the following tables:

-   Configuration Item \[cmdb\_ci\]
-   Service \[cmdb\_ci\_service\]

Data type: String

</td></tr><tr><td>

relatedEntity.@referredType

</td><td>

Type of item or service.Valid values for case tickets:

-   asset
-   product
-   product\_inventory

Valid values for incident tickets:

-   cmdb\_ci
-   cmdb\_ci\_service

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

Details about contacts for the ticket. For cases, this parameter populates the Contact or Account field. For incidents, this parameter populates the Caller or Company field.Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "@referredType": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the related party. If you provide a contact or a user \(caller\), their account or company is automatically populated on the ticket. Data type: String

Table: For cases, the sys\_id is from the Contact \[customer\_contact\] or Account \[customer\_account\] tables. For incidents, the sys\_id is from the User \[sys\_user\] or Company \[core\_company\] tables.

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of related party.Valid values:

-   customer: Company or account for the ticket.
-   customer\_contact: Caller or contact for the ticket.

Data type: String

</td></tr><tr><td>

severity

</td><td>

Required. The severity of the issue described by the trouble ticket. Maps to the **Priority** field.Valid values:

-   1: Critical
-   2: High
-   3: Moderate
-   4: Low
-   5: Planning. Incident only.

Valid values are the choices for the Priority field. You must provide the choice value only. For example, `1`. If an invalid value is provided, the severity is set to Low.

Data type: String

</td></tr><tr><td>

status

</td><td>

Required. The current status of the trouble ticket. Maps to the **State** field.Valid values are the choices for the **State** field. You can provide the choice label or value. For example, `New` or `1`. If you provide an invalid value, the status is set to New.

Data type: String

</td></tr><tr><td>

ticketType

</td><td>

The type of ticket. This value determines whether the record is created in the Case \[sn\_customerservice\_case\], Incident \[incident\], or Service Problem Case \[sn\_sprb\_mgmt\_case\] table.Valid values:

-   Case
-   Incident
-   Service Problem Case

Data type: String

Default: Incident

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

201

</td><td>

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. A bad request type or malformed request was detected for one or more of the following reasons.-   Empty payload.
-   Invalid payload. Mandatory field missing.
-   Invalid ticketType.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

This value is always `TroubleTicket`.Data type: String

</td></tr><tr><td>

channel

</td><td>

Method of contact that the ticket was created through.Data type: Object

```
"channel":{
  "name": "String"
}
```

</td></tr><tr><td>

channel.name

</td><td>

The name of the contact method.Data type: String

</td></tr><tr><td>

creationDate

</td><td>

The date that the case or incident record was created.Data type: String

</td></tr><tr><td>

description

</td><td>

The description of the issue from the ticket.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the case or incident record.Data type: String

</td></tr><tr><td>

id

</td><td>

The sys\_id of the case or incident record that was created.Data type: String

</td></tr><tr><td>

lastUpdate

</td><td>

The date that the case or incident record was last updated.Data type: String

</td></tr><tr><td>

name

</td><td>

The name of the trouble ticket, typically a short description of the issue.Data type: String

</td></tr><tr><td>

note

</td><td>

A list of all comments on the ticket. This list does not include work notes.Data type: Array

```

"note":[
   {
      "author": "String",
      "date": "String",
      "text": "String",
      "@type": "String"
   }
]
```

</td></tr><tr><td>

note.@type

</td><td>

The type of note. Only comments are returned \(not work notes\) so this value is always `comments`.Data type: String

</td></tr><tr><td>

note.author

</td><td>

The name of the user who wrote the comment.Data type: String

</td></tr><tr><td>

note.date

</td><td>

The date the comment was created in the ServiceNow instance.Data type: String

</td></tr><tr><td>

note.text

</td><td>

The comment text.Data type: String

</td></tr><tr><td>

relatedEntity

</td><td>

List of impacted assets, products, sold products \(product inventory\), configuration items, or services.Data type: Array of Objects

```
"relatedEntity": [
  {
    "id": "String",
    "href": "String",
    "name": "String",
    "role": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

relatedEntity.id

</td><td>

Sys\_id of the impacted item or service.For cases, this value is from one of the following tables:

-   Asset \[alm\_asset\]
-   Product Inventory \[sn\_prd\_invt\_product\_inventory\], which extends the Sold Product \[sn\_install\_base\_sold\_product\] table
-   Product Model \[cmdb\_model\]
-   Sold Product \[sn\_install\_base\_sold\_product\]

For incidents, this value is from one of the following tables:

-   Configuration Item \[cmdb\_ci\]
-   Service \[cmdb\_ci\_service\]

Data type: String

</td></tr><tr><td>

relatedEntity.href

</td><td>

Returns an empty string.Data type: String

</td></tr><tr><td>

relatedEntity.name

</td><td>

Name of the impacted item or service.Data type: String

</td></tr><tr><td>

relatedEntity.role

</td><td>

Description of the impacted item or service.Data type: String

</td></tr><tr><td>

relatedEntity.@referredType

</td><td>

Type of item or service.Valid values for case tickets:

-   asset
-   product
-   product\_inventory

Valid values for incident tickets:

-   cmdb\_ci
-   cmdb\_ci\_service

Data type: String

</td></tr><tr><td>

relatedEntity.@type

</td><td>

This value is always `relatedEntity`.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

Details about contacts for the ticket.Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the related party. The sys\_id can be from the following tables depending on the ticket type and the related party type.Case:

-   Account \[customer\_account\]; Related party type is `customer`
-   Contact \[customer\_contact\]; Related party type is `customer_contact`

Incident:

-   Company \[core\_company\]; Related party type is `customer`
-   User \[sys\_user\]; Related party type is `customer_contact`

Case or incident:

-   Group \[sys\_user\_group\]; Related party type is `assignment_group`
-   User \[sys\_user\]; Related party type is `assigned_to`

Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of related party.Possible values:

-   `assigned_to`: User assigned to work on the ticket.
-   `assignment_group`: Group assigned to work on the ticket.
-   `customer`: Company or account for the ticket.
-   `customer_contact`: Caller or contact for the ticket.

Data type: String

</td></tr><tr><td>

severity

</td><td>

The severity of the issue described by the trouble ticket.Data type: String

</td></tr><tr><td>

status

</td><td>

The current status of the trouble ticket.Data type: String

</td></tr><tr><td>

ticketType

</td><td>

The type of ticket.Possible values:

-   Case
-   Incident
-   Service Problem Case

Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates a trouble ticket case record.

```
curl "https://instance.servicenow.com/api/sn_ind_tsm_sdwan/ticket/troubleTicket" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   "name": "Laptop problem",
   "description": "Laptop keeps shutting off unexpectedly",
   "severity": "2",
   "status": "New",
   "ticketType": "Case",
   "channel": {
      "name": "Web"
   },
   "note": [
      {
         "text": "Work note about this case",
         "@type": "work_notes"
      },
      {
         "text": "Comment about this case",
         "@type": "comments"
      }
   ],
   "relatedEntity": [
      {
         "id": "74a9ec0d3790200044e0bfc8bcbe5d7f",
         "@referredType": "asset"
      }
   ],
   "relatedParty": [
      {
         "id": "62826bf03710200044e0bfc8bcbe5df1",
         "@referredType": "customer_contact"
      }
   ]
}" \
--user 'username':'password'
```

Response body.

```
{
   "id": "6467508d47e345508761b955d36d43f6",
   "href": "/api/sn_ind_tsm_sdwan/ticket/troubleTicket/6467508d47e345508761b955d36d43f6",
   "creationDate": "2022-05-16 23:38:55",
   "lastUpdate": "2022-05-16 23:38:55",
   "description": "Laptop keeps shutting off unexpectedly",
   "severity": "2 - High",
   "ticketType": "Case",
   "name": "Laptop problem",
   "status": "New",
   "channel": {
      "name": "web"
   },
   "relatedParty": [
      {
         "id": "",
         "name": "",
         "@referredType": "customer"
      },
      {
         "id": "62826bf03710200044e0bfc8bcbe5df1",
         "name": "",
         "@referredType": "customer_contact"
      },
      {
         "id": "",
         "name": "",
         "@referredType": "assignment_group"
      },
      {
         "id": "",
         "name": "",
         "@referredType": "assigned_to"
      }
   ],
   "relatedEntity": [
      {
         "id": "",
         "href": "",
         "name": "",
         "role": "This is the product associated with the case.",
         "@type": "relatedEntity",
         "@referredType": "product"
      },
      {
         "id": "74a9ec0d3790200044e0bfc8bcbe5d7f",
         "href": "",
         "name": "P1000597 - Apple MacBook Pro 15\"",
         "role": "This is the asset associated with the case.",
         "@type": "relatedEntity",
         "@referredType": "asset"
      }
      {
         "id": "a1913c3577b301108e191e599a5a99e8",
         "href": "",
         "name": "Deduplication and Compression PI0000037",
         "role": "This is the product inventory associated with the case.",
         "@type": "relatedEntity",
         "@referredType": "product_inventory"
      }
   ],
   "note": [
      {
         "text": "Comment about this case",
         "date": "2022-05-16 16:38:55",
         "author": "admin",
         "@type": "comments"
      }
   ],
   "@type": "TroubleTicket"
}
```

