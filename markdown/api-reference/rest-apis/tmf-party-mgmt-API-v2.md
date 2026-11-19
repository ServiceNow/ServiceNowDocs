---
title: Party Management Open API v2
description: The Party Management Open API v2 provides endpoints for managing parties with a relationship to the enterprise, such as accounts, consumers, and contacts. Use this API to create, update, retrieve, and inactivate records in the Consumer \[csm\_consumer\], Account \[customer\_account\], and Contact \[customer\_contact\] tables.Inactivates a specified record from the Consumer \[csm\_consumer\] and Contact \[customer\_contact\] tables.Retrieves a specified record from the Consumer \[csm\_consumer\] or Contact \[customer\_contact\] tables. You can filter results by specific fields.Retrieves a list of all individual \(party\) records with a relationship to the enterprise. You can filter results by specific fields or IDs.Retrieves a specified record from the Account \[customer\_account\] tables. You can filter results by specific fields or IDs.Retrieves organization-level party records from the Company \[core\_company\] and Account \[customer\_account\] tables. You can filter results by specific fields or IDs.Updates an existing individual party record in the Consumer \[csm\_consumer\] or Contact \[customer\_contact\] table without replacing the entire resource.Updates an existing individual party record in the Account \[customer\_account\] tables without replacing the entire resource.Creates a new individual party management record in the Consumer \[csm\_consumer\] or Contact \[customer\_contact\] tables.Creates a new party organization record in the Account \[customer\_account\] tables. You can also create and associate Contact and Location records inline during organization creation, eliminating the need for separate POST operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/rest-apis/tmf-party-mgmt-API-v2.html
release: brazil
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-11-04"
reading_time_minutes: 106
breadcrumb: [Party Management Open API, REST API reference, API reference, API implementation and reference]
---

# Party Management Open API v2

The Party Management Open API v2 provides endpoints for managing parties with a relationship to the enterprise, such as accounts, consumers, and contacts. Use this API to create, update, retrieve, and inactivate records in the Consumer \[csm\_consumer\], Account \[customer\_account\], and Contact \[customer\_contact\] tables.

The Party Management Open API is a ServiceNow implementation of the TM Forum Party Management API REST specification, based on the TMF632 Party Management API Conformance Profile v5.0.0, June 2025. The API is conformance certified by TM Forum.

This API is provided within the sn\_tmf\_api namespace. The calling user must have the sn\_tmf\_api.party\_integrator role. The Customer Service Base Entities \(com.snc.cs\_base\) plugin is required.

v2 is the current version of the Party Management Open API and aligns with the TMF632 CTK. Requests use v2 by default. To use a [Party Management Open API v1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/tmf-party-mgmt-API-v1.md) endpoint, specify v1 in the endpoint path.

You can extend this API to customize required parameters, request body validation, additional REST operations, and field mappings. Sensitive fields, such as phone numbers, may require special ACL permissions for update or retrieval.

**Parent Topic:**[Party Management Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/tmf-party-management-open-api.md)

## Party Management v2 – DELETE /api/sn\_tmf\_api/v2/party/individual/\{id\}

Inactivates a specified record from the Consumer \[csm\_consumer\] and Contact \[customer\_contact\] tables.

### URL format

Versioned URL: `/api/sn_tmf_api/{api_version}/party/individual/{id}`

Default URL: `/api/sn_tmf_api/v2/party/individual/{id}`

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
|404|Resource not found. Sys\_id or external\_id doesn't exist in the system. Try a different ID.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

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
curl "http://instance.service-now.com/api/sn_tmf_api/v2/party/individual/a1b2c3d4e5f6478990abcdef12345678" \
  --request DELETE \
  --header "Accept: application/json" \
  --user 'user:password'
```

Doesn't return a response body. Reference status codes for a success or failure indicator.

## Party Management - GET /api/sn\_tmf\_api/v2/party/individual/\{id\}

Retrieves a specified record from the Consumer \[csm\_consumer\] or Contact \[customer\_contact\] tables. You can filter results by specific fields.

### URL format

Versioned URL: `/api/sn_tmf_api/{api_version}/party/individual/{id}`

Default URL: `/api/sn_tmf_api/v2/party/individual/{id}`

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

-   `@type`
-   `familyName`
-   `gender`
-   `givenName`
-   `href`
-   `id`
-   `middleName`
-   `name`
-   `nationality`
-   `status`
-   `title`

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

<table id="partymgmt-GET-id-v2-response-table"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Response object\}

</td><td>

Consumer or Contact record. Consumers don't return **name**, and Contacts don't return **nationality**.```
{
  "id": "String",
  "href": "String",
  "@type": "String",
  "externalId": "String",
  "name": "String",
  "givenName": "String",
  "middleName": "String",
  "familyName": "String",
  "gender": "String",
  "nationality": "String",
  "title": "String",
  "status": "String",
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

-   `Consumer`
-   `Contact`

Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of ways to contact the individual. Always includes business, home, and mobile phone entries, even when they're empty. Consumers also include a fax entry. A fax number saved on a Contact isn't returned. Email and address entries are included only when the record has them.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "contactType": "String",
  "country": "String",
  "emailAddress": "String",
  "locationId": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": Boolean,
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
-   `FaxContactMedium`: Fax number. Consumers only.
-   `GeographicalAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `MobilePhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.contactType

</td><td>

Type of contact channel. Replaces the v1 **mediumType** parameter.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number. Consumers only.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address. Used when **contactType** is `email`.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location record linked to the address.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number. Used when **contactType** is a phone or fax type.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium. Always `false` in GET responses.Data type: Boolean

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

externalId

</td><td>

Identifier of the record in your source system or third-party application. Returned only when the record has an external ID.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the individual in external systems, such as social profiles. Empty if the individual has none.Data type: Array of Objects

```
"externalReference": [
 {
  "@type": "String",
  "externalIdentifierType": "String",
  "id": "String"
 }
]
```

</td></tr><tr><td>

externalReference.@type

</td><td>

Type of the external reference. Value is always `ExternalIdentifier`.Data type: String

</td></tr><tr><td>

externalReference.externalIdentifierType

</td><td>

Name of the external system or social channel. For example, `Instagram` or `LinkedIn`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the party in the external system, such as a profile URL or handle.Data type: String

</td></tr><tr><td>

familyName

</td><td>

Last name of the individual.Data type: String

</td></tr><tr><td>

gender

</td><td>

Gender of the individual. Must match a choice value on the record. For a Contact created without a gender, the value is set to `Not Specified`.Data type: String

</td></tr><tr><td>

givenName

</td><td>

First name of the individual.Data type: String

</td></tr><tr><td>

href

</td><td>

Link to the Consumer or Contact record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the Consumer or Contact record. Always the sys\_id, even when the record has an external ID.Table: Consumer \[csm\_consumer\] or Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

name

</td><td>

User name of the individual. For a Contact, the user name must be unique.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics of the individual, such as notification and date format preferences.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String or Boolean",
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

Name of the characteristic.Possible values for a Consumer:

-   `dateFormat`
-   `notes`
-   `notification`
-   `preferredLanguage`
-   `timeFormat`
-   `timeZone`
-   `user`

Possible values for a Contact:

-   `dateFormat`
-   `eduStatus`
-   `notification`
-   `preferredLanguage`
-   `source`
-   `timeFormat`
-   `timeZone`
-   `vip`
-   `webServiceAccessOnly`

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic. Choice characteristics, such as `dateFormat` and `timeZone`, take the display value. An invalid choice value returns a warning.Data type: String, or Boolean for `vip` and `webServiceAccessOnly`

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `string`

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties related to the individual. A Consumer returns its linked user. A Contact returns its account.Data type: Array of Objects

```
"relatedParty": [
 {
  "@type": "String",
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

Type of the related party.Possible values:

-   `Account`: Account of a Contact.
-   `User`: User linked to a Consumer.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related party.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party record.Possible values:

-   `Individual`: Related party is a user.
-   `Organization`: Related party is an account.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related record. For a Contact's account, requests also accept the account's external\_id, and the response returns the sys\_id.Table: Depends on the role:

-   Account: Account \[customer\_account\]
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

-   `Account`: Account of a Contact.
-   `User`: User linked to a Consumer.

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
curl "http://instance.service-now.com/api/sn_tmf_api/v2/party/individual/a1b2c3d4e5f6478990abcdef12345678" \
  --request GET \
  --header "Accept: application/json" \
  --user 'user:password'
```

Response body.

```
{
  "id": "a1b2c3d4e5f6478990abcdef12345678",
  "href": "http://instance.service-now.com/api/sn_tmf_api/v2/party/individual/a1b2c3d4e5f6478990abcdef12345678",
  "givenName": "John",
  "middleName": "A.",
  "familyName": "Doe",
  "gender": "male",
  "nationality": "American",
  "title": "Mr",
  "contactMedium": [
    {
      "preferred": true,
      "contactType": "email",
      "emailAddress": "john.doe@example.com",
      "@type": "EmailContactMedium"
    },
    {
      "preferred": false,
      "contactType": "mobilePhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "MobilePhoneContactMedium"
    },
    {
      "preferred": false,
      "contactType": "businessPhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "BusinessPhoneContactMedium"
    },
    {
      "preferred": false,
      "contactType": "faxPhone",
      "phoneNumber": "123456789",
      "@type": "FaxContactMedium"
    },
    {
      "preferred": false,
      "contactType": "homePhone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "HomePhoneContactMedium"
    },
    {
      "preferred": false,
      "contactType": "postalAddress",
      "@type": "GeographicalAddressContactMedium",
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
      "contactType": "postalAddress",
      "@type": "GeographicalAddressContactMedium",
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
      "@type": "User",
      "partyOrPartyRole": {
        "id": "36901a6381116a50f8776cfcbee15f3c",
        "name": "John Doe",
        "@type": "Individual"
      }
    }
  ],
  "status": "active",
  "@type": "Consumer"
}
```

## Party Management v2 – GET /api/sn\_tmf\_api/v2/party/individual

Retrieves a list of all individual \(party\) records with a relationship to the enterprise. You can filter results by specific fields or IDs.

### URL format

Versioned URL: `/api/sn_tmf_api/{version_number}/party/individual`

Default URL: `/api/sn_tmf_api/v2/party/individual`

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

@type

</td><td>

Filter the list by record type. The value isn't case-sensitive. Replaces the v1 **role** query parameter. A request that includes **role** returns an error.Valid values:

-   `Consumer`: Return only Consumer records.
-   `Contact`: Return only Contact records.

Data type: String

Default: Returns only Consumer records.

</td></tr><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored.Valid fields:

-   `@type`
-   `familyName`
-   `gender`
-   `givenName`
-   `href`
-   `id`
-   `middleName`
-   `name`
-   `nationality`
-   `status`
-   `title`

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

<table id="partymgmt-GET-individual-v2-response-table"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Response object\}

</td><td>

