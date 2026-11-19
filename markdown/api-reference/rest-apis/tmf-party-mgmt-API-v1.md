---
title: Party Management Open API v1
description: The Party Management Open API v1 provides endpoints for managing parties with a relationship to the enterprise, such as accounts, consumers, and contacts. Use this API to create, update, retrieve, and inactivate records in the Consumer \[csm\_consumer\], Account \[customer\_account\], and Contact \[customer\_contact\] tables.Inactivates a specified record from the Consumer \[csm\_consumer\] and Contact \[customer\_contact\] tables.Retrieves a specified record from the Consumer \[csm\_consumer\] or Contact \[customer\_contact\] tables. You can filter results by specific fields.Retrieves a list of all individual \(party\) records with a relationship to the enterprise. You can filter results by specific fields or IDs.Retrieves a specified record from the Account \[customer\_account\] tables. You can filter results by specific fields or IDs.Retrieves organization-level party records from the Company \[core\_company\] and Account \[customer\_account\] tables. You can filter results by specific fields or IDs.Updates an existing individual party record in the Consumer \[csm\_consumer\] or Contact \[customer\_contact\] table without replacing the entire resource.Updates an existing individual party record in the Account \[customer\_account\] tables without replacing the entire resource.Creates a new individual party management record in the Consumer \[csm\_consumer\] or Contact \[customer\_contact\] tables.Creates a new party organization record in the Account \[customer\_account\] tables. You can also create and associate Contact and Location records inline during organization creation, eliminating the need for separate POST operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/rest-apis/tmf-party-mgmt-API-v1.html
release: brazil
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-11-04"
reading_time_minutes: 85
breadcrumb: [Party Management Open API, REST API reference, API reference, API implementation and reference]
---

# Party Management Open API v1

The Party Management Open API v1 provides endpoints for managing parties with a relationship to the enterprise, such as accounts, consumers, and contacts. Use this API to create, update, retrieve, and inactivate records in the Consumer \[csm\_consumer\], Account \[customer\_account\], and Contact \[customer\_contact\] tables.

**Note:** v2 is available for all Party Management Open API endpoints. Requests use v2 by default; to use a v1 endpoint, specify v1 in the endpoint path. For differences between versions, see [Party Management Open API v2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/tmf-party-mgmt-API-v2.md).

This API is provided within the sn\_tmf\_api namespace. The calling user must have the sn\_tmf\_api.party\_integrator role. The Customer Service Base Entities \(com.snc.cs\_base\) plugin is required, particularly for all GET operations.

You can extend this API to customize required parameters, request body validation, additional REST operations, and field mappings. Sensitive fields, such as phone numbers, may require special ACL permissions for update or retrieval.

**Parent Topic:**[Party Management Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/tmf-party-management-open-api.md)

## Party Management v1 – DELETE /api/sn\_tmf\_api/v1/party/individual/\{id\}

Inactivates a specified record from the Consumer \[csm\_consumer\] and Contact \[customer\_contact\] tables.

### URL format

Versioned URL: `/api/sn_tmf_api/{api_version}/party/individual/{id}`

Default URL: `/api/sn_tmf_api/v1/party/individual/{id}`

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

id

</td><td>

Sys\_id or external\_id of the Consumer or Contact record to set to an inactive state.Table: Consumer \[csm\_consumer\] and Contact \[customer\_contact\].

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Resource not found. Sys\_id or external\_id doesn't exist in the system. Try a different ID.|

### Response body parameters \(JSON or XML\)

<table id="table_cnv_cdg_dlc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

None

</td><td>

**Note:** Doesn't return a response body. Reference status codes for a success or failure indicator.

</td></tr></tbody>
</table>### cURL request

The following example deletes the given record.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v1/party/individual/a1b2c3d4e5f6478990abcdef12345678" \
  --request DELETE \
  --header "Accept: application/json" \
  --user 'user:password'
```

Doesn't return a response body. Reference status codes for a success or failure indicator.

## Party Management v1 - GET /api/sn\_tmf\_api/v1/party/individual/\{id\}

Retrieves a specified record from the Consumer \[csm\_consumer\] or Contact \[customer\_contact\] tables. You can filter results by specific fields.

### URL format

Versioned URL: `/api/sn_tmf_api/{api_version}/party/individual`

Default URL: `/api/sn_tmf_api/v1/party/individual`

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

id

</td><td>

Sys\_id or external\_id of the consumer or contact record to retrieve.Table: Consumer \[csm\_consumer\] or Contact \[customer\_contact\]

Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored.Valid fields:

-   @type
-   familyName
-   gender
-   givenName
-   href
-   id
-   middleName
-   name
-   nationality
-   status
-   title

Data type: String

Default: Returns all fields

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

<table id="partymgmt-GET-id-response-table"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Response object\}

</td><td>

Response object structure for the v1 request.```
{
   "id": "String",
   "href": "String",
   "@type": "String",
   "givenName": "String",
   "middleName": "String",
   "familyName": "String",
   "gender": "String",
   "nationality": "String",
   "title": "String",
   "status": "String",
   "partyOrPartyRole": {Object},
   "contactMedium": [Array],
   "externalReference": [Array],
   "partyCharacteristic": [Array],
   "relatedParty": [Array]
}
```

</td></tr><tr><td>

@type

</td><td>

Type of the individual record.Possible values:

-   `Consumer`: Consumer record.
-   `Contact`: Contact record.

Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of means for contacting the individual.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "country": "String",
  "emailAddress": "String",
  "locationId": "String",
  "mediumType": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": "Boolean",
  "stateOrProvince": "String",
  "street1": "String",
  "street2": "String"
 }
]
```

</td></tr><tr><td>

contactMedium.@type

</td><td>

Schema or subclass type of the contact medium.Possible values:

-   `BusinessPhoneContactMedium`: Business phone number.
-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `PhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location record linked to the address.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact channel.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Possible values:

-   `true`: Preferred contact medium.
-   `false`: Not the preferred contact medium.

Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

State or province of the address. For example, `New Jersey`.Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

First line of the street address.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Second line of the street address, such as a suite or floor.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the individual in external systems.Data type: Array of Objects

```
"externalReference": [
 {
  "externalIdentifierType": "String",
  "id": "String"
 }
]
```

</td></tr><tr><td>

externalReference.externalIdentifierType

</td><td>

Type of external system or identifier. For example, `linkedin` or `Instagram`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the individual in the external system, such as a profile URL.Data type: String

</td></tr><tr><td>

familyName

</td><td>

Last name of the individual.Data type: String

</td></tr><tr><td>

gender

</td><td>

Gender of the individual.Data type: String

</td></tr><tr><td>

givenName

</td><td>

First name of the individual.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the Consumer or Contact record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the Consumer or Contact record.Table: Consumer \[csm\_consumer\] or Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics associated with the individual.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristic.@type

</td><td>

Subclass type of the characteristic.Possible values:

-   `BooleanCharacteristic`
-   `StringCharacteristic`

Data type: String

</td></tr><tr><td>

partyCharacteristic.name

</td><td>

Name of the characteristic. For example, `notes`, `dateFormat`, `timeZone`, `vip`, or `notification`.Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic.Data type: Depends on **valueType**. For example, String or Boolean.

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value. For example, `string` or `boolean`.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Party type and role of the individual record. In POST requests, determines whether the request creates a Consumer or Contact record.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "role": "String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

Type of party.Possible values:

-   `Consumer`
-   `Contact`

Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Role of the individual.Possible values:

-   `Consumer`: Consumer record.
-   `Contact`: Contact record.

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties related to the individual.Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related party.Data type: Object

```
"partyOrPartyRole": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party.Possible values:

-   `Individual`: Related party is a user.
-   `Organization`: Related party is a company or department.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related party record.Table: Depends on the related party role:

-   Company: Company \[core\_company\]
-   Department: Department \[cmn\_department\]
-   User: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related party plays for the individual.Possible values:

-   `Company`: Company associated with the individual.
-   `Department`: Department associated with the individual.
-   `User`: User associated with the consumer.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the individual record.Possible values:

-   `active`: Record is active.
-   `inactive`: Record is inactive.

Data type: String

</td></tr><tr><td>

title

</td><td>

Prefix or title of the individual. For example, `Mr`, `Ms`, or `Dr`.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example retrieves the Consumer record with sys\_id a1b2c3d4e5f6478990abcdef12345678.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v1/party/individual/a1b2c3d4e5f6478990abcdef12345678" \
  --request GET \
  --header "Accept: application/json" \
  --user 'user:password'
```

Response body.

```
{
  "id": "a1b2c3d4e5f6478990abcdef12345678",
  "href": "api/sn_tmf_api/party/individual/a1b2c3d4e5f6478990abcdef12345678",
  "@type": "Consumer",
  "givenName": "John",
  "middleName": "A.",
  "familyName": "Doe",
  "gender": "male",
  "nationality": "American",
  "title": "Mr",
  "status": "active",
  "partyOrPartyRole": {
    "@type": "Consumer",
    "role": "Consumer"
  },
  "contactMedium": [
    {
      "preferred": true,
      "mediumType": "email",
      "emailAddress": "john.doe@example.com",
      "@type": "EmailContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "mobilePhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "PhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "businessPhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "BusinessPhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "faxPhone",
      "phoneNumber": "123456789",
      "@type": "FaxPhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "homePhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "HomePhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "postalAddress",
      "@type": "GeographicAddressContactMedium",
      "locationId": "25ab9e240a0a0bb3009eb9ef8dd0a2c0",
      "city": "Morristown",
      "country": "USA",
      "postCode": "07960",
      "stateOrProvince": "New Jersey",
      "street1": "240 Headquarters Plaza",
      "street2": "East Tower - 10th Floor"
    },
    {
      "preferred": false,
      "mediumType": "postalAddress",
      "@type": "GeographicAddressContactMedium",
      "locationId": "25aba17a0a0a0bb3007efd809d6e695c",
      "city": "Nashville",
      "country": "USA",
      "postCode": "37203",
      "stateOrProvince": "Tennessee",
      "street1": "100 Broadway",
      "street2": "Suite 1100"
    }
  ],
  "externalReference": [
    {
      "externalIdentifierType": "facebook",
      "id": "http://facebook.com/johndoe"
    }
  ],
  "partyCharacteristic": [
    {
      "name": "notes",
      "value": "Notes about the consumer.",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "dateFormat",
      "value": "dd-mm-yyyy",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "timeFormat",
      "value": "hh.mm.ss (12 hour)",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "notification",
      "value": "Enable",
      "valueType": "string",
      "@type": "StringCharacteristic"
    }
  ],
  "relatedParty": [
    {
      "role": "User",
      "partyOrPartyRole": {
        "id": "36901a6381116a50f8776cfcbee15f3c",
        "name": "John Doe",
        "@type": "Individual"
      }
    }
  ]
}
```

## Party Management v1 – GET /api/sn\_tmf\_api/v1/party/individual

Retrieves a list of all individual \(party\) records with a relationship to the enterprise. You can filter results by specific fields or IDs.

### URL format

Versioned URL: `/api/sn_tmf_api/v1/party/individual`

Default URL: `/api/sn_tmf_api/v1/party/individual`

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

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored.Valid fields:

-   @type
-   familyName
-   gender
-   givenName
-   href
-   id
-   middleName
-   name
-   nationality
-   status
-   title

Data type: String

Default: Returns all fields.

</td></tr><tr><td>

id

</td><td>

Filter party management by sys\_id. Specified sys\_ids are returned in the response.Data type: String

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval.Data type: Number

Default: 20

Maximum: 100

</td></tr><tr><td>

offset

</td><td>

Starting index at which to begin retrieving records. Use this value to paginate record retrieval.Data type: Number

Default: 0

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Range

</td><td>

Range of content returned in a paginated call.For example, if offset=2 and limit=3, the value of the Content-Range header is items 3-5.

</td></tr><tr><td>

Content-Type

</td><td>

Data format of the response body. Only supports application/json.

</td></tr><tr><td>

Link

</td><td>

Contains the following links to navigate through query results:

-   first
-   last
-   next
-   previous

</td></tr><tr><td>

X-Total-Count

</td><td>

For paginated queries, this header specifies the total number of records available on the server.

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Request successfully processed. Full resource returned in response \(no pagination\).

</td></tr><tr><td>

206

</td><td>

Partial resource returned in response \(with pagination\).

</td></tr><tr><td>

400

</td><td>

Bad request. Possible reasons:-   Invalid path parameter
-   Invalid URI

</td></tr><tr><td>

404

</td><td>

Record not found. No records matching the query parameters are found in the table.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="partymgmt-GET-individual-response-table"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Response object\}

</td><td>

List of individual records. Each record in the array has the following structure.```
[
 {
   "id": "String",
   "href": "String",
   "@type": "String",
   "givenName": "String",
   "middleName": "String",
   "familyName": "String",
   "gender": "String",
   "nationality": "String",
   "title": "String",
   "status": "String",
   "partyOrPartyRole": {Object},
   "contactMedium": [Array],
   "externalReference": [Array],
   "partyCharacteristic": [Array],
   "relatedParty": [Array]
 }
]
```

</td></tr><tr><td>

@type

</td><td>

Type of the individual record.Possible values:

-   `Consumer`: Consumer record.
-   `Contact`: Contact record.

Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of means for contacting the individual.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "country": "String",
  "emailAddress": "String",
  "locationId": "String",
  "mediumType": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": "Boolean",
  "stateOrProvince": "String",
  "street1": "String",
  "street2": "String"
 }
]
```

</td></tr><tr><td>

contactMedium.@type

</td><td>

Schema or subclass type of the contact medium.Possible values:

-   `BusinessPhoneContactMedium`: Business phone number.
-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `PhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location record linked to the address.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact channel.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Possible values:

-   `true`: Preferred contact medium.
-   `false`: Not the preferred contact medium.

Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

State or province of the address. For example, `New Jersey`.Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

First line of the street address.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Second line of the street address, such as a suite or floor.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the individual in external systems.Data type: Array of Objects

```
"externalReference": [
 {
  "externalIdentifierType": "String",
  "id": "String"
 }
]
```

</td></tr><tr><td>

externalReference.externalIdentifierType

</td><td>

Type of external system or identifier. For example, `linkedin` or `Instagram`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the individual in the external system, such as a profile URL.Data type: String

</td></tr><tr><td>

familyName

</td><td>

Last name of the individual.Data type: String

</td></tr><tr><td>

gender

</td><td>

Gender of the individual.Data type: String

</td></tr><tr><td>

givenName

</td><td>

First name of the individual.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the Consumer or Contact record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the Consumer or Contact record.Table: Consumer \[csm\_consumer\] or Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

name

</td><td>

User name of the individual.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics associated with the individual.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristic.@type

</td><td>

Subclass type of the characteristic.Possible values:

-   `BooleanCharacteristic`
-   `StringCharacteristic`

Data type: String

</td></tr><tr><td>

partyCharacteristic.name

</td><td>

Name of the characteristic. For example, `notes`, `dateFormat`, `timeZone`, `vip`, or `notification`.Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic.Data type: Depends on **valueType**. For example, String or Boolean.

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value. For example, `string` or `boolean`.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Party type and role of the individual record. In POST requests, determines whether the request creates a Consumer or Contact record.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "role": "String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

Type of party.Possible values:

-   `Consumer`
-   `Contact`

Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Role of the individual.Possible values:

-   `Consumer`: Consumer record.
-   `Contact`: Contact record.

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties related to the individual.Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related party.Data type: Object

```
"partyOrPartyRole": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party.Possible values:

-   `Individual`: Related party is a user.
-   `Organization`: Related party is a company or department.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related party record.Table: Depends on the related party role:

-   Company: Company \[core\_company\]
-   Department: Department \[cmn\_department\]
-   User: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related party plays for the individual.Possible values:

-   `Company`: Company associated with the individual.
-   `Department`: Department associated with the individual.
-   `User`: User associated with the consumer.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the individual record.Possible values:

-   `active`: Record is active.
-   `inactive`: Record is inactive.

Data type: String

</td></tr><tr><td>

title

</td><td>

Prefix or title of the individual. For example, `Mr`, `Ms`, or `Dr`.Data type: String

</td></tr></tbody>
</table>### cURL request

Retrieves a list of all party management records in the instance.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v1/party/individual" \
  --request GET \
  --header "Accept: application/json" \
  --user 'user:password'
```

Response body for a Contact record.

```
[
{
   "id": "34d92aaa11f43110f877366201dea67b",
   "href": "api/sn_tmf_api/party/individual/34d92aaa11f43110f877366201dea67b",
   "name": "carlos.star",
   "givenName": "Carlos",
   "middleName": "",
   "familyName": "Star",
   "gender": "",
   "title": "",
   "partyCharacteristic": [
     {
       "name": "notification",
       "value": "Enable",
       "valueType": "string",
       "@type": "StringCharacteristic"
     },
     {
       "name": "preferredLanguage",
       "value": "",
       "valueType": "string",
       "@type": "StringCharacteristic"
     },
     {
       "name": "dateFormat",
       "value": "",
       "valueType": "string",
       "@type": "StringCharacteristic"
     },
     {
       "name": "timeFormat",
       "value": "",
       "valueType": "string",
       "@type": "StringCharacteristic"
     },
     {
       "name": "timeZone",
       "value": "",
       "valueType": "string",
       "@type": "StringCharacteristic"
     },
     {
       "name": "vip",
       "value": false,
       "valueType": "boolean",
       "@type": "BooleanCharacteristic"
     },
     {
       "name": "webServiceAccessOnly",
       "value": false,
       "valueType": "boolean",
       "@type": "BooleanCharacteristic"
     },
     {
       "name": "source",
       "value": "",
       "valueType": "string",
       "@type": "StringCharacteristic"
     },
     {
       "name": "eduStatus",
       "value": "Faculty",
       "valueType": "string",
       "@type": "StringCharacteristic"
     }
   ],
   "contactMedium": [
     {
       "preferred": false,
       "mediumType": "email",
       "emailAddress": "carlos.star@example.com",
       "@type": "EmailContactMedium"
     },
     {
       "preferred": false,
       "mediumType": "businessPhone",
       "phoneNumber": "",
       "@type": "BusinessPhoneContactMedium"
     },
     {
       "preferred": false,
       "mediumType": "homePhone",
       "phoneNumber": "",
       "@type": "HomePhoneContactMedium"
     },
     {
       "preferred": false,
       "mediumType": "mobilePhone",
       "phoneNumber": "",
       "@type": "PhoneContactMedium"
     }
   ],
   "externalReference": [],
   "relatedParty": [
     {
       "role": "Company",
       "partyOrPartyRole": {
         "id": "9e2fd2ee11b43110f877366201dea674",
         "name": "Startech svcs",
         "@type": "Organization"
       }
     },
     {
       "role": "Department",
       "partyOrPartyRole": {
         "id": "",
         "name": "",
         "@type": "Organization"
       }
     }
   ],
   "status": "active",
   "@type": "Contact",
   "partyOrPartyRole": {
     "@type": "Contact",
     "role": "Contact"
   }
 }
]
```

Response body for a Consumer record.

```
[
{
   "id": "168bfc6953a46210132bddeeff7b129f",
   "href": "api/sn_tmf_api/party/individual/168bfc6953a46210132bddeeff7b129f",
   "givenName": "Priya",
   "middleName": "",
   "familyName": "Patel",
   "gender": "",
   "nationality": "",
   "title": "",
   "partyCharacteristic": [
     {
       "name": "notes",
       "value": "",
       "valueType": "string",
       "@type": "StringCharacteristic"
     },
     {
       "name": "user",
       "value": "",
       "valueType": "string",
       "@type": "StringCharacteristic"
     },
     {
       "name": "notification",
       "value": "Enable",
       "valueType": "string",
       "@type": "StringCharacteristic"
     },
     {
       "name": "preferredLanguage",
       "value": "",
       "valueType": "string",
       "@type": "StringCharacteristic"
     },
     {
       "name": "dateFormat",
       "value": "",
       "valueType": "string",
       "@type": "StringCharacteristic"
     },
     {
       "name": "timeFormat",
       "value": "",
       "valueType": "string",
       "@type": "StringCharacteristic"
     },
     {
       "name": "timeZone",
       "value": "",
       "valueType": "string",
       "@type": "StringCharacteristic"
     }
   ],
   "contactMedium": [
     {
       "preferred": false,
       "mediumType": "businessPhone",
       "phoneNumber": "",
       "@type": "BusinessPhoneContactMedium"
     },
     {
       "preferred": false,
       "mediumType": "homePhone",
       "phoneNumber": "",
       "@type": "HomePhoneContactMedium"
     },
     {
       "preferred": false,
       "mediumType": "mobilePhone",
       "phoneNumber": "",
       "@type": "PhoneContactMedium"
     },
     {
       "preferred": false,
       "mediumType": "faxPhone",
       "phoneNumber": "",
       "@type": "FaxPhoneContactMedium"
     },
     {
       "preferred": false,
       "mediumType": "postalAddress",
       "@type": "GeographicAddressContactMedium",
       "city": "Austin",
       "locationId": "a39bfc6953a46210132bddeeff7b12b7",
       "country": "USA",
       "postCode": "78701",
       "stateOrProvince": "Texas",
       "street1": "500 Congress Ave",
       "street2": ""
     }
   ],
   "externalReference": [],
   "relatedParty": [
     {
       "role": "User",
       "partyOrPartyRole": {
         "id": "",
         "name": "",
         "@type": "Individual"
       }
     }
   ],
   "status": "active",
   "@type": "Consumer",
   "partyOrPartyRole": {
     "@type": "Consumer",
     "role": "Consumer"
   }
 }
]
```

## Party Management v1 – GET/api/ sn\_tmf\_api/v1/party/organization/\{id\}

Retrieves a specified record from the Account \[customer\_account\] tables. You can filter results by specific fields or IDs.

### URL format

Versioned URL: `/api/sn_tmf_api/v1/party/organization/{id}`

Default URL: `/api/sn_tmf_api/v1/party/organization/{id}`

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

id

</td><td>

Sys\_id of the company or account record to retrieve.Table: Account \[customer\_account\]

Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored.Valid fields:

-   @type
-   href
-   id
-   legalName
-   name
-   status
-   tradingName

Data type: String

Default: Returns all fields

</td></tr><tr><td>

id

</td><td>

Filter party management by sys\_id. Specified sys\_ids are returned in the response.Data type: String

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval.Data type: Number

Default: 20

Maximum: 100

</td></tr><tr><td>

offset

</td><td>

Starting index at which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks.Data type: Number

Default: 0

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

<table id="partymgmt-GET-org-id-response-table"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Response object\}

</td><td>

Response object structure for the v1 request.```
{
  "id": "String",
  "href": "String",
  "@type": "String",
  "name": "String",
  "legalName": "String",
  "tradingName": "String",
  "status": "String",
  "partyOrPartyRole": {Object},
  "contactMedium": [Array],
  "externalReference": [Array],
  "partyCharacteristic": [Array],
  "relatedParty": [Array],
  "organizationChildRelationship": [Array],
  "organizationParentRelationship": {Object}
}
```

</td></tr><tr><td>

@type

</td><td>

Type of the organization record. Value is always `Account`.Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of means for contacting the organization.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "emailAddress": "String",
  "mediumType": "String",
  "phoneNumber": "String",
  "preferred": "Boolean"
 }
]
```

</td></tr><tr><td>

contactMedium.@type

</td><td>

Schema or subclass type of the contact medium.Possible values:

-   `BusinessPhoneContactMedium`: Business phone number.
-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `PhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address.Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact channel.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Possible values:

-   `true`: Preferred contact medium.
-   `false`: Not the preferred contact medium.

Data type: Boolean

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the organization in external systems.Data type: Array of Objects

```
"externalReference": [
 {
  "externalIdentifierType": "String",
  "name": "String"
 }
]
```

</td></tr><tr><td>

externalReference.externalIdentifierType

</td><td>

Type of external system or identifier. For example, `linkedin` or `Instagram`.Data type: String

</td></tr><tr><td>

externalReference.name

</td><td>

Name or identifier of the organization in the external system. For example, `facebook.com`.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the Account record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the Account record.Table: Account \[customer\_account\]

Data type: String

</td></tr><tr><td>

legalName

</td><td>

Legal name of the organization.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the organization.Data type: String

</td></tr><tr><td>

organizationChildRelationship

</td><td>

List of child organization relationships, such as partner, subsidiary, or branch organizations.Data type: Array of Objects

```
"organizationChildRelationship": [
 {
  "relationshipType": "String",
  "organization": {Object}
 }
]
```

</td></tr><tr><td>

organizationChildRelationship.organization

</td><td>

Details about the child organization.Data type: Object

```
"organization": {
  "id": "String",
  "name": "String",
  "href": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

organizationChildRelationship.organization.@type

</td><td>

Type of the organization object. Value is always `Organization`.Data type: String

</td></tr><tr><td>

organizationChildRelationship.organization.href

</td><td>

Relative link to the child organization record.Data type: String

</td></tr><tr><td>

organizationChildRelationship.organization.id

</td><td>

Sys\_id of the child organization record.Table: Account \[customer\_account\] or Company \[core\_company\]

Data type: String

</td></tr><tr><td>

organizationChildRelationship.organization.name

</td><td>

Display name of the child organization.Data type: String

</td></tr><tr><td>

organizationChildRelationship.relationshipType

</td><td>

Type of relationship between this organization and the child organization. For example, `Partner Account`.Data type: String

</td></tr><tr><td>

organizationParentRelationship

</td><td>

Relationship to the parent organization.Data type: Object

```
"organizationParentRelationship": {
  "relationshipType": "String",
  "organization": {Object}
}
```

</td></tr><tr><td>

organizationParentRelationship.organization

</td><td>

Details about the parent organization.Data type: Object

```
"organization": {
  "id": "String",
  "name": "String",
  "href": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

organizationParentRelationship.organization.@type

</td><td>

Type of the organization object. Value is always `Organization`.Data type: String

</td></tr><tr><td>

organizationParentRelationship.organization.href

</td><td>

Relative link to the parent organization record.Data type: String

</td></tr><tr><td>

organizationParentRelationship.organization.id

</td><td>

Sys\_id of the parent organization record.Table: Account \[customer\_account\] or Company \[core\_company\]

Data type: String

</td></tr><tr><td>

organizationParentRelationship.organization.name

</td><td>

Display name of the parent organization.Data type: String

</td></tr><tr><td>

organizationParentRelationship.relationshipType

</td><td>

Type of relationship between this organization and its parent.Possible values:

-   `Account`
-   `Company`
-   `HoldingCompany`
-   `ParentAccount`

Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics associated with the organization.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristic.@type

</td><td>

Subclass type of the characteristic.Possible values:

-   `BooleanCharacteristic`
-   `IntegerCharacteristic`
-   `StringArrayCharacteristic`
-   `StringCharacteristic`

Data type: String

</td></tr><tr><td>

partyCharacteristic.name

</td><td>

Name of the characteristic.Possible values:

-   `accountCode`
-   `identificationNumber`
-   `industry`
-   `manufacturer`
-   `marketCap`
-   `notes`
-   `numEmployees`
-   `profits`
-   `publiclyTraded`
-   `rankTier`
-   `registrationCode`
-   `revenuePerYear`
-   `stockPrice`
-   `stockSymbol`
-   `taxId`
-   `vendor`
-   `vendorType`
-   `website`

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic, as a string regardless of **valueType**. For example, `"false"` or `"10"`.Data type: String

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `choice`
-   `integer`
-   `list`
-   `string`

Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Party type, role, and account classification of the organization record.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "role": "String",
  "name": "String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

Type of party. Value is always `Account`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.name

</td><td>

Account classification. Multiple classifications are joined with underscores. For example, `customer` or `customer_partner`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Role of the party. Value is always `Account`.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts related to the organization.Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related contact.Data type: Object

```
"partyOrPartyRole": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Value is always `Individual`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related contact record.Table: Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the related contact.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related contact plays for the organization.Possible values:

-   `other`: Other contact for the organization.
-   `primaryContact`: Primary contact for the organization.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the organization record.Possible values:

-   `active`: Organization is active.
-   `inactive`: Organization is inactive.

Data type: String

</td></tr><tr><td>

tradingName

</td><td>

Name that the organization trades under.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example retrieves the Account record with sys\_id a1b2c3d4e5f6478990abcdef12345678.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v1/party/organization/a1b2c3d4e5f6478990abcdef12345678" \
  --request GET \
  --header "Accept: application/json" \
  --user 'user:password'
```

Response body.

```
{
  "id": "a1b2c3d4e5f6478990abcdef12345678",
  "href": "api/sn_tmf_api/party/organization/a1b2c3d4e5f6478990abcdef12345678",
  "@type": "Account",
  "name": "Advanced Super Computing",
  "legalName": "Advanced Super Computing Inc.",
  "tradingName": "ASC",
  "status": "inactive",
  "partyOrPartyRole": {
    "@type": "Account",
    "role": "Account",
    "name": "customer_partner_vendor_manufacturer"
  },
  "contactMedium": [
    {
      "preferred": false,
      "mediumType": "email",
      "emailAddress": "user@example.com",
      "@type": "EmailContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "businessPhone",
      "phoneNumber": "+1-202-555-0123",
      "@type": "BusinessPhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "faxPhone",
      "phoneNumber": "",
      "@type": "FaxPhoneContactMedium"
    }
  ],
  "externalReference": [
    {
      "externalIdentifierType": "Facebook",
      "name": "facebook.com"
    },
    {
      "externalIdentifierType": "Twitter",
      "name": "twitter.com"
    }
  ],
  "partyCharacteristic": [
    {
      "name": "notes",
      "value": "Strategic hardware partner.",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "registrationCode",
      "value": "23456789",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "accountCode",
      "value": "ACCT0001030",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "identificationNumber",
      "value": "",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "taxId",
      "value": "",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "industry",
      "value": "Manufacturing",
      "valueType": "choice",
      "@type": "StringCharacteristic"
    },
    {
      "name": "numEmployees",
      "value": "",
      "valueType": "integer",
      "@type": "IntegerCharacteristic"
    },
    {
      "name": "rankTier",
      "value": "",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "publiclyTraded",
      "value": "false",
      "valueType": "boolean",
      "@type": "BooleanCharacteristic"
    },
    {
      "name": "stockSymbol",
      "value": "",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "stockPrice",
      "value": "",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "vendorType",
      "value": "Services, Applications",
      "valueType": "list",
      "@type": "StringArrayCharacteristic"
    },
    {
      "name": "marketCap",
      "value": "0",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "profits",
      "value": "0",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "revenuePerYear",
      "value": "0",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "website",
      "value": "example.com",
      "valueType": "string",
      "@type": "StringCharacteristic"
    }
  ],
  "relatedParty": [
    {
      "role": "primaryContact",
      "partyOrPartyRole": {
        "id": "b88d14843bc02300bfe04d72f3efc4cd",
        "name": "Amy Chen",
        "@type": "Individual"
      }
    },
    {
      "role": "other",
      "partyOrPartyRole": {
        "id": "016b7a36ff14a610f8dfffffffffffcb",
        "name": "Mary Star",
        "@type": "Individual"
      }
    }
  ],
  "organizationChildRelationship": [
    {
      "relationshipType": "Partner Account",
      "organization": {
        "id": "9e2fd2ee11b43110f877366201dea674",
        "name": "Startech svcs",
        "href": "api/sn_tmf_api/party/organization/9e2fd2ee11b43110f877366201dea674",
        "@type": "Organization"
      }
    }
  ],
  "organizationParentRelationship": {
    "relationshipType": "Account",
    "organization": {
      "id": "ffc68911c35420105252716b7d40dd55",
      "name": "Funco Intl.",
      "href": "api/sn_tmf_api/party/organization/ffc68911c35420105252716b7d40dd55",
      "@type": "Organization"
    }
  }
}
```

## Party Management v1 - GET /api/sn\_tmf\_api/v1/party/organization

Retrieves organization-level party records from the Company \[core\_company\] and Account \[customer\_account\] tables. You can filter results by specific fields or IDs.

### URL format

Versioned URL: `/api/sn_tmf_api/v1/party/organization`

Default URL: `/api/sn_tmf_api/v1/party/organization`

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

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored.Valid fields:

-   @type
-   href
-   id
-   legalName
-   name
-   status
-   tradingName

Data type: String

Default: Returns all fields

</td></tr><tr><td>

id

</td><td>

Filter party management by sys\_id. Specified sys\_ids are returned in the response.Data type: String

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval.Data type: Number

Default: 20

Maximum: 100

</td></tr><tr><td>

offset

</td><td>

Starting index at which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks.Data type: Number

Default: 0

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

<table id="partymgmt-GET-org-response-table"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Response object\}

</td><td>

List of organization records. Each record in the array has the following structure.```
[
  {
    "id": "String",
    "href": "String",
    "@type": "String",
    "name": "String",
    "legalName": "String",
    "tradingName": "String",
    "status": "String",
    "partyOrPartyRole": {Object},
    "contactMedium": [Array],
    "externalReference": [Array],
    "partyCharacteristic": [Array],
    "relatedParty": [Array],
    "organizationChildRelationship": [Array],
    "organizationParentRelationship": {Object}
  }
]
```

</td></tr><tr><td>

@type

</td><td>

Type of the organization record. Value is always `Account`.Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of means for contacting the organization.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "emailAddress": "String",
  "mediumType": "String",
  "phoneNumber": "String",
  "preferred": "Boolean"
 }
]
```

</td></tr><tr><td>

contactMedium.@type

</td><td>

Schema or subclass type of the contact medium.Possible values:

-   `BusinessPhoneContactMedium`: Business phone number.
-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `PhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address.Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact channel.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Possible values:

-   `true`: Preferred contact medium.
-   `false`: Not the preferred contact medium.

Data type: Boolean

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the organization in external systems.Data type: Array of Objects

```
"externalReference": [
 {
  "externalIdentifierType": "String",
  "name": "String"
 }
]
```

</td></tr><tr><td>

externalReference.externalIdentifierType

</td><td>

Type of external system or identifier. For example, `linkedin` or `Instagram`.Data type: String

</td></tr><tr><td>

externalReference.name

</td><td>

Name or identifier of the organization in the external system. For example, `facebook.com`.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the Account record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the Account record.Table: Account \[customer\_account\]

Data type: String

</td></tr><tr><td>

legalName

</td><td>

Legal name of the organization.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the organization.Data type: String

</td></tr><tr><td>

organizationChildRelationship

</td><td>

List of child organization relationships, such as partner, subsidiary, or branch organizations.Data type: Array of Objects

```
"organizationChildRelationship": [
 {
  "relationshipType": "String",
  "organization": {Object}
 }
]
```

</td></tr><tr><td>

organizationChildRelationship.organization

</td><td>

Details about the child organization.Data type: Object

```
"organization": {
  "id": "String",
  "name": "String",
  "href": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

organizationChildRelationship.organization.@type

</td><td>

Type of the organization object. Value is always `Organization`.Data type: String

</td></tr><tr><td>

organizationChildRelationship.organization.href

</td><td>

Relative link to the child organization record.Data type: String

</td></tr><tr><td>

organizationChildRelationship.organization.id

</td><td>

Sys\_id of the child organization record.Table: Account \[customer\_account\] or Company \[core\_company\]

Data type: String

</td></tr><tr><td>

organizationChildRelationship.organization.name

</td><td>

Display name of the child organization.Data type: String

</td></tr><tr><td>

organizationChildRelationship.relationshipType

</td><td>

Type of relationship between this organization and the child organization. For example, `Partner Account`.Data type: String

</td></tr><tr><td>

organizationParentRelationship

</td><td>

Relationship to the parent organization.Data type: Object

```
"organizationParentRelationship": {
  "relationshipType": "String",
  "organization": {Object}
}
```

</td></tr><tr><td>

organizationParentRelationship.organization

</td><td>

Details about the parent organization.Data type: Object

```
"organization": {
  "id": "String",
  "name": "String",
  "href": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

organizationParentRelationship.organization.@type

</td><td>

Type of the organization object. Value is always `Organization`.Data type: String

</td></tr><tr><td>

organizationParentRelationship.organization.href

</td><td>

Relative link to the parent organization record.Data type: String

</td></tr><tr><td>

organizationParentRelationship.organization.id

</td><td>

Sys\_id of the parent organization record.Table: Account \[customer\_account\] or Company \[core\_company\]

Data type: String

</td></tr><tr><td>

organizationParentRelationship.organization.name

</td><td>

Display name of the parent organization.Data type: String

</td></tr><tr><td>

organizationParentRelationship.relationshipType

</td><td>

Type of relationship between this organization and its parent.Possible values:

-   `Account`
-   `Company`
-   `HoldingCompany`
-   `ParentAccount`

Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics associated with the organization.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristic.@type

</td><td>

Subclass type of the characteristic.Possible values:

-   `BooleanCharacteristic`
-   `IntegerCharacteristic`
-   `StringArrayCharacteristic`
-   `StringCharacteristic`

Data type: String

</td></tr><tr><td>

partyCharacteristic.name

</td><td>

Name of the characteristic.Possible values:

-   `accountCode`
-   `identificationNumber`
-   `industry`
-   `manufacturer`
-   `marketCap`
-   `notes`
-   `numEmployees`
-   `profits`
-   `publiclyTraded`
-   `rankTier`
-   `registrationCode`
-   `revenuePerYear`
-   `stockPrice`
-   `stockSymbol`
-   `taxId`
-   `vendor`
-   `vendorType`
-   `website`

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic, as a string regardless of **valueType**. For example, `"false"` or `"10"`.Data type: String

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `choice`
-   `integer`
-   `list`
-   `string`

Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Party type, role, and account classification of the organization record.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "role": "String",
  "name": "String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

Type of party. Value is always `Account`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.name

</td><td>

Account classification. Multiple classifications are joined with underscores. For example, `customer` or `customer_partner`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Role of the party. Value is always `Account`.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts related to the organization.Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related contact.Data type: Object

```
"partyOrPartyRole": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Value is always `Individual`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related contact record.Table: Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the related contact.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related contact plays for the organization.Possible values:

-   `other`: Other contact for the organization.
-   `primaryContact`: Primary contact for the organization.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the organization record.Possible values:

-   `active`: Organization is active.
-   `inactive`: Organization is inactive.

Data type: String

</td></tr><tr><td>

tradingName

</td><td>

Name that the organization trades under.Data type: String

</td></tr></tbody>
</table>### cURL request

This returns all organization records related to the enterprise.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v1/party/organization" \
  --request GET \
  --header "Accept: application/json" \
  --user 'user:password'
```

Response body.

```
[
  {
    "id": "0bd6717c184da610f87765359bc696d3",
    "href": "api/sn_tmf_api/party/organization/0bd6717c184da610f87765359bc696d3",
    "@type": "Account",
    "name": "SERVICENOW 144",
    "legalName": "",
    "tradingName": "",
    "status": "active",
    "partyOrPartyRole": {
      "@type": "Account",
      "role": "Account",
      "name": "customer_partner"
    },
    "contactMedium": [
      {
        "preferred": false,
        "mediumType": "email",
        "emailAddress": "user@example.com",
        "@type": "EmailContactMedium"
      },
      {
        "preferred": false,
        "mediumType": "businessPhone",
        "phoneNumber": "+1-202-555-0123",
        "@type": "BusinessPhoneContactMedium"
      },
      {
        "preferred": false,
        "mediumType": "faxPhone",
        "phoneNumber": "",
        "@type": "FaxPhoneContactMedium"
      }
    ],
    "externalReference": [
      {
        "externalIdentifierType": "Instagram",
        "name": ""
      }
    ],
    "partyCharacteristic": [
      {
        "name": "notes",
        "value": "Testing for update the notes",
        "valueType": "string",
        "@type": "StringCharacteristic"
      },
      {
        "name": "registrationCode",
        "value": "111122112211",
        "valueType": "string",
        "@type": "StringCharacteristic"
      },
      {
        "name": "accountCode",
        "value": "accountcode1",
        "valueType": "string",
        "@type": "StringCharacteristic"
      },
      {
        "name": "identificationNumber",
        "value": "",
        "valueType": "string",
        "@type": "StringCharacteristic"
      },
      {
        "name": "taxId",
        "value": "CTNUM1000123",
        "valueType": "string",
        "@type": "StringCharacteristic"
      },
      {
        "name": "industry",
        "value": "Manufacturing",
        "valueType": "choice",
        "@type": "StringCharacteristic"
      },
      {
        "name": "numEmployees",
        "value": "",
        "valueType": "integer",
        "@type": "IntegerCharacteristic"
      },
      {
        "name": "rankTier",
        "value": "Valued Partner",
        "valueType": "string",
        "@type": "StringCharacteristic"
      },
      {
        "name": "publiclyTraded",
        "value": "false",
        "valueType": "boolean",
        "@type": "BooleanCharacteristic"
      },
      {
        "name": "stockSymbol",
        "value": "Market",
        "valueType": "string",
        "@type": "StringCharacteristic"
      },
      {
        "name": "stockPrice",
        "value": "1000",
        "valueType": "string",
        "@type": "StringCharacteristic"
      },
      {
        "name": "vendorType",
        "value": "Hardware",
        "valueType": "list",
        "@type": "StringArrayCharacteristic"
      },
      {
        "name": "marketCap",
        "value": "0",
        "valueType": "string",
        "@type": "StringCharacteristic"
      },
      {
        "name": "profits",
        "value": "0",
        "valueType": "string",
        "@type": "StringCharacteristic"
      },
      {
        "name": "revenuePerYear",
        "value": "0",
        "valueType": "string",
        "@type": "StringCharacteristic"
      },
      {
        "name": "website",
        "value": "",
        "valueType": "string",
        "@type": "StringCharacteristic"
      }
    ],
    "relatedParty": [],
    "organizationChildRelationship": [
      {
        "relationshipType": "Partner Account",
        "organization": {
          "id": "396b47201841a610f87765359bc696cf",
          "name": "Spark Technologies",
          "href": "api/sn_tmf_api/party/organization/396b47201841a610f87765359bc696cf",
          "@type": "Organization"
        }
      }
    ],
    "organizationParentRelationship": {
      "relationshipType": "Account",
      "organization": {
        "id": "9e2fd2ee11b43110f877366201dea674",
        "name": "Startech svcs",
        "href": "api/sn_tmf_api/party/organization/9e2fd2ee11b43110f877366201dea674",
        "@type": "Organization"
      }
    }
  }
]
```

## Party Management v1 – PATCH/api/sn\_tmf\_api/v1/party/individual/\{id\}

Updates an existing individual party record in the Consumer \[csm\_consumer\] or Contact \[customer\_contact\] table without replacing the entire resource.

### URL format

Versioned URL: `/api/sn_tmf_api/v1/party/individual`

Default URL: `/api/sn_tmf_api/v1/party/individual`

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

id

</td><td>

Sys\_id of the consumer or contact.Tables: Consumer \[csm\_consumer\] or Contact \[customer\_contact\]

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="partymgmt-PATCH-id-request-table" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Request object\}

</td><td>

Request object structure for the v1 request. Include only the fields to update.```
{
  "@type": "String",
  "name": "String",
  "givenName": "String",
  "middleName": "String",
  "familyName": "String",
  "gender": "String",
  "nationality": "String",
  "title": "String",
  "status": "String",
  "partyOrPartyRole": {Object},
  "contactMedium": [Array],
  "partyCharacteristic": [Array],
  "relatedParty": [Array]
}
```

</td></tr><tr><td>

@type

</td><td>

Type of the individual record.Possible values:

-   `Consumer`: Consumer record.
-   `Contact`: Contact record.

Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of means for contacting the individual.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "country": "String",
  "emailAddress": "String",
  "mediumType": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": "Boolean",
  "stateOrProvince": "String",
  "street1": "String",
  "street2": "String"
 }
]
```

</td></tr><tr><td>

contactMedium.@type

</td><td>

Schema or subclass type of the contact medium.Possible values:

-   `BusinessPhoneContactMedium`: Business phone number.
-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `PhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address.Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact channel.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Possible values:

-   `true`: Preferred contact medium.
-   `false`: Not the preferred contact medium.

Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

State or province of the address. For example, `New Jersey`.Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

First line of the street address.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Second line of the street address, such as a suite or floor.Data type: String

</td></tr><tr><td>

familyName

</td><td>

Last name of the individual.Data type: String

</td></tr><tr><td>

gender

</td><td>

Gender of the individual.Data type: String

</td></tr><tr><td>

givenName

</td><td>

First name of the individual.Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

name

</td><td>

User name of the individual.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics associated with the individual.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristic.@type

</td><td>

Subclass type of the characteristic.Possible values:

-   `BooleanCharacteristic`
-   `StringCharacteristic`

Data type: String

</td></tr><tr><td>

partyCharacteristic.name

</td><td>

Name of the characteristic. For example, `notes`, `dateFormat`, `timeZone`, `vip`, or `notification`.Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic.Data type: Depends on **valueType**. For example, String or Boolean.

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value. For example, `string` or `boolean`.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Party type and role of the individual record. In POST requests, determines whether the request creates a Consumer or Contact record.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "role": "String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

Type of party.Possible values:

-   `Consumer`
-   `Contact`

Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Role of the individual.Possible values:

-   `Consumer`: Consumer record.
-   `Contact`: Contact record.

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties related to the individual.Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related party.Data type: Object

```
"partyOrPartyRole": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party.Possible values:

-   `Individual`: Related party is a user.
-   `Organization`: Related party is a company or department.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related party record.Table: Depends on the related party role:

-   Company: Company \[core\_company\]
-   Department: Department \[cmn\_department\]
-   User: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related party plays for the individual.Possible values:

-   `Company`: Company associated with the individual.
-   `Department`: Department associated with the individual.
-   `User`: User associated with the consumer.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the individual record.Possible values:

-   `active`: Record is active.
-   `inactive`: Record is inactive.

Data type: String

</td></tr><tr><td>

title

</td><td>

Prefix or title of the individual. For example, `Mr`, `Ms`, or `Dr`.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

<table id="partymgmt-PATCH-id-response-table"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Response object\}

</td><td>

Response object structure for the v1 request.```
{
  "id": "String",
  "href": "String",
  "@type": "String",
  "name": "String",
  "givenName": "String",
  "middleName": "String",
  "familyName": "String",
  "gender": "String",
  "nationality": "String",
  "title": "String",
  "status": "String",
  "partyOrPartyRole": {Object},
  "contactMedium": [Array],
  "partyCharacteristic": [Array],
  "relatedParty": [Array]
}
```

</td></tr><tr><td>

@type

</td><td>

Type of the individual record.Possible values:

-   `Consumer`: Consumer record.
-   `Contact`: Contact record.

Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of means for contacting the individual.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "country": "String",
  "emailAddress": "String",
  "locationId": "String",
  "mediumType": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": "Boolean",
  "stateOrProvince": "String",
  "street1": "String",
  "street2": "String"
 }
]
```

</td></tr><tr><td>

contactMedium.@type

</td><td>

Schema or subclass type of the contact medium.Possible values:

-   `BusinessPhoneContactMedium`: Business phone number.
-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `PhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location record linked to the address.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact channel.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Possible values:

