---
title: Party Management Open API
description: The Party Management Open API provides endpoints for managing parties with a relationship to the enterprise, like a consumer, account, or contact. Use this API to create, update, and retrieve data from the Consumer \[csm\_consumer\], Account \[customer\_account\], and Contact \[customer\_contact\] tables.Inactivates a specified record from the Consumer \[csm\_consumer\] and Contact \[customer\_contact\] tables.Retrieves a specified record from the Consumer \[csm\_consumer\] or Contact \[customer\_contact\] tables. You can filter results by specific fields.Retrieves a list of all individual \(party\) records with a relationship to the enterprise. You can filter results by specific fields or IDs.Retrieves a specified record from the Account \[customer\_account\] tables. You can filter results by specific fields or IDs.Retrieves organization-level party records from the Company \[core\_company\] and Account \[customer\_account\] tables. You can filter results by specific fields or IDs.Updates an existing individual party record in the Consumer \[csm\_consumer\] or Contact \[customer\_contact\] table without replacing the entire resource.Updates an existing individual party record in the Account \[customer\_account\] tables without replacing the entire resource.Creates a new individual party management record in the Consumer \[csm\_consumer\] or Contact \[customer\_contact\] tables.Creates a new party organization record in the Account \[customer\_account\] tables.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-11-17"
reading_time_minutes: 73
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Party Management Open API

The Party Management Open API provides endpoints for managing parties with a relationship to the enterprise, like a consumer, account, or contact. Use this API to create, update, and retrieve data from the Consumer \[csm\_consumer\], Account \[customer\_account\], and Contact \[customer\_contact\] tables.

