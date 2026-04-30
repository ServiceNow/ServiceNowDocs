---
title: Verify Entitlements API
description: The Verify Entitlements API provides endpoints that enable you to obtain a list of valid entitlements, details about the characteristics of entitlements, and an entitlement's latest usage information.Returns the valid entitlement records based on the provided filter.Returns details of the specified entitlement characteristic record and its latest usage record.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 14
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Verify Entitlements API

The Verify Entitlements API provides endpoints that enable you to obtain a list of valid entitlements, details about the characteristics of entitlements, and an entitlement's latest usage information.

To access this API, the Entitlement Verification \(com.sn\_ent\_verify\) plugin must be activated.

This API is provided within the `sn_ent_verify` namespace.

The calling user must have the sn\_pss\_core.pss\_integrator role.

The REST endpoints of this API query data from the following tables:

-   Account \[customer\_account\]
-   Consumer \[csm\_consumer\]
-   Entitlement \[service\_entitlement\]
-   Entitlement Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]
-   Entitlement Usages \[sn\_pss\_core\_entitlement\_usage\]
-   Household \[csm\_household\]
-   Install Base \[sn\_install\_base\_item\]
-   Product Model \[cmdb\_model\]
-   Product Offering \[sn\_prd\_pm\_product\_offering\]
-   Product Specification \[sn\_prd\_pm\_product\_specification\]
-   Service Contract \[sn\_pss\_core\_service\_contract\]
-   Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]
-   Sold Product \[sn\_install\_base\_sold\_product\]

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Verify Entitlements - GET /sn\_ent\_verify/verifyentitlements

Returns the valid entitlement records based on the provided filter.

You can filter entitlements based on:

-   Account
-   Consumer
-   Contract
-   Household
-   Install base
-   Product model
-   Product offering
-   Product specification
-   Service contract line
-   Sold entitlement
-   Sold product
-   State

At a minimum, you must specify either the account or the consumer on which to filter the entitlements.

When multiple filter parameters are passed, the endpoint applies the `AND` operator to the parameters. For example, if you pass filter parameters such as `"account = boxeo"` and `“state = draft”`, the endpoint returns all the entitlements with Account = boxeo `AND` state = draft.

You can implement pagination for the return results by passing the system pagination parameters **sysparm\_offset** and **sysparm\_limit**. By default **sysparm\_offset** is set to 0 and **sysparm\_limit** is set to 10. So, if after applying the filter, 100 entitlements satisfy the criteria, the response will include the first 10 entitlements. You can modify these values by passing them in the endpoint call.

### URL format

Versioned URL: `/api/sn_ent_verify/{api_version}/verifyentitlements`

Default URL: `/api/sn_ent_verify/verifyentitlements`

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

sysparm\_limit

</td><td>

Optional.Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval.

In the response, the boolean parameter **hasMore** is returned. It indicates whether there are more records to return that meet the filter criteria.

Data type: Number

Default: 10

Maximum: 100

</td></tr><tr><td>

sysparm\_offset

</td><td>

Optional. Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks.

For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Do not pass a negative number in the **sysparm\_offset** parameter.

Data type: Number

Default: 0

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td>

Either the **account** or **consumer** parameter must be passed. They are mutually exclusive. Sys\_id of the account record for which to return entitlement records.Data type: String

Default: None

Table: Account \[customer\_account\]

</td></tr><tr><td>

consumer

</td><td>

Either the **account** or **consumer** parameter must be passed. They are mutually exclusive. Sys\_id of the consumer record for which to return entitlement records. Data type: String

Default: None

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

contract

</td><td>

Sys\_id of the contract record for which to return entitlement records.Data type: String

Default: None

Table: Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

display\_value

</td><td id="csm-display_value-entry">

Flag that indicates whether to return the associated field value, display value, or both.Valid values:

-   true: Response contains only the display values of the fields. For example: `"state": "Draft"`.
-   false: Response contains only the values of the fields. For example:`"state": "draft"`.
-   all: Response contains all the information for the fields.

