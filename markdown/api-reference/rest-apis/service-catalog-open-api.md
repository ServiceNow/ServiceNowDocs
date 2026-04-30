---
title: Service Catalog Open API
description: The Service Catalog Open API provides endpoints to create and retrieve service specifications.Retrieves a list of all service specifications.Retrieves a service specification.Creates a service specification.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 20
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Service Catalog Open API

The Service Catalog Open API provides endpoints to create and retrieve service specifications.

Use this API to manage service catalog information between external systems and the ServiceNow AI Platform. The Service Catalog Open API is a ServiceNow® implementation of the TM Forum Service Catalog API REST specification. This implementation is based on the [TMF633 Service Catalog API REST Specification Version 4](https://www.tmforum.org/resources/standard/tmf633-service-catalog-api-user-guide-v4-0-0/), October 2020.

This API is included in the Product Catalog Advanced application, which is available on the ServiceNow Store.

This API is provided within the `sn_prd_pm_adv` namespace.

The calling user must have the sn\_prd\_pm\_adv.catalog\_integrator role.

This API creates and updates data in the following tables.

-   Characteristic \[sn\_prd\_pm\_characteristic\]
-   Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]
-   Service Specification \[sn\_prd\_pm\_service\_specification\]
-   Specification Relationship \[sn\_prd\_pm\_specification\_relationship\]

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Service Catalog Open - GET /servicespecification

Retrieves a list of all service specifications.

### URL format

Default URL: `/api/sn_prd_pm_adv/catalogmanagement/servicespecification`

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

List of fields to return in the response. Invalid fields are ignored. If this parameter is not used, all fields are returned. Data type: String

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

</td></tr><tr><td>

state

</td><td>

Filter service specifications by state. Only specifications with a state matching the value of this parameter are returned in the response.Data type: String

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

<table id="table_hnx_3gy_fsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the specification.Data type: String

</td></tr><tr><td>

externalId

</td><td>

External ID of the service specification.Data type: String

Table: In the external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

id

</td><td>

Initial version or external ID of the service specification.Data type: String

Table: In the initial\_version or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

internalId

</td><td>

Initial version of the service specification.Data type: String

Table: In the initial\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

internalVersion

</td><td>

Version of the service specification.Data type: String

Table: In the version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

lastUpdate

</td><td>

Date the specification was last updated.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the specification.Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

Resource specifications for this service specification.Data type: Array of Objects

```
"resourceSpecification": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "name": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

resourceSpecification.id

</td><td>

The initial\_version or external\_id of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.internalId

</td><td>

The initial\_version of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.internalVersion

</td><td>

The external\_version of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.name

</td><td>

Name of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.version

</td><td>

Version of the resource specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship

</td><td>

This specification's relationships to other service specifications.Data type: Array of Objects

```
"serviceSpecificationRelationship": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "relationshipType": "String",
    "validFor": {Object},
    "version": "String"
  }
]
```

</td></tr><tr><td>

serviceSpecificationRelationship.id

</td><td>

The initial\_version or external\_id of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.internalId

</td><td>

The initial\_version of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.internalVersion

</td><td>

Version of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.relationshipType

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.validFor

</td><td>

Date range the relationship is valid for.Data type: Object

```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

serviceSpecificationRelationship.validFor.endDateTime

</td><td>

End date of the relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.validFor.startDateTime

</td><td>

Start date of the relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.version

</td><td>

The external\_version of the related specification.Data type: String

</td></tr><tr><td>

specCharacteristic

</td><td>

Specification characteristic.Data type: Array of Objects

```
"specCharacteristic": [
  {
    "characteristicValueSpecification": [Array],
    "description": "String",
    "name": "String",
    "validFor": {Object},
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification

</td><td>

List of possible values of the characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [
  {
    "value": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

specCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.valueType

</td><td>

Value type of the characteristic, such as choice or email.Data type: String

</td></tr><tr><td>

validFor

</td><td>

Date range the specification is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date of the specification.Data type: String

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date of the specification.Data type: String

</td></tr><tr><td>

version

</td><td>

External version of the service specification.Data type: String

Table: In the external\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

@type

</td><td>

Type of specification.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves all service specifications.

```
curl --location --request GET "https://instance.servicenow.com/api/sn_prd_pm_adv/catalogmanagement/servicespecification" \
--user 'username':'password'



