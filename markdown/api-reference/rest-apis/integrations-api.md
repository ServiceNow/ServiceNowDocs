---
title: Install Base Item API
description: The Install Base Item API provides endpoints to access and manage install base items records within a ServiceNow instance.Disassociates a specified related parties record from a specified install base item record.Returns all install base items. You can pass parameters within the call to filter the return results.Returns a specified install base item record and its child hierarchy.Returns the cases associated with a specified install base item record.Returns the child install base items associated with a specified install base item record.Returns the contracts associated with a specified install base item record.Returns the entitlements associated with a specified install base item record.Returns the maintenance plans associated with a specified install base item record.Returns the related parties associated with a specified install base item record.Returns the sold products records associated with a specified install base item record.Returns the work orders associated with a specified install base item record.Updates a specified install base item record with specified field values.Updates the specified related party record, associated with a specified install base item, with the values in the request body.Uninstalls the specified install base item.Creates one or more install base item records in the default Install Base Item table, or in its extended table if specified, and populates them with the specified field values.Creates a related party record and associates it with a specified install base item record. The values specified in the request parameters are stored in the newly created related party record.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 150
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Install Base Item API

The Install Base Item API provides endpoints to access and manage install base items records within a ServiceNow instance.

An install base item represents an instance of a product that has been configured for a customer. Install base items enable you to track all purchases made by a customer.

You can also perform CRUD operations on the Install Base Related Parties related list using this API. In addition, you can read records in other install base items related lists, such as cases, contracts, entitlements, maintenance plans, sold products, and work orders.

To access this API you must have either the sn\_install\_base.ib\_api\_write or sn\_install\_base.ib\_api\_read role depending on the type of CRUD action that you are trying to perform.

To access the various endpoints in this API the following plugins must be installed:

-   Customer Service Install Base Management \(com.snc.install\_base\)
-   Planned Work Management \(sn\_fsm\_planned\_wm\) if you want to retrieve maintenance plan and work order data.

This API runs in the `sn_install_base` namespace.

**Note:** This API only returns non-empty fields in the endpoint responses. Also, none of the system level fields \(those prefaced with "sys\_"\) are returned except the sys\_id field.

For additional information on install base items, see [Create an Install base item](https://www.servicenow.com/docs/access?context=create-install-base-item&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Install Base Item - DELETE /sn\_install\_base/integrations/installbaseitems/\{id\}/relatedparties/\{related\_party\_sys\_id\}

Disassociates a specified related parties record from a specified install base item record.

### URL format

Versioned URL: `/api/sn_install_base/{api_version}/integrations/installbaseitems/{id}/relatedparties/{related_party_sys_id}`

Default URL: `/api/sn_install_base/integrations/installbaseitems/{id}/relatedparties/{related_party_sys_id}`

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

</td><td id="integrate-id-entry">

Sys\_id of the install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

related\_party\_sys\_id

</td><td id="related_party_sys_id-integrate-entry">

Sys\_id of the related party record.Data type: String

Table: Install Base Related Party \[sn\_install\_base\_related\_party\]

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
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="id_zk1_w5w_ywb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="error-integration-row"><td>

error

</td><td id="error-integration-entry">

Details about the error that occurred when trying to process the request.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr id="error_detail-integration-row"><td>

error.detail

</td><td id="error_detail-integration-entry">

Additional details about the associated error.Data type: String

</td></tr><tr id="error_message-integration-row"><td>

error.message

</td><td id="error_message-integration-entry">

Error message that describes the problem that occurred when trying to execute the request.Data type: String

</td></tr><tr id="result-integration-row"><td>

result

</td><td id="result-integration-entry">

Description of the endpoint results.Data type: Object

</td></tr><tr><td>

result.status

</td><td>

Status of the endpoint request. Possible values:

-   SUCCESS
-   FAILURE

Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/installbaseitems/f77c7542b7343300ece839a6ee11a991/relatedparties/2a42dfae872521100b6afc86dabb356b" \
--request DELETE \
--header "Accept:application/json" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "status": "SUCCESS"
  }
}
```

## Install Base Item - GET /sn\_install\_base/integrations/installbaseitems

Returns all install base items. You can pass parameters within the call to filter the return results.

### URL format

Versioned URL: `/api/sn_install_base/{api_version}/integrations/installbaseitems`

Default URL: `/api/sn_install_base/integrations/installbaseitems`

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
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

field name-value pairs

</td><td>

Field-value pairs to use to filter the install base item records. If you specify a different table in **sys\_class\_name**, then specify the fields in that table.You can pass one or more field-value pairs to filter the return results.

For example, to return only records where the state field is set to "in\_use" and the status field is set to "replacement", pass the follow: `&state=in_use&status=replacement`.

Data type: String

Default: All fields

Table: Install Base Item \[sn\_istall\_base\_item\]

</td></tr><tr><td>

related\_party

</td><td>

Sys\_id of a related party record.Filters the install base item records based on the specified related party. A related party can be linked to an install base item or a sold product.

Valid values:

-   account sys\_id: Located in the Account \[customer\_account\] table.
-   consumer sys\_id: Located in the Consumer \[csm\_consumer\] table.
-   contact sys\_id: Located in the Contact \[customer-contact\] table.
-   service organization sys\_id: Located in the Service Organization \[sn\_customer\_service\_organization\] table.
-   user sys\_id: Located in the User \[sys-user\] table.

Data type: String

Table: Install Base Related Party \[sn\_install\_base\_related\_party\]

</td></tr><tr><td>

responsibility

</td><td>

Sys\_id of the associated responsibility record. This record defines the access level for the install base information.This parameter is only valid if the **related\_party** field is also specified. If specified, it only returns the install base items that match both the **related\_party** and **responsibility** parameters.

For additional information, see [Configure related parties for Items Received](https://www.servicenow.com/docs/access?context=psds-add-related-parties-to-record&version=zurich&pubname=zurich-government-industry&ft:locale=en-US).

Data type: String

</td></tr><tr><td>

sys\_class\_name

</td><td>

If the desired records are in a table that extends the Install Base Items \[sn\_install\_base\_item\] table, the name of the extended table to query.Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td id="sysparm_limit-entry-RESTAPI">

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. This limit is applied before ACL evaluation. If no records return, including records you have access to, rearrange the record order so records you have access to return first.

**Note:** Unusually large **sysparm\_limit** values can impact system performance.

Data type: Number

Default: 10000

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-entry-RESTAPI">

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

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
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

The following return results only describe the return values for records returned from the Install Base Items \[sn\_install\_base\_items\] table.

<table id="id_qgj_jg2_zwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Details about the error that occurred when trying to process the request.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional details about the associated error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that describes the problem that occurred when trying to execute the request.Data type: String

</td></tr><tr id="has_more-integration-row"><td>

has\_more

</td><td id="has_more-integration-entry">

Flag that indicates whether there are more records in the table to return.Possible values:

-   true: More records to return.
-   false: No more records to return.

Data type: Boolean string

</td></tr><tr><td>

items

</td><td>

List of the install base items that matched the specified filter results.Data type: Array of Objects

```
"items":[
  {
    "account": {Object},
    "active": "String",
    "asset": {Object},
    "configuration_item": {Object},
    "consumer": {Object},
    "consumer_profile": {Object},
    "contact": {Object},
    "health_status": {Object},
    "health_status_last_updated": "String",
    "household": {Object},
    "install_date": {Object},
    "location": {Object},
    "name": "String",
    "number": "String",
    "parent": {Object},
    "product": {Object},
    "service_context": {Object},
    "service_organization" {Object},
    "sys_class_name": "String",
    "sys_id": "String",
    "sys_mod_count": "String",
    "state": {Object},
    "status": {Object},
    "uninstall_date": "String"
  }
]
```

</td></tr><tr id="account-integration-row"><td>

items.account

</td><td id="account-integration-entry">

Details about the customer account associated with the install base item record.Data type: Object

```
"account": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="account_display_value-integration-row"><td>

items.account.display\_value

</td><td id="account_display_value-integration-entry">

Text name of the customer account associated with the install base item record. Use this value to display the customer account name in the UI.Data type: String

</td></tr><tr id="account_sys_id-integration-row"><td>

items.account.sys\_id

</td><td id="account_sys_id-integration-entry">

Sys\_id of the customer account record associated with the install base item record.Data type: String

</td></tr><tr id="active-integration-row"><td>

items.active

</td><td id="active-integration-entry">

Flag that indicates whether the install base item is active.Possible values:

-   true: Install base item is active.
-   false: Install base item is inactive.

Data type: Boolean String

</td></tr><tr id="asset-integration-row"><td>

items.asset

</td><td id="asset-integration-entry">

Details about the asset associated with the install base item record.Data type: Object

```
"asset": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="asset_display_value-integration-row"><td>

items.asset.display\_value

</td><td id="asset_display_value-integration-entry">

Text name of the asset associated with the install base item record. Use this value to display the asset name in the UI.Data type: String

</td></tr><tr id="asset_sys_id-integration-row"><td>

items.asset.sys\_id

</td><td id="asset_sys_id-integration-entry">

Sys\_id of the asset record associated with the install base item record.Data type: String

</td></tr><tr id="configuration_item-integration-row"><td>

items.configuration\_item

</td><td id="configuration_item-integration-entry">

Details about the configuration item associated with the install base item record.Data type: Object

```
"configuration_item": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="configuration_item_display_value-integration-row"><td>

items.configuration\_item.display\_value

</td><td id="configuration_item_display_value-integration-entry">

Text name of the configuration item associated with the install base item record. Use this value to display the configuration item name in the UI.Data type: String

</td></tr><tr id="configuration_item_sys_id-integration-row"><td>

items.configuration\_item.sys\_id

</td><td id="configuration_item_sys_id-integration-entry">

Sys\_id of the configuration item record associated with the install base item record.Data type: String

</td></tr><tr id="consumer-integration-row"><td>

items.consumer

</td><td id="consumer-integration-entry">

Details about the consumer associated with the install base item record.**Note:** The consumer field is only available if the B2B2C plugin is installed.

Data type: Object

```
"consumer": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="consumer_display_value-integration-row"><td>

items.consumer.display\_value

</td><td id="consumer_display_value-integration-entry">

Text name of the consumer associated with the install base item record. Use this value to display the consumer name in the UI.Data type: String

</td></tr><tr id="consumer_sys_id-integration-row"><td>

items.consumer.sys\_id

</td><td id="consumer_sys_id-integration-entry">

Sys\_id of the consumer record associated with the install base item record.Data type: String

</td></tr><tr id="consumer_profile-integration-row"><td>

items.consumer\_profile

</td><td id="consumer_profile-integration-entry">

Details about the consumer profile associated with the install base item record.**Note:** The consumer profile field is only available if the B2B2C plugin is installed.

Data type: Object

```
"consumer_profile": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="consumer_profile_display_value-integration-row"><td>

items.consumer\_profile.display\_value

</td><td id="consumer_profile_display_value-integration-entry">

Text name of the consumer profile associated with the install base item record. Use this value to display the consumer profile name in the UI.Data type: String

</td></tr><tr id="consumer_profile_sys_id-integration-row"><td>

items.consumer\_profile.sys\_id

</td><td id="consumer_profile_sys_id-integration-entry">

Sys\_id of the consumer profile record associated with the install base item record.Data type: String

</td></tr><tr id="contact-integration-row"><td>

items.contact

</td><td id="contact-integration-entry">

Details about the account contact responsible for the install base item record.Data type: Object

```
"contact": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="contact_display_value-integration-row"><td>

items.contact.display\_value

</td><td id="contact_display_value-integration-entry">

Text name of the account contact associated with the install base item record. Use this value to display the account contact name in the UI.Data type: String

</td></tr><tr id="contact_sys_id-integration-row"><td>

items.contact.sys\_id

</td><td id="contact_sys_id-integration-entry">

Sys\_id of the account contact record associated with the install base item record.Data type: String

</td></tr><tr id="health_status-integration-row"><td>

items.health\_status

</td><td id="health_status-integration-entry">

Details about the current health status of the install base item. Only returned if the Proactive Customer Service Operations \(com.snc.proactive\_cs\_itom\) plugin is installed.Data type: Object

```
"health_status": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="health_status_display_value-integration-row"><td>

items.health\_status.display\_value

</td><td id="health_status_display_value-integration-entry">

Text string of the current health status of the install base item. Use this value to display the health status in the UI.Data type: String

</td></tr><tr id="health_status_value-integration-row"><td>

items.health\_status.value

</td><td id="health_status_value-integration-entry">

Internal value of the health status of the install base item.Data type: String

</td></tr><tr id="health_status_last_updated-integration-row"><td>

items.health\_status\_last\_updated

</td><td id="health_status_last_updated-integration-entry">

Date and time when the health status was last updated for the install base item.Data type: String

</td></tr><tr id="household-integration-row"><td>

items.household

</td><td id="household-integration-entry">

Details about the household associated with the install base item record. Only returned if the Customer Service Household \(com.snc.household\) plugin is installed.Data type: Object

```
"household": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="household_display_value-integration-row"><td>

items.household.display\_value

</td><td id="household_display_value-integration-entry">

Text name of the household associated with the install base item record. Use this value to display the household name in the UI.Data type: String

</td></tr><tr id="household_sys_id-integration-row"><td>

items.household.sys\_id

</td><td id="household_sys_id-integration-entry">

Sys\_id of the household associated with the install base item record.Data type: String

</td></tr><tr id="install_date-integration-row"><td>

items.install\_date

</td><td id="install_date-integration-entry">

Details about the date when the install base item became active.Data type: Object

```
"install_date": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="install_date_isplay_value-integration-row"><td>

items.install\_date.display\_value

</td><td id="install_date_display_value-integration-entry">

Text install date. Use this value to display the install date in the UI.Data type: String

</td></tr><tr id="install_date_value-integration-row"><td>

items.install\_date.value

</td><td id="install_date_value-integration-entry">

Internal value of the install date.Data type: String

</td></tr><tr id="location-integration-row"><td>

items.location

</td><td id="location-integration-entry">

Details about the location of the install base item.Data type: Object

```
"location": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="location_display_value-integration-row"><td>

items.location.display\_value

</td><td id="location_display_value-integration-entry">

Text name of the install base item location. Use this value to display the location name in the UI.Data type: String

</td></tr><tr id="location_sys_id-integration-row"><td>

items.location.sys\_id

</td><td id="location_sys_id-integration-entry">

Sys\_id of the location record associated with the install base item record.Data type: String

</td></tr><tr id="name-integration-row"><td>

items.name

</td><td id="name-integration-entry">

Name of the install base item.Data type: String

</td></tr><tr id="number-integration-row"><td>

items.number

</td><td id="number-integration-entry">

Unique ID of the install base item.Data type: String

</td></tr><tr id="parent-integration-row"><td>

items.parent

</td><td id="parent-integration-entry">

Details about the parent record of the install base item record.Data type: Object

```
"parent": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="parent_display_value-integration-row"><td>

items.parent.display\_value

</td><td id="parent_display_value-integration-entry">

Text name of the parent record associated with the install base item record. Use this value to display the parent name in the UI.Data type: String

</td></tr><tr id="parent_sys_id-integration-row"><td>

items.parent.sys\_id

</td><td id="parent_sys_id-integration-entry">

Sys\_id of the parent record associated with the install base item record.Data type: String

</td></tr><tr id="product-integration-row"><td>

items.product

</td><td id="product-integration-entry">

Details about the product model associated with the install base item record. Use this information to identify the services associated with any product model.Data type: Object

```
"product": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="product_display_value-integration-row"><td>

items.product.display\_value

</td><td id="product_display_value-integration-entry">

Text name of the product model associated with the install base item record. Use this value to display the product name in the UI.Data type: String

</td></tr><tr id="product_sys_id-integration-row"><td>

items.product.sys\_id

</td><td id="product_sys_id-integration-entry">

Sys\_id of the product model record associated with the install base item record.Data type: String

</td></tr><tr id="service_context-integration-row"><td>

items.service\_context

</td><td id="service_context-integration-entry">

Details about the service context associated with the install base item record.Data type: Object

```
"service_context": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="service_context_display_value-integration-row"><td>

items.service\_context.display\_value

</td><td id="service_context_display_value-integration-entry">

Text name of the service context associated with the install base item record. Use this value to display the service context name in the UI.Data type: String

</td></tr><tr id="service_context_sys_id-integration-row"><td>

items.service\_context.sys\_id

</td><td id="service_context_sys_id-integration-entry">

Sys\_id of the service context record associated with the install base item record.Data type: String

</td></tr><tr id="service_organization-integration-row"><td>

items.service\_organization

</td><td id="service_organization-integration-entry">

Details about the service organization associated with the install base item record. Only returned if the Service Organization \(com.snc.service\_organization\) plugin is installed.Data type: Object

```
"service_organization": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="service_organization_display_value-integration-row"><td>

items.service\_organization.display\_value

</td><td id="service_organization_display_value-integration-entry">

Text name of the service organization associated with the install base item record. Use this value to display the service organization name in the UI.Data type: String

</td></tr><tr id="service_organization_sys_id-integration-row"><td>

items.service\_organization.sys\_id

</td><td id="service_organization_sys_id-integration-entry">

Sys\_id of the service organization record associated with the install base item record.Data type: String

</td></tr><tr id="sys_class_name-integration-row"><td>

items.sys\_class\_name

</td><td id="sys_class_name-integration-entry">

Table containing the install base item record.Data type: String

</td></tr><tr id="sys_id-integration-row"><td>

items.sys\_id

</td><td id="sys_id-integration-entry">

Sys\_id of the install base item record. Located in the table specified in the **sys\_class\_name** parameter.Data type: String

</td></tr><tr id="sys_mod_count-integration-row"><td>

items.sys\_mod\_count

</td><td id="sys_mod_count-integration-entry">

Number of times that the associated install base item record has been modified.Data type: String

</td></tr><tr id="state-integration-row"><td>

items.state

</td><td id="state-integration-entry">

Details about the current state of the install base item.Data type: Object

```
"state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="state_display_value-integration-row"><td>

items.state.display\_value

</td><td id="state_display_value-integration-entry">

Text string of the current state of the install base item. Use this value to display the state in the UI.Data type: String

</td></tr><tr id="state_value-integration-row"><td>

items.state.value

</td><td id="state_value-integration-entry">

Internal value of the state of the install base item.Data type: String

</td></tr><tr id="status1-integration-row"><td>

items.status

</td><td id="status1-integration-entry">

Details about the status of the install base item.Data type: Object

```
"status": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="status1_display_value-integration-row"><td>

items.status.display\_value

</td><td id="status1_display_value-integration-entry">

Text string of the status of the install base item. Use this value to display the status in the UI.Data type: String

</td></tr><tr id="status1_value-integration-row"><td>

items.status.value

</td><td id="status1_value-integration-entry">

Internal value of the status of the install base item.Data type: String

</td></tr><tr id="uninstall_date-integration-row"><td>

items.uninstall\_date

</td><td id="uninstall_date-integration-entry">

Details about the date when the install base item became inactive.Data type: Object

```
"uninstall_date": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="uninstall_date_display_value-integration-row"><td>

items.uninstall\_date.display\_value

</td><td id="uninstall_date_display_value-integration-entry">

Text uninstall date. Use this value to display the uninstall date in the UI.Data type: String

</td></tr><tr id="uninstall_date_value-integration-row"><td>

items.uninstall\_date.value

</td><td id="uninstall_date_value-integration-entry">

Internal value of the uninstall date.Data type: String

</td></tr><tr id="status-integration-row"><td>

status

</td><td id="status-integration-entry">

Status of the endpoint call.Data type: String

</td></tr><tr id="sysparm_depth-integration-row"><td>

sysparm\_depth

</td><td id="sysparm_depth-integration-entry">

Number of levels deep the returned child install base item is in the hierarchy.Data type: Integer

</td></tr><tr id="sysparm_limit-integration-row"><td>

sysparm\_limit

</td><td id="sysparm_limit-integration-entry">

Number of records that were returned. If this value isn't specified in the original request, it uses the default value.Data type: Number

</td></tr><tr id="sysparm_offset-integration-row"><td>

sysparm\_offset

</td><td id="sysparm_offset-integration-entry">

Offset \(starting point\) in the associated table from which records were evaluated and retrieved.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows a simple call that only returns a single record starting at offset 5.

```
curl "https://instance.servicenow.com/api/sn_install_base/v1/integrations/installbaseitems?sysparm_limit=1&sysparm_offset=5" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "sysparm_offset": "5",
    "sysparm_limit": 1,
    "has_more": true,
    "items": [
      {
        "sys_class_name": "sn_install_base_item",
        "number": "IBITM001100",
        "sys_id": "181df7ff530a1110539dddeeff7b12f4",
        "state": {
          "value": "in_use",
          "display_value": "In Use"
        },
        "sys_mod_count": "2",
        "active": "true",
        "configuration_item": {
          "sys_id": "62446ae8535e5510539dddeeff7b12db",
          "display_value": "boxeoproderp"
        },
        "name": "boxeoproderp",
        "account": {
          "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
          "display_value": "Boxeo"
        }
      }
    ],
    "status": "SUCCESS"
  }
}
```

### cURL request

The following code example shows how to search for the fields **state** = "in\_use" and **status** = "replacement" within the Install Base Item table.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/installbaseitems?state=in_use&status=replacement" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "sysparm_offset": "0",
    "sysparm_limit": "10",
    "has_more": false,
    "items": [
      {
        "parent": {
          "sys_id": "ffd023f453de9910539dddeeff7b1264",
          "display_value": "Point of Sale System"
        },
        "sys_class_name": "sn_install_base_item",
        "number": "IBITM001140",
        "sys_id": "a1a123745312d910539dddeeff7b127b",
        "state": {
          "value": "in_use",
          "display_value": "In Use"
        },
        "install_date": {
          "value": "2018-12-14 07:00:00",
          "display_value": "2018-12-13 23:00:00"
        },
        "product": {
          "sys_id": "2dd1e7b753421110539dddeeff7b12d1",
          "display_value": "Stand"
        },
        "active": "true",
        "name": "Stand",
        "service_organization": {
          "sys_id": "42b51f5ab3401010700b4d43c6a8dc5a",
          "display_value": "LA City Center - West"
        },
        "status": {
          "value": "replacement",
          "display_value": "Replacement"
        }
      },
      {
        "parent": {
          "sys_id": "ffd023f453de9910539dddeeff7b1264",
          "display_value": "Point of Sale System"
        },
        "sys_class_name": "sn_install_base_item",
        "number": "IBITM001139",
        "sys_id": "d0916bb05312d910539dddeeff7b1232",
        "state": {
          "value": "in_use",
          "display_value": "In Use"
        },
        "install_date": {
          "value": "2018-12-14 07:00:00",
          "display_value": "2018-12-13 23:00:00"
        },
        "product": {
          "sys_id": "dfc127b753421110539dddeeff7b12ac",
          "display_value": "Register"
        },
        "active": "true",
        "name": "Register",
        "service_organization": {
          "sys_id": "42b51f5ab3401010700b4d43c6a8dc5a",
          "display_value": "LA City Center - West"
        },
        "status": {
          "value": "replacement",
          "display_value": "Replacement"
        }
      },
      {
        "parent": {
          "sys_id": "ffd023f453de9910539dddeeff7b1264",
          "display_value": "Point of Sale System"
        },
        "sys_class_name": "sn_install_base_item",
        "number": "IBITM001141",
        "sys_id": "ffb123745312d910539dddeeff7b12cb",
        "state": {
          "value": "in_use",
          "display_value": "In Use"
        },
        "install_date": {
          "value": "2018-12-14 07:00:00",
          "display_value": "2018-12-13 23:00:00"
        },
        "product": {
          "sys_id": "59e1e7b753421110539dddeeff7b12cc",
          "display_value": "Terminal"
        },
        "active": "true",
        "name": "Terminal",
        "service_organization": {
          "sys_id": "42b51f5ab3401010700b4d43c6a8dc5a",
          "display_value": "LA City Center - West"
        },
        "status": {
          "value": "replacement",
          "display_value": "Replacement"
        }
      }
    ],
    "status": "SUCCESS"
  }
}

