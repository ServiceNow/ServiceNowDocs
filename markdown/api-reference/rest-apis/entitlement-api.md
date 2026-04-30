---
title: Entitlement API
description: The Entitlement API provides endpoints to create and retrieve entitlement records from an instance.Returns the specified entitlement record, its associated coverage, and its latest usage details.Creates an entitlement record and all its related detail records.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 15
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Entitlement API

The Entitlement API provides endpoints to create and retrieve entitlement records from an instance.

Entitlement checks occur as part of post-sales support services for customers that purchase a product, such as an appliance or computer. Entitlement checks are made by agents to determine what services customers are eligible to receive for the products they've purchased. Use the Entitlement API to define and retrieve entitlements.

This API accesses and stores data in the following tables:

-   Account \[customer\_account\]
-   Consumer \[csm\_consumer\]
-   Household \[csm\_household\]
-   Install Base \[sn\_install\_base\_item\]
-   Product Model \[cmdb\_model\]
-   Product Offering \[sn\_prd\_pm\_product\_offering\]
-   Sold Product \[sn\_install\_base\_sold\_product\]

To access this API, the following plugins must be activated on the associated instance:

-   Customer Contracts and Entitlements \(com.sn\_pss\_core\) 
-   Customer Service Install Base Management \(com.snc.install\_base\)
-   Product Catalog Management Core \(com.sn\_prd\_pm\)

In addition, to successfully call this API you must have the sn\_pss\_core.pss\_integrator role. This API runs in the `sn_pss_core` namespace.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Entitlement - GET /sn\_pss\_core/entitlement/\{id\}

Returns the specified entitlement record, its associated coverage, and its latest usage details.

The following is the list of tables in which the entitlement data is stored:

-   Characteristics \[sn\_pss\_core\_entitlement\_characteristic\]
-   Entitlement \[service\_entitlement\]
-   Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]
-   Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\] - This table contains information for both sold products covered and install base items covered.

### URL format

Versioned URL: `/api/sn_pss_core/{api_version}/entitlement/{id}`

Default URL: `/api/sn_pss_core/entitlement/{id}`

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

Sys\_id of the entitlement record to retrieve.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

display\_value

</td><td>

Type of data to return.Valid values:

-   false: Return the `value` for all fields. For example, `"state":"draft"`.
-   true: Return the `display_value` for all fields. For example, `"state":"Draft"`
-   all: Return all information for all fields.

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
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td>

Sys\_id of the account record to which the entitlement belongs.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

consumer

</td><td>

Sys\_id of the consumer record to which the entitlement belongs.

Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

contract

</td><td>

Sys\_id of the contract record to which the entitlement belongs.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

end\_date

</td><td>

End date of the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

entitlement\_characteristics

</td><td>

List of characteristics associated with the entitlement.Data type: Array of Objects

```
"entitlement_characteristics" [
  {
    "characteristic": "String",
    "characteristic_option": "String",
    "entitlement": "String",
    "entitlement_usage": [Array],
    "service_contract_line": "String",
    "sys_created_by": "String",
    "sys_created_on": "String",
    "sys_id": "String",
    "sys_updated_by": "String",
    "sys_updated_on": "String",
    "type": "String",
    "value": "String"
  }
]
```

Stored in: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

entitlement\_characteristics.​characteristic

</td><td>

Sys\_id of the characteristic record associated with the entitlement.

Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

entitlement\_characteristics.​characteristic\_option

</td><td>

Sys\_id of the characteristic option record associated with the entitlement.Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

entitlement\_characteristics.​entitlement

</td><td>

Sys\_id of the associated entitlement record.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage

</td><td>

List of entitlement usages associated with the entitlement characteristic.Data type: Array of Objects

```
"entitlement_usage": [
  {
    "entitlement": "String",
    "entitlement_characteristic": "String",
    "period_end": "String",
    "period_start": "String",
    "service_contract_line": "String",
    "sys_created_by": "String",
    "sys_created_on": "String",
    "sys_id": "String",
    "sys_updated_by": "String",
    "sys_updated_on": "String",
    "total_units": "String",
    "used_units": "String"
  }
]
```

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the entitlement usage.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage.​entitlement\_characteristic