The Party Management Open API is a ServiceNow® implementation of the TM Forum Party Management API REST specification. This implementation is based on the [TMF632 Party Management API Conformance Profile v5.0.0 – TM Forum](https://www.tmforum.org/resources/reference/tmf632b-party-management-api-conformance-profile-v5-0-0/), June 2025. The Party Management Open API is conformance certified by TM Forum.

The Party Management Open API is provided within the sn\_tmf\_api namespace. The calling user must have the sn\_tmf\_api.party\_integrator role. This API requires the Telecommunications Open APIs \(sn\_tmf\_api\) and Customer Service Management \(com.sn\_customerservice\) plugins to access it.

This API can be extended to make customizations around required parameters, request body validation, additional REST operations, and field mappings. Sensitive fields like phone numbers may require special ACL permissions for update or retrieval.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Party Management – DELETE /api/sn\_tmf\_api/v1/party/individual/\{id\}

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

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

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

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|None||

### cURL request

The following example deletes the given record.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v1/party/individual/dca96eaa11f43110f877366201dea6c1" \
--request DELETE \
--header "Accept:application/json" \
--user 'user':'password' \
```

Doesn't return a response body. Reference status codes for a success or failure indicator.

## Party Management - GET /api/sn\_tmf\_api/v1/party/individual/\{id\}

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

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

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

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

<table id="table_mh2_hc4_3hc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contactMedium

</td><td>

List of means for contacting the party. Data type: Array of Objects

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

Type of contacting party. Indicates the specific schema or subclass type of the object.Possible values:

-   BusinessPhoneContactMedium: Business phone number
-   EmailContactMedium: Email address
-   FaxPhoneContactMedium: Fax number
-   GeographicAddressContactMedium: Physical address \(street, city, state, postal code\)
-   HomePhoneContactMedium: Home phone number
-   MobilePhoneContactMedium: Mobile number

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the individual. Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the individual.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address of the contact.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the party location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

The type of contact medium. Indicates the business-level attribute that specifies the kind of contact channel being used.Possible values:

-   email
-   businessPhone
-   homePhone
-   mobilePhone
-   postalAddress

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone number of the individual.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postcode of the individual.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

This value is always false.Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

Indicates whether the location is from a state or province.Possible values:

-   state
-   province

Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

Describes the street.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Complementary street description.Data type: String

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

Relative link to the user or consumer or contact record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the user or consumer or contact record to retrieve.Tables: Consumer \[csm\_consumer\] or Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

name

</td><td>

User name of the user or contact individual.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristics

</td><td>

List of characteristics associated with the party.Data type: Array of Objects

```
"partyCharacteristics": [
 {
  "@type": "String",
  "name": " String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristics.@type

</td><td>

When subclassing, this defines the subclass extensible name.Possible values:

-   StringCharacteristic
-   StringArrayCharacteristic
-   IntegerCharacteristic
-   BooleanCharacteristic

Data type: String

</td></tr><tr><td>

partyCharacteristics.name

</td><td>

Name of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.value

</td><td>

Value of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.valueType

</td><td>

Data type of the characteristic's value.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Roles related to this party are defined where the party is created in table. For example, `User`, `Consumer`, `Customer Contact`.**partyOrPartyRole** indicates which type of record is retrieved in the operation. If the provided sys\_id belongs to the Consumer \[csm\_consumer\] table, then **partyOrPartyRole.role** is set to `Consumer`. Likewise, if the sys\_id belongs to the Contact \[customer\_contact\] table, then **partyOrPartyRole.role** is set to `Contact`.

Data type: Object

```
"partyOrPartyRole":
{
  "@type": "String",
  "role":"String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

This value is always `Party`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Type of party role. Possible values:

-   Consumer
-   Contact

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties or party roles related to this party.Data type: Array of Objects

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

Represents information about the related party and the role it plays in the context of the record. For example, if the role is `Company`, then **partyOrPartyRole.id** contains the sys\_id of the Company \[core\_company\] record, and **partyOrPartyRole.name** contains the company’s name. This structure ensures that both the party reference and its role are explicitly defined and easily identifiable.

Data type: Object

```
"partyOrPartyRole":
{
  "@type": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Possible value for user:

-   Organization
-   Individual

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related party.-   Possible value for `user`:
    -   Company
    -   Department
-   Possible value for `customer`: Account
-   Possible value for `consumer`: User

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Business role that the related party plays in the context of the current entity.Possible values:

-   Company \(if related party is User\)
-   Department \(if related party is User\)
-   Account \(if related party is Customer\)
-   User \(if related party is Consumer\)

Data type: String

</td></tr><tr><td>

status

</td><td>

Flag that indicates the status of the individual.Valid values:

-   active: Individual is in an active status.
-   inactive: Individual is in an inactive status.

Data type: Boolean

</td></tr><tr><td>

title

</td><td>

Prefix or title of the individual. For example, `Dr.`, `Mr.`, `Ms.`\).Data type: String

</td></tr></tbody>
</table>### cURL request

Retrieves a specified record, `12345`, from the table.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/v1/party/individual/12345" \
--request GET \
--header "Accept:application/json" \
--user 'user':'password' \
```

Response body.

```
{
  "id": "12345",
  "givenName": "JohnTest6",
  "middleName": "A.",
  "familyName": "Doe",
  "gender": "male",
  "nationality": "American",
  "title": "Mr",
  "contactMedium": [
    {
      "preferred": true,
      "mediumType": "email",
      "emailAddress": "john.doe18723@example.com",
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
      "preferred":false,
      "mediumType":"faxPhone",
      "phoneNumber":"123456789",
      "@type":"FaxContactMedium"
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
      "locationId":"25ab9e240a0a0bb3009eb9ef8dd0a2c0",
      "city": "Town",
      "country": "USA",
      "postCode": "07960",
      "stateOrProvince": "New Jersey",
      "street1": "1820 Harris Houston Road, Charlotte",
      "street2": "East Tower - 10th Floor"
    },
    {
      "preferred": false,
      "mediumType": "postalAddress",
      "@type": "GeographicAddressContactMedium",
      "locationId":"25aba17a0a0a0bb3007efd809d6e695c",
      "city": "Webster",
      "country": "USA",
      "postCode": "76022",
      "stateOrProvince": "TN",
      "street1": "17077 Texas Avenue, Webster",
      "street2": "East Tower - 11th Floor"
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
      "value": "notes about the consumer",
      "valueType": "string",
      "@type": "string"
    },
    {
      "name": "dateFormat",
      "value": "dd-mm-yyyy",
      "valueType": "string",
      "@type": "string"
    },
    {
      "name": "timeformat",
      "value": "hh.mm.ss (12 hour)",
      "valueType": "string",
      "@type": "string"
    },
    {
      "name": "notification",
      "value": "Enable",
      "valueType": "string",
      "@type": "string"
    }
  ],
  "relatedParty": [
    {
      "role": "User",
      "partyOrPartyRole": {
        "id": "36901a6381116a50f8776cfcbee15f3c",
        "name": "Hr",
        "@type": "Individual"
      }
    }
  ],
  "status": "active",
  "@type": "Individual",
  "partyOrPartyRole": {
    "role": "Consumer",
    "@type":"Party"
  }
}
```

## Party Management – GET /api/sn\_tmf\_api/v1/party/individual

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

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

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

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

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

<table id="id_eyq_bh4_3hc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contactMedium

</td><td>

List of means for contacting the party. Data type: Array of Objects

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

Type of contacting party. Indicates the specific schema or subclass type of the object.Possible values:

-   BusinessPhoneContactMedium: Business phone number
-   EmailContactMedium: Email address
-   FaxPhoneContactMedium: Fax number
-   GeographicAddressContactMedium: Physical address \(street, city, state, postal code\)
-   HomePhoneContactMedium: Home phone number
-   MobilePhoneContactMedium: Mobile number

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the individual. Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the individual.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address of the contact.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the party location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

The type of contact medium. Indicates the business-level attribute that specifies the kind of contact channel being used.Possible values:

-   email
-   businessPhone
-   homePhone
-   mobilePhone
-   postalAddress

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone number of the individual.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postcode of the individual.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

This value is always false.Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

Indicates whether the location is from a state or province.Possible values:

-   state
-   province

Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

Describes the street.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Complementary street description.Data type: String

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

Relative link to the user or consumer or contact record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the user or consumer or contact record to retrieve.Tables: Consumer \[csm\_consumer\] or Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

name

</td><td>

User name of the user or contact individual.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristics

</td><td>

List of characteristics associated with the party.Data type: Array of Objects

```
"partyCharacteristics": [
 {
  "@type": "String",
  "name": " String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristics.@type

</td><td>

When subclassing, this defines the subclass extensible name.Possible values:

-   StringCharacteristic
-   StringArrayCharacteristic
-   IntegerCharacteristic
-   BooleanCharacteristic

Data type: String

</td></tr><tr><td>

partyCharacteristics.name

</td><td>

Name of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.value

</td><td>

Value of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.valueType

</td><td>

Data type of the characteristic's value.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Roles related to this party are defined where the party is created in table. For example, `User`, `Consumer`, `Customer Contact`.**partyOrPartyRole** indicates which type of record is retrieved in the operation. If the provided sys\_id belongs to the Consumer \[csm\_consumer\] table, then **partyOrPartyRole.role** is set to `Consumer`. Likewise, if the sys\_id belongs to the Contact \[customer\_contact\] table, then **partyOrPartyRole.role** is set to `Contact`.

Data type: Object

```
"partyOrPartyRole":
{
  "@type": "String",
  "role":"String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

This value is always `Party`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Type of party role. Possible values:

-   Consumer
-   Contact

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties or party roles related to this party.Data type: Array of Objects

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

Represents information about the related party and the role it plays in the context of the record. For example, if the role is `Company`, then **partyOrPartyRole.id** contains the sys\_id of the Company \[core\_company\] record, and **partyOrPartyRole.name** contains the company’s name. This structure ensures that both the party reference and its role are explicitly defined and easily identifiable.

Data type: Object

```
"partyOrPartyRole":
{
  "@type": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Possible value for user:

-   Organization
-   Individual

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related party.-   Possible value for `user`:
    -   Company
    -   Department
-   Possible value for `customer`: Account
-   Possible value for `consumer`: User

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Business role that the related party plays in the context of the current entity.Possible values:

-   Company \(if related party is User\)
-   Department \(if related party is User\)
-   Account \(if related party is Customer\)
-   User \(if related party is Consumer\)

Data type: String

</td></tr><tr><td>

status

</td><td>

Flag that indicates the status of the individual.Valid values:

-   active: Individual is in an active status.
-   inactive: Individual is in an inactive status.

Data type: Boolean

</td></tr><tr><td>

title

</td><td>

Prefix or title of the individual. For example, `Dr.`, `Mr.`, `Ms.`\).Data type: String

</td></tr></tbody>
</table>### cURL request

Retrieves a list of all party management records in the instance.

```
curl"http://instance.servicenow.com/api/v1/sn_tmf_api/party/individual" \
--request GET \
--header "Accept:application/json" \
--user 'user:password' 
```

Response body for a Individual Contact party.

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
   "partyCharacteristics": [
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
       "@type": "MobilePhoneContactMedium"
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
   "status": "Active",
   "@type": "Individual",
   "partyOrPartyRole": {
     "name": "Contact",
     "@type": "Party"
   }
 }
]
```

Response body for a Individual Consumer party.

```
[
{
   "id": "168bfc6953a46210132bddeeff7b129f",
   "href": "api/sn_tmf_api/party/individual/168bfc6953a46210132bddeeff7b129f",
   "givenName": "yyyg",
   "middleName": "hhh",
   "familyName": "bhhhbjhh",
   "gender": "",
   "nationality": "",
   "title": "",
   "partyCharacteristics": [
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
       "@type": "MobilePhoneContactMedium"
     },
     {
       "preferred": false,
       "mediumType": "fax",
       "phoneNumber": "",
       "@type": "FaxContactMedium"
     },
     {
       "preferred": false,
       "mediumType": "postalAddress",
       "@type": "GeographicalAddressContactMedium",
       "city": "ygyg",
       "locationId": "a39bfc6953a46210132bddeeff7b12b7",
       "country": "",
       "postCode": "hh",
       "stateOrProvince": "gyg",
       "street1": "hgg",
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
   "status": "Active",
   "@type": "Individual",
   "partyOrPartyRole": {
     "name": "Consumer",
     "@type": "Party"
   }
 }
]
```

## Party Management – GET/api/ sn\_tmf\_api/v1/party/organization/\{id\}

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

Sys\_id of the company or account record to retrieve.Table: Account \[customer\_account\] or Company \[csm\_company\]

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

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

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

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

### Response body parameters \(JSON or XML\)

<table id="table_edn_qnn_3hc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

This value is always `Organization`.Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of means for contacting the party. A contact medium represents the way you communicate with or reach a party like an individual or organization. For example, a channel or method of contact associated with that party.Data type: Array of Objects

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

Type of contact medium. Type of contacting party. Indicates the specific schema or subclass type of the object.Possible values:

-   BusinessPhoneContactMedium: Business phone number
-   EmailContactMedium: Email address
-   FaxPhoneContactMedium: Fax number
-   GeographicAddressContactMedium: Physical address \(street, city, state, postal code\)
-   HomePhoneContactMedium: Home phone number
-   MobilePhoneContactMedium: Mobile number

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the organization.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the organization.Data type: String

</td></tr><tr><td>

contactMedium.emailAdress

</td><td>

Email address of the organization contact.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

The type of contact medium. Possible values:

-   businessPhone
-   email
-   faxPhone
-   homePhone
-   mobilePhone
-   postalAddress

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone number of the organization contact.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postcode of the organization.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

This value is always `false`.Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

Indicates whether the location is from a state or province.Possible values:

-   state
-   province

Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

Describes the street.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Complementary street description.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the party in an external system.Data type: Array of Objects

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

Type of entity within the external system.Data type: String

</td></tr><tr><td>

externalReference.name

</td><td>

Human-readable name of the external system or reference.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the account record \(URI\).Table: Account \[customer\_account\]

Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the external entity account record.Table: Account \[customer\_account\]

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

partyCharacteristics

</td><td>

List of characteristics that a party can take on. Data type: Array of Objects

```
"partyCharacteristics": [ 
 { 
  "@type": "String" 
  "name": "String",   
  "value": "String", 
  "valueType": "String"
 } 
]
```

</td></tr><tr><td>

partyCharacteristics.@type

</td><td>

When subclassing, **@type** defines the subclass extensible name.Possible value:

-   BooleanCharacteristic
-   IntegerCharacteristic
-   StringArrayCharacteristic
-   StringCharacteristic

Data type: String

</td></tr><tr><td>

partyCharacteristics.name

</td><td>

Name of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.value

</td><td>

Value of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.valueType

</td><td>

Data type of the characteristic's value.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Roles related to this party are defined where the party is created in the table. For example, `Company` or `Account`.**partyOrPartyRole** indicates which type of record is retrieved in the operation. If the provided sys\_id belongs to the Account \[customer\_account\] table, then **partyOrPartyRole.role** is set to `Account`. Likewise, if the sys\_id belongs to the Company \[core\_company\] table, then **partyOrPartyRole.role** is set to `Company`.

Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "name":"String",
  "role":"String",
}
```

</td></tr><tr><td>

PartyOrPartyRole.@type

</td><td>

This value is always `party`.Data type: String

</td></tr><tr><td>

PartyOrPartyRole.name

</td><td>

Defines the type of the account or company.Data type: String

</td></tr><tr><td>

PartyOrPartyRole.role

</td><td>

Type of the role.Possible value:

-   Account
-   Company

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties or party roles related to this party.Data type: Array of Objects

```
"relatedParty": [ 
 { 
  "partyOrPartyRole": {Object},
  "role": "String"
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Roles related to this party.Data type: Array of Objects

```
"partyOrPartyRole": [ 
 { 
  "@type": "String", 
  "id": "String",
  "name": "String",
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Value is always `Organization`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related party. Possible value:

-   Contact
-   Other

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role played by the related party or party role in the context of the specific entity it's linked to. Possible values:

-   Contact
-   Other

Data type: String

</td></tr><tr><td>

status

</td><td>

Flag that indicates the status of organization.Valid values:

-   active: Organization is active.
-   inactive: Organization is inactive.

Data type: Boolean

</td></tr><tr><td>

tradingName

</td><td>

Name that the organization trades under.Data type: String

</td></tr></tbody>
</table>### cURL request

The following GET call returns fields for the specified party management organization record with sys\_id, 12345.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/v1/party/organization/12345" \
--request GET \
--header "Accept:application/json" \
--user 'user':'password' \
```

Response body.

```
{
   "id": "2154376",
   "name": "Advances Super Computing",
   "href": "api/sn_tmf_api/party/organization/2154376",
   "legalName": "Hello",
   "tradingName": "World",
   "contactMedium": [
     {
       "preferred": "false",
       "mediumType": "email",
       "@type": "EmailContactMedium",
       "emailAddress": "user@servicenow.com"
     },
     {
       "preferred": "false",
       "mediumType": "phone",
       "@type": "PhoneContactMedium",
       "phone": "(555) 555-5555"
     },
     {
       "preferred": "false",
       "mediumType": "faxPhone",
       "@type": "FaxPhoneContactMedium",
       "fax_phone": ""
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
       "value": "efdxcjkn ",
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
       "value": "####30",
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
       "value": "",
       "valueType": "choice",
       "@type": "StringCharacteristic"
     },
     {
       "name": "numEmployees",
       "value": "",
       "valueType": "integer",
       "@type": "IntergerCharacteristic"
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
       "value": "sdfgh.com",
       "valueType": "string",
       "@type": "StringCharacteristic"
     }
   ],
   "relatedParty": [
     {
       "role": "primary",
       "partyOrPartyRole": {
         "@type": "Organization",
         "id": "b88d14843bc02300bfe04d72f3efc4cd",
         "name": "Amy Chen"
       }
     },
     {
       "role": "other",
       "partyOrPartyRole": {
         "@type": "Organization",
         "id": "016b7a36ff14a610f8dfffffffffffcb",
         "name": "Kutty"
       }
     },
     {
       "role": "other",
       "partyOrPartyRole": {
         "@type": "Organization",
         "id": "e8bb9d1aff94a210f8dfffffffffff1d",
         "name": "World"
       }
     }
   ],
   "organizationChildRelationship": [
     {
       "relationshipType": "partner_account",
       "organization": {
         "id": "9e2fd2ee11b43110f877366201dea674",
         "name": "Startech svcs",
         "href": "api/sn_tmf_api/party/organization/9e2fd2ee11b43110f877366201dea674",
         "@type": "Organization"
       }
     },
     {
       "relationshipType": "New type",
       "organization": {
         "id": "9e2fd2ee11b43110f877366201dea674",
         "name": "Startech svcs",
         "href": "api/sn_tmf_api/party/organization/9e2fd2ee11b43110f877366201dea674",
         "@type": "Organization"
       }
     },
     {
       "relationshipType": "child",
       "organization": {
         "id": "9e2fd2ee11b43110f877366201dea674",
         "name": "Startech svcs",
         "href": "api/sn_tmf_api/party/organization/null",
         "@type": "Organization"
       }
     }
   ],
   "organizationParentRelationship": {
     "relationshipType": "parent",
     "organization": {
       "id": "ffc68911c35420105252716b7d40dd55",
       "name": "Funco Intl",
       "href": "undefinedffc68911c35420105252716b7d40dd55",
       "@type": "Organization"
     }
   },
   "status": "inActive",
   "@type": "Organization",
   "partyOrPartyRole": {
     "name": "customer_partner_vendor_manufacturer",
     "role": "Account",
     "@type": "Party"
   }
 }
```

## Party Management - GET /api/sn\_tmf\_api/v1/party/organization

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
</table><table id="id_avm_mj4_3hc" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contactMedium

</td><td>

List of means for contacting the party. Data type: Array of Objects

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

Type of contacting party. Indicates the specific schema or subclass type of the object.Possible values:

-   BusinessPhoneContactMedium: Business phone number
-   EmailContactMedium: Email address
-   FaxPhoneContactMedium: Fax number
-   GeographicAddressContactMedium: Physical address \(street, city, state, postal code\)
-   HomePhoneContactMedium: Home phone number
-   MobilePhoneContactMedium: Mobile number

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the individual. Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the individual.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address of the contact.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the party location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

The type of contact medium. Indicates the business-level attribute that specifies the kind of contact channel being used.Possible values:

-   email
-   businessPhone
-   homePhone
-   mobilePhone
-   postalAddress

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone number of the individual.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postcode of the individual.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

This value is always false.Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

Indicates whether the location is in a state or province.Possible values:

-   state
-   province

Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

Describes the street.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Complementary street description.Data type: String

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

Relative link to the user or consumer or contact record.Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

name

</td><td>

User name of the user or contact individual.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristics

</td><td>

List of characteristics associated with the party.Data type: Array of Objects

```
"partyCharacteristics": [
 {
  "@type": "String",
  "name": " String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristics.@type

</td><td>

When subclassing, this parameter defines the subclass extensible name.Possible values:

-   StringCharacteristic
-   StringArrayCharacteristic
-   IntegerCharacteristic
-   BooleanCharacteristic

Data type: String

</td></tr><tr><td>

partyCharacteristics.name

</td><td>

Name of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.value

</td><td>

Value of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.valueType

</td><td>

Data type of the characteristic's value.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Roles related to this party are defined where the party is created in table. For example, `User`, `Consumer`, `Customer Contact`.**partyOrPartyRole** indicates which type of record is retrieved in the operation. If the provided sys\_id belongs to the Consumer \[csm\_consumer\] table, then **partyOrPartyRole.role** is set to `Consumer`. Likewise, if the sys\_id belongs to the Contact \[customer\_contact\] table, then **partyOrPartyRole.role** is set to `Contact`.

Data type: Object

```
"partyOrPartyRole":
{
  "@type": "String",
  "role":"String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

This value is always `Party`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Type of the role. Possible values:

-   Consumer
-   Contact

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties and party roles related to this party.Data type: Array of Objects

```
"relatedParty": [
  {
    "role": "String",
    "partyOrPartyRole": {Object}
  }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Possible value for user:

-   Organization
-   Individual

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

ID for the linked entity in the Party Management or Party Role Management system.

-   Possible value for user:
    -   `Company`
    -   `Department`
-   Possible value for customer: `Account`
-   Possible value for consumer: `User`

 Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Business role that the related party plays in the context of the current entity.Possible values:

-   Company \(if related party is User\)
-   Department \(if related party is User\)
-   Account \(if related party is Customer\)
-   User \(if related party is Consumer\)

Data type: String

</td></tr><tr><td>

status

</td><td>

Flag that indicates the status of the individual.Valid values:

-   active: Individual is in an active status.
-   inactive: Individual isn't in an active status.

Data type: Boolean

</td></tr><tr><td>

title

</td><td>

Prefix or title of the individual. For example, `Dr.`, `Mr.`, `Ms.`\).Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

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

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|None||

### cURL request

This returns all organization records related to the enterprise.

```
curl"http://instance.servicenow.com/api/sn_tmf_api/v1/party/organization" \
--request GET \
--header "Accept:application/json" \
--user 'user':'password'
```

Response body.

```
[
  {
    "id": "0bd6717c184da610f87765359bc696d3",
    "name": "SERVICENOW 144",
    "href": "api/sn_tmf_api/party/organization0bd6717c184da610f87765359bc696d3",
    "legalName": "",
    "tradingName": "",
    "contactMedium": [
      {
        "preferred": "false",
        "mediumType": "email",
        "@type": "EmailContactMedium",
        "emailAddress": "user@email.com"
      },
      {
        "preferred": "false",
        "mediumType": "phone",
        "@type": "PhoneContactMedium",
        "phone": "+1-555-555-5555"
      },
      {
        "preferred": "false",
        "mediumType": "faxPhone",
        "@type": "FaxPhoneContactMedium",
        "fax_phone": ""
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
        "value": "technology_services",
        "valueType": "choice",
        "@type": "StringCharacteristic"
      },
      {
        "name": "numEmployees",
        "value": "",
        "valueType": "integer",
        "@type": "IntergerCharacteristic"
      },
      {
        "name": "rankTier",
        "value": "rankTier",
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
          "name": "child",
          "href": "api/sn_tmf_api/party/organization396b47201841a610f87765359bc696cf",
          "@type": "Organization"
        }
      }
    ],
    "organizationParentRelationship": {
      "relationshipType": "parent",
      "organization": {
        "id": "9e2fd2ee11b43110f877366201dea674",
        "name": "Startech svcs",
        "href": "api/sn_tmf_api/party/organization9e2fd2ee11b43110f877366201dea674",
        "@type": "Organization"
      }
    },
    "@type": "Organization",
    "partyOrPartyRole": {
      "name": "customer_partner",
      "role": "Account",
      "@type": "Party"
    }
  }
]
```

## Party Management – PATCH/api/sn\_tmf\_api/v1/party/individual/\{id\}

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

<table id="id_zhv_km4_3hc" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contactMedium

</td><td>

List of means for contacting the party. Data type: Array of Objects

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

Type of contacting party. Indicates the specific schema or subclass type of the object.Possible values:

-   BusinessPhoneContactMedium: Business phone number
-   EmailContactMedium: Email address
-   FaxPhoneContactMedium: Fax number
-   GeographicAddressContactMedium: Physical address \(street, city, state, postal code\)
-   HomePhoneContactMedium: Home phone number
-   MobilePhoneContactMedium: Mobile number

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the individual. Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the individual.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address of the contact.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the party location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

The type of contact medium. Indicates the business-level attribute that specifies the kind of contact channel being used.Possible values:

-   email
-   businessPhone
-   homePhone
-   mobilePhone
-   postalAddress

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone number of the individual.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postcode of the individual.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

This value is always false.Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

Indicates whether the location is in a state or province.Possible values:

-   state
-   province

Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

Describes the street.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Complementary street description.Data type: String

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

Relative link to the user or consumer or contact record.Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

name

</td><td>

User name of the user or contact individual.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristics

</td><td>

List of characteristics associated with the party.Data type: Array of Objects

```
"partyCharacteristics": [
 {
  "@type": "String",
  "name": " String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristics.@type

</td><td>

When subclassing, this parameter defines the subclass extensible name.Possible values:

-   StringCharacteristic
-   StringArrayCharacteristic
-   IntegerCharacteristic
-   BooleanCharacteristic

Data type: String

</td></tr><tr><td>

partyCharacteristics.name

</td><td>

Name of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.value

</td><td>

Value of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.valueType

</td><td>

Data type of the characteristic's value.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Roles related to this party are defined where the party is created in table. For example, `User`, `Consumer`, `Customer Contact`.**partyOrPartyRole** indicates which type of record is retrieved in the operation. If the provided sys\_id belongs to the Consumer \[csm\_consumer\] table, then **partyOrPartyRole.role** is set to `Consumer`. Likewise, if the sys\_id belongs to the Contact \[customer\_contact\] table, then **partyOrPartyRole.role** is set to `Contact`.

Data type: Object

```
"partyOrPartyRole":
{
  "@type": "String",
  "role":"String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

This value is always `Party`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Type of the role. Possible values:

-   Consumer
-   Contact

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties and party roles related to this party.Data type: Array of Objects

```
"relatedParty": [
  {
    "role": "String",
    "partyOrPartyRole": {Object}
  }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Possible value for user:

-   Organization
-   Individual

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

ID for the linked entity in the Party Management or Party Role Management system.

-   Possible value for user:
    -   `Company`
    -   `Department`
-   Possible value for customer: `Account`
-   Possible value for consumer: `User`

 Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Business role that the related party plays in the context of the current entity.Possible values:

-   Company \(if related party is User\)
-   Department \(if related party is User\)
-   Account \(if related party is Customer\)
-   User \(if related party is Consumer\)

Data type: String

</td></tr><tr><td>

status

</td><td>

Flag that indicates the status of the individual.Valid values:

-   active: Individual is in an active status.
-   inactive: Individual isn't in an active status.

Data type: Boolean

</td></tr><tr><td>

title

</td><td>

Prefix or title of the individual. For example, `Dr.`, `Mr.`, `Ms.`\).Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

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

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

<table id="id_t1b_mm4_3hc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contactMedium

</td><td>

List of means for contacting the party. Data type: Array of Objects

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

Type of contacting party. Indicates the specific schema or subclass type of the object.Possible values:

-   BusinessPhoneContactMedium: Business phone number
-   EmailContactMedium: Email address
-   FaxPhoneContactMedium: Fax number
-   GeographicAddressContactMedium: Physical address \(street, city, state, postal code\)
-   HomePhoneContactMedium: Home phone number
-   MobilePhoneContactMedium: Mobile number

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the individual. Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the individual.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address of the contact.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the party location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

The type of contact medium. Indicates the business-level attribute that specifies the kind of contact channel being used.Possible values:

-   email
-   businessPhone
-   homePhone
-   mobilePhone
-   postalAddress

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone number of the individual.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postcode of the individual.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

This value is always false.Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

Indicates whether the location is from a state or province.Possible values:

-   state
-   province

Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

Describes the street.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Complementary street description.Data type: String

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

Relative link to the user or consumer or contact record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the user or consumer or contact record to retrieve.Tables: Consumer \[csm\_consumer\] or Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

name

</td><td>

User name of the user or contact individual.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristics

</td><td>

List of characteristics associated with the party.Data type: Array of Objects

```
"partyCharacteristics": [
 {
  "@type": "String",
  "name": " String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristics.@type

</td><td>

When subclassing, this defines the subclass extensible name.Possible values:

-   StringCharacteristic
-   StringArrayCharacteristic
-   IntegerCharacteristic
-   BooleanCharacteristic

Data type: String

</td></tr><tr><td>

partyCharacteristics.name

</td><td>

Name of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.value

</td><td>

Value of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.valueType

</td><td>

Data type of the characteristic's value.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Roles related to this party are defined where the party is created in table. For example, `User`, `Consumer`, `Customer Contact`.**partyOrPartyRole** indicates which type of record is retrieved in the operation. If the provided sys\_id belongs to the Consumer \[csm\_consumer\] table, then **partyOrPartyRole.role** is set to `Consumer`. Likewise, if the sys\_id belongs to the Contact \[customer\_contact\] table, then **partyOrPartyRole.role** is set to `Contact`.

Data type: Object

```
"partyOrPartyRole":
{
  "@type": "String",
  "role":"String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

This value is always `Party`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Type of party role. Possible values:

-   Consumer
-   Contact

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties or party roles related to this party.Data type: Array of Objects

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

Represents information about the related party and the role it plays in the context of the record. For example, if the role is `Company`, then **partyOrPartyRole.id** contains the sys\_id of the Company \[core\_company\] record, and **partyOrPartyRole.name** contains the company’s name. This structure ensures that both the party reference and its role are explicitly defined and easily identifiable.

Data type: Object

```
"partyOrPartyRole":
{
  "@type": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Possible value for user:

-   Organization
-   Individual

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related party.-   Possible value for `user`:
    -   Company
    -   Department
-   Possible value for `customer`: Account
-   Possible value for `consumer`: User

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Business role that the related party plays in the context of the current entity.Possible values:

-   Company \(if related party is User\)
-   Department \(if related party is User\)
-   Account \(if related party is Customer\)
-   User \(if related party is Consumer\)

Data type: String

</td></tr><tr><td>

status

</td><td>

Flag that indicates the status of the individual.Valid values:

-   active: Individual is in an active status.
-   inactive: Individual is in an inactive status.

Data type: Boolean

</td></tr><tr><td>

title

</td><td>

Prefix or title of the individual. For example, `Dr.`, `Mr.`, `Ms.`\).Data type: String

</td></tr></tbody>
</table>### cURL request

Updates an existing individual party record with sys\_id, 12345, in the Consumer \[csm\_consumer\] or Contact \[customer\_contact\] table without replacing the entire resource.

```
curl "http://localhost:8080/api/sn_tmf_api/v1/party/Individual/12345" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--user 'user':'password'
--data "{
  \"name\": \"John.Doe\",
  \"givenName\": \"John\",
  \"middleName\": \"A.\",
  \"familyName\": \"Doe\",
  \"gender\": \"male\",
  \"nationality\": \"American\",
  \"title\": \"Mr\",
  \"contactMedium\": [
    {
      \"preferred\": true,
      \"mediumType\": \"email\",
      \"emailAddress\": \"john.doe@gmail.com\",
      \"@type\": \"EmailContactMedium\"
    },
    {
      \"preferred\": false,
      \"mediumType\": \"businessPhone\",
      \"phoneNumber\": \"+1-202-555-0188\",
      \"@type\": \"PhoneContactMedium\"
    },
    {
      \"preferred\": false,
      \"mediumType\": \"homePhone\",
      \"phoneNumber\": \"+1-202-555-0198\",
      \"@type\": \"HomePhoneContactMedium\"
    },
    {
      \"preferred\": false,
      \"mediumType\": \"postalAddress\",
      \"@type\": \"GeographicAddressContactMedium\",
      \"locationId\":\"92656927259338967\",
      \"city\": \"Morristown\",
      \"country\": \"USA\",
      \"postCode\": \"07960\",
      \"stateOrProvince\": \"New Jersey\",
      \"street1\": \"240 Headquarters Plazza\", 
      \"street2\": \"East Tower - 10th Floor\"
    }
  ],
  \"partyCharacteristic\": [
    {
        \"name\": \"notification\",
        \"value\": \"enable\",
        \"valueType\": \"string\",
        \"@type\": \"string\"
    },
    {
        \"name\": \"dateFormat\",
        \"value\": \"MM/DD/YYYY\",
        \"valueType\": \"string\",
        \"@type\": \"string\"
    },
    {
        \"name\": \"timeFormat\",
        \"value\": \"12-hour\",
        \"valueType\": \"string\",
        \"@type\": \"string\"
    },
    {
        \"name\": \"timeZone\",
        \"value\": \"EST\",
        \"valueType\": \"string\",
        \"@type\": \"string\"
    },
    {
        \"name\": \"vip\",
        \"value\": true,
        \"valueType\": \"boolean\",
        \"@type\": \"string\"
    },
    {
        \"name\": \"webServiceAccessOnly\",
        \"value\": false,
        \"valueType\": \"boolean\",
        \"@type\": \"string\"
    },
    {
        \"name\": \"source\",
        \"value\": \"Third-party system\",
        \"valueType\": \"string\",
        \"@type\": \"string\"
    },
    {
        \"name\": \"eduStatus\",
        \"value\": \"Graduated\",
        \"valueType\": \"string\",
        \"@type\": \"string\"
    }
  ],
  \"relatedParty\": [
    {
      \"role\": \"Company\",
      \"partyOrPartyRole\": {
        \"id\": \"86c1f3193790200044e0bfc8bcbe5d95\",
        \"name\": \"Acme Corporation\",
        \"@type\": \"Organization\"
      }
    },
    {
      \"role\": \"Department\",
      \"partyOrPartyRole\": {
        \"id\": \"c3fdd27a7b9822105e0d5494548cb6b0\",
        \"name\": \"Acme Corporation\",
        \"@type\": \"Organization\"
      }
    }
  ],
  \"status\": \"active\",
  \"@type\": \"Individual\",
  \"partyOrPartyRole\": {
    \"role\": \"Consumer\",
    \"@type\":\"Party\"
  }
}" \
```

