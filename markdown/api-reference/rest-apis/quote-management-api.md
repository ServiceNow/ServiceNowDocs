---
title: Quote Management API
description: The Quote Management API provides endpoints to create, update, and retrieve customer quote data.Deletes the specified quote.Retrieves all quotes.Retrieves a specified quote.Updates the specified quote.Creates a quote.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 42
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Quote Management API

The Quote Management API provides endpoints to create, update, and retrieve customer quote data.

The Quote Management Open API is a ServiceNow implementation of the TM Forum Quote Management API REST specification. This implementation is based on [https://www.tmforum.org/resources/standard/tmf648-quote-management-api-rest-specification-r19-0-0/](https://www.tmforum.org/resources/standard/tmf648-quote-management-api-rest-specification-r19-0-0/).

This API can be extended to make customizations around required parameters, request body validation, additional REST operations and field mappings.

The Quote Management API requires the Quote Management \(com.sn\_quote\_mgmt\) plugin and the quote\_integrator role. This API belongs to the sn\_tmf\_api namespace. See [Quote Management](https://www.servicenow.com/docs/access?context=quote-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US).

The Quote Management API creates or updates data in the following tables:

-   Quote \[sn\_quote\_mgmt\_core\_quote\]
-   Sales Agreement \[sn\_sales\_agmt\_core\_sales\_agreement\]
-   Quote Line Item \[sn\_quote\_mgmt\_core\_quote\_line\_item\]
-   Quote Line Characteristic \[sn\_quote\_mgmt\_core\_quote\_line\_characteristic\]
-   Quote Pricing Adjustment \[sn\_quote\_mgmt\_core\_pricing\_adjustment\]

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Quote Management API - DELETE /sn\_tmf\_api/quote\_management\_api/quote/\{id\}

Deletes the specified quote.

### URL format

Versioned URL: `/api/sn_tmf_api/{api_version}/quote_management_api/quote/{id}`

Default URL: `/api/sn_tmf_api/quote_management_api/quote/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the quote to delete.Data type: String

Table: Quote \[sn\_quote\_mgmt\_core\_quote\]

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
|204|Successful. Request completed successfully and the specified quote was deleted. No content.|
|400|Bad Request. A bad request type or malformed request was detected.|

### Response body parameters \(JSON\)

|Header|Description|
|------|-----------|
|None| |

### cURL request

This example shows how to delete a quote.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/quote_management_api/quote/cb15734fd5692a10f8774663edf0ac19" \ 
--request DELETE\ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

## Quote Management API – GET /sn\_tmf\_api/quote\_management\_api/quote

Retrieves all quotes.

This API retrieves quote information from the following related tables:

-   Quote \[sn\_quote\_mgmt\_core\_quote\]
-   Sales Agreement \[sn\_sales\_agmt\_core\_sales\_agreement\]
-   Quote Line Item \[sn\_quote\_mgmt\_core\_quote\_line\_item\]
-   Quote Line Characteristic \[sn\_quote\_mgmt\_core\_quote\_line\_characteristic\]
-   Quote Pricing Adjustment \[sn\_quote\_mgmt\_core\_pricing\_adjustment\]

### URL format

Versioned URL: `/api/sn_tmf_api/{api_version}/quote_management_api/quote`

Default URL: `/api/sn_tmf_api/quote_management_api/quote`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table id="table_pfr_vgy_fsb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. Valid fields:

-   quoteNumber
-   href
-   id
-   description
-   externalId
-   expectedQuoteCompletionDate
-   version
-   @type

Data type: String

Default: All fields returned.

</td></tr><tr><td>

id

</td><td>

Filter results by quote sys\_id.Table: Quote \[sn\_quote\_mgmt\_core\_quote\]

Data type: String

Default: Empty

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval. Data type: Number

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

|Header|Description|
|------|-----------|
|None| |

<table id="table_h4r_fxr_nsb" class="rest_api_response_headers"><thead><tr><th>

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

<table id="table_abf_sn5_4sb"><thead><tr><th>

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

<table id="table_jlb_1qx_kqb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contactMedium

</td><td>

List of contact mediums. Contact information related to the quote requester.```
"contactMedium": [
 {
  "city": "String",
  "country": "String",
  "locationId": "String",
  "mediumType": "String",
  "postCode": "String",
  "stateOrProvince": "String",
  "street": "String",
  "@type": "String"
 }
]
```

</td></tr><tr><td>

contactMedium.city

</td><td>

City in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location listed in the Location \[cmn\_location\] table or custom address.Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact medium, such as email address, telephone number, or postal address.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the quote requester.Data type: String

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

State or province in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.street

</td><td>

Street address of the quote requester.Data type: String

</td></tr><tr><td>

contactMedium.@type

</td><td>

Type of medium per the TMF Open API standard. For example, `GeographicalAddressContactMedium`.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the quote.Data type: String

</td></tr><tr><td>

expectedQuoteCompletionDate

</td><td>

The expected date from quote supplier to be able to send back a response for this quote.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Unique consumer-provided ID for the quote.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to access the quote.Data type: String

Default: Empty string

</td></tr><tr><td>

id

</td><td>

Sys\_id of the requested quote.Table: Quote \[sn\_quote\_mgmt\_core\_quote\]

Data type: String

</td></tr><tr><td>

note

</td><td>

List of notes associated with the quote. Data type: Array

```
"note": [
  {
    "author": "String",
    "date": "String",
    "text": "String",
    "@type": "String"
 }
]
```

</td></tr><tr><td>

note.author

</td><td>

User name of the person that authored the associated note.Data type: String

</td></tr><tr><td>

note.date

</td><td>

Date that the note was created.Data type: String

</td></tr><tr><td>

note.text

</td><td>

Contents of the note. Data type: String

</td></tr><tr><td>

note.@type

</td><td>

This value is always `Note`.Data type: String

</td></tr><tr><td>

quoteDate

</td><td>

Date and time at which the quote was created.Data type: String

</td></tr><tr><td>

quoteItem

</td><td>

A list of quote items. Each quote item describes an action for a product to be quoted.```
"quoteItem": [
 {
  "action": "String",
  "id": "String",
  "product": {Object},
  "productOffering": {Object},
  "quantity": Number,
  "state": "String",
  "@type": "String"
 }
]
```

Data type: Array of Objects

</td></tr><tr><td>

quoteItem.action

</td><td>

Action to be performed on this quote item \(add, modify, remove, etc.\).Data type: String

</td></tr><tr><td>

quoteItem.id

</td><td>

Sys\_id of the quote item.Table: Quote Line Item \[sn\_quote\_mgmt\_core\_quote\_line\_item\]

Data type: String

</td></tr><tr><td>

quoteItem.product

</td><td>

List of products included in the quote.```
"product": {
  "characteristic": "String",
  "specification": "String",
  "@type": "String"
}
```

Data type: Object

</td></tr><tr><td>

quoteItem.product. characteristic

</td><td>

List of product characteristics.Data type: Array of Objects

```
"characteristic": [
  {
    "id": "String",
    "name": "String",
    "@type": "String",
    "value": "String"
  }
]
```

See [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=zurich&pubname=zurich-order-management&ft:locale=en-US).

</td></tr><tr><td>

quoteItem.product. characteristic.id

</td><td>

Sys\_id of the product characteristic.Table: Quote Line Characteristic \[sn\_quote\_mgmt\_core\_quote\_line\_characteristic\]

Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.name

</td><td>

Name of the product characteristic.Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.@type

</td><td>

This value is always `StringCharacteristic`.Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

quoteItem.product. specification

</td><td>

Detailed description of a tangible or intangible object made available externally in the form of a ProductOffering to customers or other parties playing a party role.Data type: String

</td></tr><tr><td>

quoteItem.product.@type

</td><td>

This value is always `Product`.Data type: String

</td></tr><tr><td>

quoteItem.productOffering

</td><td>

A product offering reference \(ProductOfferingRef\). A product offering represents entities that are orderable from the provider of the catalog.```
"productOffering": {
  "href": "String",
  "name": "String",
  "name": "String",
  "@type": "String"
}
```

Data type: Object

</td></tr><tr><td>

quoteItem. productOffering.href

</td><td>

Reference of the related entity.Data type: String

</td></tr><tr><td>

quoteItem. productOffering.id

</td><td>

Sys\_id of product offering.Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

Data type: String

</td></tr><tr><td>

quoteItem. productOffering.name

</td><td>

Name of the related entity.Data type: String

</td></tr><tr><td>

quoteItem. productOffering.@type

</td><td>

This value is always `ProductOfferingRef`.Data type: String

</td></tr><tr><td>

quoteItem.quantity

</td><td>

Quantity asked for this quote item.Data type: Number

</td></tr><tr><td>

quoteItem.state

</td><td>

A quote state type \(QuoteStateType\). State of the quote.Data type: String

</td></tr><tr><td>

quoteItem.@type

</td><td>

This value is always `QuoteItem`.Data type: String

</td></tr><tr><td>

quoteNumber

</td><td>

Quote line item record number assigned to the quote.Table: Quote Line Item \[sn\_quote\_mgmt\_core\_quote\_line\_item\]

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order.Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String",
    "role": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the quote table to get the account, contact, or customer.Table: Quote \[sn\_quote\_mgmt\_core\_quote\]

 Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

The role of the party in the context of the quote \(e.g., Account, Contact, or Customer\).Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

This value is always `ProductOfferingRef`.Data type: String

</td></tr><tr><td>

requestedQuoteCompletionDate

</td><td>

A date time \(DateTime\). This value represents the date specified by the quote requester by which to receive a complete response for this quote.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the quote item.Data type: String

</td></tr><tr><td>

@type

</td><td>

Type of resource. This value is always `Quote`. This information isn’t stored.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves all quotes.

```
curl "https://instance.service-now.com/api/sn_tmf_api/quote_management_api/quote" \
--request GET \
--header "Accept:application/json" \
--user 'userName':'password'
```

Response body.

```
{
  "id": "47e562bad565a610f8774663edf0ac10",
  "quoteNumber": "QT0001001",
  "href": "api/sn_tmf_api/quote_management_api/quote/47e562bad565a610f8774663edf0ac10",
  "@type": "Quote",
  "description": "Testing Quote",
  "expectedQuoteCompletionDate": "2025-05-23 11:12:08",
  "externalId": "Test_1234",
  "quoteDate": "2025-05-20 11:11:13",
  "requestedQuoteCompletionDate": "2025-05-23 11:12:08",
  "version": "3",
  "agreement": [],
  "contactMedium": [
    {
      "@type": "GeographicalAddressContactMedium",
      "mediumType": "ShippingAddressRef",
      "locationId": "6774fee611383110f877366201dea64f",
      "city": "Santa Clara",
      "country": "USA",
      "postCode": "94560",
      "stateOrProvince": "CA",
      "street": "222 Star St"
    }
  ],
  "note": [],
  "quoteItem": [
    {
      "id": "8be562bad565a610f8774663edf0ac16",
      "@type": "QuoteItem",
      "action": "add",
      "quantity": "1",
      "state": "Draft",
      "product": {
        "@type": "Product",
        "productCharacteristic": [
          {
            "id": "0fe562bad565a610f8774663edf0ac17",
            "name": "Voice Pack",
            "value": "1500 Minutes/Month"
          },
          {
            "id": "4be562bad565a610f8774663edf0ac17",
            "name": "SMS Pack",
            "value": "700 /Month"
          },
          {
            "id": "83e562bad565a610f8774663edf0ac18",
            "name": "Data Pack",
            "value": "20 GB/Month"
          },
          {
            "id": "87e562bad565a610f8774663edf0ac17",
            "name": "Mobile Number",
            "value": ""
          },
          {
            "id": "cfe562bad565a610f8774663edf0ac17",
            "name": "Shipping Address",
            "value": ""
          }
        ],
        "productSpecification": {
          "id": "3ee1fdb1c3331010d216b5183c40dd81",
          "href": "api/sn_tmf_api/catalogmanagement/productSpecification/3ee1fdb1c3331010d216b5183c40dd81",
          "name": "Mobile Plan",
          "@type": "ProductSpecificationRef"
        }
      },
      "productOffering": {
        "id": "2cb5588fc30020105252716b7d40dddd",
        "href": "api/sn_tmf_api/catalogmanagement/productOffering/2cb5588fc30020105252716b7d40dddd",
        "name": "All in one mobile plan starting from $49/month",
        "@type": "ProductOfferingRef"
      },
      "quoteItemPrice": [
        {
          "description": "Standard Price List",
          "name": "Standard Price List",
          "priceType": "Recurring",
          "recurringChargePeriod": "",
          "unitOfMeasure": "",
          "unitMarginPercentage": "",
          "price": {
            "totalOneTimePrice": {
              "unit": "USD",
              "value": 0
            },
            "monthlyRecurringPrice": {
              "unit": "USD",
              "value": 0
            },
            "annualRecurringPrice": {
              "unit": "USD",
              "value": 0
            },
            "cumulativeRecurringPrice": {
              "unit": "USD",
              "value": 0
            },
            "cumulativeAnnualRecurringPrice": {
              "unit": "USD",
              "value": 0
            },
            "cumulativeNetPrice": {
              "unit": "USD",
              "value": 0
            },
            "unitMarginAmount": {
              "unit": "USD",
              "value": 0
            },
            "unitMarginBasePrice": {
              "unit": "USD",
              "value": 0
            },
            "listPrice": {
              "unit": "USD",
              "value": 0
            },
            "unitCost": {
              "unit": "USD",
              "value": 0
            },
            "unitPrice": {
              "unit": "USD",
              "value": 0
            },
            "dutyFreeAmount": {
              "unit": "USD",
              "value": 0
            },
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 0
            }
          },
          "priceAlteration": []
        }
      ]
    }
  ],
  "relatedParty": [
    {
      "role": "Customer",
      "id": "9e2fd2ee11b43110f877366201dea674",
      "name": "Startech svcs",
      "@type": "RelatedPartyRef",
      "@referredType": "Organization"
    },
    {
      "role": "CustomerContact",
      "id": "dca96eaa11f43110f877366201dea6c1",
      "name": "Alex Star",
      "@type": "RelatedPartyRef",
      "@referredType": "Individual"
    }
  ],
  "state": "Draft"
}
```

## Quote Management API – GET /sn\_tmf\_api/quote\_management\_api/quote/\{id\}

Retrieves a specified quote.

This API retrieves quote information from the following related tables:

-   Quote \[sn\_quote\_mgmt\_core\_quote\]
-   Sales Agreement \[sn\_sales\_agmt\_core\_sales\_agreement\]
-   Quote Line Item \[sn\_quote\_mgmt\_core\_quote\_line\_item\]
-   Quote Line Characteristic \[sn\_quote\_mgmt\_core\_quote\_line\_characteristic\]
-   Quote Pricing Adjustment \[sn\_quote\_mgmt\_core\_pricing\_adjustment\]

### URL format

Versioned URL: `/api/sn_tmf_api/{api_version}/quote_management_api/quote/{id}`

Default URL: `/api/sn_tmf_api/quote_management_api/quote/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the quote to retrieve.Data type: String

Table: Quote \[sn\_quote\_mgmt\_core\_quote\]

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
|None| |

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_abf_sn5_4sb"><thead><tr><th>

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

<table id="table_jlb_1qx_kqb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contactMedium

</td><td>

List of contact mediums. Contact information related to the quote requester.```
"contactMedium": [
 {
  "city": "String",
  "country": "String",
  "locationId": "String",
  "mediumType": "String",
  "postCode": "String",
  "stateOrProvince": "String",
  "street": "String",
  "@type": "String"
 }
]
```

</td></tr><tr><td>

contactMedium.city

</td><td>

City in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location listed in the Location \[cmn\_location\] table or custom address.Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact medium, such as email address, telephone number, or postal address.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the quote requester.Data type: String

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

State or province in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.street

</td><td>

Street address of the quote requester.Data type: String

</td></tr><tr><td>

contactMedium.@type

</td><td>

Type of medium per the TMF Open API standard. For example, `GeographicalAddressContactMedium`.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the quote.Data type: String

</td></tr><tr><td>

expectedQuoteCompletionDate

</td><td>

The expected date from quote supplier to be able to send back a response for this quote.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Unique consumer-provided ID for the quote.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to access the quote.Data type: String

Default: Empty string

</td></tr><tr><td>

id

</td><td>

Sys\_id of the requested quote.Table: Quote \[sn\_quote\_mgmt\_core\_quote\]

Data type: String

</td></tr><tr><td>

note

</td><td>

List of notes associated with the quote. Data type: Array

```
"note": [
  {
    "author": "String",
    "date": "String",
    "text": "String",
    "@type": "String"
 }
]
```

</td></tr><tr><td>

note.author

</td><td>

User name of the person that authored the associated note.Data type: String

</td></tr><tr><td>

note.date

</td><td>

Date that the note was created.Data type: String

</td></tr><tr><td>

note.text

</td><td>

Contents of the note. Data type: String

</td></tr><tr><td>

note.@type

</td><td>

This value is always `Note`.Data type: String

</td></tr><tr><td>

quoteDate

</td><td>

Date and time at which the quote was created.Data type: String

</td></tr><tr><td>

quoteItem

</td><td>

A list of quote items. Each quote item describes an action for a product to be quoted.```
"quoteItem": [
 {
  "action": "String",
  "id": "String",
  "product": {Object},
  "productOffering": {Object},
  "quantity": Number,
  "state": "String",
  "@type": "String"
 }
]
```

Data type: Array of Objects

</td></tr><tr><td>

quoteItem.action

</td><td>

Action to be performed on this quote item \(add, modify, remove, etc.\).Data type: String

</td></tr><tr><td>

quoteItem.id

</td><td>

Sys\_id of the quote item.Table: Quote Line Item \[sn\_quote\_mgmt\_core\_quote\_line\_item\]

Data type: String

</td></tr><tr><td>

quoteItem.product

</td><td>

List of products included in the quote.```
"product": {
  "characteristic": "String",
  "specification": "String",
  "@type": "String"
}
```

Data type: Object

</td></tr><tr><td>

quoteItem.product. characteristic

</td><td>

List of product characteristics.Data type: Array of Objects

```
"characteristic": [
  {
    "id": "String",
    "name": "String",
    "@type": "String",
    "value": "String"
  }
]
```

See [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=zurich&pubname=zurich-order-management&ft:locale=en-US).

</td></tr><tr><td>

quoteItem.product. characteristic.id

</td><td>

Sys\_id of the product characteristic.Table: Quote Line Characteristic \[sn\_quote\_mgmt\_core\_quote\_line\_characteristic\]

Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.name

</td><td>

Name of the product characteristic.Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.@type

</td><td>

This value is always `StringCharacteristic`.Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

quoteItem.product. specification

</td><td>

Detailed description of a tangible or intangible object made available externally in the form of a ProductOffering to customers or other parties playing a party role.Data type: String

</td></tr><tr><td>

quoteItem.product.@type

</td><td>

This value is always `Product`.Data type: String

</td></tr><tr><td>

quoteItem.productOffering

</td><td>

A product offering reference \(ProductOfferingRef\). A product offering represents entities that are orderable from the provider of the catalog.```
"productOffering": {
  "href": "String",
  "name": "String",
  "name": "String",
  "@type": "String"
}
```

Data type: Object

</td></tr><tr><td>

quoteItem. productOffering.href

</td><td>

Reference of the related entity.Data type: String

</td></tr><tr><td>

quoteItem. productOffering.id

</td><td>

Sys\_id of product offering.Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

Data type: String

</td></tr><tr><td>

quoteItem. productOffering.name

</td><td>

Name of the related entity.Data type: String

</td></tr><tr><td>

quoteItem. productOffering.@type

</td><td>

This value is always `ProductOfferingRef`.Data type: String

</td></tr><tr><td>

quoteItem.quantity

</td><td>

Quantity asked for this quote item.Data type: Number

</td></tr><tr><td>

quoteItem.state

</td><td>

A quote state type \(QuoteStateType\). State of the quote.Data type: String

</td></tr><tr><td>

quoteItem.@type

</td><td>

This value is always `QuoteItem`.Data type: String

</td></tr><tr><td>

quoteNumber

</td><td>

Quote line item record number assigned to the quote.Table: Quote Line Item \[sn\_quote\_mgmt\_core\_quote\_line\_item\]

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order.Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String",
    "role": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the quote table to get the account, contact, or customer.Table: Quote \[sn\_quote\_mgmt\_core\_quote\]

 Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

The role of the party in the context of the quote \(e.g., Account, Contact, or Customer\).Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

This value is always `ProductOfferingRef`.Data type: String

</td></tr><tr><td>

requestedQuoteCompletionDate

</td><td>

A date time \(DateTime\). This value represents the date specified by the quote requester by which to receive a complete response for this quote.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the quote item.Data type: String

</td></tr><tr><td>

@type

</td><td>

Type of resource. This value is always `Quote`. This information isn’t stored.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example retrieves a specified quote.

```
curl "https://instance.service-now.com/api/sn_tmf_api/quote_management_api/quote/04ba9004f11f3110f8777d7194f166f6" \
--request GET \
--header "Accept:application/json" \
--user 'userName':'password'
```

Response body.

```
{
  "id": "47e562bad565a610f8774663edf0ac10",
  "quoteNumber": "QT0001001",
  "href": "api/sn_tmf_api/quote_management_api/quote/47e562bad565a610f8774663edf0ac10",
  "@type": "Quote",
  "description": "Testing Quote",
  "expectedQuoteCompletionDate": "2025-05-23 11:12:08",
  "externalId": "Test_1234",
  "quoteDate": "2025-05-20 11:11:13",
  "requestedQuoteCompletionDate": "2025-05-23 11:12:08",
  "version": "3",
  "agreement": [],
  "contactMedium": [
    {
      "@type": "GeographicalAddressContactMedium",
      "mediumType": "ShippingAddressRef",
      "locationId": "6774fee611383110f877366201dea64f",
      "city": "Santa Clara",
      "country": "USA",
      "postCode": "94560",
      "stateOrProvince": "CA",
      "street": "222 Star St"
    }
  ],
  "note": [],
  "quoteItem": [
    {
      "id": "8be562bad565a610f8774663edf0ac16",
      "@type": "QuoteItem",
      "action": "add",
      "quantity": "1",
      "state": "Draft",
      "product": {
        "@type": "Product",
        "productCharacteristic": [
          {
            "id": "0fe562bad565a610f8774663edf0ac17",
            "name": "Voice Pack",
            "value": "1500 Minutes/Month"
          },
          {
            "id": "4be562bad565a610f8774663edf0ac17",
            "name": "SMS Pack",
            "value": "700 /Month"
          },
          {
            "id": "83e562bad565a610f8774663edf0ac18",
            "name": "Data Pack",
            "value": "20 GB/Month"
          },
          {
            "id": "87e562bad565a610f8774663edf0ac17",
            "name": "Mobile Number",
            "value": ""
          },
          {
            "id": "cfe562bad565a610f8774663edf0ac17",
            "name": "Shipping Address",
            "value": ""
          }
        ],
        "productSpecification": {
          "id": "3ee1fdb1c3331010d216b5183c40dd81",
          "href": "api/sn_tmf_api/catalogmanagement/productSpecification/3ee1fdb1c3331010d216b5183c40dd81",
          "name": "Mobile Plan",
          "@type": "ProductSpecificationRef"
        }
      },
      "productOffering": {
        "id": "2cb5588fc30020105252716b7d40dddd",
        "href": "api/sn_tmf_api/catalogmanagement/productOffering/2cb5588fc30020105252716b7d40dddd",
        "name": "All in one mobile plan starting from $49/month",
        "@type": "ProductOfferingRef"
      },
      "quoteItemPrice": [
        {
          "description": "Standard Price List",
          "name": "Standard Price List",
          "priceType": "Recurring",
          "recurringChargePeriod": "",
          "unitOfMeasure": "",
          "unitMarginPercentage": "",
          "price": {
            "totalOneTimePrice": {
              "unit": "USD",
              "value": 0
            },
            "monthlyRecurringPrice": {
              "unit": "USD",
              "value": 0
            },
            "annualRecurringPrice": {
              "unit": "USD",
              "value": 0
            },
            "cumulativeRecurringPrice": {
              "unit": "USD",
              "value": 0
            },
            "cumulativeAnnualRecurringPrice": {
              "unit": "USD",
              "value": 0
            },
            "cumulativeNetPrice": {
              "unit": "USD",
              "value": 0
            },
            "unitMarginAmount": {
              "unit": "USD",
              "value": 0
            },
            "unitMarginBasePrice": {
              "unit": "USD",
              "value": 0
            },
            "listPrice": {
              "unit": "USD",
              "value": 0
            },
            "unitCost": {
              "unit": "USD",
              "value": 0
            },
            "unitPrice": {
              "unit": "USD",
              "value": 0
            },
            "dutyFreeAmount": {
              "unit": "USD",
              "value": 0
            },
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 0
            }
          },
          "priceAlteration": []
        }
      ]
    }
  ],
  "relatedParty": [
    {
      "role": "Customer",
      "id": "9e2fd2ee11b43110f877366201dea674",
      "name": "Startech svcs",
      "@type": "RelatedPartyRef",
      "@referredType": "Organization"
    },
    {
      "role": "CustomerContact",
      "id": "dca96eaa11f43110f877366201dea6c1",
      "name": "Alex Star",
      "@type": "RelatedPartyRef",
      "@referredType": "Individual"
    }
  ],
  "state": "Draft"
}
```

## Quote Management API - PATCH /sn\_tmf\_api/quote\_management\_api/quote/\{id\}

Updates the specified quote.

### URL format

Versioned URL: `/api/sn_tmf_api/{api_version}/quote_management_api/quote/{id}`

Default URL: `/api/sn_tmf_api/quote_management_api/quote/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the quote to update.Data type: String

Table: Quote \[sn\_quote\_mgmt\_core\_quote\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="table_m32_1l1_hwb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contactMedium

</td><td>

List of contact mediums. Contact information related to the quote requester.```
"contactMedium": [
 {
  "city": "String",
  "country": "String",
  "locationId": "String",
  "mediumType": "String",
  "postCode": "String",
  "stateOrProvince": "String",
  "street": "String",
  "@type": "String"
 }
]
```

</td></tr><tr><td>

contactMedium.city

</td><td>

City in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location listed in the Location \[cmn\_location\] table or custom address.Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact medium, such as email address, telephone number, or postal address.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the quote requester.Data type: String

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

State or province in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.street

</td><td>

Street address of the quote requester.Data type: String

</td></tr><tr><td>

contactMedium.@type

</td><td>

Type of medium per the TMF Open API standard. For example, `GeographicalAddressContactMedium`.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the quote.Data type: String

</td></tr><tr><td>

note

</td><td>

List of notes associated with the quote. Data type: Array

```
"note": [
  {
    "text": "String",
    "@type": "String"
 }
]
```

</td></tr><tr><td>

note.text

</td><td>

Contents of the note. Data type: String

</td></tr><tr><td>

note.@type

</td><td>

This value is always `Note`.Data type: String

</td></tr><tr><td>

quoteDate

</td><td>

Date and time at which the quote was created.Data type: String

</td></tr><tr><td>

quoteItem

</td><td>

A list of quote items. Each quote item describes an action for a product to be quoted.```
"quoteItem": [
 {
  "action": "String",
  "id": "String",
  "product": {Object},
  "productOffering": {Object},
  "productRelationship": {Object},
  "quantity": Number,
  "state": "String",
  "@type": "String"
 }
]
```

Data type: Array of Objects

</td></tr><tr><td>

quoteItem.action

</td><td>

Action to be performed on this quote item \(add, modify, remove, etc.\).Data type: String

</td></tr><tr><td>

quoteItem.id

</td><td>

Sys\_id of the quote item.Table: Quote Line Item \[sn\_quote\_mgmt\_core\_quote\_line\_item\]

Data type: String

</td></tr><tr><td>

quoteItem.product

</td><td>

List of products included in the quote.```
"product": {
  "characteristic": "String",
  "specification": "String",
  "@type": "String"
}
```

Data type: Object

</td></tr><tr><td>

quoteItem.product. characteristic

</td><td>

List of product characteristics.Data type: Array of Objects

```
"characteristic": [
  {
    "id": "String",
    "name": "String",
    "@type": "String",
    "value": "String"
  }
]
```

See [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=zurich&pubname=zurich-order-management&ft:locale=en-US).

</td></tr><tr><td>

quoteItem.product. characteristic.id

</td><td>

Sys\_id of the product characteristic.Table: Quote Line Characteristic \[sn\_quote\_mgmt\_core\_quote\_line\_characteristic\]

Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.name

</td><td>

Name of the product characteristic.Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.@type

</td><td>

This value is always `StringCharacteristic`.Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

quoteItem.product. specification

</td><td>

Detailed description of a tangible or intangible object made available externally in the form of a ProductOffering to customers or other parties playing a party role.Data type: String

</td></tr><tr><td>

quoteItem.product.@type

</td><td>

This value is always `Product`.Data type: String

</td></tr><tr><td>

quoteItem.productOffering

</td><td>

A product offering reference \(ProductOfferingRef\). A product offering represents entities that are orderable from the provider of the catalog.```
"productOffering": {
  "href": "String",
  "name": "String",
  "name": "String",
  "@type": "String"
}
```

Data type: Object

</td></tr><tr><td>

quoteItem. productOffering.href

</td><td>

Reference of the related entity.Data type: String

</td></tr><tr><td>

quoteItem. productOffering.id

</td><td>

Sys\_id of product offering.Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

Data type: String

</td></tr><tr><td>

quoteItem. productOffering.name

</td><td>

Name of the related entity.Data type: String

</td></tr><tr><td>

quoteItem. productOffering.@type

</td><td>

This value is always `ProductOfferingRef`.Data type: String

</td></tr><tr><td>

quoteItem.productRelationship

</td><td>

A list of quote items. Each quote item describes an action for a product to be quoted.```
"productRelationship": [
 {
  "product": "String",
  "relationshipType": "String"
 }
]
```

Data type: Array of Objects

</td></tr><tr><td>

quoteItem.productRelationship. product

</td><td>

A product reference or value \(ProductRefOrValue\). A produt to be created defined by value or existing defined by reference.The product meets one of the following criteria:

-   Pending product creation defined by the value.
-   Existing product defined by reference.

Data type: String

</td></tr><tr><td>

quoteItem.productRelationship. relationshipType

</td><td>

Type of the product relationship, such as `bundled` if the product is a bundle and you want to describe the the bundled products within.Data type: String

</td></tr><tr><td>

quoteItem.quantity

</td><td>

Quantity asked for this quote item.Data type: Number

</td></tr><tr><td>

quoteItem.state

</td><td>

A quote state type \(QuoteStateType\). State of the quote.Data type: String

</td></tr><tr><td>

quoteItem.@type

</td><td>

This value is always `QuoteItem`.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order.Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String",
    "role": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the quote table to get the account, contact, or customer.Table: Quote \[sn\_quote\_mgmt\_core\_quote\]

 Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

The role of the party in the context of the quote \(e.g., Account, Contact, or Customer\).Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

This value is always `ProductOfferingRef`.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the quote item.Data type: String

</td></tr><tr><td>

@type

</td><td>

Type of resource. This value is always `Quote`. This information isn’t stored.Data type: String

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

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_xfv_2vk_5rb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Request successfully processed. Full resource returned in response \(no pagination\).

</td></tr><tr><td>

400

</td><td>

Bad request. Possible reasons:

-   Invalid path parameter
-   Invalid URI

</td></tr><tr><td>

404

</td><td>

Record not found. No records matching the query parameters are found in the table.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_t5s_hm1_hwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contactMedium

</td><td>

List of contact mediums. Contact information related to the quote requester.```
"contactMedium": [
 {
  "city": "String",
  "country": "String",
  "locationId": "String",
  "mediumType": "String",
  "postCode": "String",
  "stateOrProvince": "String",
  "street": "String",
  "@type": "String"
 }
]
```

</td></tr><tr><td>

contactMedium.city

</td><td>

City in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location listed in the Location \[cmn\_location\] table or custom address.Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact medium, such as email address, telephone number, or postal address.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the quote requester.Data type: String

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

State or province in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.street

</td><td>

Street address of the quote requester.Data type: String

</td></tr><tr><td>

contactMedium.@type

</td><td>

Type of medium per the TMF Open API standard. For example, `GeographicalAddressContactMedium`.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the quote.Data type: String

</td></tr><tr><td>

note

</td><td>

List of notes associated with the quote. Data type: Array

```
"note": [
  {
    "text": "String",
    "@type": "String"
 }
]
```

</td></tr><tr><td>

note.text

</td><td>

Contents of the note. Data type: String

</td></tr><tr><td>

note.@type

</td><td>

This value is always `Note`.Data type: String

</td></tr><tr><td>

quoteDate

</td><td>

Date and time at which the quote was created.Data type: String

</td></tr><tr><td>

quoteItem

</td><td>

A list of quote items. Each quote item describes an action for a product to be quoted.```
"quoteItem": [
 {
  "action": "String",
  "id": "String",
  "product": {Object},
  "productOffering": {Object},
  "productRelationship": {Object},
  "quantity": Number,
  "state": "String",
  "@type": "String"
 }
]
```

Data type: Array of Objects

</td></tr><tr><td>

quoteItem.action

</td><td>

Action to be performed on this quote item \(add, modify, remove, etc.\).Data type: String

</td></tr><tr><td>

quoteItem.id

</td><td>

Sys\_id of the quote item.Table: Quote Line Item \[sn\_quote\_mgmt\_core\_quote\_line\_item\]

Data type: String

</td></tr><tr><td>

quoteItem.product

</td><td>

List of products included in the quote.```
"product": {
  "characteristic": "String",
  "specification": "String",
  "@type": "String"
}
```

Data type: Object

</td></tr><tr><td>

quoteItem.product. characteristic

</td><td>

List of product characteristics.Data type: Array of Objects

```
"characteristic": [
  {
    "id": "String",
    "name": "String",
    "@type": "String",
    "value": "String"
  }
]
```

See [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=zurich&pubname=zurich-order-management&ft:locale=en-US).

</td></tr><tr><td>

quoteItem.product. characteristic.id

</td><td>

Sys\_id of the product characteristic.Table: Quote Line Characteristic \[sn\_quote\_mgmt\_core\_quote\_line\_characteristic\]

Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.name

</td><td>

Name of the product characteristic.Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.@type

</td><td>

This value is always `StringCharacteristic`.Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

quoteItem.product. specification

</td><td>

Detailed description of a tangible or intangible object made available externally in the form of a ProductOffering to customers or other parties playing a party role.Data type: String

</td></tr><tr><td>

quoteItem.product.@type

</td><td>

This value is always `Product`.Data type: String

</td></tr><tr><td>

quoteItem.productOffering

</td><td>

A product offering reference \(ProductOfferingRef\). A product offering represents entities that are orderable from the provider of the catalog.```
"productOffering": {
  "href": "String",
  "name": "String",
  "name": "String",
  "@type": "String"
}
```

Data type: Object

</td></tr><tr><td>

quoteItem. productOffering.href

</td><td>

Reference of the related entity.Data type: String

</td></tr><tr><td>

quoteItem. productOffering.id

</td><td>

Sys\_id of product offering.Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

Data type: String

</td></tr><tr><td>

quoteItem. productOffering.name

</td><td>

Name of the related entity.Data type: String

</td></tr><tr><td>

quoteItem. productOffering.@type

</td><td>

This value is always `ProductOfferingRef`.Data type: String

</td></tr><tr><td>

quoteItem.productRelationship

</td><td>

A list of quote items. Each quote item describes an action for a product to be quoted.```
"productRelationship": [
 {
  "product": "String",
  "relationshipType": "String"
 }
]
```

Data type: Array of Objects

</td></tr><tr><td>

quoteItem.productRelationship. product

</td><td>

A product reference or value \(ProductRefOrValue\). A produt to be created defined by value or existing defined by reference.The product meets one of the following criteria:

-   Pending product creation defined by the value.
-   Existing product defined by reference.

Data type: String

</td></tr><tr><td>

quoteItem.productRelationship. relationshipType

</td><td>

Type of the product relationship, such as `bundled` if the product is a bundle and you want to describe the the bundled products within.Data type: String

</td></tr><tr><td>

quoteItem.quantity

</td><td>

Quantity asked for this quote item.Data type: Number

</td></tr><tr><td>

quoteItem.state

</td><td>

A quote state type \(QuoteStateType\). State of the quote.Data type: String

</td></tr><tr><td>

quoteItem.@type

</td><td>

This value is always `QuoteItem`.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order.Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String",
    "role": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the quote table to get the account, contact, or customer.Table: Quote \[sn\_quote\_mgmt\_core\_quote\]

 Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

The role of the party in the context of the quote \(e.g., Account, Contact, or Customer\).Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

This value is always `ProductOfferingRef`.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the quote item.Data type: String

</td></tr><tr><td>

@type

</td><td>

Type of resource. This value is always `Quote`. This information isn’t stored.Data type: String

</td></tr></tbody>
</table>### cURL request

This example shows how to update a quote.

```
curl "https://k8s0747687-node1.thunder.devsnc.com/api/sn_tmf_api/quote_management_api/quote/cb15734fd5692a10f8774663edf0ac19" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"@type\": \"Quote\",
  \"description\": \"Quote for Internet and OTT Bundle\",
  \"contactMedium\": [
    {
      \"@type\": \"GeographicalAddressContactMedium\",
      \"mediumType\": \"ShippingAddressRef\",
      \"locationId\": \"25ab96060a0a0bb300a6d66ce72095f2\",
      \"city\": \"Santa Clara\",
      \"country\": \"USA\",
      \"postCode\": \"95050\",
      \"stateOrProvince\": \"CA\",
      \"street\": \"2866 Stevens Creek Blvd\"
    }
  ],
  \"note\": [
    {
      \"@type\": \"Note\",
      \"text\": \"This is a quote request following today call\"
    }
  ],
  \"quoteItem\": [
    {
      \"id\": \"086be79bd5e1aa10f8774663edf0acba\",
      \"@type\": \"QuoteItem\",
      \"action\": \"add\",
      \"quantity\": \"1\",
      \"state\": \"Draft\",
      \"product\": {
        \"@type\": \"Product\"
      },
      \"productOffering\": {
        \"id\": \"ffeb447211bc3110f877366201dea6df\",
        \"name\": \"Internet and OTT Bundle\",
        \"@type\": \"ProductOfferingRef\"
      },
      \"productRelationship\": [
        {
          \"product\": \"597bab9bd5e1aa10f8774663edf0ac1b\",
          \"relationshipType\": \"HasChild\"
        },
        {
          \"product\": \"d57bab9bd5e1aa10f8774663edf0ac1a\",
          \"relationshipType\": \"HasChild\"
        },
        {
          \"product\": \"d57bab9bd5e1aa10f8774663edf0ac1c\",
          \"relationshipType\": \"HasChild\"
        }
      ]
    },
    {
      \"id\": \"d57bab9bd5e1aa10f8774663edf0ac1a\",
      \"@type\": \"QuoteItem\",
      \"action\": \"add\",
      \"quantity\": \"1\",
      \"state\": \"Draft\",
      \"product\": {
        \"@type\": \"Product\"
      },
      \"productOffering\": {
        \"id\": \"0761dd9fd0a63110f8770dbf976be173\",
        \"name\": \"Solana Modem N Series\",
        \"@type\": \"ProductOfferingRef\"
      },
      \"productRelationship\": [
        {
          \"product\": \"086be79bd5e1aa10f8774663edf0acba\",
          \"relationshipType\": \"HasParent\"
        }
      ]
    },
    {
      \"id\": \"597bab9bd5e1aa10f8774663edf0ac1b\",
      \"@type\": \"QuoteItem\",
      \"action\": \"add\",
      \"quantity\": \"1\",
      \"state\": \"Draft\",
      \"product\": {
        \"@type\": \"Product\"
      },
      \"productOffering\": {
        \"id\": \"8b61dd9fd0a63110f8770dbf976be140\",
        \"name\": \"Basic internet - 100 Mbps Plan\",
        \"@type\": \"ProductOfferingRef\"
      },
      \"productRelationship\": [
        {
          \"product\": \"086be79bd5e1aa10f8774663edf0acba\",
          \"relationshipType\": \"HasParent\"
        }
      ]
    },
    {
      \"id\": \"d57bab9bd5e1aa10f8774663edf0ac1c\",
      \"@type\": \"QuoteItem\",
      \"action\": \"add\",
      \"quantity\": \"1\",
      \"state\": \"Draft\",
      \"product\": {
        \"@type\": \"Product\"
      },
      \"productOffering\": {
        \"id\": \"62619d9fd0a63110f8770dbf976be180\",
        \"name\": \"Solana Movie streaming channel\",
        \"@type\": \"ProductOfferingRef\"
      },
      \"productRelationship\": [
        {
          \"product\": \"086be79bd5e1aa10f8774663edf0acba\",
          \"relationshipType\": \"HasParent\"
        }
      ]
    },
    {
      \"id\": \"797ca71fd5e1aa10f8774663edf0ac2b\",
      \"@type\": \"QuoteItem\",
      \"action\": \"add\",
      \"quantity\": \"1\",
      \"state\": \"Draft\",
      \"product\": {
        \"@type\": \"Product\",
        \"productCharacteristic\": [
          {
            \"name\": \"Internet breakout\",
            \"value\": \"No\"
          },
          {
            \"name\": \"Quality of Service\",
            \"value\": \"Basic\"
          },
          {
            \"name\": \"Speed\",
            \"value\": \"High\"
          }
        ],
        \"productSpecification\": {
          \"id\": \"cd81594e74ae4a10f877468e695efa81\",
          \"name\": \"VPN Site PS\",
          \"@type\": \"ProductSpecificationRef\"
        }
      },
      \"productOffering\": {
        \"id\": \"6c3d1e86a5e20210f8774c9b4be6ce42\",
        \"name\": \"VPN Site\",
        \"@type\": \"ProductOfferingRef\"
      },
      \"productRelationship\": [
        {
          \"product\": \"7f8c6b1fd5e1aa10f8774663edf0ac71\",
          \"relationshipType\": \"HasChild\"
        },
        {
          \"product\": \"bb8c6b1fd5e1aa10f8774663edf0ac73\",
          \"relationshipType\": \"HasChild\"
        },
        {
          \"product\": \"bf8c6b1fd5e1aa10f8774663edf0ac70\",
          \"relationshipType\": \"HasChild\"
        },
        {
          \"product\": \"fb8c6b1fd5e1aa10f8774663edf0ac72\",
          \"relationshipType\": \"HasChild\"
        }
      ]
    },
    {
      \"id\": \"bf8c6b1fd5e1aa10f8774663edf0ac70\",
      \"@type\": \"QuoteItem\",
      \"action\": \"add\",
      \"quantity\": \"1\",
      \"state\": \"Draft\",
      \"product\": {
        \"@type\": \"Product\"
      },
      \"productOffering\": {
        \"id\": \"2c265d4274ee4a10f877468e695efa45\",
        \"name\": \"Maintenance Fee\",
        \"@type\": \"ProductOfferingRef\"
      },
      \"productRelationship\": [
        {
          \"product\": \"797ca71fd5e1aa10f8774663edf0ac2b\",
          \"relationshipType\": \"HasParent\"
        }
      ]
    },
    {
      \"id\": \"7f8c6b1fd5e1aa10f8774663edf0ac71\",
      \"@type\": \"QuoteItem\",
      \"action\": \"add\",
      \"quantity\": \"1\",
      \"state\": \"Draft\",
      \"product\": {
        \"@type\": \"Product\"
      },
      \"productOffering\": {
        \"id\": \"4466d50674ee4a10f877468e695efa0d\",
        \"name\": \"Security Fee\",
        \"@type\": \"ProductOfferingRef\"
      },
      \"productRelationship\": [
        {
          \"product\": \"797ca71fd5e1aa10f8774663edf0ac2b\",
          \"relationshipType\": \"HasParent\"
        }
      ]
    },
    {
      \"id\": \"fb8c6b1fd5e1aa10f8774663edf0ac72\",
      \"@type\": \"QuoteItem\",
      \"action\": \"add\",
      \"quantity\": \"1\",
      \"state\": \"Draft\",
      \"product\": {
        \"@type\": \"Product\",
        \"productCharacteristic\": [
          {
            \"name\": \"Speed\",
            \"value\": \"High\"
          },
          {
            \"name\": \"Internet breakout\",
            \"value\": \"No\"
          }
        ],
        \"productSpecification\": {
          \"id\": \"ee4f8d8a74ae4a10f877468e695efa3f\",
          \"name\": \"VPN Endpoint PS\",
          \"@type\": \"ProductSpecificationRef\"
        }
      },
      \"productOffering\": {
        \"id\": \"7acc9e46a5e20210f8774c9b4be6ce9e\",
        \"name\": \"VPN Endpoint\",
        \"@type\": \"ProductOfferingRef\"
      },
      \"productRelationship\": [
        {
          \"product\": \"797ca71fd5e1aa10f8774663edf0ac2b\",
          \"relationshipType\": \"HasParent\"
        }
      ]
    },
    {
      \"id\": \"bb8c6b1fd5e1aa10f8774663edf0ac73\",
      \"@type\": \"QuoteItem\",
      \"action\": \"add\",
      \"quantity\": \"1\",
      \"state\": \"Draft\",
      \"product\": {
        \"@type\": \"Product\",
        \"productCharacteristic\": [
          {
            \"name\": \"Quality of Service\",
            \"value\": \"Basic\"
          }
        ],
        \"productSpecification\": {
          \"id\": \"3ba0914e74ae4a10f877468e695efa6e\",
          \"name\": \"VPN Firewall PS\",
          \"@type\": \"ProductSpecificationRef\"
        }
      },
      \"productOffering\": {
        \"id\": \"4407d90674ee4a10f877468e695efaab\",
        \"name\": \"VPN Firewall\",
        \"@type\": \"ProductOfferingRef\"
      },
      \"productRelationship\": [
        {
          \"product\": \"797ca71fd5e1aa10f8774663edf0ac2b\",
          \"relationshipType\": \"HasParent\"
        }
      ]
    }
  ],
  \"relatedParty\": [
    {
      \"role\": \"Customer\",
      \"id\": \"9e2fd2ee11b43110f877366201dea674\",
      \"name\": \"Startech svcs\",
      \"@type\": \"RelatedPartyRef\",
      \"@referredType\": \"Organization\"
    }
  ],
  \"state\": \"Draft\"
}" \
--user 'userName':'password'
```

Response body.

```
{
  "@type": "Quote",
  "description": "Quote for Internet and OTT Bundle",
  "contactMedium": [
    {
      "@type": "GeographicalAddressContactMedium",
      "mediumType": "ShippingAddressRef",
      "locationId": "25ab96060a0a0bb300a6d66ce72095f2",
      "city": "Santa Clara",
      "country": "USA",
      "postCode": "95050",
      "stateOrProvince": "CA",
      "street": "2866 Stevens Creek Blvd"
    }
  ],
  "note": [
    {
      "@type": "Note",
      "text": "This is a quote request following today call"
    }
  ],
  "quoteItem": [
    {
      "id": "086be79bd5e1aa10f8774663edf0acba",
      "@type": "QuoteItem",
      "action": "add",
      "quantity": "1",
      "state": "Draft",
      "product": {
        "@type": "Product"
      },
      "productOffering": {
        "id": "ffeb447211bc3110f877366201dea6df",
        "name": "Internet and OTT Bundle",
        "@type": "ProductOfferingRef"
      },
      "productRelationship": [
        {
          "product": "597bab9bd5e1aa10f8774663edf0ac1b",
          "relationshipType": "HasChild"
        },
        {
          "product": "d57bab9bd5e1aa10f8774663edf0ac1a",
          "relationshipType": "HasChild"
        },
        {
          "product": "d57bab9bd5e1aa10f8774663edf0ac1c",
          "relationshipType": "HasChild"
        }
      ]
    },
    {
      "id": "d57bab9bd5e1aa10f8774663edf0ac1a",
      "@type": "QuoteItem",
      "action": "add",
      "quantity": "1",
      "state": "Draft",
      "product": {
        "@type": "Product"
      },
      "productOffering": {
        "id": "0761dd9fd0a63110f8770dbf976be173",
        "name": "Solana Modem N Series",
        "@type": "ProductOfferingRef"
      },
      "productRelationship": [
        {
          "product": "086be79bd5e1aa10f8774663edf0acba",
          "relationshipType": "HasParent"
        }
      ]
    },
    {
      "id": "597bab9bd5e1aa10f8774663edf0ac1b",
      "@type": "QuoteItem",
      "action": "add",
      "quantity": "1",
      "state": "Draft",
      "product": {
        "@type": "Product"
      },
      "productOffering": {
        "id": "8b61dd9fd0a63110f8770dbf976be140",
        "name": "Basic internet - 100 Mbps Plan",
        "@type": "ProductOfferingRef"
      },
      "productRelationship": [
        {
          "product": "086be79bd5e1aa10f8774663edf0acba",
          "relationshipType": "HasParent"
        }
      ]
    },
    {
      "id": "d57bab9bd5e1aa10f8774663edf0ac1c",
      "@type": "QuoteItem",
      "action": "add",
      "quantity": "1",
      "state": "Draft",
      "product": {
        "@type": "Product"
      },
      "productOffering": {
        "id": "62619d9fd0a63110f8770dbf976be180",
        "name": "Solana Movie streaming channel",
        "@type": "ProductOfferingRef"
      },
      "productRelationship": [
        {
          "product": "086be79bd5e1aa10f8774663edf0acba",
          "relationshipType": "HasParent"
        }
      ]
    },
    {
      "id": "797ca71fd5e1aa10f8774663edf0ac2b",
      "@type": "QuoteItem",
      "action": "add",
      "quantity": "1",
      "state": "Draft",
      "product": {
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "Internet breakout",
            "value": "No"
          },
          {
            "name": "Quality of Service",
            "value": "Basic"
          },
          {
            "name": "Speed",
            "value": "High"
          }
        ],
        "productSpecification": {
          "id": "cd81594e74ae4a10f877468e695efa81",
          "name": "VPN Site PS",
          "@type": "ProductSpecificationRef"
        }
      },
      "productOffering": {
        "id": "6c3d1e86a5e20210f8774c9b4be6ce42",
        "name": "VPN Site",
        "@type": "ProductOfferingRef"
      },
      "productRelationship": [
        {
          "product": "7f8c6b1fd5e1aa10f8774663edf0ac71",
          "relationshipType": "HasChild"
        },
        {
          "product": "bb8c6b1fd5e1aa10f8774663edf0ac73",
          "relationshipType": "HasChild"
        },
        {
          "product": "bf8c6b1fd5e1aa10f8774663edf0ac70",
          "relationshipType": "HasChild"
        },
        {
          "product": "fb8c6b1fd5e1aa10f8774663edf0ac72",
          "relationshipType": "HasChild"
        }
      ]
    },
    {
      "id": "bf8c6b1fd5e1aa10f8774663edf0ac70",
      "@type": "QuoteItem",
      "action": "add",
      "quantity": "1",
      "state": "Draft",
      "product": {
        "@type": "Product"
      },
      "productOffering": {
        "id": "2c265d4274ee4a10f877468e695efa45",
        "name": "Maintenance Fee",
        "@type": "ProductOfferingRef"
      },
      "productRelationship": [
        {
          "product": "797ca71fd5e1aa10f8774663edf0ac2b",
          "relationshipType": "HasParent"
        }
      ]
    },
    {
      "id": "7f8c6b1fd5e1aa10f8774663edf0ac71",
      "@type": "QuoteItem",
      "action": "add",
      "quantity": "1",
      "state": "Draft",
      "product": {
        "@type": "Product"
      },
      "productOffering": {
        "id": "4466d50674ee4a10f877468e695efa0d",
        "name": "Security Fee",
        "@type": "ProductOfferingRef"
      },
      "productRelationship": [
        {
          "product": "797ca71fd5e1aa10f8774663edf0ac2b",
          "relationshipType": "HasParent"
        }
      ]
    },
    {
      "id": "fb8c6b1fd5e1aa10f8774663edf0ac72",
      "@type": "QuoteItem",
      "action": "add",
      "quantity": "1",
      "state": "Draft",
      "product": {
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "Speed",
            "value": "High"
          },
          {
            "name": "Internet breakout",
            "value": "No"
          }
        ],
        "productSpecification": {
          "id": "ee4f8d8a74ae4a10f877468e695efa3f",
          "name": "VPN Endpoint PS",
          "@type": "ProductSpecificationRef"
        }
      },
      "productOffering": {
        "id": "7acc9e46a5e20210f8774c9b4be6ce9e",
        "name": "VPN Endpoint",
        "@type": "ProductOfferingRef"
      },
      "productRelationship": [
        {
          "product": "797ca71fd5e1aa10f8774663edf0ac2b",
          "relationshipType": "HasParent"
        }
      ]
    },
    {
      "id": "bb8c6b1fd5e1aa10f8774663edf0ac73",
      "@type": "QuoteItem",
      "action": "add",
      "quantity": "1",
      "state": "Draft",
      "product": {
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "Quality of Service",
            "value": "Basic"
          }
        ],
        "productSpecification": {
          "id": "3ba0914e74ae4a10f877468e695efa6e",
          "name": "VPN Firewall PS",
          "@type": "ProductSpecificationRef"
        }
      },
      "productOffering": {
        "id": "4407d90674ee4a10f877468e695efaab",
        "name": "VPN Firewall",
        "@type": "ProductOfferingRef"
      },
      "productRelationship": [
        {
          "product": "797ca71fd5e1aa10f8774663edf0ac2b",
          "relationshipType": "HasParent"
        }
      ]
    }
  ],
  "relatedParty": [
    {
      "role": "Customer",
      "id": "9e2fd2ee11b43110f877366201dea674",
      "name": "Startech svcs",
      "@type": "RelatedPartyRef",
      "@referredType": "Organization"
    }
  ],
  "state": "Draft",
  "id": "cb15734fd5692a10f8774663edf0ac19",
  "version": "2",
  "quoteDate": "2025-05-21 04:56:50",
  "href": "api/sn_tmf_api/quote_management_api/quote/cb15734fd5692a10f8774663edf0ac19"
}
```

## Quote Management API – POST /sn\_tmf\_api/quote\_management\_api/quote

Creates a quote.

New quote records are created in the following tables:

-   Quote \[sn\_quote\_mgmt\_core\_quote\]
-   Sales Agreement \[sn\_sales\_agmt\_core\_sales\_agreement\]
-   Quote Line Item \[sn\_quote\_mgmt\_core\_quote\_line\_item\]
-   Quote Line Characteristic \[sn\_quote\_mgmt\_core\_quote\_line\_characteristic\]
-   Quote Pricing Adjustment \[sn\_quote\_mgmt\_core\_pricing\_adjustment\]

### URL format

Versioned URL: `/api/sn_tmf_api/{api_version}/quote_management_api/quote`

Default URL: `/api/sn_tmf_api/quote_management_api/quote`

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

contactMedium

</td><td>

List of contact mediums. Contact information related to the quote requester.```
"contactMedium": [
 {
  "city": "String",
  "country": "String",
  "locationId": "String",
  "mediumType": "String",
  "postCode": "String",
  "stateOrProvince": "String",
  "street": "String",
  "@type": "String"
 }
]
```

</td></tr><tr><td>

contactMedium.city

</td><td>

City in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location listed in the Location \[cmn\_location\] table or custom address.Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact medium, such as email address, telephone number, or postal address.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the quote requester.Data type: String

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

State or province in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.street

</td><td>

Street address of the quote requester.Data type: String

</td></tr><tr><td>

contactMedium.@type

</td><td>

Type of medium per the TMF Open API standard. For example, `GeographicalAddressContactMedium`.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the quote.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Unique consumer-provided ID for the quote.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to access the quote.Data type: String

Default: Empty string

</td></tr><tr><td>

note

</td><td>

List of notes associated with the quote. Data type: Array

```
"note": [
  {
    "text": "String",
    "@type": "String"
 }
]
```

</td></tr><tr><td>

note.text

</td><td>

Contents of the note. Data type: String

</td></tr><tr><td>

note.@type

</td><td>

This value is always `Note`.Data type: String

</td></tr><tr><td>

quoteDate

</td><td>

Date and time at which the quote was created.Data type: String

</td></tr><tr><td>

quoteItem

</td><td>

A list of quote items. Each quote item describes an action for a product to be quoted.```
"quoteItem": [
 {
  "action": "String",
  "id": "String",
  "product": {Object},
  "productOffering": {Object},
  "productRelationship": {Object},
  "quantity": Number,
  "state": "String",
  "@type": "String"
 }
]
```

Data type: Array of Objects

</td></tr><tr><td>

quoteItem.action

</td><td>

Action to be performed on this quote item \(add, modify, remove, etc.\).Data type: String

</td></tr><tr><td>

quoteItem.id

</td><td>

Sys\_id of the quote item.Table: Quote Line Item \[sn\_quote\_mgmt\_core\_quote\_line\_item\]

Data type: String

</td></tr><tr><td>

quoteItem.product

</td><td>

List of products included in the quote.```
"product": {
  "characteristic": "String",
  "specification": "String",
  "@type": "String"
}
```

Data type: Object

</td></tr><tr><td>

quoteItem.product. characteristic

</td><td>

List of product characteristics.Data type: Array of Objects

```
"characteristic": [
  {
    "id": "String",
    "name": "String",
    "@type": "String",
    "value": "String"
  }
]
```

See [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=zurich&pubname=zurich-order-management&ft:locale=en-US).

</td></tr><tr><td>

quoteItem.product. characteristic.id

</td><td>

Sys\_id of the product characteristic.Table: Quote Line Characteristic \[sn\_quote\_mgmt\_core\_quote\_line\_characteristic\]

Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.name

</td><td>

Name of the product characteristic.Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.@type

</td><td>

This value is always `StringCharacteristic`.Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

quoteItem.product. specification

</td><td>

Detailed description of a tangible or intangible object made available externally in the form of a ProductOffering to customers or other parties playing a party role.Data type: String

</td></tr><tr><td>

quoteItem.product.@type

</td><td>

This value is always `Product`.Data type: String

</td></tr><tr><td>

quoteItem.productOffering

</td><td>

A product offering reference \(ProductOfferingRef\). A product offering represents entities that are orderable from the provider of the catalog.```
"productOffering": {
  "href": "String",
  "name": "String",
  "name": "String",
  "@type": "String"
}
```

Data type: Object

</td></tr><tr><td>

quoteItem. productOffering.href

</td><td>

Reference of the related entity.Data type: String

</td></tr><tr><td>

quoteItem. productOffering.id

</td><td>

Sys\_id of product offering.Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

Data type: String

</td></tr><tr><td>

quoteItem. productOffering.name

</td><td>

Name of the related entity.Data type: String

</td></tr><tr><td>

quoteItem. productOffering.@type

</td><td>

This value is always `ProductOfferingRef`.Data type: String

</td></tr><tr><td>

quoteItem.productRelationship

</td><td>

A list of quote items. Each quote item describes an action for a product to be quoted.```
"productRelationship": [
 {
  "product": "String",
  "relationshipType": "String"
 }
]
```

Data type: Array of Objects

</td></tr><tr><td>

quoteItem.productRelationship. product

</td><td>

A product reference or value \(ProductRefOrValue\). A produt to be created defined by value or existing defined by reference.The product meets one of the following criteria:

-   Pending product creation defined by the value.
-   Existing product defined by reference.

Data type: String

</td></tr><tr><td>

quoteItem.productRelationship. relationshipType

</td><td>

Type of the product relationship, such as `bundled` if the product is a bundle and you want to describe the the bundled products within.Data type: String

</td></tr><tr><td>

quoteItem.quantity

</td><td>

Quantity asked for this quote item.Data type: Number

</td></tr><tr><td>

quoteItem.state

</td><td>

A quote state type \(QuoteStateType\). State of the quote.Data type: String

</td></tr><tr><td>

quoteItem.@type

</td><td>

This value is always `QuoteItem`.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order.Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String",
    "role": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the quote table to get the account, contact, or customer.Table: Quote \[sn\_quote\_mgmt\_core\_quote\]

 Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

The role of the party in the context of the quote \(e.g., Account, Contact, or Customer\).Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

This value is always `ProductOfferingRef`.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the quote item.Data type: String

</td></tr><tr><td>

@type

</td><td>

Type of resource. This value is always `Quote`. This information isn’t stored.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_kmf_3jm_gqb"><thead><tr><th>

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

Bad Request. A bad request type or malformed request was detected.Possible reasons:

-   Empty payload.
-   Invalid payload. Mandatory field missing: &lt;field name&gt;.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contactMedium

</td><td>

List of contact mediums. Contact information related to the quote requester.```
"contactMedium": [
 {
  "city": "String",
  "country": "String",
  "locationId": "String",
  "mediumType": "String",
  "postCode": "String",
  "stateOrProvince": "String",
  "street": "String",
  "@type": "String"
 }
]
```

</td></tr><tr><td>

contactMedium.city

</td><td>

City in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.country

</td><td>

Country in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.locationId

</td><td>

Sys\_id of the location listed in the Location \[cmn\_location\] table or custom address.Data type: String

</td></tr><tr><td>

contactMedium.mediumType

</td><td>

Type of contact medium, such as email address, telephone number, or postal address.Data type: String

</td></tr><tr><td>

contactMedium.postCode

</td><td>

Postal code of the quote requester.Data type: String

</td></tr><tr><td>

contactMedium.stateOrProvince

</td><td>

State or province in which the quote requester resides.Data type: String

</td></tr><tr><td>

contactMedium.street

</td><td>

Street address of the quote requester.Data type: String

</td></tr><tr><td>

contactMedium.@type

</td><td>

Type of medium per the TMF Open API standard. For example, `GeographicalAddressContactMedium`.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the quote.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Unique consumer-provided ID for the quote.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to access the quote.Data type: String

Default: Empty string

</td></tr><tr><td>

note

</td><td>

List of notes associated with the quote. Data type: Array

```
"note": [
  {
    "text": "String",
    "@type": "String"
 }
]
```

</td></tr><tr><td>

note.text

</td><td>

Contents of the note. Data type: String

</td></tr><tr><td>

note.@type

</td><td>

This value is always `Note`.Data type: String

</td></tr><tr><td>

quoteDate

</td><td>

Date and time at which the quote was created.Data type: String

</td></tr><tr><td>

quoteItem

</td><td>

A list of quote items. Each quote item describes an action for a product to be quoted.```
"quoteItem": [
 {
  "action": "String",
  "id": "String",
  "product": {Object},
  "productOffering": {Object},
  "productRelationship": {Object},
  "quantity": Number,
  "state": "String",
  "@type": "String"
 }
]
```

Data type: Array of Objects

</td></tr><tr><td>

quoteItem.action

</td><td>

Action to be performed on this quote item \(add, modify, remove, etc.\).Data type: String

</td></tr><tr><td>

quoteItem.id

</td><td>

Sys\_id of the quote item.Table: Quote Line Item \[sn\_quote\_mgmt\_core\_quote\_line\_item\]

Data type: String

</td></tr><tr><td>

quoteItem.product

</td><td>

List of products included in the quote.```
"product": {
  "characteristic": "String",
  "specification": "String",
  "@type": "String"
}
```

Data type: Object

</td></tr><tr><td>

quoteItem.product. characteristic

</td><td>

List of product characteristics.Data type: Array of Objects

```
"characteristic": [
  {
    "id": "String",
    "name": "String",
    "@type": "String",
    "value": "String"
  }
]
```

See [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=zurich&pubname=zurich-order-management&ft:locale=en-US).

</td></tr><tr><td>

quoteItem.product. characteristic.id

</td><td>

Sys\_id of the product characteristic.Table: Quote Line Characteristic \[sn\_quote\_mgmt\_core\_quote\_line\_characteristic\]

Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.name

</td><td>

Name of the product characteristic.Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.@type

</td><td>

This value is always `StringCharacteristic`.Data type: String

</td></tr><tr><td>

quoteItem.product. characteristic.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

quoteItem.product. specification

</td><td>

Detailed description of a tangible or intangible object made available externally in the form of a ProductOffering to customers or other parties playing a party role.Data type: String

</td></tr><tr><td>

quoteItem.product.@type

</td><td>

This value is always `Product`.Data type: String

</td></tr><tr><td>

quoteItem.productOffering

</td><td>

A product offering reference \(ProductOfferingRef\). A product offering represents entities that are orderable from the provider of the catalog.```
"productOffering": {
  "href": "String",
  "name": "String",
  "name": "String",
  "@type": "String"
}
```

Data type: Object

</td></tr><tr><td>

quoteItem. productOffering.href

</td><td>

Reference of the related entity.Data type: String

</td></tr><tr><td>

quoteItem. productOffering.id

</td><td>

Sys\_id of product offering.Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

Data type: String

</td></tr><tr><td>

quoteItem. productOffering.name

</td><td>

Name of the related entity.Data type: String

</td></tr><tr><td>

quoteItem. productOffering.@type

</td><td>

This value is always `ProductOfferingRef`.Data type: String

</td></tr><tr><td>

quoteItem.productRelationship

</td><td>

A list of quote items. Each quote item describes an action for a product to be quoted.```
"productRelationship": [
 {
  "product": "String",
  "relationshipType": "String"
 }
]
```

Data type: Array of Objects

</td></tr><tr><td>

quoteItem.productRelationship. product

</td><td>

A product reference or value \(ProductRefOrValue\). A produt to be created defined by value or existing defined by reference.The product meets one of the following criteria:

-   Pending product creation defined by the value.
-   Existing product defined by reference.

Data type: String

</td></tr><tr><td>

quoteItem.productRelationship. relationshipType

</td><td>

Type of the product relationship, such as `bundled` if the product is a bundle and you want to describe the the bundled products within.Data type: String

</td></tr><tr><td>

quoteItem.quantity

</td><td>

Quantity asked for this quote item.Data type: Number

</td></tr><tr><td>

quoteItem.state

</td><td>

A quote state type \(QuoteStateType\). State of the quote.Data type: String

</td></tr><tr><td>

quoteItem.@type

</td><td>

This value is always `QuoteItem`.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order.Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String",
    "role": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the quote table to get the account, contact, or customer.Table: Quote \[sn\_quote\_mgmt\_core\_quote\]

 Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

The role of the party in the context of the quote \(e.g., Account, Contact, or Customer\).Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

This value is always `ProductOfferingRef`.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the quote item.Data type: String

</td></tr><tr><td>

@type

</td><td>

Type of resource. This value is always `Quote`. This information isn’t stored.Data type: String

</td></tr></tbody>
</table>The following example shows how to create a quote.

```
curl "http://localhost:8080/api/sn_tmf_api/quote_management_api/quote" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"@type\": \"Quote\",
  \"description\": \"Quote for Internet and OTT Bundle\",
  \"state\": \"Draft\",
  \"externalId\": \"12233\",
  \"contactMedium\": [
    {
      \"@type\": \"GeographicalAddressContactMedium\",
      \"mediumType\": \"ShippingAddressRef\",
      \"locationId\": \"6774fee611383110f877366201dea64f\",
      \"city\": \"Santa Clara\",
      \"country\": \"USA\",
      \"postCode\": \"95050\",
      \"stateOrProvince\": \"CA\",
      \"street\": \"2866 Stevens Creek Blvd\"
    }
  ],
  \"note\": [
    {
      \"@type\": \"Note\",
      \"text\": \"This is a quote request for the Internet and OTT Bundle\"
    }
  ],
  \"quoteItem\": [
    {
      \"id\": \"ea88d77c4165ae10f8776348db5f9196\",
      \"@type\": \"QuoteItem\",
      \"action\": \"add\",
      \"quantity\": \"1\",
      \"state\": \"Draft\",
      \"product\": {
        \"@type\": \"Product\"
      },
      \"productOffering\": {
        \"id\": \"ffeb447211bc3110f877366201dea6df\",
        \"href\": \"api/sn_tmf_api/catalogmanagement/productOffering/ffeb447211bc3110f877366201dea6df\",
        \"name\": \"Internet and OTT Bundle\",
        \"@type\": \"ProductOfferingRef\"
      },
      \"productRelationship\": [
        {
          \"product\": \"3688d77c4165ae10f8776348db5f91cf\",
          \"relationshipType\": \"HasChild\"
        },
        {
          \"product\": \"3a881b7c4165ae10f8776348db5f911b\",
          \"relationshipType\": \"HasChild\"
        },
        {
          \"product\": \"7e88d77c4165ae10f8776348db5f91fb\",
          \"relationshipType\": \"HasChild\"
        }
      ]
    },
    {
      \"id\": \"3688d77c4165ae10f8776348db5f91cf\",
      \"@type\": \"QuoteItem\",
      \"action\": \"add\",
      \"quantity\": \"1\",
      \"state\": \"Draft\",
      \"product\": {
        \"@type\": \"Product\"
      },
      \"productOffering\": {
        \"id\": \"0761dd9fd0a63110f8770dbf976be173\",
        \"href\": \"api/sn_tmf_api/catalogmanagement/productOffering/0761dd9fd0a63110f8770dbf976be173\",
        \"name\": \"Solana Modem N Series\",
        \"@type\": \"ProductOfferingRef\"
      },
      \"productRelationship\": [
        {
          \"product\": \"ea88d77c4165ae10f8776348db5f9196\",
          \"relationshipType\": \"HasParent\"
        }
      ]
    },
    {
      \"id\": \"7e88d77c4165ae10f8776348db5f91fb\",
      \"@type\": \"QuoteItem\",
      \"action\": \"add\",
      \"quantity\": \"1\",
      \"state\": \"Draft\",
      \"product\": {
        \"@type\": \"Product\"
      },
      \"productOffering\": {
        \"id\": \"8b61dd9fd0a63110f8770dbf976be140\",
        \"href\": \"api/sn_tmf_api/catalogmanagement/productOffering/8b61dd9fd0a63110f8770dbf976be140\",
        \"name\": \"Basic internet - 100 Mbps Plan\",
        \"@type\": \"ProductOfferingRef\"
      },
      \"productRelationship\": [
        {
          \"product\": \"ea88d77c4165ae10f8776348db5f9196\",
          \"relationshipType\": \"HasParent\"
        }
      ]
    },
    {
      \"id\": \"3a881b7c4165ae10f8776348db5f911b\",
      \"@type\": \"QuoteItem\",
      \"action\": \"add\",
      \"quantity\": \"1\",
      \"state\": \"Draft\",
      \"product\": {
        \"@type\": \"Product\"
      },
      \"productOffering\": {
        \"id\": \"62619d9fd0a63110f8770dbf976be180\",
        \"href\": \"api/sn_tmf_api/catalogmanagement/productOffering/62619d9fd0a63110f8770dbf976be180\",
        \"name\": \"Solana Movie streaming channel\",
        \"@type\": \"ProductOfferingRef\"
      },
      \"productRelationship\": [
        {
          \"product\": \"ea88d77c4165ae10f8776348db5f9196\",
          \"relationshipType\": \"HasParent\"
        }
      ]
    }
  ],
  \"relatedParty\": [
    {
      \"role\": \"Customer\",
      \"id\": \"ab9a0e8b2fc9a610b79db3bf42faf3a6\",
      \"name\": \"Funco Intl\",
      \"@type\": \"RelatedPartyRef\",
      \"@referredType\": \"Organization\"
    }
  ]
}" \
--user 'userName':'password'
```

Response body.

```
{
  "@type": "Quote",
  "description": "Quote for Internet and OTT Bundle",
  "state": "Draft",
  "externalId": "12233",
  "contactMedium": [
    {
      "@type": "GeographicalAddressContactMedium",
      "mediumType": "ShippingAddressRef",
      "locationId": "6774fee611383110f877366201dea64f",
      "city": "Santa Clara",
      "country": "USA",
      "postCode": "95050",
      "stateOrProvince": "CA",
      "street": "2866 Stevens Creek Blvd"
    }
  ],
  "note": [
    {
      "@type": "Note",
      "text": "This is a quote request for the Internet and OTT Bundle"
    }
  ],
  "quoteItem": [
    {
      "id": "ea88d77c4165ae10f8776348db5f9196",
      "@type": "QuoteItem",
      "action": "add",
      "quantity": "1",
      "state": "Draft",
      "product": {
        "@type": "Product"
      },
      "productOffering": {
        "id": "ffeb447211bc3110f877366201dea6df",
        "href": "api/sn_tmf_api/catalogmanagement/productOffering/ffeb447211bc3110f877366201dea6df",
        "name": "Internet and OTT Bundle",
        "@type": "ProductOfferingRef",
        "internalVersion": "1",
        "version": "",
        "internalId": "ffeb447211bc3110f877366201dea6df"
      },
      "productRelationship": [
        {
          "product": "3688d77c4165ae10f8776348db5f91cf",
          "relationshipType": "HasChild"
        },
        {
          "product": "3a881b7c4165ae10f8776348db5f911b",
          "relationshipType": "HasChild"
        },
        {
          "product": "7e88d77c4165ae10f8776348db5f91fb",
          "relationshipType": "HasChild"
        }
      ]
    },
    {
      "id": "3688d77c4165ae10f8776348db5f91cf",
      "@type": "QuoteItem",
      "action": "add",
      "quantity": "1",
      "state": "Draft",
      "product": {
        "@type": "Product"
      },
      "productOffering": {
        "id": "0761dd9fd0a63110f8770dbf976be173",
        "href": "api/sn_tmf_api/catalogmanagement/productOffering/0761dd9fd0a63110f8770dbf976be173",
        "name": "Solana Modem N Series",
        "@type": "ProductOfferingRef",
        "internalVersion": "1",
        "version": "",
        "internalId": "0761dd9fd0a63110f8770dbf976be173"
      },
      "productRelationship": [
        {
          "product": "ea88d77c4165ae10f8776348db5f9196",
          "relationshipType": "HasParent"
        }
      ]
    },
    {
      "id": "7e88d77c4165ae10f8776348db5f91fb",
      "@type": "QuoteItem",
      "action": "add",
      "quantity": "1",
      "state": "Draft",
      "product": {
        "@type": "Product"
      },
      "productOffering": {
        "id": "8b61dd9fd0a63110f8770dbf976be140",
        "href": "api/sn_tmf_api/catalogmanagement/productOffering/8b61dd9fd0a63110f8770dbf976be140",
        "name": "Basic internet - 100 Mbps Plan",
        "@type": "ProductOfferingRef",
        "internalVersion": "1",
        "version": "",
        "internalId": "8b61dd9fd0a63110f8770dbf976be140"
      },
      "productRelationship": [
        {
          "product": "ea88d77c4165ae10f8776348db5f9196",
          "relationshipType": "HasParent"
        }
      ]
    },
    {
      "id": "3a881b7c4165ae10f8776348db5f911b",
      "@type": "QuoteItem",
      "action": "add",
      "quantity": "1",
      "state": "Draft",
      "product": {
        "@type": "Product"
      },
      "productOffering": {
        "id": "62619d9fd0a63110f8770dbf976be180",
        "href": "api/sn_tmf_api/catalogmanagement/productOffering/62619d9fd0a63110f8770dbf976be180",
        "name": "Solana Movie streaming channel",
        "@type": "ProductOfferingRef",
        "internalVersion": "1",
        "version": "",
        "internalId": "62619d9fd0a63110f8770dbf976be180"
      },
      "productRelationship": [
        {
          "product": "ea88d77c4165ae10f8776348db5f9196",
          "relationshipType": "HasParent"
        }
      ]
    }
  ],
  "relatedParty": [
    {
      "role": "Customer",
      "id": "ab9a0e8b2fc9a610b79db3bf42faf3a6",
      "name": "Funco Intl",
      "@type": "RelatedPartyRef",
      "@referredType": "Organization"
    }
  ],
  "id": "acc805bcfff5a610b79dffffffffffe6",
  "href": "api/sn_tmf_api/quote_management_api/quote/acc805bcfff5a610b79dffffffffffe6"
}
```