</td><td>

Sys\_id of the entitlement characteristic record associated with the entitlement usage.Data type: String

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage.​period\_end

</td><td>

End date when the entitlement usage is no longer tracked.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage.​period\_start

</td><td>

Starting date of when the entitlement usage is tracked.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage.​service\_contract\_line

</td><td>

Sys\_id of the service contract line to which the current entitlement usage belongs. Data type: String

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage.​sys\_created\_by

</td><td>

Name of the user that created the entitlement usage record.Data type: String

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage.​sys\_created\_on

</td><td>

Date and time that the entitlement usage record was created.Data type: String

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage.​sys\_id

</td><td>

Sys\_id of the entitlement usage record.Data type: String

Table: Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage.​sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement usage record.Data type: String

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage.​sys\_updated\_on

</td><td>

Date and time that the entitlement usage record was last updated.Data type: String

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage.​total\_units

</td><td>

Total coverage value of the associated entitlement characteristic.Data type: String

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage.​used\_units

</td><td>

Number of units used by the account or consumer between the **period\_start** and the **period\_end**.Data type: String

</td></tr><tr><td>

entitlement\_characteristics.​type

</td><td>

Type of entitlement characteristic. Valid values:

-   coverage
-   coverage\_and\_usage

Data type: String

</td></tr><tr><td>

entitlement\_characteristics.​value

</td><td>

Value of the characteristic.

Data type: String

</td></tr><tr><td>

entitlement\_name

</td><td>

Name of the entitlement.

Data type: String

</td></tr><tr><td>

household

</td><td>

Sys\_id of the household record associated with the entitlement.

Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

install\_base\_items\_covered

</td><td>

List of install base items covered under the  entitlement.Data type: Array of Objects

```
 "install_base_items_covered": [ 
  {
    "added": "String",
    "contract": "String",
    "entitlement": "String",
    "install_base": "String",
    "removed": "String",
    "service_contract_line": "String",
    "sys_created_by": "String",
    "sys_created_on": "String",
    "sys_id": "String",
    "sys_updated_by": "String",
    "sys_updated_on": "String"
  }
]
```

Table: Sold Product Covered  \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

install\_base\_items\_covered.​added

</td><td>

Date that the associated install base item was added to the entitlement.Data type: String

</td></tr><tr><td>

install\_base\_items\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the install base item.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the install base item covered by the service contract line.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

install\_base\_items\_covered.​removed

</td><td>

Date that the associated install base item was removed from the entitlement.Data type: String

</td></tr><tr><td>

install\_base\_items\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the install base item.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

install\_base\_items\_covered.​service\_contract\_line

</td><td>

Sys\_id of the associated service contract line record.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

install\_base\_items\_covered.​sys\_created\_by

</td><td>

Name of the user that created the install base item record.Data type: String

</td></tr><tr><td>

install\_base\_items\_covered.​sys\_created\_on

</td><td>

Date and time that the install base item record was created.Data type: String

</td></tr><tr><td>

install\_base\_items\_covered.​sys\_id

</td><td>

Sys\_id of the install base item covered.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

install\_base\_items\_covered.​sys\_updated\_by

</td><td>

Name of the user that last updated the install base item record.Data type: String

</td></tr><tr><td>

install\_base\_items\_covered.​sys\_updated\_on

</td><td>

Date and time that the install base item record was last updated.Data type: String

</td></tr><tr><td>

product

</td><td>

Sys\_id of the product model record associated with the entitlement.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

product\_offering

</td><td>

Sys\_id of the product offering record associated with the entitlement.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

sold\_entitlement

</td><td>

Sys\_id of the sold product record associated with the entitlement.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

sold\_products\_covered

</td><td>

List of products covered.Data type: Array of Objects

```
"sold_products_covered": [ 
  {
    "added": "String",
    "contract": "String",
    "entitlement": "String",
    "removed": "String",
    "service_contract_line": "String",
    "sold_product": "String",
    "sys_created_by": "String",
    "sys_created_on": "String",
    "sys_id": "String",
    "sys_updated_by": "String",
    "sys_updated_on": "String"
  }
]
```

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