Response body.

```
{
   "name": "Jane Smith",
  "givenName": "Jane",
  "middleName": "B.",
  "familyName": "Smith",
  "gender": "female",
  "nationality": "American",
  "title": "Ms",
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
      "mediumType": "fax",
      "fax": "987654321",
      "@type": "FaxContactMedium"
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
      "@type": "string"
    },
    {
      "name": "userName",
      "value": "janesmith",
      "valueType": "string",
      "@type": "string"
    },
    {
      "name": "vip",
      "value": false,
      "valueType": "boolean",
      "@type": "string"
    },
    {
      "name": "source",
      "value": "CRM System",
      "valueType": "string",
      "@type": "string"
    },
    {
      "name": "dateFormat",
      "value": "yyyy-mm-dd",
      "valueType": "string",
      "@type": "string"
    },
    {
      "name": "timeformat",
      "value": "HH:mm:ss (24 hour)",
      "valueType": "string",
      "@type": "string"
    },
    {
      "name": "notification",
      "value": "Disabled",
      "valueType": "string",
      "@type": "string"
    }
  ],
  "relatedParty": [
    {
      "role": "User",
      "partyOrPartyRole": {
        "id": "c456def03710200044e0bfc8bcbe5d99",
        "name": "Global Corp",
        "@type": "Individual"
      }
    }
  ],
  "status": "active",
  "@type": "Individual",
  "partyOrPartyRole": {
    "role": "Consumer",
    "@type": "Party"
  },
   "warning": [
    "relatedParty[0] is incorrect. User does not exist"
  ]
}
```