-   `true`: Preferred contact medium.
-   `false`: Not the preferred contact medium.

Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

State or province of the address. For example, `New Jersey`.Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

First line of the street address.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Second line of the street address, such as a suite or floor.Data type: String

</td></tr><tr><td>

familyName

</td><td>

Last name of the individual.Data type: String

</td></tr><tr><td>

gender

</td><td>

Gender of the individual.Data type: String

</td></tr><tr><td>

givenName

</td><td>

First name of the individual.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the Consumer or Contact record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the Consumer or Contact record.Table: Consumer \[csm\_consumer\] or Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

name

</td><td>

User name of the individual.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics associated with the individual.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristic.@type

</td><td>

Subclass type of the characteristic.Possible values:

-   `BooleanCharacteristic`
-   `StringCharacteristic`

Data type: String

</td></tr><tr><td>

partyCharacteristic.name

</td><td>

Name of the characteristic. For example, `notes`, `dateFormat`, `timeZone`, `vip`, or `notification`.Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic.Data type: Depends on **valueType**. For example, String or Boolean.

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value. For example, `string` or `boolean`.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Party type and role of the individual record. In POST requests, determines whether the request creates a Consumer or Contact record.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "role": "String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

Type of party.Possible values:

-   `Consumer`
-   `Contact`

Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Role of the individual.Possible values:

-   `Consumer`: Consumer record.
-   `Contact`: Contact record.

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties related to the individual.Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related party.Data type: Object

```
"partyOrPartyRole": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party.Possible values:

-   `Individual`: Related party is a user.
-   `Organization`: Related party is a company or department.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related party record.Table: Depends on the related party role:

-   Company: Company \[core\_company\]
-   Department: Department \[cmn\_department\]
-   User: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related party plays for the individual.Possible values:

-   `Company`: Company associated with the individual.
-   `Department`: Department associated with the individual.
-   `User`: User associated with the consumer.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the individual record.Possible values:

-   `active`: Record is active.
-   `inactive`: Record is inactive.

Data type: String

</td></tr><tr><td>

title

</td><td>

Prefix or title of the individual. For example, `Mr`, `Ms`, or `Dr`.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example updates the Consumer record with sys\_id a1b2c3d4e5f6478990abcdef12345678 without replacing the entire resource.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v1/party/individual/a1b2c3d4e5f6478990abcdef12345678" \
  --request PATCH \
  --header "Accept: application/json" \
  --header "Content-Type: application/json" \
  --user 'user:password' \
  --data '{
  "@type": "Consumer",
  "name": "John.Doe",
  "givenName": "John",
  "middleName": "A.",
  "familyName": "Doe",
  "gender": "male",
  "nationality": "American",
  "title": "Mr",
  "status": "active",
  "partyOrPartyRole": {
    "@type": "Consumer",
    "role": "Consumer"
  },
  "contactMedium": [
    {
      "preferred": true,
      "mediumType": "email",
      "emailAddress": "john.doe@example.com",
      "@type": "EmailContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "businessPhone",
      "phoneNumber": "+1-202-555-0188",
      "@type": "BusinessPhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "homePhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "HomePhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "postalAddress",
      "@type": "GeographicAddressContactMedium",
      "city": "Morristown",
      "country": "USA",
      "postCode": "07960",
      "stateOrProvince": "New Jersey",
      "street1": "240 Headquarters Plaza",
      "street2": "East Tower - 10th Floor"
    }
  ],
  "partyCharacteristic": [
    {
      "name": "notification",
      "value": "enable",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "dateFormat",
      "value": "MM/DD/YYYY",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "timeFormat",
      "value": "12-hour",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "timeZone",
      "value": "EST",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "vip",
      "value": true,
      "valueType": "boolean",
      "@type": "BooleanCharacteristic"
    },
    {
      "name": "webServiceAccessOnly",
      "value": false,
      "valueType": "boolean",
      "@type": "BooleanCharacteristic"
    },
    {
      "name": "source",
      "value": "Third-party system",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "eduStatus",
      "value": "Graduated",
      "valueType": "string",
      "@type": "StringCharacteristic"
    }
  ],
  "relatedParty": [
    {
      "role": "Company",
      "partyOrPartyRole": {
        "id": "86c1f3193790200044e0bfc8bcbe5d95",
        "name": "Acme Corporation",
        "@type": "Organization"
      }
    },
    {
      "role": "Department",
      "partyOrPartyRole": {
        "id": "c3fdd27a7b9822105e0d5494548cb6b0",
        "name": "Sales",
        "@type": "Organization"
      }
    }
  ]
}'
```

Response body.

```
{
  "id": "a1b2c3d4e5f6478990abcdef12345678",
  "href": "api/sn_tmf_api/party/individual/a1b2c3d4e5f6478990abcdef12345678",
  "@type": "Consumer",
  "name": "John.Doe",
  "givenName": "John",
  "middleName": "A.",
  "familyName": "Doe",
  "gender": "male",
  "nationality": "American",
  "title": "Mr",
  "status": "active",
  "partyOrPartyRole": {
    "@type": "Consumer",
    "role": "Consumer"
  },
  "contactMedium": [
    {
      "preferred": true,
      "mediumType": "email",
      "emailAddress": "john.doe@example.com",
      "@type": "EmailContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "businessPhone",
      "phoneNumber": "+1-202-555-0188",
      "@type": "BusinessPhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "homePhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "HomePhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "postalAddress",
      "@type": "GeographicAddressContactMedium",
      "locationId": "25ab9e240a0a0bb3009eb9ef8dd0a2c0",
      "city": "Morristown",
      "country": "USA",
      "postCode": "07960",
      "stateOrProvince": "New Jersey",
      "street1": "240 Headquarters Plaza",
      "street2": "East Tower - 10th Floor"
    }
  ],
  "partyCharacteristic": [
    {
      "name": "notification",
      "value": "enable",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "dateFormat",
      "value": "MM/DD/YYYY",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "timeFormat",
      "value": "12-hour",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "timeZone",
      "value": "EST",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "vip",
      "value": true,
      "valueType": "boolean",
      "@type": "BooleanCharacteristic"
    },
    {
      "name": "webServiceAccessOnly",
      "value": false,
      "valueType": "boolean",
      "@type": "BooleanCharacteristic"
    },
    {
      "name": "source",
      "value": "Third-party system",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "eduStatus",
      "value": "Graduated",
      "valueType": "string",
      "@type": "StringCharacteristic"
    }
  ],
  "relatedParty": [
    {
      "role": "Company",
      "partyOrPartyRole": {
        "id": "86c1f3193790200044e0bfc8bcbe5d95",
        "name": "Acme Corporation",
        "@type": "Organization"
      }
    },
    {
      "role": "Department",
      "partyOrPartyRole": {
        "id": "c3fdd27a7b9822105e0d5494548cb6b0",
        "name": "Sales",
        "@type": "Organization"
      }
    }
  ]
}
```