```

### cURL request

The following code example shows how to filter the return results using the **related\_party** and **responsibility** query parameters.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/installbaseitems?related_party=dc0185d94f341200025ba3618110c77c&responsibility=c009bbedb3730010700b4d43c6a8dce" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "sysparm_offset": "0",
    "sysparm_limit": "10",
    "has_more": false,
    "items": [
      {
        "sys_class_name": "sn_install_base_item",
        "number": "IBITM0001004",
        "sys_id": "3ea014a778de1110f877d304c76fdd0d",
        "state": {
          "value": "in_use",
          "display_value": "In Use"
        },
        "consumer": {
          "sys_id": "feb5139ab3401010700b4d43c6a8dc43",
          "display_value": "Kenny Smith"
        },
        "product": {
          "sys_id": "63c8bc9778921110f877d304c76fdd34",
          "display_value": "X4 Sport Utility 4D"
        },
        "active": "true",
        "name": "X4 Sport Utility 4D",
        "status": {
          "value": "original",
          "display_value": "Original"
        }
      },
      {
        "sys_class_name": "sn_install_base_item",
        "number": "IBITM001003",
        "sys_id": "6e94e3c853500010df5dddeeff7b1234",
        "contact": {
          "sys_id": "4d147a386f0331003b3c498f5d3ee437",
          "display_value": "Julie Lewis"
        },
        "active": "true",
        "configuration_item": {
          "sys_id": "a96a570453500010df5dddeeff7b1206",
          "display_value": "boxeosandbox"
        },
        "name": "Boxeo - Sandbox",
        "account": {
          "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
          "display_value": "Boxeo"
        }
      },
      {
        "sys_class_name": "sn_install_base_item",
        "number": "IBITM0001010",
        "sys_id": "83332fde87e5a1105d0055373cbb3567",
        "contact": {
          "sys_id": "ddce70866f9331003b3c498f5d3ee417",
          "display_value": "George Warren"
        },
        "state": {
          "value": "in_use",
          "display_value": "In Use"
        },
        "install_date": {
          "value": "2023-02-26 18:59:52",
          "display_value": "2023-02-26 10:59:52"
        },
        "health_status": {
          "value": "not_available",
          "display_value": "Not Available"
        },
        "product": {
          "sys_id": "a9a2d0c3c6112276010db16c5ddd3461",
          "display_value": "Lenovo ThinkStation S20"
        },
        "active": "true",
        "configuration_item": {
          "sys_id": "affd3c8437201000deeabfc8bcbe5dc3",
          "display_value": "*BETH-IBM"
        },
        "name": "IB B2B",
        "location": {
          "sys_id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
          "display_value": "100 South Charles Street, Baltimore,MD"
        },
        "asset": {
          "sys_id": "bfc1fa8837f3100044e0bfc8bcbe5ddf",
          "display_value": "P1000228 - Lenovo ThinkStation S20"
        },
        "account": {
          "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
          "display_value": "Boxeo"
        },
        "status": {
          "value": "original",
          "display_value": "Original"
        }
      },
      {
        "sys_class_name": "sn_install_base_item",
        "number": "IBITM0001011",
        "sys_id": "9d766f168729a1105d0055373cbb3597",
        "health_status": {
          "value": "not_available",
          "display_value": "Not Available"
        },
        "product": {
          "sys_id": "8583ce8237732000158bbfc8bcbe5dd9",
          "display_value": "Fujitsu 1TB Hybrid Solid State Drive"
        },
        "active": "true",
        "name": "IBA",
        "account": {
          "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
          "display_value": "Boxeo"
        }
      },
      {
        "sys_class_name": "sn_install_base_item",
        "number": "IBITM0001013",
        "sys_id": "bd955a2687ada1100b6afc86dabb35fb",
        "health_status": {
          "value": "not_available",
          "display_value": "Not Available"
        },
        "consumer": {
          "sys_id": "59e788fbdb1b1200b6075200cf9619d2",
          "display_value": "Gilly Parker"
        },
        "product": {
          "sys_id": "1a13974053500010df5dddeeff7b122c",
          "display_value": "12000XHD Digital Press"
        },
        "active": "true",
        "name": "IBConsumer"
      },
      {
        "sys_class_name": "sn_install_base_item",
        "number": "IBITM0000901",
        "sys_id": "f77c7542b7343300ece839a6ee11a991",
        "product": {
          "sys_id": "8583ce8237732000158bbfc8bcbe5dd9",
          "display_value": "Fujitsu 1TB Hybrid Solid State Drive"
        },
        "active": "true",
        "name": "KX Series - KX5001",
        "account": {
          "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
          "display_value": "Boxeo"
        }
      }
    ],
    "status": "SUCCESS"
  }
}

```

## Install Base Item - GET /sn\_install\_base/integrations/installbaseitem/\{id\}

Returns a specified install base item record and its child hierarchy.

### URL format

Versioned URL: `/api/sn_install_base/{api_version}/integrations/installbaseitem/{id}`

Default URL: `/api/sn_install_base/integrations/installbaseitem/{id}`

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

</td><td id="integrate-id-entry">

Sys\_id of the install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_class\_name

</td><td>

If the intended record is in a table that extends the Install Base Items \[sn\_install\_base\_item\] table, the name of the extended table to query. This table must extend the sn\_install\_base\_item table.Data type: String

</td></tr><tr><td>

sysparm\_depth

</td><td>

Maximum depth of the child install base item's hierarchy to return.Data type: Integer

Default: 7

Maximum: 10

</td></tr><tr><td>

sysparm\_limit

</td><td>

Maximum number records to return in each child hierarchy.Data type: Integer

Default: 10

Maximum: 100

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

### Response body parameters \(JSON or XML\)

<table id="id_fw5_m3f_xwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

childinstallbase

</td><td>

List of child install base item records associated with the specified install base item.Data type: Object

```
"childinstallbase": {
  "items": [Array],
  "sysparm_depth": Integer
}
```

</td></tr><tr><td>

childinstallbase.items

</td><td>

Child install base items associated with the specified install base item. The values within this array are defined under the **items\[\]** array further down in this section.

</td></tr><tr><td>

childinstallbase.sysparm\_depth

</td><td>

Child-level of the install base item.Data type: Integer

</td></tr><tr><td>

error

</td><td id="error-integration-entry">

Details about the error that occurred when trying to process the request.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td id="error_detail-integration-entry">

Additional details about the associated error.Data type: String

</td></tr><tr><td>

error.message

</td><td id="error_message-integration-entry">

Error message that describes the problem that occurred when trying to execute the request.Data type: String

</td></tr><tr><td>

has\_children

</td><td>

Flag that indicates whether the requested install base item record has child install base item records.-   true: Has child install base item records.
-   false: Doesn't have child install base item records.

Data type: Boolean

</td></tr><tr><td>

item

</td><td>

Install base item that matched the specified filter results.Data type: Object

```
"item": {
  "account": {Object},
  "active": "String",
  "asset": {Object},
  "configuration_item": {Object},
  "consumer": {Object},
  "consumer_profile": {Object},
  "contact": {Object},
  "health_status": "Object",
  "health_status_last_updated": "String",
  "household": {Object},
  "install_date": {Object},
  "location": {Object},
  "name": "String",
  "number": "String",
  "parent": {Object},
  "product": {Object},
  "service_context": {Object},
  "service_organization" {Object},
  "sys_class_name": "String",
  "sys_id": "String",
  "state": {Object},
  "status": {Object},
  "uninstall_date": "String"
}
```

</td></tr><tr id="account-integration-row"><td>

item.account

</td><td>

Details about the customer account associated with the install base item record.Data type: Object

```
"account": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="account_display_value-integration-row"><td>

item.account.display\_value

</td><td>

Text name of the customer account associated with the install base item record. Use this value to display the customer account name in the UI.Data type: String

</td></tr><tr id="account_sys_id-integration-row"><td>

item.account.sys\_id

</td><td>

Sys\_id of the customer account record associated with the install base item record.Data type: String

</td></tr><tr id="active-integration-row"><td>

item.active

</td><td>

Flag that indicates whether the install base item is active.Possible values:

-   true: Install base item is active.
-   false: Install base item is inactive.

Data type: Boolean String

</td></tr><tr><td>

item.asset

</td><td>

Details about the asset associated with the install base item record.Data type: Object

```
"asset": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.asset.display\_value

</td><td>

Text name of the asset associated with the install base item record. Use this value to display the asset name in the UI.Data type: String

</td></tr><tr><td>

item.asset.sys\_id

</td><td>

Sys\_id of the asset record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.configuration\_item

</td><td>

Details about the configuration item associated with the install base item record.Data type: Object

```
"configuration_item": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.configuration\_item.display\_value

</td><td>

Text name of the configuration item associated with the install base item record. Use this value to display the configuration item name in the UI.Data type: String

</td></tr><tr><td>

item.configuration\_item.sys\_id

</td><td>

Sys\_id of the configuration item record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.consumer

</td><td>

Details about the consumer associated with the install base item record.**Note:** The consumer field is only available if the B2B2C plugin is installed.

Data type: Object

```
"consumer": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.consumer.display\_value

</td><td>

Text name of the consumer associated with the install base item record. Use this value to display the consumer name in the UI.Data type: String

</td></tr><tr><td>

item.consumer.sys\_id

</td><td>

Sys\_id of the consumer record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.consumer\_profile

</td><td>

Details about the consumer profile associated with the install base item record.**Note:** The consumer profile field is only available if the B2B2C plugin is installed.

Data type: Object

```
"consumer_profile": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.consumer\_profile.display\_value

</td><td>

Text name of the consumer profile associated with the install base item record. Use this value to display the consumer profile name in the UI.Data type: String

</td></tr><tr><td>

item.consumer\_profile.sys\_id

</td><td>

Sys\_id of the consumer profile record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.contact

</td><td>

Details about the account contact responsible for the install base item record.Data type: Object

```
"contact": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.contact.display\_value

</td><td>

Text name of the account contact associated with the install base item record. Use this value to display the account contact name in the UI.Data type: String

</td></tr><tr><td>

item.contact.sys\_id

</td><td>

Sys\_id of the account contact record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.health\_status

</td><td>

Details about the current health status of the install base item. Only returned if the Proactive Customer Service Operations \(com.snc.proactive\_cs\_itom\) plugin is installed.Data type: Object

```
"health_status": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

item.health\_status.display\_value

</td><td>

Text string of the current health status of the install base item. Use this value to display the health status in the UI.Data type: String

</td></tr><tr><td>

item.health\_status.value

</td><td>

Internal value of the health status of the install base item.Data type: String

</td></tr><tr><td>

item.health\_status\_last\_updated

</td><td>

Date and time when the health status was last updated for the install base item.Data type: String

</td></tr><tr><td>

item.household

</td><td>

Details about the household associated with the install base item record. Only returned if the Customer Service Household \(com.snc.household\) plugin is installed.Data type: Object

```
"household": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.household.display\_value

</td><td>

Text name of the household associated with the install base item record. Use this value to display the household name in the UI.Data type: String

</td></tr><tr><td>

item.household.sys\_id

</td><td>

Sys\_id of the household associated with the install base item record.Data type: String

</td></tr><tr><td>

item.install\_date

</td><td>

Details about the date when the install base item became active.Data type: Object

```
"install_date": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

item.install\_date.display\_value

</td><td>

Text install date. Use this value to display the install date in the UI.Data type: String

</td></tr><tr><td>

item.install\_date.value

</td><td>

Internal value of the install date.Data type: String

</td></tr><tr><td>

item.location

</td><td>

Details about the location of the install base item.Data type: Object

```
"location": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.location.display\_value

</td><td>

Text name of the install base item location. Use this value to display the location name in the UI.Data type: String

</td></tr><tr><td>

item.location.sys\_id

</td><td>

Sys\_id of the location record associated with the install base item record.Data type: String

</td></tr><tr id="name-integration-row"><td>

item.name

</td><td>

Name of the install base item.Data type: String

</td></tr><tr id="number-integration-row"><td>

item.number

</td><td>

Unique ID of the install base item.Data type: String

</td></tr><tr><td>

item.parent

</td><td>

Details about the parent record of the install base item record.Data type: Object

```
"parent": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.parent.display\_value

</td><td>

Text name of the parent record associated with the install base item record. Use this value to display the parent name in the UI.Data type: String

</td></tr><tr><td>

item.parent.sys\_id

</td><td>

Sys\_id of the parent record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.product

</td><td>

Details about the product model associated with the install base item record. Use this information to identify the services associated with any product model.Data type: Object

```
"product": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.product.display\_value

</td><td>

Text name of the product model associated with the install base item record. Use this value to display the product name in the UI.Data type: String

</td></tr><tr><td>

item.product.sys\_id

</td><td>

Sys\_id of the product model record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.service\_context

</td><td>

Details about the service context associated with the install base item record.Data type: Object

```
"service_context": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.service\_context.display\_value

</td><td>

Details about the service context associated with the install base item record.Data type: Object

```
"service_context": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.service\_context.sys\_id

</td><td>

Sys\_id of the service context record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.service\_organization

</td><td>

Details about the service organization associated with the install base item record. Only returned if the Service Organization \(com.snc.service\_organization\) plugin is installed.Data type: Object

```
"service_organization": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.service\_organization.display\_value

</td><td>

Text name of the service organization associated with the install base item record. Use this value to display the service organization name in the UI.Data type: String

</td></tr><tr><td>

item.service\_organization.sys\_id

</td><td>

Sys\_id of the service organization record associated with the install base item record.Data type: String

</td></tr><tr id="sys_class_name-integration-row"><td>

item.sys\_class\_name

</td><td>

Table containing the install base item record.Data type: String

</td></tr><tr id="sys_id-integration-row"><td>

item.sys\_id

</td><td>

Sys\_id of the install base item record. Located in the table specified in the **sys\_class\_name** parameter.Data type: String

</td></tr><tr><td>

item.sys\_mod\_count

</td><td>

Number of times that the associated install base item record has been modified.Data type: String

</td></tr><tr id="state-integration-row"><td>

item.state

</td><td>

Details about the current state of the install base item.Data type: Object

```
"state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="state_display_value-integration-row"><td>

item.state.display\_value

</td><td>

Text string of the current state of the install base item. Use this value to display the state in the UI.Data type: String

</td></tr><tr id="state_value-integration-row"><td>

item.state.value

</td><td>

Internal value of the state of the install base item.Data type: String

</td></tr><tr><td>

item.status

</td><td>

Details about the status of the install base item.Data type: Object

```
"status": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

item.status.display\_value

</td><td>

Text string of the status of the install base item. Use this value to display the status in the UI.Data type: String

</td></tr><tr><td>

item.status.value

</td><td>

Internal value of the status of the install base item.Data type: String

</td></tr><tr><td>

item.uninstall\_date

</td><td>

Details about the date when the install base item became inactive.Data type: Object

```
"uninstall_date": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

item.uninstall\_date.display\_value

</td><td>

Text uninstall date. Use this value to display the uninstall date in the UI.Data type: String

</td></tr><tr><td>

item.uninstall\_date.value

</td><td>

Internal value of the uninstall date.Data type: String

</td></tr><tr id="status-integration-row"><td>

status

</td><td>

Status of the endpoint call.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint. The associated install base item doesn't have any children.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/installbaseitem/f77c7542b7343300ece839a6ee11a991" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "status": "SUCCESS",
    "item": {
      "sys_class_name": "sn_install_base_item",
      "number": "IBITM0000901",
      "sys_id": "f77c7542b7343300ece839a6ee11a991",
      "product": {
        "sys_id": "8583ce8237732000158bbfc8bcbe5dd9",
        "display_value": "Fujitsu 1TB Hybrid Solid State Drive"
      },
      "active": "true",
      "name": "KX Series - KX5001",
      "account": {
        "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
        "display_value": "Boxeo"
      }
    },
    "hasChildren": "false"
  }
}
```

### cURL request

The following code example shows how to call this endpoint specifying a maximum depth of four child-levels.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/installbaseitems/e0a80e4b87b521100b6afc86dabb3565?depth=4" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "status": "SUCCESS",
    "item": {
      "sys_class_name": "sn_install_base_item",
      "number": "IBITM0001073",
      "sys_id": "e0a80e4b87b521100b6afc86dabb3565",
      "health_status": {
        "value": "not_available",
        "display_value": "Not Available"
      },
      "active": "true",
      "name": "parent",
      "account": {
        "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
        "display_value": "Boxeo"
      }
    },
    "hasChildren": "true",
    "childinstallbase": {
      "sysparm_depth": 2,
      "items": [
        {
          "parent": {
            "sys_id": "e0a80e4b87b521100b6afc86dabb3565",
            "display_value": "parent"
          },
          "sys_class_name": "sn_install_base_item",
          "number": "IBITM0001074",
          "sys_id": "6db80e4b87b521100b6afc86dabb356b",
          "state": {
            "value": "in_use",
            "display_value": "In Use"
          },
          "health_status": {
            "value": "not_available",
            "display_value": "Not Available"
          },
          "active": "true",
          "name": "child1",
          "account": {
            "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
            "display_value": "Boxeo"
          },
          "hasChildren": "true",
          "items": {
            "sysparm_depth": 3,
            "items": [
              {
                "parent": {
                  "sys_id": "6db80e4b87b521100b6afc86dabb356b",
                  "display_value": "child1"
                },
                "sys_class_name": "sn_install_base_item",
                "number": "IBITM0001075",
                "sys_id": "36ecce4b87b521100b6afc86dabb3503",
                "health_status": {
                  "value": "not_available",
                  "display_value": "Not Available"
                },
                "active": "true",
                "name": "childL2",
                "account": {
                  "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
                  "display_value": "Boxeo"
                },
                "hasChildren": "false"
              }
            ]
          }
        }
      ]
    }
  }
}
```

## Install Base Item - GET /sn\_install\_base/integrations/installbaseitems/\{id\}/cases

Returns the cases associated with a specified install base item record.

### URL format

Versioned URL: `/api/sn_install_base/{api_version}/integrations/installbaseitems/{id}/cases`

Default URL: `/api/sn_install_base/integrations/installbaseitems/{id}/cases`

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

</td><td id="integrate-id-entry">

Sys\_id of the install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

field name-value pairs

</td><td>

Field-value pairs to use to filter the case records. If you specify a different table in **sys\_class\_name**, then specify the fields in that table.You can pass one or more field-value pairs to filter the return results.

For example, to return only records where the approval field is set to "rejected" and the category field is set to "2", pass the follow: `&approval=rejected&category=2`.

Data type: String

Table: Case \[sn\_customerservice\_case\]

Default: All fields

</td></tr><tr><td>

sys\_class\_name

</td><td>

If using an extended case table \(not sn\_customerservice\_case\), the name of the extended table to query.Data type: String

Default: sn\_customerservice\_case

</td></tr><tr><td>

sysparm\_limit

</td><td id="sysparm_limit-entry-RESTAPI">

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. This limit is applied before ACL evaluation. If no records return, including records you have access to, rearrange the record order so records you have access to return first.

**Note:** Unusually large **sysparm\_limit** values can impact system performance.

Data type: Number

Default: 10000

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-entry-RESTAPI">

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

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
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cases

</td><td>

List of cases associated with the specified install base item record.Data type: Array of Objects

```
"cases": [
  {
    "account": "String",
    "active": Boolean,
    "active_account_escalation": "String",
    "active_escalation": "String",
    "activity_due": "String",
    "additional_assignee_list": "String",
    "approval": "String",
    "approval_history": "String",
    "approval_set": "String",
    "asset": "String",
    "assigned_on": "String",
    "assigned_to": "String",
    "assignment_group": "String",
    "auto_close": Boolean,
    "business_duration": "String",
    "business_impact": "String",
    "business_service": "String",
    "calendar_duration": "String",
    "case": "String",
    "case_report": "String",
    "category": Number,
    "cause": "String",
    "caused_by": "String",
    "change": "String",
    "child_case_creation_progress": Boolean,
    "closed_at": "String",
    "closed_by": "String",
    "close_notes: "String",
    "cmdb_ci": "String",
    "comments": "String",
    "comments_and_work_notes": "String",
    "company": "String",
    "consumer": "String",
    "contact": "String",
    "contact_local_time: "String",
    "contact_time_zone": "String",
    "contact_type": "String",
    "contract": "String",
    "contributor_groups": "String",
    "contributor_users": "String",
    "correlation_display": "String",
    "correlation_id": "String",
    "delivery_plan": "String",
    "delivery_task": "String",
    "description": "string",
    "due_date": "String",
    "entitlement": "String",
    "escalation": Number,
    "expected_start": "String",
    "first_response_time": "String",
    "follow_the_sun": Boolean,
    "follow_up": "String",
    "group_list": [Array],
    "impact": Number,
    "internal_user": "String",
    "initiated_as_request": Boolean,
    "knowledge": Boolean,
    "location": "String",
    "made_sla": Boolean,
    "major_case_state": "String",
    "needs_attention": Boolean,
    "notes_to_comments": Boolean,
    "notify": Number,
    "number": "String",
    "opened_at": "String",
    "opened_by": "String",
    "order": Number,
    "parent": "String",
    "partner": "String",
    "partner_contact": "String",
    "priority": Number,
    "proactive": Boolean,
    "probable_cause": "String",
    "problem": "String",
    "product": "String",
    "reassignment_count": Number,
    "recipient_list": "String",
    "rejection_goto": "String",
    "resolution_code": "String",
    "resolved_at": "String",
    "resolved_by": "String",
    "route_reason": "String",
    "service_offering": "String",
    "short_description": "String",
    "skills": "String",
    "sla_due": "String",
    "sn_app_cs_social_social_profile": "String",
    "sold_product": "String",
    "stage": "String",
    "state": Number,
    "subcategory": Number,
    "support_manager" "String",
    "sync_driver": Boolean,
    "sys_class_name": "String",
    "sys_domain": "String",
    "sys_domain_path": "String",
    "sys_id": "String",
    "task_effective_number": "String",
    "time_worked": "String",
    "universal_request": "String",
    "upon_approval": "String",
    "upon_reject": "String",
    "urgency": Number,
    "user_input": "String",
    "variables":  "String",
    "watch_list": [Array],
    "wf_activity": "String",
    "work_end": "String",
    "work_notes": "String",
    "work_notes_list": [Array],
    "work_start": "String"
```

</td></tr><tr><td>

cases.account

</td><td>

Sys\_id of the account record associated with the case.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

cases.active

</td><td>

Flag that indicates whether the case is open and active.Possible values:

-   true: Case is active
-   false: Case is closed

Data type: Boolean

Default: true

</td></tr><tr><td>

cases.active\_account\_escalation

</td><td>

Sys\_id of the active account escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

cases.active\_escalation

</td><td>

Sys\_id of the active escalation record associated with the case.Data type: String

Table: Escalation \[sn\_customerservice\_escalation\]

</td></tr><tr><td>

cases.activity\_due

</td><td>

Date for which the associated case is expected to be completed.Data type: String

</td></tr><tr><td>

cases.additional\_assignee\_list

</td><td>

List of the sys\_ids of the additional persons \(other than the primary assignee\) that have been assigned to the account.Data type: Array

Maximum: 4,000

Table: User \[sys\_user\]

</td></tr><tr><td>

cases.approval

</td><td>

String that describes the type of approval required.Possible values:

-   approved
-   cancelled
-   duplicate
-   not\_required
-   not requested
-   rejected
-   requested

Data type: String

Maximum characters: 40

Default: not requested

</td></tr><tr><td>

cases.approval\_history

</td><td>

List of all approvals associated with the case.Data type: String

Maximum characters: 4,000

</td></tr><tr><td>

cases.approval\_set

</td><td>

Date and time that the associated action was approved.Data type: String

</td></tr><tr><td>

cases.asset

</td><td>

Sys\_id of the asset record associated with the case.Data type: String

Table: Asset \[alm\_asset\]

</td></tr><tr><td>

cases.assigned\_on

</td><td>

Date and time that the case was assigned to the person identified in the **assigned\_to** parameter.Data type: String \(Date\)

Maximum length: 40

</td></tr><tr><td>

cases.assigned\_to

</td><td>

Sys\_id of the person assigned to the case.

Table: User \[sys\_user\]

 Data type: String

</td></tr><tr><td>

cases.assignment\_group

</td><td>

Sys\_id of the customer service agent group assigned to the case.Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

cases.auto\_close

</td><td>

Flag that indicates whether the case was automatically closed.Possible values:

-   true: Case was auto closed
-   false: Case wasn't auto closed

Data type: Boolean

Default: false

</td></tr><tr><td>

cases.business\_duration

</td><td>

Length in calendar work hours, work days, and work weeks that it took to complete the case.Data type: String

</td></tr><tr><td>

cases.business\_impact

</td><td>

Impact of the issue on the associated customer.Data type: String

Maximum characters: 4,000

</td></tr><tr><td>

cases.business\_service

</td><td>

Sys\_id of the service record associated with the case.Data type: String

Table: Service \[cmdb\_ci\_service\]

</td></tr><tr><td>

cases.calendar\_duration

</td><td>

Length in calendar hours, days, and weeks that it took to complete the case.Data type: String \(Duration\)

Maximum length: 40

</td></tr><tr><td>

cases.case

</td><td>

Case short description and case number.Data type: String

Maximum length: 300

</td></tr><tr><td>

cases.case\_report

</td><td>

Sys\_id of the associated case report.Data type: String

Table: Case Report \[sn\_customerservice\_case\_report\]

</td></tr><tr><td>

cases.category

</td><td>

Case category.Possible values:

-   0: Question
-   1: Issue
-   2: Feature

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

cases.cause

</td><td>

Details about the cause of the problem.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

cases.caused\_by

</td><td>