## Party Management - PATCH /api/sn\_tmf\_api/v1/party/organization/\{id\}

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

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="id_czh_nnj_jhc" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

This value is always `Organization`.Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of means for contacting the party. A contact medium represents the way you communicate with or reach a party like an individual or organization. For example, a channel or method of contact associated with that party.Data type: Array of Objects

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

Type of contact medium. Type of contacting party. Indicates the specific schema or subclass type of the object.Possible values:

-   BusinessPhoneContactMedium: Business phone number
-   EmailContactMedium: Email address
-   FaxPhoneContactMedium: Fax number
-   GeographicAddressContactMedium: Physical address \(street, city, state, postal code\)
-   HomePhoneContactMedium: Home phone number
-   MobilePhoneContactMedium: Mobile number

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the organization.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the organization.Data type: String

</td></tr><tr><td>

contactMedium.emailAdress

</td><td>

Email address of the organization contact.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

The type of contact medium. Possible values:

-   businessPhone
-   email
-   faxPhone
-   homePhone
-   mobilePhone
-   postalAddress

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone number of the organization contact.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postcode of the organization.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

This value is always `false`.Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

Indicates whether the location is from a state or province.Possible values:

-   state
-   province

Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

Describes the street.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Complementary street description.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the party in an external system.Data type: Array of Objects

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

Type of entity within the external system.Data type: String

</td></tr><tr><td>

externalReference.name

</td><td>