```

Response body.

```
[
   {
      "id": "16d79ec3532520103b6bddeeff7b12a6",
      "name": "SD WAN Optimization Service",
      "description": "SD WAN Optimization Service",
      "lastUpdate": "2022-01-23 22:48:55",
      "validFor": {
         "startDateTime": "2022-01-12",
         "endDateTime": "2027-02-11"
      },
      "serviceSpecificationRelationship": [
         {
            "id": "a1f5fe981bb420106ba59acf034bcb4f",
            "name": "Deduplication and Compression",
            "version": "1",
            "type": "rfs",
            "validFor": {
               "startDateTime": "2021-02-11",
               "endDateTime": "2027-02-11"
            }
         }
      ],
      "resourceSpecification": [],
      "serviceSpecCharacteristic": [
         {
            "name": "SSL Optimization",
            "description": "SSL Optimization",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2022-01-14 07:47:57"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "False",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "True",
                  "validFor": {
                     "startDateTime": ""
                  }
               }
            ]
         },
         {
            "name": "CIFS Optimization",
            "description": "CIFS Optimization Protocol",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2022-01-14 07:49:09"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "SMB1",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "SMB2",
                  "validFor": {
                     "startDateTime": ""
                  }
               }
            ]
         }
      ]
   },
   {
      "id": "31c5caff07266010a7955b7e0ad3006b",
      "name": "Firewall Administration",
      "description": "Firewall Administration",
      "lastUpdate": "2022-01-23 11:46:48",
      "validFor": {
         "startDateTime": "2021-11-22",
         "endDateTime": ""
      },
      "serviceSpecificationRelationship": [],
      "resourceSpecification": [
         {
            "id": "3546463307666010a7955b7e0ad3005d",
            "name": "Cisco Firewall Management system",
            "version": "1"
         }
      ],
      "serviceSpecCharacteristic": [
         {
            "name": "Firewall Administration CPE Model",
            "description": "Firewall Administration CPE Model",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2022-02-20 00:55:37"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "2100 series",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "4100 series",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "7300 series",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "9300 series",
                  "validFor": {
                     "startDateTime": ""
                  }
               }
            ]
         },
         {
            "name": "Firewall Administration CPE Type",
            "description": "Firewall Administration CPE Type",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2022-02-20 00:53:45"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "Physical",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Virtual",
                  "validFor": {
                     "startDateTime": ""
                  }
               }
            ]
         },
         {
            "name": "Configuration and Policy backup",
            "description": "Configuration and Policy backup",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2022-01-21 10:46:02"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "Weekly",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Monthly",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Daily",
                  "validFor": {
                     "startDateTime": ""
                  }
               }
            ]
         },
         {
            "name": "Remote CLI troubleshoot support",
            "description": "Remote CLI troubleshoot support",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2022-01-21 10:45:38"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "Standard support",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Premium support",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Basic support",
                  "validFor": {
                     "startDateTime": ""
                  }
               }
            ]
         },
         {
            "name": "Firewall Administration CPE ID",
            "description": "Firewall Administration CPE ID",
            "valueType": "single_line_text",
            "validFor": {
               "startDatetime": "2022-02-20 00:57:50"
            },
            "productSpecCharacteristicValue": []
         }
      ]
   }
]
```

## Service Catalog Open - GET /servicespecification/\{specificationId\}

Retrieves a service specification.

### URL format

Default URL: `/api/sn_prd_pm_adv/catalogmanagement/servicespecification/{specificationId}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

specificationId

</td><td>

Sys\_id of the service specification to retrieve.Data type: String

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr></tbody>
</table><table id="table_pfr_vgy_fsb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. If this parameter is not used, all fields are returned. Data type: String

</td></tr><tr><td>

state

</td><td>

Filter service specifications by state. Only specifications with a state matching the value of this parameter are returned in the response.Data type: String

</td></tr></tbody>
</table>|Name|Description|
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

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Request successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. Could be any of the following reasons:

-   Invalid path parameter
-   Invalid URI

</td></tr><tr><td>

404

</td><td>

Record not found. Record associated with the ID is not found in the table.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_hnx_3gy_fsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the specification.Data type: String

</td></tr><tr><td>

externalId

</td><td>

External ID of the service specification.Data type: String

Table: In the external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

id

</td><td>

Initial version or external ID of the service specification.Data type: String

Table: In the initial\_version or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

internalId

</td><td>

Initial version of the service specification.Data type: String

Table: In the initial\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

internalVersion

</td><td>

Version of the service specification.Data type: String