sold\_products\_covered.​added

</td><td>

Date that the associated sold product was added to the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

sold\_products\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the sold product covered.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

sold\_products\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the sold product covered.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

sold\_products\_covered.removed

</td><td>

Date that the associated sold product was removed from the entitlement.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

sold\_products\_covered.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the sold product covered.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

sold\_products\_covered.​sold\_product

</td><td>

Sys\_id of the product covered by the entitlement.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

sold\_products\_covered.​sys\_created\_by

</td><td>

Name of the user that created the sold product covered record.Data type: String

</td></tr><tr><td>

sold\_products\_covered.​sys\_created\_on

</td><td>

Date and time that the sold product covered record was created.Data type: String

</td></tr><tr><td>

sold\_products\_covered.​sys\_id

</td><td>

Sys\_id of the product covered by this service contract.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

sold\_products\_covered.​sys\_updated\_by

</td><td>

Name of the user that last updated the sold product covered record.Data type: String

</td></tr><tr><td>

sold\_products\_covered.​sys\_updated\_on

</td><td>

Date and time that the sold product covered record was last updated.Data type: String

</td></tr><tr><td>

start\_date

</td><td>

Start date of the entitlement.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

state

</td><td>

Current state of the entitlement.

Valid values: \(case-sensitive\)

-   active
-   cancelled
-   draft
-   expired
-   suspended

Data type: String

</td></tr><tr><td>

sys\_created\_by

</td><td>

Name of the user that created the entitlement record.Data type: String

</td></tr><tr><td>

sys\_created\_on

</td><td>

Date and time that the entitlement record was created.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the associated entitlement record.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement record.Data type: String

</td></tr><tr><td>

sys\_updated\_on

</td><td>

Date and time that the entitlement record was created.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to call this endpoint to retrieve an entitlement template.

