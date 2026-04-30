---
title: Service Contract API
description: The Service Contract API provides endpoints to create and retrieve service contract records.Retrieves a specified service contract record.Retrieves the details of a specified service contract line record and its related entities.Creates a service contract record and all its related entities from a specified payload.Creates a contract line record and all of its related entities.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 103
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Service Contract API

The Service Contract API provides endpoints to create and retrieve service contract records.

**Note:** This API is for creating data in the tables for the Customer Contracts and Entitlements application. It is not a general purpose API.

To access this API the following plugins must be activated on the associated instance:

-   Customer Contracts and Entitlements \(com.sn\_pss\_core\)
-   Customer Service Install Base Management \(com.snc.install\)
-   Product Catalog Management Core \(com.sn\_prd\)

In addition, to successfully call this API you must have the sn\_pss\_core.pss\_integrator role. This API runs in the `sn_pss_core` namespace.

Before using this API, you should have associated data in the following tables. For additional information, see [Create service contracts](https://www.servicenow.com/docs/access?context=create-csm-service-contracts&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

-   Account \[customer\_account\]
-   Consumer \[csm\_consumer\]
-   Household \[csm\_household\]
-   Install Base \[sn\_install\_base\_item\]
-   Product Specification \[sn\_prd\_pm\_product\_specification\]
-   Product Offering \[sn\_prd\_pm\_product\_offering\]
-   Product Model \[cmdb\_model\]
-   Sold Product \[sn\_install\_base\_sold\_product\]

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Service Contract - GET /sn\_pss\_core/servicecontract/\{id\}

Retrieves a specified service contract record.

This endpoint retrieves data from the following tables when processing the request:

-   Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]
-   Entitlement \[service\_entitlement\]
-   Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]
-   Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\] - This table contains information for both sold products covered and install base items covered.
-   Service Contract \[sn\_pss\_core\_service\_contract\]
-   Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

### URL format

Versioned URL: `/api/sn_pss_core/{api_version}/servicecontract/{id}`

Default URL: `/api/sn_pss_core/servicecontract/{id}`

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

Sys\_id of the service contract to retrieve.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

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
|403|Forbidden. The user doesn't have permission to access the API.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td>

Sys\_id of the account record to which the service contract belongs.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

consumer

</td><td>

Sys\_id of the consumer record to which the service contract belongs.

Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

ends

</td><td>

Date on which the service contract ends.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

household

</td><td>

Sys\_id of the household associated with the service contract.

Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

install\_base\_items\_covered

</td><td>

List of install base items covered under the service contract line.Data type: Array of Objects

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

</td></tr><tr><td>

install\_base\_items\_covered.​added

</td><td>

Date that the associated service contract starts to cover the install base item.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

install\_base\_items\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the install base item.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

install\_base\_items\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the install base item.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the associated install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

install\_base\_items\_covered.​removed

</td><td>

Date that the associated service contract ends coverage of the install base item.

Data type: String

Format: yyyy-mm-dd

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

number

</td><td>

Auto-generated service contract number.Data type: String

</td></tr><tr><td>

service\_contract\_lines

</td><td>

List of service contract lines \(services\) associated with the service contract. Data type: Array of Objects

