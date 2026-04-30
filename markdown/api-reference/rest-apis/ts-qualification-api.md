---
title: Technical Service Qualification Open API
description: The Technical Service Qualification Open API provides endpoints to check the availability of resources and services before submitting orders for fulfillment.Retrieves a technical qualification request that is associated with a given customer order ID.Retrieves a list of all technical qualification requests.Creates a technical service qualification request entity containing a list of qualification items.Processes a technical service qualification result sent to the Technical Service Qualification Open API.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 50
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Technical Service Qualification Open API

The Technical Service Qualification Open API provides endpoints to check the availability of resources and services before submitting orders for fulfillment.

This API is a ServiceNow implementation of the TMF645 Service Qualification API REST Specification. For more information about service qualification requests, see [Service qualification requests](https://www.servicenow.com/docs/access?context=order-mgt-tsq-about&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US).

The Technical Service Qualification Open API is provided within the `sn_ord_qual_mgmt` namespace and requires the following plugins:

-   Product Catalog Management Core \[com.sn\_prd\_pm\]
-   Product Catalog Advanced \[com.sn\_prd\_pm\_adv\]
-   Order Qualification Management \[com.sn\_ord\_qual\_mgmt\]
-   Order Management for Telecom, Media &amp; Tech \[com.sn\_tmt\_core\]
-   Telecom Core \[com.sn\_tmt\_core\]

The sn\_ind\_tmt\_orm.order\_integrator role is required to use this API.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Technical Service Qualification Open API - GET sn\_ord\_qual\_mgmt/qualification/checkServiceQualification/\{id\}

Retrieves a technical qualification request that is associated with a given customer order ID.

This endpoint retrieves order information from the following tables:

-   Customer Order \[sn\_ind\_tmt\_orm\_order\]
-   Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

### URL format

Default URL: `/api/sn_ord_qual_mgmt/qualification/checkServiceQualification/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the qualification customer order to retrieve.Data type: String

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

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

| | |
|---|---|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON or XML\)

<table id="id_lb3_gpq_fwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="TSQ-return-id"><td>

id

</td><td>

Sys\_id of the qualification customer order.Data type: String

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr id="TSQ-return-href"><td>

href

</td><td>

Relative link to the qualification order record. Data type: String

</td></tr><tr id="TSQ-return-descriptions"><td>

description

</td><td>

Description of the qualification request which is fetched from the short\_description field of the customer order.Data type: String

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr id="TSQ-return-externalId"><td>

externalId

</td><td>

External ID of the customer order. Data type: String

Table: in the external\_id field of the Customer Order \[sn\_ind\_tmt\_orm\_order\] table.

</td></tr><tr id="TSQ-return-qualificationResult"><td>

qualificationResult

</td><td>

Qualification status of the result field of the customer order. Possible values:

-   alternate
-   none
-   pending
-   qualified
-   unqualified

Data type: String

</td></tr><tr id="TSQ-return-state"><td>

state

</td><td>

State of customer order from the status field of customer order.Data type: String

</td></tr><tr id="TSQ-return-type"><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the qualification. This value is always `CheckServiceQualification`. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-checkServiceQualificationDate"><td>

checkServiceQualificationDate

</td><td>

Date and time the qualification request that was created from the order\_date field of the customer order.Data type: String

Format: YYYY-MM-DDTHH:MM:SS.SSSZ

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr id="TSQ-return-effectiveQualificationDate"><td>

effectiveQualificationDate

</td><td>

Effective qualification date fetched from the order\_date field of the customer order.Data type: String

Format: YYYY-MM-DDTHH:MM:SS.SSSZ

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr id="TSQ-return-expectedQualificationDate"><td>

expectedQualificationDate

</td><td>

Stores the expected qualification date. Persisted in expected\_end\_date field of the customer order.Data type: String

Format: YYYY-MM-DDTHH:MM:SS.SSSZ

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr id="TSQ-return-relatedParty"><td>

relatedParty

</td><td>

List of contacts for the qualification request. Each contact is an object in the array.Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr id="TSQ-return-relatedParty.id"><td>

relatedParty.id

</td><td>

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order.Data type: String

Table: Account \[customer\_account\] table, Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\]

</td></tr><tr id="TSQ-return-relatedParty.name"><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer.Data type: String

</td></tr><tr id="TSQ-return-relatedParty.type"><td>

relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for the order line item contact. This value is always `RelatedParty`. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-relatedParty.referredType"><td>

relatedParty.@referredType

</td><td>

Type of related party.Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem"><td>

serviceQualificationItem

</td><td>

List of service qualification items containing information about location, service information, and service characteristics. Stored as order line items for the customer order. Data type: Array of Objects

```
"serviceQualificationItem": [
  {
    "id": "String",
    "action": "String",
    "expectedServiceAvailabilityDate": "Number",
    "service": {Object},
    "@type": "String"
  }
]
```

</td></tr><tr id="TSQ-return-serviceQualificationItem.id"><td>

serviceQualificationItem.id

</td><td>

ID of the qualification item.Data type: String

Stored in: The external\_id field of customer order line item in the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr id="TSQ-return-serviceQualificationItem.qualificationResult"><td>

serviceQualificationItem.qualificationResult

</td><td>

Result of qualification item. Stored in the ‘result’ field of customer order line item. Possible values:

-   alternate
-   none
-   pending
-   qualified
-   unqualified

Data type: String

Table: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.state"><td>

serviceQualificationItem.state

</td><td>

State of qualification item derived from the ‘status’ field of customer order line item. Data type: String

Table: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.quantity"><td>

serviceQualificationItem.quantity

</td><td>

Quantity of qualification item derived from the ‘quantity’ field of customer order line item.Data type: Number

Table:Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.type"><td>

serviceQualificationItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the qualification item. This value is always ServiceQualificationItem. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service"><td>

serviceQualificationItem.service

</td><td>

Service information which includes details about location \(place\), service specifications, and service characteristics.Data type: Object

```
"service": {
  "@type": "String",
  "place": [Array],
  "serviceCharacteristic": [Array],
  "serviceSpecification": {Object}
}
```

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.type"><td>

serviceQualificationItem.service.@type

</td><td>

Part of TMF Open API standard. Annotation for the service. This value is always `Service`. This information is not stored. Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.place"><td>

serviceQualificationItem.service.place

</td><td>

Location information for the service qualification item.Data type: Array of Objects

**Note:** This array can contain only one location.

```
"place": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String"
  }
]
```

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.place.id"><td>

serviceQualificationItem.service.place.id

</td><td>

Sys\_id of the location.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.place.name"><td>

serviceQualificationItem.service.place.name

</td><td>

Name of the location. Not verified against an entry in the Location \[cmn\_location\] table.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.place.type"><td>

serviceQualificationItem.service.place.@type

</td><td>

Part of TMF Open API standard. Annotation for Service. This value is always `GeographicSite`. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification"><td>

serviceQualificationItem.service.serviceSpecification

</td><td>

Service specification details for the qualification item.Data type: Array of Objects

```
"serviceSpecification": {
  "id": "String",
  "internalVersion": "Number",
  "internalId": "String",
  "name": "String"
  "@type": "ServiceSpecification"
  "version": "String",
}

```

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.id"><td>

serviceQualificationItem.service.serviceSpecification.id

</td><td>

External ID or initial version of the service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.name"><td>

serviceQualificationItem.service.serviceSpecification.name

</td><td>

Name of the service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.version"><td>

serviceQualificationItem.service.serviceSpecification.version

</td><td>

External version of the service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.internalVersion"><td>

serviceQualificationItem.service.serviceSpecification.internalVersion

</td><td>

Internal version of the service specification.Data type: Number

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.internalId"><td>

serviceQualificationItem.service.serviceSpecification.internalId

</td><td>

Initial version of the service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.type"><td>

serviceQualificationItem.service.serviceSpecification.@type

</td><td>

Part of TMF Open API standard. Annotation for Service Specification. This value is always `ServiceSpecification`. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceCharacteristic"><td>

serviceQualificationItem.service.serviceCharacteristic

</td><td>

List of service characteristics.Data type: Array of objects

```
"serviceCharacteristic": [
  {
    "name": "String",
    "value": "String",
    "valueType": "String"
  }
]
```

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceCharacteristic.valueType"><td>

serviceQualificationItem.service.serviceCharacteristic.valueType

</td><td>

Value type of the characteristic.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceCharacteristic.name"><td>

serviceQualificationItem.service.serviceCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceCharacteristic.value"><td>

serviceQualificationItem.service.serviceCharacteristic.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal"><td>

ServiceQualificationItem.alternateServiceProposal

</td><td>

Alternate service proposal for the qualification order.Data type: String

Stored in: Alternate Proposal \[sn\_ord\_qual\_mgmt\_alternate\_proposal\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.id"><td>

ServiceQualificationItem.alternateServiceProposal.id

</td><td>

Sys\_id of the alternate proposal record.Data type: String

Table: Alternate Proposal \[sn\_ord\_qual\_mgmt\_alternate\_proposal\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.alternateServiceAvailabilityDate"><td>

ServiceQualificationItem.alternateServiceProposal.alternateServiceAvailabilityDate

</td><td>

The available\_date field value of the alternate proposal entry in the Alternate Proposal \[sn\_ord\_qual\_mgmt\_alternate\_proposal\] table.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.alternateService"><td>

serviceQualificationItem.alternateServiceProposal.alternateService

</td><td>

Service information represented by the alternate proposal.Data type: Object

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.alternateService.serviceSpecification"><td>

serviceQualificationItem.alternateServiceProposal.alternateService.serviceSpecification

</td><td>

Service specification of the alternate proposal persisted in specification.Data type: Object

Table: Alternate Proposal \[sn\_ord\_qual\_mgmt\_alternate\_proposal\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.id"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.id

</td><td>

External ID or initial version of the alternate service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.name"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.name

</td><td>

Name of the alternate service specification. Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.version"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.version

</td><td>

External version of the alternate service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.internalVersion"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.internalVersion

</td><td>

Internal version of the alternate service specification.Data type: Number

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.internalId"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.internalId

</td><td>

Initial version of the alternate service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.type"><td>

ServiceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.@type

</td><td>

Part of TMF Open API standard. Annotation for Service Specification. This value is always `ServiceSpecification`. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.serviceCharacteristic"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceCharacteristic

</td><td>

List of service characteristics for the alternate service proposal.Data type: Array of Objects

```
"serviceCharacteristic": [
  {
    "name": "String",
    "value": "String",
    "valueType": "String"
  }
]
```

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.serviceCharacteristic.valueType"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceCharacteristic.valueType

</td><td>

Value type of the alternate service characteristic.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.serviceCharacteristic.name"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceCharacteristic.name

</td><td>

Name of the alternate service characteristic.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.serviceCharacteristic.value"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceCharacteristic.value

</td><td>

Value of the alternate service characteristic.Data type: String

</td></tr><tr id="serviceQualificationItem.eligibilityUnavailabilityReason"><td>

serviceQualificationItem.eligibilityUnavailabilityReason

</td><td>

List of service eligibility unavailability reasons to explain why the service is not available. Data type: Array

Stored in: The unavailability\_reason field of the Domain Order \[sn\_ind\_tmt\_orm\_domain\_order\] table.

</td></tr><tr id="serviceQualificationItem.eligibilityUnavailabilityReason.code"><td>

serviceQualificationItem.eligibilityUnavailabilityReason.code

</td><td>

Service eligibility unavailability reason code.Data type: String

</td></tr><tr id="serviceQualificationItem.eligibilityUnavailabilityReason.label"><td>

serviceQualificationItem.eligibilityUnavailabilityReason.label

</td><td>

Service eligibility unavailability reason label.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

The following example retrieves an entire specific qualification order associated with a given Sys\_id of a qualification customer order.

```
curl -location --request GET "https://instance.service-now.com/api/sn_ord_qual_mgmt/qualification/checkServiceQualification/4b5aa0a538b31110f877c8d44c4b8947" \ 
--user "username":"password"