## Party Management v1 - PATCH /api/sn\_tmf\_api/v1/party/organization/\{id\}

Updates an existing individual party record in the Account \[customer\_account\] tables without replacing the entire resource.

### URL format

Versioned URL: `/api/sn_tmf_api/v1/party/organization/{id}`

Default URL: `/api/sn_tmf_api/v1/party/organization/{id}`

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

id

</td><td>

Sys\_id of the account record to update.Table: Account \[customer\_account\]

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="partymgmt-PATCH-org-id-request-table" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Request object\}

</td><td>

Request object structure for the v1 request. Include only the fields to update.```
{
  "@type": "String",
  "name": "String",
  "legalName": "String",
  "tradingName": "String",
  "status": "String",
  "partyOrPartyRole": {Object},
  "contactMedium": [Array],
  "externalReference": [Array],
  "partyCharacteristic": [Array],
  "relatedParty": [Array],
  "organizationChildRelationship": [Array],
  "organizationParentRelationship": {Object}
}
```

</td></tr><tr><td>

@type

</td><td>

Type of the organization record. Value is always `Account`.Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of means for contacting the organization.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "country": "String",
  "emailAddress": "String",
  "mediumType": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": "Boolean",
  "stateOrProvince": "String",
  "street1": "String",
  "street2": "String",
  "validFor": {Object}
 }
]
```

</td></tr><tr><td>

contactMedium.@type

</td><td>

Schema or subclass type of the contact medium.Possible values:

-   `BusinessPhoneContactMedium`: Business phone number.
-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `PhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address.Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact channel.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Possible values:

-   `true`: Preferred contact medium.
-   `false`: Not the preferred contact medium.

Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

State or province of the address. For example, `New Jersey`.Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

First line of the street address.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Second line of the street address, such as a suite or floor.Data type: String

</td></tr><tr><td>

contactMedium.validFor

</td><td>

Period during which the address is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

contactMedium.validFor.startDateTime

</td><td>

Date and time from which the address is valid, in ISO 8601 format. For example, `2017-03-15T07:49:25.246Z`.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the organization in external systems.Data type: Array of Objects

```
"externalReference": [
 {
  "externalIdentifierType": "String",
  "id": "String"
 }
]
```

</td></tr><tr><td>

externalReference.externalIdentifierType

</td><td>

Type of external system or identifier. For example, `linkedin` or `Instagram`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the organization in the external system.Data type: String

</td></tr><tr><td>

legalName

</td><td>

Legal name of the organization.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the organization.Data type: String

</td></tr><tr><td>

organizationChildRelationship

</td><td>

List of child organization relationships, such as partner, subsidiary, or branch organizations.Data type: Array of Objects

```
"organizationChildRelationship": [
 {
  "relationshipType": "String",
  "organization": {Object}
 }
]
```

</td></tr><tr><td>

organizationChildRelationship.organization

</td><td>

Details about the child organization.Data type: Object

```
"organization": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

organizationChildRelationship.organization.@type

</td><td>

Type of the organization object. Value is always `Organization`.Data type: String

</td></tr><tr><td>

organizationChildRelationship.organization.id

</td><td>

Sys\_id of the child organization record.Table: Account \[customer\_account\] or Company \[core\_company\]

Data type: String

</td></tr><tr><td>

organizationChildRelationship.organization.name

</td><td>

Display name of the child organization.Data type: String

</td></tr><tr><td>

organizationChildRelationship.relationshipType

</td><td>

Type of relationship between this organization and the child organization. For example, `Partner Account`.Data type: String

</td></tr><tr><td>

organizationParentRelationship

</td><td>

Relationship to the parent organization.Data type: Object

```
"organizationParentRelationship": {
  "relationshipType": "String",
  "organization": {Object}
}
```

</td></tr><tr><td>

organizationParentRelationship.organization

</td><td>

Details about the parent organization.Data type: Object

```
"organization": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

organizationParentRelationship.organization.@type

</td><td>

Type of the organization object. Value is always `Organization`.Data type: String

</td></tr><tr><td>

organizationParentRelationship.organization.id

</td><td>

Sys\_id of the parent organization record.Table: Account \[customer\_account\] or Company \[core\_company\]

Data type: String

</td></tr><tr><td>

organizationParentRelationship.organization.name

</td><td>

Display name of the parent organization.Data type: String

</td></tr><tr><td>

organizationParentRelationship.relationshipType

</td><td>

Type of relationship between this organization and its parent.Possible values:

-   `Account`
-   `Company`
-   `HoldingCompany`
-   `ParentAccount`

Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics associated with the organization.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristic.@type

</td><td>

Subclass type of the characteristic.Possible values:

-   `BooleanCharacteristic`
-   `IntegerCharacteristic`
-   `StringArrayCharacteristic`
-   `StringCharacteristic`

Data type: String

</td></tr><tr><td>

partyCharacteristic.name

</td><td>

Name of the characteristic.Possible values:

-   `accountCode`
-   `identificationNumber`
-   `industry`
-   `manufacturer`
-   `marketCap`
-   `notes`
-   `numEmployees`
-   `profits`
-   `publiclyTraded`
-   `rankTier`
-   `registrationCode`
-   `revenuePerYear`
-   `stockPrice`
-   `stockSymbol`
-   `taxId`
-   `vendor`
-   `vendorType`
-   `website`

**Note:** For the `industry` and `rankTier` choice fields, **partyCharacteristic.value** accepts the display value. Invalid values trigger a warning message in the response.

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic, as a string regardless of **valueType**. For example, `"false"` or `"10"`.Data type: String

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `choice`
-   `integer`
-   `list`
-   `string`

Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Party type, role, and account classification of the organization record.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "role": "String",
  "name": "String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

Type of party. Value is always `Account`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.name

</td><td>

Account classification. Multiple classifications are joined with underscores. For example, `customer` or `customer_partner`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Role of the party. Value is always `Account`.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts related to the organization.Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related contact.Data type: Object

```
"partyOrPartyRole": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Value is always `Individual`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related contact record.Table: Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the related contact.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related contact plays for the organization.Possible values:

-   `other`: Other contact for the organization.
-   `primaryContact`: Primary contact for the organization.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the organization record.Possible values:

-   `active`: Organization is active.
-   `inactive`: Organization is inactive.

Data type: String

</td></tr><tr><td>

tradingName

</td><td>

Name that the organization trades under.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

<table id="partymgmt-PATCH-org-id-response-table"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Response object\}

</td><td>

Response object structure for the v1 request.```
{
  "id": "String",
  "href": "String",
  "@type": "String",
  "name": "String",
  "legalName": "String",
  "tradingName": "String",
  "status": "String",
  "partyOrPartyRole": {Object},
  "contactMedium": [Array],
  "externalReference": [Array],
  "partyCharacteristic": [Array],
  "relatedParty": [Array],
  "organizationChildRelationship": [Array],
  "organizationParentRelationship": {Object},
  "createdDate": "String",
  "lastModifiedDate": "String"
}
```

</td></tr><tr><td>

@type

</td><td>

Type of the organization record. Value is always `Account`.Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of means for contacting the organization.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "country": "String",
  "emailAddress": "String",
  "locationId": "String",
  "mediumType": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": "Boolean",
  "stateOrProvince": "String",
  "street1": "String",
  "street2": "String",
  "validFor": {Object}
 }
]
```

</td></tr><tr><td>

contactMedium.@type

</td><td>

Schema or subclass type of the contact medium.Possible values:

-   `BusinessPhoneContactMedium`: Business phone number.
-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `PhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location record linked to the address.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact channel.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Possible values:

-   `true`: Preferred contact medium.
-   `false`: Not the preferred contact medium.

Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

State or province of the address. For example, `New Jersey`.Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

First line of the street address.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Second line of the street address, such as a suite or floor.Data type: String

</td></tr><tr><td>

contactMedium.validFor

</td><td>

Period during which the address is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

contactMedium.validFor.startDateTime

</td><td>

Date and time from which the address is valid, in ISO 8601 format. For example, `2017-03-15T07:49:25.246Z`.Data type: String

</td></tr><tr><td>

createdDate

</td><td>

Date and time when the organization record was created, in ISO 8601 format. For example, `2025-06-25T14:32:18.000Z`.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the organization in external systems.Data type: Array of Objects

```
"externalReference": [
 {
  "externalIdentifierType": "String",
  "id": "String"
 }
]
```

</td></tr><tr><td>

externalReference.externalIdentifierType

</td><td>

Type of external system or identifier. For example, `linkedin` or `Instagram`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the organization in the external system.Data type: String

</td></tr><tr><td>

href

</td><td>

Link to the Account record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the Account record.Table: Account \[customer\_account\]

Data type: String

</td></tr><tr><td>

lastModifiedDate

</td><td>

Date and time when the organization record was last modified, in ISO 8601 format. For example, `2026-11-05T10:15:42.000Z`.Data type: String

</td></tr><tr><td>

legalName

</td><td>

Legal name of the organization.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the organization.Data type: String

</td></tr><tr><td>

organizationChildRelationship

</td><td>

List of child organization relationships, such as partner, subsidiary, or branch organizations.Data type: Array of Objects

```
"organizationChildRelationship": [
 {
  "relationshipType": "String",
  "organization": {Object}
 }
]
```

</td></tr><tr><td>

organizationChildRelationship.organization

</td><td>

Details about the child organization.Data type: Object

```
"organization": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

organizationChildRelationship.organization.@type

</td><td>

Type of the organization object. Value is always `Organization`.Data type: String

</td></tr><tr><td>

organizationChildRelationship.organization.id

</td><td>

Sys\_id of the child organization record.Table: Account \[customer\_account\] or Company \[core\_company\]

Data type: String

</td></tr><tr><td>

organizationChildRelationship.organization.name

</td><td>

Display name of the child organization.Data type: String

</td></tr><tr><td>

organizationChildRelationship.relationshipType

</td><td>

Type of relationship between this organization and the child organization. For example, `Partner Account`.Data type: String

</td></tr><tr><td>

organizationParentRelationship

</td><td>

Relationship to the parent organization.Data type: Object

```
"organizationParentRelationship": {
  "relationshipType": "String",
  "organization": {Object}
}
```

</td></tr><tr><td>

organizationParentRelationship.organization

</td><td>

Details about the parent organization.Data type: Object

```
"organization": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

organizationParentRelationship.organization.@type

</td><td>

Type of the organization object. Value is always `Organization`.Data type: String

</td></tr><tr><td>

organizationParentRelationship.organization.id

</td><td>

Sys\_id of the parent organization record.Table: Account \[customer\_account\] or Company \[core\_company\]

Data type: String

</td></tr><tr><td>

organizationParentRelationship.organization.name

</td><td>

Display name of the parent organization.Data type: String

</td></tr><tr><td>

organizationParentRelationship.relationshipType

</td><td>

Type of relationship between this organization and its parent.Possible values:

-   `Account`
-   `Company`
-   `HoldingCompany`
-   `ParentAccount`

Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics associated with the organization.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristic.@type

</td><td>

Subclass type of the characteristic.Possible values:

-   `BooleanCharacteristic`
-   `IntegerCharacteristic`
-   `StringArrayCharacteristic`
-   `StringCharacteristic`

Data type: String

</td></tr><tr><td>

partyCharacteristic.name

</td><td>

Name of the characteristic.Possible values:

-   `accountCode`
-   `identificationNumber`
-   `industry`
-   `manufacturer`
-   `marketCap`
-   `notes`
-   `numEmployees`
-   `profits`
-   `publiclyTraded`
-   `rankTier`
-   `registrationCode`
-   `revenuePerYear`
-   `stockPrice`
-   `stockSymbol`
-   `taxId`
-   `vendor`
-   `vendorType`
-   `website`

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic, as a string regardless of **valueType**. For example, `"false"` or `"10"`.Data type: String

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `choice`
-   `integer`
-   `list`
-   `string`

Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Party type, role, and account classification of the organization record.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "role": "String",
  "name": "String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

Type of party. Value is always `Account`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.name

</td><td>

Account classification. Multiple classifications are joined with underscores. For example, `customer` or `customer_partner`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Role of the party. Value is always `Account`.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts related to the organization.Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related contact.Data type: Object

```
"partyOrPartyRole": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Value is always `Individual`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related contact record.Table: Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the related contact.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related contact plays for the organization.Possible values:

-   `other`: Other contact for the organization.
-   `primaryContact`: Primary contact for the organization.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the organization record.Possible values:

-   `active`: Organization is active.
-   `inactive`: Organization is inactive.

Data type: String

</td></tr><tr><td>

tradingName

</td><td>