```
curl "https://instance.servicenow.com/api/sn_pss_core/entitlement/fc73d2de89226110f877430a4e008" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Response:

```
{
  "result": {
    "sys_id": "5a651515d1f53110f8776589fa411f7b",
    "sys_created_by": "admin",
    "sys_updated_by": "admin",
    "sys_created_on": "2023-10-09 11:31:59",
    "sys_updated_on": "2023-10-09 11:31:59",
    "entitlement_name": "indep entl",
    "account": "4c325111d1f53110f8776589fa411f3d",
    "consumer": null,
    "household": null,
    "contract": null,
    "service_contract_line": null,
    "state": "active",
    "product_offering": null,
    "sold_entitlement": null,
    "product": null,
    "start_date": "2023-10-03",
    "end_date": "2024-12-03",
    "sold_products_covered": [
      {
        "sys_id": "d6651515d1f53110f8776589fa411f7c",
        "sys_created_by": "admin",
        "sys_updated_by": "admin",
        "sys_created_on": "2023-10-09 11:31:59",
        "sys_updated_on": "2023-10-09 11:31:59",
        "contract": null,
        "service_contract_line": null,
        "entitlement": "5a651515d1f53110f8776589fa411f7b",
        "sold_product": "0df21151d1f53110f8776589fa411f1b",
        "added": "",
        "removed": ""
      }
    ],
    "install_base_items_covered": [
      {
        "sys_id": "12651515d1f53110f8776589fa411f7d",
        "sys_created_by": "admin",
        "sys_updated_by": "admin",
        "sys_created_on": "2023-10-09 11:31:59",
        "sys_updated_on": "2023-10-09 11:31:59",
        "contract": null,
        "service_contract_line": null,
        "entitlement": "5a651515d1f53110f8776589fa411f7b",
        "install_base": "e2639951d1f53110f8776589fa411f2b",
        "added": "",
        "removed": ""
      }
    ],
    "entitlement_characteristics": [
      {
        "sys_id": "12651515d1f53110f8776589fa411f7e",
        "sys_created_by": "admin",
        "sys_updated_by": "admin",
        "sys_created_on": "2023-10-09 11:31:59",
        "sys_updated_on": "2023-10-09 11:31:59",
        "service_contract_line": null,
        "entitlement": "5a651515d1f53110f8776589fa411f7b",
        "characteristic_option": "495149b7539e61106bfcddeeff7b1262",
        "value": "5",
        "characteristic": "63418db7539e61106bfcddeeff7b1238",
        "type": "coverage_and_usage",
        "entitlement_usage": [
          {
            "sys_id": "de651515d1f53110f8776589fa411f7e",
            "sys_created_by": "admin",
            "sys_updated_by": "admin",
            "sys_created_on": "2023-10-09 11:31:59",
            "sys_updated_on": "2023-10-09 11:31:59",
            "entitlement": "5a651515d1f53110f8776589fa411f7b",
            "service_contract_line": null,
            "entitlement_characteristic": "12651515d1f53110f8776589fa411f7e",
            "period_start": "2023-10-03",
            "period_end": "2024-12-03",
            "total_units": "5",
            "used_units": "25"
          }
        ]
      }
    ]
  }
}
```

## Entitlement - POST /sn\_pss\_core/entitlement

Creates an entitlement record and all its related detail records.

The following is the list of tables in which the entitlement data is stored:

-   Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]
-   Entitlement \[service\_entitlement\]
-   Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]
-   Sold Products Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\] - This table contains information for both sold products covered and install base items covered.

### URL format

Versioned URL: `/api/sn_pss_core/{api_version}/entitlement`

Default URL: `/api/sn_pss_core/entitlement`

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

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td>

Required if the **consumer** parameter is not passed.Sys\_id of the account record to which the entitlement belongs.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

consumer

</td><td>

Required if the **account** parameter is not passed. Sys\_id of the consumer record to which the entitlement belongs.

Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

end\_date

</td><td>

End date of the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

entitlement\_characteristics

</td><td>

List of characteristics associated with the entitlement.Data type: Array of Objects

```
"entitlement_characteristics": [
  {
    "characteristic": "String",
    "characteristic_option": "String",
    "entitlement_usage": {Object},
    "type": "String",
    "value": "String"
  }
]
```

Stored in: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

entitlement\_characteristics.​characteristic

</td><td>

Required. Sys\_id of the characteristic record associated with the entitlement.

Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

entitlement\_characteristics.​characteristic\_option

</td><td>

Sys\_id of the characteristic option record associated with the entitlement.Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage

</td><td>

Used unit value for the associated entitlement characteristic.Only pass this parameter if the entitlement\_characteristics are under the entitlement.

Data type: Object

```
"entitlement_usage": {
    "used_units": "String"
}
```

Stored in: Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage.​usage\_units

</td><td>

Usage of the associated entitlement characteristic.Data type: String

</td></tr><tr><td>

entitlement\_characteristics.​type

</td><td>

Type of entitlement characteristic. Valid values:

-   coverage
-   coverage\_and\_usage

Data type: String

</td></tr><tr><td>

entitlement\_characteristics.​value

</td><td>

Required if the **input\_type** parameter contained in the record specified in the **entitlement\_characteristics.characteristic** parameter, is not `choice`.Value of the characteristic.

Data type: String

</td></tr><tr><td>

entitlement\_name

</td><td>

Required. Name of the entitlement.

Data type: String

</td></tr><tr><td>

household

</td><td>

Only passed when the household plugins are active and the **consumer** parameter is passed. Sys\_id of the household record associated with the entitlement.

Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

install\_base\_items\_covered

</td><td>

List of install base items covered under the entitlement. The information in this array is inserted in the Sold Product Covered  \[sn\_install\_base\_m2m\_contract\_sold\_product\] table.

Data type: Array of Objects

 ```