For example:

    ```
"state": {
  "name": "state",
  "label": "State",
  "value": "draft",
  "display_value": "true",
  "type": "string"
}
    ```


Data type: String

Default: false

</td></tr><tr><td>

household

</td><td>

Sys\_id of the household record for which to return entitlement records.Data type: String

Default: None

Table: Household \[csm\_household\]

</td></tr><tr><td>

install\_base

</td><td>

Sys\_id of the install base record for which to return entitlement records.The endpoint uses the sys\_id of the install base record to search the Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\] table to return all entitlements covered by the associated install base.

Data type: String

Default: None

Table: Install Base \[sn\_install\_base\_item\]

</td></tr><tr><td>

product

</td><td>

Sys\_id of the product record for which to return entitlement records.Data type: String

Default: None

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

product\_offering

</td><td>

Sys\_id of the product offering record for which to return entitlement records.Data type: String

Default: None

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

product\_specification

</td><td>

Sys\_id of product specification record for which to return entitlement records. Data type: String

Default: None

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

service\_contract\_line

</td><td>

Sys\_id of the service contract line record for which to return entitlement records.Data type: String

Default: None

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

sold\_entitlement

</td><td>

Sys\_id of the sold entitlement record for which to return entitlement records.Data type: String

Default: None

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

sold\_product

</td><td>

Sys\_id of the sold product record for which to return entitlement records.The endpoint uses the sys\_id of the Sold Product record to search the Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\] table to return all entitlements covered by the associated sold product.

Data type: String

Default: None

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

state

</td><td>

State of the entitlements to return.Valid values:

-   active
-   cancelled
-   draft
-   expired
-   suspended

Data type: String

Default: All

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
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

entitlements

</td><td>

List of entitlements that match the passed filter criteria.Data type: Array of Objects

```
"entitlements": [
  {
    "account": "String",
    "consumer": "String",
    "contract": "String",
    "end_date": "String",
    "entitlement_name": "String",
    "household": "String",
    "product": "String",
    "product_offering": "String",
    "product_specification": "String",
    "service_contract_line": "String",
    "sold_entitlement": "String",
    "start_date": "String",
    "state": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

entitlements.account

</td><td>

Sys\_id of the account record associated with this entitlement.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

entitlements.consumer

</td><td>

Sys\_id of the consumer record associated with this entitlement.Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

entitlements.contract

</td><td>

Sys\_id of the contract record associated with this entitlement.Data type: String

Table: Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

entitlements.end\_date

</td><td>

Value of the End Date field on the associated entitlement record.Data type: String

</td></tr><tr><td>

entitlements.entitlement\_name

</td><td>

Name of the entitlement.Data type: String

</td></tr><tr><td>

entitlements.household

</td><td>

Sys\_id of the household record associated with this entitlement.Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

entitlements.product

</td><td>

Sys\_id of the product record associated with this entitlement.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

entitlements.product\_offering

</td><td>

Sys\_id of the product offer record associated with this entitlement.Data type: String

Table: Product Offer \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

entitlements.product\_specification

</td><td>

Sys\_id of the product specification record associated with this entitlement.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

entitlements.service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with this entitlement.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

entitlements.sold\_entitlement

</td><td>

Sys\_id of the sold entitlement record associated with this entitlement.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

entitlements.start\_date

</td><td>

Value of the Start Date field on the associated entitlement record.Data type: String

</td></tr><tr><td>

entitlements.state

</td><td>

State of the entitlements record.Possible values:

-   active
-   cancelled
-   draft
-   expired
-   suspended

Data type: String

</td></tr><tr><td>

entitlements.sys\_id

</td><td>

Sys\_id of the entitlement record.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

error

</td><td>

Describes the error that occurred.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

Examples of error responses:

-   Error message: Page size -20 is Invalid. Page size must be an integer between 1 and 100

Error condition: Invalid **sysparm\_limit** parameter passed. The **sysparm\_limit** parameter must be between 1 and 100.

-   Error message: Page offset -23 is invalid. Offset must be an integer greater than or equal to 0

Error condition: Invalid **sysparm\_offset** parameter passed. The **sysparm\_offset** parameter must be a whole number.

-   Error message: Invalid Query Parameter - accnt

Error condition: Invalid query parameter, "accnt", was passed. Parameter should be "account".

-   Error message: Invalid choice value: state = drft

Error condition: Invalid value, "drft", was passed. Parameter value should be "draft".


</td></tr><tr><td>

error.detail

</td><td>

Detailed information as to why the endpoint call failed.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Message that describes the error at a high-level.Data type: String

</td></tr><tr><td>

hasMore

</td><td>

Flag that indicates whether there are more entitlement records to return.Possible values:

-   true: More entitlement records to return.
-   false: No more entitlement records.

Data type: Boolean

</td></tr><tr><td>

status

</td><td>

Status of the endpoint call.Possible values:

-   failure: An error occurred when processing the request.
-   success: The call was processed successfully.

Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td>

If the **sysparm\_limit** parameters was passed in the endpoint call, it contains the passed value, otherwise it contains the default value.Data type: Number

</td></tr><tr><td>

sysparm\_offset

</td><td>

If the **sysparm\_offset** parameters was passed in the endpoint call, it contains the passed value, otherwise it contains the default value.Data type: Number

</td></tr></tbody>
</table>### cURL request

The following code example shows how to return entitlements for a specific account.

```
curl "https://instance.service-now.com/api/sn_ent_verify/verifyentitlements?account=9e2fd2ee11b43110f877366201dea674" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Return results:

```
{
  "result": {
    "sysparm_offset": "0",
    "sysparm_limit": "10",
    "has_more": "false",
    "entitlements": [
      {
        "sys_id": "38374bf251e27110f877bf82d3ddf30a",
        "entitlement_name": "test ent",
        "account": "9e2fd2ee11b43110f877366201dea674",
        "consumer": null,
        "household": null,
        "contract": "0e1747f251e27110f877bf82d3ddf31c",
        "service_contract_line": "da278fb251e27110f877bf82d3ddf3b7",
        "state": "active",
        "product_offering": null,
        "product_specification": null,
        "sold_entitlement": null,
        "product": null,
        "start_date": "2023-11-21",
        "end_date": ""
      },
      {
        "sys_id": "e6ad4e4151723d10f877bf82d3ddf3fb",
        "entitlement_name": "tets entitlement",
        "account": "9e2fd2ee11b43110f877366201dea674",
        "consumer": null,
        "household": null,
        "contract": "0e1747f251e27110f877bf82d3ddf31c",
        "service_contract_line": "e79dce4151723d10f877bf82d3ddf31d",
        "state": "active",
        "product_offering": null,
        "product_specification": null,
        "sold_entitlement": null,
        "product": null,
        "start_date": "2023-11-21",
        "end_date": ""
      }
    ],
    "status": "success"
  }
}
```

### cURL request

The following code example shows how to return entitlements for a specific account and service contract line.

```
curl "https://instance.service-now.com/api/sn_ent_verify/verifyentitlements?service_contract_line=e79dce4151723d10f877bf82d3ddf31d&account=9e2fd2ee11b43110f877366201dea674" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Return results:

```
{
  "result": {
    "sysparm_offset": "0",
    "sysparm_limit": "10",
    "has_more": "false",
    "entitlements": [
      {
        "sys_id": "e6ad4e4151723d10f877bf82d3ddf3fb",
        "entitlement_name": "test entitlement",
        "account": "9e2fd2ee11b43110f877366201dea674",
        "consumer": null,
        "household": null,
        "contract": "0e1747f251e27110f877bf82d3ddf31c",
        "service_contract_line": "e79dce4151723d10f877bf82d3ddf31d",
        "state": "active",
        "product_offering": null,
        "product_specification": null,
        "sold_entitlement": null,
        "product": null,
        "start_date": "2023-11-21",
        "end_date": ""
      }
    ],
    "status": "success"
  }
}
```

### cURL request

The following code example shows an error response.

```
curl "https://instance.service-now.com/api/sn_ent_verify/verifyentitlements?service_contract_line=e79dce4151723d10f877bf82d3ddf31d" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Return results:

```
{
  "error": {
    "detail": "At least one of Account or Consumer parameter is mandatory.",
    "message": "At least one of Account or Consumer parameter is mandatory."
  },
  "status": "failure"
}
```

## Verify Entitlements - GET /sn\_ent\_verify/verifyentitlements/getEntitlementCharacteristic/\{id\}

Returns details of the specified entitlement characteristic record and its latest usage record.

The latest usage record for a characteristic is defined as the record where the period start date is less than or equal to the current date and the period end date is greater than or equal to the current date.

### URL format

Versioned URL: `/api/sn_ent_verify/{api_version}/verifyentitlements/getEntitlementCharacteristic/{id}`

Default URL: `/api/sn_ent_verify/verifyentitlements/getEntitlementCharacteristic/{id}`

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

id

</td><td>

Sys\_id of the entitlement characteristic record to return.Data type: String

Table: Entitlement Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

display\_value

</td><td id="csm-display_value-entry">

Flag that indicates whether to return the associated field value, display value, or both.Valid values:

-   true: Response contains only the display values of the fields. For example: `"state": "Draft"`.
-   false: Response contains only the values of the fields. For example:`"state": "draft"`.
-   all: Response contains all the information for the fields.

For example:

    ```
"state": {
  "name": "state",
  "label": "State",
  "value": "draft",
  "display_value": "true",
  "type": "string"
}
    ```


Data type: String

Default: false

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
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

characteristic

</td><td>

Sys\_id of the associated entitlement characteristic record.Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

characteristic\_option

</td><td>

Sys\_id of the associated characteristic options record.Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

entitlement\_usage

</td><td>

Details about the entitlement usage record associated with the specified entitlement characteristic record.Data type: Array of Objects

```
"entitlement_usage": [
  {
    "entitlement_characteristic": "String",
    "period_end": "String",
    "period_start": "String",
    "sys_id": "String",
    "total_units": "String",
    "used_units": "String"
  }
]
```

</td></tr><tr><td>

entitlement\_usage.​entitlement\_characteristic

</td><td>

Sys\_id of the associated entitlement characteristic record.Data type: String

Table: Entitlement Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

entitlement\_usage.​period\_end

</td><td>

Value of the period end field in the entitlement usage record. This value is the date that the usage tracking ends for this entitlement.Data type: String

</td></tr><tr><td>

entitlement\_usage.​period\_start

</td><td>

Value of the period start field in the entitlement usage record. This value is the date that the usage tracking starts for this entitlement.Data type: String

</td></tr><tr><td>

entitlement\_usage.​sys\_id

</td><td>

Sys\_id of the returned entitlement usage record.Data type: String

Table: Entitlement Usages \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

entitlement\_usage.​total\_units

</td><td>

Total number of units purchased. Data type: String

Table: In the total\_units field of the Entitlement Usages \[sn\_pss\_core\_entitlement\_usage\] table.

</td></tr><tr><td>

entitlement\_usage.​used\_units

</td><td>

Number of units that have been used.Data type: String

Table: In the used\_units field in the Entitlement Usages \[sn\_pss\_core\_entitlement\_usage\] table.

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the entitlement characteristic record.Data type: String

Table: Entitlement Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

type

</td><td>

Value of the type field in the entitlement characteristic record.Possible values:

-   coverage
-   coverage\_and\_usage

Data type: String

</td></tr><tr><td>

value

</td><td>