Name that the organization trades under.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example updates the Account record with sys\_id a1b2c3d4e5f6478990abcdef12345678.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v1/party/organization/a1b2c3d4e5f6478990abcdef12345678" \
  --request PATCH \
  --header "Accept: application/json" \
  --header "Content-Type: application/json" \
  --user 'user:password' \
  --data '{
  "@type": "Account",
  "name": "SERVICENOW 144",
  "legalName": "Acme Corp Ltd.",
  "tradingName": "Acme Inc.",
  "status": "active",
  "partyOrPartyRole": {
    "@type": "Account",
    "role": "Account",
    "name": "customer"
  },
  "contactMedium": [
    {
      "preferred": true,
      "mediumType": "email",
      "emailAddress": "athammhd@email.com",
      "@type": "EmailContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "mobilePhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "PhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "businessPhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "BusinessPhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "homePhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "HomePhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "postalAddress",
      "validFor": {
        "startDateTime": "2017-03-15T07:49:25.246Z"
      },
      "@type": "GeographicAddressContactMedium",
      "city": "chennai",
      "country": "INDIA",
      "postCode": "608001",
      "stateOrProvince": "tamil nadu",
      "street1": "samcon street",
      "street2": "adyar,chennai"
    }
  ],
  "externalReference": [
    {
      "externalIdentifierType": "Instagram",
      "id": "Instagram"
    }
  ],
  "partyCharacteristic": [
    {
      "name": "notes",
      "value": "Testing for update the notes",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "registrationCode",
      "value": "006",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "industry",
      "value": "Manufacturing",
      "valueType": "choice",
      "@type": "StringCharacteristics"
    },
    {
      "name": "taxId",
      "value": "CTNUM1000123",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "numEmployees",
      "value": "10",
      "valueType": "integer",
      "@type": "StringCharacteristics"
    },
    {
      "name": "rankTier",
      "value": "Valued Partner",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "publiclyTraded",
      "value": "false",
      "valueType": "boolean",
      "@type": "StringCharacteristics"
    },
    {
      "name": "vendor",
      "value": "false",
      "valueType": "boolean",
      "@type": "StringCharacteristics"
    },
    {
      "name": "manufacturer",
      "value": "false",
      "valueType": "boolean",
      "@type": "StringCharacteristics"
    }
  ],
  "relatedParty": [
    {
      "role": "primaryContact",
      "partyOrPartyRole": {
        "id": "eaf68911c35420105252716b7d40ddde",
        "name": "John Doe",
        "@type": "Individual"
      }
    },
    {
      "role": "other",
      "partyOrPartyRole": {
        "id": "776a22ea11f43110f877366201dea6b7",
        "name": "Mary Star",
        "@type": "Individual"
      }
    }
  ],
  "organizationChildRelationship": [
    {
      "relationshipType": "Partner Account",
      "organization": {
        "id": "051f62b0d7300200e5982cf65e610333",
        "name": "Spark Technologies",
        "@type": "Organization"
      }
    }
  ],
  "organizationParentRelationship": {
    "relationshipType": "Partner Account",
    "organization": {
      "id": "1b1b93da43c63110341605ed0bb8f2f4",
      "name": "Funco Intl.",
      "@type": "Organization"
    }
  }
}'
```

Response body.

```
{
  "id": "a1b2c3d4e5f6478990abcdef12345678",
  "href": "http://instance.service-now.com/api/sn_tmf_api/v1/party/organization/a1b2c3d4e5f6478990abcdef12345678",
  "@type": "Account",
  "name": "SERVICENOW 144",
  "legalName": "Acme Corp Ltd.",
  "tradingName": "Acme Inc.",
  "status": "active",
  "partyOrPartyRole": {
    "@type": "Account",
    "role": "Account",
    "name": "customer"
  },
  "contactMedium": [
    {
      "preferred": true,
      "mediumType": "email",
      "emailAddress": "athammhd@email.com",
      "@type": "EmailContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "mobilePhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "PhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "businessPhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "BusinessPhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "homePhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "HomePhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "postalAddress",
      "validFor": {
        "startDateTime": "2017-03-15T07:49:25.246Z"
      },
      "@type": "GeographicAddressContactMedium",
      "locationId": "03e588a17be062105e0d5494548cb68c",
      "city": "chennai",
      "country": "INDIA",
      "postCode": "608001",
      "stateOrProvince": "tamil nadu",
      "street1": "samcon street",
      "street2": "adyar,chennai"
    }
  ],
  "externalReference": [
    {
      "externalIdentifierType": "Instagram",
      "id": "Instagram"
    }
  ],
  "partyCharacteristic": [
    {
      "name": "notes",
      "value": "Testing for update the notes",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "registrationCode",
      "value": "006",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "industry",
      "value": "Manufacturing",
      "valueType": "choice",
      "@type": "StringCharacteristics"
    },
    {
      "name": "taxId",
      "value": "CTNUM1000123",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "numEmployees",
      "value": "10",
      "valueType": "integer",
      "@type": "StringCharacteristics"
    },
    {
      "name": "rankTier",
      "value": "Valued Partner",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "publiclyTraded",
      "value": "false",
      "valueType": "boolean",
      "@type": "StringCharacteristics"
    },
    {
      "name": "vendor",
      "value": "false",
      "valueType": "boolean",
      "@type": "StringCharacteristics"
    },
    {
      "name": "manufacturer",
      "value": "false",
      "valueType": "boolean",
      "@type": "StringCharacteristics"
    }
  ],
  "relatedParty": [
    {
      "role": "primaryContact",
      "partyOrPartyRole": {
        "id": "eaf68911c35420105252716b7d40ddde",
        "name": "John Doe",
        "@type": "Individual"
      }
    },
    {
      "role": "other",
      "partyOrPartyRole": {
        "id": "776a22ea11f43110f877366201dea6b7",
        "name": "Mary Star",
        "@type": "Individual"
      }
    }
  ],
  "organizationChildRelationship": [
    {
      "relationshipType": "Partner Account",
      "organization": {
        "id": "051f62b0d7300200e5982cf65e610333",
        "name": "Spark Technologies",
        "@type": "Organization"
      }
    }
  ],
  "organizationParentRelationship": {
    "relationshipType": "Partner Account",
    "organization": {
      "id": "1b1b93da43c63110341605ed0bb8f2f4",
      "name": "Funco Intl.",
      "@type": "Organization"
    }
  },
  "createdDate": "2025-06-25T14:32:18.000Z",
  "lastModifiedDate": "2026-11-05T10:15:42.000Z"
}
```

## Party Management v1 - POST /api/sn\_tmf\_api/v1/party/individual

Creates a new individual party management record in the Consumer \[csm\_consumer\] or Contact \[customer\_contact\] tables.

### URL format

Versioned URL: `/api/sn_tmf_api/v1/party/individual`

Default URL: `/api/sn_tmf_api/v1/party/individual`

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

<table id="partymgmt-POST-individual-request-table" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Request object\}

</td><td>

Request object structure for the v1 request.```
{
  "@type": "String",
  "name": "String",
  "givenName": "String",
  "middleName": "String",
  "familyName": "String",
  "gender": "String",
  "nationality": "String",
  "title": "String",
  "status": "String",
  "partyOrPartyRole": {Object},
  "contactMedium": [Array],
  "externalReference": [Array],
  "partyCharacteristic": [Array],
  "relatedParty": [Array]
}
```

</td></tr><tr><td>

@type

</td><td>

Type of the individual record.Possible values:

-   `Consumer`: Consumer record.
-   `Contact`: Contact record.

Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of means for contacting the individual.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "country": "String",
  "emailAddress": "String",
  "mediumType": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": "Boolean",
  "stateOrProvince": "String",
  "street1": "String",
  "street2": "String"
 }
]
```

</td></tr><tr><td>

contactMedium.@type

</td><td>

Schema or subclass type of the contact medium.Possible values:

-   `BusinessPhoneContactMedium`: Business phone number.
-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `PhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address.Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact channel.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Possible values:

-   `true`: Preferred contact medium.
-   `false`: Not the preferred contact medium.

Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

State or province of the address. For example, `New Jersey`.Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

First line of the street address.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Second line of the street address, such as a suite or floor.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the individual in external systems.Data type: Array of Objects

```
"externalReference": [
 {
  "externalIdentifierType": "String",
  "id": "String"
 }
]
```

</td></tr><tr><td>

externalReference.externalIdentifierType

</td><td>

Type of external system or identifier. For example, `linkedin` or `Instagram`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the individual in the external system, such as a profile URL.Data type: String

</td></tr><tr><td>

familyName

</td><td>

Last name of the individual.Data type: String

</td></tr><tr><td>

gender

</td><td>

Gender of the individual.Data type: String

</td></tr><tr><td>

givenName

</td><td>

First name of the individual.Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

name

</td><td>

User name of the individual.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics associated with the individual.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristic.@type

</td><td>

Subclass type of the characteristic.Possible values:

-   `BooleanCharacteristic`
-   `StringCharacteristic`

Data type: String

</td></tr><tr><td>

partyCharacteristic.name

</td><td>

Name of the characteristic. For example, `notes`, `dateFormat`, `timeZone`, `vip`, or `notification`.Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic.Data type: Depends on **valueType**. For example, String or Boolean.

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value. For example, `string` or `boolean`.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Party type and role of the individual record. In POST requests, determines whether the request creates a Consumer or Contact record.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "role": "String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

Type of party.Possible values:

-   `Consumer`
-   `Contact`

Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Role of the individual.Possible values:

-   `Consumer`: Consumer record.
-   `Contact`: Contact record.

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties related to the individual.Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related party.Data type: Object

```
"partyOrPartyRole": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party.Possible values:

-   `Individual`: Related party is a user.
-   `Organization`: Related party is a company or department.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related party record. If no matching record exists, the record is created without the related party and the response includes a warning.Table: Depends on the related party role:

-   Company: Company \[core\_company\]
-   Department: Department \[cmn\_department\]
-   User: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related party plays for the individual.Possible values:

-   `Company`: Company associated with the individual.
-   `Department`: Department associated with the individual.
-   `User`: User associated with the consumer.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the individual record.Possible values:

-   `active`: Record is active.
-   `inactive`: Record is inactive.

Data type: String

</td></tr><tr><td>

title

</td><td>

Prefix or title of the individual. For example, `Mr`, `Ms`, or `Dr`.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

<table id="partymgmt-POST-individual-response-table"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Response object\}

</td><td>

Response object structure for the v1 request.```
{
  "id": "String",
  "href": "String",
  "@type": "String",
  "name": "String",
  "givenName": "String",
  "middleName": "String",
  "familyName": "String",
  "gender": "String",
  "nationality": "String",
  "title": "String",
  "status": "String",
  "partyOrPartyRole": {Object},
  "contactMedium": [Array],
  "externalReference": [Array],
  "partyCharacteristic": [Array],
  "relatedParty": [Array],
  "warning": [Array]
}
```

</td></tr><tr><td>

@type

</td><td>

Type of the individual record.Possible values:

-   `Consumer`: Consumer record.
-   `Contact`: Contact record.

Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of means for contacting the individual.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "country": "String",
  "emailAddress": "String",
  "locationId": "String",
  "mediumType": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": "Boolean",
  "stateOrProvince": "String",
  "street1": "String",
  "street2": "String"
 }
]
```

</td></tr><tr><td>

contactMedium.@type

</td><td>

Schema or subclass type of the contact medium.Possible values:

-   `BusinessPhoneContactMedium`: Business phone number.
-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `PhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location record linked to the address.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact channel.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Possible values:

-   `true`: Preferred contact medium.
-   `false`: Not the preferred contact medium.

Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

State or province of the address. For example, `New Jersey`.Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

First line of the street address.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Second line of the street address, such as a suite or floor.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the individual in external systems.Data type: Array of Objects

```
"externalReference": [
 {
  "externalIdentifierType": "String",
  "id": "String"
 }
]
```

</td></tr><tr><td>

externalReference.externalIdentifierType

</td><td>

Type of external system or identifier. For example, `linkedin` or `Instagram`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the individual in the external system, such as a profile URL.Data type: String

</td></tr><tr><td>

familyName

</td><td>

Last name of the individual.Data type: String

</td></tr><tr><td>

gender

</td><td>

Gender of the individual.Data type: String

</td></tr><tr><td>

givenName

</td><td>

First name of the individual.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the Consumer or Contact record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the Consumer or Contact record.Table: Consumer \[csm\_consumer\] or Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

name

</td><td>

User name of the individual.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics associated with the individual.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristic.@type

</td><td>

Subclass type of the characteristic.Possible values:

-   `BooleanCharacteristic`
-   `StringCharacteristic`

Data type: String

</td></tr><tr><td>

partyCharacteristic.name

</td><td>

Name of the characteristic. For example, `notes`, `dateFormat`, `timeZone`, `vip`, or `notification`.Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic.Data type: Depends on **valueType**. For example, String or Boolean.

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value. For example, `string` or `boolean`.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Party type and role of the individual record. In POST requests, determines whether the request creates a Consumer or Contact record.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "role": "String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

Type of party.Possible values:

-   `Consumer`
-   `Contact`

Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Role of the individual.Possible values:

-   `Consumer`: Consumer record.
-   `Contact`: Contact record.

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties related to the individual.Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related party.Data type: Object