"install_base_items_covered": [ 
  {
    "added": "String",
    "install_base": "String",
    "removed": "String"
  }
]
```

 For more information on Install Base Items [Configure Install base](https://www.servicenow.com/docs/access?context=configure-install-base&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

</td></tr><tr><td>

install\_base\_items\_covered.added

</td><td>

Date that the associated install base item was added to the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the associated install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

install\_base\_items\_covered.​removed

</td><td>

Date that the associated install base item was removed from the entitlement.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

product

</td><td>

Sys\_id of the product model record associated with the entitlement.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

product\_offering

</td><td>

Sys\_id of the product offering record associated with the entitlement.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

sold\_entitlement

</td><td>

Sys\_id of the sold product record associated with the entitlement.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

sold\_products\_covered

</td><td>

List of products covered under the entitlement.Data type: Array of Objects

```
"sold_products_covered": [ 
  {
    "added": "String",
    "removed": "String",
    "sold_product": "String"
  }
]
```

Stored in: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

sold\_products\_covered.added

</td><td>

Date that the associated sold product was added to the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

sold\_products\_covered.removed

</td><td>

Date that the associated sold product was removed from the entitlement.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

sold\_products\_covered.sold\_product

</td><td>

Sys\_id of the product covered by the entitlement.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

start\_date

</td><td>

Required. Start date of the entitlement.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

state

</td><td>

Required.Current state of the entitlement.

Valid values: \(case-sensitive\)

-   active
-   cancelled
-   draft
-   expired
-   suspended

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_cdz_2rp_4xb" class="rest_api_request_headers"><thead><tr><th>

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

|Status code|Description|
|-----------|-----------|
|201|Successful. The request was successfully processed and the records were created.|
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have permission to access the API.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

entitlement\_characteristics

</td><td>

List of the entitlement characteristic objects  created under the entitlement. Data type: Array of Objects

```
"entitlement_characteristics" [
  {
    "entitlement_usage": {Object},
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage

</td><td>

Entitlement usage object inserted under the entitlement\_characteristic.Data type: Object

```
"entitlement_usage": {
    "sys_id": "String"
}
```

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage.​sys\_id

</td><td>

Sys\_id of the entitlement usage record.Data type: String

Table: Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

entitlement\_characteristics.​sys\_id

</td><td>

Sys\_id of a entitlement characteristics record associated with the entitlement.Data type: String

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

entitlement\_name

</td><td>

Name of the entitlement.

Data type: String

</td></tr><tr><td>

install\_base\_items\_covered

</td><td>

List of sys\_ids of the install base items covered under the entitlement. Data type: Array of Objects

```
"install_base_items_covered": [ 
  {
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

install\_base\_items\_covered.​sys\_id

</td><td>

Sys\_id of a install base items covered by the entitlement.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

sold\_prodocts\_covered

</td><td>

List of sys\_ids of the products covered under the entitlement. Data type: Array of Objects

```
"sold_products_covered": [ 
  {
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

sold\_products\_covered.​sys\_id

</td><td>

Sys\_id of a product associated with the entitlement.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the associated entitlement record.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr></tbody>
</table>### cURL request

The following example shows how to create an entitlement template.

```
curl "https://instance.servicenow.com/api/sn_pss_core/entitlement" \
--request POST \
--header "Accept:application/json" \
--data
{
  "state": "active",
  "entitlement_name": "indep entl",
  "account": "4c325111d1f53110f8776589fa411f3d",
  "start_date": "2023-10-03",
  "end_date": "2024-12-03",
  "sold_products_covered": [
    {
      "sold_product": "0df21151d1f53110f8776589fa411f1b"
    }
  ], 
  "install_base_items_covered": [
    {
      "install_base": "e2639951d1f53110f8776589fa411f2b"
    }
  ],
  "entitlement_characteristics": [
    {
      "characteristic": "63418db7539e61106bfcddeeff7b1238",
      "characteristic_option": "495149b7539e61106bfcddeeff7b1262",
      "value": "20",
      "type": "coverage_and_usage",
      "entitlement_usage": {
        "used_units": "25"
      } 
    }
  ]
}
```

Response:

```
{
  "result": {
    "sys_id": "5a651515d1f53110f8776589fa411f7b",
    "entitlement_name": "indep entl",
    "sold_products_covered": [
      {
        "sys_id": "d6651515d1f53110f8776589fa411f7c"
      }
    ],
    "install_base_items_covered": [
      {
        "sys_id": "12651515d1f53110f8776589fa411f7d"
      }
    ],
    "entitlement_characteristics": [
      {
        "sys_id": "12651515d1f53110f8776589fa411f7e",
        "entitlement_usage": {
          "sys_id": "de651515d1f53110f8776589fa411f7e"
        }
      }
    ]
  }
}
```