```

Response:

```
[
  {
    "id": "001b359545371150f877e0588eca21ca",
    "href": "/api/sn_ord_qual_mgmt/qualification/checkServiceQualification/001b359545371150f877e0588eca21ca",
    "description": "check service qualification illustration",
    "externalId": "CSQ1",
    "qualificationResult": "none",
    "state": "new",
    "@type": "CheckServiceQualification",
    "checkServiceQualificationDate": "2022-12-14T23:44:44.000Z",
    "relatedParty": [
      {
        "id": "eaf68911c35420105252716b7d40ddde",
        "name": "Sally Thomas",
        "@type": "RelatedParty",
        "@referredType": "CustomerContact"
      },
      {
        "id": "ffc68911c35420105252716b7d40dd55",
        "name": "Funco Intl",
        "@type": "RelatedParty",
        "@referredType": "Customer"
      },
      {
        "id": "59f16de1c3b67110ff00ed23a140dd9e",
        "name": "Funco External",
        "@type": "RelatedParty",
        "@referredType": "Consumer"
      }
    ],
    "serviceSpecification": {
      "id": "91478553b7969910ff00f203ae11a97d",
      "name": "Broadband Service",
      "version": "",
      "internalVersion": "1",
      "internalId": "91478553b7969910ff00f203ae11a97d",
      "@type": "ServiceSpecification"
    },
    "place": {
      "id": "5671dd2ec3a53010188473ce3640dd81",
      "name": "3000 Main Street, Santa Clara, CA",
      "@referredType": "GeographicSite"
    },
    "expectedQualificationDate": "2022-10-11T15:20:39.000Z"
  },
  {
    "id": "0236b75145fb1150f877e0588eca2145",
    "href": "/api/sn_ord_qual_mgmt/qualification/checkServiceQualification/0236b75145fb1150f877e0588eca2145",
    "description": "check service qualification illustration",
    "externalId": "CSQ1",
    "qualificationResult": "none",
    "state": "new",
    "@type": "CheckServiceQualification",
    "checkServiceQualificationDate": "2022-12-15T08:57:50.000Z",
    "relatedParty": [
      {
        "id": "eaf68911c35420105252716b7d40ddde",
        "name": "Sally Thomas",
        "@type": "RelatedParty",
        "@referredType": "CustomerContact"
      },
      {
        "id": "ffc68911c35420105252716b7d40dd55",
        "name": "Funco Intl",
        "@type": "RelatedParty",
        "@referredType": "Customer"
      },
      {
        "id": "59f16de1c3b67110ff00ed23a140dd9e",
        "name": "Funco External",
        "@type": "RelatedParty",
        "@referredType": "Consumer"
      }
    ],
    "serviceQualificationItem": [
      {
        "id": "110",
        "qualificationResult": "none",
        "state": "new",
        "quantity": "1",
        "@type": "ServiceQualificationItem",
        "service": {
          "@type": "Service",
          "serviceCharacteristic": [
            {
              "name": "Fiber Speed",
              "valueType": "choice",
              "value": "1Gbps"
            }
          ],
          "serviceSpecification": {
            "id": "4d2b5799457b1150f877e0588eca2116",
            "name": "CFS3",
            "version": "",
            "internalVersion": "1",
            "internalId": "4d2b5799457b1150f877e0588eca2116",
            "@type": "ServiceSpecification"
          },
          "place": {
            "id": "5671dd2ec3a53010188473ce3640dd81",
            "name": "3000 Main Street, Santa Clara, CA",
            "@referredType": "GeographicSite"
          }
        }
      },
      {
        "id": "130",
        "qualificationResult": "none",
        "state": "new",
        "quantity": "1",
        "@type": "ServiceQualificationItem",
        "service": {
          "@type": "Service",
          "serviceCharacteristic": [
            {
              "name": "Wireless Speed",
              "valueType": "choice",
              "value": "100 Mbps"
            }
          ],
          "serviceSpecification": {
            "id": "28733d1d45f31150f877e0588eca2163",
            "name": "CFS2",
            "version": "",
            "internalVersion": "1",
            "internalId": "28733d1d45f31150f877e0588eca2163",
            "@type": "ServiceSpecification"
          },
          "place": {
            "id": "5671dd2ec3a53010188473ce3640dd81",
            "name": "3000 Main Street, Santa Clara, CA",
            "@referredType": "GeographicSite"
          }
        }
      },
      {
        "id": "100",
        "qualificationResult": "none",
        "state": "new",
        "quantity": "1",
        "@type": "ServiceQualificationItem",
        "service": {
          "@type": "Service",
          "serviceCharacteristic": [
            {
              "name": "Speed",
              "valueType": "choice",
              "value": ""
            }
          ],
          "serviceSpecification": {
            "id": "b3933d9d45f31150f877e0588eca21fc",
            "name": "Access Service",
            "version": "",
            "internalVersion": "1",
            "internalId": "b3933d9d45f31150f877e0588eca21fc",
            "@type": "ServiceSpecification"
          },
          "place": {
            "id": "5671dd2ec3a53010188473ce3640dd81",
            "name": "3000 Main Street, Santa Clara, CA",
            "@referredType": "GeographicSite"
          }
        }
      },
      {
        "id": "120",
        "qualificationResult": "none",
        "state": "new",
        "quantity": "1",
        "@type": "ServiceQualificationItem",
        "service": {
          "@type": "Service",
          "serviceCharacteristic": [
            {
              "name": "DSL Speed",
              "valueType": "choice",
              "value": "500 Mbps"
            }
          ],
          "serviceSpecification": {
            "id": "1d43f91d45f31150f877e0588eca21cd",
            "name": "CFS1",
            "version": "",
            "internalVersion": "1",
            "internalId": "1d43f91d45f31150f877e0588eca21cd",
            "@type": "ServiceSpecification"
          },
          "place": {
            "id": "5671dd2ec3a53010188473ce3640dd81",
            "name": "3000 Main Street, Santa Clara, CA",
            "@referredType": "GeographicSite"
          }
        }
      }
    ],
    "expectedQualificationDate": "2022-10-11T15:20:39.000Z"
  }
]
```

## Technical Service Qualification Open API - GET sn\_ord\_qual\_mgmt/qualification/checkServiceQualification

Retrieves a list of all technical qualification requests.

This endpoint retrieves order information from the following tables:

-   Customer Order \[sn\_ind\_tmt\_orm\_order\]
-   Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

This endpoint returns 20 records by default but can return a maximum of 100 records. Use query filters to narrow results according to status, field name\(s\), description, and qualification result.

### URL format

Default URL: `/api/sn_ord_qual_mgmt/qualification/checkServiceQualification`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table id="table_qbb_tlq_fwb" class="rest_api_request_parameters"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Filters qualification orders by the 'short\_description' field of the customer order. Only orders with a short description matching the value of this parameter are returned in the response.Data type: String

</td></tr><tr><td>

fields

</td><td>

List of field names to return in the response. Invalid fields are ignored. If this parameter is not provided in the request, all fields are returned.Data type: String, comma separated

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the offset parameter to paginate record retrieval.Default: 20

Maximum: 100

Data type: Number

</td></tr><tr><td>

qualificationResult

</td><td>

Filters qualification orders by result. Only orders with a result matching the value of this parameter are returned in the response.Data type: String

</td></tr><tr><td>

state

</td><td>

Filters qualification orders by state. Only orders with a state matching the value of this parameter are returned in the response.Data type: String

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

<table id="table_wwn_rhd_ct"><thead><tr><th>

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

No record found for the filter criteria.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="id_zmj_cmq_fwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="TSQ-return-id"><td>

id

</td><td>

Sys\_id of the qualification customer order.Data type: String

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr id="TSQ-return-href"><td>

href

</td><td>

Relative link to the qualification order record. Data type: String

</td></tr><tr id="TSQ-return-descriptions"><td>

description

</td><td>

Description of the qualification request which is fetched from the short\_description field of the customer order.Data type: String

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr id="TSQ-return-externalId"><td>

externalId

</td><td>

External ID of the customer order. Data type: String

Table: in the external\_id field of the Customer Order \[sn\_ind\_tmt\_orm\_order\] table.

</td></tr><tr id="TSQ-return-qualificationResult"><td>

qualificationResult

</td><td>

Qualification status of the result field of the customer order. Possible values:

-   alternate
-   none
-   pending
-   qualified
-   unqualified

Data type: String

</td></tr><tr id="TSQ-return-state"><td>

state

</td><td>

State of customer order from the status field of customer order.Data type: String

</td></tr><tr id="TSQ-return-type"><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the qualification. This value is always `CheckServiceQualification`. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-checkServiceQualificationDate"><td>

checkServiceQualificationDate

</td><td>

Date and time the qualification request that was created from the order\_date field of the customer order.Data type: String

Format: YYYY-MM-DDTHH:MM:SS.SSSZ

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr id="TSQ-return-effectiveQualificationDate"><td>

effectiveQualificationDate

</td><td>

Effective qualification date fetched from the order\_date field of the customer order.Data type: String

Format: YYYY-MM-DDTHH:MM:SS.SSSZ

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr id="TSQ-return-expectedQualificationDate"><td>

expectedQualificationDate

</td><td>

Stores the expected qualification date. Persisted in expected\_end\_date field of the customer order.Data type: String

Format: YYYY-MM-DDTHH:MM:SS.SSSZ

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr id="TSQ-return-relatedParty"><td>

relatedParty

</td><td>

List of contacts for the qualification request. Each contact is an object in the array.Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr id="TSQ-return-relatedParty.id"><td>

relatedParty.id

</td><td>

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order.Data type: String

Table: Account \[customer\_account\] table, Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\]

</td></tr><tr id="TSQ-return-relatedParty.name"><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer.Data type: String

</td></tr><tr id="TSQ-return-relatedParty.type"><td>

relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for the order line item contact. This value is always `RelatedParty`. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-relatedParty.referredType"><td>

relatedParty.@referredType

</td><td>

Type of related party.Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem"><td>

serviceQualificationItem

</td><td>

List of service qualification items containing information about location, service information, and service characteristics. Stored as order line items for the customer order. Data type: Array of Objects

```
"serviceQualificationItem": [
  {
    "id": "String",
    "action": "String",
    "expectedServiceAvailabilityDate": "Number",
    "service": {Object},
    "@type": "String"
  }
]
```

</td></tr><tr id="TSQ-return-serviceQualificationItem.id"><td>

serviceQualificationItem.id

</td><td>

ID of the qualification item.Data type: String

Stored in: The external\_id field of customer order line item in the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr id="TSQ-return-serviceQualificationItem.qualificationResult"><td>

serviceQualificationItem.qualificationResult

</td><td>

Result of qualification item. Stored in the ‘result’ field of customer order line item. Possible values:

-   alternate
-   none
-   pending
-   qualified
-   unqualified

Data type: String

Table: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.state"><td>

serviceQualificationItem.state

</td><td>

State of qualification item derived from the ‘status’ field of customer order line item. Data type: String

Table: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.quantity"><td>

serviceQualificationItem.quantity

</td><td>

Quantity of qualification item derived from the ‘quantity’ field of customer order line item.Data type: Number

Table:Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.type"><td>

serviceQualificationItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the qualification item. This value is always ServiceQualificationItem. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service"><td>

serviceQualificationItem.service

</td><td>

Service information which includes details about location \(place\), service specifications, and service characteristics.Data type: Object

```
"service": {
  "@type": "String",
  "place": [Array],
  "serviceCharacteristic": [Array],
  "serviceSpecification": {Object}
}
```

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.type"><td>

serviceQualificationItem.service.@type

</td><td>

Part of TMF Open API standard. Annotation for the service. This value is always `Service`. This information is not stored. Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.place"><td>

serviceQualificationItem.service.place

</td><td>

Location information for the service qualification item.Data type: Array of Objects

**Note:** This array can contain only one location.

```
"place": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String"
  }
]
```

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.place.id"><td>

serviceQualificationItem.service.place.id

</td><td>

Sys\_id of the location.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.place.name"><td>

serviceQualificationItem.service.place.name

</td><td>

Name of the location. Not verified against an entry in the Location \[cmn\_location\] table.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.place.type"><td>

serviceQualificationItem.service.place.@type

</td><td>

Part of TMF Open API standard. Annotation for Service. This value is always `GeographicSite`. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification"><td>

serviceQualificationItem.service.serviceSpecification

</td><td>

Service specification details for the qualification item.Data type: Array of Objects

```
"serviceSpecification": {
  "id": "String",
  "internalVersion": "Number",
  "internalId": "String",
  "name": "String"
  "@type": "ServiceSpecification"
  "version": "String",
}