```
"partyOrPartyRole": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party.Possible values:

-   `Individual`: Related party is a user.
-   `Organization`: Related party is a company or department.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related party record.Table: Depends on the related party role:

-   Company: Company \[core\_company\]
-   Department: Department \[cmn\_department\]
-   User: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related party plays for the individual.Possible values:

-   `Company`: Company associated with the individual.
-   `Department`: Department associated with the individual.
-   `User`: User associated with the consumer.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the individual record.Possible values:

-   `active`: Record is active.
-   `inactive`: Record is inactive.

Data type: String

</td></tr><tr><td>

title

</td><td>

Prefix or title of the individual. For example, `Mr`, `Ms`, or `Dr`.Data type: String

</td></tr><tr><td>

warning

</td><td>

List of warning messages about parts of the request that couldn't be processed. The record is still created, but without the invalid values. Returned only when a warning occurs.Example: `relatedParty[0] is incorrect. User does not exist`

Data type: Array of Strings

</td></tr></tbody>
</table>### cURL request

The following example creates a Consumer record. The related user in the request doesn't exist, so the response includes a warning.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v1/party/individual" \
  --request POST \
  --header "Accept: application/json" \
  --header "Content-Type: application/json" \
  --user 'user:password' \
  --data '{
  "@type": "Consumer",
  "name": "Jane Smith",
  "givenName": "Jane",
  "middleName": "B.",
  "familyName": "Smith",
  "gender": "female",
  "nationality": "American",
  "title": "Ms",
  "status": "active",
  "partyOrPartyRole": {
    "@type": "Consumer",
    "role": "Consumer"
  },
  "contactMedium": [
    {
      "preferred": true,
      "mediumType": "email",
      "emailAddress": "jane.smith@example.com",
      "@type": "EmailContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "mobilePhone",
      "phoneNumber": "+1-416-555-1234",
      "@type": "PhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "businessPhone",
      "phoneNumber": "+1-416-555-5678",
      "@type": "BusinessPhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "faxPhone",
      "phoneNumber": "987654321",
      "@type": "FaxPhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "homePhone",
      "phoneNumber": "+1-416-555-4321",
      "@type": "HomePhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "postalAddress",
      "@type": "GeographicAddressContactMedium",
      "city": "Toronto",
      "country": "Canada",
      "postCode": "M5H 2N2",
      "stateOrProvince": "Ontario",
      "street1": "123 Queen St W",
      "street2": "Suite 1500"
    }
  ],
  "externalReference": [
    {
      "externalIdentifierType": "linkedin",
      "id": "http://linkedin.com/in/janesmith"
    }
  ],
  "partyCharacteristic": [
    {
      "name": "notes",
      "value": "General consumer information.",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "userName",
      "value": "janesmith",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "vip",
      "value": false,
      "valueType": "boolean",
      "@type": "BooleanCharacteristic"
    },
    {
      "name": "source",
      "value": "CRM System",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "dateFormat",
      "value": "yyyy-mm-dd",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "timeFormat",
      "value": "HH:mm:ss (24 hour)",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "notification",
      "value": "Disabled",
      "valueType": "string",
      "@type": "StringCharacteristic"
    }
  ],
  "relatedParty": [
    {
      "role": "User",
      "partyOrPartyRole": {
        "id": "c456def03710200044e0bfc8bcbe5d99",
        "name": "Jane Smith",
        "@type": "Individual"
      }
    }
  ]
}'
```

Response body.

```
{
  "id": "83e588a17b6062105e0d5494548cb65d",
  "href": "api/sn_tmf_api/party/individual/83e588a17b6062105e0d5494548cb65d",
  "@type": "Consumer",
  "name": "Jane Smith",
  "givenName": "Jane",
  "middleName": "B.",
  "familyName": "Smith",
  "gender": "female",
  "nationality": "American",
  "title": "Ms",
  "status": "active",
  "partyOrPartyRole": {
    "@type": "Consumer",
    "role": "Consumer"
  },
  "contactMedium": [
    {
      "preferred": true,
      "mediumType": "email",
      "emailAddress": "jane.smith@example.com",
      "@type": "EmailContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "mobilePhone",
      "phoneNumber": "+1-416-555-1234",
      "@type": "PhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "businessPhone",
      "phoneNumber": "+1-416-555-5678",
      "@type": "BusinessPhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "faxPhone",
      "phoneNumber": "987654321",
      "@type": "FaxPhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "homePhone",
      "phoneNumber": "+1-416-555-4321",
      "@type": "HomePhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "postalAddress",
      "@type": "GeographicAddressContactMedium",
      "locationId": "03e588a17be062105e0d5494548cb68c",
      "city": "Toronto",
      "country": "Canada",
      "postCode": "M5H 2N2",
      "stateOrProvince": "Ontario",
      "street1": "123 Queen St W",
      "street2": "Suite 1500"
    }
  ],
  "externalReference": [
    {
      "externalIdentifierType": "linkedin",
      "id": "http://linkedin.com/in/janesmith"
    }
  ],
  "partyCharacteristic": [
    {
      "name": "notes",
      "value": "General consumer information.",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "userName",
      "value": "janesmith",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "vip",
      "value": false,
      "valueType": "boolean",
      "@type": "BooleanCharacteristic"
    },
    {
      "name": "source",
      "value": "CRM System",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "dateFormat",
      "value": "yyyy-mm-dd",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "timeFormat",
      "value": "HH:mm:ss (24 hour)",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "notification",
      "value": "Disabled",
      "valueType": "string",
      "@type": "StringCharacteristic"
    }
  ],
  "relatedParty": [
    {
      "role": "User",
      "partyOrPartyRole": {
        "id": "c456def03710200044e0bfc8bcbe5d99",
        "name": "Jane Smith",
        "@type": "Individual"
      }
    }
  ],
  "warning": [
    "relatedParty[0] is incorrect. User does not exist"
  ]
}
```

## Party Management v1 - POST /api/sn\_tmf\_api/v1/party/organization

Creates a new party organization record in the Account \[customer\_account\] tables. You can also create and associate Contact and Location records inline during organization creation, eliminating the need for separate POST operations.

### Automatic Location Creation with contactMedium

When you include address information in the **contactMedium** field \(with **@type** set to `GeographicAddressContactMedium`\), the system automatically handles location creation and association based on what you provide:

1.  If you supply a valid locationId, the system links the existing location record to the organization you are creating.
2.  If you provide address attributes \(street, city, country, postCode, stateOrProvince\) along with an invalid or non-existent locationId, the system automatically creates a new location record with those attributes and associates it to the organization.
3.  If you provide address attributes without specifying a locationId at all, the system creates a new location record and associates it to the organization.

**Note:** Location creation requires no mandatory fields. You can provide any combination of address attributes \(street1, street2, city, state, postCode, country\) based on your needs. If you omit all address attributes from the contactMedium section, no location record is created or linked to the organization.

### Inline Contact Creation with relatedParty

When you include contact attributes in the **relatedParty** field without providing a contact ID, the system automatically creates a new contact record and associates it to the organization you are creating. This eliminates the need for a separate POST request to create the contact first. You can include the following contact information directly in the **relatedParty.partyOrPartyRole** object.

Mandatory attributes for inline contact creation:

-   familyName \(or lastName\)
-   email

Optional attributes:

-   givenName
-   middleName
-   gender
-   title
-   nationality
-   contactMedium \(to include phone, address, or other contact details\)

Example: Creating a contact inline without a pre-existing ID.

```
{
  "relatedParty": [
    {
      "role": "primaryContact",
      "partyOrPartyRole": {
        "givenName": "John",
        "familyName": "Doe",
        "email": "john.doe@example.com",
        "@type": "Individual"
      }
    }
  ]
}
```

Legacy approach: Linking an existing contact by ID.

If you already have a contact record, you can link it by providing its sys\_id instead:

```
{
  "relatedParty": [
    {
      "role": "primaryContact",
      "partyOrPartyRole": {
        "id": "existing_contact_sys_id",
        "name": "John Doe",
        "@type": "Individual"
      }
    }
  ]
}
```

Both approaches are supported. The system automatically determines whether to create a new contact or link an existing one based on whether the partyOrPartyRole includes an id field.

### URL format

Versioned URL: `/api/sn_tmf_api/v1/party/organization`

Default URL: `/api/sn_tmf_api/v1/party/organization`

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

<table id="partymgmt-POST-org-request-table" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Request object\}

</td><td>

Request object structure for the v1 request.```
{
  "@type": "String",
  "name": "String",
  "legalName": "String",
  "tradingName": "String",
  "status": "String",
  "partyOrPartyRole": {Object},
  "contactMedium": [Array],
  "externalReference": [Array],
  "partyCharacteristic": [Array],
  "relatedParty": [Array],
  "organizationChildRelationship": [Array],
  "organizationParentRelationship": {Object}
}
```

</td></tr><tr><td>

@type

</td><td>

Type of the organization record. Value is always `Account`.Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of means for contacting the organization.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "country": "String",
  "emailAddress": "String",
  "locationId": "String",
  "mediumType": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": "Boolean",
  "stateOrProvince": "String",
  "street1": "String",
  "street2": "String",
  "validFor": {Object}
 }
]
```

</td></tr><tr><td>

contactMedium.@type

</td><td>

Schema or subclass type of the contact medium.Possible values:

-   `BusinessPhoneContactMedium`: Business phone number.
-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `PhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of an existing location record to link to the organization. If the ID is invalid or omitted and address attributes are provided, the system creates a new location record.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact channel.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Possible values:

-   `true`: Preferred contact medium.
-   `false`: Not the preferred contact medium.

Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

State or province of the address. For example, `New Jersey`.Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

First line of the street address.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Second line of the street address, such as a suite or floor.Data type: String

</td></tr><tr><td>

contactMedium.validFor

</td><td>

Period during which the address is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

contactMedium.validFor.startDateTime

</td><td>

Date and time from which the address is valid, in ISO 8601 format. For example, `2017-03-15T07:49:25.246Z`.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the organization in external systems.Data type: Array of Objects

```
"externalReference": [
 {
  "externalIdentifierType": "String",
  "id": "String"
 }
]
```

</td></tr><tr><td>

externalReference.externalIdentifierType

</td><td>

Type of external system or identifier. For example, `linkedin` or `Instagram`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the organization in the external system.Data type: String

</td></tr><tr><td>

legalName

</td><td>

Legal name of the organization.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the organization.Data type: String

</td></tr><tr><td>

organizationChildRelationship

</td><td>

List of child organization relationships, such as partner, subsidiary, or branch organizations.Data type: Array of Objects

```
"organizationChildRelationship": [
 {
  "relationshipType": "String",
  "organization": {Object}
 }
]
```

</td></tr><tr><td>

organizationChildRelationship.organization

</td><td>

Details about the child organization.Data type: Object

```
"organization": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

organizationChildRelationship.organization.@type

</td><td>

Type of the organization object. Value is always `Organization`.Data type: String

</td></tr><tr><td>

organizationChildRelationship.organization.id

</td><td>

Sys\_id of the child organization record.Table: Account \[customer\_account\] or Company \[core\_company\]

Data type: String

</td></tr><tr><td>

organizationChildRelationship.organization.name

</td><td>

Display name of the child organization.Data type: String

</td></tr><tr><td>

organizationChildRelationship.relationshipType

</td><td>

Type of relationship between this organization and the child organization. For example, `Partner Account`.Data type: String

</td></tr><tr><td>

organizationParentRelationship

</td><td>

Relationship to the parent organization.Data type: Object

```
"organizationParentRelationship": {
  "relationshipType": "String",
  "organization": {Object}
}
```

</td></tr><tr><td>

organizationParentRelationship.organization

</td><td>

Details about the parent organization.Data type: Object

```
"organization": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

organizationParentRelationship.organization.@type

</td><td>

Type of the organization object. Value is always `Organization`.Data type: String

</td></tr><tr><td>

organizationParentRelationship.organization.id

</td><td>

Sys\_id of the parent organization record.Table: Account \[customer\_account\] or Company \[core\_company\]

Data type: String

</td></tr><tr><td>

organizationParentRelationship.organization.name

</td><td>

Display name of the parent organization.Data type: String

</td></tr><tr><td>

organizationParentRelationship.relationshipType

</td><td>

Type of relationship between this organization and its parent.Possible values:

-   `Account`
-   `Company`
-   `HoldingCompany`
-   `ParentAccount`

Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics associated with the organization.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristic.@type

</td><td>

Subclass type of the characteristic.Possible values:

-   `BooleanCharacteristic`
-   `IntegerCharacteristic`
-   `StringArrayCharacteristic`
-   `StringCharacteristic`

Data type: String

</td></tr><tr><td>

partyCharacteristic.name

</td><td>

Name of the characteristic.Possible values:

-   `accountCode`
-   `identificationNumber`
-   `industry`
-   `manufacturer`
-   `marketCap`
-   `notes`
-   `numEmployees`
-   `profits`
-   `publiclyTraded`
-   `rankTier`
-   `registrationCode`
-   `revenuePerYear`
-   `stockPrice`
-   `stockSymbol`
-   `taxId`
-   `vendor`
-   `vendorType`
-   `website`

**Note:** For the `industry` and `rankTier` choice fields, **partyCharacteristic.value** accepts the display value. Invalid values trigger a warning message in the response.

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic, as a string regardless of **valueType**. For example, `"false"` or `"10"`.Data type: String

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `choice`
-   `integer`
-   `list`
-   `string`

Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Party type, role, and account classification of the organization record.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "role": "String",
  "name": "String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

Type of party. Value is always `Account`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.name

</td><td>

Account classification. Multiple classifications are joined with underscores. For example, `customer` or `customer_partner`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Role of the party. Value is always `Account`.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts to relate to the organization. To link an existing contact, provide its **id**. To create a new contact, omit **id** and provide the contact attributes. See Inline Contact Creation with relatedParty.Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related contact.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "contactMedium": [Array],
  "email": "String",
  "familyName": "String",
  "gender": "String",
  "givenName": "String",
  "id": "String",
  "middleName": "String",
  "name": "String",
  "nationality": "String",
  "title": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Value is always `Individual`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.contactMedium

</td><td>

Inline contact creation only. Phone, address, or other contact details for the new contact. Uses the same structure as **contactMedium**.Data type: Array of Objects

</td></tr><tr><td>

relatedParty.partyOrPartyRole.email

</td><td>

Inline contact creation only. Email address of the new contact. Required for inline contact creation.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.familyName

</td><td>

Inline contact creation only. Last name of the new contact. Required for inline contact creation.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.gender

</td><td>

Inline contact creation only. Gender of the new contact.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.givenName

</td><td>

Inline contact creation only. First name of the new contact.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of an existing contact to link to the organization. If you omit it, the system creates a new contact from the attributes in **relatedParty.partyOrPartyRole**.Table: Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.middleName

</td><td>

Inline contact creation only. Middle name of the new contact.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the existing contact. Used with **id**.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.nationality