```
"service_contract_lines": [
  {
    "child_contract_lines": [Array],
    "contract": "String",
    "ends": "String",
    "entitlements": [Array],
    "entitlement_characteristics": [Array],
    "install_base_items_covered": [Array],
    "name": "String",
    "number": "String",
    "parent_contract_line": "String",
    "product_model": "String",
    "product_offering": "String",
    "product_specification": "String",
    "sold_product": "String",
    "sold_products_covered": [Array],
    "starts": "String",
    "state": "String",
    "sys_created_by": "String",
    "sys_created_on": "String",
    "sys_id": "String",
    "sys_updated_by": "String",
    "sys_update_on": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines

</td><td>

List of child service contract lines associated with the service contract line.Data type: Array of Objects

```
"child_contract_lines": [
  {
    "child_contract_lines": [Array],
    "contract": "String",
    "ends": "String",
    "entitlements": [Array],
    "entitlement_characteristics": [Array],
    "install_base_items_covered": [Array],
    "name": "String",
    "number": "String",
    "parent_contract_line": "String",
    "product_model": "String",
    "product_offering": "String",
    "product_specification": "String",
    "sold_product": "String",
    "sold_products_covered": [Array],
    "starts": "String",
    "state": "String",
    "sys_created_by": "String",
    "sys_created_on": "String",
    "sys_id": "String",
    "sys_updated_by": "String",
    "sys_update_on": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​child\_contract\_lines

</td><td>

List of child service contract lines associated with the child service contract line. Same parameters as in **child\_contract\_lines**.Data type: Array

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​contract

</td><td>

Sys\_id of the service contract associated with the child service contract line.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​ends

</td><td>

Date on which the child service contract line ends.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements

</td><td>

List of entitlements associated with the child service contract line.Data type: Array of Objects

```
"entitlements": [
  {
    "account": "String",
    "consumer": "String",
    "contract": "String",
    "end_date": "String",
    "entitlement_characteristics": [Array],
    "entitlement_name": "String",
    "household": "String",
    "install_base_items_covered": [Array],
    "product": "String",
    "product_offering": "String",
    "product_specification": "String",
    "service_contract_line": "String",
    "sold_entitlement": "String",
    "sold_products_covered": [Array],
    "start_date": "String",
    "state": "String",
    "sys_created_by": "String",
    "sys_created_on": "String",
    "sys_id": "String",
    "sys_updated_by": "String",
    "sys_updated_on": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​account

</td><td>

Sys\_id of the account record to which the entitlement belongs.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​consumer

</td><td>

Sys\_id of the consumer record to which the entitlement belongs.

Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​contract

</td><td>

Sys\_id of the contract record to which the entitlement belongs.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​end\_date

</td><td>

End date of the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics

</td><td>

List of characteristics associated with the entitlement. Data type: Array of Objects

```
"entitlement_characteristics": [
  {
    "characteristic": "String",
    "characteristic_option": "String",
    "entitlement": "String",
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

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​characteristic

</td><td>

Sys\_id of the characteristic record associated with the entitlement.

Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​characteristic\_option

</td><td>

Sys\_id of the characteristic option record associated with the entitlement.Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement

</td><td>

Sys\_id of the entitlement record.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage

</td><td>

List of usage values for the associated product.Data type: Array of Objects

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
    "sys_update_on": "String",
    "total_units": "String",
    "used_units": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the entitlement usage.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​entitlement\_characteristic

</td><td>

Sys\_id of the entitlement characteristic record associated with the entitlement usage.Data type: String

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​period\_end

</td><td>

End date when the entitlement usage is no longer tracked.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​period\_start

</td><td>

Starting date of when the entitlement usage is tracked.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​service\_contract\_line

</td><td>

Sys\_id of the service contract line to which the current entitlement usage belongs.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_created\_by

</td><td>

Name of the user that created the entitlement usage record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_created\_on

</td><td>

Date and time that the entitlement usage record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_id

</td><td>

Sys\_id of the entitlement usage record.Data type: String

Table: Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement usage record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_updated\_on

</td><td>

Date and time that the entitlement usage record was last updated.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​total\_units

</td><td>

Total coverage value of the associated entitlement characteristic.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​used\_units

</td><td>

Number of units used by the account or consumer between the **period\_start** and the **period\_end**.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​service\_contract\_line

</td><td>

Child contract line to which the current entitlement characteristic belongs to. Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​sys\_created\_by

</td><td>

Name of the user who created the entitlement characteristic.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​sys\_created\_on

</td><td>

Date and time when the entitlement characteristic was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​sys\_id

</td><td>

Sys\_id of the entitlement characteristic record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​sys\_updated\_by

</td><td>

Name of the user who last updated the entitlement characteristic.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​sys\_updated\_on

</td><td>

Date and time when the entitlement characteristic was last updated.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​type

</td><td>

Type of entitlement characteristic. Valid values:

-   coverage
-   coverage\_and\_usage

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​value

</td><td>

Value of the characteristic.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_name

</td><td>

Name of the entitlement.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​household

</td><td>

Sys\_id of the household record associated with the entitlement.

Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered

</td><td>

List of install base items covered under the  child service contract line.Data type: Array of Objects

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

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​added

</td><td>

Date that the associated install base item was added to the service contract line.

Data type: String

 Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the install base item.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the install base item.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the associated install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​removed

</td><td>

Date that the associated service contract line ends coverage of the install base item.

Data type: String

 Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​service\_contract\_line

</td><td>

Sys\_id of the associated service contract line record.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_created\_by

</td><td>

Name of the user that created the install base item record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_created\_on

</td><td>

Date and time that the install base item record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_id

</td><td>

Sys\_id of the install base item covered.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_updated\_by

</td><td>

Name of the user that last updated the install base item record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_updated\_on

</td><td>

Date and time that the install base item record was last updated.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​product

</td><td>

Sys\_id of the product model record associated with the entitlement.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​product\_offering

</td><td>

Sys\_id of the product offering record associated with the entitlement.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​product\_specification

</td><td>

Sys\_id of the product specification record associated with the entitlement.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the entitlement.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_entitlement

</td><td>

Sys\_id of the sold product record associated with the entitlement.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_products\_covered

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

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_products\_covered.​added

</td><td>

Date that the associated service contract starts to cover the product.

Data type: String

 Format: yyyy-mm-dd

 Default: Current date

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_products\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the sold product covered.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_products\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the sold product covered.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_products\_covered.​removed

</td><td>

Date that the associated service contract ends coverage of the associated product.

Data type: String

 Format: yyyy-mm-dd

 Default: No end date

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_products\_covered.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the sold product covered.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_products\_covered.​sold\_product

</td><td>

Sys\_id of the product covered by the service contract.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_products\_covered.​sys\_created\_by

</td><td>

Name of the user that created the sold product covered record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered.​sys\_created\_on

</td><td>

Date and time that the sold product covered record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_products\_covered.​sys\_id

</td><td>

Sys\_id of the product covered by this service contract.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_products\_covered.​sys\_updated\_by

</td><td>

Name of the user that last updated the sold product covered record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_products\_covered.​sys\_updated\_on

</td><td>

Name of the user that last updated the sold product covered record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​start\_date

</td><td>

Start date of the entitlement.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​state

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

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sys\_created\_by

</td><td>

Name of the user that created the entitlement record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sys\_created\_on

</td><td>

Date and time that the entitlement record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sys\_id

</td><td>

Sys\_id of the associated entitlement record.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sys\_updated\_on

</td><td>

Date and time that the entitlement record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics

</td><td>

List of characteristics associated with the entitlement.Data type: Array of Objects

```
"entitlement_characteristics": [
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
    "sys_updated_on": "String"
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.​characteristic

</td><td>

Sys\_id of the characteristic record associated with the entitlement.

Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.​characteristic\_option

</td><td>

Sys\_id of the characteristic option record associated with the entitlement.Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.​entitlement

</td><td>

Sys\_id of the entitlement record.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the entitlement characteristic.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.​sys\_created\_by

</td><td>

Name of the user that created the entitlement characteristics record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.​sys\_created\_on

</td><td>

Date and time that the entitlement characteristics record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.​sys\_id

</td><td>

Sys\_id of the entitlement characteristics record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.​sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement characteristics record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.​sys\_updated\_on

</td><td>

Date and time that the entitlement characteristics record was last updated.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.​type

</td><td>

Type of entitlement characteristic. Valid values:

-   coverage
-   coverage\_and\_usage

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.​value

</td><td>

Value of the characteristic.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered

</td><td>

List of install base items covered under the  child service contract line.Data type: Array of Objects

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

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered.​added

</td><td>

Date that the associated install base item was added to the service contract line.

Data type: String

 Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the install base item.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the install base item.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the associated install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered.​removed

</td><td>

Date that the associated service contract line ends coverage of the install base item.

Data type: String

 Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered.​service\_contract\_line

</td><td>

Sys\_id of the associated service contract line record.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered.​sys\_created\_by

</td><td>

Name of the user that created the install base item record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered.​sys\_created\_on

</td><td>

Date and time that the install base item record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered.​sys\_id

</td><td>

Sys\_id of the install base item covered.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered.​sys\_updated\_by

</td><td>

Name of the user that last updated the install base item record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered.​sys\_updated\_on

</td><td>

Date and time that the install base item record was last updated.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​name

</td><td>

Name of the child service contract line.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​parent\_contract\_line

</td><td>

Sys\_id of the parent contract line record associated with the child service contract line.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​product\_model

</td><td>

Sys\_id of the product associated with the child service contract line.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​product\_offering

</td><td>

Sys\_id of the product offering record associated with the child service contract line.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_product

</td><td>

Sys\_id of the sold product record associated with the child service contract line.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered

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

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered.​added

</td><td>

Date that the associated service contract starts to cover the product.

Data type: String

 Format: yyyy-mm-dd

 Default: Current date

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the sold product covered.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the sold product covered.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered.​removed

</td><td>

Date that the associated service contract ends coverage of the associated product.

Data type: String

 Format: yyyy-mm-dd

 Default: No end date

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the sold product covered.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered.​sold\_product

</td><td>

Sys\_id of the product covered by the service contract.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered.​sys\_created\_by

</td><td>

Name of the user that created the sold product covered record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered.​sys\_created\_on

</td><td>

Date and time that the sold product covered record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered.​sys\_id

</td><td>

Sys\_id of the product covered by this service contract.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered.​sys\_updated\_by

</td><td>

Name of the user that last updated the sold product covered record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered.​sys\_updated\_on

</td><td>

Name of the user that last updated the sold product covered record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​starts

</td><td>

Start date of the child service contract line.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sys\_created\_by

</td><td>

Name of the user that created the child service contract line record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sys\_created\_on

</td><td>

Date and time that the child service contract line record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sys\_id

</td><td>

Sys\_id of a child service contract line record.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sys\_updated\_by

</td><td>

Name of the user that last updated the child service contract line record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sys\_updated\_on

</td><td>

Date and time that the child service contract line record was last updated.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​contract

</td><td>

Sys\_id of the service contract associated with the service contract line.

Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

service\_contract\_lines.​ends

</td><td>

Date on which the service contract line ends.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

service\_contract\_lines.​entitlements

</td><td>

List of entitlements associated with the service contract.Data type: Array of Objects

```
"entitlements": [
  {
    "account": "String",
    "consumer": "String",
    "contract": "String",
    "end_date": "String",
    "entitlement_characteristics": [Array],
    "entitlement_name": "String",
    "household": "String",
    "install_base_items_covered": [Array],
    "product": "String",
    "product_offering": "String",
    "product_specification": "String",
    "service_contract_line": "String",
    "sold_entitlement": "String",
    "sold_products_covered": [Array],
    "start_date": "String",
    "state": "String",
    "sys_created_by": "String",
    "sys_created_on": "String",
    "sys_id": "String",
    "sys_updated_by": "String",
    "sys_updated_on": "String"
  }
]
```

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​account

</td><td>

Sys\_id of the account record to which the entitlement belongs.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​consumer

</td><td>

Sys\_id of the consumer record to which the entitlement belongs.

Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​contract

</td><td>

Sys\_id of the contract record to which the entitlement belongs.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​end\_date

</td><td>

End date of the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics

</td><td>

List of characteristics associated with the entitlement.Data type: Array of Objects

```
"entitlement_characteristics": [
  {
    "characteristic": "String",
    "characteristic_option": "String",
    "entitlement": "String",
    "entitlement_usage": [Array]
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

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.characteristic

</td><td>

Sys\_id of the characteristic record associated with the entitlement.

Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.characteristic\_option

</td><td>

Sys\_id of the characteristic option record associated with the entitlement.Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement

</td><td>

Sys\_id of the associated entitlement record.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage

</td><td>

List of usage values for the associated product.Data type: Array of Objects

```
"entitlement_usage": [
  {
    "entitlement": "String",
    "entitlement_characteristic": "String",
    "period_end": "String",
    "period_start": "String",
    "sys_created_by": "String",
    "sys_created_on": "String",
    "sys_id": "String",
    "sys_updated_by": "String",
    "sys_update_on": "String",
    "total_units": "String",
    "used_units": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the entitlement usage.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​entitlement\_characteristic

</td><td>

Sys\_id of the entitlement characteristic record associated with the entitlement usage.Data type: String

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​period\_end

</td><td>

End date when the entitlement usage is no longer tracked.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​period\_start

</td><td>

Starting date of when the entitlement usage is tracked.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_created\_by

</td><td>

Name of the user that created the entitlement usage record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_created\_on

</td><td>

Date and time that the entitlement usage record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_id

</td><td>

Sys\_id of the entitlement usage record.Data type: String

Table: Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement usage record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_updated\_on

</td><td>

Date and time that the entitlement usage record was last updated.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​total\_units

</td><td>

Total coverage value of the associated entitlement characteristic.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​used\_units

</td><td>

Number of units used by the account or consumer between the **period\_start** and the **period\_end**.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the entitlement characteristic.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​sys\_created\_by

</td><td>

Name of the user that created the entitlement characteristics record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​sys\_created\_on

</td><td>

Date and time that the entitlement characteristics record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​sys\_id

</td><td>

Sys\_id of the entitlement characteristics record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement characteristics record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​sys\_updated\_on

</td><td>

Date and time that the entitlement characteristics record was last updated.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.type

</td><td>

Type of entitlement characteristic. Valid values:

-   coverage
-   coverage\_and\_usage

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​value

</td><td>

Value of the characteristic.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_name

</td><td>

Name of the entitlement.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​household

</td><td>

Sys\_id of the household record associated with the entitlement.

Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​install\_base\_items\_covered

</td><td>

List of install base items covered under the service contract line.Data type: Array of Objects

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

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​install\_base\_items\_covered.​added

</td><td>

Date that the associated install base item was added to the entitlement.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​install\_base\_items\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the install base item.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​install\_base\_items\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the install base item.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the associated install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​install\_base\_items\_covered.​removed

</td><td>

Date that the associated install base item was removed from the entitlement.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​install\_base\_items\_covered.​service\_contract\_line

</td><td>

Sys\_id of the associated service contract line record.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_created\_by

</td><td>

Name of the user that created the install base item record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_created\_on

</td><td>

Date and time that the install base item record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_id

</td><td>

Sys\_id of the install base item covered.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_updated\_by

</td><td>

Name of the user that last updated the install base item record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_updated\_on

</td><td>

Date and time that the install base item record was last updated.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​product

</td><td>

Sys\_id of the product model record associated with the entitlement.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​product\_offering

</td><td>

Sys\_id of the product offering record associated with the entitlement.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​product\_specification

</td><td>

Sys\_id of the product specification record associated with the entitlement.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the entitlement.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_entitlement

</td><td>

Sys\_id of the sold product record associated with the entitlement.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_products\_covered

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

service\_contract\_lines.​entitlements.​sold\_products\_covered.​added

</td><td>

Date that the associated sold product was added to the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_products\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the sold product covered.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_products\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the sold product covered.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_products\_covered.removed

</td><td>

Date that the associated sold product was removed from the entitlement.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_products\_covered.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the sold product covered.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_products\_covered.​sold\_product

</td><td>

Sys\_id of the product covered by the entitlement.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_products\_covered.​sys\_created\_by

</td><td>

Name of the user that created the sold product covered record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_products\_covered.​sys\_created\_on

</td><td>

Date and time that the sold product covered record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_products\_covered.​sys\_id

</td><td>

Sys\_id of the product covered by this service contract.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_products\_covered.​sys\_updated\_by

</td><td>

Name of the user that last updated the sold product covered record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_products\_covered.​sys\_updated\_on

</td><td>

Date and time that the sold product covered record was last updated.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​start\_date

</td><td>

Start date of the entitlement.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​state

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

service\_contract\_lines.​entitlements.​sys\_created\_by

</td><td>

Name of the user that created the entitlement record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sys\_created\_on

</td><td>

Date and time that the entitlement record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sys\_id

</td><td>

Sys\_id of the associated entitlement record.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sys\_updated\_on

</td><td>

Date and time that the entitlement record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics

</td><td>

List of characteristics associated with the service contract line.Data type: Array of Objects

```
"entitlement_characteristics": [
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

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.characteristic

</td><td>

Sys\_id of the characteristic record associated with the entitlement.

Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.characteristic\_option

</td><td>

Sys\_id of the characteristic option record associated with the entitlement.Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​entitlement

</td><td>

Sys\_id of the associated entitlement record.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage

</td><td>

List of usage values for the associated product.Data type: Array of Objects

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
    "sys_update_on": "String",
    "total_units": "String",
    "used_units": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the entitlement usage.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​entitlement\_characteristic

</td><td>

Sys\_id of the entitlement characteristic record associated with the entitlement usage.Data type: String

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​period\_end

</td><td>

End date when the entitlement usage is no longer tracked.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​period\_start

</td><td>

Starting date of when the entitlement usage is tracked.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​sys\_created\_by

</td><td>

Name of the user that created the entitlement usage record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​sys\_created\_on

</td><td>

Date and time that the entitlement usage record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​sys\_id

</td><td>

Sys\_id of the entitlement usage record.Data type: String

Table: Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement usage record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​sys\_updated\_on

</td><td>

Date and time that the entitlement usage record was last updated.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​total\_units

</td><td>

Total number of units purchased.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​used\_units

</td><td>

Number of units that have been used.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the entitlement characteristic.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​sys\_created\_by

</td><td>

Name of the user that created the entitlement characteristics record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​sys\_created\_on

</td><td>

Date and time that the entitlement characteristics record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​sys\_id

</td><td>

Sys\_id of the entitlement characteristics record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement characteristics record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​sys\_updated\_on

</td><td>

Date and time that the entitlement characteristics record was last updated.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.type

</td><td>

Type of entitlement characteristic. Valid values:

-   coverage
-   coverage\_and\_usage

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.value

</td><td>

Value of the characteristic.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​install\_base\_items\_covered

</td><td>

List of install base items covered under the  service contract line.Data type: Array of Objects

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

service\_contract\_lines.​install\_base\_items\_covered.​added

</td><td>

Date that the associated install base item was added to the service contract line.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​install\_base\_items\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the install base item.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

service\_contract\_lines.​install\_base\_items\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the install base item.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the install base item covered by the service contract line.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

service\_contract\_lines.​install\_base\_items\_covered.​removed

</td><td>

Date that the associated service contract line ends coverage of the install base item.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​install\_base\_items\_covered.​service\_contract\_line

</td><td>

Sys\_id of the associated service contract line record.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​install\_base\_items\_covered.​sys\_created\_by

</td><td>

Name of the user that created the install base item record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​install\_base\_items\_covered.​sys\_created\_on

</td><td>

Date and time that the install base item record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​install\_base\_items\_covered.​sys\_id

</td><td>

Sys\_id of the install base item covered.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​install\_base\_items\_covered.​sys\_updated\_by

</td><td>

Name of the user that last updated the install base item record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​install\_base\_items\_covered.​sys\_updated\_on

</td><td>

Date and time that the install base item record was last updated.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​name

</td><td>

Name of the service contract line.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​number

</td><td>

Unique number of the service contract line. Automatically generated by the endpoint. For example: CTRL9812347.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​parent\_contract\_line

</td><td>

Sys\_id of the service contract line to which the current service contract line is a child of.Null for the contract lines created under a contract.

Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​product\_model

</td><td>

Sys\_id of the product associated with the service contract line.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

service\_contract\_lines.​product\_offering

</td><td>

Sys\_id of the product offering record associated with the service contract line.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

service\_contract\_lines.​product\_specification

</td><td>

Sys\_id of the product specification record associated with the service contract line.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

service\_contract\_lines.​sold\_product

</td><td>

Sys\_id of the sold product record associated with the service contract line.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​sold\_products\_covered

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

service\_contract\_lines.​sold\_products\_covered.​added

</td><td>

Date that the associated sold product was added to the service contract line.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​sold\_products\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the sold product covered.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

service\_contract\_lines.​sold\_products\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the sold product covered.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​sold\_products\_covered.removed

</td><td>

Date that the associated sold product was removed from the service contract line.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​sold\_products\_covered.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the sold product covered.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​sold\_products\_covered.​sold\_product

</td><td>

Sys\_id of the product covered by the entitlement.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​sold\_products\_covered.​sys\_created\_by

</td><td>

Name of the user that created the sold product covered record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​sold\_products\_covered.​sys\_created\_on

</td><td>

Date and time that the sold product covered record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​sold\_products\_covered.​sys\_id

</td><td>

Sys\_id of the product covered by this service contract.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​sold\_products\_covered.​sys\_updated\_by

</td><td>

Name of the user that last updated the sold product covered record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​sold\_products\_covered.​sys\_updated\_on

</td><td>

Date and time that the sold product covered record was last updated.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​starts

</td><td>

Start date of the service contract line.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​state

</td><td>

Current state of the contract line.

Valid values: \(case-sensitive\)

-   active
-   cancelled
-   draft
-   expired
-   suspended

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​sys\_created\_by

</td><td>

Name of the user that created the service contract line record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​sys\_created\_on

</td><td>

Date and time that the service contract line record was created.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​sys\_id

</td><td>

Sys\_id of a service contract line record.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​sys\_updated\_by

</td><td>

Name of the user that last updated the service contract line record.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​sys\_updated\_on

</td><td>

Date and time that the service contract line record was last updated.Data type: String

</td></tr><tr><td>

short\_description

</td><td>

Brief description or name of the service contract.

Data type: String

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

Date that the associated sold product was added to the contract.Data type: String

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

sold\_products\_covered.​removed

</td><td>

Date that the associated sold product was removed from the contract.Data type: String

</td></tr><tr><td>

sold\_products\_covered.​service\_line\_contract

</td><td>

Sys\_id of the service contract line record associated with the sold product covered.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

sold\_products\_covered.​sold\_product

</td><td>

Sys\_id of the product covered by the service contract.Data type: String

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

starts

</td><td>

Date on which the service contract begins.

Data type: String

Format: yyyy-mm-dd

Default: Starts as soon as approved.

</td></tr><tr><td>

state

</td><td>

Current state of the service contract.

Valid values: \(case-sensitive\)

-   active
-   cancelled
-   draft
-   expired

Data type: String

</td></tr><tr><td>

sys\_created\_by

</td><td>

Name of the user that created the service contract record.Data type: String

</td></tr><tr><td>

sys\_created\_on

</td><td>

Date and time that the service contract was created record.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the service contract record.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

sys\_updated\_by

</td><td>

Name of the user that last updated the service contract record.Data type: String

</td></tr><tr><td>

sys\_updated\_on

</td><td>

Date and time that the service contract record was last updated.Data type: String

</td></tr><tr><td>

vendor\_contract

</td><td>

Unique identifier for an associated external contract.

Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "https://instance.servicenow.com/api/sn_pss_core/servicecontract/fc73d2de89226110f877430a4e008add" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Response:

```
{
  "result": {
    "sys_id": "d8641151d1f53110f8776589fa411fde",
    "sys_created_by": "admin",
    "sys_updated_by": "admin",
    "sys_created_on": "2023-10-09 11:27:29",
    "sys_updated_on": "2023-10-09 11:27:29",
    "account": "4c325111d1f53110f8776589fa411f3d",
    "consumer": null,
    "household": null,
    "number": "CNTR0010004",
    "state": "active",
    "starts": "2022-12-03",
    "ends": "",
    "short_description": null,
    "vendor_contract": "External Reference",
    "service_contract_lines": [
      {
        "sys_id": "d4641d91d1f53110f8776589fa411fbb",
        "sys_created_by": "admin",
        "sys_updated_by": "admin",
        "sys_created_on": "2023-10-09 11:27:29",
        "sys_updated_on": "2023-10-09 11:27:29",
        "name": "CLI",
        "number": "CNTRL0000001",
        "contract": "d8641151d1f53110f8776589fa411fde",
        "parent_contract_line": null,
        "sold_product": null,
        "starts": "2022-12-03",
        "ends": "",
        "product_offering": null,
        "product_specification": null,
        "product_model": null,
        "child_contract_lines": [
          {
            "sys_id": "3a39ecdc01154f4ab782da0169c9c922",
            "sys_created_by": "admin",
            "sys_updated_by": "admin",
            "sys_created_on": "2023-10-09 11:27:29",
            "sys_updated_on": "2023-10-09 11:27:29",
            "name": "Child CLI",
            "number": "CNTRL0000002",
            "contract": "d8641151d1f53110f8776589fa411fde",
            "parent_contract_line": "d4641d91d1f53110f8776589fa411fbb",
            "sold_product": null,
            "starts": "2022-12-03",
            "ends": "",
            "product_offering": null,
            "product_specification": null,
            "product_model": null,
            "child_contract_lines": [],
            "entitlements": [
              {
                "sys_id": "7439fd84c2494ba6951e58f333cfe8d4",
                "sys_created_by": "admin",
                "sys_updated_by": "admin",
                "sys_created_on": "2023-10-09 11:27:29",
                "sys_updated_on": "2023-10-09 11:27:29",
                "entitlement_name": "Child CLI - ENTL",
                "account": "4c325111d1f53110f8776589fa411f3d",
                "consumer": null,
                "household": null,
                "contract": "d8641151d1f53110f8776589fa411fde",
                "service_contract_line": "3a39ecdc01154f4ab782da0169c9c922",
                "state": "active",
                "product_offering": null,
                "product_specification": null,
                "sold_entitlement": null,
                "product": null,
                "start_date": "2022-12-03",
                "end_date": "",
                "entitlement_characteristics": [],
                "sold_products_covered": [],
                "install_base_items_covered": []
              }
            ],
            "sold_products_covered": [
              {
                "sys_id": "dfb62e9c4c6843009be02a68f65b9118",
                "sys_created_by": "admin",
                "sys_updated_by": "admin",
                "sys_created_on": "2023-10-09 11:27:29",
                "sys_updated_on": "2023-10-09 11:27:29",
                "contract": "d8641151d1f53110f8776589fa411fde",
                "service_contract_line": "d4641d91d1f53110f8776589fa411fbb",
                "entitlement": null,
                "sold_product": "ec235d9dd1b53110f8776589fa411fe2",
                "added": "2023-12-03",
                "removed": "2023-12-03"
              }
            ],
            "install_base_items_covered": [
              {
                "sys_id": "2583912e81964501b52a2e44d4797a28",
                "sys_created_by": "admin",
                "sys_updated_by": "admin",
                "sys_created_on": "2023-10-09 11:27:29",
                "sys_updated_on": "2023-10-09 11:27:29",
                "contract": "d8641151d1f53110f8776589fa411fde",
                "service_contract_line": "d4641d91d1f53110f8776589fa411fbb",
                "entitlement": null,
                "install_base": "a1731551d1f53110f8776589fa411f8d",
                "added": "2023-12-03",
                "removed": "2023-12-03"
              }
            ],
            "entitlement_characteristics": [
              {
                "sys_id": "3a00c975bb49412cae169200c7f6236e",
                "sys_created_by": "admin",
                "sys_updated_by": "admin",
                "sys_created_on": "2023-10-09 11:27:29",
                "sys_updated_on": "2023-10-09 11:27:29",
                "service_contract_line": "d4641d91d1f53110f8776589fa411fbb",
                "entitlement": null,
                "characteristic_option": "495149b7539e61106bfcddeeff7b1262",
                "value": "5",
                "characteristic": "63418db7539e61106bfcddeeff7b1238",
                "type": "coverage"
              }
            ]
          }
        ],
        "entitlements": [
          {
            "sys_id": "a8641d91d1f53110f8776589fa411fc0",
            "sys_created_by": "admin",
            "sys_updated_by": "admin",
            "sys_created_on": "2023-10-09 11:27:29",
            "sys_updated_on": "2023-10-09 11:27:29",
            "entitlement_name": "ENTL",
            "account": "4c325111d1f53110f8776589fa411f3d",
            "consumer": null,
            "household": null,
            "contract": "d8641151d1f53110f8776589fa411fde",
            "service_contract_line": "d4641d91d1f53110f8776589fa411fbb",
            "state": "active",
            "product_offering": null,
            "product_specification": null,
            "sold_entitlement": null,
            "product": null,
            "start_date": "2022-12-03",
            "end_date": "",
            "sold_products_covered": [
              {
                "sys_id": "a0641d91d1f53110f8776589fa411fc2",
                "sys_created_by": "admin",
                "sys_updated_by": "admin",
                "sys_created_on": "2023-10-09 11:27:29",
                "sys_updated_on": "2023-10-09 11:27:29",
                "contract": "d8641151d1f53110f8776589fa411fde",
                "service_contract_line": "d4641d91d1f53110f8776589fa411fbb",
                "entitlement": "a8641d91d1f53110f8776589fa411fc0",
                "sold_product": "da23d151d1f53110f8776589fa411f27",
                "added": "",
                "removed": ""
              }
            ],
            "install_base_items_covered": [
              {
                "sys_id": "e0641d91d1f53110f8776589fa411fc3",
                "sys_created_by": "admin",
                "sys_updated_by": "admin",
                "sys_created_on": "2023-10-09 11:27:29",
                "sys_updated_on": "2023-10-09 11:27:29",
                "contract": "d8641151d1f53110f8776589fa411fde",
                "service_contract_line": "d4641d91d1f53110f8776589fa411fbb",
                "entitlement": "a8641d91d1f53110f8776589fa411fc0",
                "install_base": "43739151d1f53110f8776589fa411fc1",
                "added": "2023-12-03",
                "removed": "2023-12-03"
              }
            ],
            "entitlement_characteristics": [
              {
                "sys_id": "a8641d91d1f53110f8776589fa411fd0",
                "sys_created_by": "admin",
                "sys_updated_by": "admin",
                "sys_created_on": "2023-10-09 11:27:29",
                "sys_updated_on": "2023-10-09 11:27:29",
                "service_contract_line": null,
                "entitlement": "a8641d91d1f53110f8776589fa411fc0",
                "characteristic_option": "495149b7539e61106bfcddeeff7b1262",
                "value": "5",
                "characteristic": "63418db7539e61106bfcddeeff7b1238",
                "type": "coverage_and_usage",
                "entitlement_usage": [
                  {
                    "sys_id": "a8641d91d1f53110f8776589fa411fd1",
                    "sys_created_by": "admin",
                    "sys_updated_by": "admin",
                    "sys_created_on": "2023-10-09 11:27:29",
                    "sys_updated_on": "2023-10-09 11:27:29",
                    "entitlement": "a8641d91d1f53110f8776589fa411fc0",
                    "service_contract_line": null,
                    "entitlement_characteristic": "a8641d91d1f53110f8776589fa411fd0",
                    "period_start": "2022-12-03",
                    "period_end": "",
                    "total_units": "5",
                    "used_units": "3"
                  }
                ]
              }
            ]
          }
        ],
        "sold_products_covered": [
          {
            "sys_id": "98641d91d1f53110f8776589fa411fbc",
            "sys_created_by": "admin",
            "sys_updated_by": "admin",
            "sys_created_on": "2023-10-09 11:27:29",
            "sys_updated_on": "2023-10-09 11:27:29",
            "contract": "d8641151d1f53110f8776589fa411fde",
            "service_contract_line": "d4641d91d1f53110f8776589fa411fbb",
            "entitlement": null,
            "sold_product": "ec235d9dd1b53110f8776589fa411fe2",
            "added": "2023-12-03",
            "removed": "2023-12-03"
          }
        ],
        "install_base_items_covered": [
          {
            "sys_id": "58641d91d1f53110f8776589fa411fbd",
            "sys_created_by": "admin",
            "sys_updated_by": "admin",
            "sys_created_on": "2023-10-09 11:27:29",
            "sys_updated_on": "2023-10-09 11:27:29",
            "contract": "d8641151d1f53110f8776589fa411fde",
            "service_contract_line": "d4641d91d1f53110f8776589fa411fbb",
            "entitlement": null,
            "install_base": "a1731551d1f53110f8776589fa411f8d",
            "added": "2023-12-03",
            "removed": "2023-12-03"
          }
        ],
        "entitlement_characteristics": [
          {
            "sys_id": "e0641d91d1f53110f8776589fa411fbf",
            "sys_created_by": "admin",
            "sys_updated_by": "admin",
            "sys_created_on": "2023-10-09 11:27:29",
            "sys_updated_on": "2023-10-09 11:27:29",
            "service_contract_line": "d4641d91d1f53110f8776589fa411fbb",
            "entitlement": null,
            "characteristic_option": "495149b7539e61106bfcddeeff7b1262",
            "value": "5",
            "characteristic": "63418db7539e61106bfcddeeff7b1238",
            "type": "coverage"
          }
        ]
      },
      {
        "sys_id": "e4641d91d1f53110f8776589fa411fd2",
        "sys_created_by": "admin",
        "sys_updated_by": "admin",
        "sys_created_on": "2023-10-09 11:27:29",
        "sys_updated_on": "2023-10-09 11:27:29",
        "name": "CLI 2",
        "number": "CNTRL0000003”,
        "contract": "d8641151d1f53110f8776589fa411fde",
        "parent_contract_line": null,
        "sold_product": null,
        "starts": "2022-12-03",
        "ends": "",
        "product_offering": null,
        "product_specification": null,
        "product_model": null,
        "child_contract_lines": [],
        "entitlements": [],
        "sold_products_covered": [
          {
            "sys_id": "e8641d91d1f53110f8776589fa411fd3",
            "sys_created_by": "admin",
            "sys_updated_by": "admin",
            "sys_created_on": "2023-10-09 11:27:29",
            "sys_updated_on": "2023-10-09 11:27:29",
            "contract": "d8641151d1f53110f8776589fa411fde",
            "service_contract_line": "e4641d91d1f53110f8776589fa411fd2",
            "entitlement": null,
            "sold_product": "7f23995dd1b53110f8776589fa411f66",
            "added": "2023-12-03",
            "removed": "2023-12-03"
          }
        ],
        "install_base_items_covered": [
          {
            "sys_id": "a8641d91d1f53110f8776589fa411fd4",
            "sys_created_by": "admin",
            "sys_updated_by": "admin",
            "sys_created_on": "2023-10-09 11:27:29",
            "sys_updated_on": "2023-10-09 11:27:29",
            "contract": "d8641151d1f53110f8776589fa411fde",
            "service_contract_line": "e4641d91d1f53110f8776589fa411fd2",
            "entitlement": null,
            "install_base": "a483d951d1f53110f8776589fa411fad",
            "added": "2023-12-03",
            "removed": "2023-12-03"
          }
        ],
        "entitlement_characteristics": [
          {
            "sys_id": "a8641d91d1f53110f8776589fa411fd5",
            "sys_created_by": "admin",
            "sys_updated_by": "admin",
            "sys_created_on": "2023-10-09 11:27:29",
            "sys_updated_on": "2023-10-09 11:27:29",
            "service_contract_line": "e4641d91d1f53110f8776589fa411fd2",
            "entitlement": null,
            "characteristic_option": "495149b7539e61106bfcddeeff7b1262",
            "value": "5",
            "characteristic": "63418db7539e61106bfcddeeff7b1238",
            "type": "coverage"
          }
        ]
      }
    ],
    "sold_products_covered": [
      {
        "sys_id": "9c641d91d1f53110f8776589fa411fb9",
        "sys_created_by": "admin",
        "sys_updated_by": "admin",
        "sys_created_on": "2023-10-09 11:27:29",
        "sys_updated_on": "2023-10-09 11:27:29",
        "contract": "d8641151d1f53110f8776589fa411fde",
        "service_contract_line": null,
        "entitlement": null,
        "sold_product": "0df21151d1f53110f8776589fa411f1b",
        "added": "2023-12-03",
        "removed": "2023-12-03"
      }
    ],
    "install_base_items_covered": [
      {
        "sys_id": "d8641d91d1f53110f8776589fa411fba",
        "sys_created_by": "admin",
        "sys_updated_by": "admin",
        "sys_created_on": "2023-10-09 11:27:29",
        "sys_updated_on": "2023-10-09 11:27:29",
        "contract": "d8641151d1f53110f8776589fa411fde",
        "service_contract_line": null,
        "entitlement": null,
        "install_base": "e2639951d1f53110f8776589fa411f2b",
        "added": "2023-12-03",
        "removed": "2023-12-03"
      }
    ]
  }
}
```

## Service Contract - GET /sn\_pss\_core/servicecontract/contractline/\{id\}

Retrieves the details of a specified service contract line record and its related entities.

This endpoint retrieves data in the following tables when processing the request:

-   Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]
-   Entitlement \[service\_entitlement\]
-   Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]
-   Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\] - This table contains information for both sold products covered and install base items covered.
-   Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

### URL format

Versioned URL: `/api/sn_pss_core/{api_version}/servicecontract/contractline/{id}`

Default URL: `/api/sn_pss_core/servicecontract/contractline/{id}`

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

Sys\_id of the service contract line record to retrieve.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

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
|403|Forbidden. The user doesn't have permission to access the API.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

child\_contract\_lines

</td><td>

List of child service contract lines associated with the service contract line.Data type: Array of Objects

```
"child_contract_lines": [
  {
    "child_contract_lines": [Array],
    "contract": "String",
    "ends": "String",
    "entitlements": [Array],
    "entitlement_characteristics": [Array],
    "install_base_items_covered": [Array],
    "name": "String",
    "number": "String",
    "parent_contract_line": "String",
    "product_model": "String",
    "product_offering": "String",
    "product_specification": "String",
    "sold_product": "String",
    "sold_products_covered": [Array],
    "starts": "String",
    "state": "String",
    "sys_created_by": "String",
    "sys_created_on": "String",
    "sys_id": "String",
    "sys_updated_by": "String",
    "sys_update_on": "String"
  }
]
```

</td></tr><tr><td>

child\_contract\_lines.​child\_contract\_lines

</td><td>

List of child service contract line objects created under the child service contract line. The objects in this array have the same elements as the objects in the **child\_contract\_lines** parameter.Data type: Array of Objects

</td></tr><tr><td>

child\_contract\_lines.​contract

</td><td>

Sys\_id of the service contract associated with the child service contract line.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

child\_contract\_lines.​ends

</td><td>

Date on which the child service contract line ends.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

child\_contract\_lines.​entitlements

</td><td>

List of entitlements associated with the child service contract line.Data type: Array of Objects

```
"entitlements": [
  {
    "account": "String",
    "consumer": "String",
    "contract": "String",
    "end_date": "String",
    "entitlement_characteristics": [Array],
    "entitlement_name": "String",
    "household": "String",
    "install_base_items_covered": [Array],
    "product": "String",
    "product_offering": "String",
    "product_specification": "String",
    "service_contract_line": "String",
    "sold_entitlement": "String",
    "sold_products_covered": [Array],
    "start_date": "String",
    "state": "String",
    "sys_created_by": "String",
    "sys_created_on": "String",
    "sys_id": "String",
    "sys_updated_by": "String",
    "sys_updated_on": "String"
  }
]
```

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​account

</td><td>

Sys\_id of the account record to which the entitlement belongs.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​consumer

</td><td>

Sys\_id of the consumer record to which the entitlement belongs.

Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​contract

</td><td>

Sys\_id of the contract record to which the entitlement belongs.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​end\_date

</td><td>

End date of the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics

</td><td>

List of characteristics associated with the entitlement.Data type: Array of Objects

```
"entitlement_characteristics": [
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
    "sys_updated_on": "String"
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​characteristic

</td><td>

Sys\_id of the characteristic record associated with the entitlement.

Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​characteristic\_option

</td><td>

Sys\_id of the characteristic option record associated with the entitlement.Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement

</td><td>

Sys\_id of the entitlement record.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage

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

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the entitlement usage.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​entitlement\_characteristic

</td><td>

Sys\_id of the entitlement characteristic record associated with the entitlement usage.Data type: String

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

cchild\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​period\_end

</td><td>

End date when the entitlement usage is no longer tracked.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​period\_start

</td><td>

Starting date of when the entitlement usage is tracked.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​service\_contract\_line

</td><td>

Sys\_id of the service contract line to which the current entitlement usage belongs. Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_created\_by

</td><td>

Name of the user that created the entitlement usage record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_created\_on

</td><td>

Date and time that the entitlement usage record was created.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_id

</td><td>

Sys\_id of the entitlement usage record.Data type: String

Table: Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement usage record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_updated\_on

</td><td>

Date and time that the entitlement usage record was last updated.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​total\_units

</td><td>

Total coverage value of the associated entitlement characteristic.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​used\_units

</td><td>

Number of units used by the account or consumer between the **period\_start** and the **period\_end**.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​type

</td><td>

Type of entitlement characteristic. Valid values:

-   coverage
-   coverage\_and\_usage

Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​value

</td><td>

Value of the characteristic.

Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_name

</td><td>

Name of the entitlement.

Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​household

</td><td>

Sys\_id of the household record associated with the entitlement.

Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​install\_base\_items\_covered

</td><td>

List of install base items covered under the  child service contract line.Data type: Array of Objects

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

child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​added

</td><td>

Date that the associated install base item was added to the service contract line.

Data type: String

 Format: yyyy-mm-dd

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the install base item.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the install base item.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the associated install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​removed

</td><td>

Date that the associated service contract line ends coverage of the install base item.

Data type: String

 Format: yyyy-mm-dd

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​service\_contract\_line

</td><td>

Sys\_id of the associated service contract line record.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_created\_by

</td><td>

Name of the user that created the install base item record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_created\_on

</td><td>

Date and time that the install base item record was created.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_id

</td><td>

Sys\_id of the install base item covered.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_updated\_by

</td><td>

Name of the user that last updated the install base item record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_updated\_on

</td><td>

Date and time that the install base item record was last updated.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​product

</td><td>

Sys\_id of the product model record associated with the entitlement.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​product\_offering

</td><td>

Sys\_id of the product offering record associated with the entitlement.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​product\_specification

</td><td>

Sys\_id of the product specification record associated with the entitlement.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the entitlement.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_entitlement

</td><td>

Sys\_id of the sold product record associated with the entitlement.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_products\_covered

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

child\_contract\_lines.​entitlements.​sold\_products\_covered.​added

</td><td>

Date that the associated service contract starts to cover the product.

Data type: String

 Format: yyyy-mm-dd

 Default: Current date

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_products\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the sold product covered.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_products\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the sold product covered.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_products\_covered.​removed

</td><td>

Date that the associated service contract ends coverage of the associated product.

Data type: String

 Format: yyyy-mm-dd

 Default: No end date

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_products\_covered.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the sold product covered.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_products\_covered.​sold\_product

</td><td>

Sys\_id of the product covered by the service contract.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_products\_covered​sys\_created\_by

</td><td>

Name of the user that created the sold product covered record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_products\_covered.​sys\_created\_on

</td><td>

Date and time that the sold product covered record was created.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_products\_covered.​sys\_id

</td><td>

Sys\_id of the product covered by this service contract.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_products\_covered.​sys\_updated\_by

</td><td>

Name of the user that last updated the sold product covered record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_products\_covered.​sys\_updated\_on

</td><td>

Name of the user that last updated the sold product covered record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​start\_date

</td><td>

Start date of the entitlement.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​state

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

child\_contract\_lines.​entitlements.​sys\_created\_by

</td><td>

Name of the user that created the entitlement record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sys\_created\_on

</td><td>

Date and time that the entitlement record was created.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sys\_id

</td><td>

Sys\_id of the associated entitlement record.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sys\_updated\_on

</td><td>

Date and time that the entitlement record was created.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics

</td><td>

List of characteristics associated with the entitlement.Data type: Array of Objects

```
"entitlement_characteristics": [
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
    "sys_updated_on": "String"
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​characteristic

</td><td>

Sys\_id of the characteristic record associated with the entitlement.

Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​characteristic\_option

</td><td>

Sys\_id of the characteristic option record associated with the entitlement.Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​entitlement

</td><td>

Sys\_id of the entitlement record.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage

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

child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the entitlement usage.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​entitlement\_characteristic

</td><td>

Sys\_id of the entitlement characteristic record associated with the entitlement usage.Data type: String

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​period\_end

</td><td>

End date when the entitlement usage is no longer tracked.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​period\_start

</td><td>

Starting date of when the entitlement usage is tracked.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​service\_contract\_line

</td><td>

Sys\_id of the service contract line to which the current entitlement usage belongs. Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​sys\_created\_by

</td><td>

Name of the user that created the entitlement usage record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​sys\_created\_on

</td><td>

Date and time that the entitlement usage record was created.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​sys\_id

</td><td>

Sys\_id of the entitlement usage record.Data type: String

Table: Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement usage record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​sys\_updated\_on

</td><td>

Date and time that the entitlement usage record was last updated.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​total\_units

</td><td>

Total coverage value of the associated entitlement characteristic.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​used\_units

</td><td>

Number of units used by the account or consumer between the **period\_start** and the **period\_end**.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the entitlement characteristic.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​sys\_created\_by

</td><td>

Name of the user that created the entitlement characteristics record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​sys\_created\_on

</td><td>

Date and time that the entitlement characteristics record was created.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​sys\_id

</td><td>

Sys\_id of the entitlement characteristics record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement characteristics record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​sys\_updated\_on

</td><td>

Date and time that the entitlement characteristics record was last updated.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​type

</td><td>

Type of entitlement characteristic. Valid values:

-   coverage
-   coverage\_and\_usage

Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​value

</td><td>

Value of the characteristic.

Data type: String

</td></tr><tr><td>

child\_contract\_lines.​install\_base\_items\_covered

</td><td>

List of install base items covered under the  child service contract line.Data type: Array of Objects

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

child\_contract\_lines.​install\_base\_items\_covered.​added

</td><td>

Date that the associated install base item was added to the service contract line.

Data type: String

 Format: yyyy-mm-dd

</td></tr><tr><td>

child\_contract\_lines.​install\_base\_items\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the install base item.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

child\_contract\_lines.​install\_base\_items\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the install base item.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

child\_contract\_lines.​install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the associated install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

child\_contract\_lines.​install\_base\_items\_covered.​removed

</td><td>

Date that the associated service contract line ends coverage of the install base item.

Data type: String

 Format: yyyy-mm-dd

</td></tr><tr><td>

child\_contract\_lines.​install\_base\_items\_covered.​service\_contract\_line

</td><td>

Sys\_id of the associated service contract line record.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

child\_contract\_lines.​install\_base\_items\_covered.​sys\_created\_by

</td><td>

Name of the user that created the install base item record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​install\_base\_items\_covered.​sys\_created\_on

</td><td>

Date and time that the install base item record was created.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​install\_base\_items\_covered.​sys\_id

</td><td>

Sys\_id of the install base item covered.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

child\_contract\_lines.​install\_base\_items\_covered.​sys\_updated\_by

</td><td>

Name of the user that last updated the install base item record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​install\_base\_items\_covered.​sys\_updated\_on

</td><td>

Date and time that the install base item record was last updated.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​name

</td><td>

Name of the child service contract line.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​number

</td><td>

Unique number of the service contract line. Automatically generated by the endpoint. For example: CTRL000001.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​parent\_contract\_line

</td><td>

Sys\_id of the parent contract line record associated with the child service contract line.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​product\_model

</td><td>

Sys\_id of the product associated with the child service contract line.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

child\_contract\_lines.​product\_offering

</td><td>

Sys\_id of the product offering record associated with the child service contract line.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

child\_contract\_lines.​product\_specification

</td><td>

Sys\_id of the product specification record associated with the child service contract line.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

child\_contract\_lines.​sold\_product

</td><td>

Sys\_id of the sold product record associated with the child service contract line.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

child\_contract\_lines.​sold\_products\_covered

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

child\_contract\_lines.​sold\_products\_covered.​added

</td><td>

Date that the associated service contract starts to cover the product.

Data type: String

 Format: yyyy-mm-dd

 Default: Current date

</td></tr><tr><td>

child\_contract\_lines.​sold\_products\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the sold product covered.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

child\_contract\_lines.​sold\_products\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the sold product covered.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

child\_contract\_lines.​sold\_products\_covered.​removed

</td><td>

Date that the associated service contract ends coverage of the associated product.

Data type: String

 Format: yyyy-mm-dd

 Default: No end date

</td></tr><tr><td>

child\_contract\_lines.​sold\_products\_covered.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the sold product covered.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

child\_contract\_lines.​sold\_products\_covered.​sold\_product

</td><td>

Sys\_id of the product covered by the service contract.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

child\_contract\_lines.​sold\_products\_covered.​sys\_created\_by

</td><td>

Name of the user that created the sold product covered record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​sold\_products\_covered.​sys\_created\_on

</td><td>

Date and time that the sold product covered record was created.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​sold\_products\_covered.​sys\_id

</td><td>

Sys\_id of the product covered by this service contract.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

child\_contract\_lines.​sold\_products\_covered.​sys\_updated\_by

</td><td>

Name of the user that last updated the sold product covered record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​sold\_products\_covered.​sys\_updated\_on

</td><td>

Name of the user that last updated the sold product covered record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​starts

</td><td>

Start date of the child service contract line.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

child\_contract\_lines.​state

</td><td>

Current state of the contract line.

Valid values: \(case-sensitive\)

-   active
-   cancelled
-   draft
-   expired
-   suspended

Data type: String

</td></tr><tr><td>

child\_contract\_lines.​sys\_created\_by

</td><td>

Name of the user that created the child service contract line record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​sys\_created\_on

</td><td>

Date and time that the child service contract line record was created.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​sys\_id

</td><td>

Sys\_id of a child service contract line record.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

child\_contract\_lines.​sys\_updated\_by

</td><td>

Name of the user that last updated the child service contract line record.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​sys\_updated\_on

</td><td>

Date and time that the child service contract line record was last updated.Data type: String

</td></tr><tr><td>

contract

</td><td>

Sys\_id of the service contract associated with the service contract line.

Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

ends

</td><td>

Date on which the service contract line ends.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

entitlements

</td><td>

List of entitlements associated with the service contract line.Data type: Array of Objects

```
"entitlements": [
  {
    "account": "String",
    "consumer": "String",
    "contract": "String",
    "end_date": "String",
    "entitlement_characteristics": [Array],
    "entitlement_name": "String",
    "household": "String",
    "install_base_items_covered": [Array],
    "product": "String",
    "product_offering": "String",
    "product_specification": "String",
    "service_contract_line": "String",
    "sold_entitlement": "String",
    "sold_products_covered": [Array],
    "start_date": "String",
    "state": "String",
    "sys_created_by": "String",
    "sys_created_on": "String",
    "sys_id": "String",
    "sys_updated_by": "String",
    "sys_updated_on": "String"
  }
]
```

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

entitlements.​account

</td><td>

Sys\_id of the account record to which the entitlement belongs.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

entitlements.​consumer

</td><td>

Sys\_id of the consumer record to which the entitlement belongs.

Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

entitlements.​contract

</td><td>

Sys\_id of the contract record to which the entitlement belongs.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

entitlements.​end\_date

</td><td>

End date of the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

entitlements.​entitlement\_characteristics

</td><td>

List of characteristics associated with the entitlement.Data type: Array of Objects

```
"entitlement_characteristics": [
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

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.characteristic

</td><td>

Sys\_id of the characteristic record associated with the entitlement.

Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.characteristic\_option

</td><td>

Sys\_id of the characteristic option record associated with the entitlement.Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​entitlement

</td><td>

Sys\_id of the associated entitlement record.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​entitlement\_usage

</td><td>

Entitlement usage details.Data type: Array of Objects

```
"entitlement_usage": [
  {
    "entitlement": "String",
    "entitlement_characteristic": [Array],
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

entitlements.​entitlement\_characteristics.​entitlement\_usage.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the entitlement usage.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​entitlement\_usage.​entitlement\_characteristic

</td><td>

Sys\_id of the entitlement characteristic record associated with the entitlement usage.Data type: String

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​entitlement\_usage.​period\_end

</td><td>

End date when the entitlement usage is no longer tracked.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​entitlement\_usage.​period\_start

</td><td>

Starting date of when the entitlement usage is tracked.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​entitlement\_usage.​service\_contract\_line

</td><td>

Service contract line to which the current entitlement usage belongs. Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_created\_by

</td><td>

Name of the user that created the entitlement usage record.Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_created\_on

</td><td>

Date and time that the entitlement usage record was created.Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_id

</td><td>

Sys\_id of the entitlement usage record.Data type: String

Table: Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement usage record.Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_updated\_on

</td><td>

Date and time that the entitlement usage record was last updated.Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​entitlement\_usage.​total\_units

</td><td>

Total coverage value of the associated entitlement characteristic.Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​entitlement\_usage.​used\_units

</td><td>

Number of units used by the account or consumer between the **period\_start** and the **period\_end**.Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the entitlement characteristic.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​sys\_created\_by

</td><td>

Name of the user that created the entitlement characteristics record.Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​sys\_created\_on

</td><td>

Date and time that the entitlement characteristics record was created.Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​sys\_id

</td><td>

Sys\_id of the entitlement characteristics record.Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement characteristics record.Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​sys\_updated\_on

</td><td>

Date and time that the entitlement characteristics record was last updated.Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.type

</td><td>

Type of entitlement characteristic. Valid values:

-   coverage
-   coverage\_and\_usage

Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.value

</td><td>

Value of the characteristic.

Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_name

</td><td>

Name of the entitlement.

Data type: String

</td></tr><tr><td>

entitlements.​household

</td><td>

Sys\_id of the household record associated with the entitlement.

Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

entitlements.​install\_base\_items\_covered

</td><td>

List of install base items covered under the service contract line.Data type: Array of Objects

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

</td></tr><tr><td>

entitlements.​install\_base\_items\_covered.​added

</td><td>

Date that the associated install base item was added to the entitlement.Data type: String

</td></tr><tr><td>

entitlements.​install\_base\_items\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the install base item.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

entitlements.​install\_base\_items\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the install base item.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

entitlements.​install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the associated install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

entitlements.​install\_base\_items\_covered.​removed

</td><td>

Date that the associated install base item was removed from the entitlement.Data type: String

</td></tr><tr><td>

entitlements.​install\_base\_items\_covered.​service\_contract\_line

</td><td>

Sys\_id of the associated service contract line record.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

entitlements.​install\_base\_items\_covered.​sys\_created\_by

</td><td>

Name of the user that created the install base item record.Data type: String

</td></tr><tr><td>

entitlements.​install\_base\_items\_covered.​sys\_created\_on

</td><td>

Date and time that the install base item record was created.Data type: String

</td></tr><tr><td>

entitlements.​install\_base\_items\_covered.​sys\_id

</td><td>

Sys\_id of the install base item covered.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

entitlements.​install\_base\_items\_covered.​sys\_updated\_by

</td><td>

Name of the user that last updated the install base item record.Data type: String

</td></tr><tr><td>

entitlements.​install\_base\_items\_covered.​sys\_updated\_on

</td><td>

Date and time that the install base item record was last updated.Data type: String

</td></tr><tr><td>

entitlements.​product

</td><td>

Sys\_id of the product model record associated with the entitlement.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

entitlements.​product\_offering

</td><td>

Sys\_id of the product offering record associated with the entitlement.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

entitlements.​product\_specification

</td><td>

Sys\_id of the product specification record associated with the entitlement.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

entitlements.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the entitlement.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

entitlements.​sold\_entitlement

</td><td>

Sys\_id of the sold product record associated with the entitlement.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

entitlements.​sold\_products\_covered

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

entitlements.​sold\_products\_covered.​added

</td><td>

Date that the associated sold product was added to the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

entitlements.​sold\_products\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the sold product covered.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

entitlements.​sold\_products\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the sold product covered.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

entitlements.​sold\_products\_covered.removed

</td><td>

Date that the associated sold product was removed from the entitlement.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

entitlements.​sold\_products\_covered.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the sold product covered.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

entitlements.​sold\_products\_covered.​sold\_product

</td><td>

Sys\_id of the product covered by the entitlement.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

entitlements.​sold\_products\_covered.​sys\_created\_by

</td><td>

Name of the user that created the sold product covered record.Data type: String

</td></tr><tr><td>

entitlements.​sold\_products\_covered.​sys\_created\_on

</td><td>

Date and time that the sold product covered record was created.Data type: String

</td></tr><tr><td>

entitlements.​sold\_products\_covered.​sys\_id

</td><td>

Sys\_id of the product covered by this service contract.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

entitlements.​sold\_products\_covered.​sys\_updated\_by

</td><td>

Name of the user that last updated the sold product covered record.Data type: String

</td></tr><tr><td>

entitlements.​sold\_products\_covered.​sys\_updated\_on

</td><td>

Date and time that the sold product covered record was last updated.Data type: String

</td></tr><tr><td>

entitlements.​start\_date

</td><td>

Start date of the entitlement.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

entitlements.​state

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

entitlements.​sys\_created\_by

</td><td>

Name of the user that created the entitlement record.Data type: String

</td></tr><tr><td>

entitlements.​sys\_created\_on

</td><td>

Date and time that the entitlement record was created.Data type: String

</td></tr><tr><td>

entitlements.​sys\_id

</td><td>

Sys\_id of the associated entitlement record.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

entitlements.​sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement record.Data type: String

</td></tr><tr><td>

entitlements.​sys\_updated\_on

</td><td>

Date and time that the entitlement record was created.Data type: String

</td></tr><tr><td>

entitlement\_characteristics

</td><td>

List of entitlement characteristics associated with the service contract line.Data type: Array of Objects

```
"entitlement_characteristics": [
  {
    "characteristic": "String",
    "characteristic_option": "String",
    "entitlement": "String",
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

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

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

Sys\_id of the entitlement record.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

entitlement\_characteristics.​service\_contract\_line

</td><td>

Sys\_id of the service contract line record associated with the entitlement characteristic.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

entitlement\_characteristics.​sys\_created\_by

</td><td>

Name of the user that created the entitlement characteristics record.Data type: String

</td></tr><tr><td>

entitlement\_characteristics.​sys\_created\_on

</td><td>

Date and time that the entitlement characteristics record was created.Data type: String

</td></tr><tr><td>

entitlement\_characteristics.​sys\_id

</td><td>

Sys\_id of the entitlement characteristics record.Data type: String

</td></tr><tr><td>

entitlement\_characteristics.​sys\_updated\_by

</td><td>

Name of the user that last updated the entitlement characteristics record.Data type: String

</td></tr><tr><td>

entitlement\_characteristics.​sys\_updated\_on

</td><td>

Date and time that the entitlement characteristics record was last updated.Data type: String

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

install\_base\_items\_covered

</td><td>

List of install base items covered under the  service contract line.Data type: Array of Objects

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

Date that the associated install base item was added to the service contract line.

Data type: String

</td></tr><tr><td>

install\_base\_items\_covered.​contract

</td><td>

Sys\_id of the service contract record associated with the install base item.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

install\_base\_items\_covered.​entitlement

</td><td>

Sys\_id of the entitlement record associated with the install base item.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the install base item covered by the service contract line.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

install\_base\_items\_covered.​removed

</td><td>

Date that the associated service contract line ends coverage of the install base item.

Data type: String

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

name

</td><td>

Name of the service contract line.

Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number of the service contract line. Automatically generated by the endpoint. For example: CTRL9812347.Data type: String

</td></tr><tr><td>

parent\_contract\_line

</td><td>

Sys\_id of the service contract line to which the current service contract line is a child of.Null for the contract lines created under a contract.

Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

product\_model

</td><td>

Sys\_id of the product associated with the service contract line.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

product\_offering

</td><td>

Sys\_id of the product offering record associated with the service contract line.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

product\_specification

</td><td>

Sys\_id of the product specification record associated with the service contract line.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

sold\_product

</td><td>

Sys\_id of the sold product record associated with the service contract line.Data type: String

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

Date that the associated sold product was added to the service contract line.Data type: String

Format: yyyy-mm-dd

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

Date that the associated sold product was removed from the service contract line.Data type: String

Format: yyyy-mm-dd

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

starts

</td><td>

Start date of the service contract line.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

state

</td><td>

Current state of the contract line.

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

Name of the user that created the service contract line record.Data type: String

</td></tr><tr><td>

sys\_created\_on

</td><td>

Date and time that the service contract line record was created.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of a service contract line record.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

sys\_updated\_by

</td><td>

Name of the user that last updated the service contract line record.Data type: String

</td></tr><tr><td>

sys\_updated\_on

</td><td>

Date and time that the service contract line record was last updated.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "https://instance.servicenow.com/api/sn_pss_core/servicecontract/contractline/fc73d2de89226110f877430a4e008add" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Response:

```
{
  "result": {
    "sys_id": "16e451d1d1f53110f8776589fa411f80",
    "sys_created_by": "admin",
    "sys_updated_by": "admin",
    "sys_created_on": "2023-10-09 11:29:47",
    "sys_updated_on": "2023-10-09 11:29:47",
    "name": "CLI",
    "number": "CTRL0000001",
    "contract": "a4b415d1d1f53110f8776589fa411f20",
    "parent_contract_line": null,
    "sold_product": null,
    "starts": "2022-12-03",
    "ends": "",
    "product_offering": null,
    "product_specification": null,
    "product_model": null,
    "child_contract_lines": [
      {
        "sys_id": "3a39ecdc01154f4ab782da0169c9c922",
        "sys_created_by": "admin",
        "sys_updated_by": "admin",
        "sys_created_on": "2023-10-09 11:27:29",
        "sys_updated_on": "2023-10-09 11:27:29",
        "name": "Child CLI",
        "number": "CTRL0000002",
        "contract": "a4b415d1d1f53110f8776589fa411f20",
        "parent_contract_line": "16e451d1d1f53110f8776589fa411f80",
        "sold_product": null,
        "starts": "2022-12-03",
        "ends": "",
        "product_offering": null,
        "product_model": null,
        "product_specification": null,
        "child_contract_lines": [],
        "entitlements": [
          {
            "sys_id": "7439fd84c2494ba6951e58f333cfe8d4",
            "sys_created_by": "admin",
            "sys_updated_by": "admin",
            "sys_created_on": "2023-10-09 11:27:29",
            "sys_updated_on": "2023-10-09 11:27:29",
            "entitlement_name": "Child CLI - ENTL",
            "account": "4c325111d1f53110f8776589fa411f3d",
            "consumer": null,
            "household": null,
            "contract": "a4b415d1d1f53110f8776589fa411f20",
            "service_contract_line": "3a39ecdc01154f4ab782da0169c9c922",
            "state": "active",
            "product_offering": null,
            "product_specification": null,
            "sold_entitlement": null,
            "product": null,
            "start_date": "2022-12-03",
            "end_date": "",
            "entitlement_characteristics": [],
            "sold_products_covered": [],
            "install_base_items_covered": []
          }
        ],
        "sold_products_covered": [
          {
            "sys_id": "dfb62e9c4c6843009be02a68f65b9118",
            "sys_created_by": "admin",
            "sys_updated_by": "admin",
            "sys_created_on": "2023-10-09 11:27:29",
            "sys_updated_on": "2023-10-09 11:27:29",
            "contract": "a4b415d1d1f53110f8776589fa411f20",
            "service_contract_line": "3a39ecdc01154f4ab782da0169c9c922",
            "entitlement": null,
            "sold_product": "ec235d9dd1b53110f8776589fa411fe2",
            "added": "2023-12-03",
            "removed": "2023-12-03"
          }
        ],
        "install_base_items_covered": [
          {
            "sys_id": "2583912e81964501b52a2e44d4797a28",
            "sys_created_by": "admin",
            "sys_updated_by": "admin",
            "sys_created_on": "2023-10-09 11:27:29",
            "sys_updated_on": "2023-10-09 11:27:29",
            "contract": "a4b415d1d1f53110f8776589fa411f20",
            "service_contract_line": "3a39ecdc01154f4ab782da0169c9c922",
            "entitlement": null,
            "install_base": "a1731551d1f53110f8776589fa411f8d",
            "added": "2023-12-03",
            "removed": "2023-12-03"
          }
        ],
        "entitlement_characteristics": [
          {
            "sys_id": "3a00c975bb49412cae169200c7f6236e",
            "sys_created_by": "admin",
            "sys_updated_by": "admin",
            "sys_created_on": "2023-10-09 11:27:29",
            "sys_updated_on": "2023-10-09 11:27:29",
            "service_contract_line": "3a39ecdc01154f4ab782da0169c9c922",
            "entitlement": null,
            "characteristic_option": "495149b7539e61106bfcddeeff7b1262",
            "value": "5",
            "characteristic": "63418db7539e61106bfcddeeff7b1238",
            "type": "coverage"
          }
        ]
      }
    ],
    "entitlements": [
      {
        "sys_id": "16e419d1d1f53110f8776589fa411f3c",
        "sys_created_by": "admin",
        "sys_updated_by": "admin",
        "sys_created_on": "2023-10-09 11:29:48",
        "sys_updated_on": "2023-10-09 11:29:48",
        "entitlement_name": "ENTL 2",
        "account": "4c325111d1f53110f8776589fa411f3d",
        "consumer": null,
        "household": null,
        "contract": "a4b415d1d1f53110f8776589fa411f20",
        "service_contract_line": "16e451d1d1f53110f8776589fa411f80",
        "state": "active",
        "product_offering": null,
        "product_specification": null,
        "sold_entitlement": null,
        "product": null,
        "start_date": "2022-12-03",
        "end_date": "",
        "sold_products_covered": [
          {
            "sys_id": "1ae419d1d1f53110f8776589fa411f3d",
            "sys_created_by": "admin",
            "sys_updated_by": "admin",
            "sys_created_on": "2023-10-09 11:29:48",
            "sys_updated_on": "2023-10-09 11:29:48",
            "contract": "a4b415d1d1f53110f8776589fa411f20",
            "service_contract_line": "16e451d1d1f53110f8776589fa411f80",
            "entitlement": "16e419d1d1f53110f8776589fa411f3c",
            "sold_product": "da23d151d1f53110f8776589fa411f27",
            "added": "",
            "removed": ""
          }
        ],
        "install_base_items_covered": [],
        "entitlement_characteristics": [
          {
            "sys_id": "1ae419d1d1f53110f8776589fa411f3e",
            "sys_created_by": "admin",
            "sys_updated_by": "admin",
            "sys_created_on": "2023-10-09 11:29:48",
            "sys_updated_on": "2023-10-09 11:29:48",
            "service_contract_line": null,
            "entitlement": "16e419d1d1f53110f8776589fa411f3c",
            "characteristic_option": "495149b7539e61106bfcddeeff7b1262",
            "value": "5",
            "characteristic": "63418db7539e61106bfcddeeff7b1238",
            "type": "coverage_and_usage",
            "entitlement_usage": [
              {
                "sys_id": "56e419d1d1f53110f8776589fa411f3f",
                "sys_created_by": "admin",
                "sys_updated_by": "admin",
                "sys_created_on": "2023-10-09 11:29:48",
                "sys_updated_on": "2023-10-09 11:29:48",
                "entitlement": "16e419d1d1f53110f8776589fa411f3c",
                "service_contract_line": null,
                "entitlement_characteristic": "1ae419d1d1f53110f8776589fa411f3e",
                "period_start": "2022-12-03",
                "period_end": "",
                "total_units": "5",
                "used_units": "2"
              }
            ]
          }
        ]
      }
    ],
    "sold_products_covered": [
      {
        "sys_id": "5ae451d1d1f53110f8776589fa411f81",
        "sys_created_by": "admin",
        "sys_updated_by": "admin",
        "sys_created_on": "2023-10-09 11:29:47",
        "sys_updated_on": "2023-10-09 11:29:47",
        "contract": "a4b415d1d1f53110f8776589fa411f20",
        "service_contract_line": "16e451d1d1f53110f8776589fa411f80",
        "entitlement": null,
        "sold_product": "0df21151d1f53110f8776589fa411f1b",
        "added": "2023-12-03",
        "removed": "2023-12-03"
      }
    ],
    "install_base_items_covered": [],
    "entitlement_characteristics": [
      {
        "sys_id": "dae451d1d1f53110f8776589fa411f82",
        "sys_created_by": "admin",
        "sys_updated_by": "admin",
        "sys_created_on": "2023-10-09 11:29:47",
        "sys_updated_on": "2023-10-09 11:29:47",
        "service_contract_line": "16e451d1d1f53110f8776589fa411f80",
        "entitlement": null,
        "characteristic_option": "495149b7539e61106bfcddeeff7b1262",
        "value": "5",
        "characteristic": "63418db7539e61106bfcddeeff7b1238",
        "type": "coverage"
      }
    ]
  }
}
```

## Service Contract - POST /sn\_pss\_core/servicecontract

Creates a service contract record and all its related entities from a specified payload.

The Service Contract API stores data in various tables. The following is the list of tables in which records are created by this endpoint when creating a service contract:

-   Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]
-   Entitlement \[service\_entitlement\]
-   Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]
-   Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\] - This table contains information for both sold products covered and install base items covered.
-   Service Contract \[sn\_pss\_core\_service\_contract\]
-   Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

The request body of this endpoint references fields in the following tables. This information needs to be added to your instance before utilizing this API. For additional information, see [Create service contracts](https://www.servicenow.com/docs/access?context=create-csm-service-contracts&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

-   Account \[customer\_account\]
-   Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]
-   Consumer \[csm\_consumer\]
-   Household \[csm\_household\]

### URL format

Versioned URL: `/api/sn_pss_core/{api_version}/servicecontract`

Default URL: `/api/sn_pss_core/servicecontract`

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

Required if the **consumer** parameter is not specified. Sys\_id of the account record to which the service contract belongs.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

consumer

</td><td>

Required if the **account** parameter is not specified. Sys\_id of the consumer record to which the service contract belongs.

Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

ends

</td><td>

Date on which the service contract ends.

Data type: String

Format: yyyy-mm-dd

 Default: Never ends until manually removed.

</td></tr><tr><td>

household

</td><td>

Only valid for consumer service contracts. Sys\_id of the household associated with the service contract.

Data type: String

Table: Household \[csm\_household\]

Default: null \(no household\)

</td></tr><tr><td>

install\_base\_items\_covered

</td><td>

List of install base items covered under the service contract.For more information on Install Base Items [Configure Install base](https://www.servicenow.com/docs/access?context=configure-install-base&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

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

Stored in: The Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\] table.

</td></tr><tr><td>

install\_base\_items\_covered.added

</td><td>

Date that the associated service contract starts to cover the install base item.

Data type: String

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

Date that the associated service contract ends coverage of the install base item.

Data type: String

Format: yyyy-mm-dd

 Default: No end date

</td></tr><tr><td>

service\_contract\_lines

</td><td>

List of service contract lines associated with the service contract.Data type: Array of Objects

```
"service_contract_lines": [
  {
    "child_contract_lines": [Array],
    "ends": "String",
    "entitlements": [Array],
    "entitlement_characteristics": [Array],
    "install_base_items_covered": [Array],
    "name": "String",
    "number": "String",
    "product_model": "String",
    "product_offering": "String",
    "product_specification": "String",
    "sold_product": "String",
    "sold_products_covered": [Array],
    "starts": "String",
    "state": "String"
  }
]
```

Stored in: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines

</td><td>

List of child service contract lines under the service contract line.Data type: Array of Objects

```
"child_contract_lines": [
  {
    "child_contract_lines": [Array],
    "ends": "String",
    "entitlements": [Array],
    "entitlement_characteristics": [Array],
    "install_base_items_covered": [Array],
    "name": "String",
    "product_model": "String",
    "product_offering": "String",
    "product_specification": "String",
    "sold_product": "String",
    "sold_products_covered": [Array],
    "starts": "String",
    "state": "String"
  }
]
```

Stored in: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​child\_contract\_lines

</td><td>

List of child service contract line objects to create under the child service contract line. The objects in this array have the same elements as the objects in the **service\_contract\_lines.child\_contract\_lines** parameter.Data type: Array of Objects

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​ends

</td><td>

Date on which the service contract line ends.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements

</td><td>

List of entitlements to associate with the child service contract line.Data type: Array of Objects

```
"entitlements:" [
  {
    "account": "String",
    "consumer": "String",
    "end_date": "String",
    "entitlement_characteristics": [Array],
    "entitlement_name": "String",
    "household": "String",
    "install_base_items_covered": [Array],
    "product": "String",
    "product_offering": "String",
    "product_specification": "String",
    "sold_entitlement": "String",
    "sold_products_covered": [Array],
    "start_date": "String",
    "state": "String"
  }
]
```

Stored in: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​account

</td><td>

Sys\_id of the account record to which the entitlement belongs.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​consumer

</td><td>

Sys\_id of the consumer record to which the entitlement belongs.

Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​end\_date

</td><td>

End date of the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics

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

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.characteristic

</td><td>

Required. Sys\_id of the characteristic record associated with the entitlement.

Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.characteristic\_option

</td><td>

Sys\_id of the characteristic option record associated with the entitlement.Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.entitlement\_usage

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

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.entitlement\_usage.​used\_units

</td><td>

Usage of the associated entitlement characteristic.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.type

</td><td>

Type of entitlement characteristic. Valid values:

-   coverage
-   coverage\_and\_usage

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.value

</td><td>

Required if the **input\_type** parameter contained in the record specified in the **entitlement\_characteristics.characteristic** parameter, is not `choice`.Value of the characteristic.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_name

</td><td>

Required. Name of the entitlement.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​household

</td><td>

Only passed when the household plugins are active and the **consumer** parameter is passed. Sys\_id of the household record associated with the entitlement.

Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered

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

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​added

</td><td>

Date that the associated install base item was added to the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the install base item covered by the entitlement.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​removed

</td><td>

Date that the associated install base item was removed from the entitlement.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​product

</td><td>

Sys\_id of the product model record associated with the entitlement.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​product\_offering

</td><td>

Sys\_id of the product offering record associated with the entitlement.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​product\_specification

</td><td>

Sys\_id of the product specification record associated with the entitlement.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_entitlement

</td><td>

Sys\_id of the sold product record associated with the entitlement.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_products\_covered

</td><td>

List of sold products covered under the entitlement. Data type: Array of Objects

```
"sold_products_covered": [ 
  {
    "added": "String",
    "removed": "String",
    "sold_product": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_products\_covered.​added

</td><td>

Date that the associated sold product was added to the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_products\_covered.​removed

</td><td>

Date that the associated sold product was removed from the entitlement.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​start\_date

</td><td>

Required. Start date of the entitlement.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​state

</td><td>

Required.Current state of the entitlement.

Valid values: \(case-sensitive\)

-   active
-   cancelled
-   draft
-   expired
-   suspended

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics

</td><td>

List of characteristics associated with the service contract line.Data type: Array of Objects

```
"entitlement_characteristics" [
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

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.characteristic

</td><td>

Required. Sys\_id of the characteristic record associated with the service contract line.

Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.characteristic\_option

</td><td>

Sys\_id of the characteristic option record associated with the service contract line.

Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.entitlement\_usage

</td><td>

Used unit value for the associated service contract line characteristic.Data type: Object

```
"entitlement_usage": {
    "used_units": "String"
}
```

Stored in: Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.entitlement\_usage.​usage\_units

</td><td>

Usage of the associated entitlement characteristic.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.type

</td><td>

Type of service contract line characteristic. Valid values:

-   coverage
-   coverage \_and\_usage

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.value

</td><td>

Required if the **entitlement\_characteristics.type** parameter is not passed. Value of the characteristic.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered

</td><td>

List of install base items covered under the  service contract line.

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

Stored in: Sold Product Covered  \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered.​added

</td><td>

Date that the associated install base item was added to the service contract line.

Data type: String

 Format: yyyy-mm-dd

 Default: Current date

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the install base item covered by the service contract line.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered.​removed

</td><td>

Date that the associated service contract line ends coverage of the install base item.

Data type: String

 Format: yyyy-mm-dd

 Default: No end date

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​name

</td><td>

Name of the service contract line.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​product\_model

</td><td>

Sys\_id of the product associated with the service contract line.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​product\_offering

</td><td>

Sys\_id of the product offering record associated with the service contract line.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​product\_specification

</td><td>

Sys\_id of the product specification record associated with the service contract line.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_product

</td><td>

Sys\_id of the sold product record associated with the service contract line.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered

</td><td>

List of products covered under the service contract line.

Data type: Array of Objects

 ```
"sold_products_covered": [ 
  {
    "added": "String",
    "removed": "String",
    "sold_product": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​.sold\_products\_covered.​added

</td><td>

Date that the associated service contract line starts to cover the associated product.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered.​removed

</td><td>

Date that the associated service contract line ends coverage of the associated product.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered.​sold\_product

</td><td>

Sys\_id of a product associated with the service contract line.

Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​starts

</td><td>

Required. Start date of the service contract line.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​state

</td><td>

Required.Current state of the contract line.

Valid values: \(case-sensitive\)

-   active
-   cancelled
-   draft
-   expired
-   suspended

Data type: String

</td></tr><tr><td>

service\_contract\_lines.ends

</td><td>

Date on which the service contract line ends.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

service\_contract\_lines.entitlements

</td><td>

List of entitlements to associate with the service contract line. These entitlements are inserted in the Entitlement \[service\_entitlement\] table.Data type: Array of Objects

```
"entitlements:" [
  {
    "account": "String",
    "consumer": "String",
    "end_date": "String",
    "entitlement_characteristics": [Array],
    "entitlement_name": "String",
    "household": "String",
    "install_base_items_covered": [Array],
    "product": "String",
    "product_offering": "String",
    "product_specification": "String",
    "sold_entitlement": "String",
    "sold_products_covered": [Array],
    "start_date": "String",
    "state": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​account

</td><td>

Sys\_id of the account record to which the entitlement belongs.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​consumer

</td><td>

Sys\_id of the consumer record to which the entitlement belongs.

Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​end\_date

</td><td>

End date of the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics

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

service\_contract\_lines.​entitlements.​entitlement\_characteristics.characteristic

</td><td>

Required. Sys\_id of the characteristic record associated with the entitlement.

Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.characteristic\_option

</td><td>

Sys\_id of the characteristic option record associated with the entitlement.Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.entitlement\_usage

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

service\_contract\_lines.​entitlements.​entitlement\_characteristics.entitlement\_usage.​usage\_units

</td><td>

Usage of the associated entitlement characteristic.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.type

</td><td>

Type of entitlement characteristic. Valid values:

-   coverage
-   coverage\_and\_usage

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.value

</td><td>

Required if the **input\_type** parameter contained in the record specified in the **entitlement\_characteristics.characteristic** parameter, is not `choice`.Value of the characteristic.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_name

</td><td>

Required. Name of the entitlement.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​household

</td><td>

Only passed when the household plugins are active and the **consumer** parameter is passed. Sys\_id of the household record associated with the entitlement.

Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​install\_base\_items\_covered

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

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​install\_base\_items\_covered.​added

</td><td>

Date that the associated install base item was added to the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the install base item covered by the entitlement.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​install\_base\_items\_covered.​removed

</td><td>

Date that the associated install base item was removed from the entitlement.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​product

</td><td>

Sys\_id of the product model record associated with the entitlement.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​product\_offering

</td><td>

Sys\_id of the product offering record associated with the entitlement.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​product\_specification

</td><td>

Sys\_id of the product specification record associated with the entitlement.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_entitlement

</td><td>

Sys\_id of the sold product record associated with the entitlement.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_products\_covered

</td><td>

List of sold products covered under the entitlement. Data type: Array of Objects

```
"sold_products_covered": [ 
  {
    "added": "String",
    "removed": "String",
    "sold_product": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_products\_covered.​added

</td><td>

Date that the associated sold product was added to the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_products\_covered.​removed

</td><td>

Date that the associated sold product was removed from the entitlement.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_products\_covered.​sold\_product

</td><td>

Sys\_id of a product associated with the entitlement.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​start\_date

</td><td>

Required. Start date of the entitlement.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​state

</td><td>

Required.Current state of the entitlement.

Valid values: \(case-sensitive\)

-   active
-   cancelled
-   draft
-   expired
-   suspended

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics

</td><td>

List of characteristics associated with the service contract line.Data type: Array of Objects

```
"entitlement_characteristics" [
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

service\_contract\_lines.​entitlement\_characteristics.​characteristic

</td><td>

Required. Sys\_id of the characteristic record associated with the service contract line.

Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​characteristic\_option

</td><td>

Sys\_id of the characteristic option record associated with the service contract line.

Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage

</td><td>

Used unit value for the associated service contract line characteristic.Data type: Object

```
"entitlement_usage": {
    "used_units": "String"
}
```

Stored in: Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​usage\_units

</td><td>

Usage of the associated entitlement characteristic.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​type

</td><td>

Type of service contract line characteristic. Valid values:

-   coverage
-   coverage \_and\_usage

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​value

</td><td>

Required if the **entitlement\_characteristics.type** parameter is not passed. Value of the characteristic.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​install\_base\_items\_covered

</td><td>

List of install base items covered under the  service contract line.

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

Stored in: Sold Product Covered  \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​install\_base\_items\_covered.​added

</td><td>

Date that the associated install base item was added to the service contract line.

Data type: String

 Format: yyyy-mm-dd

 Default: Current date

</td></tr><tr><td>

service\_contract\_lines.​install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the install base item covered by the service contract line.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

service\_contract\_lines.​install\_base\_items\_covered.​removed

</td><td>

Date that the associated service contract line ends coverage of the install base item.

Data type: String

 Format: yyyy-mm-dd

 Default: No end date

</td></tr><tr><td>

service\_contract\_lines.​name

</td><td>

Name of the service contract line.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​product\_model

</td><td>

Sys\_id of the product associated with the service contract line.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

service\_contract\_lines.​product\_offering

</td><td>

Sys\_id of the product offering record associated with the service contract line.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

service\_contract\_lines.​product\_specification

</td><td>

Sys\_id of the product specification record associated with the service contract line.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

service\_contract\_lines.​sold\_product

</td><td>

Sys\_id of the sold product record associated with the service contract line.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​sold\_products\_covered

</td><td>

List of products covered under the service contract line.

Data type: Array of Objects

 ```
"sold_products_covered": [ 
  {
    "added": "String",
    "removed": "String",
    "sold_product": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​sold\_products\_covered.​added

</td><td>

Date that the associated service contract line starts to cover the associated product.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

service\_contract\_lines.​sold\_products\_covered.​removed

</td><td>

Date that the associated service contract line ends coverage of the associated product.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

service\_contract\_lines.​sold\_products\_covered.​sold\_product

</td><td>

Sys\_id of a product associated with the service contract line.

Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​starts

</td><td>

Required. Start date of the service contract line.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

service\_contract\_lines.​state

</td><td>

Required.Current state of the contract line.

Valid values: \(case-sensitive\)

-   active
-   cancelled
-   draft
-   expired
-   suspended

Data type: String

</td></tr><tr><td>

short\_description

</td><td>

Brief description or name of the service contract.

Data type: String

 Default: null \(empty string\)

</td></tr><tr><td>

sold\_products\_covered

</td><td>

Required if the **install\_base\_items\_covered** parameter is not specified. List of products covered under the service contract. The data in this parameter is inserted in the Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\] table.

Data type: Array of Objects

```
"sold_products_covered": [ 
  {
    "added": "String",
    "removed": "String",
    "sold_product": "String"
  }
]
```

</td></tr><tr><td>

sold\_products\_covered.added

</td><td>

Date that the associated service contract starts to cover the product.

Data type: String

 Format: yyyy-mm-dd

 Default: Current date

</td></tr><tr><td>

sold\_products\_covered.removed

</td><td>

Date that the associated service contract ends coverage of the associated product.

Data type: String

 Format: yyyy-mm-dd

 Default: No end date

</td></tr><tr><td>

sold\_products\_covered.sold\_product

</td><td>

Sys\_id of the product covered by the service contract.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

starts

</td><td>

Required.Date on which the service contract begins.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

state

</td><td>

Required.Current state of the service contract.

Valid values: \(case-sensitive\)

-   active
-   cancelled
-   draft
-   expired

Data type: String

</td></tr><tr><td>

vendor\_contract

</td><td>

Required.Unique identifier for an associated external contract.

Data type: String

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

|Status code|Description|
|-----------|-----------|
|201|Successful. The request was successfully processed and the records were created.|
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have permission to access the API.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

install\_base\_items\_covered

</td><td>

List of sys\_ids of the install base items covered under the service contract. Data type: Array of Objects

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

Sys\_id of the install base item covered.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

number

</td><td>

Auto-generated service contract number.Data type: String

</td></tr><tr><td>

service\_contract\_lines

</td><td>

List of service contract lines associated with the service contract.Data type: Array of Objects

```
"service_contract_lines": [
  {
    "child_contract_lines": [Array],
    "entitlements": [Array],
    "entitlement_characteristics": [Array],
    "install_base_items_covered": [Array],
    "name": "String",
    "number": "String",
    "sold_products_covered": [Array],
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines

</td><td>

List of child service contract line objects created under the service contract line.Data type: Array of Objects

```
"child_contract_lines": [
  {
    "child_contract_lines": [Array],
    "entitlements": [Array],
    "entitlement_characteristics": [Array],
    "install_base_items_covered": [Array],
    "name": "String",
    "number": "String",
    "sold_products_covered": [Array],
    "sys_id" "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​child\_contract\_lines

</td><td>

List of child service contract line objects created under the child service contract line. The objects in this array have the same elements as the **service\_contract\_lines.child\_contract\_lines** parameter.Data type: Array of Objects

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements

</td><td>

List of entitlements associated with the child service contract line.Data type: Array of Objects

```
"entitlements": [
  {
    "entitlement_name": "String",
    "entitlement_characteristics": [Array],
    "install_base_items_covered": [Array],
    "sold_products_covered": [Array],
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_name

</td><td>

Name of the entitlement.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics

</td><td>

List of the entitlement characteristic objects  created under the entitlement. Data type: Array of Objects

```
"entitlement_characteristics": [
  {
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​entitlement\_characteristics.​sys\_id

</td><td>

Sys\_id of an entitlement characteristics record associated with the child service contract line.Data type: String

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered

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

service\_contract\_lines.​child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_id

</td><td>

Sys\_id of a install base items covered by the entitlement.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_products\_covered

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

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sold\_products\_covered.​sys\_id

</td><td>

Sys\_id of a product associated with the entitlement.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlements.​sys\_id

</td><td>

Sys\_id of the entitlement record associated with the child service contract line.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics

</td><td>

List of characteristics associated with the chile contract line. Data type: Array of Objects

```
"entitlement_characteristics": [
  {
    "entitlement_usage": {Object},
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage

</td><td>

Entitlement usage object inserted under the entitlement\_characteristic.Data type: Object

```
"entitlement_usage": {
    "sys_id": "String"
}
```

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​sys\_id

</td><td>

Sys\_id of the entitlement usage record.Data type: String

Table: Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​entitlement\_characteristics.​sys\_id

</td><td>

Sys\_id of a entitlement characteristics record associated with the child service contract line.Data type: String

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered

</td><td>

List of sys\_ids of the install base items covered under the child contract line. Data type: Array of Objects

```
"install_base_items_covered": [ 
  {
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​install\_base\_items\_covered.​sys\_id

</td><td>

Sys\_id of the install base item covered.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​name

</td><td>

Name of the child service contract line.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​number

</td><td>

Unique number of the service contract line. Automatically generated by the endpoint. For example: CTRL000001.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered

</td><td>

List of sys\_ids of the products covered under the child service contract line. Data type: Array of Objects

```
"sold_products_covered": [ 
  {
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sold\_products\_covered.​sys\_id

</td><td>

Sys\_id of a product covered by the child service contract line.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​child\_contract\_lines.​sys\_id

</td><td>

Sys\_id of a child service contract line record.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements

</td><td>

List of entitlements associated with the service contract.Data type: Array of Objects

```
"entitlements" [
  {
    "entitlement_name": "String",
    "entitlement_characteristics": [Array],
    "install_base_items_covered": [Array],
    "sold_products_covered": [Array],
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_name

</td><td>

Name of the entitlement.

Data type: String

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics

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

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage

</td><td>

Entitlement usage object inserted under the entitlement\_characteristic.Data type: Object

```
"entitlement_usage": {
    "sys_id": "String"
}
```

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_id

</td><td>

Sys\_id of the entitlement usage record.Data type: String

Table: Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​entitlement\_characteristics.​sys\_id

</td><td>

Sys\_id of a entitlement characteristics record associated with the service contract line.Data type: String

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​install\_base\_items\_covered

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

service\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_id

</td><td>

Sys\_id of a install base items covered by the entitlement.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sold\_products\_covered

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

service\_contract\_lines.​entitlements.​sold\_products\_covered.​sys\_id

</td><td>

Sys\_id of a product associated with the entitlement.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​entitlements.​sys\_id

</td><td>

Sys\_id of the entitlement record associated with the service contract line.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics

</td><td>

List of characteristics associated with the chile contract line. Data type: Array of Objects

```
"entitlement_characteristics": [
  {
    "entitlement_usage": {Object},
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage

</td><td>

Entitlement usage object inserted under the entitlement\_characteristic.Data type: Object

```
"entitlement_usage": {
    "sys_id": "String"
}
```

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​sys\_id

</td><td>

Sys\_id of the entitlement usage record.Data type: String

Table: Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

service\_contract\_lines.​entitlement\_characteristics.​sys\_id

</td><td>

Sys\_id of a entitlement characteristics record associated with the child service contract line.Data type: String

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

service\_contract\_lines.​install\_base\_items\_covered

</td><td>

List of sys\_ids of the install base items covered under the child contract line. Data type: Array of Objects

```
"install_base_items_covered": [ 
  {
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​install\_base\_items\_covered.​sys\_id

</td><td>

Sys\_id of the install base item covered.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​name

</td><td>

Name of the child service contract line.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​number

</td><td>

Unique number of the service contract line. Automatically generated by the endpoint. For example: CTRL000001.Data type: String

</td></tr><tr><td>

service\_contract\_lines.​sold\_products\_covered

</td><td>

List of sys\_ids of the products covered under the service contract line. Data type: Array of Objects

```
"sold_products_covered": [ 
  {
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

service\_contract\_lines.​sold\_products\_covered.​sys\_id

</td><td>

Sys\_id of a product covered by the service contract line.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

service\_contract\_lines.​sys\_id

</td><td>

Sys\_id of a service contract line record.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

short\_description

</td><td>

Brief description or name of the service contract.

Data type: String

</td></tr><tr><td>

sold\_products\_covered

</td><td>

List of sys\_ids of the products covered under the service contract. Data type: Array of Objects

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

Sys\_id of a product covered by the service contract.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the service contract record.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr></tbody>
</table>### cURL request

The following is a code example that shows how to call this endpoint and create a service contract with one sold product covered record, one install base items covered record, and two service contract lines.

```
curl "https://instance.servicenow.com/api/sn_pss_core/servicecontract" \
--request POST \
--header "Accept:application/json" \
--data
{
  "state": "active",
  "account": "4c325111d1f53110f8776589fa411f3d",
  "vendor_contract": "External Reference",
  "starts": "2022-12-03",
  "service_contract_lines": [
    {
      "state": "active",
      "name": "CLI",
      "starts": "2022-12-03",
      "child_contract_lines": [
        {
          "state": "active",
          "name": "Child CLI",
          "starts": "2022-12-03",
          "entitlements": [
            {
              "state": "active",
              "entitlement_name": "Child CLI - ENTL",
              "start_date": "2022-12-03"
            }
          ],
          "sold_products_covered": [
            {
              "sold_product": "8db4258949f14ef7b90d90822dfc5800",
              "added": "2023-12-03",
              "removed": "2023-12-03"
            }
          ],
          "install_base_items_covered": [
            {
              "install_base": "2f270832699b46e78aa899a5a5dc6682",
              "added": "2023-12-03",
              "removed": "2023-12-03"
            }
          ],
          "entitlement_characteristics": [
            {
              "characteristic": "63418db7539e61106bfcddeeff7b1238",
              "characteristic_option": "495149b7539e61106bfcddeeff7b1262",
              "value": "20",
              "type": "coverage"
            }
          ]
        }
      ],
      "entitlements": [
        {
          "state": "active",
          "entitlement_name": "ENTL",
          "start_date": "2022-12-03",
          "sold_products_covered": [
            {
              "sold_product": "da23d151d1f53110f8776589fa411f27"
            }
          ],
          "install_base_items_covered": [
            {
              "install_base": "43739151d1f53110f8776589fa411fc1",
              "added": "2023-12-03",
              "removed": "2023-12-03"
            }
          ],
          "entitlement_characteristics": [
            {
              "characteristic": "63418db7539e61106bfcddeeff7b1238",
              "characteristic_option": "495149b7539e61106bfcddeeff7b1262",
              "value": "20",
              "type": "coverage_and_usage",
              "entitlement_usage": {
                "used_units": "3"
              }
            }
          ]
        }
      ],
      "sold_products_covered": [
        {
          "sold_product": "ec235d9dd1b53110f8776589fa411fe2",
          "added": "2023-12-03",
          "removed": "2023-12-03"
        }
      ],
      "install_base_items_covered": [
        {
          "install_base": "a1731551d1f53110f8776589fa411f8d",
          "added": "2023-12-03",
          "removed": "2023-12-03"
        }
      ],
      "entitlement_characteristics": [
        {
          "characteristic": "63418db7539e61106bfcddeeff7b1238",
          "characteristic_option": "495149b7539e61106bfcddeeff7b1262",
          "value": "20",
          "type": "coverage"
        }
      ]
    },
    {
      "state": "active",
      "name": "CLI 2",
      "starts": "2022-12-03",
      "sold_products_covered": [
        {
          "sold_product": "7f23995dd1b53110f8776589fa411f66",
          "added": "2023-12-03",
          "removed": "2023-12-03"
        }
      ],
      "install_base_items_covered": [
        {
          "install_base": "a483d951d1f53110f8776589fa411fad",
          "added": "2023-12-03",
          "removed": "2023-12-03"
        }
      ],
      "entitlement_characteristics": [
        {
          "characteristic": "63418db7539e61106bfcddeeff7b1238",
          "characteristic_option": "495149b7539e61106bfcddeeff7b1262",
          "value": "20",
          "type": "coverage"
        }
      ]
    }
  ],
  "sold_products_covered": [
    {
      "sold_product": "0df21151d1f53110f8776589fa411f1b",
      "added": "2023-12-03",
      "removed": "2023-12-03"
    }
  ],
  "install_base_items_covered": [
    {
      "install_base": "e2639951d1f53110f8776589fa411f2b",
      "added": "2023-12-03",
      "removed": "2023-12-03"
    }
  ]
} 
--user "username":"password"
```

Response:

```
{
  "result": {
    "sys_id": "d8641151d1f53110f8776589fa411fde",
    "number": "CNTR0010004",
    "short_description": null,
    "service_contract_lines": [
      {
        "sys_id": "d4641d91d1f53110f8776589fa411fbb",
        "name": "CLI",
        "number": "CTRL0000001,                                                                                                 
        "child_contract_lines": [
          {
            "sys_id": "3a39ecdc01154f4ab782da0169c9c922",
            "name": "Child CLI",
            "number": "CTRL0000002",
            "child_contract_lines": [],
            "entitlements": [
              {
                "sys_id": "7439fd84c2494ba6951e58f333cfe8d4",
                "entitlement_name": "Child CLI - ENTL",
                "sold_products_covered": [],
                "install_base_items_covered": [],
                "entitlement_characteristics": []
              }
            ],
            "sold_products_covered": [
              {
                "sys_id": "dfb62e9c4c6843009be02a68f65b9118"
              }
            ],
            "install_base_items_covered": [
              {
                "sys_id": "2583912e81964501b52a2e44d4797a28"
              }
            ],
            "entitlement_characteristics": [
              {
                "sys_id": "3a00c975bb49412cae169200c7f6236e",
                "entitlement_usage": {}
              }
            ]
          }
        ],
        "entitlements": [
          {
            "sys_id": "a8641d91d1f53110f8776589fa411fc0",
            "entitlement_name": "ENTL",
            "sold_products_covered": [
              {
                "sys_id": "a0641d91d1f53110f8776589fa411fc2"
              }
            ],
            "install_base_items_covered": [
              {
                "sys_id": "e0641d91d1f53110f8776589fa411fc3"
              }
            ],
            "entitlement_characteristics": [
              {
                "sys_id": "a8641d91d1f53110f8776589fa411fd0",
                "entitlement_usage": {
                  "sys_id": "a8641d91d1f53110f8776589fa411fd1"
                }
              }
            ]
          }
        ],
        "sold_products_covered": [
          {
            "sys_id": "98641d91d1f53110f8776589fa411fbc"
          }
        ],
        "install_base_items_covered": [
          {
            "sys_id": "58641d91d1f53110f8776589fa411fbd"
          }
        ],
        "entitlement_characteristics": [
          {
            "sys_id": "e0641d91d1f53110f8776589fa411fbf",
            "entitlement_usage": {}
          }
        ]
      },
      {
        "sys_id": "e4641d91d1f53110f8776589fa411fd2",
        "name": "CLI 2",
        "number": "CTRL0000003",
        "child_contract_lines": [],
        "entitlements": [],
        "sold_products_covered": [
          {
            "sys_id": "e8641d91d1f53110f8776589fa411fd3"
          }
        ],
        "install_base_items_covered": [
          {
            "sys_id": "a8641d91d1f53110f8776589fa411fd4"
          }
        ],
        "entitlement_characteristics": [
          {
            "sys_id": "a8641d91d1f53110f8776589fa411fd5",
            "entitlement_usage": {}
          }
        ]
      }
    ],
    "sold_products_covered": [
      {
        "sys_id": "9c641d91d1f53110f8776589fa411fb9"
      }
    ],
    "install_base_items_covered": [
      {
        "sys_id": "d8641d91d1f53110f8776589fa411fba"
      }
    ]
  }
}
```

## Service Contract - POST /sn\_pss\_core/servicecontract/contractline

Creates a contract line record and all of its related entities.

This endpoint stores data in the following tables when processing the request:

-   Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]
-   Entitlement \[service\_entitlement\]
-   Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]
-   Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\] - This table contains information for both sold products covered and install base items covered.
-   Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

### URL format

Versioned URL: `/api/sn_pss_core/{api_version}/servicecontract/contractline`

Default URL: `/api/sn_pss_core/servicecontract/contractline`

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

child\_contract\_lines

</td><td>

List of child service contract line objects created under the service contract line. Data type: Array of Objects

```
"child_contract_lines": [
  {
    "child_contract_lines": [Array],
    "contract": "String",
    "ends": "String",
    "entitlements": [Array],
    "entitlement_characteristics": [Array],
    "install_base_items_covered": [Array],
    "name": "String",
    "parent_contract_line": "String",
    "product_model": "String",
    "product_offering": "String",
    "product_specification": "String",
    "sold_product": "String",
    "sold_products_covered": [Array],
    "starts": "String",
    "state": "String"
  }
]
```

Stored in: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

child\_contract\_lines.​child\_contract\_lines

</td><td>

List of child service contract line objects to create under the child service contract line. The objects in this array have the same elements as the objects in the **child\_contract\_lines** parameter.Data type: Array of Objects

</td></tr><tr><td>

child\_contract\_lines.​contract

</td><td>

Sys\_id of the service contract associated with the child service contract line.Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

child\_contract\_lines.​ends

</td><td>

Date on which the child service contract line ends.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

child\_contract\_lines.​entitlements

</td><td>

List of entitlements associated with the child service contract line.Data type: Array of Objects

```
"entitlements:" [
  {
    "account": "String",
    "consumer": "String",
    "end_date": "String",
    "entitlement_characteristics": [Array],
    "entitlement_name": "String",
    "household": "String",
    "install_base_items_covered": [Array],
    "product": "String",
    "product_offering": "String",
    "product_specification": "String",
    "sold_entitlement": "String",
    "sold_products_covered": [Array],
    "start_date": "String",
    "state": "String"
  }
]
```

Stored in: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​account

</td><td>

Required if the **consumer** parameter is not passed.Sys\_id of the account record to which the entitlement belongs.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​consumer

</td><td>

Required if the **account** parameter is not passed.Sys\_id of the consumer record to which the entitlement belongs.

Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​end\_date

</td><td>

End date of the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics

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

child\_contract\_lines.​entitlements.​entitlement\_characteristics.characteristic

</td><td>

Required. Sys\_id of the characteristic record associated with the entitlement.

Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.characteristic\_option

</td><td>

Sys\_id of the characteristic option record associated with the entitlement.Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.entitlement\_usage

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

child\_contract\_lines.​entitlements.​entitlement\_characteristics.entitlement\_usage.​used\_units

</td><td>

Usage of the associated entitlement characteristic.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.type

</td><td>

Type of entitlement characteristic. Valid values:

-   coverage
-   coverage\_and\_usage

Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.value

</td><td>

Required if the **input\_type** parameter contained in the record specified in the **entitlement\_characteristics.characteristic** parameter, is not `choice`.Value of the characteristic.

Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_name

</td><td>

Required. Name of the entitlement.

Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​household

</td><td>

Only passed when the household plugins are active and the **consumer** parameter is passed. Sys\_id of the household record associated with the entitlement.

Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​install\_base\_items\_covered

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

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​added

</td><td>

Date that the associated install base item was added to the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the install base item covered by the entitlement.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​removed

</td><td>

Date that the associated install base item was removed from the entitlement.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​product

</td><td>

Sys\_id of the product model record associated with the entitlement.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​product\_offering

</td><td>

Sys\_id of the product offering record associated with the entitlement.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​product\_specification

</td><td>

Sys\_id of the product specification record associated with the entitlement.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_entitlement

</td><td>

Sys\_id of the sold product record associated with the entitlement.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_products\_covered

</td><td>

List of sold products covered under the entitlement. Data type: Array of Objects

```
"sold_products_covered": [ 
  {
    "added": "String",
    "removed": "String",
    "sold_product": "String"
  }
]
```

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_products\_covered.​added

</td><td>

Date that the associated sold product was added to the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_products\_covered.​removed

</td><td>

Date that the associated sold product was removed from the entitlement.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_products\_covered.​sold\_product

</td><td>

Sys\_id of a product associated with the entitlement.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​start\_date

</td><td>

Required. Start date of the entitlement.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​state

</td><td>

Required.Current state of the entitlement.

Valid values: \(case-sensitive\)

-   active
-   cancelled
-   draft
-   expired
-   suspended

Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics

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

child\_contract\_lines.​entitlement\_characteristics.​characteristic

</td><td>

Sys\_id of the characteristic record associated with the entitlement.

Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​characteristic\_option

</td><td>

Sys\_id of the characteristic option record associated with the entitlement.Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage

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

child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​used\_units

</td><td>

Usage of the associated entitlement characteristic.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​type

</td><td>

Type of entitlement characteristic. Valid values:

-   coverage
-   coverage\_and\_usage

Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​value

</td><td>

Value of the characteristic.

Data type: String

</td></tr><tr><td>

child\_contract\_lines.​install\_base\_items\_covered

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

</td></tr><tr><td>

child\_contract\_lines.​install\_base\_items\_covered.​added

</td><td>

Date that the associated install base item was added to the child service contract line.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

child\_contract\_lines.​install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the install base item covered by the child service contract line. Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

child\_contract\_lines.​install\_base\_items\_covered.​removed

</td><td>

Date that the associated child service contract line ends coverage of the install base item.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

child\_contract\_lines.​name

</td><td>

Name of the child service contract line.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​parent\_contract\_line

</td><td>

Sys\_id of the parent contract line record associated with the child service contract line.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​product\_model

</td><td>

Sys\_id of the product associated with the child service contract line.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

child\_contract\_lines.​product\_offering

</td><td>

Sys\_id of the product offering record associated with the child service contract line.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

child\_contract\_lines.​product\_specification

</td><td>

Sys\_id of the product specification record associated with the child service contract line.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

child\_contract\_lines.​sold\_product

</td><td>

Sys\_id of the sold product record associated with the child service contract line.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

child\_contract\_lines.​sold\_products\_covered

</td><td>

List of products covered under the child service contract line.Data type: Array of Objects

```
"sold_products_covered": [ 
  {
    "added": "String",
    "removed": "String",
    "sold_product": "String"
  }
]
```

</td></tr><tr><td>

child\_contract\_lines.​sold\_products\_covered.​added

</td><td>

Date that the associated child service contract line starts to cover the associated product.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

child\_contract\_lines.​sold\_products\_covered.​removed

</td><td>

Date that the associated child service contract line ends coverage of the associated product.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

child\_contract\_lines.​sold\_products\_covered.​sold\_product

</td><td>

Sys\_id of a product associated with the child service contract line.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

child\_contract\_lines.​starts

</td><td>

Start date of the child service contract line.Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

child\_contract\_lines.​state

</td><td>

Current state of the contract line.

Valid values: \(case-sensitive\)

-   active
-   cancelled
-   draft
-   expired
-   suspended

Data type: String

</td></tr><tr><td>

contract

</td><td>

Sys\_id of the service contract associated with the service contract line.

Data type: String

Table: Service Contract \[sn\_pss\_core\_service\_contract\]

</td></tr><tr><td>

ends

</td><td>

Date on which the service contract line ends.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

entitlements

</td><td>

List of entitlements to associate with the service contract line. These entitlements are inserted in the Entitlement \[service\_entitlement\] table.Data type: Array of Objects

```
"entitlements:" [
  {
    "account": "String",
    "consumer": "String",
    "end_date": "String",
    "entitlement_characteristics": [Array],
    "entitlement_name": "String",
    "household": "String",
    "install_base_items_covered": [Array],
    "product": "String",
    "product_offering": "String",
    "product_specification": "String",
    "sold_entitlement": "String",
    "sold_products_covered": [Array],
    "start_date": "String",
    "state": "String"
  }
]
```

</td></tr><tr><td>

entitlements.​account

</td><td>

Required if the **consumer** parameter is not passed.Sys\_id of the account record to which the entitlement belongs.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

entitlements.​consumer

</td><td>

Required if the **account** parameter is not passed.Sys\_id of the consumer record to which the entitlement belongs.

Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

entitlements.​end\_date

</td><td>

End date of the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Never ends until manually removed.

</td></tr><tr><td>

entitlements.​entitlement\_characteristics

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

entitlements.​entitlement\_characteristics.characteristic

</td><td>

Required. Sys\_id of the characteristic record associated with the entitlement.

Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.characteristic\_option

</td><td>

Sys\_id of the characteristic option record associated with the entitlement.Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.entitlement\_usage

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

entitlements.​entitlement\_characteristics.entitlement\_usage.​used\_units

</td><td>

Usage of the associated entitlement characteristic.Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.type

</td><td>

Type of entitlement characteristic. Valid values:

-   coverage
-   coverage\_and\_usage

Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.value

</td><td>

Required if the **input\_type** parameter contained in the record specified in the **entitlement\_characteristics.characteristic** parameter, is not `choice`.Value of the characteristic.

Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_name

</td><td>

Required. Name of the entitlement.

Data type: String

</td></tr><tr><td>

entitlements.​household

</td><td>

Only passed when the household plugins are active and the **consumer** parameter is passed. Sys\_id of the household record associated with the entitlement.

Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

entitlements.​install\_base\_items\_covered

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

</td></tr><tr><td>

entitlements.​install\_base\_items\_covered.​added

</td><td>

Date that the associated install base item was added to the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

entitlements.​install\_base\_items\_covered.​removed

</td><td>

Date that the associated install base item was removed from the entitlement.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

entitlements.​product

</td><td>

Sys\_id of the product model record associated with the entitlement.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

entitlements.​product\_offering

</td><td>

Sys\_id of the product offering record associated with the entitlement.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

entitlements.​product\_specification

</td><td>

Sys\_id of the product specification record associated with the entitlement.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

entitlements.​sold\_entitlement

</td><td>

Sys\_id of the sold product record associated with the entitlement.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

entitlements.​sold\_products\_covered

</td><td>

List of sold products covered under the entitlement. Data type: Array of Objects

```
"sold_products_covered": [ 
  {
    "added": "String",
    "removed": "String",
    "sold_product": "String"
  }
]
```

</td></tr><tr><td>

entitlements.​sold\_products\_covered.​added

</td><td>

Date that the associated sold product was added to the entitlement.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

entitlements.​sold\_products\_covered.​removed

</td><td>

Date that the associated sold product was removed from the entitlement.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

entitlements.​sold\_products\_covered.​sold\_product

</td><td>

Sys\_id of a product associated with the entitlement.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

entitlements.​start\_date

</td><td>

Required. Start date of the entitlement.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

entitlements.​state

</td><td>

Required.Current state of the entitlement.

Valid values: \(case-sensitive\)

-   active
-   cancelled
-   draft
-   expired
-   suspended

Data type: String

</td></tr><tr><td>

entitlement\_characteristics

</td><td>

List of characteristics associated with the service contract line.Data type: Array of Objects

```
"entitlement_characteristics" [
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

Required. Sys\_id of the characteristic record associated with the service contract line.

Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

entitlement\_characteristics.​characteristic\_option

</td><td>

Required if the **input\_type** parameter contained in the record specified in the **entitlement\_characteristics.characteristic** parameter, is set to `choice`.Sys\_id of the characteristic option record associated with the service contract line.

Data type: String

Table: Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage

</td><td>

Used unit value for the associated service contract line characteristic.Data type: Object

```
"entitlement_usage": {
    "used_units": "String"
}
```

Stored in: Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

entitlement\_characteristics.​entitlement\_usage.​used\_units

</td><td>

Usage of the associated entitlement characteristic.Data type: String

</td></tr><tr><td>

entitlement\_characteristics.​type

</td><td>

Type of service contract line characteristic. Valid values:

-   coverage
-   coverage \_and\_usage

Data type: String

</td></tr><tr><td>

entitlement\_characteristics.​value

</td><td>

Required if the **entitlement\_characteristics.type** parameter is not passed. Value of the characteristic.

Data type: String

</td></tr><tr><td>

install\_base\_items\_covered

</td><td>

Required if the **sold\_products\_covered** parameter is not passed.List of install base items covered under the  service contract line.

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

Stored in: Sold Product Covered  \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

install\_base\_items\_covered.​added

</td><td>

Date that the associated install base item was added to the service contract line.

Data type: String

 Format: yyyy-mm-dd

 Default: Current date

</td></tr><tr><td>

install\_base\_items\_covered.​install\_base

</td><td>

Sys\_id of the install base item covered by the service contract line.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

install\_base\_items\_covered.​removed

</td><td>

Date that the associated service contract line ends coverage of the install base item.

Data type: String

 Format: yyyy-mm-dd

 Default: No end date

</td></tr><tr><td>

name

</td><td>

Required. Name of the service contract line.

Data type: String

</td></tr><tr><td>

parent\_contract\_line

</td><td>

Sys\_id of the service contract line to which the current service contract line is a child of.Null for the contract lines created under a contract.

Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr><tr><td>

product\_model

</td><td>

Sys\_id of the product associated with the service contract line.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

product\_offering 

</td><td>

Sys\_id of the product offering record associated with the service contract line.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

product\_specification

</td><td>

Sys\_id of the product specification record associated with the service contract line.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

sold\_product

</td><td>

Sys\_id of the sold product record associated with the service contract line.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

sold\_products\_covered

</td><td>

Required if the **install\_base\_items\_covered** parameter is not passed.List of products covered under the service contract line.

Data type: Array of Objects

```
"sold_products_covered": [ 
  {
    "added": "String",
    "removed": "String",
    "sold_product": "String"
  }
]
```

Data is stored in the Sold Products Covered  \[sn\_install\_base\_m2m\_contract\_sold\_product\] table.

</td></tr><tr><td>

sold\_products\_covered.​added

</td><td>

Date that the associated service contract line starts to cover the associated product.Data type: String

Format: yyyy-mm-dd

Default: Current date

</td></tr><tr><td>

sold\_products\_covered.​removed

</td><td>

Date that the associated service contract line ends coverage of the associated product.Data type: String

Format: yyyy-mm-dd

Default: No end date

</td></tr><tr><td>

sold\_products\_covered.​sold\_product

</td><td>

Sys\_id of a product associated with the service contract line.

Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

starts

</td><td>

Required. Start date of the service contract line.

Data type: String

Format: yyyy-mm-dd

</td></tr><tr><td>

state

</td><td>

Required.Current state of the contract line.

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

|Status code|Description|
|-----------|-----------|
|201|Successful. The request was successfully processed and the records were created.|
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have permission to access the API.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

child\_contract\_lines

</td><td>

List of child service contract line objects created under the service contract line.Data type: Array of Objects

```
"child_contract_lines": [
  {
    "child_contract_lines": [Array],
    "entitlements": [Array],
    "entitlement_characteristics": [Array],
    "install_base_items_covered": [Array],
    "name": "String",
    "number": "String",
    "sold_products_covered": [Array],
    "sys_id" "String"
  }
]
```

</td></tr><tr><td>

child\_contract\_lines.​child\_contract\_lines

</td><td>

List of child service contract line objects created under the child service contract line. The objects in this array have the same elements as the **child\_contract\_lines** parameter.Data type: Array of Objects

</td></tr><tr><td>

child\_contract\_lines.​entitlements

</td><td>

List of entitlements associated with the child service contract line.Data type: Array of Objects

```
"entitlements": [
  {
    "entitlement_name": "String",
    "entitlement_characteristics": [Array],
    "install_base_items_covered": [Array],
    "sold_products_covered": [Array],
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_name

</td><td>

Name of the entitlement.

Data type: String

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics

</td><td>

List of the entitlement characteristic objects  created under the entitlement. Data type: Array of Objects

```
"entitlement_characteristics": [
  {
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​entitlement\_characteristics.​sys\_id

</td><td>

Sys\_id of an entitlement characteristics record associated with the child service contract line.Data type: String

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​install\_base\_items\_covered

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

child\_contract\_lines.​entitlements.​install\_base\_items\_covered.​sys\_id

</td><td>

Sys\_id of a install base items covered by the entitlement.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sold\_products\_covered

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

child\_contract\_lines.​entitlements.​sold\_products\_covered.​sys\_id

</td><td>

Sys\_id of a product associated with the entitlement.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

child\_contract\_lines.​entitlements.​sys\_id

</td><td>

Sys\_id of the entitlement record associated with the child service contract line.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics

</td><td>

List of characteristics associated with the chile contract line. Data type: Array of Objects

```
"entitlement_characteristics": [
  {
    "entitlement_usage": {Object},
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage

</td><td>

Entitlement usage object inserted under the entitlement\_characteristic.Data type: Object

```
"entitlement_usage": {
    "sys_id": "String"
}
```

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​entitlement\_usage.​sys\_id

</td><td>

Sys\_id of the entitlement usage record.Data type: String

Table: Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

child\_contract\_lines.​entitlement\_characteristics.​sys\_id

</td><td>

Sys\_id of a entitlement characteristics record associated with the child service contract line.Data type: String

Table: Characteristic \[sn\_pss\_core\_entitlement\_characteristic\]

</td></tr><tr><td>

child\_contract\_lines.​install\_base\_items\_covered

</td><td>

List of sys\_ids of the install base items covered under the child service contract line. Data type: Array of Objects

```
"install_base_items_covered": [ 
  {
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

child\_contract\_lines.​install\_base\_items\_covered.​sys\_id

</td><td>

Sys\_id of the install base item covered.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

child\_contract\_lines.​name

</td><td>

Name of the child service contract line.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​number

</td><td>

Unique number of the service contract line. Automatically generated by the endpoint. For example: CTRL9812347.Data type: String

</td></tr><tr><td>

child\_contract\_lines.​sold\_products\_covered

</td><td>

List of sys\_ids of the products covered under the child service contract line. Data type: Array of Objects

```
"sold_products_covered": [ 
  {
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

child\_contract\_lines.​sold\_products\_covered.​sys\_id

</td><td>

Sys\_id of a product covered by the child service contract line.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

child\_contract\_lines.​sys\_id

</td><td>

Sys\_id of a product covered by the child contract item.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

entitlements

</td><td>

List of entitlements associated with the service contract line.Data type: Array of Objects

```
"entitlements": [
  {
    "entitlement_characteristics": [Array],
    "entitlement_name": "String",
    "install_base_items_covered": [Array],
    "sold_products_covered": [Array],
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

entitlements.​entitlement\_characteristics

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

entitlements.​entitlement\_characteristics.​entitlement\_usage

</td><td>

Entitlement usage object inserted under the entitlement\_characteristic.Data type: Object

```
"entitlement_usage": {
    "sys_id": "String"
}
```

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​entitlement\_usage.​sys\_id

</td><td>

Sys\_id of the entitlement usage record.Data type: String

Table: Entitlement Usage \[sn\_pss\_core\_entitlement\_usage\]

</td></tr><tr><td>

entitlements.​entitlement\_characteristics.​sys\_id

</td><td>

Sys\_id of the entitlement characteristics record.Data type: String

</td></tr><tr><td>

entitlements.​entitlement\_name

</td><td>

Name of the entitlement.

Data type: String

</td></tr><tr><td>

entitlements.​install\_base\_items\_covered

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

entitlements.​install\_base\_items\_covered.​sys\_id

</td><td>

Sys\_id of a install base items covered by the entitlement.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

entitlements.​sold\_products\_covered

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

entitlements.​sold\_products\_covered.​sys\_id

</td><td>

Sys\_id of a product associated with the entitlement.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

entitlements.​sys\_id

</td><td>

Sys\_id of the entitlement record associated with the service contract line.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

entitlement\_characteristics

</td><td>

List of the entitlement characteristic objects  created under the service contract line. Data type: Array of Objects

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

Sys\_id of the entitlement characteristics record.Data type: String

</td></tr><tr><td>

install\_base\_items\_covered

</td><td>

List of sys\_ids of the install base items covered under the service contract line. Data type: Array of Objects

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

Sys\_id of the install base item covered.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

name

</td><td>

Name of the service contract line.

Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number of the service contract line. Automatically generated by the endpoint. For example: CTRL9812347.Data type: String

</td></tr><tr><td>

sold\_products\_covered

</td><td>

List of sys\_ids of the products covered under the service contract line. Data type: Array of Objects

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

Sys\_id of a product covered by the service contract line.Data type: String

Table: Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of a service contract line record.Data type: String

Table: Service Contract Line \[sn\_pss\_core\_service\_contract\_line\]

</td></tr></tbody>
</table>### cURL request

The following is a code example that shows how to call this endpoint and create a service contract line record.

```
curl "https://instance.servicenow.com/api/sn_pss_core/servicecontract/contractline" \
--request POST \
--header "Accept:application/json" \
--data
{
  "state": "active",
  "contract": "a4b415d1d1f53110f8776589fa411f20",
  "parent_contract_line": null,
  "name": "CLI",
  "starts": "2022-12-03",
  "child_contract_lines": [
    {
      "state": "active",
      "name": "Child CLI",
      "starts": "2022-12-03",
      "entitlements": [
        {
          "state": "active",
          "entitlement_name": "Child CLI - ENTL",
          "start_date": "2022-12-03"
        }
      ],
      "sold_products_covered": [
        {
          "sold_product": "8db4258949f14ef7b90d90822dfc5800",
          "added": "2023-12-03",
          "removed": "2023-12-03"
        }
      ],
      "install_base_items_covered": [
        {
          "install_base": "2f270832699b46e78aa899a5a5dc6682",
          "added": "2023-12-03",
          "removed": "2023-12-03"
        }
      ],
      "entitlement_characteristics": [
        {
          "characteristic": "63418db7539e61106bfcddeeff7b1238",
          "characteristic_option": "495149b7539e61106bfcddeeff7b1262",
          "value": "20",
          "type": "coverage"
        }
      ]
    }
  ],
  "entitlements": [
    {
      "state": "active",
      "entitlement_name": "ENTL 1",
      "start_date": "2022-12-03",
      "sold_products_covered": [
        {
          "sold_product": "ec235d9dd1b53110f8776589fa411fe2"
        }
      ],
      "entitlement_characteristics": [
        {
          "characteristic": "63418db7539e61106bfcddeeff7b1238",
          "characteristic_option": "495149b7539e61106bfcddeeff7b1262",
          "value": "20",
          "type": "coverage_and_usage",
          "entitlement_usage": {
            "used_units": "3"
          }
        }
      ]
    }
  ],
  "sold_products_covered": [
    {
      "sold_product": "0df21151d1f53110f8776589fa411f1b",
      "added": "2023-12-03",
      "removed": "2023-12-03"
    }
  ],
  "entitlement_characteristics": [
    {
      "characteristic": "63418db7539e61106bfcddeeff7b1238",
      "characteristic_option": "495149b7539e61106bfcddeeff7b1262",
      "value": "tyfy6h",
      "type": "coverage"
    }
  ]
}
```

Response:

```
{
  "result": {
    "sys_id": "16e451d1d1f53110f8776589fa411f80",
    "name": "CLI",
    "number": "CTRL00000001",
    "child_contract_lines": [
      {
        "sys_id": "3a39ecdc01154f4ab782da0169c9c922",
        "name": "Child CLI",
        "number": "CTRL00000001",
        "child_contract_lines": [],
        "entitlements": [
          {
            "sys_id": "7439fd84c2494ba6951e58f333cfe8d4",
            "entitlement_name": "Child CLI - ENTL",
            "sold_products_covered": [],
            "install_base_items_covered": [],
            "entitlement_characteristics": []
          }
        ],
        "sold_products_covered": [
          {
            "sys_id": "dfb62e9c4c6843009be02a68f65b9118"
          }
        ],
        "install_base_items_covered": [
          {
            "sys_id": "2583912e81964501b52a2e44d4797a28"
          }
        ],
        "entitlement_characteristics": [
          {
            "sys_id": "3a00c975bb49412cae169200c7f6236e",
            "entitlement_usage": {}
          }
        ]
      }
    ],
    "entitlements": [
      {
        "sys_id": "9ee451d1d1f53110f8776589fa411f83",
        "entitlement_name": "ENTL 1",
        "sold_products_covered": [
          {
            "sys_id": "92e451d1d1f53110f8776589fa411f85"
          }
        ],
        "install_base_items_covered": [],
        "entitlement_characteristics": [
          {
            "sys_id": "92e451d1d1f53110f8776589fa411f86",
            "entitlement_usage": {
              "sys_id": "dee451d1d1f53110f8776589fa411f86"
            }
          }
        ]
      }
    ],
    "sold_products_covered": [
      {
        "sys_id": "5ae451d1d1f53110f8776589fa411f81"
      }
    ],
    "install_base_items_covered": [],
    "entitlement_characteristics": [
      {
        "sys_id": "dae451d1d1f53110f8776589fa411f82",
        "entitlement_usage": {}
      }
    ]
  }
}
```