```

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.id"><td>

serviceQualificationItem.service.serviceSpecification.id

</td><td>

External ID or initial version of the service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.name"><td>

serviceQualificationItem.service.serviceSpecification.name

</td><td>

Name of the service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.version"><td>

serviceQualificationItem.service.serviceSpecification.version

</td><td>

External version of the service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.internalVersion"><td>

serviceQualificationItem.service.serviceSpecification.internalVersion

</td><td>

Internal version of the service specification.Data type: Number

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.internalId"><td>

serviceQualificationItem.service.serviceSpecification.internalId

</td><td>

Initial version of the service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.type"><td>

serviceQualificationItem.service.serviceSpecification.@type

</td><td>

Part of TMF Open API standard. Annotation for Service Specification. This value is always `ServiceSpecification`. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceCharacteristic"><td>

serviceQualificationItem.service.serviceCharacteristic

</td><td>

List of service characteristics.Data type: Array of objects

```
"serviceCharacteristic": [
  {
    "name": "String",
    "value": "String",
    "valueType": "String"
  }
]
```

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceCharacteristic.valueType"><td>

serviceQualificationItem.service.serviceCharacteristic.valueType

</td><td>

Value type of the characteristic.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceCharacteristic.name"><td>

serviceQualificationItem.service.serviceCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceCharacteristic.value"><td>

serviceQualificationItem.service.serviceCharacteristic.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal"><td>

ServiceQualificationItem.alternateServiceProposal

</td><td>

Alternate service proposal for the qualification order.Data type: String

Stored in: Alternate Proposal \[sn\_ord\_qual\_mgmt\_alternate\_proposal\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.id"><td>

ServiceQualificationItem.alternateServiceProposal.id

</td><td>

Sys\_id of the alternate proposal record.Data type: String

Table: Alternate Proposal \[sn\_ord\_qual\_mgmt\_alternate\_proposal\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.alternateServiceAvailabilityDate"><td>

ServiceQualificationItem.alternateServiceProposal.alternateServiceAvailabilityDate

</td><td>

The available\_date field value of the alternate proposal entry in the Alternate Proposal \[sn\_ord\_qual\_mgmt\_alternate\_proposal\] table.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.alternateService"><td>

serviceQualificationItem.alternateServiceProposal.alternateService

</td><td>

Service information represented by the alternate proposal.Data type: Object

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.alternateService.serviceSpecification"><td>

serviceQualificationItem.alternateServiceProposal.alternateService.serviceSpecification

</td><td>

Service specification of the alternate proposal persisted in specification.Data type: Object

Table: Alternate Proposal \[sn\_ord\_qual\_mgmt\_alternate\_proposal\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.id"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.id

</td><td>

External ID or initial version of the alternate service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.name"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.name

</td><td>

Name of the alternate service specification. Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.version"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.version

</td><td>

External version of the alternate service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.internalVersion"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.internalVersion

</td><td>

Internal version of the alternate service specification.Data type: Number

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.internalId"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.internalId

</td><td>

Initial version of the alternate service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.type"><td>

ServiceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.@type

</td><td>

Part of TMF Open API standard. Annotation for Service Specification. This value is always `ServiceSpecification`. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.serviceCharacteristic"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceCharacteristic

</td><td>

List of service characteristics for the alternate service proposal.Data type: Array of Objects

```
"serviceCharacteristic": [
  {
    "name": "String",
    "value": "String",
    "valueType": "String"
  }
]
```

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.serviceCharacteristic.valueType"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceCharacteristic.valueType

</td><td>

Value type of the alternate service characteristic.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.serviceCharacteristic.name"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceCharacteristic.name

</td><td>

Name of the alternate service characteristic.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.serviceCharacteristic.value"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceCharacteristic.value

</td><td>

Value of the alternate service characteristic.Data type: String

</td></tr><tr id="serviceQualificationItem.eligibilityUnavailabilityReason"><td>

serviceQualificationItem.eligibilityUnavailabilityReason

</td><td>

List of service eligibility unavailability reasons to explain why the service is not available. Data type: Array

Stored in: The unavailability\_reason field of the Domain Order \[sn\_ind\_tmt\_orm\_domain\_order\] table.

</td></tr><tr id="serviceQualificationItem.eligibilityUnavailabilityReason.code"><td>

serviceQualificationItem.eligibilityUnavailabilityReason.code

</td><td>

Service eligibility unavailability reason code.Data type: String

</td></tr><tr id="serviceQualificationItem.eligibilityUnavailabilityReason.label"><td>

serviceQualificationItem.eligibilityUnavailabilityReason.label

</td><td>

Service eligibility unavailability reason label.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

The following GET call retrieves all qualification orders for an instance.

```
curl -location --request GET "https://instance.service-now.com/api/sn_ord_qual_mgmt/qualification/checkServiceQualification" \ 
--user "username":"password"
```

Response:

```
[{
        "id": "001b359545371150f877e0588eca21ca",
        "href": "/api/sn_ord_qual_mgmt/qualification/checkServiceQualification/001b359545371150f877e0588eca21ca",
        "description": "check service qualification illustration",
        "externalId": "CSQ1",
        "qualificationResult": "none",
        "state": "new",
        "@type": "CheckServiceQualification",
        "checkServiceQualificationDate": "2022-12-14T23:44:44.000Z",
        "relatedParty": [{
                "id": "eaf68911c35420105252716b7d40ddde",
                "name": "Sally Thomas",
                "@type": "RelatedParty",
                "@referredType": "CustomerContact"
            },
            {
                "id": "ffc68911c35420105252716b7d40dd55",
                "name": "Funco Intl",
                "@type": "RelatedParty",
                "@referredType": "Customer"
            },
            {
                "id": "59f16de1c3b67110ff00ed23a140dd9e",
                "name": "Funco External",
                "@type": "RelatedParty",
                "@referredType": "Consumer"
            }
            {
                "id": "59f16de1c3b67110ff00ed23a140dd9e",
                "name": "Funco External",
                "@type": "RelatedParty",
                "@referredType": "Consumer"
            }
        ],
        "serviceSpecification": {
            "id": "91478553b7969910ff00f203ae11a97d",
            "name": "Broadband Service",
            "version": "",
            "internalVersion": "1",
            "internalId": "91478553b7969910ff00f203ae11a97d",
            "@type": "ServiceSpecification"
        },
        "place": {
            "id": "5671dd2ec3a53010188473ce3640dd81",
            "name": "3000 Main Street, Santa Clara, CA",
            "@referredType": "GeographicSite"
        }
    }
}],
"expectedQualificationDate": "2022-10-11T15:20:39.000Z"
}, {
    "id": "0236b75145fb1150f877e0588eca2145",
    "href": "/api/sn_ord_qual_mgmt/qualification/checkServiceQualification/0236b75145fb1150f877e0588eca2145",
    "description": "check service qualification illustration",
    "externalId": "CSQ1",
    "qualificationResult": "none",
    "state": "new",
    "@type": "CheckServiceQualification",
    "checkServiceQualificationDate": "2022-12-15T08:57:50.000Z",
    "relatedParty": [{
            "id": "ffc68911c35420105252716b7d40dd55",
            "name": "Funco Intl",
            "@type": "RelatedParty",
            "@referredType": "Customer"
        },
        {
            "id": "eaf68911c35420105252716b7d40ddde",
            "name": "Sally Thomas",
            "@type": "RelatedParty",
            "@referredType": "CustomerContact"
        }
            {
                "id": "59f16de1c3b67110ff00ed23a140dd9e",
                "name": "Funco External",
                "@type": "RelatedParty",
                "@referredType": "Consumer"
            }
    ],
    "serviceQualificationItem": [{
            "id": "110",
            "qualificationResult": "none",
            "state": "new",
            "quantity": "1",
            "@type": "ServiceQualificationItem",
            "service": {
                "@type": "Service",
                "serviceCharacteristic": [{
                    "name": "Fiber Speed",
                    "valueType": "choice",
                    "value": "1Gbps"
                }],
                "serviceSpecification": {
                    "id": "4d2b5799457b1150f877e0588eca2116",
                    "name": "CFS3",
                    "version": "",
                    "internalVersion": "1",
                    "internalId": "4d2b5799457b1150f877e0588eca2116",
                    "@type": "ServiceSpecification"
                },
                "place": {
                    "id": "5671dd2ec3a53010188473ce3640dd81",
                    "name": "3000 Main Street, Santa Clara, CA",
                    "@referredType": "GeographicSite"
                }
            }
        },
        {
            "id": "130",
            "qualificationResult": "none",
            "state": "new",
            "quantity": "1",
            "@type": "ServiceQualificationItem",
            "service": {
                "@type": "Service",
                "serviceCharacteristic": [{
                    "name": "Wireless Speed",
                    "valueType": "choice",
                    "value": "100 Mbps"
                }],
                "serviceSpecification": {
                    "id": "28733d1d45f31150f877e0588eca2163",
                    "name": "CFS2",
                    "version": "",
                    "internalVersion": "1",
                    "internalId": "28733d1d45f31150f877e0588eca2163",
                    "@type": "ServiceSpecification"
                },
                "place": {
                    "id": "5671dd2ec3a53010188473ce3640dd81",
                    "name": "3000 Main Street, Santa Clara, CA",
                    "@referredType": "GeographicSite"
                }
            }
        },
        {
            "id": "100",
            "qualificationResult": "none",
            "state": "new",
            "quantity": "1",
            "@type": "ServiceQualificationItem",
            "service": {
                "@type": "Service",
                "serviceCharacteristic": [{
                    "name": "Speed",
                    "valueType": "choice",
                    "value": ""
                }],
                "serviceSpecification": {
                    "id": "b3933d9d45f31150f877e0588eca21fc",
                    "name": "Access Service",
                    "version": "",
                    "internalVersion": "1",
                    "internalId": "b3933d9d45f31150f877e0588eca21fc",
                    "@type": "ServiceSpecification"
                },
                "place": {
                    "id": "5671dd2ec3a53010188473ce3640dd81",
                    "name": "3000 Main Street, Santa Clara, CA",
                    "@referredType": "GeographicSite"
                }
            }
        },
        {
            "id": "120",
            "qualificationResult": "none",
            "state": "new",
            "quantity": "1",
            "@type": "ServiceQualificationItem",
            "service": {
                "@type": "Service",
                "serviceCharacteristic": [{
                    "name": "DSL Speed",
                    "valueType": "choice",
                    "value": "500 Mbps"
                }],
                "serviceSpecification": {
                    "id": "1d43f91d45f31150f877e0588eca21cd",
                    "name": "CFS1",
                    "version": "",
                    "internalVersion": "1",
                    "internalId": "1d43f91d45f31150f877e0588eca21cd",
                    "@type": "ServiceSpecification"
                },
                "place": {
                    "id": "5671dd2ec3a53010188473ce3640dd81",
                    "name": "3000 Main Street, Santa Clara, CA",
                    "@referredType": "GeographicSite"
                }
            }
        }
    ],
    "expectedQualificationDate": "2022-10-11T15:20:39.000Z"
}
]
```

## Technical Service Qualification Open API - POST sn\_ord\_qual\_mgmt/qualification/checkServiceQualification

Creates a technical service qualification request entity containing a list of qualification items.

The service qualification request is persisted as a customer order with the qualify fulfillment type. Each qualification item is persisted as a customer line order in the Order \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

### Using this endpoint

You can use this API method for three specific use cases:

1.  Request to qualify a service at a specified address.
2.  Request to qualify a new service at the same location of an existing and active access service.
3.  Request to upgrade or downgrade an existing service.

Each use case requires the same request structure but uses different request parameters. Details about each use case and accepted parameters are provided:

-   To qualify a service at a specified address, use the **place** array \(**serviceQualificationItem.service.place\)** to provide a specific location and the service specification. You can optionally define additional service characteristics in your request.
-   To qualify a new service at the same location of an existing and active service, use the **referenceServiceInventory** object \(serviceQualificationItem.service.referenceServiceInventory\) instead of the **place** array. This object allows you to create a request and define service specifications without needing to provide location details. You can optionally define additional service characteristics in your request.
-   To upgrade or downgrade an existing service, use the **serviceInventory** object \(serviceQualificationItem.service.ServiceInventory\) instead of the **place** array or the **referenceServiceInventory** object. In this use case, location information and specification details are fetched from an existing service. In your request, define any service characteristics that you wish to change.

    For example, say that you want to verify that you can upgrade the download speed of an existing, active service from 100Mb/s to 600Mb/s. In this case, you can use the **serviceInventory** parameter to define the request by changing the 'Speed' characteristic from 'Low' to 'High'. The API obtains remaining characteristics from the existing service.


To understand how to form your API request per your particular use case, refer to the example calls provided in the **Example** section of this page.

### URL format

Default URL: `/api/sn_ord_qual_mgmt/qualification/checkServiceQualification`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

Optional. Part of TMF Open API standard. Annotation for the qualification. This value is always `CheckServiceQualification`. This information is not stored.Data type: String

</td></tr><tr><td>

checkServiceQualificationDate

</td><td>

Optional. The date and time the qualification request was created. Located in the order\_date field of the Customer Order \[sn\_ind\_tmt\_orm\_order\] table. If not specified, order\_date is set to the current date and time. Data type: String

Format: YYYY-MM-DDTHH:MM:SS.SSSZ

</td></tr><tr><td>

description

</td><td>

Optional. The description of the qualification request. Located in the ‘short\_description’ field of the Customer Order \[sn\_ind\_tmt\_orm\_order\] table.Data type: String

Maximum character length: 100

</td></tr><tr><td>

effectiveQualificationDate

</td><td>

Optional. The date that the qualification is effective. Persisted in ‘actual\_end\_date’ field of the customer order of the Customer Order \[sn\_ind\_tmt\_orm\_order\] table.Data type: String

Format: YYYY-MM-DDTHH:MM:SS.SSSZ

</td></tr><tr><td>

expectedQualificationDate

</td><td>

Optional. The expected qualification date. Persisted in expected\_end\_date’ field of the customer order. Located in the Customer Order \[sn\_ind\_tmt\_orm\_order\] table.Data type: String

Format: YYYY-MM-DDTHH:MM:SS.SSSZ

</td></tr><tr><td>

externalId

</td><td>

Optional. External ID assigned of the customer order. Persisted in the external\_id field of the customer order of the Customer Order \[sn\_ind\_tmt\_orm\_order\] table.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the qualification request. Each contact is an object in the array. Must list at least one item which contains customer account, customer contact, or consumer account information.Data type: Array of Objects

```
"relatedParty": [
  {
  "@referredType": "String",
  "@type": "String",
  "id": "String",
  "name": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of related party.Possible values:

-   consumer
-   customer
-   customerContact

Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Optional. Part of TMF Open API standard. Annotation for the order line item contact. This value is always `RelatedParty`. This information is not stored.Data type: String

</td></tr><tr><td>

relatedParty.id

</td><td>

The sys\_id or external\_id, if applicable, of the related party. Located in the Account \[customer\_account\] table, Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer.Data type: String

</td></tr><tr><td>

serviceQualificationItem

</td><td>

List of service qualification items with location, service information, and characteristics. Stored as order line items for the customer order. Must include at least one service qualification item in the list.Data type: Array of objects

```
"serviceQualificationItem": [{
  "@type": "String",
  "id": "String",
  "qualificationResult": "String",
  "quantity": "Number",
  "service": {Object},
  "state": "String"
]
```

</td></tr><tr><td>

serviceQualificationItem.@type

</td><td>

Optional. Part of TMF Open API standard. Annotation for qualification item. This value is always `ServiceQualificationItem`. This information is not stored.Data Type: String

</td></tr><tr><td>

serviceQualificationItem.qualificationItemRelationship

</td><td>

Optional. List of relationships with other service qualification items in the same request. This information helps to create order line items with a parent order line item.Data type: Array of objects

```
"qualificationItemRelationship": [
  {
  "id": "String"
  "relationshipType": "String"
   }
]
```

</td></tr><tr><td>

serviceQualificationItem.qualificationItemRelationship.id

</td><td>

Required. The ID of the target qualification item in the relationship.Data Type: String

</td></tr><tr><td>

serviceQualificationItem.qualificationItemRelationship.relationshipType

</td><td>

Required. The type of line item relationship.Valid values:

-   HasChild: indicates the child item.
-   HasParent:indicates the parent item.

Data Type: String

</td></tr><tr><td>

serviceQualificationItem.quantity

</td><td>

Optional. Quantity of the qualification item. Persisted in the ‘quantity’ field of customer order line item.Data type: Number

Default if not specified: 1

</td></tr><tr><td>

serviceQualificationItem.service

</td><td>

Required. Service information which can include such variables as place, service specification, and service characteristics.Data Type: Object

```
"service": {
  "@type": "String",
  "place": [Array],
  "serviceCharacteristic": [Array],
  "serviceSpecification": {Object}
}
```

</td></tr><tr><td>

serviceQualificationItem.service.@type

</td><td>

Optional. Part of TMF Open API standard. Annotation for Service information for qualification item. This value is always `Service`. This information is not stored.Data Type: String

</td></tr><tr><td>

serviceQualificationItem.service.place

</td><td>

Optional. The requested location information for the service qualification item. Located in the Location \[cmn\_location\] table.**Note:** Even though array is supported, it must contain only one location.

Data Type: Array of objects

```
"place": [
  {
  "@type": "String"
  "id": "String",
  "name": "String"
  }
]
```

</td></tr><tr><td>

serviceQualificationItem.service.place.@type

</td><td>

Optional. Part of TMF Open API standard. Annotation for Service. This value is always `GeographicSite`. This information is not stored.Data Type: String

</td></tr><tr><td>

serviceQualificationItem.service.place.id

</td><td>

Required. Sys\_id of a location in the Location \[cmn\_location\] table. This location ID should be a valid entry in the Location \[cmn\_location\] table. Data Type: String

</td></tr><tr><td>

serviceQualificationItem.service.place.name

</td><td>

Optional. Name of the location. This value is not verified against entries in the Location \[cmn\_location\] table.Data Type: String

</td></tr><tr><td>

serviceQualificationItem.service.referenceServiceInventory

</td><td>

Required. Valid service inventory entity which refers to an active service for the required location. The location information for the qualification order is obtained from this service inventory's location. **Important:** Use the **referenceServiceInventory** object to qualify a new service at the same location of an existing and active Access service. To do so, you must also omit the **place** array and **serviceInventory** object from your request, otherwise the API returns an error.

Data type: Object

```
"referenceServiceInventory": {
"id": "String"
}
```

</td></tr><tr><td>

serviceQualificationItem.service.referenceServiceInventory.id

</td><td>

Required if using **serviceQualificationItem.service.referenceServiceInventory** in the request. The sys\_id of a valid service inventory entity which refers to an active service for the required location. This information is mentioned only in the order work notes.Data type: String

</td></tr><tr><td>

serviceQualificationItem.service.serviceCharacteristic

</td><td>

Optional. Array of service characteristics.Data Type: Array of objects

```
"serviceCharacteristic": [
  {
  "name": "String",
  "value": "String",
  "valueType": "String",
  }
]
```

</td></tr><tr><td>

serviceQualificationItem.service.serviceCharacteristic.name

</td><td>

Required. Name of the characteristic.Data Type: String

</td></tr><tr><td>

serviceQualificationItem.service.serviceCharacteristic.value

</td><td>

Optional. Value of the characteristic. Part of TMF Open API standard. Annotation for Qualification item. This value is always `ServiceQualificationItem`. This information is not stored.Data Type: String

</td></tr><tr><td>

serviceQualificationItem.service.serviceCharacteristic.valueType

</td><td>

Optional. Value type of the characteristic. Data Type: String

</td></tr><tr><td>

serviceQualificationItem.service.serviceInventory

</td><td>

Optional. Valid service inventory entity which refers to an active service needing an upgrade or downgrade. **Important:** Use the **serviceInventory** object for service upgrades or downgrades. To do so, you must omit the place **array** and **referenceServiceInventory** object from your request, otherwise the API returns an error.

Data type: Object

```
"serviceInventory": {
  "id": "String"
}
```

</td></tr><tr><td>

serviceQualificationItem.service.serviceSpecification

</td><td>

Required. Service specification for the qualification item. Stored in the service\_specification field of the customer order line item in the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Service specifications for a qualification item can't be resource-facing.Data Type: Object

```
"serviceSpecification": {
  “@type”: ”String”,
  "id": "String",
  "name": "String"
}

```

</td></tr><tr><td>

serviceQualificationItem.service.serviceSpecification.@type

</td><td>

Optional. Part of TMF Open API standard. Annotation for the service specification. This value is always `ServiceSpecification`. This information is not stored.Data Type: String

</td></tr><tr><td>

serviceQualificationItem.service.serviceSpecification.id

</td><td>

Required. External ID or initial version of the service specification.Data Type: String

</td></tr><tr><td>

serviceQualificationItem.service.serviceSpecification.internalVersion

</td><td>

Optional. Internal version of the service specification.Data Type: Number

</td></tr><tr><td>

serviceQualificationItem.service.serviceSpecification.name

</td><td>

Required. Name of the service specification.Data Type: String

</td></tr><tr><td>

serviceQualificationItem.service.serviceSpecification.version

</td><td>

Optional. External version of the service specification.Data Type: String

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

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_fbw_k3z_gsb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

201

</td><td>

Request successfully processed.**Note:** If there are any issues with the characteristics or characteristics option information, the endpoint stores the following comments in the work notes fields of the associated Customer Order Line Item record similar to existing delivery orders

</td></tr><tr><td>

400

</td><td>

Bad Request. Could be any of the following reasons: -   Empty payload.
-   Invalid payload: Mandatory field missing: &lt;field name&gt;
-   Invalid payload: Request body missing - Payload was not passed in the request body.
-   Invalid payload: relatedParty is missing.
-   Invalid payload: serviceQualificationItem is missing.
-   Invalid payload: serviceQualificationItem id is missing.
-   Invalid payload: serviceQualificationItem service is missing.
-   Invalid payload: The location information is missing. Please provide place, serviceInventory or referenceServiceInventory.
-   Invalid payload: The specification information is missing, please provide serviceSpecification or serviceInventory.
-   Invalid payload: Service Specification does not exist.
-   Invalid payload: Customer Account does not exist.
-   Invalid payload: Consumer does not exist.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_mc1_pr1_tx"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the qualification customer order.Data type: String

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr><td>

href

</td><td>

Relative link to the qualification order record. Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the qualification request which is fetched from the short\_description field of the customer order.Data type: String

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr><td>

externalId

</td><td>

External ID of the customer order. Data type: String

Table: in the external\_id field of the Customer Order \[sn\_ind\_tmt\_orm\_order\] table.

</td></tr><tr><td>

qualificationResult

</td><td>

Qualification status of the result field of the customer order. Possible values:

-   alternate
-   none
-   pending
-   qualified
-   unqualified

Data type: String

</td></tr><tr><td>

state

</td><td>

State of customer order from the status field of customer order.Data type: String

</td></tr><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the qualification. This value is always `CheckServiceQualification`. This information is not stored.Data type: String

</td></tr><tr><td>

checkServiceQualificationDate

</td><td>

Date and time the qualification request that was created from the order\_date field of the customer order.Data type: String

Format: YYYY-MM-DDTHH:MM:SS.SSSZ

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr><td>

effectiveQualificationDate

</td><td>

Effective qualification date fetched from the order\_date field of the customer order.Data type: String

Format: YYYY-MM-DDTHH:MM:SS.SSSZ

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr><td>

expectedQualificationDate

</td><td>

Stores the expected qualification date. Persisted in expected\_end\_date field of the customer order.Data type: String

Format: YYYY-MM-DDTHH:MM:SS.SSSZ

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the qualification request. Each contact is an object in the array.Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order.Data type: String

Table: Account \[customer\_account\] table, Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\]

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer.Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for the order line item contact. This value is always `RelatedParty`. This information is not stored.Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of related party.Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr><td>

serviceQualificationItem

</td><td>

List of service qualification items containing information about location, service information, and service characteristics. Stored as order line items for the customer order. Data type: Array of Objects

```
"serviceQualificationItem": [
  {
    "id": "String",
    "action": "String",
    "expectedServiceAvailabilityDate": "Number",
    "service": {Object},
    "@type": "String"
  }
]
```

</td></tr><tr><td>

serviceQualificationItem.id

</td><td>

ID of the qualification item.Data type: String

Stored in: The external\_id field of customer order line item in the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

serviceQualificationItem.qualificationResult

</td><td>

Result of qualification item. Stored in the ‘result’ field of customer order line item. Possible values:

-   alternate
-   none
-   pending
-   qualified
-   unqualified

Data type: String

Table: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

serviceQualificationItem.state

</td><td>

State of qualification item derived from the ‘status’ field of customer order line item. Data type: String

Table: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

serviceQualificationItem.quantity

</td><td>

Quantity of qualification item derived from the ‘quantity’ field of customer order line item.Data type: Number

Table:Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

serviceQualificationItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the qualification item. This value is always ServiceQualificationItem. This information is not stored.Data type: String

</td></tr><tr><td>

serviceQualificationItem.service

</td><td>

Service information which includes details about location \(place\), service specifications, and service characteristics.Data type: Object

```
"service": {
  "@type": "String",
  "place": [Array],
  "serviceCharacteristic": [Array],
  "serviceSpecification": {Object}
}
```

</td></tr><tr><td>

serviceQualificationItem.service.@type

</td><td>

Part of TMF Open API standard. Annotation for the service. This value is always `Service`. This information is not stored. Data type: String

</td></tr><tr><td>

serviceQualificationItem.service.place

</td><td>

Location information for the service qualification item.Data type: Array of Objects

**Note:** This array can contain only one location.

```
"place": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String"
  }
]
```

</td></tr><tr><td>

serviceQualificationItem.service.place.id

</td><td>

Sys\_id of the location.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

serviceQualificationItem.service.place.name

</td><td>

Name of the location. Not verified against an entry in the Location \[cmn\_location\] table.Data type: String

</td></tr><tr><td>

serviceQualificationItem.service.place.@type

</td><td>

Part of TMF Open API standard. Annotation for Service. This value is always `GeographicSite`. This information is not stored.Data type: String

</td></tr><tr><td>

serviceQualificationItem.service.serviceSpecification

</td><td>

Service specification details for the qualification item.Data type: Array of Objects

```
"serviceSpecification": {
  "id": "String",
  "internalVersion": "Number",
  "internalId": "String",
  "name": "String"
  "@type": "ServiceSpecification"
  "version": "String",
}

```

</td></tr><tr><td>

serviceQualificationItem.service.serviceSpecification.id

</td><td>

External ID or initial version of the service specification.Data type: String

</td></tr><tr><td>

serviceQualificationItem.service.serviceSpecification.name

</td><td>

Name of the service specification.Data type: String

</td></tr><tr><td>

serviceQualificationItem.service.serviceSpecification.version

</td><td>

External version of the service specification.Data type: String

</td></tr><tr><td>

serviceQualificationItem.service.serviceSpecification.internalVersion

</td><td>

Internal version of the service specification.Data type: Number

</td></tr><tr><td>

serviceQualificationItem.service.serviceSpecification.internalId

</td><td>

Initial version of the service specification.Data type: String

</td></tr><tr><td>

serviceQualificationItem.service.serviceSpecification.@type

</td><td>

Part of TMF Open API standard. Annotation for Service Specification. This value is always `ServiceSpecification`. This information is not stored.Data type: String

</td></tr><tr><td>

serviceQualificationItem.service.serviceCharacteristic

</td><td>

List of service characteristics.Data type: Array of objects

```
"serviceCharacteristic": [
  {
    "name": "String",
    "value": "String",
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

serviceQualificationItem.service.serviceCharacteristic.valueType

</td><td>

Value type of the characteristic.Data type: String

</td></tr><tr><td>

serviceQualificationItem.service.serviceCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

serviceQualificationItem.service.serviceCharacteristic.value

</td><td>

Value of the characteristic.Data type: String

</td></tr></tbody>
</table>### Use Case 1

The following example shows a simple request containing a single qualification item.

```
curl -X POST "https://instance.service-now.com/api/sn_ord_qual_mgmt/qualification/checkServiceQualification " \ 
-H "Accept: application/json" \ 
-H "Content-Type: application/json" \ 
-u "username":"password" \ 
-d {
  "description": "check service qualification illustration",
  "checkServiceQualificationDate": "2022-12-14T23:44:44.000Z",
  "effectiveQualificationDate": "2023-12-14T23:44:44.000Z",
  "expectedQualificationDate": "2023-10-11T15:20:39.000Z",
  "externalId": "CSQ1",
  "relatedParty": [
    {
      "id": "eaf68911c35420105252716b7d40ddde",
      "name": "Sally Thomas",
      "@type": "RelatedParty",
      "@referredType": "CustomerContact"
    },
    {
      "id": "ffc68911c35420105252716b7d40dd55",
      "name": "Funco Intl",
      "@type": "RelatedParty",
      "@referredType": "Customer"
    },
    {
      "id": "59f16de1c3b67110ff00ed23a140dd9e",
      "name": "Funco External",
      "@type": "RelatedParty",
      "@referredType": "Consumer"
    }
  ],
  "serviceQualificationItem": [
    {
      "id": "100",
      "service": {
        "@type": "Service",
        "place": [
          {
            "id": "5671dd2ec3a53010188473ce3640dd81",
            "name": "Jean Pontus home",
            "@type": "GeographicSite"
          }
        ],
        "serviceCharacteristic": [
          {
            "valueType": "choice",
            "name": "Speed",
            "value": "High"
          }
        ],
        "serviceSpecification": {
          "id": "91478553b7969910ff00f203ae11a97d",
          "name": "Broadband Service",
          "@type": "ServiceSpecification"
        }
      },
      "@type": "ServiceQualificationItem"
    }
  ],
  "@type": "CheckServiceQualification"
}
```

Response:

```
{
  "id": "0b45c47938bf1110f877c8d44c4b895d",
  "href": "/api/sn_ord_qual_mgmt/qualification/checkServiceQualification/0b45c47938bf1110f877c8d44c4b895d",
  "description": "check service qualification illustration",
  "externalId": "CSQ1",
  "qualificationResult": "none",
  "state": "new",
  "@type": "CheckServiceQualification",
  "checkServiceQualificationDate": "2022-12-14T23:44:44.000Z",
  "relatedParty": [
    {
      "id": "eaf68911c35420105252716b7d40ddde",
      "name": "Sally Thomas",
      "@type": "RelatedParty",
      "@referredType": "CustomerContact"
    },
    {
      "id": "ffc68911c35420105252716b7d40dd55",
      "name": "Funco Intl",
      "@type": "RelatedParty",
      "@referredType": "Customer"
    },
    {
      "id": "59f16de1c3b67110ff00ed23a140dd9e",
      "name": "Funco External",
      "@type": "RelatedParty",
      "@referredType": "Consumer"
    }
  ],
  "serviceQualificationItem": [
    {
      "id": "100",
      "qualificationResult": "none",
      "state": "new",
      "quantity": "1",
      "@type": "ServiceQualificationItem",
      "service": {
        "@type": "Service",
        "serviceCharacteristic": [
          {
            "name": "Speed",
            "valueType": "choice",
            "value": "High"
          }
        ],
        "serviceSpecification": {
          "id": "91478553b7969910ff00f203ae11a97d",
          "name": "Broadband Service",
          "version": "",
          "internalVersion": "1",
          "internalId": "91478553b7969910ff00f203ae11a97d",
          "@type": "ServiceSpecification"
        },
        "place": {
          "id": "5671dd2ec3a53010188473ce3640dd81",
          "name": "3000 Main Street, Santa Clara, CA",
          "@referredType": "GeographicSite"
        }
      }
    }
  ],
  "effectiveQualificationDate": "2023-12-14T23:44:44.000Z",
  "expectedQualificationDate": "2023-10-11T15:20:39.000Z"
}
```

### Use Case 2

The following example demonstrates how to request a simple service qualification using an ID to obtain the customer's location with an existing service.

**Note:** Reference Service Inventory with id = is a product inventory with location = 20220 Bow Willow, Houston,TX

```
curl -X POST "https://instance.service-now.com/api/sn_ord_qual_mgmt/qualification/checkServiceQualification " \ 
-H "Accept: application/json" \ 
-H "Content-Type: application/json" \ 
-u "username":"password" \ 
-d {
  "description": "check service qualification illustration",
  "checkServiceQualificationDate": "2022-12-14T23:44:44.000Z",
  "effectiveQualificationDate": "2023-12-14T23:44:44.000Z",
  "expectedQualificationDate": "2023-10-11T15:20:39.000Z",
  "externalId": "CSQ1",
  "relatedParty": [
    {
      "id": "eaf68911c35420105252716b7d40ddde",
      "name": "Sally Thomas",
      "@type": "RelatedParty",
      "@referredType": "CustomerContact"
    },
    {
      "id": "ffc68911c35420105252716b7d40dd55",
      "name": "Funco Intl",
      "@type": "RelatedParty",
      "@referredType": "Customer"
    },
    {
      "id": "59f16de1c3b67110ff00ed23a140dd9e",
      "name": "Funco External",
      "@type": "RelatedParty",
      "@referredType": "Consumer"
    }
  ],
  "serviceQualificationItem": [
    {
      "id": "100",
      "service": {
        "@type": "Service",
        "referenceServiceInventory": {
          "id": "f1b2d99e777301108e191e599a5a99d2"
        },
        "serviceCharacteristic": [
          {
            "valueType": "choice",
            "name": "Speed",
            "value": "High"
          }
        ],
        "serviceSpecification": {
          "id": "91478553b7969910ff00f203ae11a97d",
          "name": "Broadband Service",
          "@type": "ServiceSpecification"
        }
      },
      "@type": "ServiceQualificationItem"
    }
  ],
  "@type": "CheckServiceQualification"
}
```

Response, where **place** is populated from **referenceServiceInventory** in the request.

```
{
    "id": "1683497138b35110f877c8d44c4b890a",
   "href":"/api/sn_ord_qual_mgmt/qualification/checkServiceQualification/1683497138b35110f877c8d44c4b890a",
    "description": "check service qualification illustration",
    "externalId": "CSQ1",
    "qualificationResult": "none",
    "state": "new",
    "@type": "CheckServiceQualification",
    "checkServiceQualificationDate": "2022-12-14T23:44:44.000Z",
    "relatedParty": [
        {
            "id": "eaf68911c35420105252716b7d40ddde",
            "name": "Sally Thomas",
            "@type": "RelatedParty",
            "@referredType": "CustomerContact"
        },
        {
            "id": "ffc68911c35420105252716b7d40dd55",
            "name": "Funco Intl",
            "@type": "RelatedParty",
            "@referredType": "Customer"
        },
        {
            "id": "59f16de1c3b67110ff00ed23a140dd9e",
            "name": "Funco External",
            "@type": "RelatedParty",
            "@referredType": "Consumer"
        }
    ],
    "serviceQualificationItem": [
        {
            "id": "100",
            "qualificationResult": "none",
            "state": "new",
            "quantity": "1",
            "@type": "ServiceQualificationItem",
            "service": {
                "@type": "Service",
                "serviceCharacteristic": [
                    {
                        "name": "Speed",
                        "valueType": "choice",
                        "value": "High"
                    }
                ],
                "serviceSpecification": {
                    "id": "91478553b7969910ff00f203ae11a97d",
                    "name": "Broadband Service",
                    "version": "",
                    "internalVersion": "1",
                    "internalId": "91478553b7969910ff00f203ae11a97d",
                    "@type": "ServiceSpecification"
                },
                "place": {
                    "id": "25aba4010a0a0bb3008f329002f12211",
                    "name": "20220 Bow Willow, Houston,TX",
                    "@referredType": "GeographicSite"
                }
            }
        }
    ],
    "effectiveQualificationDate": "2022-12-14T23:44:44.000Z",
    "expectedQualificationDate": "2023-10-11T15:20:39.000Z"
}
```

### Use Case 3

The following example demonstrates how to upgrade a user's broadband service to a higher speed. Service Inventory with id = is a product inventory with Service Specification = ‘Broadband Service’, Location = 20220 Bow Willow, Houston, TX, Characteristics=\[\{Speed:Medium\}\].

```
{
  "description": "check service qualification illustration",
  "checkServiceQualificationDate": "2022-12-14T23:44:44.000Z",
  "effectiveQualificationDate": "2023-12-14T23:44:44.000Z",
  "expectedQualificationDate": "2023-10-11T15:20:39.000Z",
  "externalId": "CSQ1",
  "relatedParty": [
    {
      "id": "eaf68911c35420105252716b7d40ddde",
      "name": "Sally Thomas",
      "@type": "RelatedParty",
      "@referredType": "CustomerContact"
    },
    {
      "id": "ffc68911c35420105252716b7d40dd55",
      "name": "Funco Intl",
      "@type": "RelatedParty",
      "@referredType": "Customer"
    },
    {
      "id": "59f16de1c3b67110ff00ed23a140dd9e",
      "name": "Funco External",
      "@type": "RelatedParty",
      "@referredType": "Consumer"
    }
  ],
  "serviceQualificationItem": [
    {
      "id": "100",
      "service": {
        "@type": "Service",
        "serviceInventory": {
          "id": "f1b2d99e777301108e191e599a5a99d2"
        },
        "serviceCharacteristic": [
          {
            "valueType": "choice",
            "name": "Speed",
            "value": "High"
          }
        ]
      },
      "@type": "ServiceQualificationItem"
    }
  ],
  "@type": "CheckServiceQualification"
}
```

Response, where **place** and **specification** are populated from **serviceInventory** in the request.

**Note:** Characteristics are taken from the request payload first, then remaining characteristics \(if any\) are obtained from **serviceInventory**.

```
{
    "id": " db8485b138b35110f877c8d44c4b892b",
    "href": "/api/sn_ord_qual_mgmt/qualification/checkServiceQualification/ db8485b138b35110f877c8d44c4b892b",
    "description": "check service qualification illustration",
    "externalId": "CSQ1",
    "qualificationResult": "none",
    "state": "new",
    "@type": "CheckServiceQualification",
    "checkServiceQualificationDate": "2022-12-14T23:44:44.000Z",
    "relatedParty": [
        {
            "id": "eaf68911c35420105252716b7d40ddde",
            "name": "Sally Thomas",
            "@type": "RelatedParty",
            "@referredType": "CustomerContact"
        },
        {
            "id": "ffc68911c35420105252716b7d40dd55",
            "name": "Funco Intl",
            "@type": "RelatedParty",
            "@referredType": "Customer"
        },
        {
            "id": "59f16de1c3b67110ff00ed23a140dd9e",
            "name": "Funco External",
            "@type": "RelatedParty",
            "@referredType": "Consumer"
        }
    ],
    "serviceQualificationItem": [
        {
            "id": "100",
            "qualificationResult": "none",
            "state": "new",
            "quantity": "1",
            "@type": "ServiceQualificationItem",
            "service": {
                "@type": "Service",
                "serviceCharacteristic": [
                    {
                        "name": "Speed",
                        "valueType": "choice",
                        "value": "High"
                    }
                ],
                "serviceSpecification": {
                    "id": "91478553b7969910ff00f203ae11a97d",
                    "name": "Broadband Service",
                    "version": "",
                    "internalVersion": "1",
                    "internalId": "91478553b7969910ff00f203ae11a97d",
                    "@type": "ServiceSpecification"
                },
                "place": {
                    "id": "25aba4010a0a0bb3008f329002f12211",
                    "name": "20220 Bow Willow, Houston,TX",
                    "@referredType": "GeographicSite"
                }
            }
        }
    ],
    "effectiveQualificationDate": "2022-12-14T23:44:44.000Z",
    "expectedQualificationDate": "2023-10-11T15:20:39.000Z"
}
```

### Use Case 4

Describes the hierarchy of parent and child line items and their relationship types. It demonstrates how multiple line items can be created via the quantity attribute.

```
curl -X POST "https://instance.service-now.com/api/sn_ord_qual_mgmt/qualification/checkServiceQualification " \ 
-H "Accept: application/json" \ 
-H "Content-Type: application/json" \ 
-u "username":"password" \ 
-d {
  "description": "check service qualification illustration",
  "checkServiceQualificationDate": "2022-12-14T23:44:44.000Z",
  "effectiveQualificationDate": "2023-12-14T23:44:44.000Z",
  "expectedQualificationDate": "2023-10-11T15:20:39.000Z",
  "externalId": "CSQ1",
  "relatedParty": [
    {
      "id": "eaf68911c35420105252716b7d40ddde",
      "name": "Sally Thomas",
      "@type": "RelatedParty",
      "@referredType": "CustomerContact"
    },
    {
      "id": "ffc68911c35420105252716b7d40dd55",
      "name": "Funco Intl",
      "@type": "RelatedParty",
      "@referredType": "Customer"
    },
    {
      "id": "59f16de1c3b67110ff00ed23a140dd9e",
      "name": "Funco External",
      "@type": "RelatedParty",
      "@referredType": "Consumer"
    }
  ],
  "serviceQualificationItem": [
    {
      "id": "100",
      "quantity": 2,
      "qualificationItemRelationship": [
        {
          "relationshipType": "HasChild",
          "id": "110"
        },
        {
          "relationshipType": "HasChild",
          "id": "120"
        },
        {
          "relationshipType": "HasChild",
          "id": "130"
        }
      ],
      "service": {
        "@type": "Service",
        "place": [
          {
            "id": "5671dd2ec3a53010188473ce3640dd81",
            "name": "Jean Pontus home",
            "@referredType": "GeographicSite"
          }
        ],
        "serviceCharacteristic": [
          {
            "valueType": "string",
            "name": "Speed",
            "value": "High"
          }
        ],
        "serviceSpecification": {
          "id": "b3933d9d45f31150f877e0588eca21fc",
          "name": "Access Service"
        }
      },
      "@type": "ServiceQualificationItem"
    },
    {
      "id": "110",
      "action": "add",
      "expectedServiceAvailabilityDate": "2022-12-10T19:20:39.239Z",
      "qualificationItemRelationship": [
        {
          "relationshipType": "HasParent",
          "id": "100"
        }
      ],
      "service": {
        "@type": "Service",
        "place": [
          {
            "id": "5671dd2ec3a53010188473ce3640dd81",
            "name": "Jean Pontus home",
            "@referredType": "GeographicSite"
          }
        ],
        "serviceCharacteristic": [
          {
            "valueType": "choice",
            "name": "Fiber Speed",
            "value": "1Gbps"
          }
        ],
        "serviceSpecification": {
          "name": "CFS3",
          "internalVersion": "1",
          "id": "4d2b5799457b1150f877e0588eca2116"
        },
        "state": "new"
      },
      "@type": "ServiceQualificationItem"
    },
    {
      "id": "120",
      "action": "add",
      "qualificationItemRelationship": [
        {
          "relationshipType": "HasParent",
          "id": "100"
        }
      ],
      "expectedServiceAvailabilityDate": "2022-11-12T19:20:39.239Z",
      "service": {
        "@type": "Service",
        "place": [
          {
            "id": "5671dd2ec3a53010188473ce3640dd81",
            "name": "Jean Pontus home",
            "@referredType": "GeographicSite"
          }
        ],
        "serviceCharacteristic": [
          {
            "valueType": "choice",
            "name": "DSL Speed",
            "value": "500 Mbps"
          }
        ],
        "serviceSpecification": {
          "name": "CF1",
          "internalVersion": "1",
          "id": "1d43f91d45f31150f877e0588eca21cd"
        },
        "state": "new"
      },
      "@type": "ServiceQualificationItem"
    },
    {
      "id": "130",
      "action": "add",
      "expectedServiceAvailabilityDate": "2020-04-11T19:20:39.239Z",
      "qualificationItemRelationship": [
        {
          "relationshipType": "HasParent",
          "id": "100"
        }
      ],
      "service": {
        "@type": "Service",
        "place": [
          {
            "id": "5671dd2ec3a53010188473ce3640dd81",
            "name": "Jean Pontus home",
            "@referredType": "GeographicSite"
          }
        ],
        "serviceCharacteristic": [
          {
            "valueType": "choice",
            "name": "Wireless Speed",
            "value": "100 Mbps"
          }
        ],
        "serviceSpecification": {
          "name": "CFS2",
          "internalVersion": "1",
          "id": "28733d1d45f31150f877e0588eca2163"
        },
        "state": "new"
      },
      "@type": "ServiceQualificationItem"
    }
  ],
  "@type": "CheckServiceQualification"
}
```

Response:

```
{
  "id": "7bf9cd7538b35110f877c8d44c4b89e4",
  "href": "/api/sn_ord_qual_mgmt/qualification/checkServiceQualification/7bf9cd7538b35110f877c8d44c4b89e4",
  "description": "check service qualification illustration",
  "externalId": "CSQ1",
  "qualificationResult": "none",
  "state": "new",
  "@type": "CheckServiceQualification",
  "checkServiceQualificationDate": "2022-12-14T23:44:44.000Z",
  "relatedParty": [
    {
      "id": "eaf68911c35420105252716b7d40ddde",
      "name": "Sally Thomas",
      "@type": "RelatedParty",
      "@referredType": "CustomerContact"
    },
    {
      "id": "ffc68911c35420105252716b7d40dd55",
      "name": "Funco Intl",
      "@type": "RelatedParty",
      "@referredType": "Customer"
    },
    {
      "id": "59f16de1c3b67110ff00ed23a140dd9e",
      "name": "Funco External",
      "@type": "RelatedParty",
      "@referredType": "Consumer"
    }
  ],
  "serviceQualificationItem": [
    {
      "id": "120",
      "qualificationResult": "none",
      "state": "new",
      "quantity": "1",
      "@type": "ServiceQualificationItem",
      "service": {
        "@type": "Service",
        "serviceCharacteristic": [
          {
            "name": "DSL Speed",
            "valueType": "choice",
            "value": "500 Mbps"
          }
        ],
        "serviceSpecification": {
          "id": "1d43f91d45f31150f877e0588eca21cd",
          "name": "CFS1",
          "version": "",
          "internalVersion": "1",
          "internalId": "1d43f91d45f31150f877e0588eca21cd",
          "@type": "ServiceSpecification"
        },
        "place": {
          "id": "5671dd2ec3a53010188473ce3640dd81",
          "name": "3000 Main Street, Santa Clara, CA",
          "@referredType": "GeographicSite"
        }
      }
    },
    {
      "id": "110",
      "qualificationResult": "none",
      "state": "new",
      "quantity": "1",
      "@type": "ServiceQualificationItem",
      "service": {
        "@type": "Service",
        "serviceCharacteristic": [
          {
            "name": "Fiber Speed",
            "valueType": "choice",
            "value": "1Gbps"
          }
        ],
        "serviceSpecification": {
          "id": "4d2b5799457b1150f877e0588eca2116",
          "name": "CFS3",
          "version": "",
          "internalVersion": "1",
          "internalId": "4d2b5799457b1150f877e0588eca2116",
          "@type": "ServiceSpecification"
        },
        "place": {
          "id": "5671dd2ec3a53010188473ce3640dd81",
          "name": "3000 Main Street, Santa Clara, CA",
          "@referredType": "GeographicSite"
        }
      }
    },
    {
      "id": "130",
      "qualificationResult": "none",
      "state": "new",
      "quantity": "1",
      "@type": "ServiceQualificationItem",
      "service": {
        "@type": "Service",
        "serviceCharacteristic": [
          {
            "name": "Wireless Speed",
            "valueType": "choice",
            "value": "100 Mbps"
          }
        ],
        "serviceSpecification": {
          "id": "28733d1d45f31150f877e0588eca2163",
          "name": "CFS2",
          "version": "",
          "internalVersion": "1",
          "internalId": "28733d1d45f31150f877e0588eca2163",
          "@type": "ServiceSpecification"
        },
        "place": {
          "id": "5671dd2ec3a53010188473ce3640dd81",
          "name": "3000 Main Street, Santa Clara, CA",
          "@referredType": "GeographicSite"
        }
      }
    },
    {
      "id": "100",
      "qualificationResult": "none",
      "state": "new",
      "quantity": "2",
      "@type": "ServiceQualificationItem",
      "service": {
        "@type": "Service",
        "serviceCharacteristic": [
          {
            "name": "Speed",
            "valueType": "choice",
            "value": "High"
          }
        ],
        "serviceSpecification": {
          "id": "b3933d9d45f31150f877e0588eca21fc",
          "name": "Access Service",
          "version": "",
          "internalVersion": "1",
          "internalId": "b3933d9d45f31150f877e0588eca21fc",
          "@type": "ServiceSpecification"
        },
        "place": {
          "id": "5671dd2ec3a53010188473ce3640dd81",
          "name": "3000 Main Street, Santa Clara, CA",
          "@referredType": "GeographicSite"
        }
      }
    }
  ],
  "effectiveQualificationDate": "2023-12-14T23:44:44.000Z",
  "expectedQualificationDate": "2023-10-11T15:20:39.000Z"
}
```

## Technical Service Qualification Open API - POST sn\_ord\_qual\_mgmt/qualification/checkServiceQualification/processResult

Processes a technical service qualification result sent to the Technical Service Qualification Open API.

### URL format

Default URL: `/api/sn_ord_qual_mgmt/qualification/checkServiceQualification/processResult`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

serviceQualificationItem

</td><td>

Required. List of Service Qualification Items each representing a domain order in the Service Order table \[sn\_ind\_tmt\_orm\_service\_order\] for the requested top order line item. All domain orders represented by each of the service qualification items must belong to the same top order line item.Data type: Array of Objects

```
"serviceQualificationItem": [
{
  "@type": "String",
  "alternateServiceProposal": [Array],
  "id": "String",
  "qualificationResult": "String"
}
]
```

</td></tr><tr><td>

serviceQualificationItem.@type

</td><td>

Optional. Part of TMF Open API standard. Annotation for qualification item. This value is always `ServiceQualificationItem`. This information is not stored.Data Type: String

</td></tr><tr><td>

serviceQualificationItem.alternateProposal

</td><td>

Alternate Proposals provided for the qualification item.Data type: Array of Objects

```
"alternateServiceProposal": [
  {
  "@type": "String",
  "alternateService": {Object},
  "alternateServiceAvailabilityDate": "Number",
  "id": "String",
  "serviceCharacteristic": [Array]
  }
]
```

Stored in: Alternate Proposal \[sn\_ord\_qual\_mgmt\_alternate\_proposal\]

</td></tr><tr><td>

serviceQualificationItem.alternateProposal.@type

</td><td>

Part of TMF Open API standard. Annotation for Service information for the qualification item. This value is always `Service`. This information is not stored.Data type: String

</td></tr><tr><td>

serviceQualificationItem.alternateProposal.alternateService

</td><td>

Required. Service information for the alternate proposal containing service specifications and characteristics.Data type: Object

```
"alternateService": {
  "@type": "String",
  "serviceSpecification": {Object},
  "serviceCharacteristic": [Array]
}
```

</td></tr><tr><td>

serviceQualificationItem.alternateProposal.alternateService.alternateService.serviceCharacteristic.valueType

</td><td>

Value type of the characteristic under the alternate service proposal. Data type: String

</td></tr><tr><td>

serviceQualificationItem.alternateProposal.alternateService.serviceCharacteristic

</td><td>

Service characteristics for the alternate service proposal.Data type: Array of Objects

```
"serviceCharacteristic": [
  {
    "name": "String",
    "value": "String",
    "valueType": "String"
  }
]
```

Stored in: The order\_characteristics field of the Alternate proposal \[sn\_ord\_qual\_mgmt\_alternate\_proposal\] table.

</td></tr><tr><td>

serviceQualificationItem.alternateProposal.alternateService.serviceCharacteristic.name

</td><td>

Required. Name of the characteristic belonging to the alternate service proposal. Data type: String

</td></tr><tr><td>

serviceQualificationItem.alternateProposal.alternateService.serviceCharacteristic.value

</td><td>

Value of the characteristic belonging to the alternate service proposal.Data type: String

</td></tr><tr><td>

serviceQualificationItem.alternateProposal.alternateService.serviceCharacteristic.valueType

</td><td>

Type of characteristic.Data type: String

</td></tr><tr><td>

serviceQualificationItem.alternateProposal.alternateService .serviceSpecification

</td><td>

Required. Service Specification for the alternate proposal.Data type: Object

```
"serviceSpecification": {
  “@type”: ”String”
  "id": "String",
  "name": "String"
}
```

Stored in: The specification field of the alternate proposal entry of the Alternate proposal \[sn\_ord\_qual\_mgmt\_alternate\_proposal\] table.

</td></tr><tr><td>

serviceQualificationItem.alternateProposal.alternateService .serviceSpecification.@type

</td><td>

Part of TMF Open API standard. Annotation for the Service Specification. This value is always `ServiceSpecification`. This information is not stored.Data type: String

</td></tr><tr><td>

serviceQualificationItem.alternateProposal.alternateService.serviceSpecification.id

</td><td>

Required. External ID or initial version of the service specification.Data type: String

</td></tr><tr><td>

serviceQualificationItem.alternateProposal.alternateService.serviceSpecification.internalVersion

</td><td>

Internal version of the service specification.Data type: String

</td></tr><tr><td>

serviceQualificationItem.alternateProposal.alternateService.serviceSpecification.name

</td><td>

Name of the service specification.Data type: String

</td></tr><tr><td>

serviceQualificationItem.alternateProposal.alternateService.serviceSpecification.version

</td><td>

External version of the service specification.Data type: String

</td></tr><tr><td>

serviceQualificationItem.alternateProposal.alternateServiceAvailabilityDate

</td><td>

Alternate service availability date. Data type: String

Format: YYYY-MM-DDTHH:MM:SS.SSSZ

Table: In the available\_date field of the Alternate Proposal \[sn\_ord\_qual\_mgmt\_alternate\_proposal\] table, where the domain order information belongs to the domain order represented by the current service qualification item.

</td></tr><tr><td>

serviceQualificationItem.alternateProposal.id

</td><td>

User-defined ID for the alternate proposal. This data is not persisted.Data type: String

</td></tr><tr><td>

serviceQualificationItem.eligibilityUnavailabilityReason

</td><td>

Reason for why the service qualification is not eligible.Data type: Object

```
"eligibilityUnavailabilityReason": [
  {
    "code": "String",
    "label": "String"
  }
]
```

Stored in: The entire list of reasons is persisted with their label fields as a string in the unavailability\_reason field of the Domain Order \[sn\_ind\_tmt\_orm\_domain\_order\] table.

</td></tr><tr><td>

serviceQualificationItem.eligibilityUnavailabilityReason.code

</td><td>

Code for the eligibility unavailability reason. This information is not persisted.Data type: String

</td></tr><tr><td>

serviceQualificationItem.eligibilityUnavailabilityReason.label

</td><td>

Required. Label for the eligibility unavailability reason. If there are multiple ineligibility reasons, the labels are separated by a comma.Data type: String

Stored in: The unavailability\_reason field of the Domain Order \[sn\_ind\_tmt\_orm\_domain\_order\] table.

</td></tr><tr><td>

serviceQualificationItem.id

</td><td>

Required. Sys\_id of the domain order represented by the qualification item.

 Data type: String

 Stored in: Sys\_id field of the Domain Order \[sn\_ind\_tmt\_orm\_service\_order\] table.

</td></tr><tr><td>

serviceQualificationItem.qualificationResult

</td><td>

Required. Qualification Result for each service qualification item. Data type: String

Stored in: The result field of the Domain Order table \[sn\_ind\_tmt\_orm\_service\_order\].

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

<table id="table_wwn_rhd_ct"><thead><tr><th>

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

Bad Request. Could be any of the following reasons: -   Invalid payload: Qualification Result should be one of \[alternate, pending, qualified, unqualified\].
-   Invalid payload: Qualification Item id does not exist.
-   All Qualification Items must belong to same Top Order Line Item.
-   Invalid payload: serviceQualificationItem qualificationResult is missing.
-   Invalid payload: Consumer does not exist.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_mc1_pr1_tx"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="TSQ-return-id"><td>

id

</td><td>

Sys\_id of the qualification customer order.Data type: String

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr id="TSQ-return-href"><td>

href

</td><td>

Relative link to the qualification order record. Data type: String

</td></tr><tr id="TSQ-return-descriptions"><td>

description

</td><td>

Description of the qualification request which is fetched from the short\_description field of the customer order.Data type: String

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr id="TSQ-return-externalId"><td>

externalId

</td><td>

External ID of the customer order. Data type: String

Table: in the external\_id field of the Customer Order \[sn\_ind\_tmt\_orm\_order\] table.

</td></tr><tr id="TSQ-return-qualificationResult"><td>

qualificationResult

</td><td>

Qualification status of the result field of the customer order. Possible values:

-   alternate
-   none
-   pending
-   qualified
-   unqualified

Data type: String

</td></tr><tr id="TSQ-return-state"><td>

state

</td><td>

State of customer order from the status field of customer order.Data type: String

</td></tr><tr id="TSQ-return-type"><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the qualification. This value is always `CheckServiceQualification`. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-checkServiceQualificationDate"><td>

checkServiceQualificationDate

</td><td>

Date and time the qualification request that was created from the order\_date field of the customer order.Data type: String

Format: YYYY-MM-DDTHH:MM:SS.SSSZ

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr id="TSQ-return-effectiveQualificationDate"><td>

effectiveQualificationDate

</td><td>

Effective qualification date fetched from the order\_date field of the customer order.Data type: String

Format: YYYY-MM-DDTHH:MM:SS.SSSZ

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr id="TSQ-return-expectedQualificationDate"><td>

expectedQualificationDate

</td><td>

Stores the expected qualification date. Persisted in expected\_end\_date field of the customer order.Data type: String

Format: YYYY-MM-DDTHH:MM:SS.SSSZ

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr id="TSQ-return-relatedParty"><td>

relatedParty

</td><td>

List of contacts for the qualification request. Each contact is an object in the array.Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr id="TSQ-return-relatedParty.id"><td>

relatedParty.id

</td><td>

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order.Data type: String

Table: Account \[customer\_account\] table, Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\]

</td></tr><tr id="TSQ-return-relatedParty.name"><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer.Data type: String

</td></tr><tr id="TSQ-return-relatedParty.type"><td>

relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for the order line item contact. This value is always `RelatedParty`. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-relatedParty.referredType"><td>

relatedParty.@referredType

</td><td>

Type of related party.Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem"><td>

serviceQualificationItem

</td><td>

List of service qualification items containing information about location, service information, and service characteristics. Stored as order line items for the customer order. Data type: Array of Objects

```
"serviceQualificationItem": [
  {
    "id": "String",
    "action": "String",
    "expectedServiceAvailabilityDate": "Number",
    "service": {Object},
    "@type": "String"
  }
]
```

</td></tr><tr id="TSQ-return-serviceQualificationItem.id"><td>

serviceQualificationItem.id

</td><td>

ID of the qualification item.Data type: String

Stored in: The external\_id field of customer order line item in the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr id="TSQ-return-serviceQualificationItem.qualificationResult"><td>

serviceQualificationItem.qualificationResult

</td><td>

Result of qualification item. Stored in the ‘result’ field of customer order line item. Possible values:

-   alternate
-   none
-   pending
-   qualified
-   unqualified

Data type: String

Table: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.state"><td>

serviceQualificationItem.state

</td><td>

State of qualification item derived from the ‘status’ field of customer order line item. Data type: String

Table: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.quantity"><td>

serviceQualificationItem.quantity

</td><td>

Quantity of qualification item derived from the ‘quantity’ field of customer order line item.Data type: Number

Table:Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.type"><td>

serviceQualificationItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the qualification item. This value is always ServiceQualificationItem. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service"><td>

serviceQualificationItem.service

</td><td>

Service information which includes details about location \(place\), service specifications, and service characteristics.Data type: Object

```
"service": {
  "@type": "String",
  "place": [Array],
  "serviceCharacteristic": [Array],
  "serviceSpecification": {Object}
}
```

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.type"><td>

serviceQualificationItem.service.@type

</td><td>

Part of TMF Open API standard. Annotation for the service. This value is always `Service`. This information is not stored. Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.place"><td>

serviceQualificationItem.service.place

</td><td>

Location information for the service qualification item.Data type: Array of Objects

**Note:** This array can contain only one location.

```
"place": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String"
  }
]
```

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.place.id"><td>

serviceQualificationItem.service.place.id

</td><td>

Sys\_id of the location.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.place.name"><td>

serviceQualificationItem.service.place.name

</td><td>

Name of the location. Not verified against an entry in the Location \[cmn\_location\] table.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.place.type"><td>

serviceQualificationItem.service.place.@type

</td><td>

Part of TMF Open API standard. Annotation for Service. This value is always `GeographicSite`. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification"><td>

serviceQualificationItem.service.serviceSpecification

</td><td>

Service specification details for the qualification item.Data type: Array of Objects

```
"serviceSpecification": {
  "id": "String",
  "internalVersion": "Number",
  "internalId": "String",
  "name": "String"
  "@type": "ServiceSpecification"
  "version": "String",
}