Table: In the version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

lastUpdate

</td><td>

Date the specification was last updated.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the specification.Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

Resource specifications for this service specification.Data type: Array of Objects

```
"resourceSpecification": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "name": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

resourceSpecification.id

</td><td>

The initial\_version or external\_id of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.internalId

</td><td>

The initial\_version of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.internalVersion

</td><td>

The external\_version of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.name

</td><td>

Name of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.version

</td><td>

Version of the resource specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship

</td><td>

This specification's relationships to other service specifications.Data type: Array of Objects

```
"serviceSpecificationRelationship": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "relationshipType": "String",
    "validFor": {Object},
    "version": "String"
  }
]
```

</td></tr><tr><td>

serviceSpecificationRelationship.id

</td><td>

The initial\_version or external\_id of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.internalId

</td><td>

The initial\_version of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.internalVersion

</td><td>

Version of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.relationshipType

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.validFor

</td><td>

Date range the relationship is valid for.Data type: Object

```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

serviceSpecificationRelationship.validFor.endDateTime

</td><td>

End date of the relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.validFor.startDateTime

</td><td>

Start date of the relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.version

</td><td>

The external\_version of the related specification.Data type: String

</td></tr><tr><td>

specCharacteristic

</td><td>

Specification characteristic.Data type: Array of Objects

```
"specCharacteristic": [
  {
    "characteristicValueSpecification": [Array],
    "description": "String",
    "name": "String",
    "validFor": {Object},
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification

</td><td>

List of possible values of the characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [
  {
    "value": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

specCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.valueType

</td><td>

Value type of the characteristic, such as choice or email.Data type: String

</td></tr><tr><td>

validFor

</td><td>

Date range the specification is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date of the specification.Data type: String

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date of the specification.Data type: String

</td></tr><tr><td>

version

</td><td>

External version of the service specification.Data type: String

Table: In the external\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

@type

</td><td>

Type of specification.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves a service specification for a firewall service.

```
curl --location --request GET "https://instance.servicenow.com/api/sn_prd_pm_adv/catalogmanagement/servicespecification/31c5caff07266010a7955b7e0ad3006b" \
--user 'username':'password'