Sys\_id of the change request that caused the case to be created.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr><td>

cases.change

</td><td>

Sys\_id of the change request that caused the case to be created.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr><td>

cases.child\_case\_creation\_progress

</td><td>

Flag that indicates whether the case is a child case that was created from a major case.Possible values:

-   true: Child case created from a major case
-   false: Not a child case

Data type: Boolean

</td></tr><tr><td>

cases.closed\_at

</td><td>

Date and time that the case was closed.Data type: String

</td></tr><tr><td>

cases.closed\_by

</td><td>

Sys\_id of the user that closed the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

cases.close\_notes

</td><td>

Notes made when the case was closed.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

cases.cmdb\_ci

</td><td>

Sys\_id of the configuration item associated with the case.Data type: String

Table: Configuration Item \[cmdb\_ci\]

</td></tr><tr><td>

cases.comments

</td><td>

Additional comments about the case.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

cases.comments\_and\_work\_notes

</td><td>

Comments and work notes entered for the case.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

cases.company

</td><td>

Sys\_id of the company associated with the case.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

cases.consumer

</td><td>

Business-to-consumer cases only. Sys\_id of the person to contact with regard to this case.Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

cases.contact

</td><td>

Business-to-business based cases only. Sys\_id of the person to contact regarding this case.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

cases.contact\_local\_time

</td><td>

Contact local time.Data type: String

Maximum length: 70

</td></tr><tr><td>

cases.contact\_time\_zone

</td><td>

Time zone of the contact associated with the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

cases.contact\_type

</td><td>

Method in which the case was initially reported.Possible values:

-   chat
-   email
-   phone
-   social
-   web

Data type: String

Maximum length: 40

</td></tr><tr><td>

cases.contract

</td><td>

Sys\_id of the contract associated with the case. This contract contains information about the type of support that is provided to the company associated to the case. A contract can include a company and contact and the specific assets that are covered. A contract can also include multiple service entitlements and SLAs.Data type: String

Table: Contract \[ast\_contract\]

</td></tr><tr><td>

cases.contributor\_groups

</td><td>

List of sys\_ids of the user groups that have contributed to the case.Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

cases.contributor\_users

</td><td>

List of sys\_ids of the users that have contributed to the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

cases.correlation\_display

</td><td>

Correlation display.Data type: String

Maximum length: 100

</td></tr><tr><td>

cases.correlation\_id

</td><td>

Correlation identifier.Data type: String

Maximum length: 100

</td></tr><tr><td>

cases.delivery\_plan

</td><td>

Sys\_id of the parent execution plan for this case.Data type: String

Table: Execution Plan \[sc\_cat\_item\_delivery\_plan\]

</td></tr><tr><td>

cases.delivery\_task

</td><td>

Sys\_id of the execution plan task.Data type: String

Table: Execution Plan Task \[sc\_cat\_item\_delivery\_task\]

</td></tr><tr><td>

cases.description

</td><td>

Detailed description of the problem associated with the case. Data type: String

Maximum length: 4,000

</td></tr><tr><td>

cases.due\_date

</td><td>

Date that the case is due to be closed.Data type: String

</td></tr><tr><td>

cases.entitlement

</td><td>

Sys\_id of the entitlement record associated with the case. Entitlements define the type of support that a customer receives as well as the supported communication channels. An entitlement can be associated with a product, an asset, an account, or a contract.Data type: String

Table: Entitlement \[service\_entitlement\]

</td></tr><tr><td>

cases.escalation

</td><td>

Current escalation level.Possible values:

-   0: Normal
-   1: Moderate
-   2: High
-   3: Overdue

Data type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

cases.expected\_start

</td><td>

Date and time when work is scheduled to begin on the case.Data type: String

</td></tr><tr><td>

cases.first\_response\_time

</td><td>

Date and time when the first action was taken on the case.Data type: String

</td></tr><tr><td>

cases.follow\_the\_sun

</td><td>

Flag that indicates whether the case should be handed-off for global follow-up.If a customer enters additional comments on a Priority 1 - Critical or a Priority 2 - High case, or if the case is escalated, the flag is automatically set to true.

Possible values:

-   true: Case should be handed-off for global follow-up
-   false: Case shouldn't be handed-off for global follow-up

Data type: Boolean

Default: false

</td></tr><tr><td>

cases.follow\_up

</td><td>

Date and time of the next follow-up action.Data type: String

</td></tr><tr><td>

cases.group\_list

</td><td>

List of sys\_ids of the group records associated with the case.Data type: Array

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

cases.impact

</td><td>

Impact on customer.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Default: 3

</td></tr><tr><td>

cases.internal\_user

</td><td>

Sys\_id of the internal user for this case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

cases.initiated\_as\_request

</td><td>

Flag that indicates if this inquiry was initiated as a request by the customer.Possible values:

-   true: Inquiry initiated by customer.
-   false: Inquiry wasn't initiated by customer.

Data type: Boolean

Default: false

</td></tr><tr><td>

cases.knowledge

</td><td>

Flag that indicates if there is a knowledge base article available for the specified issue.Possible values:

-   true: Knowledge base article is available for this issue
-   false: Knowledge base article is not available for this issue

Data type: Boolean

Default: false

</td></tr><tr><td>

cases.location

</td><td>

Sys\_id of the record describing the company location.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

cases.made\_sla

</td><td>

Flag that indicates whether the case was resolved in alignment with the associated service level agreement.Possible values:

-   true: Case was resolved in alignment with SLA
-   false: Case wasn't resolved according to the SLA

Data type: Boolean

Default: true

</td></tr><tr><td>

cases.major\_case\_state

</td><td>

Current state of the major case.Possible values:

-   accepted: Initial state when a manager creates a major case or when a manager promotes a candidate case.
-   canceled: Case is canceled.
-   proposed: Initial state when an agent or manager creates or proposes a candidate case.
-   rejected: Manager rejected candidate case.

Data type: String

Maximum length: 40

</td></tr><tr><td>

needs\_attention

</td><td>

Flag that indicates whether the case needs attention.Possible values:

-   true: Case needs additional attention
-   false: Case doesn't need additional attention

Data type: Boolean

Default: false

</td></tr><tr><td>

cases.notes\_to\_comments

</td><td>

Flag that indicates whether to add the resolution notes to the comments.Possible values:

-   true: Resolutions notes, when added, are also added to the comments
-   false: Resolution notes in comments aren't required

Data type: Boolean

</td></tr><tr><td>

cases.notify

</td><td>

Method to use to notify contact/consumer.Possible values:

-   1: Do not notify
-   2: Send email
-   3: Telephone

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

cases.number

</td><td>

Case number.Data type: String

Maximum length: 40

</td></tr><tr><td>

cases.opened\_at

</td><td>

Date and time that the case was opened.Data type: String

</td></tr><tr><td>

cases.opened\_by

</td><td>

Sys\_id of the person that initially opened the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

cases.order

</td><td>

Order of the case.Data type: Number \(Integer\)

</td></tr><tr><td>

cases.parent

</td><td>

Sys\_id of the parent case to which this case \(child\) is associated.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

cases.partner

</td><td>

Sys\_id of the partner associated with the case.Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

cases.partner\_contact

</td><td>

Sys\_id of the partner contact associated with the case.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

cases.priority

</td><td>

Priority of the case. Possible values:

-   1: Critical
-   2: High
-   3: Moderate
-   4: Low

Data type: Number \(Integer\)

Default: 4

</td></tr><tr><td>

cases.proactive

</td><td>

Flag that indicates whether the inquiry is being proactively monitored.Possible values:

-   true: Being proactively monitored.
-   false: Not being monitored.

Data type: Boolean

Default:false

</td></tr><tr><td>

cases.probable\_cause

</td><td>

Possible cause of the issue associated with the case.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

cases.problem

</td><td>

Sys\_id of the issue that the customer is encountering.Data type: String

Table: Problem \[problem\]

</td></tr><tr><td>

cases.product

</td><td>

Sys\_id of the product model of the asset associated to the case. A model is a specific version or configuration of an asset \(for example, Apple Mac Book Pro\).Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

cases.reassignment\_count

</td><td>

Number of times that the case was reassigned to a person that is responsible for moving the case forward.Data type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

cases.recipient\_list

</td><td>

Sys\_id of the record that contains the list of recipients for communications about this case.Data type: String

Table: Recipients List \[sn\_publications\_recipients\_list\]

</td></tr><tr><td>

cases.rejection\_goto

</td><td>

Sys\_id of the task to execute if the case is rejected.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

cases.resolution\_code

</td><td>

Resolution state for the case, such as "Solved - Fixed by Support/Guidance provided". Data type: String

Maximum length: 40

</td></tr><tr><td>

cases.resolved\_at

</td><td>

Date and time that the case was resolved.Data type: String

</td></tr><tr><td>

cases.resolved\_by

</td><td>

Sys\_id of the person that resolved the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

cases.route\_reason

</td><td>

Reason that the case was routed to a different assignee.Data type: Number \(Integer\)

Maximum length: 40

</td></tr><tr><td>

cases.service\_offering

</td><td>

Sys\_id of the service offering associated with the payment inquiry. Service offerings uniquely define the level of service in terms of availability, scope, pricing, and packaging options.Data type: String

Table: Service Offering \[service\_offering\]

</td></tr><tr><td>

cases.short\_description

</td><td>

Concise description of the case. Data type: String

Maximum length: 160

</td></tr><tr><td>

cases.skills

</td><td>

List of the unique identifiers \(sys\_id\) of the skills needed to complete the case.Data type: String

Table: Skill \[cmn\_skill\]

</td></tr><tr><td>

cases.sla\_due

</td><td>

Date/time at which the case must be closed based on the associated service level agreement.Data type: String

</td></tr><tr><td>

cases.sn\_app\_cs\_social\_social\_profile

</td><td>

Sys\_id of the social media profile associated with the case.Data type: String

Table: Social Profile \[sn\_app\_cs\_social\_social\_profile\]

</td></tr><tr><td>

cases.sold\_product

</td><td>

Sys\_id of the associated product.Data type: String

Table: Sold Product \[sn\_install\_base\_sold\_product\]

</td></tr><tr><td>

cases.stage

</td><td>

Stage of the inquiry, such as Closed Complete, Closed Rejected, Document Check, Authorization, and so on.Data type: String

Maximum length: 40

</td></tr><tr><td>

cases.state

</td><td>

Current state of the case.Possible values:

-   1: New
-   3: Closed
-   6: Resolved
-   10: Open
-   18: Awaiting Info

Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

cases.subcategory

</td><td>

Case subcategory.Possible values:

0: QuestionData type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

cases.support\_manager

</td><td>

Sys\_id of the CSM manager assigned to the case.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

cases.sync\_driver

</td><td>

Flag that indicates whether there's driver synchronization.Possible values:

-   true: Driver is synchronized
-   false: Driver isn't synchronized

Data type: Boolean

</td></tr><tr><td>

cases.sys\_class\_name

</td><td>

Table that contains the case record.Data type: String

Maximum length: 80

</td></tr><tr><td>

cases.sys\_domain

</td><td>

Domain associated with the case.Data type: String

Maximum length: 32

Default: global

</td></tr><tr><td>

cases.sys\_domain\_path

</td><td>

Domain path.Data type: String

Maximum length: 255

Default: /

</td></tr><tr><td>

cases.sys\_id

</td><td>

Unique identifier for the case.Data type: String

Maximum length: 32

</td></tr><tr><td>

cases.task\_effective\_number

</td><td>

Identifying number. If the task has a Universal Request associated with it, it's the UR number. Otherwise, it's the current task number.

Data type: String

Maximum length: 40

</td></tr><tr><td>

cases.time\_worked

</td><td>

Total amount of time worked on the case.Data type: String

</td></tr><tr><td>

cases.universal\_request

</td><td>

Sys\_id of a universal task that this inquiry is part of.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

cases.upon\_approval

</td><td>

Action to take if the case is approved.Possible values:

-   do\_nothing
-   proceed

Data type: String

Maximum length: 40

Default: proceed

</td></tr><tr><td>

cases.upon\_reject

</td><td>

Action to take if the case is rejected.Possible values:

-   cancel
-   goto

Data type: String

Maximum length: 40

Default: cancel

</td></tr><tr><td>

cases.urgency

</td><td>

Urgency of the case.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Default: 3

</td></tr><tr><td>

cases.user\_input

</td><td>

Additional user input.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

cases.variables

</td><td>

Name-value pairs of variables associated with the case.Data type: String

Maximum length: 40

</td></tr><tr><td>

cases.watch\_list

</td><td>

List of sys\_ids of the users who receive notifications about this case when additional comments are added or if the state of a case is changed to Resolved or Closed.Data type: Array

Table: User \[sys\_user\]

</td></tr><tr><td>

cases.wf\_activity

</td><td>

Sys\_id of the workflow activity record associated with the case.Data type: String

Table: Workflow Activity \[wf\_activity\]

</td></tr><tr><td>

cases.work\_end

</td><td>

Date and time work ended on the case.Data type: String

</td></tr><tr><td>

cases.work\_notes

</td><td>

Information about how to resolve the case, or steps taken to resolve it.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

cases.work\_notes\_list

</td><td>

List of sys\_ids of the internal users who receive notifications about this case when work notes are added.Data type: Array

Table: User \[sys\_user\]

</td></tr><tr><td>

cases.work\_start

</td><td>

Date and time that work started on the case.Data type: String

</td></tr><tr><td>

has\_more

</td><td id="has_more-integration-entry">

Flag that indicates whether there are more records in the table to return.Possible values:

-   true: More records to return.
-   false: No more records to return.

Data type: Boolean string

</td></tr><tr><td>

status

</td><td id="status-integration-entry">

Status of the endpoint call.Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td id="sysparm-limit-entry">

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval.

In the response, the boolean parameter **hasMore** is returned. It indicates whether there are more records to return that meet the filter criteria.

Data type: Number

Default: 10

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm-offset-entry">

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks.

For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Do not pass a negative number in the **sysparm\_offset** parameter.

Data type: Number

Default: 0

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/installbaseitems/1474a3c853500010df5dddeeff7b12ec/cases" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "sysparm_offset": 0,
    "sysparm_limit": 10,
    "has_more": false,
    "cases": [
      {
        "upon_reject": {
          "value": "cancel",
          "display_value": "Cancel all future Tasks"
        },
        "number": "CS0001034",
        "initiated_as_request": "0",
        "state": "1",
        "case": "Performance is impacted with latest update​CS0001034",
        "knowledge": "0",
        "impact": "3",
        "contract": {
          "sys_id": "495e16b96f0731003b3c498f5d3ee4af",
          "display_value": "CNTR0000603"
        },
        "active": "1",
        "auto_created_case": "0",
        "priority": "4",
        "sys_domain_path": "/",
        "child_case_creation_progress": "0",
        "sync_driver": "0",
        "needs_attention": "0",
        "short_description": "Performance is impacted with latest update",
        "notify": "1",
        "sys_class_name": "sn_customerservice_case",
        "reassignment_count": "0",
        "notes_to_comments": "0",
        "hierarchical_variables": "variable_pool",
        "escalation": "0",
        "upon_approval": {
          "value": "proceed",
          "display_value": "Proceed to Next Task"
        },
        "made_sla": "1",
        "task_effective_number": "CS0001034",
        "opened_by": {
          "sys_id": "ddce70866f9331003b3c498f5d3ee417",
          "display_value": "George Warren"
        },
        "contact": {
          "sys_id": "ddce70866f9331003b3c498f5d3ee417",
          "display_value": "George Warren"
        },
        "follow_the_sun": "0",
        "entitlement": {
          "sys_id": "1eb7893a6f1b31003b3c498f5d3ee4dd",
          "display_value": "24x7 Customer Support"
        },
        "opened_at": {
          "value": "2023-03-20 14:53:51",
          "display_value": "2023-03-20 07:53:51"
        },
        "case_report": {
          "sys_id": "85e8604c87f521100b6afc86dabb35b9",
          "display_value": "CSR0010014"
        },
        "subcategory": "0",
        "install_base": {
          "sys_id": "1474a3c853500010df5dddeeff7b12ec",
          "display_value": "Boxeo - Development"
        },
        "proactive": "0",
        "auto_close": "0",
        "sys_id": "92c8684087b521105d0055373cbb357e",
        "contact_type": {
          "value": "web",
          "display_value": "Web"
        },
        "urgency": "3",
        "approval": {
          "value": "not requested",
          "display_value": "Not Yet Requested"
        },
        "category": "1",
        "account": {
          "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
          "display_value": "Boxeo"
        }
      },
      {
        "upon_reject": {
          "value": "cancel",
          "display_value": "Cancel all future Tasks"
        },
        "number": "CS0001008",
        "initiated_as_request": "0",
        "state": "1",
        "case": "Test Alert​CS0001008",
        "knowledge": "0",
        "impact": "3",
        "active": "1",
        "auto_created_case": "0",
        "priority": "1",
        "sys_domain_path": "/",
        "child_case_creation_progress": "0",
        "sync_driver": "0",
        "needs_attention": "1",
        "short_description": "Test Alert",
        "notify": "1",
        "sys_class_name": "sn_customerservice_case",
        "reassignment_count": "0",
        "notes_to_comments": "0",
        "hierarchical_variables": "variable_pool",
        "escalation": "0",
        "upon_approval": {
          "value": "proceed",
          "display_value": "Proceed to Next Task"
        },
        "made_sla": "1",
        "task_effective_number": "CS0001008",
        "opened_by": {
          "sys_id": "08c83021acbe7300964fca436af2bb97",
          "display_value": "noc_operator "
        },
        "follow_the_sun": "0",
        "opened_at": {
          "value": "2023-03-15 08:02:58",
          "display_value": "2023-03-15 01:02:58"
        },
        "case_report": {
          "sys_id": "a4fa9d9a872d61105d0055373cbb356e",
          "display_value": "CSR0010005"
        },
        "subcategory": "0",
        "proactive": "1",
        "auto_close": "0",
        "sys_id": "60ea199a872d61105d0055373cbb35c9",
        "contact_type": {
          "value": "proactive",
          "display_value": "Alert"
        },
        "alert": {
          "sys_id": "506a559a872d61105d0055373cbb3581",
          "display_value": "Alert0010008"
        },
        "urgency": "3",
        "action_status": "4",
        "approval": {
          "value": "not requested",
          "display_value": "Not Yet Requested"
        },
        "category": "1"
      },
      {
        "upon_reject": {
          "value": "cancel",
          "display_value": "Cancel all future Tasks"
        },
        "number": "CS0001033",
        "initiated_as_request": "0",
        "state": "1",
        "case": "System is down​CS0001033",
        "knowledge": "0",
        "impact": "3",
        "contract": {
          "sys_id": "495e16b96f0731003b3c498f5d3ee4af",
          "display_value": "CNTR0000603"
        },
        "active": "1",
        "auto_created_case": "0",
        "priority": "4",
        "sys_domain_path": "/",
        "child_case_creation_progress": "0",
        "sync_driver": "0",
        "needs_attention": "0",
        "short_description": "System is down",
        "notify": "1",
        "sys_class_name": "sn_customerservice_case",
        "reassignment_count": "0",
        "notes_to_comments": "0",
        "hierarchical_variables": "variable_pool",
        "escalation": "0",
        "upon_approval": {
          "value": "proceed",
          "display_value": "Proceed to Next Task"
        },
        "made_sla": "1",
        "task_effective_number": "CS0001033",
        "opened_by": {
          "sys_id": "ddce70866f9331003b3c498f5d3ee417",
          "display_value": "George Warren"
        },
        "contact": {
          "sys_id": "ddce70866f9331003b3c498f5d3ee417",
          "display_value": "George Warren"
        },
        "follow_the_sun": "0",
        "entitlement": {
          "sys_id": "1eb7893a6f1b31003b3c498f5d3ee4dd",
          "display_value": "24x7 Customer Support"
        },
        "opened_at": {
          "value": "2023-03-20 14:52:48",
          "display_value": "2023-03-20 07:52:48"
        },
        "case_report": {
          "sys_id": "64b86c0c87f521100b6afc86dabb35fc",
          "display_value": "CSR0010013"
        },
        "subcategory": "0",
        "install_base": {
          "sys_id": "1474a3c853500010df5dddeeff7b12ec",
          "display_value": "Boxeo - Development"
        },
        "proactive": "0",
        "auto_close": "0",
        "sys_id": "7c98a04087b521105d0055373cbb352e",
        "contact_type": {
          "value": "web",
          "display_value": "Web"
        },
        "urgency": "3",
        "approval": {
          "value": "not requested",
          "display_value": "Not Yet Requested"
        },
        "category": "1",
        "account": {
          "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
          "display_value": "Boxeo"
        }
      },
      {
        "upon_reject": {
          "value": "cancel",
          "display_value": "Cancel all future Tasks"
        },
        "number": "CS0001048",
        "initiated_as_request": "0",
        "state": "1",
        "case": "AIB with Single account​CS0001048",
        "knowledge": "0",
        "impact": "3",
        "active": "1",
        "auto_created_case": "0",
        "priority": "4",
        "sys_domain_path": "/",
        "child_case_creation_progress": "0",
        "sync_driver": "0",
        "needs_attention": "1",
        "short_description": "AIB with Single account",
        "notify": "1",
        "sys_class_name": "sn_customerservice_case",
        "reassignment_count": "0",
        "notes_to_comments": "0",
        "hierarchical_variables": "variable_pool",
        "escalation": "0",
        "upon_approval": {
          "value": "proceed",
          "display_value": "Proceed to Next Task"
        },
        "made_sla": "1",
        "task_effective_number": "CS0001048",
        "opened_by": {
          "sys_id": "08c83021acbe7300964fca436af2bb97",
          "display_value": "noc_operator "
        },
        "contact": {
          "sys_id": "4d147a386f0331003b3c498f5d3ee437",
          "display_value": "Julie Lewis"
        },
        "follow_the_sun": "0",
        "opened_at": {
          "value": "2023-03-24 03:28:58",
          "display_value": "2023-03-23 20:28:58"
        },
        "case_report": {
          "sys_id": "4082be81877161100b6afc86dabb35fe",
          "display_value": "CSR0010023"
        },
        "subcategory": "0",
        "proactive": "1",
        "auto_close": "0",
        "sys_id": "6a723e81877161100b6afc86dabb35cf",
        "contact_type": {
          "value": "proactive",
          "display_value": "Alert"
        },
        "alert": {
          "sys_id": "6b227681877161100b6afc86dabb35d5",
          "display_value": "Alert0010094"
        },
        "urgency": "3",
        "action_status": "4",
        "approval": {
          "value": "not requested",
          "display_value": "Not Yet Requested"
        },
        "category": "1",
        "account": {
          "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
          "display_value": "Boxeo"
        }
      }
    ],
    "status": "SUCCESS"
  }
}
```

## Install Base Item - GET /sn\_install\_base/integrations/installbaseitems/\{id\}/childinstallbaseitems

Returns the child install base items associated with a specified install base item record.

### URL format

Versioned URL: `/api/sn_install_base/{api_version}/integrations/installbaseitems/{id}/childinstallbaseitems`

Default URL: `/api/sn_install_base/integrations/installbaseitems/{id}/childinstallbaseitems`

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

</td><td id="integrate-id-entry">

Sys\_id of the install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

field name-value pairs

</td><td>

Field-value pairs to use to filter the child install base item records.If you specify a different table in **sys\_class\_name**, then specify the fields in that table.You can pass one or more field-value pairs to filter the return results.

For example, to return only records where the state field is set to "in\_use" and the status field is set to "replacement", pass the follow: `&state=in_use&status=replacement`.

Data type: String

Default: All fields

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

sys\_class\_name

</td><td>

If using an extended install base items table \(not sn\_install\_base\_item\), the name of the extended table to query.Data type: String

Default: sn\_install\_base\_item

</td></tr><tr><td>

sysparm\_limit

</td><td id="sysparm_limit-entry-RESTAPI">

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. This limit is applied before ACL evaluation. If no records return, including records you have access to, rearrange the record order so records you have access to return first.

**Note:** Unusually large **sysparm\_limit** values can impact system performance.

Data type: Number

Default: 10000

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-entry-RESTAPI">

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

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
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="id_qfp_hxl_xwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Details about the error that occurred when trying to process the request.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional details about the associated error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that describes the problem that occurred when trying to execute the request.Data type: String

</td></tr><tr id="has_more-integration-row"><td>

has\_more

</td><td id="has_more-integration-entry">

Flag that indicates whether there are more records in the table to return.Possible values:

-   true: More records to return.
-   false: No more records to return.

Data type: Boolean string

</td></tr><tr><td>

items

</td><td>

List of the install base items that matched the specified filter results.Data type: Array of Objects

```
"items":[
  {
    "account": {Object},
    "active": "String",
    "asset": {Object},
    "configuration_item": {Object},
    "consumer": {Object},
    "consumer_profile": {Object},
    "contact": {Object},
    "health_status": {Object},
    "health_status_last_updated": "String",
    "household": {Object},
    "install_date": {Object},
    "location": {Object},
    "name": "String",
    "number": "String",
    "parent": {Object},
    "product": {Object},
    "service_context": {Object},
    "service_organization" {Object},
    "sys_class_name": "String",
    "sys_id": "String",
    "sys_mod_count": "String",
    "state": {Object},
    "status": {Object},
    "uninstall_date": "String"
  }
]
```

</td></tr><tr id="account-integration-row"><td>

items.account

</td><td id="account-integration-entry">

Details about the customer account associated with the install base item record.Data type: Object

```
"account": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="account_display_value-integration-row"><td>