Human-readable name of the external system or reference.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the account record \(URI\).Table: Account \[customer\_account\]

Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the external entity account record.Table: Account \[customer\_account\]

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

partyCharacteristics

</td><td>

List of characteristics that a party can take on. Data type: Array of Objects

```
"partyCharacteristics": [ 
 { 
  "@type": "String" 
  "name": "String",   
  "value": "String", 
  "valueType": "String"
 } 
]
```

</td></tr><tr><td>

partyCharacteristics.@type

</td><td>

When subclassing, **@type** defines the subclass extensible name.Possible value:

-   BooleanCharacteristic
-   IntegerCharacteristic
-   StringArrayCharacteristic
-   StringCharacteristic

Data type: String

</td></tr><tr><td>

partyCharacteristics.name

</td><td>

Name of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.value

</td><td>

Value of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.valueType

</td><td>

Data type of the characteristic's value.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Roles related to this party are defined where the party is created in the table. For example, `Company` or `Account`.**partyOrPartyRole** indicates which type of record is retrieved in the operation. If the provided sys\_id belongs to the Account \[customer\_account\] table, then **partyOrPartyRole.role** is set to `Account`. Likewise, if the sys\_id belongs to the Company \[core\_company\] table, then **partyOrPartyRole.role** is set to `Company`.

Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "name":"String",
  "role":"String",
}
```

</td></tr><tr><td>

PartyOrPartyRole.@type

</td><td>

This value is always `party`.Data type: String

</td></tr><tr><td>

PartyOrPartyRole.name

</td><td>

Defines the type of the account or company.Data type: String

</td></tr><tr><td>

PartyOrPartyRole.role

</td><td>

Type of the role.Possible value:

-   Account
-   Company

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties or party roles related to this party.Data type: Array of Objects

```
"relatedParty": [ 
 { 
  "partyOrPartyRole": {Object},
  "role": "String"
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Roles related to this party.Data type: Array of Objects

```
"partyOrPartyRole": [ 
 { 
  "@type": "String", 
  "id": "String",
  "name": "String",
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Value is always `Organization`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related party. Possible value:

-   Contact
-   Other

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role played by the related party or party role in the context of the specific entity it's linked to. Possible values:

-   Contact
-   Other

Data type: String

</td></tr><tr><td>

status

</td><td>

Flag that indicates the status of organization.Valid values:

-   active: Organization is active.
-   inactive: Organization is inactive.

Data type: Boolean

</td></tr><tr><td>

tradingName

</td><td>

Name that the organization trades under.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

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

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

<table id="table_edn_qnn_3hc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

This value is always `Organization`.Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of means for contacting the party. A contact medium represents the way you communicate with or reach a party like an individual or organization. For example, a channel or method of contact associated with that party.Data type: Array of Objects

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

Type of contact medium. Type of contacting party. Indicates the specific schema or subclass type of the object.Possible values:

-   BusinessPhoneContactMedium: Business phone number
-   EmailContactMedium: Email address
-   FaxPhoneContactMedium: Fax number
-   GeographicAddressContactMedium: Physical address \(street, city, state, postal code\)
-   HomePhoneContactMedium: Home phone number
-   MobilePhoneContactMedium: Mobile number

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the organization.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the organization.Data type: String

</td></tr><tr><td>

contactMedium.emailAdress

</td><td>

Email address of the organization contact.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

The type of contact medium. Possible values:

-   businessPhone
-   email
-   faxPhone
-   homePhone
-   mobilePhone
-   postalAddress

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone number of the organization contact.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postcode of the organization.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

This value is always `false`.Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

Indicates whether the location is from a state or province.Possible values:

-   state
-   province

Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

Describes the street.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Complementary street description.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the party in an external system.Data type: Array of Objects

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

Type of entity within the external system.Data type: String

</td></tr><tr><td>

externalReference.name

</td><td>

Human-readable name of the external system or reference.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the account record \(URI\).Table: Account \[customer\_account\]

Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the external entity account record.Table: Account \[customer\_account\]

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

partyCharacteristics

</td><td>

List of characteristics that a party can take on. Data type: Array of Objects

```
"partyCharacteristics": [ 
 { 
  "@type": "String" 
  "name": "String",   
  "value": "String", 
  "valueType": "String"
 } 
]
```

</td></tr><tr><td>

partyCharacteristics.@type

</td><td>

When subclassing, **@type** defines the subclass extensible name.Possible value:

-   BooleanCharacteristic
-   IntegerCharacteristic
-   StringArrayCharacteristic
-   StringCharacteristic

Data type: String

</td></tr><tr><td>

partyCharacteristics.name

</td><td>

Name of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.value

</td><td>

Value of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.valueType

</td><td>

Data type of the characteristic's value.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Roles related to this party are defined where the party is created in the table. For example, `Company` or `Account`.**partyOrPartyRole** indicates which type of record is retrieved in the operation. If the provided sys\_id belongs to the Account \[customer\_account\] table, then **partyOrPartyRole.role** is set to `Account`. Likewise, if the sys\_id belongs to the Company \[core\_company\] table, then **partyOrPartyRole.role** is set to `Company`.

Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "name":"String",
  "role":"String",
}
```

</td></tr><tr><td>

PartyOrPartyRole.@type

</td><td>

This value is always `party`.Data type: String

</td></tr><tr><td>

PartyOrPartyRole.name

</td><td>

Defines the type of the account or company.Data type: String

</td></tr><tr><td>

PartyOrPartyRole.role

</td><td>

Type of the role.Possible value:

-   Account
-   Company

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties or party roles related to this party.Data type: Array of Objects

```
"relatedParty": [ 
 { 
  "partyOrPartyRole": {Object},
  "role": "String"
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Roles related to this party.Data type: Array of Objects

```
"partyOrPartyRole": [ 
 { 
  "@type": "String", 
  "id": "String",
  "name": "String",
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Value is always `Organization`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related party. Possible value:

-   Contact
-   Other

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role played by the related party or party role in the context of the specific entity it's linked to. Possible values:

-   Contact
-   Other

Data type: String

</td></tr><tr><td>

status

</td><td>

Flag that indicates the status of organization.Valid values:

-   active: Organization is active.
-   inactive: Organization is inactive.

Data type: Boolean

</td></tr><tr><td>

tradingName

</td><td>

Name that the organization trades under.Data type: String

</td></tr></tbody>
</table>### cURL request

This returns specified fields for the party management organization records.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v1/party/organization" \
--request PATCH\
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--user 'user':'password' \
--data "{
  \"name\": \"SERVICENOW 144\",
  \"legalName\": \"Acme Corp Ltd.\",
  \"tradingName\": \"Acme Inc.\",
  \"contactMedium\": [
    {
      \"preferred\": true,
      \"mediumType\": \"email\",
      \"emailAddress\": \"athammhd@email.com\",
      \"@type\": \"EmailContactMedium\"
    },
    {
      \"preferred\": false,
      \"mediumType\": \"phone\",
      \"phoneNumber\": \"+1-202-555-0198\",
      \"@type\": \"PhoneContactMedium\"
    },
    {
      \"preferred\": false,
      \"mediumType\": \"businessPhone\",
      \"phoneNumber\": \"+1-202-555-0198\",
      \"@type\": \"BusinessPhoneContactMedium\"
    },
    {
      \"preferred\": false,
      \"mediumType\": \"homePhone\",
      \"phoneNumber\": \"+1-202-555-0198\",
      \"@type\": \"HomePhoneContactMedium\"
    },
    {
      \"preferred\": false,
      \"mediumType\": \"postalAddress\",
      \"validFor\": {
        \"startDateTime\": \"2017-03-15T07:49:25.246Z\"
      },
      \"@type\": \"GeographicAddressContactMedium\",
      \"city\": \"chennai\",
      \"country\": \"INDIA\",
      \"postCode\": \"608001\",
      \"stateOrProvince\": \"tamil nadu\",
      \"street1\": \"samcon street\",
      \"street2\": \"adyar,chennai\"
    }
  ],
  \"externalReference\": [
    {
      \"externalIdentifierType\": \"Instagram\",
      \"id\": \"Instagram\"
    }
  ],
  \"partyCharacteristic\": [
    {
      \"name\": \"notes\",
      \"value\": \"Testing for update the notes\",
      \"valueType\": \"string\",
      \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"customer\",
      \"value\": \"true\",
      \"valueType\": \"boolean\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"registrationCode\",
      \"value\": \"001\",
      \"valueType\": \"string\",
       \"@type\": \"StringCharacteristics\"
    },
    {
     \"name\": \"vendorType\",
     \"value\": [\"Hardware\"],
     \"valueType\": \"array\",
      \"@type\": \"StringArrayCharacteristic\"
     },
     {
      \"name\": \"industry\",
      \"value\": \"technology_services\",
      \"valueType\": \"choice\",
        \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"taxId\",
      \"value\": \"CTNUM1000123\",
      \"valueType\": \"string\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"numEmployees\",
      \"value\": \"EMP1000\",
      \"valueType\": \"integer\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"rankTier\",
      \"value\": \"rankTier\",
      \"valueType\": \"string\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"publiclyTraded\",
      \"value\": \"false\",
      \"valueType\": \"boolean\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"stockSymbol\",
      \"value\": \"Market\",
      \"valueType\": \"string\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"stockPrice\",
      \"value\": \"1000\",
      \"valueType\": \"string\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"vendor\",
      \"value\": \"false\",
      \"valueType\": \"boolean\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"manufacturer\",
      \"value\": \"false\",
      \"valueType\": \"boolean\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"marketCap\",
      \"value\": \"0\",
      \"valueType\": \"currency\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"profits\",
      \"value\": \"0\",
      \"valueType\": \"currency\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"revenuePerYear\",
      \"value\": \"0\",
      \"valueType\": \"currency\",
       \"@type\": \"StringCharacteristics\"
    }
  ],
  \"relatedParty\": [
    {
      \"role\": \"primaryContact\",
      \"partyOrPartyRole\": {
        \"id\": \"eaf68911c35420105252716b7d40ddde\",
        \"name\": \"John Doe\",
        \"@type\": \"Individual\"
      }
    },
    {
      \"role\": \"other\",
      \"partyOrPartyRole\": {
        \"id\": \"776a22ea11f43110f877366201dea6b7\",
        \"name\": \"Mary Star\",
        \"@type\": \"Individual\"
      }
    }
  ],
  \"organizationChildRelationship\": [
    {
      \"relationshipType\": \"partneraccount\",
      \"organization\": {
        \"id\": \"0fef075b2fe06a10b79db3bf42faf31a\",
        \"name\": \"mhd\",
        \"@type\": \"Organization\"
      }
    }
  ],
  \"organizationParentRelationship\": 
    {
      \"relationshipType\": \"Account\",
      \"organization\": {
        \"id\": \"9e2fd2ee11b43110f877366201dea674\",
        \"name\": \"Global Holdings Ltd.\",
        \"@type\": \"Organization\"
      }
    },
  \"status\": \"active\",
  \"@type\": \"Organization\",
  \"partyOrPartyRole\": {
    \"@type\":\"Party\",
    \"name\":\"Customer\",
    \"role\": \"Account\" 
  }
}" \
```