```

Response body.

```
{
   "id": "31c5caff07266010a7955b7e0ad3006b",
   "name": "Firewall Administration",
   "description": "Firewall Administration",
   "lastUpdate": "2022-01-23 11:46:48",
   "validFor": {
      "startDateTime": "2021-11-22",
      "endDateTime": ""
   },
   "serviceSpecificationRelationship": [],
   "resourceSpecification": [
      {
         "id": "3546463307666010a7955b7e0ad3005d",
         "name": "Cisco Firewall Management system",
         "version": "1"
      }
   ],
   "serviceSpecCharacteristic": [
      {
         "name": "Firewall Administration CPE Model",
         "description": "Firewall Administration CPE Model",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2022-02-20 00:55:37"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "2100 series",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "4100 series",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "7300 series",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "9300 series",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ]
      },
      {
         "name": "Firewall Administration CPE Type",
         "description": "Firewall Administration CPE Type",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2022-02-20 00:53:45"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Physical",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Virtual",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ]
      },
      {
         "name": "Configuration and Policy backup",
         "description": "Configuration and Policy backup",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2022-01-21 10:46:02"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Weekly",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Monthly",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Daily",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ]
      },
      {
         "name": "Remote CLI troubleshoot support",
         "description": "Remote CLI troubleshoot support",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2022-01-21 10:45:38"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Standard support",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Premium support",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Basic support",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ]
      },
      {
         "name": "Firewall Administration CPE ID",
         "description": "Firewall Administration CPE ID",
         "valueType": "single_line_text",
         "validFor": {
            "startDatetime": "2022-02-20 00:57:50"
         },
         "productSpecCharacteristicValue": []
      }
   ]
}
```

## Service Catalog Open - POST /servicespecification

Creates a service specification.

### URL format

Default URL: `/api/sn_prd_pm_adv/catalogmanagement/servicespecification`

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

description

</td><td>

Required. Description of the specification.Data type: String

</td></tr><tr><td>

externalId

</td><td>

External ID of the service specification.If both **externalId** and **id** are provided, they must refer to the same specification.

Data type: String

Default: Blank string

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr><tr><td>

id

</td><td>

The initial\_version or external\_id of the service specification. If **id** is not provided, this endpoint creates a new specification with version=1. If **id** is provided, this endpoint creates a new version of the given specification. If both **externalId** and **id** are provided, they must refer to the same specification.

Data type: String

Default: Blank string

</td></tr><tr><td>

internalVersion

</td><td>

Version of the service specification.Data type: String

Default: Blank string

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr><tr><td>

lastUpdate

</td><td>

Date the specification was last updated.Data type: String

Default: Blank string

</td></tr><tr><td>

name

</td><td>

Required. Name of the specification.Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

Required. Resource specifications for this service specification.Data type: Array of Objects

```
"resourceSpecification": [
  {
    "id": "String",
    "internalVersion": "String",
    "name": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

resourceSpecification.id

</td><td>

Required. The initial\_version or external\_id of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.internalVersion

</td><td>

The external\_version of the resource specification.Data type: String

Default: Blank string

</td></tr><tr><td>

resourceSpecification.name

</td><td>

Name of the resource specification.Data type: String

Default: Blank string

</td></tr><tr><td>

resourceSpecification.version

</td><td>

Version of the resource specification.Data type: String

Default: Blank string

</td></tr><tr><td>

serviceSpecificationRelationship

</td><td>

Details of the specification's relationships to other service specifications.Data type: Array of Objects

```
"serviceSpecificationRelationship": [
  {
    "id": "String",
    "internalVersion": "String",
    "relationshipType": "String",
    "validFor": {Object},
    "version": "String"
  }
]
```

</td></tr><tr><td>

serviceSpecificationRelationship.id

</td><td>

Required if using the **serviceSpecificationRelationship** parameter. Initial\_version or external\_id of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.internalVersion

</td><td>

Version of the related specification.Data type: String

Default: Blank string

</td></tr><tr><td>

serviceSpecificationRelationship.relationshipType

</td><td>

Required if using the **serviceSpecificationRelationship** parameter. Type of relationship.Valid values:

-   bundles
-   composed\_of

Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.validFor

</td><td>

Date range the relationship is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

serviceSpecificationRelationship.validFor.endDateTime

</td><td>

End date of the relationship.Data type: String

Default: Blank string

</td></tr><tr><td>

serviceSpecificationRelationship.validFor.startDateTime

</td><td>

Start date of the relationship.Data type: String

Default: Blank string

</td></tr><tr><td>

serviceSpecificationRelationship.version

</td><td>

The external\_version of the related specification.Data type: String

Default: Blank string

</td></tr><tr><td>

specCharacteristic

</td><td>

Specification characteristic.Data type: Array of Objects

```
"specCharacteristic": [
  {
    "characteristicValueSpecification": [Array],
    "description": "String",
    "name": "String",
    "validFor": {Object},
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification

</td><td>

Required. Possible values of the characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [
  {
    "value": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification.value

</td><td>

Required. Value of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

Default: Blank string

</td></tr><tr><td>

specCharacteristic.name

</td><td>

Required. Name of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

specCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic.Data type: String

Default: Blank string

</td></tr><tr><td>

specCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic.Data type: String

Default: Blank string

</td></tr><tr><td>

specCharacteristic.valueType

</td><td>

Required. Value type of the characteristic, such as choice or email.Data type: String

</td></tr><tr><td>

validFor

</td><td>

Required. Date range the specification is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date of the specification.Data type: String

Default: Blank string

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date of the specification.Data type: String

Default: Blank string

</td></tr><tr><td>

version

</td><td>

External version of the service specification. Version must be unique for the given version chain.

Data type: String

Default: Blank string

Table: In the external\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

@type

</td><td>

Required. Type of specification.Valid values:

-   CustomerFacingServiceSpecification
-   ResourceFacingServiceSpecification

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
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

201

</td><td>

Request successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. Could be any of the following reasons: -   Empty payload.
-   Invalid payload. Mandatory field missing: &lt;field name&gt;

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_hnx_3gy_fsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the specification.Data type: String

</td></tr><tr><td>

externalId

</td><td>

External ID of the service specification.Data type: String

Table: In the external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

id

</td><td>

Initial version or external ID of the service specification.Data type: String

Table: In the initial\_version or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

internalId

</td><td>

Initial version of the service specification.Data type: String

Table: In the initial\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

internalVersion

</td><td>

Version of the service specification.Data type: String

Table: In the version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

lastUpdate

</td><td>

Date the specification was last updated.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the specification.Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

Resource specifications for this service specification.Data type: Array of Objects

```
"resourceSpecification": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "name": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

resourceSpecification.id

</td><td>

The initial\_version or external\_id of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.internalId

</td><td>

The initial\_version of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.internalVersion

</td><td>

The external\_version of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.name

</td><td>

Name of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.version

</td><td>

Version of the resource specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship

</td><td>

This specification's relationships to other service specifications.Data type: Array of Objects

```
"serviceSpecificationRelationship": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "relationshipType": "String",
    "validFor": {Object},
    "version": "String"
  }
]
```

</td></tr><tr><td>

serviceSpecificationRelationship.id

</td><td>

The initial\_version or external\_id of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.internalId

</td><td>

The initial\_version of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.internalVersion

</td><td>

Version of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.relationshipType

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.validFor

</td><td>

Date range the relationship is valid for.Data type: Object

```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

serviceSpecificationRelationship.validFor.endDateTime

</td><td>

End date of the relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.validFor.startDateTime

</td><td>

Start date of the relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.version

</td><td>

The external\_version of the related specification.Data type: String

</td></tr><tr><td>

specCharacteristic

</td><td>

Specification characteristic.Data type: Array of Objects

```
"specCharacteristic": [
  {
    "characteristicValueSpecification": [Array],
    "description": "String",
    "name": "String",
    "validFor": {Object},
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification

</td><td>

List of possible values of the characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [
  {
    "value": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

specCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.valueType

</td><td>

Value type of the characteristic, such as choice or email.Data type: String

</td></tr><tr><td>

validFor

</td><td>

Date range the specification is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date of the specification.Data type: String

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date of the specification.Data type: String

</td></tr><tr><td>

version

</td><td>

External version of the service specification.Data type: String

Table: In the external\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

@type

</td><td>

Type of specification.Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates a service specification for a firewall service.

```
curl "https://instance.servicenow.com/api/sn_prd_pm_adv/catalogmanagement/servicespecification" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   "externalId": "7655",
   "name": "Firewall Service",
   "description": "This service specification describes a firewall service that can be deployed in customer-premises equipment.",
   "validFor": {
      "startDateTime": "2017-08-23T00:00",
      "endDateTime": "2021-03-25T00:00"
   },
   "lastUpdate": "2020-08-15T00:00",
   "resourceSpecification": [
      {
         "id": "af66e551c32f10105252716b7d40dd52",
         "name": "Firewall"
      }
   ],
   "specCharacteristic": [
      {
         "name": "Edge",
         "description": "This characteristic describes the operating system run by the service",
         "valueType": "choice",
         "validFor": {
            "startDateTime": "2017-08-12T00:00",
            "endDateTime": "2021-03-07T00:00"
         },
         "characteristicValueSpecification": [
            {
               "value": "Android KitKat"
            }
         ],
      }
   ],
   "serviceSpecRelationship": [
      {
         "relationshipType": "composed_of",
         "id": "65033023ebdb30107ee5302698522849",
         "validFor": {
            "startDateTime": "2017-08-25T00:00",
            "endDateTime": "2021-03-25T00:00"
         }
      }
   ],
   "@type": "ResourceFacingServiceSpecification"
}" \
--user 'username':'password'
```

Response body.

```
{
   "id": "21a7ee64c32310105253716b8d40dd60",
   "name": "Firewall Service",
   "description": "This service specification describes a firewall service that can be deployed in customer-premises equipment.",
   "validFor": {
      "startDateTime": "2017-08-23T00:00",
      "endDateTime": "2021-03-25T00:00"
   },
   "lastUpdate": "2020-08-15T00:00",
   "resourceSpecification": [
      {
         "id": "af66e551c32f10105252716b7d40dd52",
         "name": "Firewall"
      }
   ],
   "specCharacteristic": [
      {
         "name": "Edge",
         "description": "This characteristic describes the operating system run by the service",
         "valueType": "choice",
         "validFor": {
            "startDateTime": "2017-08-12T00:00",
            "endDateTime": "2021-03-07T00:00"
         },
         "characteristicValueSpecification": [
            {
               "value": "Android KitKat"
            }
         ],
      }
   ],
   "serviceSpecRelationship": [
      {
         "relationshipType": "composed_of",
         "id": "65033023ebdb30107ee5302698522849",
         "validFor": {
            "startDateTime": "2017-08-25T00:00",
            "endDateTime": "2021-03-25T00:00"
         }
      }
   ],
   "@type": "ResourceFacingServiceSpecification"
}
```