items.account.display\_value

</td><td id="account_display_value-integration-entry">

Text name of the customer account associated with the install base item record. Use this value to display the customer account name in the UI.Data type: String

</td></tr><tr id="account_sys_id-integration-row"><td>

items.account.sys\_id

</td><td id="account_sys_id-integration-entry">

Sys\_id of the customer account record associated with the install base item record.Data type: String

</td></tr><tr id="active-integration-row"><td>

items.active

</td><td id="active-integration-entry">

Flag that indicates whether the install base item is active.Possible values:

-   true: Install base item is active.
-   false: Install base item is inactive.

Data type: Boolean String

</td></tr><tr id="asset-integration-row"><td>

items.asset

</td><td id="asset-integration-entry">

Details about the asset associated with the install base item record.Data type: Object

```
"asset": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="asset_display_value-integration-row"><td>

items.asset.display\_value

</td><td id="asset_display_value-integration-entry">

Text name of the asset associated with the install base item record. Use this value to display the asset name in the UI.Data type: String

</td></tr><tr id="asset_sys_id-integration-row"><td>

items.asset.sys\_id

</td><td id="asset_sys_id-integration-entry">

Sys\_id of the asset record associated with the install base item record.Data type: String

</td></tr><tr id="configuration_item-integration-row"><td>

items.configuration\_item

</td><td id="configuration_item-integration-entry">

Details about the configuration item associated with the install base item record.Data type: Object

```
"configuration_item": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="configuration_item_display_value-integration-row"><td>

items.configuration\_item.display\_value

</td><td id="configuration_item_display_value-integration-entry">

Text name of the configuration item associated with the install base item record. Use this value to display the configuration item name in the UI.Data type: String

</td></tr><tr id="configuration_item_sys_id-integration-row"><td>

items.configuration\_item.sys\_id

</td><td id="configuration_item_sys_id-integration-entry">

Sys\_id of the configuration item record associated with the install base item record.Data type: String

</td></tr><tr id="consumer-integration-row"><td>

items.consumer

</td><td id="consumer-integration-entry">

Details about the consumer associated with the install base item record.**Note:** The consumer field is only available if the B2B2C plugin is installed.

Data type: Object

```
"consumer": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="consumer_display_value-integration-row"><td>

items.consumer.display\_value

</td><td id="consumer_display_value-integration-entry">

Text name of the consumer associated with the install base item record. Use this value to display the consumer name in the UI.Data type: String

</td></tr><tr id="consumer_sys_id-integration-row"><td>

items.consumer.sys\_id

</td><td id="consumer_sys_id-integration-entry">

Sys\_id of the consumer record associated with the install base item record.Data type: String

</td></tr><tr id="consumer_profile-integration-row"><td>

items.consumer\_profile

</td><td id="consumer_profile-integration-entry">

Details about the consumer profile associated with the install base item record.**Note:** The consumer profile field is only available if the B2B2C plugin is installed.

Data type: Object

```
"consumer_profile": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="consumer_profile_display_value-integration-row"><td>

items.consumer\_profile.display\_value

</td><td id="consumer_profile_display_value-integration-entry">

Text name of the consumer profile associated with the install base item record. Use this value to display the consumer profile name in the UI.Data type: String

</td></tr><tr id="consumer_profile_sys_id-integration-row"><td>

items.consumer\_profile.sys\_id

</td><td id="consumer_profile_sys_id-integration-entry">

Sys\_id of the consumer profile record associated with the install base item record.Data type: String

</td></tr><tr id="contact-integration-row"><td>

items.contact

</td><td id="contact-integration-entry">

Details about the account contact responsible for the install base item record.Data type: Object

```
"contact": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="contact_display_value-integration-row"><td>

items.contact.display\_value

</td><td id="contact_display_value-integration-entry">

Text name of the account contact associated with the install base item record. Use this value to display the account contact name in the UI.Data type: String

</td></tr><tr id="contact_sys_id-integration-row"><td>

items.contact.sys\_id

</td><td id="contact_sys_id-integration-entry">

Sys\_id of the account contact record associated with the install base item record.Data type: String

</td></tr><tr id="health_status-integration-row"><td>

items.health\_status

</td><td id="health_status-integration-entry">

Details about the current health status of the install base item. Only returned if the Proactive Customer Service Operations \(com.snc.proactive\_cs\_itom\) plugin is installed.Data type: Object

```
"health_status": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="health_status_display_value-integration-row"><td>

items.health\_status.display\_value

</td><td id="health_status_display_value-integration-entry">

Text string of the current health status of the install base item. Use this value to display the health status in the UI.Data type: String

</td></tr><tr id="health_status_value-integration-row"><td>

items.health\_status.value

</td><td id="health_status_value-integration-entry">

Internal value of the health status of the install base item.Data type: String

</td></tr><tr id="health_status_last_updated-integration-row"><td>

items.health\_status\_last\_updated

</td><td id="health_status_last_updated-integration-entry">

Date and time when the health status was last updated for the install base item.Data type: String

</td></tr><tr id="household-integration-row"><td>

items.household

</td><td id="household-integration-entry">

Details about the household associated with the install base item record. Only returned if the Customer Service Household \(com.snc.household\) plugin is installed.Data type: Object

```
"household": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="household_display_value-integration-row"><td>

items.household.display\_value

</td><td id="household_display_value-integration-entry">

Text name of the household associated with the install base item record. Use this value to display the household name in the UI.Data type: String

</td></tr><tr id="household_sys_id-integration-row"><td>

items.household.sys\_id

</td><td id="household_sys_id-integration-entry">

Sys\_id of the household associated with the install base item record.Data type: String

</td></tr><tr id="install_date-integration-row"><td>

items.install\_date

</td><td id="install_date-integration-entry">

Details about the date when the install base item became active.Data type: Object

```
"install_date": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="install_date_isplay_value-integration-row"><td>

items.install\_date.display\_value

</td><td id="install_date_display_value-integration-entry">

Text install date. Use this value to display the install date in the UI.Data type: String

</td></tr><tr id="install_date_value-integration-row"><td>

items.install\_date.value

</td><td id="install_date_value-integration-entry">

Internal value of the install date.Data type: String

</td></tr><tr id="location-integration-row"><td>

items.location

</td><td id="location-integration-entry">

Details about the location of the install base item.Data type: Object

```
"location": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="location_display_value-integration-row"><td>

items.location.display\_value

</td><td id="location_display_value-integration-entry">

Text name of the install base item location. Use this value to display the location name in the UI.Data type: String

</td></tr><tr id="location_sys_id-integration-row"><td>

items.location.sys\_id

</td><td id="location_sys_id-integration-entry">

Sys\_id of the location record associated with the install base item record.Data type: String

</td></tr><tr id="name-integration-row"><td>

items.name

</td><td id="name-integration-entry">

Name of the install base item.Data type: String

</td></tr><tr id="number-integration-row"><td>

items.number

</td><td id="number-integration-entry">

Unique ID of the install base item.Data type: String

</td></tr><tr id="parent-integration-row"><td>

items.parent

</td><td id="parent-integration-entry">

Details about the parent record of the install base item record.Data type: Object

```
"parent": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="parent_display_value-integration-row"><td>

items.parent.display\_value

</td><td id="parent_display_value-integration-entry">

Text name of the parent record associated with the install base item record. Use this value to display the parent name in the UI.Data type: String

</td></tr><tr id="parent_sys_id-integration-row"><td>

items.parent.sys\_id

</td><td id="parent_sys_id-integration-entry">

Sys\_id of the parent record associated with the install base item record.Data type: String

</td></tr><tr id="product-integration-row"><td>

items.product

</td><td id="product-integration-entry">

Details about the product model associated with the install base item record. Use this information to identify the services associated with any product model.Data type: Object

```
"product": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="product_display_value-integration-row"><td>

items.product.display\_value

</td><td id="product_display_value-integration-entry">

Text name of the product model associated with the install base item record. Use this value to display the product name in the UI.Data type: String

</td></tr><tr id="product_sys_id-integration-row"><td>

items.product.sys\_id

</td><td id="product_sys_id-integration-entry">

Sys\_id of the product model record associated with the install base item record.Data type: String

</td></tr><tr id="service_context-integration-row"><td>

items.service\_context

</td><td id="service_context-integration-entry">

Details about the service context associated with the install base item record.Data type: Object

```
"service_context": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="service_context_display_value-integration-row"><td>

items.service\_context.display\_value

</td><td id="service_context_display_value-integration-entry">

Text name of the service context associated with the install base item record. Use this value to display the service context name in the UI.Data type: String

</td></tr><tr id="service_context_sys_id-integration-row"><td>

items.service\_context.sys\_id

</td><td id="service_context_sys_id-integration-entry">

Sys\_id of the service context record associated with the install base item record.Data type: String

</td></tr><tr id="service_organization-integration-row"><td>

items.service\_organization

</td><td id="service_organization-integration-entry">

Details about the service organization associated with the install base item record. Only returned if the Service Organization \(com.snc.service\_organization\) plugin is installed.Data type: Object

```
"service_organization": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="service_organization_display_value-integration-row"><td>

items.service\_organization.display\_value

</td><td id="service_organization_display_value-integration-entry">

Text name of the service organization associated with the install base item record. Use this value to display the service organization name in the UI.Data type: String

</td></tr><tr id="service_organization_sys_id-integration-row"><td>

items.service\_organization.sys\_id

</td><td id="service_organization_sys_id-integration-entry">

Sys\_id of the service organization record associated with the install base item record.Data type: String

</td></tr><tr id="sys_class_name-integration-row"><td>

items.sys\_class\_name

</td><td id="sys_class_name-integration-entry">

Table containing the install base item record.Data type: String

</td></tr><tr id="sys_id-integration-row"><td>

items.sys\_id

</td><td id="sys_id-integration-entry">

Sys\_id of the install base item record. Located in the table specified in the **sys\_class\_name** parameter.Data type: String

</td></tr><tr id="sys_mod_count-integration-row"><td>

items.sys\_mod\_count

</td><td id="sys_mod_count-integration-entry">

Number of times that the associated install base item record has been modified.Data type: String

</td></tr><tr id="state-integration-row"><td>

items.state

</td><td id="state-integration-entry">

Details about the current state of the install base item.Data type: Object

```
"state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="state_display_value-integration-row"><td>

items.state.display\_value

</td><td id="state_display_value-integration-entry">

Text string of the current state of the install base item. Use this value to display the state in the UI.Data type: String

</td></tr><tr id="state_value-integration-row"><td>

items.state.value

</td><td id="state_value-integration-entry">

Internal value of the state of the install base item.Data type: String

</td></tr><tr id="status1-integration-row"><td>

items.status

</td><td id="status1-integration-entry">

Details about the status of the install base item.Data type: Object

```
"status": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="status1_display_value-integration-row"><td>

items.status.display\_value

</td><td id="status1_display_value-integration-entry">

Text string of the status of the install base item. Use this value to display the status in the UI.Data type: String

</td></tr><tr id="status1_value-integration-row"><td>

items.status.value

</td><td id="status1_value-integration-entry">

Internal value of the status of the install base item.Data type: String

</td></tr><tr id="uninstall_date-integration-row"><td>

items.uninstall\_date

</td><td id="uninstall_date-integration-entry">

Details about the date when the install base item became inactive.Data type: Object

```
"uninstall_date": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="uninstall_date_display_value-integration-row"><td>

items.uninstall\_date.display\_value

</td><td id="uninstall_date_display_value-integration-entry">

Text uninstall date. Use this value to display the uninstall date in the UI.Data type: String

</td></tr><tr id="uninstall_date_value-integration-row"><td>

items.uninstall\_date.value

</td><td id="uninstall_date_value-integration-entry">

Internal value of the uninstall date.Data type: String

</td></tr><tr id="status-integration-row"><td>

status

</td><td id="status-integration-entry">

Status of the endpoint call.Data type: String

</td></tr><tr id="sysparm_depth-integration-row"><td>

sysparm\_depth

</td><td id="sysparm_depth-integration-entry">

Number of levels deep the returned child install base item is in the hierarchy.Data type: Integer

</td></tr><tr id="sysparm_limit-integration-row"><td>

sysparm\_limit

</td><td id="sysparm_limit-integration-entry">

Number of records that were returned. If this value isn't specified in the original request, it uses the default value.Data type: Number

</td></tr><tr id="sysparm_offset-integration-row"><td>

sysparm\_offset

</td><td id="sysparm_offset-integration-entry">

Offset \(starting point\) in the associated table from which records were evaluated and retrieved.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/installbaseitems/767f34d378d21110f877d304c76fdd2a/childinstallbaseitems?sysparm_limit=1" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "sysparm_offset": 0,
    "sysparm_limit": 1,
    "has_more": true,
    "items": [
      {
        "parent": {
          "sys_id": "767f34d378d21110f877d304c76fdd2a",
          "display_value": "X5 Sport Utility 4D"
        },
        "sys_class_name": "sn_install_base_item",
        "number": "IBITM0001005",
        "sys_id": "0704dfcc39265110f87734024cfbc222",
        "state": {
          "value": "in_use",
          "display_value": "In Use"
        },
        "consumer": {
          "sys_id": "bab5139ab3401010700b4d43c6a8dc41",
          "display_value": "Charles Barkley"
        },
        "product": {
          "sys_id": "56c84f0439265110f87734024cfbc233",
          "display_value": "Electric Power-Assist Speed-Sensing Steering"
        },
        "active": "true",
        "name": "Electric Power-Assist Speed-Sensing Steering",
        "status": {
          "value": "original",
          "display_value": "Original"
        }
      }
    ],
    "status": "SUCCESS"
  }
}
```

## Install Base Item - GET /sn\_install\_base/integrations/installbaseitems/\{id\}/contracts

Returns the contracts associated with a specified install base item record.

### URL format

Versioned URL: `/api/sn_install_base/{api_version}/integrations/installbaseitems/{id}/contracts`

Default URL: `/api/sn_install_base/integrations/installbaseitems/{id}/contracts`

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

</td><td id="integrate-id-entry">

Sys\_id of the install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

field name-value pairs

</td><td>

Field-value pairs to use to filter the contract records. By default this references the fields in the Contract \[ast\_contract\] table. If you specify a different table in **sys\_class\_name**, then specify the fields in that table.You can pass one or more field-value pairs to filter the return results.

For example, to return only records where the renewable field is set to "true", pass the follow: `&renewable=true`.

Data type: String

Default: All fields

</td></tr><tr><td>

sys\_class\_name

</td><td>

If using an extended contracts table \(not ast\_contract\), the name of the extended table to query.Data type: String

Default: ast\_contract

</td></tr><tr><td>

sysparm\_limit

</td><td id="sysparm_limit-entry-RESTAPI">

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. This limit is applied before ACL evaluation. If no records return, including records you have access to, rearrange the record order so records you have access to return first.

**Note:** Unusually large **sysparm\_limit** values can impact system performance.

Data type: Number

Default: 10000

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-entry-RESTAPI">

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

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
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contracts

</td><td>

List of the contracts associated with the specified install base item record.Data type: Array of Object

```
"contracts": [
  {
    "active": "String", 
    "approver": {Object},
    "commitment": "String",
    "consumer": {Object},
    "cost_adjustment": "String",
    "cost_adjustment_percentage": "String",
    "cost_per_unit": "String",
    "contract_composite": "String",
    "ends": "String",
    "expiration": {Object},
    "lifetime_cost": "String",
    "monthly_cost": "String",
    "number": "String",
    "payment_amount": "String",
    "payment_schedule": {Object},
    "ratecard": "String",
    "renewable": "String",
    "sales_tax": "String",
    "short_description": "String",
    "starts": "String",
    "state": {Object},
    "sub_total_cost": "String",
    "sys_class_name": "String",
    "sys_domain_path": "String",
    "sys_id": "String",
    "tax_cost": "String",
    "tax_exempt": "String",
    "tax_rate": "String",
    "total_cost": "String",
    "vendor_contract": "String",
    "yearly_cost": "String"
  }
]
```

</td></tr><tr><td>

contracts.active

</td><td>

Flag that indicates whether the contract is active.Possible values:

-   true: Contract is active.
-   false: Contract is inactive.

Data type: Boolean string

</td></tr><tr><td>

contracts.approver

</td><td>

Details about the person authorized to approve the contract.Data type: Object

```
"approver": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

contracts.approver.display\_value

</td><td>

Text name of the approver associated with the contracts record. Use this value to display the approver name in the UI.Data type: String

</td></tr><tr><td>

contracts.approver.sys\_id

</td><td>

Sys\_id of the approver record associated with the contracts record.Data type: String

</td></tr><tr><td>

contracts.consumer

</td><td>

Details about the consumer associated with the contracts record.**Note:** The consumer field is only available if the B2B2C plugin is installed.

Data type: Object

```
"consumer": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

contracts.consumer.display\_value

</td><td>

Text name of the consumer associated with the contracts record. Use this value to display the consumer name in the UI.Data type: String

</td></tr><tr><td>

contracts.consumer.sys\_id

</td><td>

Sys\_id of the consumer record associated with the contracts record.Data type: String

</td></tr><tr><td>

contracts.cost\_adjustment

</td><td>

Type of cost adjustment applied to the contract.Possible values:

-   Fixed
-   Manual
-   CPI \(consumer price index\)

Data type: String

</td></tr><tr><td>

contracts.cost\_adjustment\_percentage

</td><td>

Percentage increase or decrease in price of contract. To indicate a decrease in price, enter a negative percentage. Either a Cost adjustment or Cost adjustment percentage can be specified, but not both.Data type: String

</td></tr><tr><td>

contracts.cost\_per\_unit

</td><td>

Cost per unit from the product provider.Data type: String

</td></tr><tr><td>

contracts.ends

</td><td>

Date that the contract terminates.Data type: String

</td></tr><tr><td>

contracts.expiration

</td><td>

Details about the expiration status of the associated contract.Data type: Object

```
"expiration": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

contracts.expiration.display\_value

</td><td>

Expiration status of the associated contract. Use this value to display the expiration status in the UI.Data type: String

</td></tr><tr><td>

contracts.expiration.sys\_id

</td><td>

Sys\_id of the expiration record associated with the contracts record.Data type: String

</td></tr><tr><td>

contracts.lifetime\_cost

</td><td>

Lifetime cost of the contract.Data type: String

</td></tr><tr><td>

contracts.monthly\_cost

</td><td>

Monthly cost of the contract.Data type: String

</td></tr><tr><td>

contracts.number

</td><td>

Contract number.Data type: String

</td></tr><tr><td>

contracts.payment\_amount

</td><td>

Amount of money that has been directly paid to the receiving party of this contract.Data type: String

</td></tr><tr><td>

contracts.payment\_schedule

</td><td>

Details about the payment schedule associated with the contract.Data type: Object

```
"payment_schedule": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

contracts.payment\_schedule.display\_value

</td><td>

Payment schedule for the associated contract. Use this value to display the payment schedule in the UI.Data type: String

</td></tr><tr><td>

contracts.payment\_schedule.value

</td><td>

Internal value of the payment schedule for this contract, such as daily, weekly, or monthly.Data type: String

</td></tr><tr><td>

contracts.ratecard

</td><td>

Flag that indicates whether there's a rate card associated with this contract.Possible values:

-   true: Rate card.
-   false: No rate card.

Data type: Boolean string

Table: Rate Care \[fm\_contract\_rate\_card\]

</td></tr><tr><td>

contracts.renewable

</td><td>

Flag that indicates whether the contract is renewable.Possible values:

-   true: Contract is renewable.
-   false: Contract isn't renewable.

Data type: Boolean string

</td></tr><tr><td>

contracts.sales\_tax

</td><td>

Flag that indicates whether sales tax is charged for items referenced by this contract.Possible values:

-   true: Sales tax is charged.
-   false: No sales tax is charged.

Data type: Boolean string

</td></tr><tr><td>

contracts.short\_description

</td><td>

Brief description of the contract.Data type: String

</td></tr><tr><td>

contracts.starts

</td><td>

Date that the contract begins.Data type: String

</td></tr><tr><td>

contracts.state

</td><td>

Details about the current state of the contract.Data type: Object

```
"state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

contracts.state.display\_value

</td><td>

Text string of the current state of the contract. Use this value to display the state in the UI.Data type: String

</td></tr><tr><td>

contracts.state.value

</td><td>

Internal value or the state of the contract.Data type: String

</td></tr><tr><td>

contracts.sub\_total\_cost

</td><td>

Subtotal of the cost of the contract.Data type: String

</td></tr><tr><td>

contracts.sys\_class\_name

</td><td>

Table containing the contract record.Data type: String

</td></tr><tr><td>

contracts.sys\_domain\_path

</td><td>

Path to the domain in which this contract is available. Data type: String

Default: "/" = Global domain

</td></tr><tr><td>

contracts.sys\_id

</td><td>

Sys\_id of the associated contract record.Data type: String

</td></tr><tr><td>

contracts.tax\_cost

</td><td>

Total tax on the contract.This field is visible only if the applicable taxes field is selected as `Sales`.

Data type: String

</td></tr><tr><td>

contracts.tax\_exempt

</td><td>

Flag that indicates whether the items associated with this contract are tax exempt.Possible values:

-   true: Items are tax exempt.
-   false: Items aren't tax exempt.

Data type: Boolean string

</td></tr><tr><td>

contracts.tax\_rate

</td><td>

Tax rate charged for taxable items associated with the contract.Data type: String

</td></tr><tr><td>

contracts.total\_cost

</td><td>

Final cost of the contract after adjustments have been applied. If a contract has one or more rate cards, this field shows the combined value of all rate cards.Data type: String

</td></tr><tr><td>

contracts.vendor\_contract

</td><td>

Vendor's contract number.Data type: String

</td></tr><tr><td>

contracts.yearly\_cost

</td><td>

Cost per year of the contract.Data type: String

</td></tr><tr><td>

error

</td><td id="error-integration-entry">

Details about the error that occurred when trying to process the request.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td id="error_detail-integration-entry">

Additional details about the associated error.Data type: String

</td></tr><tr><td>

error.message

</td><td id="error_message-integration-entry">

Error message that describes the problem that occurred when trying to execute the request.Data type: String

</td></tr><tr><td>

has\_more

</td><td id="has_more-integration-entry">

Flag that indicates whether there are more records in the table to return.Possible values:

-   true: More records to return.
-   false: No more records to return.

Data type: Boolean string

</td></tr><tr><td>

status

</td><td id="status-integration-entry">

Status of the endpoint call.Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td id="sysparm_limit-integration-entry">

Number of records that were returned. If this value isn't specified in the original request, it uses the default value.Data type: Number

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-integration-entry">