Response body.

```
{
  "name": "SERVICENOW 144",
  "legalName": "Acme Corp Ltd.",
  "tradingName": "Acme Inc.",
  "contactMedium": [
    {
      "preferred": true,
      "mediumType": "email",
      "emailAddress": "athammhd@email.com",
      "@type": "EmailContactMedium"
    },
    {
      "preferred": false,
      "mediumType": "phone",
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
      "name": "customer",
      "value": "true",
      "valueType": "boolean",
       "@type": "StringCharacteristics"
    },
    {
      "name": "registrationCode",
      "value": "001",
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
      "value": "technology_services",
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
      "value": "EMP1000",
      "valueType": "integer",
       "@type": "StringCharacteristics"
    },
    {
      "name": "rankTier",
      "value": "rankTier",
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
      "relationshipType": "partneraccount",
      "organization": {
        "id": "0fef075b2fe06a10b79db3bf42faf31a",
        "name": "mhd",
        "@type": "Organization"
      }
    }
  ],
  "organizationParentRelationship": 
    {
      "relationshipType": "Account",
      "organization": {
        "id": "9e2fd2ee11b43110f877366201dea674",
        "name": "Global Holdings Ltd.",
        "@type": "Organization"
      }
    },
  "status": "active",
  "@type": "Organization",
  "partyOrPartyRole": {
    "@type":"Party",
    "name":"Customer",
    "role": "Account" 
  }
}
```

## Party Management - POST /api/sn\_tmf\_api/v1/party/individual

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

<table id="id_tzm_xm4_3hc" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contactMedium

</td><td>

List of means for contacting the party. Data type: Array of Objects

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

Type of contacting party. Indicates the specific schema or subclass type of the object.Possible values:

-   BusinessPhoneContactMedium: Business phone number
-   EmailContactMedium: Email address
-   FaxPhoneContactMedium: Fax number
-   GeographicAddressContactMedium: Physical address \(street, city, state, postal code\)
-   HomePhoneContactMedium: Home phone number
-   MobilePhoneContactMedium: Mobile number

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the individual. Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the individual.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address of the contact.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the party location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

The type of contact medium. Indicates the business-level attribute that specifies the kind of contact channel being used.Possible values:

-   email
-   businessPhone
-   homePhone
-   mobilePhone
-   postalAddress

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone number of the individual.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postcode of the individual.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

This value is always false.Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

Indicates whether the location is in a state or province.Possible values:

-   state
-   province

Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

Describes the street.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Complementary street description.Data type: String

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

Relative link to the user or consumer or contact record.Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

name

</td><td>

User name of the user or contact individual.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristics

</td><td>

List of characteristics associated with the party.Data type: Array of Objects