</td><td>

Inline contact creation only. Nationality of the new contact.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.title

</td><td>

Inline contact creation only. Prefix or title of the new contact.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related contact plays for the organization.Possible values:

-   `Account`
-   `other`: Other contact for the organization.
-   `primaryContact`: Primary contact for the organization.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the organization record.Possible values:

-   `active`: Organization is active.
-   `inactive`: Organization is inactive.

Data type: String

</td></tr><tr><td>

tradingName

</td><td>

Name that the organization trades under.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Successful. The request was successfully processed.**Note:** Response may include a **warning** array if:

-   Invalid **relatedParty** IDs are provided \(related contact or party doesn't exist\).
-   Invalid **locationId** is provided in **contactMedium**. Example warning: `relatedParty[0] is incorrect. User does not exist`.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="partymgmt-POST-org-response-table"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Response object\}

</td><td>

Response object structure for the v1 request.```
{
  "id": "String",
  "href": "String",
  "@type": "String",
  "name": "String",
  "legalName": "String",
  "tradingName": "String",
  "status": "String",
  "partyOrPartyRole": {Object},
  "contactMedium": [Array],
  "externalReference": [Array],
  "partyCharacteristic": [Array],
  "relatedParty": [Array],
  "organizationChildRelationship": [Array],
  "organizationParentRelationship": {Object},
  "createdDate": "String",
  "lastModifiedDate": "String",
  "warning": [Array]
}
```

</td></tr><tr><td>

@type

</td><td>

Type of the organization record. Value is always `Account`.Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of means for contacting the organization.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "country": "String",
  "emailAddress": "String",
  "locationId": "String",
  "mediumType": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": "Boolean",
  "stateOrProvince": "String",
  "street1": "String",
  "street2": "String",
  "validFor": {Object}
 }
]
```

</td></tr><tr><td>

contactMedium.@type

</td><td>

Schema or subclass type of the contact medium.Possible values:

-   `BusinessPhoneContactMedium`: Business phone number.
-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `PhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location record linked to the address.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact channel.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Possible values:

-   `true`: Preferred contact medium.
-   `false`: Not the preferred contact medium.

Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

State or province of the address. For example, `New Jersey`.Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

First line of the street address.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Second line of the street address, such as a suite or floor.Data type: String

</td></tr><tr><td>

contactMedium.validFor

</td><td>

Period during which the address is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

contactMedium.validFor.startDateTime

</td><td>

Date and time from which the address is valid, in ISO 8601 format. For example, `2017-03-15T07:49:25.246Z`.Data type: String

</td></tr><tr><td>

createdDate

</td><td>

Date and time when the organization record was created, in ISO 8601 format. For example, `2025-06-25T14:32:18.000Z`.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the organization in external systems.Data type: Array of Objects

```
"externalReference": [
 {
  "externalIdentifierType": "String",
  "id": "String"
 }
]
```

</td></tr><tr><td>

externalReference.externalIdentifierType

</td><td>

Type of external system or identifier. For example, `linkedin` or `Instagram`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the organization in the external system.Data type: String

</td></tr><tr><td>

href

</td><td>

Link to the Account record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the Account record.Table: Account \[customer\_account\]

Data type: String

</td></tr><tr><td>

lastModifiedDate

</td><td>

Date and time when the organization record was last modified, in ISO 8601 format. For example, `2026-11-05T10:15:42.000Z`.Data type: String

</td></tr><tr><td>

legalName

</td><td>

Legal name of the organization.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the organization.Data type: String

</td></tr><tr><td>

organizationChildRelationship

</td><td>

List of child organization relationships, such as partner, subsidiary, or branch organizations.Data type: Array of Objects

```
"organizationChildRelationship": [
 {
  "relationshipType": "String",
  "organization": {Object}
 }
]
```

</td></tr><tr><td>

organizationChildRelationship.organization

</td><td>

Details about the child organization.Data type: Object

```
"organization": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

organizationChildRelationship.organization.@type

</td><td>

Type of the organization object. Value is always `Organization`.Data type: String

</td></tr><tr><td>

organizationChildRelationship.organization.id

</td><td>

Sys\_id of the child organization record.Table: Account \[customer\_account\] or Company \[core\_company\]

Data type: String

</td></tr><tr><td>

organizationChildRelationship.organization.name

</td><td>

Display name of the child organization.Data type: String

</td></tr><tr><td>

organizationChildRelationship.relationshipType

</td><td>

Type of relationship between this organization and the child organization. For example, `Partner Account`.Data type: String

</td></tr><tr><td>

organizationParentRelationship

</td><td>

Relationship to the parent organization.Data type: Object

```
"organizationParentRelationship": {
  "relationshipType": "String",
  "organization": {Object}
}
```

</td></tr><tr><td>

organizationParentRelationship.organization

</td><td>

Details about the parent organization.Data type: Object

```
"organization": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

organizationParentRelationship.organization.@type

</td><td>

Type of the organization object. Value is always `Organization`.Data type: String

</td></tr><tr><td>

organizationParentRelationship.organization.id

</td><td>

Sys\_id of the parent organization record.Table: Account \[customer\_account\] or Company \[core\_company\]

Data type: String

</td></tr><tr><td>

organizationParentRelationship.organization.name

</td><td>

Display name of the parent organization.Data type: String

</td></tr><tr><td>

organizationParentRelationship.relationshipType

</td><td>

Type of relationship between this organization and its parent.Possible values:

-   `Account`
-   `Company`
-   `HoldingCompany`
-   `ParentAccount`

Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics associated with the organization.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristic.@type

</td><td>

Subclass type of the characteristic.Possible values:

-   `BooleanCharacteristic`
-   `IntegerCharacteristic`
-   `StringArrayCharacteristic`
-   `StringCharacteristic`

Data type: String

</td></tr><tr><td>

partyCharacteristic.name

</td><td>

Name of the characteristic.Possible values:

-   `accountCode`
-   `identificationNumber`
-   `industry`
-   `manufacturer`
-   `marketCap`
-   `notes`
-   `numEmployees`
-   `profits`
-   `publiclyTraded`
-   `rankTier`
-   `registrationCode`
-   `revenuePerYear`
-   `stockPrice`
-   `stockSymbol`
-   `taxId`
-   `vendor`
-   `vendorType`
-   `website`

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic, as a string regardless of **valueType**. For example, `"false"` or `"10"`.Data type: String

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `choice`
-   `integer`
-   `list`
-   `string`

Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Party type, role, and account classification of the organization record.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "role": "String",
  "name": "String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

Type of party. Value is always `Account`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.name

</td><td>

Account classification. Multiple classifications are joined with underscores. For example, `customer` or `customer_partner`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Role of the party. Value is always `Account`.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts related to the organization.Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related contact.Data type: Object

```
"partyOrPartyRole": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Value is always `Individual`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related contact record.Table: Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the related contact.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related contact plays for the organization.Possible values:

-   `Account`
-   `other`: Other contact for the organization.
-   `primaryContact`: Primary contact for the organization.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the organization record.Possible values:

-   `active`: Organization is active.
-   `inactive`: Organization is inactive.

Data type: String

</td></tr><tr><td>

tradingName

</td><td>

Name that the organization trades under.Data type: String

</td></tr><tr><td>

warning

</td><td>

List of warning messages about parts of the request that couldn't be processed. The record is still created, but without the invalid values. Returned only when a warning occurs.Possible causes:

-   A **relatedParty** ID that doesn't match an existing record.
-   An invalid **locationId** in **contactMedium**.
-   An invalid display value for the `industry` or `rankTier` characteristic.

Example: `relatedParty[0] is incorrect. User does not exist`

Data type: Array of Strings

</td></tr></tbody>
</table>### cURL request

The following example creates an Account record, creates a location from the postal address, and links an existing contact.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v1/party/organization" \
  --request POST \
  --header "Accept: application/json" \
  --header "Content-Type: application/json" \
  --user 'user:password' \
  --data '{
  "@type": "Account",
  "name": "SERVICENOW 144",
  "legalName": "Acme Corp Ltd.",
  "tradingName": "Acme Inc.",
  "status": "active",
  "partyOrPartyRole": {
    "@type": "Account",
    "role": "Account",
    "name": "customer"
  },
  "contactMedium": [
    {
      "preferred": true,
      "mediumType": "email",
      "emailAddress": "athammhd@email.com",
      "@type": "EmailContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "mobilePhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "PhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "businessPhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "BusinessPhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "homePhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "HomePhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "postalAddress",
      "validFor": {
        "startDateTime": "2017-03-15T07:49:25.246Z"
      },
      "@type": "GeographicAddressContactMedium",
      "city": "chennai",
      "country": "INDIA",
      "postCode": "608001",
      "stateOrProvince": "tamil nadu",
      "street1": "samcon street",
      "street2": "adyar,chennai"
    }
  ],
  "externalReference": [
    {
      "externalIdentifierType": "Instagram",
      "id": "Instagram"
    }
  ],
  "partyCharacteristic": [
    {
      "name": "notes",
      "value": "Testing for update the notes",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "registrationCode",
      "value": "006",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "industry",
      "value": "Manufacturing",
      "valueType": "choice",
      "@type": "StringCharacteristics"
    },
    {
      "name": "taxId",
      "value": "CTNUM1000123",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "numEmployees",
      "value": "10",
      "valueType": "integer",
      "@type": "StringCharacteristics"
    },
    {
      "name": "rankTier",
      "value": "Valued Partner",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "publiclyTraded",
      "value": "false",
      "valueType": "boolean",
      "@type": "StringCharacteristics"
    },
    {
      "name": "vendor",
      "value": "false",
      "valueType": "boolean",
      "@type": "StringCharacteristics"
    },
    {
      "name": "manufacturer",
      "value": "false",
      "valueType": "boolean",
      "@type": "StringCharacteristics"
    }
  ],
  "relatedParty": [
    {
      "role": "Account",
      "partyOrPartyRole": {
        "id": "00189b324f1e0200c0adfe618110c76d",
        "name": "Crissy Stark",
        "@type": "Individual"
      }
    }
  ],
  "organizationChildRelationship": [
    {
      "relationshipType": "Partner Account",
      "organization": {
        "id": "051f62b0d7300200e5982cf65e610333",
        "name": "Spark Technologies",
        "@type": "Organization"
      }
    }
  ],
  "organizationParentRelationship": {
    "relationshipType": "Partner Account",
    "organization": {
      "id": "1b1b93da43c63110341605ed0bb8f2f4",
      "name": "Funco Intl.",
      "@type": "Organization"
    }
  }
}'
```

Response body.

```
{
  "id": "0fef075b2fe06a10b79db3bf42faf31c",
  "href": "http://instance.service-now.com/api/sn_tmf_api/v1/party/organization/0fef075b2fe06a10b79db3bf42faf31c",
  "@type": "Account",
  "name": "SERVICENOW 144",
  "legalName": "Acme Corp Ltd.",
  "tradingName": "Acme Inc.",
  "status": "active",
  "partyOrPartyRole": {
    "@type": "Account",
    "role": "Account",
    "name": "customer"
  },
  "contactMedium": [
    {
      "preferred": true,
      "mediumType": "email",
      "emailAddress": "athammhd@email.com",
      "@type": "EmailContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "mobilePhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "PhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "businessPhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "BusinessPhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "homePhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "HomePhoneContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "postalAddress",
      "validFor": {
        "startDateTime": "2017-03-15T07:49:25.246Z"
      },
      "@type": "GeographicAddressContactMedium",
      "locationId": "03e588a17be062105e0d5494548cb68c",
      "city": "chennai",
      "country": "INDIA",
      "postCode": "608001",
      "stateOrProvince": "tamil nadu",
      "street1": "samcon street",
      "street2": "adyar,chennai"
    }
  ],
  "externalReference": [
    {
      "externalIdentifierType": "Instagram",
      "id": "Instagram"
    }
  ],
  "partyCharacteristic": [
    {
      "name": "notes",
      "value": "Testing for update the notes",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "registrationCode",
      "value": "006",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "industry",
      "value": "Manufacturing",
      "valueType": "choice",
      "@type": "StringCharacteristics"
    },
    {
      "name": "taxId",
      "value": "CTNUM1000123",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "numEmployees",
      "value": "10",
      "valueType": "integer",
      "@type": "StringCharacteristics"
    },
    {
      "name": "rankTier",
      "value": "Valued Partner",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "publiclyTraded",
      "value": "false",
      "valueType": "boolean",
      "@type": "StringCharacteristics"
    },
    {
      "name": "vendor",
      "value": "false",
      "valueType": "boolean",
      "@type": "StringCharacteristics"
    },
    {
      "name": "manufacturer",
      "value": "false",
      "valueType": "boolean",
      "@type": "StringCharacteristics"
    }
  ],
  "relatedParty": [
    {
      "role": "Account",
      "partyOrPartyRole": {
        "id": "00189b324f1e0200c0adfe618110c76d",
        "name": "Crissy Stark",
        "@type": "Individual"
      }
    }
  ],
  "organizationChildRelationship": [
    {
      "relationshipType": "Partner Account",
      "organization": {
        "id": "051f62b0d7300200e5982cf65e610333",
        "name": "Spark Technologies",
        "@type": "Organization"
      }
    }
  ],
  "organizationParentRelationship": {
    "relationshipType": "Partner Account",
    "organization": {
      "id": "1b1b93da43c63110341605ed0bb8f2f4",
      "name": "Funco Intl.",
      "@type": "Organization"
    }
  },
  "createdDate": "2025-06-25T14:32:18.000Z",
  "lastModifiedDate": "2025-06-25T14:32:18.000Z"
}
```