```

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.id"><td>

serviceQualificationItem.service.serviceSpecification.id

</td><td>

External ID or initial version of the service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.name"><td>

serviceQualificationItem.service.serviceSpecification.name

</td><td>

Name of the service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.version"><td>

serviceQualificationItem.service.serviceSpecification.version

</td><td>

External version of the service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.internalVersion"><td>

serviceQualificationItem.service.serviceSpecification.internalVersion

</td><td>

Internal version of the service specification.Data type: Number

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.internalId"><td>

serviceQualificationItem.service.serviceSpecification.internalId

</td><td>

Initial version of the service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceSpecification.type"><td>

serviceQualificationItem.service.serviceSpecification.@type

</td><td>

Part of TMF Open API standard. Annotation for Service Specification. This value is always `ServiceSpecification`. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceCharacteristic"><td>

serviceQualificationItem.service.serviceCharacteristic

</td><td>

List of service characteristics.Data type: Array of objects

```
"serviceCharacteristic": [
  {
    "name": "String",
    "value": "String",
    "valueType": "String"
  }
]
```

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceCharacteristic.valueType"><td>

serviceQualificationItem.service.serviceCharacteristic.valueType

</td><td>

Value type of the characteristic.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceCharacteristic.name"><td>

serviceQualificationItem.service.serviceCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.service.serviceCharacteristic.value"><td>

serviceQualificationItem.service.serviceCharacteristic.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal"><td>

ServiceQualificationItem.alternateServiceProposal

</td><td>

Alternate service proposal for the qualification order.Data type: String

Stored in: Alternate Proposal \[sn\_ord\_qual\_mgmt\_alternate\_proposal\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.id"><td>

ServiceQualificationItem.alternateServiceProposal.id

</td><td>

Sys\_id of the alternate proposal record.Data type: String

Table: Alternate Proposal \[sn\_ord\_qual\_mgmt\_alternate\_proposal\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.alternateServiceAvailabilityDate"><td>

ServiceQualificationItem.alternateServiceProposal.alternateServiceAvailabilityDate

</td><td>

The available\_date field value of the alternate proposal entry in the Alternate Proposal \[sn\_ord\_qual\_mgmt\_alternate\_proposal\] table.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.alternateService"><td>

serviceQualificationItem.alternateServiceProposal.alternateService

</td><td>

Service information represented by the alternate proposal.Data type: Object

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.alternateService.serviceSpecification"><td>

serviceQualificationItem.alternateServiceProposal.alternateService.serviceSpecification

</td><td>

Service specification of the alternate proposal persisted in specification.Data type: Object

Table: Alternate Proposal \[sn\_ord\_qual\_mgmt\_alternate\_proposal\]

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.id"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.id

</td><td>

External ID or initial version of the alternate service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.name"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.name

</td><td>

Name of the alternate service specification. Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.version"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.version

</td><td>

External version of the alternate service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.internalVersion"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.internalVersion

</td><td>

Internal version of the alternate service specification.Data type: Number

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.internalId"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.internalId

</td><td>

Initial version of the alternate service specification.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.type"><td>

ServiceQualificationItem. alternateServiceProposal.alternateService.serviceSpecification.@type

</td><td>

Part of TMF Open API standard. Annotation for Service Specification. This value is always `ServiceSpecification`. This information is not stored.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.serviceCharacteristic"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceCharacteristic

</td><td>

List of service characteristics for the alternate service proposal.Data type: Array of Objects

```
"serviceCharacteristic": [
  {
    "name": "String",
    "value": "String",
    "valueType": "String"
  }
]
```

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.serviceCharacteristic.valueType"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceCharacteristic.valueType

</td><td>

Value type of the alternate service characteristic.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.serviceCharacteristic.name"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceCharacteristic.name

</td><td>

Name of the alternate service characteristic.Data type: String

</td></tr><tr id="TSQ-return-serviceQualificationItem.alternateServiceProposal.serviceSpecification.serviceCharacteristic.value"><td>

serviceQualificationItem. alternateServiceProposal.alternateService.serviceCharacteristic.value

</td><td>

Value of the alternate service characteristic.Data type: String

</td></tr><tr id="serviceQualificationItem.eligibilityUnavailabilityReason"><td>

serviceQualificationItem.eligibilityUnavailabilityReason

</td><td>

List of service eligibility unavailability reasons to explain why the service is not available. Data type: Array

Stored in: The unavailability\_reason field of the Domain Order \[sn\_ind\_tmt\_orm\_domain\_order\] table.

</td></tr><tr id="serviceQualificationItem.eligibilityUnavailabilityReason.code"><td>

serviceQualificationItem.eligibilityUnavailabilityReason.code

</td><td>

Service eligibility unavailability reason code.Data type: String

</td></tr><tr id="serviceQualificationItem.eligibilityUnavailabilityReason.label"><td>

serviceQualificationItem.eligibilityUnavailabilityReason.label

</td><td>

Service eligibility unavailability reason label.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

The following example shows how the endpoint processes a qualification order sent in the API request.

```
curl -X POST "https://instance.service-now.com/api/sn_ord_qual_mgmt/qualification/checkServiceQualification/processResult " \ 
-H "Accept: application/json" \ 
-H "Content-Type: application/json" \ 
-u "username":"password" \ 
-d {
  "serviceQualificationItem": [
    {
      "eligibilityUnavailabilityReason": [
        {
          "code": "26-001",
          "label": "not enough bandwith at this place"
        }
      ],
      "qualificationResult": "alternate",
      "alternateServiceProposal": [
        {
          "alternateServiceAvailabilityDate": "2022-12-15T19:20:39.239Z",
          "@type": "AlternateServiceProposal",
          "id": "1",
          "alternateService": {
            "@type": "Service",
            "serviceSpecification": {
              "@type": "ServiceSpecification",
              "name": "Mobile Service",
              "id": "23",
              "href": "string"
            },
            "serviceCharacteristic": [
              {
                "@type": "ServiceCharacteristic",
                "valueType": "string",
                "name": "BroadcastQuality",
                "id": "1",
                "value": "HD"
              }
            ]
          }
        }
      ],
      "@type": "ServiceQualificationItem",
      "id": "295580b938bf1110f877c8d44c4b8912"
    },
    {
      "qualificationResult": "alternate",
      "alternateServiceProposal": [
        {
          "alternateServiceAvailabilityDate": "2022-12-15T19:20:39.239Z",
          "@type": "AlternateServiceProposal",
          "id": "1",
          "alternateService": {
            "@type": "Service",
            "serviceSpecification": {
              "@type": "ServiceSpecification",
              "name": "Mobile Service",
              "id": "23",
              "href": "string"
            },
            "serviceCharacteristic": [
              {
                "@type": "ServiceCharacteristic",
                "valueType": "string",
                "name": "BroadcastQuality",
                "id": "1",
                "value": "HD"
              }
            ]
          }
        }
      ],
      "@type": "ServiceQualificationItem",
      "action": "add",
      "id": "295580b938bf1110f877c8d44c4b8915"
    },
    {
      "qualificationResult": "alternate",
      "alternateServiceProposal": [
        {
          "alternateServiceAvailabilityDate": "2022-12-15T19:20:39.239Z",
          "@type": "AlternateServiceProposal",
          "id": "1",
          "alternateService": {
            "@type": "Service",
            "serviceSpecification": {
              "@type": "ServiceSpecification",
              "name": "Mobile Service",
              "id": "23",
              "href": "string"
            },
            "serviceCharacteristic": [
              {
                "@type": "ServiceCharacteristic",
                "valueType": "string",
                "name": "BroadcastQuality",
                "id": "1",
                "value": "HD"
              }
            ]
          }
        }
      ],
      "@type": "ServiceQualificationItem",
      "id": "2d5580b938bf1110f877c8d44c4b8902"
    }
  ],
  "@type": "CheckServiceQualification",
  "description": "check service qualification illustration"
}
```

Response body:

```
{
  "id": "0b45c47938bf1110f877c8d44c4b895d",
  "href": "/api/sn_ord_qual_mgmt/qualification/checkServiceQualification/0b45c47938bf1110f877c8d44c4b895d",
  "description": "check service qualification illustration",
  "externalId": "CSQ1",
  "qualificationResult": "alternate",
  "state": "new",
  "@type": "CheckServiceQualification",
  "checkServiceQualificationDate": "2022-12-14T23:44:44.000Z",
  "relatedParty": [
    {
      "id": "eaf68911c35420105252716b7d40ddde",
      "name": "Sally Thomas",
      "@type": "RelatedParty",
      "@referredType": "CustomerContact"
    },
    {
      "id": "ffc68911c35420105252716b7d40dd55",
      "name": "Funco Intl",
      "@type": "RelatedParty",
      "@referredType": "Customer"
    },
    {
      "id": "59f16de1c3b67110ff00ed23a140dd9e",
      "name": "Funco External",
      "@type": "RelatedParty",
      "@referredType": "Consumer"
    }
  ],
  "serviceQualificationItem": [
    {
      "id": "100",
      "qualificationResult": "alternate",
      "state": "in_progress",
      "quantity": "1",
      "@type": "ServiceQualificationItem",
      "service": {
        "@type": "Service",
        "serviceCharacteristic": [
          {
            "name": "Speed",
            "valueType": "choice",
            "value": "High"
          }
        ],
        "serviceSpecification": {
          "id": "91478553b7969910ff00f203ae11a97d",
          "name": "Broadband Service",
          "version": "",
          "internalVersion": "1",
          "internalId": "91478553b7969910ff00f203ae11a97d",
          "@type": "ServiceSpecification"
        },
        "place": {
          "id": "5671dd2ec3a53010188473ce3640dd81",
          "name": "3000 Main Street, Santa Clara, CA",
          "@referredType": "GeographicSite"
        }
      },
      "alternateServiceProposal": [
        {
          "id": "350e66a2e5331110f87741b459ef19b0",
          "alternateServiceAvailabilityDate": "2022-12-15 19:20:39",
          "alternateService": {
            "serviceCharacteristic": [
              {
                "@type": "ServiceCharacteristic",
                "valueType": "string",
                "name": "BroadcastQuality",
                "id": "1",
                "value": "HD"
              }
            ],
            "serviceSpecification": {
              "id": "23e7ed67c32310105252716b7d40dd80",
              "name": "Mobile Service",
              "version": "",
              "internalVersion": "1",
              "internalId": "23e7ed67c32310105252716b7d40dd80",
              "@type": "ServiceSpecification"
            },
            "@type": "Service"
          },
          "@type": "AlternateServiceProposal"
        }
      ],
      "eligibilityUnavailabilityReason": [
        {
          "label": "not enough bandwith at this place",
          "@type": "string"
        }
      ]
    }
  ],
  "effectiveQualificationDate": "2023-12-14T23:44:44.000Z",
  "expectedQualificationDate": "2023-10-11T15:20:39.000Z"
}
```