Offset \(starting point\) in the associated table from which records were evaluated and retrieved.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/installbaseitems/167e96f053961910539dddeeff7b1298/contracts" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "sysparm_offset": 0,
    "sysparm_limit": 10,
    "has_more": false,
    "contracts": [
      {
        "cost_adjustment_percentage": "0",
        "total_cost": "0",
        "cost_adjustment": "0",
        "tax_rate": "7.75",
        "number": "CNTR0000701",
        "tax_cost": "0",
        "sub_total_cost": "0",
        "state": {
          "value": "expired",
          "display_value": "Expired"
        },
        "starts": "2016-07-01",
        "contract_composite": "CoolMate KL300 1 year Limited Warranty\n\t\t​CNTR0000701",
        "tax_exempt": "false",
        "yearly_cost": "0",
        "active": "true",
        "payment_amount": "0",
        "commitment": "0",
        "sys_domain_path": "/",
        "payment_schedule": {
          "value": "Monthly",
          "display_value": "Monthly"
        },
        "renewable": "true",
        "expiration": {
          "sys_id": "c752e78ec3103000c111113e5bba8f3a",
          "display_value": "Expired"
        },
        "short_description": "CoolMate KL300 1 year Limited Warranty\n\t\t",
        "ratecard": "false",
        "sys_class_name": "ast_contract",
        "sys_id": "3f9db778c3302200e7c7d44d81d3ae0a",
        "ends": "2017-06-30",
        "consumer": {
          "sys_id": "59e788fbdb1b1200b6075200cf9619d2",
          "display_value": "Gilly Parker"
        },
        "approver": {
          "sys_id": "f2c0b27247702000cdd1706eecde27c8",
          "display_value": "Software Manager"
        },
        "monthly_cost": "0",
        "vendor_contract": "CNTR0000701",
        "lifetime_cost": "0",
        "sales_tax": "true",
        "cost_per_unit": "0"
      }
    ],
    "status": "SUCCESS"
  }
}
```

## Install Base Item - GET /sn\_install\_base/integrations/installbaseitems/\{id\}/entitlements

Returns the entitlements associated with a specified install base item record.

### URL format

Versioned URL: `/api/sn_install_base/{api_version}/integrations/installbaseitems/{id}/entitlements`

Default URL: `/api/sn_install_base/integrations/installbaseitems/{id}/entitlements`

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

</td><td id="integrate-id-entry">

Sys\_id of the install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

field name-value pairs

</td><td>

Field-value pairs to use to filter the entitlements records. By default this references the fields in the Entitlement \[service\_entitlement\] table. If you specify a different table in **sys\_class\_name**, then specify the fields in that table.You can pass one or more field-value pairs to filter the return results.

For example, to return only records that are active, pass the following: `&active=true`.

Data type: String

Default: All fields

</td></tr><tr><td>

sys\_class\_name

</td><td>

If using an extended entitlements table \(not service\_entitlement\), the name of the extended table to query.Data type: String

Default: service\_entitlement

</td></tr><tr><td>

sysparm\_limit

</td><td id="sysparm_limit-entry-RESTAPI">

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. This limit is applied before ACL evaluation. If no records return, including records you have access to, rearrange the record order so records you have access to return first.

**Note:** Unusually large **sysparm\_limit** values can impact system performance.

Data type: Number

Default: 10000

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-entry-RESTAPI">

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

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
|400|Bad Request. A bad request type or malformed request was detected.|
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

List of the entitlements associated with the specified install base item record.Data type: Object

```
"entitlements": {
  "account": {Object},
  "active": "String",
  "business_hour": {Object},
  "contract": {Object},
  "end_date": "String",
  "entitlement_name": "String",
  "install_base_item": {Object},
  "per_unit": "String",
  "start_date": "String",
  "sys_id": "String",
  "total_units": "String",
  "remaining_units": "String",
  "unit": {Object}
  }
```

</td></tr><tr><td>

entitlements.account

</td><td>

Details about the account associated with the entitlements record.Data type: Object

```
"account": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

entitlements.account.display\_value

</td><td>

Text name of the account associated with the entitlements record. Use this value to display the account name in the UI.Data type: String

</td></tr><tr><td>

entitlements.account.sys\_id

</td><td>

Sys\_id of the account record associated with the entitlements record.Data type: String

</td></tr><tr><td>

entitlements.active

</td><td>

Flag that indicates whether the entitlement is active.Possible values:

-   0: Entitlement isn't active.
-   1: Entitlement is active.

Data type: String

Default: 1

</td></tr><tr><td>

entitlements.business\_hour

</td><td>

Details about the business hours for the entitlements record.Data type: Object

```
"business_hour": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

entitlements.business\_hour.display\_value

</td><td>

Text name of the business hours record associated with the entitlements record. Use this value to display the business hours in the UI.Data type: String

</td></tr><tr><td>

entitlements.business\_hour.sys\_id

</td><td>

Sys\_id of the business hours record associated with the entitlements record.Data type: String

</td></tr><tr><td>

entitlements.contract

</td><td>

Details about the contract associated with the entitlement record.Data type: Object

```
"contract": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

entitlements.contract.display\_value

</td><td>

Text name of the contract associated with the entitlement record. Use this value to display the contract name in the UI.Data type: String

</td></tr><tr><td>

entitlements.contract.sys\_id

</td><td>

Sys\_id of the contract record associated with the entitlement record.Data type: String

</td></tr><tr><td>

entitlements.end\_date

</td><td>

End date of the entitlement.Data type: String

</td></tr><tr><td>

entitlements.entitlement\_name

</td><td>

Name of the entitlement.Data type: String

</td></tr><tr><td>

entitlements.install\_base\_item

</td><td>

Details about the install base item associated with the entitlements record.Data type: Object

```
"install_base_item": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

entitlements.install\_base\_item.display\_value

</td><td>

Text name of the install base item associated with the entitlements record. Use this value to display the install base item name in the UI.Data type: String

</td></tr><tr><td>

entitlements.install\_base\_item.sys\_id

</td><td>

Sys\_id of the install base item record associated with the entitlements record.Data type: String

</td></tr><tr><td>

entitlements.per\_unit

</td><td>

Number of products in a unit. For example, if the **unit** is `case`, this value would be 12 if there are 12 items per case.Data type: String

</td></tr><tr><td>

entitlements.start\_date

</td><td>

Start date of the entitlement.Data type: String

</td></tr><tr><td>

entitlements.sys\_id

</td><td>

Sys\_id of the associated entitlements record.Data type: String

</td></tr><tr><td>

entitlements.total\_units

</td><td>

Number of units that were originally available.Data type: String

</td></tr><tr><td>

entitlements.remaining\_units

</td><td>

Number of units that are remaining.Data type: String

</td></tr><tr><td>

entitlements.unit

</td><td>

Details about the unit of the item associated with the entitlements record.Data type: Object

```
"unit": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

entitlements.unit.display\_value

</td><td>

Text name of the unit of the item associated with the entitlements record. Use this value to display the unit name in the UI.Data type: String

</td></tr><tr><td>

entitlements.unit.value

</td><td>

Internal name of the unit of the item associated with the entitlements record.Data type: String

</td></tr><tr><td>

error

</td><td id="error-integration-entry">

Details about the error that occurred when trying to process the request.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td id="error_detail-integration-entry">

Additional details about the associated error.Data type: String

</td></tr><tr><td>

error.message

</td><td id="error_message-integration-entry">

Error message that describes the problem that occurred when trying to execute the request.Data type: String

</td></tr><tr><td>

has\_more

</td><td id="has_more-integration-entry">

Flag that indicates whether there are more records in the table to return.Possible values:

-   true: More records to return.
-   false: No more records to return.

Data type: Boolean string

</td></tr><tr><td>

status

</td><td id="status-integration-entry">

Status of the endpoint call.Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td id="sysparm_limit-integration-entry">

Number of records that were returned. If this value isn't specified in the original request, it uses the default value.Data type: Number

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-integration-entry">

Offset \(starting point\) in the associated table from which records were evaluated and retrieved.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/installbaseitems/42746a3b876121100b6afc86dabb3597/entitlements" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "sysparm_offset": 0,
    "sysparm_limit": 10,
    "has_more": false,
    "entitlements": [
      {
        "end_date": "2023-04-28",
        "remaining_units": "4978",
        "business_hour": {
          "sys_id": "08fcd0830a0a0b2600079f56b1adb9ae",
          "display_value": "8-5 weekdays"
        },
        "entitlement_name": "Entitlement",
        "sys_id": "7206095d87f121105d0055373cbb3504",
        "total_units": "5000",
        "start_date": "2023-03-27",
        "contract": {
          "sys_id": "495e16b96f0731003b3c498f5d3ee4af",
          "display_value": "CNTR0000603"
        },
        "active": "1",
        "install_base_item": {
          "sys_id": "42746a3b876121100b6afc86dabb3597",
          "display_value": "KX Series - KX5000"
        },
        "unit": {
          "value": "cases",
          "display_value": "Cases"
        },
        "per_unit": "0",
        "account": {
          "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
          "display_value": "Boxeo"
        }
      }
    ],
    "status": "SUCCESS"
  }
}
```

## Install Base Item - GET /sn\_install\_base/integrations/installbaseitems/\{id\}/maintenanceplans

Returns the maintenance plans associated with a specified install base item record.

### URL format

Versioned URL: `/api/sn_install_base/{api_version}/integrations/installbaseitems/{id}/maintenanceplans`

Default URL: `/api/sn_install_base/integrations/installbaseitems/{id}/maintenanceplans`

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

</td><td id="integrate-id-entry">

Sys\_id of the install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

field name-value pairs

</td><td>

Field-value pairs to use to filter the maintenance plan records. By default this references the fields in the Maintenance Plan \[sm\_maint\_plan\] table. If you specify a different table in **sys\_class\_name**, then specify the fields in that table.You can pass one or more field-value pairs to filter the return results.

For example, to return only records that are active, pass the follow: `&active=true`.

Data type: String

Default: All fields

</td></tr><tr><td>

sys\_class\_name

</td><td>

If using an extended maintenance plans table \(not maintenanceplans\), the name of the extended table to query.Data type: String

Default: maintenanceplans

</td></tr><tr><td>

sysparm\_limit

</td><td id="sysparm_limit-entry-RESTAPI">

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. This limit is applied before ACL evaluation. If no records return, including records you have access to, rearrange the record order so records you have access to return first.

**Note:** Unusually large **sysparm\_limit** values can impact system performance.

Data type: Number

Default: 10000

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-entry-RESTAPI">

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

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
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="error-integration-entry">

Details about the error that occurred when trying to process the request.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td id="error_detail-integration-entry">

Additional details about the associated error.Data type: String

</td></tr><tr><td>

error.message

</td><td id="error_message-integration-entry">

Error message that describes the problem that occurred when trying to execute the request.Data type: String

</td></tr><tr><td>

has\_more

</td><td id="has_more-integration-entry">

Flag that indicates whether there are more records in the table to return.Possible values:

-   true: More records to return.
-   false: No more records to return.

Data type: Boolean string

</td></tr><tr><td>

maintenanceplans

</td><td>

List of the maintenance plans associated with the specified install base item record.Data type: Array of Object

```
"maintenanceplans": [
  {
    "active": "String",
    "apply_to_new": "String",
    "allow_future_wo": "String",
    "maintenance_override_policy": {Object},
    "model": "String",
    "name": "String",
    "number": "String",
    "propagation_flag": "String",
    "sys_class_name": "String",
    "sys_id": "String",
    "table": "String",
    "type": {Object}
  }
]
```

</td></tr><tr><td>

maintenanceplans.​​active

</td><td>

Flag that indicates whether the maintenance plan is active.Possible values:

-   true: Maintenance plan is active.
-   false: Maintenance plan is inactive.

Data type: String

</td></tr><tr><td>

maintenanceplans.​​apply\_to\_new

</td><td>

Flag that indicates whether the schedules defined for this maintenance plan are applied to all records that have been added to the specified table since the last time the plan was executed, and that they meet the conditions entered in the Filter condition. Possible values:

-   true: Applied to all new record.
-   false:Not applied to all new records.

Data type: String

</td></tr><tr><td>

maintenanceplans.​​allow\_future\_wo

</td><td>

Flag that indicates whether work orders can be associated with the maintenance plan.Possible values:

-   true: New work orders can be associated.
-   false: No new work orders can be associated.

Data type: String

</td></tr><tr><td>

maintenanceplans.​​maintenance\_override\_policy

</td><td>

Details about the maintenance override policy for the maintenance plan.Data type: Object

```
"maintenance_override_policy": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

maintenanceplans.​​maintenance\_override\_policy.​​display\_value

</td><td>

Text string describing the override policy. Use this value to display the override policy in the UI.Data type: String

</td></tr><tr><td>

maintenanceplans.​​maintenance\_override\_policy.​​value

</td><td>

Internal value of the override policy.Data type: String

</td></tr><tr><td>

maintenanceplans.​​model

</td><td>

Sys\_id of the model record associated with the maintenance plan.Data type: String

</td></tr><tr><td>

maintenanceplans.​​number

</td><td>

Maintenance plan number.Data type: String

</td></tr><tr><td>

maintenanceplans.​​propagation\_flag

</td><td>

Flag that indicates whether the maintenance plan can be propagated.Possible values:

-   true: Maintenance plan can be propagated.
-   false: Maintenance plan can't be propagated.

Data type: String

</td></tr><tr><td>

maintenanceplans.​​sys\_class\_name

</td><td>

Table containing the maintenance plan record.Data type: String

</td></tr><tr><td>

maintenanceplans.​​sys\_id

</td><td>

Sys\_id of the associated maintenance plan.Data type: String

</td></tr><tr><td>

maintenanceplans.​​table

</td><td>

Table that contains the associated install base time record.Data type: String

</td></tr><tr><td>

maintenanceplans.​​type

</td><td>

Details about the type of maintenance plan.Data type: Object

```
"type": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

maintenanceplans.​​type.​​display\_value

</td><td>

Text string describing the maintenance plan type. Use this value to display the type in the UI.Data type: String

</td></tr><tr><td>

maintenanceplans.​​type.​​value

</td><td>

Internal value of the maintenance plan type.Data type: String

</td></tr><tr><td>

status

</td><td id="status-integration-entry">

Status of the endpoint call.Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td id="sysparm_limit-integration-entry">

Number of records that were returned. If this value isn't specified in the original request, it uses the default value.Data type: Number

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-integration-entry">

Offset \(starting point\) in the associated table from which records were evaluated and retrieved.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/installbaseitems/167e96f053961910539dddeeff7b1298/maintenanceplans" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "sysparm_offset": 0,
    "sysparm_limit": 1,
    "has_more": true,
    "maintenanceplans": [
      {
        "propagation_flag": "false",
        "active": "true",
        "type": {
          "value": "install_base",
          "display_value": "Install base"
        },
        "maintenance_override_policy": {
          "value": "do_nothing",
          "display_value": "Leave alone"
        },
        "sys_class_name": "wm_planned_work_plan",
        "allow_future_wo": "true",
        "sys_id": "0b809d70877561105d0055373cbb357f",
        "number": "WP0001026",
        "name": "Plan 10",
        "model": "8583ce8237732000158bbfc8bcbe5dd9",
        "apply_to_new": "true",
        "table": "sn_install_base_item"
      }
    ],
    "status": "SUCCESS"
  }
}
```

## Install Base Item - GET /sn\_install\_base/integrations/installbaseitems/\{id\}/relatedparties

Returns the related parties associated with a specified install base item record.

### URL format

Versioned URL: `/api/sn_install_base/{api_version}/integrations/installbaseitems/{id}/relatedparties`

Default URL: `/api/sn_install_base/integrations/installbaseitems/{id}/relatedparties`

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

</td><td id="integrate-id-entry">

Sys\_id of the install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

field name-value pairs

</td><td>

Field-value pairs to use to filter the related parties records. By default this references the fields in the Related Parties \[sn\_install\_base\_related\_party\] table. If you specify a different table in **sys\_class\_name**, then specify the fields in that table.You can pass one or more field-value pairs to filter the return results.

For example, if you wanted to filter on a specific account and responsible party, pass the sys\_ids of the two records: `&account=86837a386f0331003b3c498f5d3ee4ca&responsibility=c009bbedb3730010700b4d43c6a8dcef`.

Data type: String

Default: All fields

</td></tr><tr><td>

sys\_class\_name

</td><td>

If using an extended related parties table \(not sn\_install\_base\_related\_party\), the name of the extended table to query.Data type: String

Default: sn\_install\_base\_related\_party

</td></tr><tr><td>

sysparm\_limit

</td><td id="sysparm_limit-entry-RESTAPI">

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. This limit is applied before ACL evaluation. If no records return, including records you have access to, rearrange the record order so records you have access to return first.

**Note:** Unusually large **sysparm\_limit** values can impact system performance.

Data type: Number

Default: 10000

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-entry-RESTAPI">

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

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
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="id_gls_y2f_zwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Details about the error that occurred when trying to process the request.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional details about the associated error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that describes the problem that occurred when trying to execute the request.Data type: String

</td></tr><tr><td>

has\_more

</td><td>

Flag that indicates whether there are more records in the table to return.Possible values:

-   true: More records to return.
-   false: No more records to return.

Data type: Boolean string

</td></tr><tr><td>

relatedparties

</td><td id="related_parties-integration-entry">

List of the related parties associated with the specified install base item record.Data type: Array of Objects

```
"relatedparties": [
  {
    "account": {Object},
    "consumer": {Object},
    "contact": {Object},
    "install_base_item": {Object},
    "responsibility": {Object},
    "service_organization": {Object},
    "sys_class_name": "String",
    "sys_id": "String",
    "type": {Object},
    "user": {Object}
  }
]
```

</td></tr><tr><td>

relatedparties.account

</td><td id="account-rp-integration-entry">

Details about the account associated with the related parties record.Data type: Object

```
account": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

relatedparties.account.display\_value

</td><td id="account_display_value-rp-integration-entry">

Text name of the account associated with the related parties record. Use this value to display the account name in the UI.Data type: String

</td></tr><tr><td>

relatedparties.account.sys\_id

</td><td id="account_sys_id-rp-integration-entry">

Sys\_id of the account record associated with the related parties record.Data type: String

</td></tr><tr id="consumer-rp-integration-row"><td>

relatedparties.consumer

</td><td id="consumer-rp-integration-entry">

Details about the consumer associated with the related parties record.Data type: Object

```
"consumer": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="consumer_display_value-rp-integration-row"><td>

relatedparties.consumer.display\_value

</td><td id="consumer_display_value-rp-integration-entry">

Text name of the consumer associated with the related parties record. Use this value to display the consumer name in the UI.Data type: String

</td></tr><tr id="consumer_sys_id-rp-integration-row"><td>

relatedparties.consumer.sys\_id

</td><td id="consumer_sys_id-rp-integration-entry">

Sys\_id of the consumer record associated with the related parties record.Data type: String

</td></tr><tr><td>

relatedparties.contact

</td><td id="contact-rp-integration-entry">

Details about the account contact responsible for the related parties record.Data type: Object

```
"contact": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

relatedparties.contact.display\_value

</td><td id="contact_display_value-rp-integration-entry">

Text name of the contact associated with the related parties record. Use this value to display the contact name in the UI.Data type: String

</td></tr><tr id="contact_sys_id-rp-integration-row"><td>

relatedparties.contact.sys\_id

</td><td id="contact_sys_id-rp-integration-entry">

Sys\_id of the contact record associated with the related parties record.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

relatedparties.install\_base\_item

</td><td id="install_base_item-rp-integration-entry">

Details about the install base item associated with the related parties record.Data type: Object

```
"install_base_item": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

relatedparties.install\_base\_item.display\_value

</td><td id="install_base_item_display_value-rp-integration-entry">

Text name of the install base item associated with the related parties record. Use this value to display the install base item name in the UI.Data type: String

</td></tr><tr><td>

relatedparties.install\_base\_item.sys\_id

</td><td id="install_base_item_sys_id-rp-integration-entry">

Sys\_id of the install base item record associated with the related parties record.Data type: String

</td></tr><tr><td>

relatedparties.responsibility

</td><td id="responsibility-rp-integration-entry">

Details about the access level for the install base information. Data type: Object

```
"responsibility": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

relatedparties.responsibility.display\_value

</td><td id="responsibility_display_value-rp-integration-entry">

Text display value for the access level for the install base information.Data type: String

</td></tr><tr><td>

relatedparties.responsibility.sys\_id

</td><td id="responsibility_sys_id-rp-integration-entry">

Sys\_id of the associated responsibility record. This record defines the access level for the install base information.This parameter is only valid if the **related\_party** field is also specified. If specified, it only returns the install base items that match both the **related\_party** and **responsibility** parameters.

For additional information, see [Configure related parties for Items Received](https://www.servicenow.com/docs/access?context=psds-add-related-parties-to-record&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)

Data type: String

Table: Responsibility Definition \[sn\_customerservice\_responsibility\_def\]

</td></tr><tr><td>

relatedparties.service\_organization

</td><td>

Details about the service organization associated with the related parties record.Data type: Object

```
"service_organization": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

relatedparties.service\_organization.display\_value

</td><td>

Text name of the service organization associated with the related parties record. Use this value to display the service organization name in the UI.Data type: String

</td></tr><tr><td>

relatedparties.service\_organization.sys\_id

</td><td>

Sys\_id of the service organization record associated with the related parties record.Data type: String

Table: Service Organization \[sn\_customer\_service\_organization\]

</td></tr><tr><td>

relatedparties.sys\_class\_name

</td><td id="sys_class_name-rp-integration-entry">

Table containing the related parties record.Data type: String

Default: sn\_install\_base\_related\_party

</td></tr><tr><td>

relatedparties.sys\_id

</td><td id="sys_id-rp-integration-entry">

Sys\_id of the associated related parties record.Data type: String

</td></tr><tr><td>

relatedparties.type

</td><td id="type-rp-integration-entry">

Details about the type of contact associated with the related parties record.Data type: Object

```
"type": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

relatedparties.type.display\_value

</td><td id="type_display_value-rp-integration-entry">

Text name of the type of contact associated with the related parties record. Use this value to display the type of contact in the UI. For additional information, see [Create related party configurations](https://www.servicenow.com/docs/access?context=adding-related-party-config-to-case&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).Possible types:

-   Authorized Account
-   Authorized Consumer
-   Authorized Contact
-   Authorized Contributor
-   Authorized Member
-   Authorized Service Organization
-   Listed Account
-   Listed Consumer
-   Listed Contact
-   Listed Contributor
-   Listed Member
-   Listed Service Organization

Data type: String

</td></tr><tr><td>

relatedparties.type.sys\_id

</td><td id="type_sys_id-rp-integration-entry">

Sys\_id of the type record associated with the related parties record.Data type: String

</td></tr><tr id="user-rp-integration-row"><td>

relatedparties.user

</td><td id="user-rp-integration-entry">

Details about the user associated with the related parties record.Data type: Object

```
"user": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="user_display_value-rp-integration-row"><td>

relatedparties.user.display\_value

</td><td id="user_display_value-rp-integration-entry">

Text name of the user associated with the related parties record. Use this value to display the user name in the UI.Data type: String

</td></tr><tr id="user_sys_id-rp-integration-row"><td>

relatedparties.user.sys\_id

</td><td id="user_sys_id-rp-integration-entry">

Sys\_id of the user record associated with the related parties record.

Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

status

</td><td id="status-integration-entry">

Status of the endpoint call.Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td id="sysparm_limit-integration-entry">

Number of records that were returned. If this value isn't specified in the original request, it uses the default value.Data type: Number

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-integration-entry">

Offset \(starting point\) in the associated table from which records were evaluated and retrieved.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/installbaseitems/42746a3b876121100b6afc86dabb3597/relatedparties" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Return results:

```

  "result": {
    "sysparm_offset": 0,
    "sysparm_limit": 10,
    "has_more": false,
    "relatedparties": [
      {
        "type": {
          "sys_id": "68ec8b2965e99110f87764df53db779f",
          "display_value": "Authorized Contact"
        },
        "install_base_item": {
          "sys_id": "42746a3b876121100b6afc86dabb3597",
          "display_value": "KX Series - KX5000"
        },
        "sys_class_name": "sn_install_base_related_party",
        "sys_id": "8547774087f561100b6afc86dabb351a",
        "responsibility": {
          "sys_id": "c009bbedb3730010700b4d43c6a8dcef",
          "display_value": "Authorized Representative"
        },
        "contact": {
          "sys_id": "dc0185d94f341200025ba3618110c77c",
          "display_value": "Cindy Contact"
        },
        "account": {
          "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
          "display_value": "Boxeo"
        }
      }
    ],
    "status": "SUCCESS"
  }
}

```

## Install Base Item - GET /sn\_install\_base/integrations/installbaseitems/\{id\}/soldproducts

Returns the sold products records associated with a specified install base item record.

### URL format

Versioned URL: `/api/sn_install_base/{api_version}/integrations/installbaseitems/{id}/soldproducts`

Default URL: `/api/sn_install_base/integrations/installbaseitems/{id}/soldproducts`

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

</td><td id="integrate-id-entry">

Sys\_id of the install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

field name-value pairs

</td><td>

Field-value pairs to use to filter the related parties records. By default this references the fields in the Sold Products \[sn\_install\_base\_sold\_product\] table. If you specify a different table in **sys\_class\_name**, specify the fields in that table.You can pass one or more field-value pairs to filter the return results.

For example, if you wanted to filter on the products sold to a specific account, pass something similar to the following, where the passed value is the sys\_id of the account: `&account=86837a386f0331003b3c498f5d3ee4ca`.

Data type: String

Default: All fields

</td></tr><tr><td>

sys\_class\_name

</td><td>

If using an extended sold products table \(not sn\_install\_base\_sold\_product\), the name of the extended table to query.Data type: String

Default: sn\_install\_base\_sold\_product

</td></tr><tr><td>

sysparm\_limit

</td><td id="sysparm_limit-entry-RESTAPI">

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. This limit is applied before ACL evaluation. If no records return, including records you have access to, rearrange the record order so records you have access to return first.

**Note:** Unusually large **sysparm\_limit** values can impact system performance.

Data type: Number

Default: 10000

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-entry-RESTAPI">

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

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
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="error-integration-entry">

Details about the error that occurred when trying to process the request.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td id="error_detail-integration-entry">

Additional details about the associated error.Data type: String

</td></tr><tr><td>

error.message

</td><td id="error_message-integration-entry">

Error message that describes the problem that occurred when trying to execute the request.Data type: String