```
"partyCharacteristics": [
 {
  "@type": "String",
  "name": " String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristics.@type

</td><td>

When subclassing, this parameter defines the subclass extensible name.Possible values:

-   StringCharacteristic
-   StringArrayCharacteristic
-   IntegerCharacteristic
-   BooleanCharacteristic

Data type: String

</td></tr><tr><td>

partyCharacteristics.name

</td><td>

Name of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.value

</td><td>

Value of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.valueType

</td><td>

Data type of the characteristic's value.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Roles related to this party are defined where the party is created in table. For example, `User`, `Consumer`, `Customer Contact`.**partyOrPartyRole** indicates which type of record is retrieved in the operation. If the provided sys\_id belongs to the Consumer \[csm\_consumer\] table, then **partyOrPartyRole.role** is set to `Consumer`. Likewise, if the sys\_id belongs to the Contact \[customer\_contact\] table, then **partyOrPartyRole.role** is set to `Contact`.

Data type: Object

```
"partyOrPartyRole":
{
  "@type": "String",
  "role":"String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

This value is always `Party`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Type of the role. Possible values:

-   Consumer
-   Contact

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties and party roles related to this party.Data type: Array of Objects

```
"relatedParty": [
  {
    "role": "String",
    "partyOrPartyRole": {Object}
  }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Possible value for user:

-   Organization
-   Individual

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

ID for the linked entity in the Party Management or Party Role Management system.

-   Possible value for user:
    -   `Company`
    -   `Department`
-   Possible value for customer: `Account`
-   Possible value for consumer: `User`

 Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Business role that the related party plays in the context of the current entity.Possible values:

-   Company \(if related party is User\)
-   Department \(if related party is User\)
-   Account \(if related party is Customer\)
-   User \(if related party is Consumer\)

Data type: String

</td></tr><tr><td>

status

</td><td>

Flag that indicates the status of the individual.Valid values:

-   active: Individual is in an active status.
-   inactive: Individual isn't in an active status.

Data type: Boolean

</td></tr><tr><td>

title

</td><td>

Prefix or title of the individual. For example, `Dr.`, `Mr.`, `Ms.`\).Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

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

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

<table id="id_vql_zm4_3hc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contactMedium

</td><td>

List of means for contacting the party. Data type: Array of Objects

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

Type of contacting party. Indicates the specific schema or subclass type of the object.Possible values:

-   BusinessPhoneContactMedium: Business phone number
-   EmailContactMedium: Email address
-   FaxPhoneContactMedium: Fax number
-   GeographicAddressContactMedium: Physical address \(street, city, state, postal code\)
-   HomePhoneContactMedium: Home phone number
-   MobilePhoneContactMedium: Mobile number

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the individual. Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the individual.Data type: String

</td></tr><tr><td>

contactMedium.emailAddress

</td><td>

Email address of the contact.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the party location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

The type of contact medium. Indicates the business-level attribute that specifies the kind of contact channel being used.Possible values:

-   email
-   businessPhone
-   homePhone
-   mobilePhone
-   postalAddress

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone number of the individual.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postcode of the individual.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

This value is always false.Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

Indicates whether the location is from a state or province.Possible values:

-   state
-   province

Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

Describes the street.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Complementary street description.Data type: String

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

Relative link to the user or consumer or contact record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the user or consumer or contact record to retrieve.Tables: Consumer \[csm\_consumer\] or Contact \[customer\_contact\]

Data type: String

</td></tr><tr><td>

middleName

</td><td>

Middle name of the individual.Data type: String

</td></tr><tr><td>

name

</td><td>

User name of the user or contact individual.Data type: String

</td></tr><tr><td>

nationality

</td><td>

Nationality of the individual.Data type: String

</td></tr><tr><td>

partyCharacteristics

</td><td>

List of characteristics associated with the party.Data type: Array of Objects

```
"partyCharacteristics": [
 {
  "@type": "String",
  "name": " String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

partyCharacteristics.@type

</td><td>

When subclassing, this defines the subclass extensible name.Possible values:

-   StringCharacteristic
-   StringArrayCharacteristic
-   IntegerCharacteristic
-   BooleanCharacteristic

Data type: String

</td></tr><tr><td>

partyCharacteristics.name

</td><td>

Name of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.value

</td><td>

Value of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.valueType

</td><td>

Data type of the characteristic's value.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Roles related to this party are defined where the party is created in table. For example, `User`, `Consumer`, `Customer Contact`.**partyOrPartyRole** indicates which type of record is retrieved in the operation. If the provided sys\_id belongs to the Consumer \[csm\_consumer\] table, then **partyOrPartyRole.role** is set to `Consumer`. Likewise, if the sys\_id belongs to the Contact \[customer\_contact\] table, then **partyOrPartyRole.role** is set to `Contact`.

Data type: Object

```
"partyOrPartyRole":
{
  "@type": "String",
  "role":"String"
}
```

</td></tr><tr><td>

partyOrPartyRole.@type

</td><td>

This value is always `Party`.Data type: String

</td></tr><tr><td>

partyOrPartyRole.role

</td><td>

Type of party role. Possible values:

-   Consumer
-   Contact

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties or party roles related to this party.Data type: Array of Objects

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

Represents information about the related party and the role it plays in the context of the record. For example, if the role is `Company`, then **partyOrPartyRole.id** contains the sys\_id of the Company \[core\_company\] record, and **partyOrPartyRole.name** contains the company’s name. This structure ensures that both the party reference and its role are explicitly defined and easily identifiable.

Data type: Object

```
"partyOrPartyRole":
{
  "@type": "String",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Possible value for user:

-   Organization
-   Individual

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related party.-   Possible value for `user`:
    -   Company
    -   Department
-   Possible value for `customer`: Account
-   Possible value for `consumer`: User

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Business role that the related party plays in the context of the current entity.Possible values:

-   Company \(if related party is User\)
-   Department \(if related party is User\)
-   Account \(if related party is Customer\)
-   User \(if related party is Consumer\)

Data type: String

</td></tr><tr><td>

status

</td><td>

Flag that indicates the status of the individual.Valid values:

-   active: Individual is in an active status.
-   inactive: Individual is in an inactive status.

Data type: Boolean

</td></tr><tr><td>

title

</td><td>

Prefix or title of the individual. For example, `Dr.`, `Mr.`, `Ms.`\).Data type: String

</td></tr></tbody>
</table>### cURL request

This returns specified fields for the party management individual records.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/v1/party/individual" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--user 'user':'password'
--data "{
    \"id\": \"98765\",
    \"name\": \"Jane Smith\",
    \"givenName\": \"Jane\",
    \"middleName\": \"B.\",
    \"familyName\": \"Smith\",
    \"gender\": \"female\",
    \"nationality\": \"American\",
    \"title\": \"Ms\",
    \"contactMedium\": [
      {
        \"preferred\": true,
        \"mediumType\": \"email\",
        \"emailAddress\": \"jane.smith@example.com\",
        \"@type\": \"EmailContactMedium\"
      },
      {
        \"preferred\": false,
        \"mediumType\": \"mobilePhone\",
        \"phoneNumber\": \"+1-416-555-1234\",
        \"@type\": \"PhoneContactMedium\"
      },
      {
        \"preferred\": false,
        \"mediumType\": \"businessPhone\",
        \"phoneNumber\": \"+1-416-555-5678\",
        \"@type\": \"BusinessPhoneContactMedium\"
      },
      {
        \"preferred\": false,
        \"mediumType\": \"fax\",
        \"fax\": \"987654321\",
        \"@type\": \"FaxContactMedium\"
      },
      {
        \"preferred\": false,
        \"mediumType\": \"homePhone\",
        \"phoneNumber\": \"+1-416-555-4321\",
        \"@type\": \"HomePhoneContactMedium\"
      },
      {
        \"preferred\": false,
        \"mediumType\": \"postalAddress\",
        \"@type\": \"GeographicAddressContactMedium\",
        \"locationId\": \"12345678901234567\",
        \"city\": \"Toronto\",
        \"country\": \"Canada\",
        \"postCode\": \"M5H 2N2\",
        \"stateOrProvince\": \"Ontario\",
        \"street1\": \"123 Queen St W\",
        \"street2\": \"Suite 1500\"
      }
    ],
    \"externalReference\": [
      {
        \"externalIdentifierType\": \"linkedin\",
        \"id\": \"http://linkedin.com/in/janesmith\"
      }
    ],
    \"partyCharacteristic\": [
      {
        \"name\": \"notes\",
        \"value\": \"General consumer information.\",
        \"valueType\": \"string\",
        \"@type\": \"string\"
      },
      {
        \"name\": \"userName\",
        \"value\": \"janesmith\",
        \"valueType\": \"string\",
        \"@type\": \"string\"
      },
      {
        \"name\": \"vip\",
        \"value\": false,
        \"valueType\": \"boolean\",
        \"@type\": \"string\"
      },
      {
        \"name\": \"source\",
        \"value\": \"CRM System\",
        \"valueType\": \"string\",
        \"@type\": \"string\"
      },
      {
        \"name\": \"dateFormat\",
        \"value\": \"yyyy-mm-dd\",
        \"valueType\": \"string\",
        \"@type\": \"string\"
      },
      {
        \"name\": \"timeformat\",
        \"value\": \"HH:mm:ss (24 hour)\",
        \"valueType\": \"string\",
        \"@type\": \"string\"
      },
      {
        \"name\": \"notification\",
        \"value\": \"Disabled\",
        \"valueType\": \"string\",
        \"@type\": \"string\"
      }
    ],
    \"relatedParty\": [
      {
        \"role\": \"User\",
        \"partyOrPartyRole\": {
          \"id\": \"c456def03710200044e0bfc8bcbe5d99\",
          \"name\": \"Global Corp\",
          \"@type\": \"Individual\"
        }
      }
    ],
    \"status\": \"active\",
    \"@type\": \"Individual\",
    \"partyOrPartyRole\": {
      \"role\": \"Consumer\",
      \"@type\": \"Party\"
    }
  }" \

```

Response body.

```
{
  "id": "83e588a17b6062105e0d5494548cb65d",
"href": "api/sn_tmf_api/party/individual/83e588a17b6062105e0d5494548cb65d",
  "name": "Jane Smith",
  "givenName": "Jane",
  "middleName": "B.",
  "familyName": "Smith",
  "gender": "female",
  "nationality": "American",
  "title": "Ms",
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
      "mediumType": "fax",
      "fax": "987654321",
      "@type": "FaxContactMedium"
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
      "@type": "string"
    },
    {
      "name": "userName",
      "value": "janesmith",
      "valueType": "string",
      "@type": "string"
    },
    {
      "name": "vip",
      "value": false,
      "valueType": "boolean",
      "@type": "string"
    },
    {
      "name": "source",
      "value": "CRM System",
      "valueType": "string",
      "@type": "string"
    },
    {
      "name": "dateFormat",
      "value": "yyyy-mm-dd",
      "valueType": "string",
      "@type": "string"
    },
    {
      "name": "timeformat",
      "value": "HH:mm:ss (24 hour)",
      "valueType": "string",
      "@type": "string"
    },
    {
      "name": "notification",
      "value": "Disabled",
      "valueType": "string",
      "@type": "string"
    }
  ],
  "relatedParty": [
    {
      "role": "User",
      "partyOrPartyRole": {
        "id": "c456def03710200044e0bfc8bcbe5d99",
        "name": "Global Corp",
        "@type": "Individual"
      }
    }
  ],
  "status": "active",
  "@type": "Individual",
  "partyOrPartyRole": {
    "role": "Consumer",
    "@type": "Party"
  },
   "warning": [
    "relatedParty[0] is incorrect. User does not exist"
  ]
}
```

## Party Management - POST /api/sn\_tmf\_api/v1/party/organization

Creates a new party organization record in the Account \[customer\_account\] tables.

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

<table id="id_gby_knj_jhc" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

This value is always `Organization`.Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of means for contacting the party. A contact medium represents the way you communicate with or reach a party like an individual or organization. For example, a channel or method of contact associated with that party.Data type: Array of Objects

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

Type of contact medium. Type of contacting party. Indicates the specific schema or subclass type of the object.Possible values:

-   BusinessPhoneContactMedium: Business phone number
-   EmailContactMedium: Email address
-   FaxPhoneContactMedium: Fax number
-   GeographicAddressContactMedium: Physical address \(street, city, state, postal code\)
-   HomePhoneContactMedium: Home phone number
-   MobilePhoneContactMedium: Mobile number

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the organization.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the organization.Data type: String

</td></tr><tr><td>

contactMedium.emailAdress

</td><td>

Email address of the organization contact.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

The type of contact medium. Possible values:

-   businessPhone
-   email
-   faxPhone
-   homePhone
-   mobilePhone
-   postalAddress

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone number of the organization contact.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postcode of the organization.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

This value is always `false`.Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

Indicates whether the location is from a state or province.Possible values:

-   state
-   province

Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

Describes the street.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Complementary street description.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the party in an external system.Data type: Array of Objects

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

Type of entity within the external system.Data type: String

</td></tr><tr><td>

externalReference.name

</td><td>

Human-readable name of the external system or reference.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the account record \(URI\).Table: Account \[customer\_account\]

Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the external entity account record.Table: Account \[customer\_account\]

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

partyCharacteristics

</td><td>

List of characteristics that a party can take on. Data type: Array of Objects

```
"partyCharacteristics": [ 
 { 
  "@type": "String" 
  "name": "String",   
  "value": "String", 
  "valueType": "String"
 } 
]
```

</td></tr><tr><td>

partyCharacteristics.@type

</td><td>

When subclassing, **@type** defines the subclass extensible name.Possible value:

-   BooleanCharacteristic
-   IntegerCharacteristic
-   StringArrayCharacteristic
-   StringCharacteristic

Data type: String

</td></tr><tr><td>

partyCharacteristics.name

</td><td>

Name of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.value

</td><td>

Value of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.valueType

</td><td>

Data type of the characteristic's value.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Roles related to this party are defined where the party is created in the table. For example, `Company` or `Account`.**partyOrPartyRole** indicates which type of record is retrieved in the operation. If the provided sys\_id belongs to the Account \[customer\_account\] table, then **partyOrPartyRole.role** is set to `Account`. Likewise, if the sys\_id belongs to the Company \[core\_company\] table, then **partyOrPartyRole.role** is set to `Company`.

Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "name":"String",
  "role":"String",
}
```

</td></tr><tr><td>

PartyOrPartyRole.@type

</td><td>

This value is always `party`.Data type: String

</td></tr><tr><td>

PartyOrPartyRole.name

</td><td>

Defines the type of the account or company.Data type: String

</td></tr><tr><td>

PartyOrPartyRole.role

</td><td>

Type of the role.Possible value:

-   Account
-   Company

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties or party roles related to this party.Data type: Array of Objects

```
"relatedParty": [ 
 { 
  "partyOrPartyRole": {Object},
  "role": "String"
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Roles related to this party.Data type: Array of Objects

```
"partyOrPartyRole": [ 
 { 
  "@type": "String", 
  "id": "String",
  "name": "String",
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Value is always `Organization`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related party. Possible value:

-   Contact
-   Other

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role played by the related party or party role in the context of the specific entity it's linked to. Possible values:

-   Contact
-   Other

Data type: String

</td></tr><tr><td>

status

</td><td>

Flag that indicates the status of organization.Valid values:

-   active: Organization is active.
-   inactive: Organization is inactive.

Data type: Boolean

</td></tr><tr><td>

tradingName

</td><td>

Name that the organization trades under.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

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

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

### Response body parameters \(JSON or XML\)

<table id="table_edn_qnn_3hc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

This value is always `Organization`.Data type: String

</td></tr><tr><td>

contactMedium

</td><td>

List of means for contacting the party. A contact medium represents the way you communicate with or reach a party like an individual or organization. For example, a channel or method of contact associated with that party.Data type: Array of Objects

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

Type of contact medium. Type of contacting party. Indicates the specific schema or subclass type of the object.Possible values:

-   BusinessPhoneContactMedium: Business phone number
-   EmailContactMedium: Email address
-   FaxPhoneContactMedium: Fax number
-   GeographicAddressContactMedium: Physical address \(street, city, state, postal code\)
-   HomePhoneContactMedium: Home phone number
-   MobilePhoneContactMedium: Mobile number

Data type: String

</td></tr><tr><td>

contactMedium.city

</td><td>

City of the organization.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country of the organization.Data type: String

</td></tr><tr><td>

contactMedium.emailAdress

</td><td>

Email address of the organization contact.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

The type of contact medium. Possible values:

-   businessPhone
-   email
-   faxPhone
-   homePhone
-   mobilePhone
-   postalAddress

Data type: String

</td></tr><tr><td>

contactMedium.phoneNumber

</td><td>

Phone number of the organization contact.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postcode of the organization.Data type: String

</td></tr><tr><td>

contactMedium.preferred

</td><td>

This value is always `false`.Data type: Boolean

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

Indicates whether the location is from a state or province.Possible values:

-   state
-   province

Data type: String

</td></tr><tr><td>

contactMedium.street1

</td><td>

Describes the street.Data type: String

</td></tr><tr><td>

contactMedium.street2

</td><td>

Complementary street description.Data type: String

</td></tr><tr><td>

externalReference

</td><td>

List of identifiers of the party in an external system.Data type: Array of Objects

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

Type of entity within the external system.Data type: String

</td></tr><tr><td>

externalReference.name

</td><td>

Human-readable name of the external system or reference.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the account record \(URI\).Table: Account \[customer\_account\]

Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the external entity account record.Table: Account \[customer\_account\]

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

partyCharacteristics

</td><td>

List of characteristics that a party can take on. Data type: Array of Objects

```
"partyCharacteristics": [ 
 { 
  "@type": "String" 
  "name": "String",   
  "value": "String", 
  "valueType": "String"
 } 
]
```

</td></tr><tr><td>

partyCharacteristics.@type

</td><td>

When subclassing, **@type** defines the subclass extensible name.Possible value:

-   BooleanCharacteristic
-   IntegerCharacteristic
-   StringArrayCharacteristic
-   StringCharacteristic

Data type: String

</td></tr><tr><td>

partyCharacteristics.name

</td><td>

Name of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.value

</td><td>

Value of the party characteristic.Data type: String

</td></tr><tr><td>

partyCharacteristics.valueType

</td><td>

Data type of the characteristic's value.Data type: String

</td></tr><tr><td>

partyOrPartyRole

</td><td>

Roles related to this party are defined where the party is created in the table. For example, `Company` or `Account`.**partyOrPartyRole** indicates which type of record is retrieved in the operation. If the provided sys\_id belongs to the Account \[customer\_account\] table, then **partyOrPartyRole.role** is set to `Account`. Likewise, if the sys\_id belongs to the Company \[core\_company\] table, then **partyOrPartyRole.role** is set to `Company`.

Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "name":"String",
  "role":"String",
}
```

</td></tr><tr><td>

PartyOrPartyRole.@type

</td><td>

This value is always `party`.Data type: String

</td></tr><tr><td>

PartyOrPartyRole.name

</td><td>

Defines the type of the account or company.Data type: String

</td></tr><tr><td>

PartyOrPartyRole.role

</td><td>

Type of the role.Possible value:

-   Account
-   Company

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties or party roles related to this party.Data type: Array of Objects

```
"relatedParty": [ 
 { 
  "partyOrPartyRole": {Object},
  "role": "String"
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Roles related to this party.Data type: Array of Objects

```
"partyOrPartyRole": [ 
 { 
  "@type": "String", 
  "id": "String",
  "name": "String",
 }
]
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Type of the related party. Value is always `Organization`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the related party. Possible value:

-   Contact
-   Other

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role played by the related party or party role in the context of the specific entity it's linked to. Possible values:

-   Contact
-   Other

Data type: String

</td></tr><tr><td>

status

</td><td>

Flag that indicates the status of organization.Valid values:

-   active: Organization is active.
-   inactive: Organization is inactive.

Data type: Boolean

</td></tr><tr><td>

tradingName

</td><td>

Name that the organization trades under.Data type: String

</td></tr></tbody>
</table>### cURL request

This returns specified fields for the party management organization records.

```
curl "http://instance.service-now.com/api/sn_tmf_api/v1/party/organization" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--user 'user':'password'
--data "{
  \"name\": \"SERVICENOW 144\",
  \"legalName\": \"Acme Corp Ltd.\",
  \"tradingName\": \"Acme Inc.\",
  \"contactMedium\": [
    {
      \"preferred\": true,
      \"mediumType\": \"email\",
      \"emailAddress\": \"athammhd@email.com\",
      \"@type\": \"EmailContactMedium\"
    },
    {
      \"preferred\": false,
      \"mediumType\": \"phone\",
      \"phoneNumber\": \"+1-202-555-0198\",
      \"@type\": \"PhoneContactMedium\"
    },
    {
      \"preferred\": false,
      \"mediumType\": \"businessPhone\",
      \"phoneNumber\": \"+1-202-555-0198\",
      \"@type\": \"BusinessPhoneContactMedium\"
    },
    {
      \"preferred\": false,
      \"mediumType\": \"homePhone\",
      \"phoneNumber\": \"+1-202-555-0198\",
      \"@type\": \"HomePhoneContactMedium\"
    },
    {
      \"preferred\": false,
      \"mediumType\": \"postalAddress\",
      \"validFor\": {
        \"startDateTime\": \"2017-03-15T07:49:25.246Z\"
      },
      \"@type\": \"GeographicAddressContactMedium\",
      \"city\": \"chennai\",
      \"country\": \"INDIA\",
      \"postCode\": \"608001\",
      \"stateOrProvince\": \"tamil nadu\",
      \"street1\": \"samcon street\",
      \"street2\": \"adyar,chennai\"
    }
  ],
  \"externalReference\": [
    {
      \"externalIdentifierType\": \"Instagram\",
      \"id\": \"Instagram\"
    }
  ],
  \"partyCharacteristic\": [
    {
      \"name\": \"notes\",
      \"value\": \"Testing for update the notes\",
      \"valueType\": \"string\",
      \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"customer\",
      \"value\": \"true\",
      \"valueType\": \"boolean\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"registrationCode\",
      \"value\": \"001\",
      \"valueType\": \"string\",
       \"@type\": \"StringCharacteristics\"
    },
    {
     \"name\": \"vendorType\",
     \"value\": [\"Hardware\"],
     \"valueType\": \"array\",
      \"@type\": \"StringArrayCharacteristic\"
     },
     {
      \"name\": \"industry\",
      \"value\": \"technology_services\",
      \"valueType\": \"choice\",
        \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"taxId\",
      \"value\": \"CTNUM1000123\",
      \"valueType\": \"string\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"numEmployees\",
      \"value\": \"EMP1000\",
      \"valueType\": \"integer\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"rankTier\",
      \"value\": \"rankTier\",
      \"valueType\": \"string\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"publiclyTraded\",
      \"value\": \"false\",
      \"valueType\": \"boolean\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"stockSymbol\",
      \"value\": \"Market\",
      \"valueType\": \"string\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"stockPrice\",
      \"value\": \"1000\",
      \"valueType\": \"string\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"vendor\",
      \"value\": \"false\",
      \"valueType\": \"boolean\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"manufacturer\",
      \"value\": \"false\",
      \"valueType\": \"boolean\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"marketCap\",
      \"value\": \"0\",
      \"valueType\": \"currency\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"profits\",
      \"value\": \"0\",
      \"valueType\": \"currency\",
       \"@type\": \"StringCharacteristics\"
    },
    {
      \"name\": \"revenuePerYear\",
      \"value\": \"0\",
      \"valueType\": \"currency\",
       \"@type\": \"StringCharacteristics\"
    }
  ],
  \"relatedParty\": [
    {
      \"role\": \"primaryContact\",
      \"partyOrPartyRole\": {
        \"id\": \"eaf68911c35420105252716b7d40ddde\",
        \"name\": \"John Doe\",
        \"@type\": \"Individual\"
      }
    },
    {
      \"role\": \"other\",
      \"partyOrPartyRole\": {
        \"id\": \"776a22ea11f43110f877366201dea6b7\",
        \"name\": \"Mary Star\",
        \"@type\": \"Individual\"
      }
    }
  ],
  \"organizationChildRelationship\": [
    {
      \"relationshipType\": \"partneraccount\",
      \"organization\": {
        \"id\": \"0fef075b2fe06a10b79db3bf42faf31a\",
        \"name\": \"mhd\",
        \"@type\": \"Organization\"
      }
    }
  ],
  \"organizationParentRelationship\": 
    {
      \"relationshipType\": \"Account\",
      \"organization\": {
        \"id\": \"9e2fd2ee11b43110f877366201dea674\",
        \"name\": \"Global Holdings Ltd.\",
        \"@type\": \"Organization\"
      }
    },
  \"status\": \"active\",
  \"@type\": \"Organization\",
  \"partyOrPartyRole\": {
    \"@type\":\"Party\",
    \"name\":\"Customer\",
    \"role\": \"Account\" 
  }
}" \
```

Response body.

```
{
   "name": "SERVICENOW 144",
   "legalName": "Acme Corp Ltd.",
   "tradingName": "Acme Inc.",
   "contactMedium": [
     {
       "preferred": true,
       "mediumType": "email",
       "emailAddress": "athammhd@email.com",
       "@type": "EmailContactMedium"
     },
     {
       "preferred": false,
       "mediumType": "phone",
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
       "name": "customer",
       "value": "true",
       "valueType": "boolean",
        "@type": "StringCharacteristics"
     },
     {
       "name": "registrationCode",
       "value": "001",
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
       "value": "technology_services",
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
       "value": "EMP1000",
       "valueType": "integer",
        "@type": "StringCharacteristics"
     },
     {
       "name": "rankTier",
       "value": "rankTier",
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
       "relationshipType": "partneraccount",
       "organization": {
         "id": "0fef075b2fe06a10b79db3bf42faf31a",
         "name": "mhd",
         "@type": "Organization"
       }
     }
   ],
   "organizationParentRelationship": 
     {
       "relationshipType": "Account",
       "organization": {
         "id": "9e2fd2ee11b43110f877366201dea674",
         "name": "Global Holdings Ltd.",
         "@type": "Organization"
       }
     },
   "status": "active",
   "@type": "Organization",
   "partyOrPartyRole": {
     "@type":"Party",
     "name":"Customer",
     "role": "Account" 
   }
 }
```