Coverage to give the characteristic.For some characteristics, coverages are defined in the Characteristic Option table. However, if there are no coverages defined in the Characteristic Option table, then you can pass the coverage information in the **value** parameter.

Characteristic options are only defined for the characteristic types of:

-   check box
-   choice
-   yes/no

For all other types of characteristics, the **value** parameter should contain the coverage value.

For example, if the characteristic is “Number of Replacements” and its coverages are not defined in the Characteristic Option table, you can specify the coverages, such as "10", "20", in this parameter.

**Note:** This parameter contains the final coverage value for the characteristic. If there is information in the Characteristic Option table, it is propagated to this parameter.

Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint using all of its default values.

```
curl "https://instance.servicenow.com/api/sn_ent_verify/verifyentitlements/getEntitlementCharacteristic/3c817faa43823110341605ed0bb8f23a" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Return results:

```
{
  "result": {
    "sys_id": "3c817faa43823110341605ed0bb8f23a",
    "characteristic": "b73177aa43823110341605ed0bb8f246",
    "type": "coverage",
    "characteristic_option": "ff617baa43823110341605ed0bb8f266",
    "value": "Minor parts",
    "entitlement_usage": [
      {
        "sys_id": "03e3224d51b23d10f877bf82d3ddf310",
        "period_start": "2022-12-12",
        "period_end": "2025-12-12",
        "entitlement_characteristic": "3c817faa43823110341605ed0bb8f23a",
        "total_units": "10",
        "used_units": "5"
      }
    ]
  }
}
```

### cURL request

The following code example shows how to call this endpoint and return all display values.

```
curl "https://instance.servicenow.com/api/sn_ent_verify/verifyentitlements/getEntitlementCharacteristic/3c817faa43823110341605ed0bb8f23a?display_value=all" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Return results:

```
{
  "result": {
    "sys_id": {
      "label": "Sys ID",
      "value": "3c817faa43823110341605ed0bb8f23a",
      "displayValue": "3c817faa43823110341605ed0bb8f23a",
      "type": "GUID"
    },
    "characteristic": {
      "name": "characteristic",
      "label": "Characteristic",
      "value": "b73177aa43823110341605ed0bb8f246",
      "display_value": "Repair parts covered",
      "type": "reference"
    },
    "type": {
      "name": "type",
      "label": "Type",
      "value": "coverage",
      "display_value": "Coverage",
      "type": "string"
    },
    "characteristic_option": {
      "name": "characteristic_option",
      "label": "Characteristic option",
      "value": "ff617baa43823110341605ed0bb8f266",
      "display_value": "Minor parts",
      "type": "reference"
    },
    "value": {
      "name": "value",
      "label": "Value",
      "value": "Minor parts",
      "display_value": "Minor parts",
      "type": "string"
    },
    "entitlement_usage": [
      {
        "sys_id": {
          "label": "Sys ID",
          "value": "03e3224d51b23d10f877bf82d3ddf310",
          "displayValue": "03e3224d51b23d10f877bf82d3ddf310",
          "type": "GUID"
        },
        "period_start": {
          "name": "period_start",
          "label": "Period start",
          "value": "2022-12-12",
          "display_value": "2022-12-12",
          "type": "glide_date"
        },
        "period_end": {
          "name": "period_end",
          "label": "Period end",
          "value": "2025-12-12",
          "display_value": "2025-12-12",
          "type": "glide_date"
        },
        "entitlement_characteristic": {
          "name": "entitlement_characteristic",
          "label": "Entitlement characteristic",
          "value": "3c817faa43823110341605ed0bb8f23a",
          "display_value": "Repair parts covered",
          "type": "reference"
        },
        "total_units": {
          "name": "total_units",
          "label": "Total units",
          "value": "10",
          "display_value": "10",
          "type": "string"
        },
        "used_units": {
          "name": "used_units",
          "label": "Used units",
          "value": "5",
          "display_value": "5",
          "type": "string"
        }
      }
    ]  
  }
}
```