</td></tr><tr><td>

has\_more

</td><td id="has_more-integration-entry">

Flag that indicates whether there are more records in the table to return.Possible values:

-   true: More records to return.
-   false: No more records to return.

Data type: Boolean string

</td></tr><tr><td>

soldproducts

</td><td>

List of the sold products associated with the specified install base item record.Data type: Array of Objects

```
"soldproducts":[
  {
    "account": {Object},
    "contact": {Object},
    "name": "String",
    "number": "String",
    "product": {Object},
    "sys_class_name": "String",
    "sys_id": "String",
    "state": {Object}
  }
]
```

</td></tr><tr><td>

soldproducts.account

</td><td>

Details about the account associated with the product record.Data type: Object

```
account": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

soldproducts.account.display\_value

</td><td>

Text name of the account associated with the product record. Use this value to display the account name in the UI.Data type: String

</td></tr><tr><td>

soldproducts.account.sys\_id

</td><td>

Sys\_id of the account record associated with the product record.Data type: String

</td></tr><tr><td>

soldproducts.contact

</td><td>

Details about the account contact responsible for the product.Data type: Object

```
"contact": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

soldproducts.contact.display\_value

</td><td>

Text name of the contact associated with the product. Use this value to display the contact name in the UI.Data type: String

</td></tr><tr><td>

soldproducts.contact.sys\_id

</td><td>

Sys\_id of the contact record associated with the product record.Data type: String

</td></tr><tr><td>

soldproducts.name

</td><td>

Name of the product.Data type: String

</td></tr><tr><td>

soldproducts.number

</td><td>

Product number.Data type: String

</td></tr><tr><td>

soldproducts.sys\_class\_name

</td><td>

Table containing the product record.Data type: String

</td></tr><tr><td>

soldproducts.sys\_id

</td><td>

Sys\_id of the associated product.Data type: String

</td></tr><tr><td>

soldproducts.state

</td><td>

Details about the current state of the product.Data type: Object

```
"state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

soldproducts.state.display\_value

</td><td>

Text string of the current state of the product. Use this value to display the state in the UI.Data type: String

</td></tr><tr><td>

soldproducts.state.value

</td><td>

Internal value of the state of the product.Data type: String

</td></tr><tr><td>

status

</td><td id="status-integration-entry">

Status of the endpoint call.Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td id="sysparm_limit-integration-entry">

Number of records that were returned. If this value isn't specified in the original request, it uses the default value.Data type: Number

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-integration-entry">

Offset \(starting point\) in the associated table from which records were evaluated and retrieved.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/installbaseitems/f77c7542b7343300ece839a6ee11a991/soldproducts?sysparm_limit=1" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "sysparm_offset": 0,
    "sysparm_limit": 1,
    "has_more": true,
    "soldproducts": [
      {
        "product": {
          "sys_id": "a9a2d0c3c6112276010db16c5ddd3461",
          "display_value": "Lenovo ThinkStation S20"
        },
        "sys_class_name": "sn_install_base_sold_product",
        "number": "SLPRD0001008",
        "sys_id": "17a3a7128729a1105d0055373cbb35fb",
        "contact": {
          "sys_id": "ddce70866f9331003b3c498f5d3ee417",
          "display_value": "George Warren"
        },
        "name": "SP B2B",
        "state": {
          "value": "active",
          "display_value": "Active"
        },
        "account": {
          "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
          "display_value": "Boxeo"
        }
      }
    ],
    "status": "SUCCESS"
  }
}
```

## Install Base Item - GET /sn\_install\_base/integrations/installbaseitems/\{id\}/workorders

Returns the work orders associated with a specified install base item record.

### URL format

Versioned URL: `/api/sn_install_base/{api_version}/integrations/installbaseitems/{id}/workorders`

Default URL: `/api/sn_install_base/integrations/installbaseitems/{id}/workorders`

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

</td><td id="integrate-id-entry">

Sys\_id of the install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

field name-value pairs

</td><td>

Field-value pairs to use to filter the related parties records. By default this references the fields in the Sold Products \[sn\_install\_base\_sold\_product\] table. If you specify a different table in **sys\_class\_name**, then specify the fields in that table.You can pass one or more field-value pairs to filter the return results.

For example, if you wanted to filter on the products sold to a specific account, pass something similar to the following where the passed value is the sys\_id of the account: `&account=86837a386f0331003b3c498f5d3ee4ca`.

Data type: String

Default: All fields

</td></tr><tr><td>

sys\_class\_name

</td><td>

If using an extended sold products table \(not sn\_install\_base\_sold\_product\), the name of the extended table to query.Data type: String

Default: sn\_install\_base\_sold\_product

</td></tr><tr><td>

sysparm\_limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. **Note:** Unusually large **sysparm\_limit** values can impact system performance.

Data type: Number

Default: 10

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-entry-RESTAPI">

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

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
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="error-integration-entry">

Details about the error that occurred when trying to process the request.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td id="error_detail-integration-entry">

Additional details about the associated error.Data type: String

</td></tr><tr><td>

error.message

</td><td id="error_message-integration-entry">

Error message that describes the problem that occurred when trying to execute the request.Data type: String

</td></tr><tr><td>

has\_more

</td><td id="has_more-integration-entry">

Flag that indicates whether there are more records in the table to return.Possible values:

-   true: More records to return.
-   false: No more records to return.

Data type: Boolean string

</td></tr><tr><td>

status

</td><td id="status-integration-entry">

Status of the endpoint call.Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td id="sysparm_limit-integration-entry">

Number of records that were returned. If this value isn't specified in the original request, it uses the default value.Data type: Number

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-integration-entry">

Offset \(starting point\) in the associated table from which records were evaluated and retrieved.Data type: String

</td></tr><tr><td>

workorders

</td><td>

List of the work orders associated with the specified install base item record.Data type: Array of Objects

```
"workorders":[
  {
    "active": "String",
    "approval": {Object},
    "billable": "String",
    "escalation": "String",
    "has_appointment": "String",
    "hierarchical_variables": "String",
    "impact": "String",
    "install_base_item": {Object},
    "is_catalog": "String",
    "knowledge": "String",
    "location": {Object},
    "made_sla": "String",
    "needs_attention": "String",
    "number": "String",
    "opened_at": {Object},
    "opened_by": {Object},
    "opened_for": {Object},
    "priority": "String",
    "reassignment_count": "String",
    "reschedule_maintenance_if_canceled": "String",
    "short_description": "String",
    "sla_suspended": "String",
    "state": "String",
    "sys_class_name": "String",
    "sys_domain_path": "String"
    "sys_id": "String",
    "task_created": "String",
    "task_effective_number": "String",
    "template_workflow_invoked": "String",
    "upon_approval": {Object},
    "upon_reject": {Object},
    "urgency": "String"
  }
]
```

</td></tr><tr><td>

workorders.active

</td><td>

Flag that indicates whether the work order is active.Possible values:

-   true: Work order is active.
-   false: Work order is inactive.

Data type: Boolean string

</td></tr><tr><td>

workorders.approval

</td><td>

Details about the current approval process for the work order.Data type: Object

```
"approval": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

workorders.​approval.display\_value

</td><td>

Text string of the current state of the approval process. Use this value to display the approval state in the UI.Data type: String

</td></tr><tr><td>

workorders.​approval.value

</td><td>

Internal value of the state of the approval process.Data type: String

</td></tr><tr><td>

workorders.​billable

</td><td>

Flag that indicates whether the work order is billable.Possible values:

-   true: Work order is billable.
-   false: Work order isn't billable

Data type: Boolean string

</td></tr><tr><td>

workorders.​escalation

</td><td>

Level of escalation of the work order.Data type: String

</td></tr><tr><td>

workorders.​has\_appointment

</td><td>

Flag that indicates whether the work order has a scheduled appointment.Possible values:

-   true: Work order has an appointment.
-   false: Work order doesn't have an appointment.

Data type: Boolean string

</td></tr><tr><td>

workorders.​install\_base\_item

</td><td>

Details about the install base item associated with the work order record.Data type: Object

```
"install_base_item": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

workorders.​install\_base\_item.​display\_value

</td><td>

Text name of the install base item associated with the work order record. Use this value to display the install base item name in the UI.Data type: String

</td></tr><tr><td>

workorders.​install\_base\_item.sys\_id

</td><td>

Sys\_id of the install base item record associated with the work order record.Data type: String

</td></tr><tr><td>

workorders.​is\_catalog

</td><td>

Flag that indicates whether is part of a catalog.Possible values:

-   true: Work order is part of a catalog.
-   false: Work order isn't part of a catalog.

Data type: Boolean string

</td></tr><tr><td>

workorders.knowledge

</td><td>

Flag that indicates if there's a knowledge base article available for the specified work order issue.Possible values:

-   true: Knowledge base article is available for this issue.
-   false: Knowledge base article isn't available for this issue.

Data type: Boolean string

</td></tr><tr><td>

workorders.location

</td><td>

Details about the location of the item that needs to be worked on.Data type: Object

```
"location": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

workorders.​location.​display\_value

</td><td>

Text name of the location of the item to be worked on. Use this value to display the location in the UI.Data type: String

</td></tr><tr><td>

workorders.​location.​sys\_id

</td><td>

Sys\_id of the location record associated with the work order record.Data type: String

</td></tr><tr><td>

workorders.​made\_sla

</td><td>

Flag that indicates whether the work associated with the work order met the associated Service Level Agreement \(SLA\).Possible values:

-   true: SLA was met.
-   false: SLA wasn't met.

Data type: Boolean string

</td></tr><tr><td>

workorders.​needs\_attention

</td><td>

Flag that indicates whether this work order needs attention.Possible values:

-   true: Work order needs attention.
-   false: Work order doesn't need attention.

Data type: Boolean string

</td></tr><tr><td>

workorders.​number

</td><td>

Unique number used to identify the work order.Data type: String

</td></tr><tr><td>

workorders.​opened\_at

</td><td>

Details about when the work order was opened.Data type: Object

```
"opened_at": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

workorders.​opened\_at.​display\_value

</td><td>

Date and time that the work order was opened. Use this value to display the value in the UI.Data type: String

</td></tr><tr><td>

workorders.​opened\_at.​value

</td><td>

Date and time that the work order was opened.Data type: String

</td></tr><tr><td>

workorders.​opened\_by

</td><td>

Details about the person that opened the work order.Data type: Object

```
"opened_by": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

workorders.​opened\_by.​display\_value

</td><td>

Text name of the person that opened the work order. Use this value to display this name in the UI.Data type: String

</td></tr><tr><td>

workorders.​opened\_by.​sys\_id

</td><td>

Sys\_id of the user record of the person that opened the work order. Data type: String

</td></tr><tr><td>

workorders.opened\_for

</td><td>

Details about the person that the work order was opened for if different than the **opened\_by** person.Data type: Object

```
"opened_for": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

workorders.​opened\_for.​display\_value

</td><td>

Text name of the person that the work order was opened for. Use this value to display this name in the UI.Data type: String

</td></tr><tr><td>

workorders.​opened\_for.​sys\_id

</td><td>

Sys\_id of the user record of the person that the work order was opened for. Data type: String

</td></tr><tr><td>

workorders.priority

</td><td>

Priority of the work order.Data type: String

</td></tr><tr><td>

workorders.​reassignment\_count

</td><td>

Number of times that the work order was reassigned to a person that is responsible for moving the work order forward.Data type: String

</td></tr><tr><td>

workorders.​reschedule\_maintenance\_if\_canceled

</td><td>

Flag that indicates whether the work should be rescheduled if the associated work order is canceled.Possible values:

-   true: Reschedule the work.
-   false: Check before rescheduling the work.

Data type: Boolean string

</td></tr><tr><td>

workorders.​short\_description

</td><td>

Brief text that describes the work associated with the work order.Data type: String

</td></tr><tr><td>

workorders.​sla\_suspended

</td><td>

Flag that indicates whether the SLA associated with the work order has been suspended.Valid values:

-   true: SLA has been suspended.
-   false: SLA hasn't been suspended.

Data type: Boolean string

</td></tr><tr><td>

workorders.state

</td><td>

Current state of the work order.Data type: String

</td></tr><tr><td>

workorders.​sys\_class\_name

</td><td>

Table containing the work order record.Data type: String

</td></tr><tr><td>

workorders.​sys\_domain\_path

</td><td>

Domain path.Data type: String

</td></tr><tr><td>

workorders.sys\_id

</td><td>

Sys\_id of the associated work order record.Data type: String

</td></tr><tr><td>

workorders.​task\_created

</td><td>

Flag that indicates whether a task has been created for this work order.Possible values:

-   true: Task has been created for this work order.
-   false: Task hasn't been created for this work order.

Data type: Boolean string

</td></tr><tr><td>

workorders.​task\_effective\_number

</td><td>

Unique number used to identify the work order.Data type: String

</td></tr><tr><td>

workorders.​template\_workflow\_invoked

</td><td>

Flag that indicates whether the associated workflow has been invoked for this work order.Possible values:

-   true: Workflow has been invoked.
-   false: Worflow hasn't been invoked.

Data type: Boolean string

</td></tr><tr><td>

workorders.​upon\_approval

</td><td>

Details about the next action to take if the work order is approved.Data type: Object

```
"upon_approval": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

workorders.​upon\_approval.​display\_value

</td><td>

Text string of the action to take if the work order is approved. Use this value to display this information in the UI.Data type: String

</td></tr><tr><td>

workorders.​upon\_approval.​value

</td><td>

Action to take if the work order is approved.Possible values:

-   do\_nothing
-   proceed

Data type: String

</td></tr><tr><td>

workorders.​upon\_reject

</td><td>

Details about the next action to take if the work order is rejected.Data type: Object

```
"upon_reject": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

workorders.​upon\_reject.​display\_value

</td><td>

Text string of the action to take if the work order is rejected. Use this value to display this information in the UI.Data type: String

</td></tr><tr><td>

workorders.​upon\_reject.​value

</td><td>

Action to take if the work order is rejected.Possible values:

-   cancel
-   goto

Data type: String

</td></tr><tr><td>

workorders.urgency

</td><td>