List of Consumer or Contact records. Each record in the array has the following structure. Consumers don't return **name**, and Contacts don't return **nationality**.```
[
 {
   "id": "String",
   "href": "String",
   "@type": "String",
   "externalId": "String",
   "name": "String",
   "givenName": "String",
   "middleName": "String",
   "familyName": "String",
   "gender": "String",
   "nationality": "String",
   "title": "String",
   "status": "String",
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

-   `Consumer`
-   `Contact`

Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of ways to contact the individual. Always includes business, home, and mobile phone entries, even when they're empty. Consumers also include a fax entry. A fax number saved on a Contact isn't returned. Email and address entries are included only when the record has them.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "contactType": "String",
  "country": "String",
  "emailAddress": "String",
  "locationId": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": Boolean,
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
-   `FaxContactMedium`: Fax number. Consumers only.
-   `GeographicalAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `MobilePhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.contactType

</td><td>

Type of contact channel. Replaces the v1 **mediumType** parameter.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number. Consumers only.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address. Used when **contactType** is `email`.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location record linked to the address.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number. Used when **contactType** is a phone or fax type.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium. Always `false` in GET responses.Data type: Boolean

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

externalId

</td><td>

Identifier of the record in your source system or third-party application. Returned only when the record has an external ID.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the individual in external systems, such as social profiles. Empty if the individual has none.Data type: Array of Objects

```
"externalReference": [
 {
  "@type": "String",
  "externalIdentifierType": "String",
  "id": "String"
 }
]
```

</td></tr><tr><td>

externalReference.@type

</td><td>

Type of the external reference. Value is always `ExternalIdentifier`.Data type: String

</td></tr><tr><td>

externalReference.externalIdentifierType

</td><td>

Name of the external system or social channel. For example, `Instagram` or `LinkedIn`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the party in the external system, such as a profile URL or handle.Data type: String

</td></tr><tr><td>

familyName

</td><td>

Last name of the individual.Data type: String

</td></tr><tr><td>

gender

</td><td>

Gender of the individual. Must match a choice value on the record. For a Contact created without a gender, the value is set to `Not Specified`.Data type: String

</td></tr><tr><td>

givenName

</td><td>

First name of the individual.Data type: String

</td></tr><tr><td>

href

</td><td>

Link to the Consumer or Contact record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the Consumer or Contact record. Always the sys\_id, even when the record has an external ID.Table: Consumer \[csm\_consumer\] or Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

name

</td><td>

User name of the individual. For a Contact, the user name must be unique.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics of the individual, such as notification and date format preferences.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String or Boolean",
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

Name of the characteristic.Possible values for a Consumer:

-   `dateFormat`
-   `notes`
-   `notification`
-   `preferredLanguage`
-   `timeFormat`
-   `timeZone`
-   `user`

Possible values for a Contact:

-   `dateFormat`
-   `eduStatus`
-   `notification`
-   `preferredLanguage`
-   `source`
-   `timeFormat`
-   `timeZone`
-   `vip`
-   `webServiceAccessOnly`

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic. Choice characteristics, such as `dateFormat` and `timeZone`, take the display value. An invalid choice value returns a warning.Data type: String, or Boolean for `vip` and `webServiceAccessOnly`

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `string`

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties related to the individual. A Consumer returns its linked user. A Contact returns its account.Data type: Array of Objects

```
"relatedParty": [
 {
  "@type": "String",
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

Type of the related party.Possible values:

-   `Account`: Account of a Contact.
-   `User`: User linked to a Consumer.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related party.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party record.Possible values:

-   `Individual`: Related party is a user.
-   `Organization`: Related party is an account.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related record. For a Contact's account, requests also accept the account's external\_id, and the response returns the sys\_id.Table: Depends on the role:

-   Account: Account \[customer\_account\]
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

-   `Account`: Account of a Contact.
-   `User`: User linked to a Consumer.

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
curl "http://instance.service-now.com/api/sn_tmf_api/v2/party/individual" \
  --request GET \
  --header "Accept: application/json" \
  --user 'user:password'
```

Response body for a Contact record.

```
[
{
   "id": "a1b2c3d4e5f6478990abcdef12345678",
   "href": "http://instance.service-now.com/api/sn_tmf_api/v2/party/individual/a1b2c3d4e5f6478990abcdef12345678",
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
       "contactType": "email",
       "emailAddress": "carlos.star@example.com",
       "@type": "EmailContactMedium"
     },
     {
       "preferred": false,
       "contactType": "businessPhone",
       "phoneNumber": "",
       "@type": "BusinessPhoneContactMedium"
     },
     {
       "preferred": false,
       "contactType": "homePhone",
       "phoneNumber": "",
       "@type": "HomePhoneContactMedium"
     },
     {
       "preferred": false,
       "contactType": "mobilePhone",
       "phoneNumber": "",
       "@type": "MobilePhoneContactMedium"
     }
   ],
   "externalReference": [],
   "relatedParty": [
     {
       "role": "Account",
       "@type": "Account",
       "partyOrPartyRole": {
         "id": "9e2fd2ee11b43110f877366201dea674",
         "name": "Startech svcs",
         "@type": "Organization"
       }
     }
   ],
   "status": "active",
   "@type": "Contact"
 }
]
```

Response body for a Consumer record.

```
[
{
   "id": "168bfc6953a46210132bddeeff7b129f",
   "href": "http://instance.service-now.com/api/sn_tmf_api/v2/party/individual/168bfc6953a46210132bddeeff7b129f",
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
       "contactType": "businessPhone",
       "phoneNumber": "",
       "@type": "BusinessPhoneContactMedium"
     },
     {
       "preferred": false,
       "contactType": "homePhone",
       "phoneNumber": "",
       "@type": "HomePhoneContactMedium"
     },
     {
       "preferred": false,
       "contactType": "mobilePhone",
       "phoneNumber": "",
       "@type": "MobilePhoneContactMedium"
     },
     {
       "preferred": false,
       "contactType": "faxPhone",
       "phoneNumber": "",
       "@type": "FaxContactMedium"
     },
     {
       "preferred": false,
       "contactType": "postalAddress",
       "@type": "GeographicalAddressContactMedium",
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
       "@type": "User",
       "partyOrPartyRole": {
         "id": "",
         "name": "",
         "@type": "Individual"
       }
     }
   ],
   "status": "active",
   "@type": "Consumer"
 }
]
```

## Party Management v2 – GET/api/ sn\_tmf\_api/v2/party/organization/\{id\}

Retrieves a specified record from the Account \[customer\_account\] tables. You can filter results by specific fields or IDs.

### URL format

Versioned URL: `/api/sn_tmf_api/{version_number}/party/organization/{id}`

Default URL: `/api/sn_tmf_api/v2/party/organization/{id}`

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

-   `@type`
-   `href`
-   `id`
-   `legalName`
-   `name`
-   `status`
-   `tradingName`

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

<table id="partymgmt-GET-org-id-v2-response-table"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Response object\}

</td><td>

Account record.```
{
  "id": "String",
  "href": "String",
  "@type": "String",
  "externalId": "String",
  "name": "String",
  "legalName": "String",
  "tradingName": "String",
  "organizationType": "String",
  "status": "String",
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

List of ways to contact the organization. Always includes email, phone, and fax entries, even when they're empty, plus an entry for each linked address.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "contactType": "String",
  "country": "String",
  "emailAddress": "String",
  "latitude": "String",
  "locationId": "String",
  "longitude": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": "String",
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

-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicalAddressContactMedium`: Physical address.
-   `PhoneContactMedium`: Phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.contactType

</td><td>

Type of contact channel. Replaces the v1 **mediumType** parameter.Possible values:

-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `phone`: Phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address. Used when **contactType** is `email`.Data type: String

</td></tr><tr><td>

contactMedium.latitude

</td><td>

Latitude of the address.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location record linked to the address.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.longitude

</td><td>

Longitude of the address.Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number. Used when **contactType** is a phone or fax type.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium. Always `"false"` in GET responses.Data type: String

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

externalId

</td><td>

Identifier of the record in your source system or third-party application. Returned only when the record has an external ID.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the organization in external systems, such as social profiles. Empty if the organization has none.Data type: Array of Objects

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

Name of the external system or social channel. For example, `Instagram`.Data type: String

</td></tr><tr><td>

externalReference.name

</td><td>

Profile URL of the organization in the external system.Data type: String

</td></tr><tr><td>

href

</td><td>

Link to the Account record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the Account record. Always the sys\_id, even when the record has an external ID.Table: Account \[customer\_account\]

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

List of child organizations related to this organization, such as partner, subsidiary, or branch accounts.Data type: Array of Objects

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
  "@type": "String",
  "href": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

organizationChildRelationship.organization.@type

</td><td>

Type of the organization object. Value is always `Organization`.Data type: String

</td></tr><tr><td>

organizationChildRelationship.organization.href

</td><td>

Link to the child organization record.Data type: String

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

Type of relationship between this organization and the child organization.In requests, the value is converted to lowercase and must match a relationship type defined in your instance. If no match is found, the response includes a warning. Available values depend on your instance configuration.

Table: Account Relationship Type \[sn\_customerservice\_account\_relationship\_type\]

Data type: String

</td></tr><tr><td>

organizationParentRelationship

</td><td>

Parent organization of this organization. Empty if the organization has no parent.Data type: Object

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
  "@type": "String",
  "href": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

organizationParentRelationship.organization.@type

</td><td>

Type of the organization object. Value is always `Organization`.Data type: String

</td></tr><tr><td>

organizationParentRelationship.organization.href

</td><td>

Link to the parent organization record.Data type: String

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

Type of relationship between this organization and its parent. Value is always `parent`.Data type: String

</td></tr><tr><td>

organizationType

</td><td>

Account classification of the organization, such as `customer` or `customer_partner`. Multiple classifications are joined with underscores, in the order customer, partner, vendor, manufacturer. Returned only when the account has at least one classification.Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics of the organization, such as industry and number of employees.Data type: Array of Objects

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
-   `customer`: Request only.
-   `identificationNumber`
-   `industry`
-   `manufacturer`: Request only.
-   `marketCap`
-   `notes`
-   `numEmployees`
-   `partner`: Request only.
-   `profits`
-   `publiclyTraded`
-   `rankTier`
-   `registrationCode`
-   `revenuePerYear`
-   `stockPrice`
-   `stockSymbol`
-   `taxId`
-   `vendor`: Request only.
-   `vendorType`
-   `website`

**Note:** For the `industry` and `rankTier` characteristics, provide the display value of the choice, such as `Manufacturing` or `Valued Partner`. An invalid value returns a warning.

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic. GET returns all values as strings, regardless of **valueType**. For example, `"false"` or `"10"`.Data type: String. Requests also accept a Boolean, or an Array of Strings for `vendorType`.

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `choice`
-   `currency`
-   `integer`
-   `list`
-   `string`
-   `url`

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts related to the organization. Empty if the organization has no contacts.Data type: Array of Objects

```
"relatedParty": [
 {
  "@type": "String",
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

Type of the related party. Value is always `contact`. Required in each request entry.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related contact.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party record. Value is always `Organization`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related contact record. Requests also accept the contact's external\_id.Table: Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the related contact.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related contact plays for the organization. Requests use `primaryContact`, but GET returns `primary`.Possible values:

-   `other`: Other contact for the organization.
-   `primary`: Primary contact for the organization.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the organization record. Returned only when the Domain Extensions Installer plugin \(com.glide.domain.msp\_extensions.installer\) is active.Possible values:

-   `Active`: Organization is active.
-   `InActive`: Organization is inactive.

Data type: String

</td></tr><tr><td>

tradingName

</td><td>

Name that the organization trades under.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example retrieves the Account record with sys\_id a1b2c3d4e5f6478990abcdef12345678.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v2/party/organization/a1b2c3d4e5f6478990abcdef12345678" \
  --request GET \
  --header "Accept: application/json" \
  --user 'user:password'
```

Response body.

```
{
  "id": "a1b2c3d4e5f6478990abcdef12345678",
  "href": "http://instance.service-now.com/api/sn_tmf_api/v2/party/organization/a1b2c3d4e5f6478990abcdef12345678",
  "name": "Advanced Super Computing",
  "legalName": "Advanced Super Computing Inc.",
  "tradingName": "ASC",
  "organizationType": "partner_vendor",
  "contactMedium": [
    {
      "preferred": false,
      "contactType": "email",
      "emailAddress": "user@example.com",
      "@type": "EmailContactMedium"
    },
    {
      "preferred": false,
      "contactType": "phone",
      "phoneNumber": "+1-202-555-0123",
      "@type": "PhoneContactMedium"
    },
    {
      "preferred": false,
      "contactType": "faxPhone",
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
      "role": "primary",
      "@type": "contact",
      "partyOrPartyRole": {
        "id": "b88d14843bc02300bfe04d72f3efc4cd",
        "name": "Amy Chen",
        "@type": "Organization"
      }
    },
    {
      "role": "other",
      "@type": "contact",
      "partyOrPartyRole": {
        "id": "016b7a36ff14a610f8dfffffffffffcb",
        "name": "Mary Star",
        "@type": "Organization"
      }
    }
  ],
  "organizationChildRelationship": [
    {
      "relationshipType": "Partner Account",
      "organization": {
        "id": "9e2fd2ee11b43110f877366201dea674",
        "name": "Startech svcs",
        "href": "http://instance.service-now.com/api/sn_tmf_api/v2/party/organization/9e2fd2ee11b43110f877366201dea674",
        "@type": "Organization"
      }
    }
  ],
  "organizationParentRelationship": {
    "relationshipType": "parent",
    "organization": {
      "id": "ffc68911c35420105252716b7d40dd55",
      "name": "Funco Intl.",
      "href": "http://instance.service-now.com/api/sn_tmf_api/v2/party/organization/ffc68911c35420105252716b7d40dd55",
      "@type": "Organization"
    }
  },
  "status": "InActive",
  "@type": "Account"
}
```

## Party Management v2 - GET /api/sn\_tmf\_api/v2/party/organization

Retrieves organization-level party records from the Company \[core\_company\] and Account \[customer\_account\] tables. You can filter results by specific fields or IDs.

### URL format

Versioned URL: `/api/sn_tmf_api/{version_number}/party/organization`

Default URL: `/api/sn_tmf_api/v2/party/organization`

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

@type

</td><td>

Filter the list by record type. Value must be `Account`. Any other value returns an error.Data type: String

</td></tr><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored.Valid fields:

-   `@type`
-   `href`
-   `id`
-   `legalName`
-   `name`
-   `status`
-   `tradingName`

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

<table id="partymgmt-GET-org-v2-response-table"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Response object\}

</td><td>

List of Account records. Each record in the array has the following structure.```
[
 {
   "id": "String",
   "href": "String",
   "@type": "String",
   "externalId": "String",
   "name": "String",
   "legalName": "String",
   "tradingName": "String",
   "organizationType": "String",
   "status": "String",
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

List of ways to contact the organization. Always includes email, phone, and fax entries, even when they're empty, plus an entry for each linked address.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "contactType": "String",
  "country": "String",
  "emailAddress": "String",
  "latitude": "String",
  "locationId": "String",
  "longitude": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": "String",
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

-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicalAddressContactMedium`: Physical address.
-   `PhoneContactMedium`: Phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.contactType

</td><td>

Type of contact channel. Replaces the v1 **mediumType** parameter.Possible values:

-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `phone`: Phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address. Used when **contactType** is `email`.Data type: String

</td></tr><tr><td>

contactMedium.latitude

</td><td>

Latitude of the address.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location record linked to the address.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.longitude

</td><td>

Longitude of the address.Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number. Used when **contactType** is a phone or fax type.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium. Always `"false"` in GET responses.Data type: String

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

externalId

</td><td>

Identifier of the record in your source system or third-party application. Returned only when the record has an external ID.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the organization in external systems, such as social profiles. Empty if the organization has none.Data type: Array of Objects

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

Name of the external system or social channel. For example, `Instagram`.Data type: String

</td></tr><tr><td>

externalReference.name

</td><td>

Profile URL of the organization in the external system.Data type: String

</td></tr><tr><td>

href

</td><td>

Link to the Account record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the Account record. Always the sys\_id, even when the record has an external ID.Table: Account \[customer\_account\]

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

List of child organizations related to this organization, such as partner, subsidiary, or branch accounts.Data type: Array of Objects

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
  "@type": "String",
  "href": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

organizationChildRelationship.organization.@type

</td><td>

Type of the organization object. Value is always `Organization`.Data type: String

</td></tr><tr><td>

organizationChildRelationship.organization.href

</td><td>

Link to the child organization record.Data type: String

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

Type of relationship between this organization and the child organization.In requests, the value is converted to lowercase and must match a relationship type defined in your instance. If no match is found, the response includes a warning. Available values depend on your instance configuration.

Table: Account Relationship Type \[sn\_customerservice\_account\_relationship\_type\]

Data type: String

</td></tr><tr><td>

organizationParentRelationship

</td><td>

Parent organization of this organization. Empty if the organization has no parent.Data type: Object

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
  "@type": "String",
  "href": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

organizationParentRelationship.organization.@type

</td><td>

Type of the organization object. Value is always `Organization`.Data type: String

</td></tr><tr><td>

organizationParentRelationship.organization.href

</td><td>

Link to the parent organization record.Data type: String

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

Type of relationship between this organization and its parent. Value is always `parent`.Data type: String

</td></tr><tr><td>

organizationType

</td><td>

Account classification of the organization, such as `customer` or `customer_partner`. Multiple classifications are joined with underscores, in the order customer, partner, vendor, manufacturer. Returned only when the account has at least one classification.Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics of the organization, such as industry and number of employees.Data type: Array of Objects

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
-   `customer`: Request only.
-   `identificationNumber`
-   `industry`
-   `manufacturer`: Request only.
-   `marketCap`
-   `notes`
-   `numEmployees`
-   `partner`: Request only.
-   `profits`
-   `publiclyTraded`
-   `rankTier`
-   `registrationCode`
-   `revenuePerYear`
-   `stockPrice`
-   `stockSymbol`
-   `taxId`
-   `vendor`: Request only.
-   `vendorType`
-   `website`

**Note:** For the `industry` and `rankTier` characteristics, provide the display value of the choice, such as `Manufacturing` or `Valued Partner`. An invalid value returns a warning.

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic. GET returns all values as strings, regardless of **valueType**. For example, `"false"` or `"10"`.Data type: String. Requests also accept a Boolean, or an Array of Strings for `vendorType`.

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `choice`
-   `currency`
-   `integer`
-   `list`
-   `string`
-   `url`

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts related to the organization. Empty if the organization has no contacts.Data type: Array of Objects

```
"relatedParty": [
 {
  "@type": "String",
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

Type of the related party. Value is always `contact`. Required in each request entry.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related contact.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party record. Value is always `Organization`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related contact record. Requests also accept the contact's external\_id.Table: Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the related contact.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related contact plays for the organization. Requests use `primaryContact`, but GET returns `primary`.Possible values:

-   `other`: Other contact for the organization.
-   `primary`: Primary contact for the organization.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the organization record. Returned only when the Domain Extensions Installer plugin \(com.glide.domain.msp\_extensions.installer\) is active.Possible values:

-   `Active`: Organization is active.
-   `InActive`: Organization is inactive.

Data type: String

</td></tr><tr><td>

tradingName

</td><td>

Name that the organization trades under.Data type: String

</td></tr></tbody>
</table>### cURL request

This returns all organization records related to the enterprise.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v2/party/organization" \
  --request GET \
  --header "Accept: application/json" \
  --user 'user:password'
```

Response body.

```
[
  {
    "id": "0bd6717c184da610f87765359bc696d3",
    "href": "http://instance.service-now.com/api/sn_tmf_api/v2/party/organization/0bd6717c184da610f87765359bc696d3",
    "name": "SERVICENOW 144",
    "legalName": "",
    "tradingName": "",
    "organizationType": "customer",
    "contactMedium": [
      {
        "preferred": false,
        "contactType": "email",
        "emailAddress": "user@example.com",
        "@type": "EmailContactMedium"
      },
      {
        "preferred": false,
        "contactType": "phone",
        "phoneNumber": "+1-202-555-0123",
        "@type": "PhoneContactMedium"
      },
      {
        "preferred": false,
        "contactType": "faxPhone",
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
          "href": "http://instance.service-now.com/api/sn_tmf_api/v2/party/organization/396b47201841a610f87765359bc696cf",
          "@type": "Organization"
        }
      }
    ],
    "organizationParentRelationship": {
      "relationshipType": "parent",
      "organization": {
        "id": "9e2fd2ee11b43110f877366201dea674",
        "name": "Startech svcs",
        "href": "http://instance.service-now.com/api/sn_tmf_api/v2/party/organization/9e2fd2ee11b43110f877366201dea674",
        "@type": "Organization"
      }
    },
    "status": "Active",
    "@type": "Account"
  }
]
```

## Party Management v2 – PATCH/api/sn\_tmf\_api/v2/party/individual/\{id\}

Updates an existing individual party record in the Consumer \[csm\_consumer\] or Contact \[customer\_contact\] table without replacing the entire resource.

### URL format

Versioned URL: `/api/sn_tmf_api/{version_number}/party/individual/{id}`

Default URL: `/api/sn_tmf_api/v2/party/individual/{id}`

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

Sys\_id of the Consumer or Contact record to update. External IDs aren't accepted.Tables: Consumer \[csm\_consumer\] or Contact \[customer\_contact\]

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="partymgmt-PATCH-id-v2-request-table" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Request object\}

</td><td>

Fields to update on the Consumer or Contact record. Include only the fields to change, plus the required **@type**. The **@type** value must match the record type.```
{
  "@type": "String",
  "externalId": "String",
  "name": "String",
  "givenName": "String",
  "middleName": "String",
  "familyName": "String",
  "gender": "String",
  "nationality": "String",
  "title": "String",
  "status": "String",
  "contactMedium": [Array],
  "externalReference": [Array],
  "partyCharacteristic": [Array],
  "relatedParty": [Array]
}
```

</td></tr><tr><td>

@type

</td><td>

Required. Type of individual record to create or update. Replaces the root **partyOrPartyRole** object from v1. The value isn't case-sensitive.Valid values:

-   `Consumer`: Consumer record.
-   `Contact`: Contact record.

Any other value, including `Account`, returns an error.

Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of ways to contact the individual.For a Contact, a POST request must include an entry with **contactType** set to `email` and a valid **emailAddress**.

Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "contactType": "String",
  "country": "String",
  "emailAddress": "String",
  "locationId": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": Boolean,
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
-   `FaxContactMedium`: Fax number.
-   `GeographicalAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `MobilePhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.contactType

</td><td>

Type of contact channel. Replaces the v1 **mediumType** parameter.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address. Used when **contactType** is `email`.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id or external\_id of an existing location record to link to the individual. Used when **contactType** is `postalAddress`.How the location is handled depends on the record type:

-   Consumer: If you provide a locationId that doesn't exist, the system creates a new location from the address fields and returns a warning. If you omit locationId, the system creates a new location from the address fields.
-   Contact: The locationId must match an existing location. If it doesn't, the address is skipped and the response returns a warning.

Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number. Used when **contactType** is a phone or fax type.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Valid values:

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

Period during which the contact medium is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

contactMedium.validFor.startDateTime

</td><td>

Date and time from which the contact medium is valid, in ISO 8601 format. For example, `2017-03-15T07:49:25.246Z`.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Identifier of the record in your source system or third-party application. Leading and trailing spaces are removed, and a blank value is ignored.On a PATCH request, you can't clear an external ID once it's set. If you send a blank value for a record that already has one, the existing value is kept and the response includes a warning.

Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the individual in external systems, such as social profiles. Each entry requires **externalIdentifierType** and **id**.Data type: Array of Objects

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

Name of the external system or social channel. For example, `Instagram` or `LinkedIn`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the party in the external system, such as a profile URL or handle.Data type: String

</td></tr><tr><td>

familyName

</td><td>

Last name of the individual.Data type: String

</td></tr><tr><td>

gender

</td><td>

Gender of the individual. Must match a choice value on the record. For a Contact created without a gender, the value is set to `Not Specified`.Data type: String

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

User name of the individual. For a Contact, the user name must be unique.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics of the individual, such as notification and date format preferences. Each entry requires **name**, **valueType**, and **@type**.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String or Boolean",
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

Name of the characteristic.Possible values for a Consumer:

-   `dateFormat`
-   `notes`
-   `notification`
-   `preferredLanguage`
-   `timeFormat`
-   `timeZone`
-   `user`

Possible values for a Contact:

-   `dateFormat`
-   `eduStatus`
-   `notification`
-   `preferredLanguage`
-   `source`
-   `timeFormat`
-   `timeZone`
-   `vip`
-   `webServiceAccessOnly`

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic. Choice characteristics, such as `dateFormat` and `timeZone`, take the display value. An invalid choice value returns a warning.Data type: String, or Boolean for `vip` and `webServiceAccessOnly`

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `string`

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties related to the individual. The rules depend on the record type:-   Consumer: Optional. Use the `User` role to link a user. Each `User` entry requires **@type** set to `User`, or the request fails. Entries with any other role are ignored and return a warning.
-   Contact: Required on POST. Must include an entry with the `Account` role, **@type** set to `Account`, and a **partyOrPartyRole** object with **@type** and the **id** of an existing account. Only the first `Account` entry is used. On PATCH, omit this object to keep the current account. An empty array returns an error.

Data type: Array of Objects

```
"relatedParty": [
 {
  "@type": "String",
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

Type of the related party.Possible values:

-   `Account`: Account of a Contact.
-   `User`: User linked to a Consumer.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related party.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party record.Possible values:

-   `Individual`: Related party is a user.
-   `Organization`: Related party is an account.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related record. For a Contact's account, requests also accept the account's external\_id, and the response returns the sys\_id.Table: Depends on the role:

-   Account: Account \[customer\_account\]
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

-   `Account`: Account of a Contact.
-   `User`: User linked to a Consumer.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the individual record. The value isn't case-sensitive. Any value other than `inactive` sets the record to active.Valid values:

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

<table id="partymgmt-PATCH-id-v2-response-table"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Response object\}

</td><td>

Updated Consumer or Contact record. The response returns the fields sent in the request, plus the record's **id** and **href**.```
{
  "id": "String",
  "href": "String",
  "@type": "String",
  "externalId": "String",
  "name": "String",
  "givenName": "String",
  "middleName": "String",
  "familyName": "String",
  "gender": "String",
  "nationality": "String",
  "title": "String",
  "status": "String",
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

-   `Consumer`
-   `Contact`

Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of ways to contact the individual, as sent in the request. Address entries include the **locationId** of the linked location.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "contactType": "String",
  "country": "String",
  "emailAddress": "String",
  "locationId": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": Boolean,
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
-   `FaxContactMedium`: Fax number.
-   `GeographicalAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `MobilePhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.contactType

</td><td>

Type of contact channel. Replaces the v1 **mediumType** parameter.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address. Used when **contactType** is `email`.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location record linked to the address.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number. Used when **contactType** is a phone or fax type.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Valid values:

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

Period during which the contact medium is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

contactMedium.validFor.startDateTime

</td><td>

Date and time from which the contact medium is valid, in ISO 8601 format. For example, `2017-03-15T07:49:25.246Z`.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Identifier of the record in your source system or third-party application. Returned only when the record has an external ID.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the individual in external systems, as sent in the request.Data type: Array of Objects

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

Name of the external system or social channel. For example, `Instagram` or `LinkedIn`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the party in the external system, such as a profile URL or handle.Data type: String

</td></tr><tr><td>

familyName

</td><td>

Last name of the individual.Data type: String

</td></tr><tr><td>

gender

</td><td>

Gender of the individual. Must match a choice value on the record. For a Contact created without a gender, the value is set to `Not Specified`.Data type: String

</td></tr><tr><td>

givenName

</td><td>

First name of the individual.Data type: String

</td></tr><tr><td>

href

</td><td>

Link to the Consumer or Contact record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the Consumer or Contact record. Always the sys\_id, even when the record has an external ID.Table: Consumer \[csm\_consumer\] or Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

name

</td><td>

User name of the individual. For a Contact, the user name must be unique.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics of the individual, such as notification and date format preferences.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String or Boolean",
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

Name of the characteristic.Possible values for a Consumer:

-   `dateFormat`
-   `notes`
-   `notification`
-   `preferredLanguage`
-   `timeFormat`
-   `timeZone`
-   `user`

Possible values for a Contact:

-   `dateFormat`
-   `eduStatus`
-   `notification`
-   `preferredLanguage`
-   `source`
-   `timeFormat`
-   `timeZone`
-   `vip`
-   `webServiceAccessOnly`

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic. Choice characteristics, such as `dateFormat` and `timeZone`, take the display value. An invalid choice value returns a warning.Data type: String, or Boolean for `vip` and `webServiceAccessOnly`

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `string`

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties related to the individual. A Consumer returns its linked user. A Contact returns its account.Data type: Array of Objects

```
"relatedParty": [
 {
  "@type": "String",
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

Type of the related party.Possible values:

-   `Account`: Account of a Contact.
-   `User`: User linked to a Consumer.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related party.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party record.Possible values:

-   `Individual`: Related party is a user.
-   `Organization`: Related party is an account.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related record. For a Contact's account, requests also accept the account's external\_id, and the response returns the sys\_id.Table: Depends on the role:

-   Account: Account \[customer\_account\]
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

-   `Account`: Account of a Contact.
-   `User`: User linked to a Consumer.

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

List of warning messages about parts of the request that couldn't be processed. The request still succeeds, but the record is created or updated without the invalid values. Returned only when a warning occurs.Data type: Array of Strings

</td></tr></tbody>
</table>### cURL request

The following example updates the Consumer record with sys\_id a1b2c3d4e5f6478990abcdef12345678 without replacing the entire resource.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v2/party/individual/a1b2c3d4e5f6478990abcdef12345678" \
  --request PATCH \
  --header "Accept: application/json" \
  --header "Content-Type: application/json" \
  --user 'user:password' \
  --data '{
  "@type": "Consumer",
  "givenName": "John",
  "middleName": "A.",
  "familyName": "Doe",
  "title": "Dr.",
  "gender": "Male",
  "nationality": "American",
  "status": "Active",
  "contactMedium": [
    {
      "preferred": true,
      "contactType": "email",
      "@type": "EmailContactMedium",
      "emailAddress": "john.doe@example.com"
    },
    {
      "preferred": false,
      "contactType": "mobilePhone",
      "@type": "MobilePhoneContactMedium",
      "phoneNumber": "+1-202-555-0111"
    },
    {
      "preferred": false,
      "contactType": "homePhone",
      "@type": "HomePhoneContactMedium",
      "phoneNumber": "+1-202-555-0112"
    },
    {
      "preferred": false,
      "contactType": "businessPhone",
      "@type": "BusinessPhoneContactMedium",
      "phoneNumber": "+1-202-555-0113"
    },
    {
      "preferred": false,
      "contactType": "faxPhone",
      "@type": "FaxContactMedium",
      "phoneNumber": "+1-202-555-0114"
    },
    {
      "preferred": false,
      "contactType": "postalAddress",
      "@type": "GeographicalAddressContactMedium",
      "street1": "240 Headquarters Plaza",
      "street2": "East Tower - 10th Floor",
      "city": "Morristown",
      "country": "US",
      "postCode": "07960",
      "stateOrProvince": "NJ"
    }
  ],
  "partyCharacteristic": [
    {
      "name": "notification",
      "value": "Disable",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "notes",
      "value": "Updated mailing address.",
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
      "value": "hh:mm:ss (24 hour)",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "timeZone",
      "value": "US/Eastern",
      "valueType": "string",
      "@type": "StringCharacteristic"
    }
  ]
}'
```

Response body.

```
{
  "id": "a1b2c3d4e5f6478990abcdef12345678",
  "href": "http://instance.service-now.com/api/sn_tmf_api/v2/party/individual/a1b2c3d4e5f6478990abcdef12345678",
  "@type": "Consumer",
  "givenName": "John",
  "middleName": "A.",
  "familyName": "Doe",
  "title": "Dr.",
  "gender": "Male",
  "nationality": "American",
  "status": "Active",
  "contactMedium": [
    {
      "preferred": true,
      "contactType": "email",
      "@type": "EmailContactMedium",
      "emailAddress": "john.doe@example.com"
    },
    {
      "preferred": false,
      "contactType": "mobilePhone",
      "@type": "MobilePhoneContactMedium",
      "phoneNumber": "+1-202-555-0111"
    },
    {
      "preferred": false,
      "contactType": "homePhone",
      "@type": "HomePhoneContactMedium",
      "phoneNumber": "+1-202-555-0112"
    },
    {
      "preferred": false,
      "contactType": "businessPhone",
      "@type": "BusinessPhoneContactMedium",
      "phoneNumber": "+1-202-555-0113"
    },
    {
      "preferred": false,
      "contactType": "faxPhone",
      "@type": "FaxContactMedium",
      "phoneNumber": "+1-202-555-0114"
    },
    {
      "preferred": false,
      "contactType": "postalAddress",
      "@type": "GeographicalAddressContactMedium",
      "locationId": "25ab9e240a0a0bb3009eb9ef8dd0a2c0",
      "street1": "240 Headquarters Plaza",
      "street2": "East Tower - 10th Floor",
      "city": "Morristown",
      "country": "US",
      "postCode": "07960",
      "stateOrProvince": "NJ"
    }
  ],
  "partyCharacteristic": [
    {
      "name": "notification",
      "value": "Disable",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "notes",
      "value": "Updated mailing address.",
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
      "value": "hh:mm:ss (24 hour)",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "timeZone",
      "value": "US/Eastern",
      "valueType": "string",
      "@type": "StringCharacteristic"
    }
  ]
}
```

## Party Management v2 - PATCH /api/sn\_tmf\_api/v2/party/organization/\{id\}

Updates an existing individual party record in the Account \[customer\_account\] tables without replacing the entire resource.

### URL format

Versioned URL: `/api/sn_tmf_api/{version_number}/party/organization/{id}`

Default URL: `/api/sn_tmf_api/v2/party/organization/{id}`

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

Sys\_id of the Account record to update. External IDs aren't accepted.Table: Account \[customer\_account\]

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="partymgmt-PATCH-org-id-v2-request-table" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Request object\}

</td><td>

Fields to update on the Account record. Include only the fields to change, plus the required **name** and **@type**.```
{
  "@type": "String",
  "externalId": "String",
  "name": "String",
  "legalName": "String",
  "tradingName": "String",
  "organizationType": "String",
  "status": "String",
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

Required. Type of organization record to create or update. Replaces the root **partyOrPartyRole** object from v1. Value must be `Account`. Any other value returns an error.Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of ways to contact the organization. Each entry requires **@type**, **contactType**, and **preferred**.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "contactType": "String",
  "country": "String",
  "emailAddress": "String",
  "latitude": "String",
  "locationId": "String",
  "longitude": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": Boolean,
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

-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicalAddressContactMedium`: Physical address.
-   `PhoneContactMedium`: Phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.contactType

</td><td>

Type of contact channel. Replaces the v1 **mediumType** parameter.Valid values:

-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `phone`: Phone number.
-   `postalAddress`: Physical address.

**Note:** Entries with any other value, such as `mobilePhone`, `businessPhone`, or `homePhone`, are ignored. The response doesn't return a warning for them.

Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address. Used when **contactType** is `email`.Data type: String

</td></tr><tr><td>

contactMedium.latitude

</td><td>

Latitude of the address.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id or external\_id of an existing location record to link to the organization. Used when **contactType** is `postalAddress`.How the location is handled:

-   If the locationId matches a location, the system links that location to the organization.
-   If the matching location belongs to a Consumer, the address is skipped and the response returns a warning.
-   If the locationId doesn't match a location, the system creates a new location from the address fields and saves the locationId as its external ID.
-   If you omit locationId, the system creates a new location from the address fields.

Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.longitude

</td><td>

Longitude of the address.Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number. Used when **contactType** is a phone or fax type.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Valid values:

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

Period during which the contact medium is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

contactMedium.validFor.startDateTime

</td><td>

Date and time from which the contact medium is valid, in ISO 8601 format. For example, `2017-03-15T07:49:25.246Z`.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Identifier of the record in your source system or third-party application. Leading and trailing spaces are removed, and a blank value is ignored.On a PATCH request, you can't clear an external ID once it's set. If you send a blank value for a record that already has one, the existing value is kept and the response includes a warning.

Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the organization in external systems, such as social profiles. Each entry requires **externalIdentifierType** and **id**.Data type: Array of Objects

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

Name of the external system or social channel. For example, `Instagram` or `LinkedIn`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the party in the external system, such as a profile URL or handle.Data type: String

</td></tr><tr><td>

legalName

</td><td>

Legal name of the organization.Data type: String

</td></tr><tr><td>

name

</td><td>

Required. Name of the organization.Data type: String

</td></tr><tr><td>

organizationChildRelationship

</td><td>

List of child organizations to relate to this organization, such as partner, subsidiary, or branch accounts. Each entry requires **relationshipType** and **organization**.Data type: Array of Objects

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

Details about the child organization. Requires **id**, **name**, and **@type**.Data type: Object

```
"organization": {
  "@type": "String",
  "id": "String",
  "name": "String"
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

Type of relationship between this organization and the child organization.In requests, the value is converted to lowercase and must match a relationship type defined in your instance. If no match is found, the response includes a warning. Available values depend on your instance configuration.

Table: Account Relationship Type \[sn\_customerservice\_account\_relationship\_type\]

Data type: String

</td></tr><tr><td>

organizationParentRelationship

</td><td>

Parent organization to relate to this organization. Requires **relationshipType** and **organization**.Data type: Object

```
"organizationParentRelationship": {
  "relationshipType": "String",
  "organization": {Object}
}
```

</td></tr><tr><td>

organizationParentRelationship.organization

</td><td>

Details about the parent organization. Requires **id**, **name**, and **@type**.Data type: Object

```
"organization": {
  "@type": "String",
  "id": "String",
  "name": "String"
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

Type of relationship between this organization and its parent.The value is converted to lowercase and must match a relationship type defined in your instance. If no match is found, the response includes a warning. Available values depend on your instance configuration.

Table: Account Relationship Type \[sn\_customerservice\_account\_relationship\_type\]

Data type: String

</td></tr><tr><td>

organizationType

</td><td>

Account classification of the organization. Replaces **partyOrPartyRole.name** from v1. To set more than one classification, join them with underscores. The value is converted to lowercase.Possible values:

-   `customer`
-   `manufacturer`
-   `partner`
-   `vendor`

For example, `customer_partner`.

Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics of the organization, such as industry and number of employees. Each entry requires **name**, **value**, **valueType**, and **@type**.Data type: Array of Objects

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
-   `customer`: Request only.
-   `identificationNumber`
-   `industry`
-   `manufacturer`: Request only.
-   `marketCap`
-   `notes`
-   `numEmployees`
-   `partner`: Request only.
-   `profits`
-   `publiclyTraded`
-   `rankTier`
-   `registrationCode`
-   `revenuePerYear`
-   `stockPrice`
-   `stockSymbol`
-   `taxId`
-   `vendor`: Request only.
-   `vendorType`
-   `website`

**Note:** For the `industry` and `rankTier` characteristics, provide the display value of the choice, such as `Manufacturing` or `Valued Partner`. An invalid value returns a warning.

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic. GET returns all values as strings, regardless of **valueType**. For example, `"false"` or `"10"`.Data type: String. Requests also accept a Boolean, or an Array of Strings for `vendorType`.

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `choice`
-   `currency`
-   `integer`
-   `list`
-   `string`
-   `url`

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts related to the organization. Omit this object to keep the current contacts. Each entry requires **role**, **@type** set to `contact`, and a **partyOrPartyRole** object with **id**, **name**, and **@type**.Data type: Array of Objects

```
"relatedParty": [
 {
  "@type": "String",
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

Type of the related party. Value is always `contact`. Required in each request entry.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related contact.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party record. For example, `Individual`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related contact record. Requests also accept the contact's external\_id.Table: Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the related contact.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related contact plays for the organization. The value isn't case-sensitive.Possible values:

-   `other`: Other contact for the organization.
-   `primaryContact`: Primary contact for the organization. If you send more than one, only the first is used.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the organization record. The value isn't case-sensitive.Valid values:

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

<table id="partymgmt-PATCH-org-id-v2-response-table"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Response object\}

</td><td>

Updated Account record. The response returns the fields sent in the request, plus the record's **id**, **href**, and dates.```
{
  "id": "String",
  "href": "String",
  "@type": "String",
  "externalId": "String",
  "name": "String",
  "legalName": "String",
  "tradingName": "String",
  "organizationType": "String",
  "status": "String",
  "createdDate": "String",
  "lastModifiedDate": "String",
  "contactMedium": [Array],
  "externalReference": [Array],
  "partyCharacteristic": [Array],
  "relatedParty": [Array],
  "organizationChildRelationship": [Array],
  "organizationParentRelationship": {Object},
  "warnings": [Array]
}
```

</td></tr><tr><td>

@type

</td><td>

Type of the organization record. Value is always `Account`.Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of ways to contact the organization, as sent in the request.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "contactType": "String",
  "country": "String",
  "emailAddress": "String",
  "latitude": "String",
  "locationId": "String",
  "longitude": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": Boolean,
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

-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicalAddressContactMedium`: Physical address.
-   `PhoneContactMedium`: Phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.contactType

</td><td>

Type of contact channel. Replaces the v1 **mediumType** parameter.Valid values:

-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `phone`: Phone number.
-   `postalAddress`: Physical address.

**Note:** Entries with any other value, such as `mobilePhone`, `businessPhone`, or `homePhone`, are ignored. The response doesn't return a warning for them.

Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address. Used when **contactType** is `email`.Data type: String

</td></tr><tr><td>

contactMedium.latitude

</td><td>

Latitude of the address.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location record linked to the address.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.longitude

</td><td>

Longitude of the address.Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number. Used when **contactType** is a phone or fax type.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Valid values:

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

Period during which the contact medium is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

contactMedium.validFor.startDateTime

</td><td>

Date and time from which the contact medium is valid, in ISO 8601 format. For example, `2017-03-15T07:49:25.246Z`.Data type: String

</td></tr><tr><td>

createdDate

</td><td>

Date and time when the organization record was created, in ISO 8601 format. For example, `2025-06-25T14:32:18.000Z`.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Identifier of the record in your source system or third-party application. Returned only when the record has an external ID.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the organization in external systems, as sent in the request.Data type: Array of Objects

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

Name of the external system or social channel. For example, `Instagram` or `LinkedIn`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the party in the external system, such as a profile URL or handle.Data type: String

</td></tr><tr><td>

href

</td><td>

Link to the Account record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the Account record. Always the sys\_id, even when the record has an external ID.Table: Account \[customer\_account\]

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

List of child organizations related to this organization, such as partner, subsidiary, or branch accounts.Data type: Array of Objects

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

Details about the child organization. Requires **id**, **name**, and **@type**.Data type: Object

```
"organization": {
  "@type": "String",
  "id": "String",
  "name": "String"
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

Type of relationship between this organization and the child organization.In requests, the value is converted to lowercase and must match a relationship type defined in your instance. If no match is found, the response includes a warning. Available values depend on your instance configuration.

Table: Account Relationship Type \[sn\_customerservice\_account\_relationship\_type\]

Data type: String

</td></tr><tr><td>

organizationParentRelationship

</td><td>

Parent organization of this organization. Empty if the organization has no parent.Data type: Object

```
"organizationParentRelationship": {
  "relationshipType": "String",
  "organization": {Object}
}
```

</td></tr><tr><td>

organizationParentRelationship.organization

</td><td>

Details about the parent organization. Requires **id**, **name**, and **@type**.Data type: Object

```
"organization": {
  "@type": "String",
  "id": "String",
  "name": "String"
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

Type of relationship between this organization and its parent.The value is converted to lowercase and must match a relationship type defined in your instance. If no match is found, the response includes a warning. Available values depend on your instance configuration.

Table: Account Relationship Type \[sn\_customerservice\_account\_relationship\_type\]

Data type: String

</td></tr><tr><td>

organizationType

</td><td>

Account classification of the organization, such as `customer` or `customer_partner`. Multiple classifications are joined with underscores, in the order customer, partner, vendor, manufacturer. Returned only when the account has at least one classification.Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics of the organization, such as industry and number of employees.Data type: Array of Objects

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
-   `customer`: Request only.
-   `identificationNumber`
-   `industry`
-   `manufacturer`: Request only.
-   `marketCap`
-   `notes`
-   `numEmployees`
-   `partner`: Request only.
-   `profits`
-   `publiclyTraded`
-   `rankTier`
-   `registrationCode`
-   `revenuePerYear`
-   `stockPrice`
-   `stockSymbol`
-   `taxId`
-   `vendor`: Request only.
-   `vendorType`
-   `website`

**Note:** For the `industry` and `rankTier` characteristics, provide the display value of the choice, such as `Manufacturing` or `Valued Partner`. An invalid value returns a warning.

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic. GET returns all values as strings, regardless of **valueType**. For example, `"false"` or `"10"`.Data type: String. Requests also accept a Boolean, or an Array of Strings for `vendorType`.

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `choice`
-   `currency`
-   `integer`
-   `list`
-   `string`
-   `url`

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts related to the organization, as sent in the request.Data type: Array of Objects

```
"relatedParty": [
 {
  "@type": "String",
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

Type of the related party. Value is always `contact`. Required in each request entry.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related contact.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party record. For example, `Individual`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related contact record. Requests also accept the contact's external\_id.Table: Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the related contact.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related contact plays for the organization. The value isn't case-sensitive.Possible values:

-   `other`: Other contact for the organization.
-   `primaryContact`: Primary contact for the organization. If you send more than one, only the first is used.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the organization record, as sent in the request.Data type: String

</td></tr><tr><td>

tradingName

</td><td>

Name that the organization trades under.Data type: String

</td></tr><tr><td>

warnings

</td><td>

List of warning messages about parts of the request that couldn't be processed. The request still succeeds, but the record is created or updated without the invalid values. Returned only when a warning occurs.Data type: Array of Strings

</td></tr></tbody>
</table>### cURL request

The following example updates the Account record with sys\_id a1b2c3d4e5f6478990abcdef12345678.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v2/party/organization/a1b2c3d4e5f6478990abcdef12345678" \
  --request PATCH \
  --header "Accept: application/json" \
  --header "Content-Type: application/json" \
  --user 'user:password' \
  --data '{
  "name": "SERVICENOW 144",
  "legalName": "Acme Corp Ltd.",
  "tradingName": "Acme Inc.",
  "contactMedium": [
    {
      "preferred": true,
      "contactType": "email",
      "emailAddress": "athammhd@email.com",
      "@type": "EmailContactMedium"
    },
    {
      "preferred": false,
      "contactType": "phone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "PhoneContactMedium"
    },
    {
      "preferred": false,
      "contactType": "faxPhone",
      "phoneNumber": "+1-202-555-0199",
      "@type": "FaxPhoneContactMedium"
    },
    {
      "preferred": false,
      "contactType": "postalAddress",
      "validFor": {
        "startDateTime": "2017-03-15T07:49:25.246Z"
      },
      "@type": "GeographicalAddressContactMedium",
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
      "name": "customer",
      "value": "true",
      "valueType": "boolean",
      "@type": "StringCharacteristics"
    },
    {
      "name": "registrationCode",
      "value": "003",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "vendorType",
      "value": ["Hardware"],
      "valueType": "array",
      "@type": "StringArrayCharacteristic"
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
      "name": "stockSymbol",
      "value": "Market",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "stockPrice",
      "value": "1000",
      "valueType": "string",
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
    },
    {
      "name": "marketCap",
      "value": "0",
      "valueType": "currency",
      "@type": "StringCharacteristics"
    },
    {
      "name": "profits",
      "value": "0",
      "valueType": "currency",
      "@type": "StringCharacteristics"
    },
    {
      "name": "revenuePerYear",
      "value": "0",
      "valueType": "currency",
      "@type": "StringCharacteristics"
    }
  ],
  "relatedParty": [
    {
      "role": "primaryContact",
      "@type": "contact",
      "partyOrPartyRole": {
        "id": "eaf68911c35420105252716b7d40ddde",
        "name": "John Doe",
        "@type": "Individual"
      }
    },
    {
      "role": "other",
      "@type": "contact",
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
    "relationshipType": "Account",
    "organization": {
      "id": "9e2fd2ee11b43110f877366201dea674",
      "name": "Global Holdings Ltd.",
      "@type": "Organization"
    }
  },
  "status": "active",
  "@type": "Account"
}'
```

Response body.

```
{
  "id": "a1b2c3d4e5f6478990abcdef12345678",
  "href": "http://instance.service-now.com/api/sn_tmf_api/v2/party/organization/a1b2c3d4e5f6478990abcdef12345678",
  "name": "SERVICENOW 144",
  "legalName": "Acme Corp Ltd.",
  "tradingName": "Acme Inc.",
  "contactMedium": [
    {
      "preferred": true,
      "contactType": "email",
      "emailAddress": "athammhd@email.com",
      "@type": "EmailContactMedium"
    },
    {
      "preferred": false,
      "contactType": "phone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "PhoneContactMedium"
    },
    {
      "preferred": false,
      "contactType": "faxPhone",
      "phoneNumber": "+1-202-555-0199",
      "@type": "FaxPhoneContactMedium"
    },
    {
      "preferred": false,
      "contactType": "postalAddress",
      "validFor": {
        "startDateTime": "2017-03-15T07:49:25.246Z"
      },
      "@type": "GeographicalAddressContactMedium",
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
      "name": "customer",
      "value": "true",
      "valueType": "boolean",
      "@type": "StringCharacteristics"
    },
    {
      "name": "registrationCode",
      "value": "003",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "vendorType",
      "value": ["Hardware"],
      "valueType": "array",
      "@type": "StringArrayCharacteristic"
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
      "name": "stockSymbol",
      "value": "Market",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "stockPrice",
      "value": "1000",
      "valueType": "string",
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
    },
    {
      "name": "marketCap",
      "value": "0",
      "valueType": "currency",
      "@type": "StringCharacteristics"
    },
    {
      "name": "profits",
      "value": "0",
      "valueType": "currency",
      "@type": "StringCharacteristics"
    },
    {
      "name": "revenuePerYear",
      "value": "0",
      "valueType": "currency",
      "@type": "StringCharacteristics"
    }
  ],
  "relatedParty": [
    {
      "role": "primaryContact",
      "@type": "contact",
      "partyOrPartyRole": {
        "id": "eaf68911c35420105252716b7d40ddde",
        "name": "John Doe",
        "@type": "Individual"
      }
    },
    {
      "role": "other",
      "@type": "contact",
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
    "relationshipType": "Account",
    "organization": {
      "id": "9e2fd2ee11b43110f877366201dea674",
      "name": "Global Holdings Ltd.",
      "@type": "Organization"
    }
  },
  "status": "active",
  "@type": "Account",
  "createdDate": "2025-06-25T14:32:18.000Z",
  "lastModifiedDate": "2026-11-05T10:15:42.000Z"
}
```

## Party Management v2 - POST /api/sn\_tmf\_api/v2/party/individual

Creates a new individual party management record in the Consumer \[csm\_consumer\] or Contact \[customer\_contact\] tables.

### URL format

Versioned URL: `/api/sn_tmf_api/{version_number}/party/individual`

Default URL: `/api/sn_tmf_api/v2/party/individual`

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

<table id="partymgmt-POST-individual-v2-request-table" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Request object\}

</td><td>

Consumer or Contact record to create. Requires **@type**, **givenName**, and **familyName**. A Contact also requires an email entry in **contactMedium** and an account in **relatedParty**.```
{
  "@type": "String",
  "externalId": "String",
  "name": "String",
  "givenName": "String",
  "middleName": "String",
  "familyName": "String",
  "gender": "String",
  "nationality": "String",
  "title": "String",
  "status": "String",
  "contactMedium": [Array],
  "externalReference": [Array],
  "partyCharacteristic": [Array],
  "relatedParty": [Array]
}
```

</td></tr><tr><td>

@type

</td><td>

Required. Type of individual record to create or update. Replaces the root **partyOrPartyRole** object from v1. The value isn't case-sensitive.Valid values:

-   `Consumer`: Consumer record.
-   `Contact`: Contact record.

Any other value, including `Account`, returns an error.

Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of ways to contact the individual.For a Contact, a POST request must include an entry with **contactType** set to `email` and a valid **emailAddress**.

Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "contactType": "String",
  "country": "String",
  "emailAddress": "String",
  "locationId": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": Boolean,
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
-   `FaxContactMedium`: Fax number.
-   `GeographicalAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `MobilePhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.contactType

</td><td>

Type of contact channel. Replaces the v1 **mediumType** parameter.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address. Used when **contactType** is `email`.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id or external\_id of an existing location record to link to the individual. Used when **contactType** is `postalAddress`.How the location is handled depends on the record type:

-   Consumer: If you provide a locationId that doesn't exist, the system creates a new location from the address fields and returns a warning. If you omit locationId, the system creates a new location from the address fields.
-   Contact: The locationId must match an existing location. If it doesn't, the address is skipped and the response returns a warning.

Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number. Used when **contactType** is a phone or fax type.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Valid values:

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

Period during which the contact medium is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

contactMedium.validFor.startDateTime

</td><td>

Date and time from which the contact medium is valid, in ISO 8601 format. For example, `2017-03-15T07:49:25.246Z`.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Identifier of the record in your source system or third-party application. Leading and trailing spaces are removed, and a blank value is ignored.On a PATCH request, you can't clear an external ID once it's set. If you send a blank value for a record that already has one, the existing value is kept and the response includes a warning.

Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the individual in external systems, such as social profiles. Each entry requires **externalIdentifierType** and **id**.Data type: Array of Objects

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

Name of the external system or social channel. For example, `Instagram` or `LinkedIn`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the party in the external system, such as a profile URL or handle.Data type: String

</td></tr><tr><td>

familyName

</td><td>

Required. Last name of the individual.Data type: String

</td></tr><tr><td>

gender

</td><td>

Gender of the individual. Must match a choice value on the record. For a Contact created without a gender, the value is set to `Not Specified`.Data type: String

</td></tr><tr><td>

givenName

</td><td>

Required. First name of the individual.Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

name

</td><td>

User name of the individual. For a Contact, the user name must be unique.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics of the individual, such as notification and date format preferences. Each entry requires **name**, **valueType**, and **@type**.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String or Boolean",
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

Name of the characteristic.Possible values for a Consumer:

-   `dateFormat`
-   `notes`
-   `notification`
-   `preferredLanguage`
-   `timeFormat`
-   `timeZone`
-   `user`

Possible values for a Contact:

-   `dateFormat`
-   `eduStatus`
-   `notification`
-   `preferredLanguage`
-   `source`
-   `timeFormat`
-   `timeZone`
-   `vip`
-   `webServiceAccessOnly`

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic. Choice characteristics, such as `dateFormat` and `timeZone`, take the display value. An invalid choice value returns a warning.Data type: String, or Boolean for `vip` and `webServiceAccessOnly`

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `string`

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties related to the individual. The rules depend on the record type:-   Consumer: Optional. Use the `User` role to link a user. Each `User` entry requires **@type** set to `User`, or the request fails. Entries with any other role are ignored and return a warning.
-   Contact: Required on POST. Must include an entry with the `Account` role, **@type** set to `Account`, and a **partyOrPartyRole** object with **@type** and the **id** of an existing account. Only the first `Account` entry is used. On PATCH, omit this object to keep the current account. An empty array returns an error.

Data type: Array of Objects

```
"relatedParty": [
 {
  "@type": "String",
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

Type of the related party.Possible values:

-   `Account`: Account of a Contact.
-   `User`: User linked to a Consumer.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related party.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party record.Possible values:

-   `Individual`: Related party is a user.
-   `Organization`: Related party is an account.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related record. For a Contact's account, requests also accept the account's external\_id, and the response returns the sys\_id.Table: Depends on the role:

-   Account: Account \[customer\_account\]
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

-   `Account`: Account of a Contact.
-   `User`: User linked to a Consumer.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the individual record. The value isn't case-sensitive. Any value other than `inactive` sets the record to active.Valid values:

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

<table id="partymgmt-POST-individual-v2-response-table"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Response object\}

</td><td>

New Consumer or Contact record. The response returns the fields sent in the request, plus the record's **id** and **href**.```
{
  "id": "String",
  "href": "String",
  "@type": "String",
  "externalId": "String",
  "name": "String",
  "givenName": "String",
  "middleName": "String",
  "familyName": "String",
  "gender": "String",
  "nationality": "String",
  "title": "String",
  "status": "String",
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

-   `Consumer`
-   `Contact`

Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of ways to contact the individual, as sent in the request. Address entries include the **locationId** of the linked location.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "contactType": "String",
  "country": "String",
  "emailAddress": "String",
  "locationId": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": Boolean,
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
-   `FaxContactMedium`: Fax number.
-   `GeographicalAddressContactMedium`: Physical address.
-   `HomePhoneContactMedium`: Home phone number.
-   `MobilePhoneContactMedium`: Mobile phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.contactType

</td><td>

Type of contact channel. Replaces the v1 **mediumType** parameter.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.
-   `postalAddress`: Physical address.

Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address. Used when **contactType** is `email`.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location record linked to the address.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number. Used when **contactType** is a phone or fax type.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Valid values:

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

Period during which the contact medium is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

contactMedium.validFor.startDateTime

</td><td>

Date and time from which the contact medium is valid, in ISO 8601 format. For example, `2017-03-15T07:49:25.246Z`.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Identifier of the record in your source system or third-party application. Returned only when the record has an external ID.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the individual in external systems, as sent in the request.Data type: Array of Objects

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

Name of the external system or social channel. For example, `Instagram` or `LinkedIn`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the party in the external system, such as a profile URL or handle.Data type: String

</td></tr><tr><td>

familyName

</td><td>

Last name of the individual.Data type: String

</td></tr><tr><td>

gender

</td><td>

Gender of the individual. Must match a choice value on the record. For a Contact created without a gender, the value is set to `Not Specified`.Data type: String

</td></tr><tr><td>

givenName

</td><td>

First name of the individual.Data type: String

</td></tr><tr><td>

href

</td><td>

Link to the Consumer or Contact record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the Consumer or Contact record. Always the sys\_id, even when the record has an external ID.Table: Consumer \[csm\_consumer\] or Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

name

</td><td>

User name of the individual. For a Contact, the user name must be unique.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics of the individual, such as notification and date format preferences.Data type: Array of Objects

```
"partyCharacteristic": [
 {
  "@type": "String",
  "name": "String",
  "value": "String or Boolean",
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

Name of the characteristic.Possible values for a Consumer:

-   `dateFormat`
-   `notes`
-   `notification`
-   `preferredLanguage`
-   `timeFormat`
-   `timeZone`
-   `user`

Possible values for a Contact:

-   `dateFormat`
-   `eduStatus`
-   `notification`
-   `preferredLanguage`
-   `source`
-   `timeFormat`
-   `timeZone`
-   `vip`
-   `webServiceAccessOnly`

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic. Choice characteristics, such as `dateFormat` and `timeZone`, take the display value. An invalid choice value returns a warning.Data type: String, or Boolean for `vip` and `webServiceAccessOnly`

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `string`

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties related to the individual. A Consumer returns its linked user. A Contact returns its account.Data type: Array of Objects

```
"relatedParty": [
 {
  "@type": "String",
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

Type of the related party.Possible values:

-   `Account`: Account of a Contact.
-   `User`: User linked to a Consumer.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related party.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party record.Possible values:

-   `Individual`: Related party is a user.
-   `Organization`: Related party is an account.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related record. For a Contact's account, requests also accept the account's external\_id, and the response returns the sys\_id.Table: Depends on the role:

-   Account: Account \[customer\_account\]
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

-   `Account`: Account of a Contact.
-   `User`: User linked to a Consumer.

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

List of warning messages about parts of the request that couldn't be processed. The request still succeeds, but the record is created or updated without the invalid values. Returned only when a warning occurs.Data type: Array of Strings

</td></tr></tbody>
</table>### cURL request

The following example creates a Consumer record and creates a location from the postal address.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v2/party/individual" \
  --request POST \
  --header "Accept: application/json" \
  --header "Content-Type: application/json" \
  --user 'user:password' \
  --data '{
  "@type": "Consumer",
  "externalId": "CONS-10045",
  "givenName": "Robert",
  "middleName": "A.",
  "familyName": "Smith",
  "title": "Mr.",
  "gender": "Male",
  "nationality": "American",
  "status": "Active",
  "contactMedium": [
    {
      "preferred": true,
      "contactType": "email",
      "@type": "EmailContactMedium",
      "emailAddress": "robert.smith@example.com"
    },
    {
      "preferred": false,
      "contactType": "mobilePhone",
      "@type": "MobilePhoneContactMedium",
      "phoneNumber": "+1-214-555-0101"
    },
    {
      "preferred": false,
      "contactType": "homePhone",
      "@type": "HomePhoneContactMedium",
      "phoneNumber": "+1-214-555-0102"
    },
    {
      "preferred": false,
      "contactType": "businessPhone",
      "@type": "BusinessPhoneContactMedium",
      "phoneNumber": "+1-214-555-0103"
    },
    {
      "preferred": false,
      "contactType": "faxPhone",
      "@type": "FaxContactMedium",
      "phoneNumber": "+1-214-555-0104"
    },
    {
      "preferred": false,
      "contactType": "postalAddress",
      "@type": "GeographicalAddressContactMedium",
      "street1": "9 Elm St",
      "street2": "Apt 3",
      "city": "Dallas",
      "country": "US",
      "postCode": "75001",
      "stateOrProvince": "TX"
    }
  ],
  "partyCharacteristic": [
    {
      "name": "notification",
      "value": "Enable",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "notes",
      "value": "Prefers email contact.",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "dateFormat",
      "value": "dd/mm/yyyy",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "timeFormat",
      "value": "hh.mm.ss (24 hour)",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "timeZone",
      "value": "US/Central",
      "valueType": "string",
      "@type": "StringCharacteristic"
    }
  ],
  "externalReference": [
    {
      "externalIdentifierType": "Instagram",
      "id": "robert.smith"
    }
  ]
}'
```

Response body.

```
{
  "id": "83e588a17b6062105e0d5494548cb65d",
  "href": "http://instance.service-now.com/api/sn_tmf_api/v2/party/individual/83e588a17b6062105e0d5494548cb65d",
  "@type": "Consumer",
  "externalId": "CONS-10045",
  "givenName": "Robert",
  "middleName": "A.",
  "familyName": "Smith",
  "title": "Mr.",
  "gender": "Male",
  "nationality": "American",
  "status": "Active",
  "contactMedium": [
    {
      "preferred": true,
      "contactType": "email",
      "@type": "EmailContactMedium",
      "emailAddress": "robert.smith@example.com"
    },
    {
      "preferred": false,
      "contactType": "mobilePhone",
      "@type": "MobilePhoneContactMedium",
      "phoneNumber": "+1-214-555-0101"
    },
    {
      "preferred": false,
      "contactType": "homePhone",
      "@type": "HomePhoneContactMedium",
      "phoneNumber": "+1-214-555-0102"
    },
    {
      "preferred": false,
      "contactType": "businessPhone",
      "@type": "BusinessPhoneContactMedium",
      "phoneNumber": "+1-214-555-0103"
    },
    {
      "preferred": false,
      "contactType": "faxPhone",
      "@type": "FaxContactMedium",
      "phoneNumber": "+1-214-555-0104"
    },
    {
      "preferred": false,
      "contactType": "postalAddress",
      "@type": "GeographicalAddressContactMedium",
      "locationId": "03e588a17be062105e0d5494548cb68c",
      "street1": "9 Elm St",
      "street2": "Apt 3",
      "city": "Dallas",
      "country": "US",
      "postCode": "75001",
      "stateOrProvince": "TX"
    }
  ],
  "partyCharacteristic": [
    {
      "name": "notification",
      "value": "Enable",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "notes",
      "value": "Prefers email contact.",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "dateFormat",
      "value": "dd/mm/yyyy",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "timeFormat",
      "value": "hh.mm.ss (24 hour)",
      "valueType": "string",
      "@type": "StringCharacteristic"
    },
    {
      "name": "timeZone",
      "value": "US/Central",
      "valueType": "string",
      "@type": "StringCharacteristic"
    }
  ],
  "externalReference": [
    {
      "externalIdentifierType": "Instagram",
      "id": "robert.smith"
    }
  ]
}
```

## Party Management v2 - POST /api/sn\_tmf\_api/v2/party/organization

Creates a new party organization record in the Account \[customer\_account\] tables. You can also create and associate Contact and Location records inline during organization creation, eliminating the need for separate POST operations.

### Automatic Location Creation with contactMedium

When you include address information in the **contactMedium** field \(with **@type** set to `GeographicalAddressContactMedium`\), the system automatically handles location creation and association based on what you provide:

1.  If you supply a valid locationId, the system links the existing location record to the organization you are creating.
2.  If you provide address attributes \(street, city, country, postCode, stateOrProvince\) along with an invalid or non-existent locationId, the system automatically creates a new location record with those attributes and associates it to the organization.
3.  If you provide address attributes without specifying a locationId at all, the system creates a new location record and associates it to the organization.

**Note:** Location creation requires no mandatory fields. You can provide any combination of address attributes \(street1, street2, city, state, postCode, country\) based on your needs. If you omit all address attributes from the contactMedium section, no location record is created or linked to the organization.

### Inline Contact Creation with relatedParty

When you include contact attributes in the **relatedParty** field without providing a contact ID, the system automatically creates a new contact record and associates it to the organization you are creating. This eliminates the need for a separate POST request to create the contact first. You can include the following contact information directly in the **relatedParty.partyOrPartyRole** object.

Mandatory attributes for inline contact creation:

-   familyName
-   contactMedium entry with contactType set to email and a valid emailAddress

Optional attributes:

-   givenName
-   contactMedium entries for businessPhone, homePhone, or mobilePhone

Example: Creating a contact inline without a pre-existing ID.

```
{
  "relatedParty": [
    {
      "role": "primaryContact",
      "@type": "contact",
      "partyOrPartyRole": {
        "givenName": "John",
        "familyName": "Doe",
        "contactMedium": [
          {
            "contactType": "email",
            "emailAddress": "john.doe@example.com",
            "@type": "EmailContactMedium"
          }
        ],
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
      "@type": "contact",
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

Versioned URL: `/api/sn_tmf_api/{version_number}/party/organization`

Default URL: `/api/sn_tmf_api/v2/party/organization`

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

<table id="partymgmt-POST-org-v2-request-table" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Request object\}

</td><td>

Account record to create. Requires **name** and **@type**.```
{
  "@type": "String",
  "externalId": "String",
  "name": "String",
  "legalName": "String",
  "tradingName": "String",
  "organizationType": "String",
  "status": "String",
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

Required. Type of organization record to create or update. Replaces the root **partyOrPartyRole** object from v1. Value must be `Account`. Any other value returns an error.Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of ways to contact the organization. Each entry requires **@type**, **contactType**, and **preferred**.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "contactType": "String",
  "country": "String",
  "emailAddress": "String",
  "latitude": "String",
  "locationId": "String",
  "longitude": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": Boolean,
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

-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicalAddressContactMedium`: Physical address.
-   `PhoneContactMedium`: Phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.contactType

</td><td>

Type of contact channel. Replaces the v1 **mediumType** parameter.Valid values:

-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `phone`: Phone number.
-   `postalAddress`: Physical address.

**Note:** Entries with any other value, such as `mobilePhone`, `businessPhone`, or `homePhone`, are ignored. The response doesn't return a warning for them.

Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address. Used when **contactType** is `email`.Data type: String

</td></tr><tr><td>

contactMedium.latitude

</td><td>

Latitude of the address.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id or external\_id of an existing location record to link to the organization. Used when **contactType** is `postalAddress`.How the location is handled:

-   If the locationId matches a location, the system links that location to the organization.
-   If the matching location belongs to a Consumer, the address is skipped and the response returns a warning.
-   If the locationId doesn't match a location, the system creates a new location from the address fields and saves the locationId as its external ID.
-   If you omit locationId, the system creates a new location from the address fields.

Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.longitude

</td><td>

Longitude of the address.Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number. Used when **contactType** is a phone or fax type.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Valid values:

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

Period during which the contact medium is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

contactMedium.validFor.startDateTime

</td><td>

Date and time from which the contact medium is valid, in ISO 8601 format. For example, `2017-03-15T07:49:25.246Z`.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Identifier of the record in your source system or third-party application. Leading and trailing spaces are removed, and a blank value is ignored.On a PATCH request, you can't clear an external ID once it's set. If you send a blank value for a record that already has one, the existing value is kept and the response includes a warning.

Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the organization in external systems, such as social profiles. Each entry requires **externalIdentifierType** and **id**.Data type: Array of Objects

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

Name of the external system or social channel. For example, `Instagram` or `LinkedIn`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the party in the external system, such as a profile URL or handle.Data type: String

</td></tr><tr><td>

legalName

</td><td>

Legal name of the organization.Data type: String

</td></tr><tr><td>

name

</td><td>

Required. Name of the organization.Data type: String

</td></tr><tr><td>

organizationChildRelationship

</td><td>

List of child organizations to relate to this organization, such as partner, subsidiary, or branch accounts. Each entry requires **relationshipType** and **organization**.Data type: Array of Objects

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

Details about the child organization. Requires **id**, **name**, and **@type**.Data type: Object

```
"organization": {
  "@type": "String",
  "id": "String",
  "name": "String"
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

Type of relationship between this organization and the child organization.In requests, the value is converted to lowercase and must match a relationship type defined in your instance. If no match is found, the response includes a warning. Available values depend on your instance configuration.

Table: Account Relationship Type \[sn\_customerservice\_account\_relationship\_type\]

Data type: String

</td></tr><tr><td>

organizationParentRelationship

</td><td>

Parent organization to relate to this organization. Requires **relationshipType** and **organization**.Data type: Object

```
"organizationParentRelationship": {
  "relationshipType": "String",
  "organization": {Object}
}
```

</td></tr><tr><td>

organizationParentRelationship.organization

</td><td>

Details about the parent organization. Requires **id**, **name**, and **@type**.Data type: Object

```
"organization": {
  "@type": "String",
  "id": "String",
  "name": "String"
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

Type of relationship between this organization and its parent.The value is converted to lowercase and must match a relationship type defined in your instance. If no match is found, the response includes a warning. Available values depend on your instance configuration.

Table: Account Relationship Type \[sn\_customerservice\_account\_relationship\_type\]

Data type: String

</td></tr><tr><td>

organizationType

</td><td>

Account classification of the organization. Replaces **partyOrPartyRole.name** from v1. To set more than one classification, join them with underscores. The value is converted to lowercase.Possible values:

-   `customer`
-   `manufacturer`
-   `partner`
-   `vendor`

For example, `customer_partner`.

Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics of the organization, such as industry and number of employees. Each entry requires **name**, **value**, **valueType**, and **@type**.Data type: Array of Objects

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
-   `customer`: Request only.
-   `identificationNumber`
-   `industry`
-   `manufacturer`: Request only.
-   `marketCap`
-   `notes`
-   `numEmployees`
-   `partner`: Request only.
-   `profits`
-   `publiclyTraded`
-   `rankTier`
-   `registrationCode`
-   `revenuePerYear`
-   `stockPrice`
-   `stockSymbol`
-   `taxId`
-   `vendor`: Request only.
-   `vendorType`
-   `website`

**Note:** For the `industry` and `rankTier` characteristics, provide the display value of the choice, such as `Manufacturing` or `Valued Partner`. An invalid value returns a warning.

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic. GET returns all values as strings, regardless of **valueType**. For example, `"false"` or `"10"`.Data type: String. Requests also accept a Boolean, or an Array of Strings for `vendorType`.

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `choice`
-   `currency`
-   `integer`
-   `list`
-   `string`
-   `url`

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts to relate to the organization. Each entry requires **role** and **@type** set to `contact`.For each entry, the system links or creates a contact based on what you provide in **partyOrPartyRole**:

-   If the **id** matches an existing contact, the system links that contact to the organization.
-   If you omit **id**, or it doesn't match a contact, the system creates a new contact from **familyName**, **givenName**, and **contactMedium**. A supplied **id** is saved as the new contact's external ID.
-   If a new contact is missing **familyName** or a valid email entry in **contactMedium**, the contact isn't created and the response returns a warning.

Data type: Array of Objects

```
"relatedParty": [
 {
  "@type": "String",
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

Type of the related party. Value is always `contact`. Required in each request entry.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the contact to link or create. To link an existing contact, provide **id**. To create a new contact, provide **familyName** and a **contactMedium** entry with an email address.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "contactMedium": [Array],
  "familyName": "String",
  "givenName": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party record. For example, `Individual`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.contactMedium

</td><td>

List of contact details for a new contact. Must include an entry with **contactType** set to `email` and a valid **emailAddress**. Address entries are ignored, and invalid email addresses or phone numbers return a warning.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "contactType": "String",
  "emailAddress": "String",
  "phoneNumber": "String"
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.contactMedium.@type

</td><td>

Schema or subclass type of the contact medium. For example, `EmailContactMedium`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.contactMedium.contactType

</td><td>

Type of contact channel.Possible values:

-   `businessPhone`: Business phone number.
-   `email`: Email address.
-   `homePhone`: Home phone number.
-   `mobilePhone`: Mobile phone number.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.contactMedium.emailAddress

</td><td>

Email address of the new contact. Used when **contactType** is `email`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.contactMedium.phoneNumber

</td><td>

Phone number of the new contact. Used when **contactType** is a phone type.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.familyName

</td><td>

Last name of the new contact. Required to create a contact inline.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.givenName

</td><td>

First name of the new contact.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related contact record. Requests also accept the contact's external\_id.Table: Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the related contact.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related contact plays for the organization. The value isn't case-sensitive.Possible values:

-   `other`: Other contact for the organization.
-   `primaryContact`: Primary contact for the organization. If you send more than one, only the first is used.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the organization record. The value isn't case-sensitive.Valid values:

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

Successful. The request was successfully processed.**Note:** Response may include a **warnings** array if:

-   Invalid **relatedParty** IDs are provided \(related contact or party doesn't exist\).
-   Invalid **locationId** is provided in **contactMedium**. Example warning: `relatedParty[0] is incorrect. User does not exist`.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="partymgmt-POST-org-v2-response-table"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{Response object\}

</td><td>

New Account record. The response returns the fields sent in the request, plus the record's **id**, **href**, and dates. Contacts that were linked or created inline include their sys\_id in **relatedParty.partyOrPartyRole.id**.```
{
  "id": "String",
  "href": "String",
  "@type": "String",
  "externalId": "String",
  "name": "String",
  "legalName": "String",
  "tradingName": "String",
  "organizationType": "String",
  "status": "String",
  "createdDate": "String",
  "lastModifiedDate": "String",
  "contactMedium": [Array],
  "externalReference": [Array],
  "partyCharacteristic": [Array],
  "relatedParty": [Array],
  "organizationChildRelationship": [Array],
  "organizationParentRelationship": {Object},
  "warnings": [Array]
}
```

</td></tr><tr><td>

@type

</td><td>

Type of the organization record. Value is always `Account`.Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of ways to contact the organization, as sent in the request.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "city": "String",
  "contactType": "String",
  "country": "String",
  "emailAddress": "String",
  "latitude": "String",
  "locationId": "String",
  "longitude": "String",
  "phoneNumber": "String",
  "postCode": "String",
  "preferred": Boolean,
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

-   `EmailContactMedium`: Email address.
-   `FaxPhoneContactMedium`: Fax number.
-   `GeographicalAddressContactMedium`: Physical address.
-   `PhoneContactMedium`: Phone number.

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the address.Data type: String

</td></tr><tr><td>

contactMedium.contactType

</td><td>

Type of contact channel. Replaces the v1 **mediumType** parameter.Valid values:

-   `email`: Email address.
-   `faxPhone`: Fax number.
-   `phone`: Phone number.
-   `postalAddress`: Physical address.

**Note:** Entries with any other value, such as `mobilePhone`, `businessPhone`, or `homePhone`, are ignored. The response doesn't return a warning for them.

Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the address.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address. Used when **contactType** is `email`.Data type: String

</td></tr><tr><td>

contactMedium.latitude

</td><td>

Latitude of the address.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location record linked to the address.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.longitude

</td><td>

Longitude of the address.Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone or fax number. Used when **contactType** is a phone or fax type.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the address.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

Flag that indicates whether this is the preferred contact medium.Valid values:

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

Period during which the contact medium is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

contactMedium.validFor.startDateTime

</td><td>

Date and time from which the contact medium is valid, in ISO 8601 format. For example, `2017-03-15T07:49:25.246Z`.Data type: String

</td></tr><tr><td>

createdDate

</td><td>

Date and time when the organization record was created, in ISO 8601 format. For example, `2025-06-25T14:32:18.000Z`.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Identifier of the record in your source system or third-party application. Returned only when the record has an external ID.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the organization in external systems, as sent in the request.Data type: Array of Objects

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

Name of the external system or social channel. For example, `Instagram` or `LinkedIn`.Data type: String

</td></tr><tr><td>

externalReference.id

</td><td>

Identifier of the party in the external system, such as a profile URL or handle.Data type: String

</td></tr><tr><td>

href

</td><td>

Link to the Account record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the Account record. Always the sys\_id, even when the record has an external ID.Table: Account \[customer\_account\]

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

List of child organizations related to this organization, such as partner, subsidiary, or branch accounts.Data type: Array of Objects

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

Details about the child organization. Requires **id**, **name**, and **@type**.Data type: Object

```
"organization": {
  "@type": "String",
  "id": "String",
  "name": "String"
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

Type of relationship between this organization and the child organization.In requests, the value is converted to lowercase and must match a relationship type defined in your instance. If no match is found, the response includes a warning. Available values depend on your instance configuration.

Table: Account Relationship Type \[sn\_customerservice\_account\_relationship\_type\]

Data type: String

</td></tr><tr><td>

organizationParentRelationship

</td><td>

Parent organization of this organization. Empty if the organization has no parent.Data type: Object

```
"organizationParentRelationship": {
  "relationshipType": "String",
  "organization": {Object}
}
```

</td></tr><tr><td>

organizationParentRelationship.organization

</td><td>

Details about the parent organization. Requires **id**, **name**, and **@type**.Data type: Object

```
"organization": {
  "@type": "String",
  "id": "String",
  "name": "String"
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

Type of relationship between this organization and its parent.The value is converted to lowercase and must match a relationship type defined in your instance. If no match is found, the response includes a warning. Available values depend on your instance configuration.

Table: Account Relationship Type \[sn\_customerservice\_account\_relationship\_type\]

Data type: String

</td></tr><tr><td>

organizationType

</td><td>

Account classification of the organization, such as `customer` or `customer_partner`. Multiple classifications are joined with underscores, in the order customer, partner, vendor, manufacturer. Returned only when the account has at least one classification.Data type: String

</td></tr><tr><td>

partyCharacteristic

</td><td>

List of characteristics of the organization, such as industry and number of employees.Data type: Array of Objects

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
-   `customer`: Request only.
-   `identificationNumber`
-   `industry`
-   `manufacturer`: Request only.
-   `marketCap`
-   `notes`
-   `numEmployees`
-   `partner`: Request only.
-   `profits`
-   `publiclyTraded`
-   `rankTier`
-   `registrationCode`
-   `revenuePerYear`
-   `stockPrice`
-   `stockSymbol`
-   `taxId`
-   `vendor`: Request only.
-   `vendorType`
-   `website`

**Note:** For the `industry` and `rankTier` characteristics, provide the display value of the choice, such as `Manufacturing` or `Valued Partner`. An invalid value returns a warning.

Data type: String

</td></tr><tr><td>

partyCharacteristic.value

</td><td>

Value of the characteristic. GET returns all values as strings, regardless of **valueType**. For example, `"false"` or `"10"`.Data type: String. Requests also accept a Boolean, or an Array of Strings for `vendorType`.

</td></tr><tr><td>

partyCharacteristic.valueType

</td><td>

Data type of the characteristic's value.Possible values:

-   `boolean`
-   `choice`
-   `currency`
-   `integer`
-   `list`
-   `string`
-   `url`

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts related to the organization, as sent in the request.Data type: Array of Objects

```
"relatedParty": [
 {
  "@type": "String",
  "role": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

Type of the related party. Value is always `contact`. Required in each request entry.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Details about the related contact, as sent in the request. For a contact that was linked or created, **id** holds the contact's sys\_id.Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "contactMedium": [Array],
  "familyName": "String",
  "givenName": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party record. For example, `Individual`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.contactMedium

</td><td>

List of contact details for an inline contact, as sent in the request.Data type: Array of Objects

```
"contactMedium": [
 {
  "@type": "String",
  "contactType": "String",
  "emailAddress": "String",
  "phoneNumber": "String"
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.familyName

</td><td>

Last name of an inline contact, as sent in the request.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.givenName

</td><td>

First name of an inline contact, as sent in the request.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related contact record. Requests also accept the contact's external\_id.Table: Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Display name of the related contact.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role that the related contact plays for the organization. The value isn't case-sensitive.Possible values:

-   `other`: Other contact for the organization.
-   `primaryContact`: Primary contact for the organization. If you send more than one, only the first is used.

Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the organization record, as sent in the request.Data type: String

</td></tr><tr><td>

tradingName

</td><td>

Name that the organization trades under.Data type: String

</td></tr><tr><td>

warnings

</td><td>

List of warning messages about parts of the request that couldn't be processed. The request still succeeds, but the record is created or updated without the invalid values. Returned only when a warning occurs.Data type: Array of Strings

</td></tr></tbody>
</table>### cURL request

The following example creates an Account record, creates a location from the postal address, and creates two contacts inline.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v2/party/organization" \
  --request POST \
  --header "Accept: application/json" \
  --header "Content-Type: application/json" \
  --user 'user:password' \
  --data '{
  "name": "SERVICENOW 144",
  "legalName": "Acme Corp Ltd.",
  "tradingName": "Acme Inc.",
  "contactMedium": [
    {
      "preferred": true,
      "contactType": "email",
      "emailAddress": "athammhd@email.com",
      "@type": "EmailContactMedium"
    },
    {
      "preferred": false,
      "contactType": "phone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "PhoneContactMedium"
    },
    {
      "preferred": false,
      "contactType": "faxPhone",
      "phoneNumber": "+1-202-555-0199",
      "@type": "FaxPhoneContactMedium"
    },
    {
      "preferred": false,
      "contactType": "postalAddress",
      "validFor": {
        "startDateTime": "2017-03-15T07:49:25.246Z"
      },
      "@type": "GeographicalAddressContactMedium",
      "locationId": "12345678901234567",
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
      "name": "customer",
      "value": "true",
      "valueType": "boolean",
      "@type": "StringCharacteristics"
    },
    {
      "name": "registrationCode",
      "value": "003",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "vendorType",
      "value": ["Hardware"],
      "valueType": "array",
      "@type": "StringArrayCharacteristic"
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
      "name": "stockSymbol",
      "value": "Market",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "stockPrice",
      "value": "1000",
      "valueType": "string",
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
    },
    {
      "name": "marketCap",
      "value": "0",
      "valueType": "currency",
      "@type": "StringCharacteristics"
    },
    {
      "name": "profits",
      "value": "0",
      "valueType": "currency",
      "@type": "StringCharacteristics"
    },
    {
      "name": "revenuePerYear",
      "value": "0",
      "valueType": "currency",
      "@type": "StringCharacteristics"
    }
  ],
  "relatedParty": [
    {
      "role": "primaryContact",
      "@type": "contact",
      "partyOrPartyRole": {
        "givenName": "John",
        "familyName": "Doe",
        "contactMedium": [
          {
            "contactType": "email",
            "emailAddress": "john.doe@example.com",
            "@type": "EmailContactMedium"
          }
        ],
        "@type": "Individual"
      }
    },
    {
      "role": "other",
      "@type": "contact",
      "partyOrPartyRole": {
        "givenName": "Mary",
        "familyName": "Star",
        "contactMedium": [
          {
            "contactType": "email",
            "emailAddress": "mary.star@example.com",
            "@type": "EmailContactMedium"
          }
        ],
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
    "relationshipType": "Account",
    "organization": {
      "id": "9e2fd2ee11b43110f877366201dea674",
      "name": "Global Holdings Ltd.",
      "@type": "Organization"
    }
  },
  "status": "active",
  "@type": "Account"
}'
```

Response body.

```
{
  "id": "0fef075b2fe06a10b79db3bf42faf31c",
  "href": "http://instance.service-now.com/api/sn_tmf_api/v2/party/organization/0fef075b2fe06a10b79db3bf42faf31c",
  "name": "SERVICENOW 144",
  "legalName": "Acme Corp Ltd.",
  "tradingName": "Acme Inc.",
  "contactMedium": [
    {
      "preferred": true,
      "contactType": "email",
      "emailAddress": "athammhd@email.com",
      "@type": "EmailContactMedium"
    },
    {
      "preferred": false,
      "contactType": "phone",
      "phoneNumber": "+1-202-555-0198",
      "@type": "PhoneContactMedium"
    },
    {
      "preferred": false,
      "contactType": "faxPhone",
      "phoneNumber": "+1-202-555-0199",
      "@type": "FaxPhoneContactMedium"
    },
    {
      "preferred": false,
      "contactType": "postalAddress",
      "validFor": {
        "startDateTime": "2017-03-15T07:49:25.246Z"
      },
      "@type": "GeographicalAddressContactMedium",
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
      "name": "customer",
      "value": "true",
      "valueType": "boolean",
      "@type": "StringCharacteristics"
    },
    {
      "name": "registrationCode",
      "value": "003",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "vendorType",
      "value": ["Hardware"],
      "valueType": "array",
      "@type": "StringArrayCharacteristic"
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
      "name": "stockSymbol",
      "value": "Market",
      "valueType": "string",
      "@type": "StringCharacteristics"
    },
    {
      "name": "stockPrice",
      "value": "1000",
      "valueType": "string",
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
    },
    {
      "name": "marketCap",
      "value": "0",
      "valueType": "currency",
      "@type": "StringCharacteristics"
    },
    {
      "name": "profits",
      "value": "0",
      "valueType": "currency",
      "@type": "StringCharacteristics"
    },
    {
      "name": "revenuePerYear",
      "value": "0",
      "valueType": "currency",
      "@type": "StringCharacteristics"
    }
  ],
  "relatedParty": [
    {
      "role": "primaryContact",
      "@type": "contact",
      "partyOrPartyRole": {
        "id": "eaf68911c35420105252716b7d40ddde",
        "givenName": "John",
        "familyName": "Doe",
        "contactMedium": [
          {
            "contactType": "email",
            "emailAddress": "john.doe@example.com",
            "@type": "EmailContactMedium"
          }
        ],
        "name": "John Doe",
        "@type": "Individual"
      }
    },
    {
      "role": "other",
      "@type": "contact",
      "partyOrPartyRole": {
        "id": "776a22ea11f43110f877366201dea6b7",
        "givenName": "Mary",
        "familyName": "Star",
        "contactMedium": [
          {
            "contactType": "email",
            "emailAddress": "mary.star@example.com",
            "@type": "EmailContactMedium"
          }
        ],
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
    "relationshipType": "Account",
    "organization": {
      "id": "9e2fd2ee11b43110f877366201dea674",
      "name": "Global Holdings Ltd.",
      "@type": "Organization"
    }
  },
  "status": "active",
  "@type": "Account",
  "createdDate": "2025-06-25T14:32:18.000Z",
  "lastModifiedDate": "2025-06-25T14:32:18.000Z"
}
```