Urgency of the work order.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/installbaseitems/f77c7542b7343300ece839a6ee11a991/workorders?sysparm_limit=1" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "sysparm_offset": 0,
    "sysparm_limit": 10,
    "has_more": false,
    "workorders": [
      {
        "upon_reject": {
          "value": "cancel",
          "display_value": "Cancel all future Tasks"
        },
        "number": "WO0010372",
        "state": "1",
        "template_workflow_invoked": "false",
        "knowledge": "false",
        "impact": "3",
        "active": "true",
        "priority": "4",
        "sys_domain_path": "/",
        "sla_suspended": "false",
        "needs_attention": "false",
        "short_description": "Test WO1",
        "sys_class_name": "wm_order",
        "reschedule_maintenance_if_canceled": "true",
        "reassignment_count": "0",
        "hierarchical_variables": "variable_pool",
        "opened_for": {
          "sys_id": "85453c616fc331003b3c498f5d3ee4fa",
          "display_value": "Jodi Seals"
        },
        "install_base_item": {
          "sys_id": "42746a3b876121100b6afc86dabb3597",
          "display_value": "KX Series - KX5000"
        },
        "has_appointment": "false",
        "escalation": "0",
        "upon_approval": {
          "value": "proceed",
          "display_value": "Proceed to Next Task"
        },
        "spam": "false",
        "made_sla": "true",
        "is_catalog": "false",
        "task_effective_number": "WO0010372",
        "opened_by": {
          "sys_id": "85453c616fc331003b3c498f5d3ee4fa",
          "display_value": "Jodi Seals"
        },
        "opened_at": {
          "value": "2023-03-20 13:33:22",
          "display_value": "2023-03-20 06:33:22"
        },
        "task_created": "false",
        "sys_id": "19761cc087b521100b6afc86dabb352f",
        "urgency": "3",
        "approval": {
          "value": "not requested",
          "display_value": "Not Yet Requested"
        },
        "billable": "false",
        "location": {
          "sys_id": "1cd145bc23070110766713d1d7bf654f",
          "display_value": "2866 Stevens Creek Blvd,Santa Clara,CA"
        }
      }
    ],
    "status": "SUCCESS"
  }
}
```

## Install Base Item - PATCH /sn\_install\_base/integrations/installbaseitems/\{id\}

Updates a specified install base item record with specified field values.

### URL format

Versioned URL: `/api/sn_install_base/{api_version}/integrations/installbaseitems/{id}`

Default URL: `/api/sn_install_base/integrations/installbaseitems/{id}`

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

<table id="id_x5m_53g_xwb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td id="account-request-integration-entry">

Required when creating an install base item for an account.Sys\_id of the account to associate with the install base item.

**Note:** If you pass the **account** parameter, you can't also pass the **consumer** parameter.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr><td>

active

</td><td id="active-request-integration-entry">

Flag that indicates whether the install base item is active.Valid values:

-   true, "true", or "0": Item is active.
-   false, "false", or "1": Item isn't active.

Data type: Boolean

Default: true

</td></tr><tr><td>

asset

</td><td id="asset-request-integration-entry">

Sys\_id of the asset associated with the install base item record.Data type: String

Table: Asset \[alm\_asset\]

</td></tr><tr><td>

child\_install\_base\_items

</td><td id="child_install_base_items-request-integration-entry">

List of the child install base items associated with this install base item.**Note:** The following child install base item fields can't be different from its parent:

-   account
-   consumer
-   contact
-   service organization

Data type: Array of Objects

```
"child_install_base_items": [
  {
    "name": "String",
    "product": "String"
  }
]
```

</td></tr><tr><td>

child\_install\_base\_items.name

</td><td id="child_install_base_items_name-request-integration-entry">

Name of the child install base item.Data type: String

</td></tr><tr><td>

child\_install\_base\_items.product

</td><td id="child_install_base_items_product-request-integration-entry">

Sys\_id of the associated child base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

configuration\_item

</td><td id="configuration_item-request-integration-entry">

Sys\_id of the configuration item associated with the install base item record.Data type: String

Table: Configuration Item \[cmdb\_ci\]

</td></tr><tr><td>

consumer

</td><td id="consumer-request-integration-entry">

Required when creating an install base item for a consumer.Sys\_id of the consumer associated with the install base item record.

**Note:** If you pass the **consumer** parameter, you can't also pass the **account** parameter. In addition, you can only associate a consumer with an install base item if the B2B2C plugin is installed on your instance.

Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

consumer\_profile

</td><td id="consumer_profile-request-integration-entry">

Sys\_id of the consumer profile associated with the install base item record.Data type: String

Table: Consumer Profile \[sn\_csm\_consumer\_profile\]

</td></tr><tr><td>

contact

</td><td id="contact-request-integration-entry">

Sys\_id of the account contact record that is primarily responsible for the install base item.

**Note:** Contacts can only be specified for account install base items.

Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

household

</td><td id="household-request-integration-entry">

Sys\_id of the household associated with the install base item record.**Note:** This field is only valid when the Customer Service Household \(com.snc.household\) plugin is installed.

Data type: String

Table: Household \[csm\_household\]

</td></tr><tr><td>

install\_date

</td><td id="install_date-request-integration-entry">

Date on which the install base item becomes active.Data type: String

Format: yyyy-MM-dd HH:mm:ss

</td></tr><tr><td>

location

</td><td id="location-request-integration-entry">

Sys\_id of the location of the associated product.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

name

</td><td id="name-request-integration-entry">

Name of the install base item.Data type: String

</td></tr><tr><td>

number

</td><td id="number-request-integration-entry">

Unique identifier for the install base item.Data type: String

Default: Automatically generated by the endpoint.

</td></tr><tr><td>

parent

</td><td id="parent-request-integration-entry">

Sys\_id of the parent record for this install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

product\_model

</td><td id="product-request-integration-entry">

Sys\_id of the product model associated with the install base item record.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr><td>

quantity

</td><td id="quantity-request-integration-entry">

Number of items installed.Data type: Integer

</td></tr><tr><td>

service\_context

</td><td id="service_context-request-integration-entry">

Sys\_id of the service that is associated to the underlying CI for calculating the impact severity from Event Management. For more information, see [Service health status for install base](https://www.servicenow.com/docs/access?context=service-health-pcso&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).**Note:** This field is only valid if the Proactive Customer Service Operations with Event Management plugin is installed.

Data type: String

</td></tr><tr><td>

service\_organization

</td><td id="service_organization-request-integration-entry">

Required when creating an install base item for a service organization.Sys\_id of the service organization record that is involved in providing service to the customer.

**Note:** If you pass this parameter, you shouldn't also pass the account, contact, or consumer parameters. The **service\_organization** parameter is only available when the Service Organization \(com.snc.service\_organization\) plugin is installed on your instance.

Data type: String

Table: Service Organization \[sn\_customer\_service\_organization\]

</td></tr><tr><td>

state

</td><td id="state-request-integration-entry">

Current state of the install base item.Valid values:

-   in\_use
-   inactive

Data type: String

</td></tr><tr><td>

status

</td><td id="status-request-integration-entry">

Status of the product.Valid values:

-   original
-   replacement

Data type: String

</td></tr><tr><td>

sys\_class\_name

</td><td>

Name of the extended install base table in which to update the install base item record.Data type: String

</td></tr><tr><td>

uninstall\_date

</td><td id="uninstall_date-request-integration-entry">

Date on which the install base becomes inactive.Data type: String

Format: yyyy-MM-dd HH:mm:ss

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
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="id_zk1_w5w_ywb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="error-integration-entry">

Details about the error that occurred when trying to process the request.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td id="error_detail-integration-entry">

Additional details about the associated error.Data type: String

</td></tr><tr><td>

error.message

</td><td id="error_message-integration-entry">

Error message that describes the problem that occurred when trying to execute the request.Data type: String

</td></tr><tr><td>

item

</td><td>

Details about the install base item that was updated.Data type: Object

```
"item": {
  "account": {Object},
  "active": Boolean,
  "name": "String",
  "number": "String",
  "state": {Object},
  "sys_class_name": {Object},
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.account

</td><td>

Details about the customer account associated with the install base item record.Data type: Object

```
"account": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.account.display\_value

</td><td>

Text name of the customer account associated with the install base item record. Use this value to display the customer account name in the UI.Data type: String

</td></tr><tr><td>

item.account.sys\_id

</td><td>

Sys\_id of the customer account record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.active

</td><td>

Flag that indicates whether the install base item is active.Possible values:

-   true: Install base item is active.
-   false: Install base item is inactive.

Data type: Boolean String

</td></tr><tr><td>

item.name

</td><td>

Name of the install base item.Data type: String

</td></tr><tr><td>

item.number

</td><td>

Unique ID of the install base item.Data type: String

</td></tr><tr><td>

item.state

</td><td>

Details about the current state of the install base item.Data type: Object

```
"state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

item.state.display\_value

</td><td>

Text string of the current state of the install base item. Use this value to display the state in the UI.Data type: String

</td></tr><tr><td>

item.state.value

</td><td>

Internal value of the state of the install base item.Data type: String

</td></tr><tr><td>

item.sys\_class\_name

</td><td>

Details about the table that contains the install base item.Data type: Object

```
"sys_class_name": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

item.sys\_class\_name.display\_value

</td><td>

Text string of the name of the table that contains the install base item. Use this value to display the table name in the UI.Data type: String

</td></tr><tr><td>

item.sys\_class\_name.value

</td><td>

Internal value of the table that contains the install base itemData type: String

</td></tr><tr><td>

item.sys\_id

</td><td>

Sys\_id of the install base item record. Located in the table specified in the **sys\_class\_name** parameter.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the endpoint call.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to update the name and active fields in the install base item record.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/installbaseitems/f77c7542b7343300ece839a6ee11a991" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"name\": \"KX Series - KX5001\",
  \"active\":true
}" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "status": "SUCCESS",
    "item": {
      "sys_class_name": {
        "value": "sn_install_base_item",
        "display_value": "Install Base Item"
      },
      "number": "IBITM0001001",
      "sys_id": "bc610d38cb76211050501ebfe8076d8b",
      "state": {
        "value": "inactive",
        "display_value": "Inactive"
      },
      "active": "false",
      "name": "NewTestIB",
      "account": {
        "sys_id": "8637a386f0331003b3c498f5d3ee4ca",
        "display_value": "Boxeo"
      }
    }
  }
}
      
}
```

## Install Base Item - PATCH /sn\_install\_base/integrations/installbaseitems/\{id\}/relatedparties/\{related\_party\_sys\_id\}

Updates the specified related party record, associated with a specified install base item, with the values in the request body.

If you need to modify the type of related party associated with an Install Base Item, you must remove the type-specific fields for the current related party type and replace them with the type-specific fields of the new related party type. For example, to change from a type of Authorized Account to Authorized Consumer, pass the following:

-   **type** = "Authorized Consumer"
-   **account** = ""
-   **consumer** = "&lt;sys\_id of consumer record&gt;"
-   **responsibility** = "&lt;sys\_id of responsibility of consumer&gt;"

### URL format

Versioned URL: `/api/sn_install_base/{api_version}/integrations/installbaseitems/{id}/relatedparties/{related_party_sys_id}`

Default URL: `/api/sn_install_base/integrations/installbaseitems/{id}/relatedparties/{related_party_sys_id}`

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

</td><td id="integrate-id-entry">

Sys\_id of the install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

related\_party\_sys\_id

</td><td id="related_party_sys_id-integrate-entry">

Sys\_id of the related party record.Data type: String

Table: Install Base Related Party \[sn\_install\_base\_related\_party\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="account-request-integration-row"><td>

account

</td><td id="account-request-integration-entry">

Required if the **type** parameter is one of the following: -   `Authorized Account`
-   `Authorized Contact`
-   `Listed Account`
-   `Listed Contact`

Sys\_id of the account to associate with the install base item.

**Note:** If you pass the **account** parameter, you can't also pass the **consumer** parameter.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr id="consumer-request-integration-row"><td>

consumer

</td><td id="consumer-request-integration-entry">

Required if the **type** parameter is `Authorized Consumer` or `Listed Consumer`. Sys\_id of the consumer associated with the install base item record.

**Note:** If you pass the **consumer** parameter, you can't also pass the **account** parameter. In addition, you can only associate a consumer with an install base item if the B2B2C plugin is installed on your instance.

Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

contact

</td><td>

Sys\_id of the contact record associated with the related parties record.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

responsibility

</td><td>

Sys\_id of the associated responsibility record. This record defines the access level for the install base information.This parameter is only valid if the **related\_party** field is also specified. If specified, it only returns the install base items that match both the **related\_party** and **responsibility** parameters.

For additional information, see [Configure related parties for Items Received](https://www.servicenow.com/docs/access?context=psds-add-related-parties-to-record&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)

Data type: String

Table: Responsibility Definition \[sn\_customerservice\_responsibility\_def\]

</td></tr><tr id="service_organization-request-integration-row"><td>

service\_organization

</td><td id="service_organization-request-integration-entry">

Required if the **type** parameter is one of the following: -   `Authorized Member`
-   `Authorized Service Organization`
-   `Listed Member`
-   `Listed Service Organization`

Sys\_id of the service organization record that is involved in providing service to the customer.

**Note:** If you pass this parameter, you shouldn't also pass the account, contact, or consumer parameters. The **service\_organization** parameter is only available when the Service Organization \(com.snc.service\_organization\) plugin is installed on your instance.

Data type: String

Table: Service Organization \[sn\_customer\_service\_organization\]

</td></tr><tr><td>

sys\_class\_name

</td><td>

Table containing the related parties record.Data type: String

Default: sn\_install\_base\_related\_party

</td></tr><tr><td>

type

</td><td>

Required. Sys\_id of the type of related party to create.Possible types:

-   Authorized Account
-   Authorized Consumer
-   Authorized Contact
-   Authorized Contributor
-   Authorized Member
-   Authorized Service Organization
-   Listed Account
-   Listed Consumer
-   Listed Contact
-   Listed Contributor
-   Listed Member
-   Listed Service Organization

Data type: String

Table: Related Party Configuration \[sn\_customerservice\_related\_party\_configuration\]

</td></tr><tr><td>

user

</td><td>

Required if the **type** parameter is one of the following related party types: -   `Authorized Contributor`
-   `Authorized Member`
-   `Listed Contributor`
-   `Listed Member`

Sys\_id of the user record associated with the related parties record.

Data type: String

Table: User \[sys\_user\]

For `Authorized Member` and `Listed Member`, this user must be associated with the specified **service\_organization** record.

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
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="id_gls_y2f_zwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="error-integration-entry">

Details about the error that occurred when trying to process the request.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td id="error_detail-integration-entry">

Additional details about the associated error.Data type: String

</td></tr><tr><td>

error.message

</td><td id="error_message-integration-entry">

Error message that describes the problem that occurred when trying to execute the request.Data type: String

</td></tr><tr><td>

item

</td><td>

Details about the related parties record.Data type: Array

```
"item": {
  "account": {Object},
  "consumer": {Object},
  "contact": {Object},
  "install_base_item": {Object},
  "responsibility": {Object},
  "service_organization": {Object},
  "sys_class_name": "String",
  "sys_id": "String",
  "type": {Object},
  "user": {Object}
}
```

</td></tr><tr><td>

item.account

</td><td>

Details about the account associated with the related parties record.Data type: Object

```
account": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.account.display\_value

</td><td>

Text name of the account associated with the related parties record. Use this value to display the account name in the UI.Data type: String

</td></tr><tr><td>

item.account.sys\_id

</td><td>

Sys\_id of the account record associated with the related parties record.Data type: String

</td></tr><tr><td>

item.consumer

</td><td>

Details about the consumer associated with the related parties record.Data type: Object

```
"consumer": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.consumer.display\_value

</td><td>

Text name of the consumer associated with the related parties record. Use this value to display the consumer name in the UI.Data type: String

</td></tr><tr><td>

item.consumer.sys\_id

</td><td>

Sys\_id of the consumer record associated with the related parties record.Data type: String

</td></tr><tr><td>

item.contact

</td><td>

Details about the account contact responsible for the related parties record.Data type: Object

```
"contact": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.contact.display\_value

</td><td>

Text name of the contact associated with the related parties record. Use this value to display the contact name in the UI.Data type: String

</td></tr><tr><td>

item.contact.sys\_id

</td><td>

Sys\_id of the contact record associated with the related parties record.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

item.install\_base\_item

</td><td>

Details about the install base item associated with the related parties record.Data type: Object

```
"install_base_item": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.install\_base\_item.display\_value

</td><td>

Text name of the install base item associated with the related parties record. Use this value to display the install base item name in the UI.Data type: String

</td></tr><tr><td>

item.install\_base\_item.sys\_id

</td><td>

Sys\_id of the install base item record associated with the related parties record.Data type: String

</td></tr><tr><td>

item.responsibility

</td><td>

Details about the access level for the install base information. Data type: Object

```
"responsibility": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.responsibility.display\_value

</td><td>

Text display value for the access level for the install base information.Data type: String

</td></tr><tr><td>

item.responsibility.sys\_id

</td><td>

Sys\_id of the associated responsibility record. This record defines the access level for the install base information.This parameter is only valid if the **related\_party** field is also specified. If specified, it only returns the install base items that match both the **related\_party** and **responsibility** parameters.

For additional information, see [Configure related parties for Items Received](https://www.servicenow.com/docs/access?context=psds-add-related-parties-to-record&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)

Data type: String

Table: Responsibility Definition \[sn\_customerservice\_responsibility\_def\]

</td></tr><tr><td>

item.sys\_class\_name

</td><td>

Table containing the related parties record.Data type: String

Default: sn\_install\_base\_related\_party

</td></tr><tr><td>

item.sys\_id

</td><td>

Sys\_id of the associated related parties record.Data type: String

</td></tr><tr><td>

item.type

</td><td>

Details about the type of contact associated with the related parties record.Data type: Object

```
"type": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.type.display\_value

</td><td>

Text name of the type of contact associated with the related parties record. Use this value to display the type of contact in the UI. For additional information, see [Create related party configurations](https://www.servicenow.com/docs/access?context=adding-related-party-config-to-case&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).Possible types:

-   Authorized Account
-   Authorized Consumer
-   Authorized Contact
-   Authorized Contributor
-   Authorized Member
-   Authorized Service Organization
-   Listed Account
-   Listed Consumer
-   Listed Contact
-   Listed Contributor
-   Listed Member
-   Listed Service Organization

Data type: String

</td></tr><tr><td>

item.type.sys\_id

</td><td>

Sys\_id of the type record associated with the related parties record.Data type: String

</td></tr><tr><td>

item.user

</td><td>

Details about the user associated with the related parties record.Data type: Object

```
"user": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.user.display\_value

</td><td>

Text name of the user associated with the related parties record. Use this value to display the user name in the UI.Data type: String

</td></tr><tr><td>

item.user.sys\_id

</td><td>

Sys\_id of the user record associated with the related parties record.

Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

status

</td><td id="status-integration-entry">

Status of the endpoint call.Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td id="sysparm_limit-integration-entry">

Number of records that were returned. If this value isn't specified in the original request, it uses the default value.Data type: Number

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-integration-entry">

Offset \(starting point\) in the associated table from which records were evaluated and retrieved.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint to update the contact record associated with the related party.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/relatedparties/f77c7542b7343300ece839a6ee11a991" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
\"contact\": \"dc0185d94f341200025ba3618110c77c\"
}" \
--user 'username':'password'
```

Return results:

```
{
"result":
  {
    "type": {
      "display_value":"Authorized Contact",
      "sys_id":"68ec8b2965e99110f87764df53db779f"
    },
    "install_base_item": {
      "display_value":"KX Series - KX5000",
      "sys_id":"f77c7542b7343300ece839a6ee11a991"
    },
    "sys_class_name":"sn_install_base_related_party",
    "sys_id":"4659539814ac6910f877ae314c1fb43a",
    "responsibility": {
      "display_value":"Authorized Representative",
      "sys_id":"c009bbedb3730010700b4d43c6a8dcef"
    },
    "contact": {
      "display_value":"Cindy Contact",
      "sys_id":"dc0185d94f341200025ba3618110c77c"
    },
    "account": {
      "display_value":"Boxeo",
      "value":"86837a386f0331003b3c498f5d3ee4ca"
    },
    "status":"SUCCESS",
  }
}
```

## Install Base Item - PATCH /sn\_install\_base/integrations/installbaseitems/\{id\}/uninstall

Uninstalls the specified install base item.

An uninstall consists of setting the **active** field to `false` and setting the **unistall\_date** field to a specified date. Empty if a date value isn't provided.

### URL format

Versioned URL: `/api/sn_install_base/{api_version}/integrations/installbaseitems/{id}/uninstall`

Default URL: `/api/sn_install_base/integrations/installbaseitems/{id}/uninstall`

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

</td><td id="integrate-id-entry">

Sys\_id of the install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

uninstall\_date

</td><td>

Date on which to uninstall the specified install base item. If not specified, it's uninstalled immediately.Data type: String

Format: yyyy-mm-dd hh:mm:ss

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
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="error-integration-entry">

Details about the error that occurred when trying to process the request.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td id="error_detail-integration-entry">

Additional details about the associated error.Data type: String

</td></tr><tr><td>

error.message

</td><td id="error_message-integration-entry">

Error message that describes the problem that occurred when trying to execute the request.Data type: String

</td></tr><tr><td>

item

</td><td>

Description of the uninstalled item.Data type: Object

```
"item": {
  "account": {Object},
  "active": "String",
  "asset": {Object},
  "configuration_item": {Object},
  "consumer": {Object},
  "consumer_profile": {Object},
  "contact": {Object},
  "health_status": {Object},
  "health_status_last_updated": "String",
  "household": {Object},
  "install_date": {Object},
  "location": {Object},
  "name": "String",
  "number": "String",
  "parent": {Object},
  "product": {Object},
  "service_context": {Object},
  "service_organization" {Object},
  "sys_class_name": "String",
  "sys_id": "String",
  "state": {Object},
  "status": {Object},
  "uninstall_date": "String"
}
```

</td></tr><tr id="account-integration-row"><td>

item.account

</td><td>

Details about the customer account associated with the install base item record.Data type: Object

```
"account": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="account_display_value-integration-row"><td>

item.account.display\_value

</td><td>

Text name of the customer account associated with the install base item record. Use this value to display the customer account name in the UI.Data type: String

</td></tr><tr id="account_sys_id-integration-row"><td>

item.account.sys\_id

</td><td>

Sys\_id of the customer account record associated with the install base item record.Data type: String

</td></tr><tr id="active-integration-row"><td>

item.active

</td><td>

Flag that indicates whether the install base item is active.Possible values:

-   true: Install base item is active.
-   false: Install base item is inactive.

Data type: Boolean String

</td></tr><tr><td>

item.asset

</td><td>

Details about the asset associated with the install base item record.Data type: Object

```
"asset": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.asset.display\_value

</td><td>

Text name of the asset associated with the install base item record. Use this value to display the asset name in the UI.Data type: String

</td></tr><tr><td>

item.asset.sys\_id

</td><td>

Sys\_id of the asset record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.child\_install\_base\_items

</td><td>

List of the child install base items associated with this install base item.**Note:** The following child install base item fields can't be different from its parent:

-   account
-   consumer
-   contact
-   service organization

Data type: Array of Objects

```
"child_install_base_items": [
  {
    "name": "String",
    "product": "String"
  }
]
```

</td></tr><tr><td>

item.child\_install\_base\_items.name

</td><td>

Name of the child install base item.Data type: String

</td></tr><tr><td>

item.child\_install\_base\_items.product

</td><td>

Sys\_id of the associated child base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

item.configuration\_item

</td><td>

Details about the configuration item associated with the install base item record.Data type: Object

```
"configuration_item": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.configuration\_display\_value

</td><td>

Text name of the configuration item associated with the install base item record. Use this value to display the configuration item name in the UI.Data type: String

</td></tr><tr><td>

item.configuration\_sys\_id

</td><td>

Sys\_id of the configuration item record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.consumer

</td><td>

Details about the consumer associated with the install base item record.**Note:** The consumer field is only available if the B2B2C plugin is installed.

Data type: Object

```
"consumer": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.consumer.display\_value

</td><td>

Text name of the consumer associated with the install base item record. Use this value to display the consumer name in the UI.Data type: String

</td></tr><tr><td>

item.consumer.sys\_id

</td><td>

Sys\_id of the consumer record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.consumer\_profile

</td><td>

Details about the consumer profile associated with the install base item record.**Note:** The consumer profile field is only available if the B2B2C plugin is installed.

Data type: Object

```
"consumer_profile": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.consumer\_profile.display\_value

</td><td>

Text name of the consumer profile associated with the install base item record. Use this value to display the consumer profile name in the UI.Data type: String

</td></tr><tr><td>

item.consumer\_profile.sys\_id

</td><td>

Sys\_id of the consumer profile record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.contact

</td><td>

Details about the account contact responsible for the install base item record.Data type: Object

```
"contact": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.contact.display\_value

</td><td>

Text name of the account contact associated with the install base item record. Use this value to display the account contact name in the UI.Data type: String

</td></tr><tr><td>

item.contact.sys\_id

</td><td>

Sys\_id of the account contact record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.health\_status

</td><td>

Details about the current health status of the install base item. Only returned if the Proactive Customer Service Operations \(com.snc.proactive\_cs\_itom\) plugin is installed.Data type: Object

```
"health_status": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

item.health\_status.display\_value

</td><td>

Text string of the current health status of the install base item. Use this value to display the health status in the UI.Data type: String

</td></tr><tr><td>

item.health\_status.value

</td><td>

Internal value of the health status of the install base item.Data type: String

</td></tr><tr><td>

item.health\_status\_last\_updated

</td><td>

Date and time when the health status was last updated for the install base item.Data type: String

</td></tr><tr><td>

item.household

</td><td>

Details about the household associated with the install base item record. Only returned if the Customer Service Household \(com.snc.household\) plugin is installed.Data type: Object

```
"household": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.household.display\_value

</td><td>

Text name of the household associated with the install base item record. Use this value to display the household name in the UI.Data type: String

</td></tr><tr><td>

item.household.sys\_id

</td><td>

Sys\_id of the household associated with the install base item record.Data type: String

</td></tr><tr><td>

item.install\_date

</td><td>

Details about the date when the install base item became active.Data type: Object

```
"install_date": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

item.install\_date.display\_value

</td><td>

Text install date. Use this value to display the install date in the UI.Data type: String

</td></tr><tr><td>

item.install\_date.value

</td><td>

Internal value of the install date.Data type: String

</td></tr><tr><td>

item.location

</td><td>

Details about the location of the install base item.Data type: Object

```
"location": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.location.display\_value

</td><td>

Text name of the install base item location. Use this value to display the location name in the UI.Data type: String

</td></tr><tr><td>

item.location.sys\_id

</td><td>

Sys\_id of the location record associated with the install base item record.Data type: String

</td></tr><tr id="name-integration-row"><td>

item.name

</td><td>

Name of the install base item.Data type: String

</td></tr><tr id="number-integration-row"><td>

item.number

</td><td>

Unique ID of the install base item.Data type: String

</td></tr><tr><td>

item.parent

</td><td>

Details about the parent record of the install base item record.Data type: Object

```
"parent": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.parent.display\_value

</td><td>

Text name of the parent record associated with the install base item record. Use this value to display the parent name in the UI.Data type: String

</td></tr><tr><td>

item.parent.sys\_id

</td><td>

Sys\_id of the parent record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.product

</td><td>

Details about the product model associated with the install base item record. Use this information to identify the services associated with any product model.Data type: Object

```
"product": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.product.display\_value

</td><td>

Text name of the product model associated with the install base item record. Use this value to display the product name in the UI.Data type: String

</td></tr><tr><td>

item.product.sys\_id

</td><td>

Sys\_id of the product model record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.quantity

</td><td>

Number of items installed.Data type: Integer

</td></tr><tr><td>

item.service\_context

</td><td>

Details about the service context associated with the install base item record.Data type: Object

```
"service_context": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.service\_context.display\_value

</td><td>

Details about the service context associated with the install base item record.Data type: Object

```
"service_context": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.service\_context.sys\_id

</td><td>

Sys\_id of the service context record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.service\_organization

</td><td>

Details about the service organization associated with the install base item record. Only returned if the Service Organization \(com.snc.service\_organization\) plugin is installed.Data type: Object

```
"service_organization": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.service\_organization.display\_value

</td><td>

Text name of the service organization associated with the install base item record. Use this value to display the service organization name in the UI.Data type: String

</td></tr><tr><td>

item.service\_organization.sys\_id

</td><td>

Sys\_id of the service organization record associated with the install base item record.Data type: String

</td></tr><tr id="sys_class_name-integration-row"><td>

item.sys\_class\_name

</td><td>

Table containing the install base item record.Data type: String

</td></tr><tr id="sys_id-integration-row"><td>

item.sys\_id

</td><td>

Sys\_id of the install base item record. Located in the table specified in the **sys\_class\_name** parameter.Data type: String

</td></tr><tr id="state-integration-row"><td>

item.state

</td><td>

Details about the current state of the install base item.Data type: Object

```
"state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="state_display_value-integration-row"><td>

item.state.display\_value

</td><td>

Text string of the current state of the install base item. Use this value to display the state in the UI.Data type: String

</td></tr><tr id="state_value-integration-row"><td>

item.state.value

</td><td>

Internal value of the state of the install base item.Data type: String

</td></tr><tr><td>

item.status

</td><td>

Details about the status of the install base item.Data type: Object

```
"status": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

item.status.display\_value

</td><td>

Text string of the status of the install base item. Use this value to display the status in the UI.Data type: String

</td></tr><tr><td>

item.status.value

</td><td>

Internal value of the status of the install base item.Data type: String

</td></tr><tr><td>

item.uninstall\_date

</td><td>

Details about the date when the install base item became inactive.Data type: Object

```
"uninstall_date": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

item.uninstall\_date.display\_value

</td><td>

Text uninstall date. Use this value to display the uninstall date in the UI.Data type: String

</td></tr><tr><td>

item.uninstall\_date.value

</td><td>

Internal value of the uninstall date.Data type: String

</td></tr><tr><td>

status

</td><td id="status-integration-entry">

Status of the endpoint call.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/installbaseitems/42746a3b876121100b6afc86dabb3597/uninstall" \
--request PATCH \
--header "Accept:application/json" \
--user 'username':'password'
```

Return results:

```
{
  "result": {
    "status": "SUCCESS",
    "item": {
      "sys_class_name": {
        "value": "sn_install_base_item",
        "display_value": "Install Base Item"
      },
      "number": "IBITM0000901",
      "sys_id": "f77c7542b7343300ece839a6ee11a991",
      "contact": {
        "sys_id": "4d147a386f0331003b3c498f5d3ee437",
        "display_value": "Julie Lewis"
      },
      "state": {
        "value": "inactive",
        "display_value": "Inactive"
      },
      "active": "false",
      "configuration_item": {
        "sys_id": "e5a28e07c30202001efd5cb981d3aedb",
        "display_value": "KX Series - KX5000"
      },
      "name": "KX Series - KX5000",
      "account": {
        "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
        "display_value": "Boxeo"
      }
    }
  }
}
```

## Install Base Item - POST /sn\_install\_base/integrations/installbaseitems

Creates one or more install base item records in the default Install Base Item table, or in its extended table if specified, and populates them with the specified field values.

When creating a single install base item record, you pass an object in the request body that contains all of the fields to include in the request body. When you create multiple install base item records in a single call, you pass an array of objects in the request body that contains all of the records to create. The endpoint processes and reports on each of the record creation objects individually. If one or more of the records fail to be created, it doesn't affect the creation of other record.

### URL format

Versioned URL: `/api/sn_install_base/{api_version}/integrations/installbaseitems`

Default URL: `/api/sn_install_base/integrations/installbaseitems`

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

<table id="id_x5m_53g_xwb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="account-request-integration-row"><td>

account

</td><td id="account-request-integration-entry">

Required when creating an install base item for an account.Sys\_id of the account to associate with the install base item.

**Note:** If you pass the **account** parameter, you can't also pass the **consumer** parameter.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr id="active-request-integration-row"><td>

active

</td><td id="active-request-integration-entry">

Flag that indicates whether the install base item is active.Valid values:

-   true, "true", or "0": Item is active.
-   false, "false", or "1": Item isn't active.

Data type: Boolean

Default: true

</td></tr><tr id="asset-request-integration-row"><td>

asset

</td><td id="asset-request-integration-entry">

Sys\_id of the asset associated with the install base item record.Data type: String

Table: Asset \[alm\_asset\]

</td></tr><tr id="child_install_base_items-request-integration-row"><td>

child\_install\_base\_items

</td><td id="child_install_base_items-request-integration-entry">

List of the child install base items associated with this install base item.**Note:** The following child install base item fields can't be different from its parent:

-   account
-   consumer
-   contact
-   service organization

Data type: Array of Objects

```
"child_install_base_items": [
  {
    "name": "String",
    "product": "String"
  }
]
```

</td></tr><tr id="child_install_base_items_name-request-integration-row"><td>

child\_install\_base\_items.name

</td><td id="child_install_base_items_name-request-integration-entry">

Name of the child install base item.Data type: String

</td></tr><tr id="child_install_base_items_product-request-integration-row"><td>

child\_install\_base\_items.product

</td><td id="child_install_base_items_product-request-integration-entry">

Sys\_id of the associated child base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr id="configuration_item-request-integration-row"><td>

configuration\_item

</td><td id="configuration_item-request-integration-entry">

Sys\_id of the configuration item associated with the install base item record.Data type: String

Table: Configuration Item \[cmdb\_ci\]

</td></tr><tr id="consumer-request-integration-row"><td>

consumer

</td><td id="consumer-request-integration-entry">

Required when creating an install base item for a consumer.Sys\_id of the consumer associated with the install base item record.

**Note:** If you pass the **consumer** parameter, you can't also pass the **account** parameter. In addition, you can only associate a consumer with an install base item if the B2B2C plugin is installed on your instance.

Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr id="consumer_profile-request-integration-row"><td>

consumer\_profile

</td><td id="consumer_profile-request-integration-entry">

Sys\_id of the consumer profile associated with the install base item record.Data type: String

Table: Consumer Profile \[sn\_csm\_consumer\_profile\]

</td></tr><tr id="contact-request-integration-row"><td>

contact

</td><td id="contact-request-integration-entry">

Sys\_id of the account contact record that is primarily responsible for the install base item.

**Note:** Contacts can only be specified for account install base items.

Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr id="household-request-integration-row"><td>

household

</td><td id="household-request-integration-entry">

Sys\_id of the household associated with the install base item record.**Note:** This field is only valid when the Customer Service Household \(com.snc.household\) plugin is installed.

Data type: String

Table: Household \[csm\_household\]

</td></tr><tr id="install_date-request-integration-row"><td>

install\_date

</td><td id="install_date-request-integration-entry">

Date on which the install base item becomes active.Data type: String

Format: yyyy-MM-dd HH:mm:ss

</td></tr><tr id="location-request-integration-row"><td>

location

</td><td id="location-request-integration-entry">

Sys\_id of the location of the associated product.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr id="name-request-integration-row"><td>

name

</td><td id="name-request-integration-entry">

Name of the install base item.Data type: String

</td></tr><tr id="number-request-integration-row"><td>

number

</td><td id="number-request-integration-entry">

Unique identifier for the install base item.Data type: String

Default: Automatically generated by the endpoint.

</td></tr><tr id="parent-request-integration-row"><td>

parent

</td><td id="parent-request-integration-entry">

Sys\_id of the parent record for this install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr id="product-request-integration-row"><td>

product\_model

</td><td id="product-request-integration-entry">

Sys\_id of the product model associated with the install base item record.Data type: String

Table: Product Model \[cmdb\_model\]

</td></tr><tr id="quantity-request-integration-row"><td>

quantity

</td><td id="quantity-request-integration-entry">

Number of items installed.Data type: Integer

</td></tr><tr id="service_context-request-integration-row"><td>

service\_context

</td><td id="service_context-request-integration-entry">

Sys\_id of the service that is associated to the underlying CI for calculating the impact severity from Event Management. For more information, see [Service health status for install base](https://www.servicenow.com/docs/access?context=service-health-pcso&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).**Note:** This field is only valid if the Proactive Customer Service Operations with Event Management plugin is installed.

Data type: String

</td></tr><tr id="service_organization-request-integration-row"><td>

service\_organization

</td><td id="service_organization-request-integration-entry">

Required when creating an install base item for a service organization.Sys\_id of the service organization record that is involved in providing service to the customer.

**Note:** If you pass this parameter, you shouldn't also pass the account, contact, or consumer parameters. The **service\_organization** parameter is only available when the Service Organization \(com.snc.service\_organization\) plugin is installed on your instance.

Data type: String

Table: Service Organization \[sn\_customer\_service\_organization\]

</td></tr><tr id="state-request-integration-row"><td>

state

</td><td id="state-request-integration-entry">

Current state of the install base item.Valid values:

-   in\_use
-   inactive

Data type: String

</td></tr><tr id="status-request-integration-row"><td>

status

</td><td id="status-request-integration-entry">

Status of the product.Valid values:

-   original
-   replacement

Data type: String

</td></tr><tr><td>

sys\_class\_name

</td><td>

Name of the extended install base table in which to create the install base item record.Data type: String

Default: Install Base Item \[sn\_install\_base\_item\] table

</td></tr><tr id="uninstall_date-request-integration-row"><td>

uninstall\_date

</td><td id="uninstall_date-request-integration-entry">

Date on which the install base becomes inactive.Data type: String

Format: yyyy-MM-dd HH:mm:ss

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
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="id_fw5_m3f_xwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="error-integration-entry">

Details about the error that occurred when trying to process the request.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td id="error_detail-integration-entry">

Additional details about the associated error.Data type: String

</td></tr><tr><td>

error.message

</td><td id="error_message-integration-entry">

Error message that describes the problem that occurred when trying to execute the request.Data type: String

</td></tr><tr><td>

item

</td><td>

Install base item that matched the specified filter results. Only non-empty fields are returned.Data type: Array of Objects

```
"item": {
  "account": {Object},
  "active": "String",
  "asset": {Object},
  "child_install_base_items": {Object},
  "condition": "String",
  "configuration_item": {Object},
  "consumer": {Object},
  "consumer_profile": {Object},
  "contact": {Object},
  "health_status": {Object},
  "health_status_last_updated": "String",
  "household": {Object},
  "install_date": {Object},
  "location": {Object},
  "name": "String",
  "number": "String",
  "parent": {Object},
  "product": {Object},
  "quantity": Integer,
  "service_context": {Object},
  "service_organization" {Object},
  "sys_id": "String",
  "state": {Object},
  "status": {Object},
  "uninstall_date": "String"
}
```

</td></tr><tr id="account-integration-row"><td>

item.account

</td><td>

Details about the customer account associated with the install base item record.Data type: Object

```
"account": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="account_display_value-integration-row"><td>

item.account.display\_value

</td><td>

Text name of the customer account associated with the install base item record. Use this value to display the customer account name in the UI.Data type: String

</td></tr><tr id="account_sys_id-integration-row"><td>

item.account.sys\_id

</td><td>

Sys\_id of the customer account record associated with the install base item record.Data type: String

</td></tr><tr id="active-integration-row"><td>

item.active

</td><td>

Flag that indicates whether the install base item is active.Possible values:

-   true: Install base item is active.
-   false: Install base item is inactive.

Data type: Boolean String

</td></tr><tr><td>

item.asset

</td><td>

Details about the asset associated with the install base item record.Data type: Object

```
"asset": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.asset.display\_value

</td><td>

Text name of the asset associated with the install base item record. Use this value to display the asset name in the UI.Data type: String

</td></tr><tr><td>

item.asset.sys\_id

</td><td>

Sys\_id of the asset record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.child\_install\_base\_items

</td><td>

List of the child install base items associated with this install base item.**Note:** The following child install base item fields can't be different from its parent:

-   account
-   consumer
-   contact
-   service organization

Data type: Array of Objects

```
"child_install_base_items": [
  {
    "name": "String",
    "product": "String"
  }
]
```

</td></tr><tr><td>

item.child\_install\_base\_items.name

</td><td>

Name of the child install base item.Data type: String

</td></tr><tr><td>

item.child\_install\_base\_items.product

</td><td>

Sys\_id of the associated child base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr><tr><td>

item.configuration\_item

</td><td>

Details about the configuration item associated with the install base item record.Data type: Object

```
"configuration_item": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.configuration\_item.display\_value

</td><td>

Text name of the configuration item associated with the install base item record. Use this value to display the configuration item name in the UI.Data type: String

</td></tr><tr><td>

item.configuration\_item.sys\_id

</td><td>

Sys\_id of the configuration item record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.consumer

</td><td>

Details about the consumer associated with the install base item record.**Note:** The consumer field is only available if the B2B2C plugin is installed.

Data type: Object

```
"consumer": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.consumer.display\_value

</td><td>

Text name of the consumer associated with the install base item record. Use this value to display the consumer name in the UI.Data type: String

</td></tr><tr><td>

item.consumer.sys\_id

</td><td>

Sys\_id of the consumer record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.consumer\_profile

</td><td>

Details about the consumer profile associated with the install base item record.**Note:** The consumer profile field is only available if the B2B2C plugin is installed.

Data type: Object

```
"consumer_profile": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.consumer\_profile.display\_value

</td><td>

Text name of the consumer profile associated with the install base item record. Use this value to display the consumer profile name in the UI.Data type: String

</td></tr><tr><td>

item.consumer\_profile.sys\_id

</td><td>

Sys\_id of the consumer profile record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.contact

</td><td>

Details about the account contact responsible for the install base item record.Data type: Object

```
"contact": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.contact.display\_value

</td><td>

Text name of the account contact associated with the install base item record. Use this value to display the account contact name in the UI.Data type: String

</td></tr><tr><td>

item.contact.sys\_id

</td><td>

Sys\_id of the account contact record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.health\_status

</td><td>

Details about the current health status of the install base item. Only returned if the Proactive Customer Service Operations \(com.snc.proactive\_cs\_itom\) plugin is installed.Data type: Object

```
"health_status": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

item.health\_status.display\_value

</td><td>

Text string of the current health status of the install base item. Use this value to display the health status in the UI.Data type: String

</td></tr><tr><td>

item.health\_status.value

</td><td>

Internal value of the health status of the install base item.Data type: String

</td></tr><tr><td>

item.health\_status\_last\_updated

</td><td>

Date and time when the health status was last updated for the install base item.Data type: String

</td></tr><tr><td>

item.household

</td><td>

Details about the household associated with the install base item record. Only returned if the Customer Service Household \(com.snc.household\) plugin is installed.Data type: Object

```
"household": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.household.display\_value

</td><td>

Text name of the household associated with the install base item record. Use this value to display the household name in the UI.Data type: String

</td></tr><tr><td>

item.household.sys\_id

</td><td>

Sys\_id of the household associated with the install base item record.Data type: String

</td></tr><tr><td>

item.install\_date

</td><td>

Details about the date when the install base item became active.Data type: Object

```
"install_date": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

item.install\_date.display\_value

</td><td>

Text install date. Use this value to display the install date in the UI.Data type: String

</td></tr><tr><td>

item.install\_date.value

</td><td>

Internal value of the install date.Data type: String

</td></tr><tr><td>

item.location

</td><td>

Details about the location of the install base item.Data type: Object

```
"location": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.location.display\_value

</td><td>

Text name of the install base item location. Use this value to display the location name in the UI.Data type: String

</td></tr><tr><td>

item.location.sys\_id

</td><td>

Sys\_id of the location record associated with the install base item record.Data type: String

</td></tr><tr id="name-integration-row"><td>

item.name

</td><td>

Name of the install base item.Data type: String

</td></tr><tr id="number-integration-row"><td>

item.number

</td><td>

Unique ID of the install base item.Data type: String

</td></tr><tr><td>

item.parent

</td><td>

Details about the parent record of the install base item record.Data type: Object

```
"parent": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.parent.display\_value

</td><td>

Text name of the parent record associated with the install base item record. Use this value to display the parent name in the UI.Data type: String

</td></tr><tr><td>

item.parent.sys\_id

</td><td>

Sys\_id of the parent record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.product

</td><td>

Details about the product model associated with the install base item record. Use this information to identify the services associated with any product model.Data type: Object

```
"product": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.product.display\_value

</td><td>

Text name of the product model associated with the install base item record. Use this value to display the product name in the UI.Data type: String

</td></tr><tr><td>

item.product.sys\_id

</td><td>

Sys\_id of the product model record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.quantity

</td><td>

Number of items installed.Data type: Integer

</td></tr><tr><td>

item.service\_context

</td><td>

Details about the service context associated with the install base item record.Data type: Object

```
"service_context": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.service\_context.display\_value

</td><td>

Details about the service context associated with the install base item record.Data type: Object

```
"service_context": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.service\_context.sys\_id

</td><td>

Sys\_id of the service context record associated with the install base item record.Data type: String

</td></tr><tr><td>

item.service\_organization

</td><td>

Details about the service organization associated with the install base item record. Only returned if the Service Organization \(com.snc.service\_organization\) plugin is installed.Data type: Object

```
"service_organization": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

item.service\_organization.display\_value

</td><td>

Text name of the service organization associated with the install base item record. Use this value to display the service organization name in the UI.Data type: String

</td></tr><tr><td>

item.service\_organization.sys\_id

</td><td>

Sys\_id of the service organization record associated with the install base item record.Data type: String

</td></tr><tr id="sys_class_name-integration-row"><td>

item.sys\_class\_name

</td><td>

Table containing the install base item record.Data type: String

</td></tr><tr id="sys_id-integration-row"><td>

item.sys\_id

</td><td>

Sys\_id of the install base item record. Located in the table specified in the **sys\_class\_name** parameter.Data type: String

</td></tr><tr id="state-integration-row"><td>

item.state

</td><td>

Details about the current state of the install base item.Data type: Object

```
"state": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr id="state_display_value-integration-row"><td>

item.state.display\_value

</td><td>

Text string of the current state of the install base item. Use this value to display the state in the UI.Data type: String

</td></tr><tr id="state_value-integration-row"><td>

item.state.value

</td><td>

Internal value of the state of the install base item.Data type: String

</td></tr><tr><td>

item.status

</td><td>

Details about the status of the install base item.Data type: Object

```
"status": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

item.status.display\_value

</td><td>

Text string of the status of the install base item. Use this value to display the status in the UI.Data type: String

</td></tr><tr><td>

item.status.value

</td><td>

Internal value of the status of the install base item.Data type: String

</td></tr><tr><td>

item.uninstall\_date

</td><td>

Details about the date when the install base item became inactive.Data type: Object

```
"uninstall_date": {
  "display_value": "String",
  "value": "String"
}
```

</td></tr><tr><td>

item.uninstall\_date.display\_value

</td><td>

Text uninstall date. Use this value to display the uninstall date in the UI.Data type: String

</td></tr><tr><td>

item.uninstall\_date.value

</td><td>

Internal value of the uninstall date.Data type: String

</td></tr><tr id="status-integration-row"><td>

status

</td><td>

Status of the endpoint call.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to create a single Install Base Item record.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/installbaseitems" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"name\":\"Base Monitor\",
  \"quantity\": 4,
  \"account\":\"86837a386f0331003b3c498f5d3ee4ca\",
  \"contact\": \"dc0185d94f341200025ba3618110c77c\",
  \"configuration_item\":\"0c43baaac61122750182c132ee74bcf0\",
  \"state\":\"in_use\"
}" \
--user 'username':'password'
```

Return results: Only non-empty fields are returned.

```
{
  "result": {
    "status": "SUCCESS",
    "item": {
      "sys_class_name": "sn_install_base_item",
      "number": "IBITM0001003",
      "sys_id": "27cb093114c66910f877324710112fd6",
      "contact": {
        "sys_id": "dc0185d94f341200025ba3618110c77c",
        "display_value": "Cindy Contact"
      },
      "state": {
        "value": "in_use",
        "display_value": "In Use"
      },
      "quantity": "4",
      "active": "true",
      "configuration_item": {
        "sys_id": "0c43baaac61122750182c132ee74bcf0",
        "display_value": "3D Pinball"
      },
      "name": "Base Monitor",
      "account": {
        "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
        "display_value": "Boxeo"
      }
    }
  }
}
```

### cURL request

The following code example shows how to create multiple Install Base Item records.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/installbaseitems" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "[
  {
    \"name\":\"AST4 Laptop\",
    \"consumer\":\"b119803fdb1b1200b6075200cf961917\",
    \"status\":\"replacement\",
    \"install_date\":\"2023-05-18 12:00:00\",
    \"uninstall_date\":\"2023-09-28 12:00:00\"
  },
{
    \"name\":\"Base Monitor\",
    \"quantity\": 4,
    \"account\":\"86837a386f0331003b3c498f5d3ee4ca\",
    \"contact\": \"dc0185d94f341200025ba3618110c77c\",
    \"configuration_item\":\"0c43baaac61122750182c132ee74bcf0\",
    \"state\":\"in_use\"
  }
]" \
--user 'username':'password'
```

Return results: Only non-empty fields are returned.

```
{
  "result": {
    "status": "SUCCESS",
    "items": [
      {
        "status": "SUCCESS",
        "item": {
          "sys_class_name": "sn_install_base_item",
          "number": "IBITM0001018",
          "sys_id": "16fe91b1140a6910f877324710112f40",
          "uninstall_date": {
            "value": "2023-09-28 12:00:00",
            "display_value": "2023-09-28 05:00:00"
          },
          "install_date": {
            "value": "2023-05-18 12:00:00",
            "display_value": "2023-05-18 05:00:00"
          },
          "consumer": {
            "sys_id": "b119803fdb1b1200b6075200cf961917",
            "display_value": "Silvester Erik"
          },
          "active": "true",
          "name": "AST4 Laptop",
          "status": {
            "value": "replacement",
            "display_value": "Replacement"
          }
        }
      },
      {
        "status": "SUCCESS",
        "item": {
          "sys_class_name": "sn_install_base_item",
          "number": "IBITM0001019",
          "sys_id": "5efe91b1140a6910f877324710112f40",
          "contact": {
            "sys_id": "dc0185d94f341200025ba3618110c77c",
            "display_value": "Cindy Contact"
          },
          "state": {
            "value": "in_use",
            "display_value": "In Use"
          },
          "quantity": "4",
          "active": "true",
          "configuration_item": {
            "sys_id": "0c43baaac61122750182c132ee74bcf0",
            "display_value": "3D Pinball"
          },
          "name": "Base Monitor",
          "account": {
            "sys_id": "86837a386f0331003b3c498f5d3ee4ca",
            "display_value": "Boxeo"
          }
        }
      }
    ]
  }
}
```

## Install Base Item - POST /sn\_install\_base/integrations/installbaseitems/\{id\}/relatedparties

Creates a related party record and associates it with a specified install base item record. The values specified in the request parameters are stored in the newly created related party record.

### URL format

Versioned URL: `/api/sn_install_base/{api_version}/integrations/installbaseitems/{id}/relatedparties`

Default URL: `/api/sn_install_base/integrations/installbaseitems/{id}/relatedparties`

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

</td><td id="integrate-id-entry">

Sys\_id of the install base item record.Data type: String

Table: Install Base Item \[sn\_install\_base\_item\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="account-request-integration-row"><td>

account

</td><td id="account-request-integration-entry">

Required if the **type** parameter is one of the following: -   `Authorized Account`
-   `Authorized Contact`
-   `Listed Account`
-   `Listed Contact`

Sys\_id of the account to associate with the install base item.

**Note:** If you pass the **account** parameter, you can't also pass the **consumer** parameter.

Data type: String

Table: Account \[customer\_account\]

</td></tr><tr id="consumer-request-integration-row"><td>

consumer

</td><td id="consumer-request-integration-entry">

Required if the **type** parameter is `Authorized Consumer` or `Listed Consumer`. Sys\_id of the consumer associated with the install base item record.

**Note:** If you pass the **consumer** parameter, you can't also pass the **account** parameter. In addition, you can only associate a consumer with an install base item if the B2B2C plugin is installed on your instance.

Data type: String

Table: Consumer \[csm\_consumer\]

</td></tr><tr><td>

contact

</td><td>

Sys\_id of the contact record associated with the related parties record.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

install\_base\_item

</td><td>

Sys\_id of the install base item record associated with the related parties record.Data type: String

</td></tr><tr><td>

responsibility

</td><td>

Sys\_id of the associated responsibility record. This record defines the access level for the install base information.This parameter is only valid if the **related\_party** field is also specified. If specified, it only returns the install base items that match both the **related\_party** and **responsibility** parameters.

For additional information, see [Configure related parties for Items Received](https://www.servicenow.com/docs/access?context=psds-add-related-parties-to-record&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)

Data type: String

Table: Responsibility Definition \[sn\_customerservice\_responsibility\_def\]

</td></tr><tr id="service_organization-request-integration-row"><td>

service\_organization

</td><td id="service_organization-request-integration-entry">

Required if the **type** parameter is one of the following: -   `Authorized Member`
-   `Authorized Service Organization`
-   `Listed Member`
-   `Listed Service Organization`

Sys\_id of the service organization record that is involved in providing service to the customer.

**Note:** If you pass this parameter, you shouldn't also pass the account, contact, or consumer parameters. The **service\_organization** parameter is only available when the Service Organization \(com.snc.service\_organization\) plugin is installed on your instance.

Data type: String

Table: Service Organization \[sn\_customer\_service\_organization\]

</td></tr><tr><td>

sys\_class\_name

</td><td>

Table containing the related parties record.Data type: String

Default: sn\_install\_base\_related\_party

</td></tr><tr><td>

type

</td><td>

Required. Sys\_id of the type of related party to create.Possible types:

-   Authorized Account
-   Authorized Consumer
-   Authorized Contact
-   Authorized Contributor
-   Authorized Member
-   Authorized Service Organization
-   Listed Account
-   Listed Consumer
-   Listed Contact
-   Listed Contributor
-   Listed Member
-   Listed Service Organization

Data type: String

Table: Related Party Configuration \[sn\_customerservice\_related\_party\_configuration\]

</td></tr><tr><td>

user

</td><td>

Required if the **type** parameter is one of the following related party types: -   `Authorized Contributor`
-   `Authorized Member`
-   `Listed Contributor`
-   `Listed Member`

For `Authorized Member` and `Listed Member`, this user must be associated with the specified **service\_organization** record.

Sys\_id of the user record associated with the related parties record.

Data type: String

Table: User \[sys\_user\]

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
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
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

Details about the account associated with the related parties record.Data type: Object

```
account": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

account.display\_value

</td><td>

Text name of the account associated with the related parties record. Use this value to display the account name in the UI.Data type: String

</td></tr><tr><td>

account.sys\_id

</td><td>

Sys\_id of the account record associated with the related parties record.Data type: String

</td></tr><tr><td>

consumer

</td><td>

Details about the consumer associated with the related parties record.Data type: Object

```
"consumer": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

consumer.display\_value

</td><td>

Text name of the consumer associated with the related parties record. Use this value to display the consumer name in the UI.Data type: String

</td></tr><tr><td>

consumer.sys\_id

</td><td>

Sys\_id of the consumer record associated with the related parties record.Data type: String

</td></tr><tr><td>

contact

</td><td>

Details about the account contact responsible for the related parties record.Data type: Object

```
"contact": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

contact.display\_value

</td><td>

Text name of the contact associated with the related parties record. Use this value to display the contact name in the UI.Data type: String

</td></tr><tr><td>

contact.sys\_id

</td><td>

Sys\_id of the contact record associated with the related parties record.Data type: String

Table: Contact \[customer\_contact\]

</td></tr><tr><td>

error

</td><td id="error-integration-entry">

Details about the error that occurred when trying to process the request.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td id="error_detail-integration-entry">

Additional details about the associated error.Data type: String

</td></tr><tr><td>

error.message

</td><td id="error_message-integration-entry">

Error message that describes the problem that occurred when trying to execute the request.Data type: String

</td></tr><tr><td>

install\_base\_item

</td><td>

Details about the install base item associated with the related parties record.Data type: Object

```
"install_base_item": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

install\_base\_item.display\_value

</td><td>

Text name of the install base item associated with the related parties record. Use this value to display the install base item name in the UI.Data type: String

</td></tr><tr><td>

install\_base\_item.sys\_id

</td><td>

Sys\_id of the install base item record associated with the related parties record.Data type: String

</td></tr><tr><td>

responsibility

</td><td>

Details about the access level for the install base information. Data type: Object

```
"responsibility": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

responsibility.display\_value

</td><td>

Text display value for the access level for the install base information.Data type: String

</td></tr><tr><td>

responsibility.sys\_id

</td><td>

Sys\_id of the associated responsibility record. This record defines the access level for the install base information.This parameter is only valid if the **related\_party** field is also specified. If specified, it only returns the install base items that match both the **related\_party** and **responsibility** parameters.

For additional information, see [Configure related parties for Items Received](https://www.servicenow.com/docs/access?context=psds-add-related-parties-to-record&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)

Data type: String

Table: Responsibility Definition \[sn\_customerservice\_responsibility\_def\]

</td></tr><tr><td>

status

</td><td id="status-integration-entry">

Status of the endpoint call.Data type: String

</td></tr><tr><td>

sys\_class\_name

</td><td>

Table containing the related parties record.Data type: String

Default: sn\_install\_base\_related\_party

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the associated related parties record.Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td id="sysparm_limit-integration-entry">

Number of records that were returned. If this value isn't specified in the original request, it uses the default value.Data type: Number

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-integration-entry">

Offset \(starting point\) in the associated table from which records were evaluated and retrieved.Data type: String

</td></tr><tr><td>

type

</td><td>

Details about the type of contact associated with the related parties record.Data type: Object

```
"type": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

type.display\_value

</td><td>

Text name of the type of contact associated with the related parties record. Use this value to display the type of contact in the UI. For additional information, see [Create related party configurations](https://www.servicenow.com/docs/access?context=adding-related-party-config-to-case&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).Possible types:

-   Authorized Account
-   Authorized Consumer
-   Authorized Contact
-   Authorized Contributor
-   Authorized Member
-   Authorized Service Organization
-   Listed Account
-   Listed Consumer
-   Listed Contact
-   Listed Contributor
-   Listed Member
-   Listed Service Organization

Data type: String

</td></tr><tr><td>

type.sys\_id

</td><td>

Sys\_id of the type record associated with the related parties record.Data type: String

</td></tr><tr><td>

user

</td><td>

Details about the user associated with the related parties record.Data type: Object

```
"user": {
  "display_value": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

user.display\_value

</td><td>

Text name of the user associated with the related parties record. Use this value to display the user name in the UI.Data type: String

</td></tr><tr><td>

user.sys\_id

</td><td>

Sys\_id of the user record associated with the related parties record.

Data type: String

Table: User \[sys\_user\]

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint to create an Authorized Account related record and associate it with an install base item.

```
curl "https://instance.servicenow.com/api/sn_install_base/integrations/relatedparties/f77c7542b7343300ece839a6ee11a991" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  "contact":"0a232a0013691200042ab3173244b075",
  "type":"68ec8b2965e99110f87764df53db779f",
  "account":"86837a386f0331003b3c498f5d3ee4ca",
  "install_base_item":"f77c7542b7343300ece839a6ee11a991",
  "responsibility":"c009bbedb3730010700b4d43c6a8dcef",
  "sys_class_name":"sn_install_base_related_party"
}" \
--user 'username':'password'
```

Return results:

```
{
"result":
  {
    "type": {
      "display_value":"Authorized Contact",
      "sys_id":"68ec8b2965e99110f87764df53db779f"
    },
    "install_base_item": {
      "display_value":"KX Series - KX5000",
      "sys_id":"f77c7542b7343300ece839a6ee11a991"
    },
    "sys_class_name":"sn_install_base_related_party",
    "sys_id":"4659539814ac6910f877ae314c1fb43a",
    "responsibility": {
      "display_value":"Authorized Representative",
      "sys_id":"c009bbedb3730010700b4d43c6a8dcef"
    },
    "contact": {
      "display_value":"Cindy Contact",
      "sys_id":"dc0185d94f341200025ba3618110c77c"
    },
    "account": {
      "display_value":"Boxeo",
      "value":"86837a386f0331003b3c498f5d3ee4ca"
    },
    "status":"SUCCESS",
  }
}
```

