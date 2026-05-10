---
title: CMDB Instance API
description: The CMDB Instance API provides endpoints to create, read, update, and delete operations on existing Configuration Management Database \(CMDB\) tables. You can only insert, update, or delete one record at a time.Deletes the relation for the specified configuration item \(CI\).Returns the available configuration items \(CI\) for a specified Configuration Management Database \(CMDB\) class \(table\).Returns attributes and relationship information for a specified configuration item \(CI\) record.Creates a single configuration item \(CI\) with the specified outbound and inbound relations within the specified Configuration Management Database \(CMDB\) table.Updates the specified configuration item \(CI\) record with the specified attribute name-value pairs. This endpoint does not create, update, or delete the associated relations.Adds an inbound and/or outbound relation to the specified configuration item \(CI\). The specified CI is the parent.Replaces the attributes in the specified configuration item \(CI\) record with the specified name-value pairs. This endpoint does not create, update, or delete the associated relations.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 43
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# CMDB Instance API

The CMDB Instance API provides endpoints to create, read, update, and delete operations on existing Configuration Management Database \(CMDB\) tables. You can only insert, update, or delete one record at a time.

This API requires the user have the ITIL role.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## CMDB Instance - DELETE /now/cmdb/instance/\{classname\}/\{sys\_id\}/relation/\{rel\_sys\_id\}

Deletes the relation for the specified configuration item \(CI\).

### URL format

Versioned URL: `/api/now/{api_version}/cmdb/instance/{className}/{sys_id}/relation/{rel_sys_id}`

Default URL: `/api/now/cmdb/instance/{className}/{sys_id}/relation/{rel_sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

className

</td><td id="entry-className-cmdb">

CMDB class name. This is the name of the table that contains the desired CI records, such as cmdb\_ci\_linux\_server or cmdb\_ci\_apache\_web\_server.Data type: String

</td></tr><tr><td>

rel\_sys\_id

</td><td>

Sys\_id of the relation to remove.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the CI.Data type: String

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
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|405|Invalid method. The functionality is disabled.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|None||

### Sample cURL request

```
curl "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci_linux_server/0f4ac6c4b750230096c3e4f6ee11a9fe/relation/b0dbda5347c12200e0ef563dbb9a718f" \
--request DELETE \
--user 'username':'password'

```

## CMDB Instance - GET /now/cmdb/instance/\{classname\}

Returns the available configuration items \(CI\) for a specified Configuration Management Database \(CMDB\) class \(table\).

### URL format

Versioned URL: `/api/now/{api_version}/cmdb/instance/{className}`

Default URL: `/api/now/cmdb/instance/{className}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

className

</td><td id="entry-className-cmdb">

CMDB class name. This is the name of the table that contains the desired CI records, such as cmdb\_ci\_linux\_server or cmdb\_ci\_apache\_web\_server.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

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

</td></tr><tr><td>

sysparm\_query

</td><td id="sysparm-query-RESTAPI">

[Encoded query](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_EncodedQueryStrings.md) used to filter the result set. You can use a UI filter to obtain a properly encoded query.Syntax: `sysparm_query=<col_name><operator><value>`. Column names, operators, and values are case-sensitive.

-   &lt;col\_name&gt;: Name of the table column to filter on.
-   &lt;operator&gt;: Supports the following values:
    -   `=`: &lt;col\_name&gt; exactly matches &lt;value&gt;.
    -   `!=`: &lt;col\_name&gt; does not match &lt;value&gt;.
    -   `LIKE`: &lt;col\_name&gt; contains the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `STARTSWITH`: &lt;col\_name&gt; starts with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `ENDSWITH`: &lt;col\_name&gt; ends with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `^`: AND operator to add an additional query condition. Records included in the result set match both conditions.
    -   `^OR`: OR operator to add an additional query condition. Records included in the result set match at least one of the conditions.
-   &lt;value&gt;: Value to filter on.

For more information about operators, see [Operators available for filters and queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/r_OpAvailableFiltersQueries.md).

Queries can contain multiple conditions. For example, the following query returns records where the caller is the current user and the record is active.

`sysparm_query=caller_id=javascript:gs.getUserID()^active=true`

Encoded queries also support order by ascending and descending functionality. To sort responses based on certain fields, use the `ORDERBY` and `ORDERBYDESC` clauses in **sysparm\_query**.

Syntax:

-   `ORDERBY<col_name>`
-   `ORDERBYDESC<col_name>`

For example, the following query gets all active records and orders the results in ascending order by number, and then in descending order by category.

`sysparm_query=active=true^ORDERBYnumber^ORDERBYDESCcategory`

By default, if part of a query is invalid, such as an invalid field name, the instance ignores the invalid part. It then returns rows using only the valid portion of the query. Set the property **glide.invalid\_query.returns\_no\_rows** to `true` to instead return no rows on an invalid query.

**Note:** The **glide.invalid\_query.returns\_no\_rows** property controls the behavior of all queries across the instance, such as in lists, scripts \(GlideRecord.query\(\)\), and web service APIs.

Data type: String

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
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|405|Invalid method. The functionality is disabled.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

Name of a CI within the specified class.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the CI.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci_linux_server" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'

```

```
"result": [
  {
    "sys_id": "3a290cc60a0a0bb400000bdb386af1cf",
    "name": "PS LinuxApp01"
  },
  {
    "sys_id": "3a5dd3dbc0a8ce0100655f1ec66ed42c",
    "name": "PS LinuxApp02"
  }
]
```

## CMDB Instance - GET /now/cmdb/instance/\{classname\}/\{sys\_id\}

Returns attributes and relationship information for a specified configuration item \(CI\) record.

### URL format

Versioned URL: `/api/now/{api_version}/cmdb/instance/{className}/{sys_id}`

Default URL: `/api/now/cmdb/instance/{className}/{sys_id}`

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

className

</td><td id="entry-className-cmdb">

CMDB class name. This is the name of the table that contains the desired CI records, such as cmdb\_ci\_linux\_server or cmdb\_ci\_apache\_web\_server.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the CI record to retrieve.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None||

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
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|405|Invalid method. The functionality is disabled.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_d5p_jn4_3mb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td>

Data attributes currently in the CI record. The available attributes depend on the specified CMDB class. You can locate the available attributes in the associated CMDB table which typically begins with "cmdb\_ci", such as cmdb\_ci\_linux\_server or cmdb\_ci\_mfp\_printer.Data type: Object

</td></tr><tr id="row-result-error-cmdb"><td>

error

</td><td id="entry-result-error-cmdb">

Information on any errors encountered while processing the endpoint request. Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr id="row-result-error_detail-cmdb"><td>

error.detail

</td><td id="entry-result-error_detail-cmdb">

Additional information about the error.Data type: String

</td></tr><tr id="row-result-error_message-cmdb"><td>

error.message

</td><td id="entry-result-error_message-cmdb">

Message that identifies the error.Data type: String

</td></tr><tr id="row-result-inbound_relations-cmdb"><td>

inbound\_relations

</td><td id="entry-result-inbound_relations-cmdb">

List of objects that define the inbound relations associated with the CI.Data type: Array

```
"inbound_relations": [
  {
    "sys_id": "String",
    "target": {Object},
    "type": {Object}
  }
]
```

</td></tr><tr id="row-result-inbound_relations_sys_id-cmdb"><td>

inbound\_relations.sys\_id

</td><td id="entry-result-inbound_relations_sys_id-cmdb">

Sys\_id of the inbound CI relationship. Located in the CI Relationship \[cmdb\_rel\_ci\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_target-cmdb"><td>

inbound\_relations.target

</td><td id="entry-result-inbound_relations_target-cmdb">

Information that describes the target inbound relation.Data type: Object

```
"target": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-inbound_relations_target_display_value-cmdb"><td>

inbound\_relations.target.display\_value

</td><td id="entry-result-inbound_relations_target_display_value-cmdb">

Name of the inbound relation to display in a user interface.Data type: String

</td></tr><tr id="row-result-inbound_relations_target_link-cmdb"><td>

inbound\_relations.target.link

</td><td id="entry-result-inbound_relations_target_link-cmdb">

CMDB REST endpoint URL to use to retrieve the inbound relation from the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_target_value-cmdb"><td>

inbound\_relations.target.value

</td><td id="entry-result-inbound_relations_target_value-cmdb">

Sys\_id of the inbound CI. Located in the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_type-cmdb"><td>

inbound\_relations.type

</td><td id="entry-result-inbound_relations_type-cmdb">

Information about the type of inbound relationship. Data type: Object

```
"type": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-inbound_relations_type_display_value-cmdb"><td>

inbound\_relations.type.display\_value

</td><td id="entry-result-inbound_relations_type_display_value-cmdb">

Name of the inbound type to display in a user interface.Data type: String

</td></tr><tr id="row-result-inbound_relations_type_link-cmdb"><td>

inbound\_relations.type.link

</td><td id="entry-result-inbound_relations_type_link-cmdb">

Table REST endpoint URL to use to retrieve the inbound relation type from the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_type_value-cmdb"><td>

inbound\_relations.type.value

</td><td id="entry-result-inbound_relations_type_value-cmdb">

Sys\_id of the type of inbound relationship. Located in the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations-cmdb"><td>

outbound\_relations

</td><td id="entry-result-outbound_relations-cmdb">

List of objects that define the outbound relations associated with the CI.Data type: Array

```
"outbound_relations": [
  {
    "sys_id": "String",
    "target": {Object},
    "type": {Object}
  }
]
```

</td></tr><tr id="row-result-outbound_relations_sys_id-cmdb"><td>

outbound\_relations.sys\_id

</td><td id="entry-result-outbound_relations_sys_id-cmdb">

Sys\_id of the outbount CI relationship. Located in the CI Relationship \[cmdb\_rel\_ci\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_target-cmdb"><td>

outbound\_relations.target

</td><td id="entry-result-outbound_relations_target-cmdb">

Required. Information about the target outbound relation.Data type: Object

```
"target": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-outbound_relations_target_display_value-cmdb"><td>

outbound\_relations.target.display\_value

</td><td id="entry-result-outbound_relations_target_display_value-cmdb">

Name of the outbound relation to display in a user interface.Data type: String

</td></tr><tr id="row-result-outbound_relations_target_link-cmdb"><td>

outbound\_relations.target.link

</td><td id="entry-result-outbound_relations_target_link-cmdb">

CMDB REST endpoint URL to use to retrieve the outbound relation from the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_target_value-cmdb"><td>

outbound\_relations.target.value

</td><td id="entry-result-outbound_relations_target_value-cmdb">

Sys\_id of the outbound CI. Located in the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_type-cmdb"><td>

outbound\_relations.type

</td><td id="entry-result-outbound_relations_type-cmdb">

Information about the type of outbound relationship. Data type: Object

```
"type": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-outbound_relations_type_display_value-cmdb"><td>

outbound\_relations.type.display\_value

</td><td id="entry-result-outbound_relations_type_display_value-cmdb">

Name of the outbound type to display in a user interface.Data type: String

</td></tr><tr id="row-result-outbound_relations_type_link-cmdb"><td>

outbound\_relations.type.link

</td><td id="entry-result-outbound_relations_type_link-cmdb">

Table REST endpoint URL to use to retrieve the outbound relation from the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_type_value-cmdb"><td>

outbound\_relations.type.value

</td><td id="entry-result-outbound_relations_type_value-cmdb">

Sys\_id of the type of outbound relationship. Located in the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-status-cmdb"><td>

status

</td><td id="entry-result-status-cmdb">

Only appears if an error is encountered. Status of the endpoint processing.Possible value: failure

Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci_linux_server/70bc4e11c0a8210d01f074cbe6bd73b4" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "result": {
    "outbound_relations": [
      {
        "sys_id": "3a62e64ac0a8ce0100aead1e3fd5439f",
        "type": {
          "display_value": "Depends on::Used by",
          "link": "https://instance.servicenow.com/api/now/table/cmdb_rel_type/1a9cb166f1571100a92eb60da2bce5c5",
          "value": "1a9cb166f1571100a92eb60da2bce5c5"
        },
        "target": {
          "display_value": "PS ORA01",
          "link": "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci/3a307c930a0a0bb400353965d0b8861f",
          "value": "3a307c930a0a0bb400353965d0b8861f"
        }
      },
      {
        "sys_id": "3a67513fc0a8ce0100914a76cea11b02",
        "type": {
          "display_value": "Exchanges data with::Exchanges data with",
          "link": "https://instance.servicenow.com/api/now/table/cmdb_rel_type/607ad1b2c0a8010e01941856b365af90",
          "value": "607ad1b2c0a8010e01941856b365af90"
        },
        "target": {
          "display_value": "PS ORA01",
          "link": "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci/3a307c930a0a0bb400353965d0b8861f",
          "value": "3a307c930a0a0bb400353965d0b8861f"
        }
      }
    ],
    "attributes": {
      "firewall_status": "Intranet",
      "os_address_width": "",
      "attested_date": "",
      "operational_status": "1",
      "os_service_pack": "",
      "cpu_core_thread": "",
      "cpu_manufacturer": "",
      "sys_updated_on": "2020-07-08 11:16:51",
      "discovery_source": "",
      "first_discovered": "",
      "due_in": "",
      "used_for": "Production",
      "invoice_number": "",
      "gl_account": "",
      "sys_created_by": "glide.maint",
      "warranty_expiration": "",
      "ram": "2048",
      "cpu_name": "",
      "cpu_speed": "2800",
      "owned_by": "",
      "checked_out": "",
      "kernel_release": "",
      "sys_domain_path": "/",
      "classification": "Production",
      "disk_space": "40",
      "object_id": "",
      "maintenance_schedule": "",
      "cost_center": "",
      "attested_by": "",
      "dns_domain": "",
      "assigned": "2020-01-04 07:00:00",
      "purchase_date": "",
      "life_cycle_stage": "",
      "short_description": "",
      "cd_speed": "",
      "floppy": "",
      "managed_by": {
        "display_value": "Lynda Caraway",
        "link": "https://instance.service-now.com/api/now/table/sys_user/8a826bf03710200044e0bfc8bcbe5d72",
        "value": "8a826bf03710200044e0bfc8bcbe5d72"
      },
      "os_domain": "",
      "last_discovered": "",
      "can_print": "false",
      "sys_class_name": "cmdb_ci_linux_server",
      "manufacturer": {
        "display_value": "Iris",
        "link": "https://instance.servicenow.com/api/now/table/core_company/c115c2f737e3100044e0bfc8bcbe5d46",
        "value": "c115c2f737e3100044e0bfc8bcbe5d46"
      },
      "cpu_count": "1",
      "vendor": {
        "display_value": "Cloudward Inc",
        "link": "https://instance.servicenow.com/api/now/table/core_company/3efe8c4c37423000158bbfc8bcbe5d7d",
        "value": "3efe8c4c37423000158bbfc8bcbe5d7d"
      },
      "life_cycle_stage_status": "",
      "model_number": "",
      "assigned_to": "",
      "start_date": "",
      "os_version": "2.6.9-22.0.1.ELsmp",
      "serial_number": "",
      "cd_rom": "false",
      "support_group": "",
      "unverified": "false",
      "correlation_id": "",
      "attributes": "",
      "asset": {
        "display_value": "P1000091 - Iris 5875",
        "link": "https://instance.servicenow.com/api/now/table/alm_asset/0bc1ba8837f3100044e0bfc8bcbe5dbb",
        "value": "0bc1ba8837f3100044e0bfc8bcbe5dbb"
      },
      "form_factor": "",
      "cpu_core_count": "",
      "skip_sync": "false",
      "attestation_score": "",
      "sys_updated_by": "system",
      "sys_created_on": "2008-10-26 17:17:28",
      "sys_domain": {
        "display_value": "global",
        "link": "https://instance.servicenow.com/api/now/table/sys_user_group/global",
        "value": "global"
      },
      "cpu_type": "Intel",
      "install_date": "2019-08-18 08:00:00",
      "asset_tag": "P1000091",
      "dr_backup": "",
      "hardware_substatus": "",
      "fqdn": "",
      "change_control": "",
      "internet_facing": "false",
      "delivery_date": "",
      "hardware_status": "",
      "install_status": "1",
      "supported_by": "",
      "name": "PS LinuxApp01",
      "subcategory": "",
      "default_gateway": "",
      "chassis_type": "",
      "virtual": "false",
      "assignment_group": "",
      "managed_by_group": "",
      "sys_id": "3a290cc60a0a0bb400000bdb386af1cf",
      "po_number": "",
      "checked_in": "",
      "sys_class_path": "/!!/!2/!(/!!/!0",
      "mac_address": "",
      "company": {
        "display_value": "ACME Corporation",
        "link": "https://instance.servicenow.com/api/now/table/core_company/e7c1f3d53790200044e0bfc8bcbe5deb",
        "value": "e7c1f3d53790200044e0bfc8bcbe5deb"
      },
      "justification": "",
      "department": "",
      "cost": "45557.5",
      "comments": "",
      "os": "Linux Red Hat",
      "sys_mod_count": "24",
      "monitor": "false",
      "model_id": {
        "display_value": "Iris 5875",
        "link": "https://instance.servicenow.com/api/now/table/cmdb_model/5f5fbcc3c0a8010e00f3b27814f3b96b",
        "value": "5f5fbcc3c0a8010e00f3b27814f3b96b"
      },
      "ip_address": "",
      "duplicate_of": "",
      "sys_tags": "",
      "cost_cc": "USD",
      "order_date": "",
      "schedule": "",
      "environment": "",
      "due": "",
      "attested": "false",
      "location": {
        "display_value": "322 West 52nd Street, New York,NY",
        "link": "https://instance.servicenow.com/api/now/table/cmn_location/25ab9f690a0a0bb3001c5fec1d0d7bcb",
        "value": "25ab9f690a0a0bb3001c5fec1d0d7bcb"
      },
      "category": "Do not migrate to asset",
      "fault_count": "0",
      "host_name": "",
      "lease_id": ""
    },
    "inbound_relations": [
      {
        "sys_id": "3a5e4d8ac0a8ce010005145afb730818",
        "type": {
          "display_value": "Depends on::Used by",
          "link": "https://instance.servicenow.com/api/now/table/cmdb_rel_type/1a9cb166f1571100a92eb60da2bce5c5",
          "value": "1a9cb166f1571100a92eb60da2bce5c5"
        },
        "target": {
          "display_value": "PS Apache01",
          "link": "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci/3a27d4370a0a0bb4006316812bf45439",
          "value": "3a27d4370a0a0bb4006316812bf45439"
        }
      },
      {
        "sys_id": "3a5e4d9cc0a8ce010097f2f5c2f65fd8",
        "type": {
          "display_value": "Depends on::Used by",
          "link": "https://instance.servicenow.com/api/now/table/cmdb_rel_type/1a9cb166f1571100a92eb60da2bce5c5",
          "value": "1a9cb166f1571100a92eb60da2bce5c5"
        },
        "target": {
          "display_value": "PS Apache02",
          "link": "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci/3a27f1520a0a0bb400ecd6ff7afcf036",
          "value": "3a27f1520a0a0bb400ecd6ff7afcf036"
        }
      },
      {
        "sys_id": "3a5e4d9fc0a8ce0100a3754fac26fe56",
        "type": {
          "display_value": "Depends on::Used by",
          "link": "https://instance.servicenow.com/api/now/table/cmdb_rel_type/1a9cb166f1571100a92eb60da2bce5c5",
          "value": "1a9cb166f1571100a92eb60da2bce5c5"
        },
        "target": {
          "display_value": "PS Apache03",
          "link": "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci/3a2810c20a0a0bb400268337d6e942ca",
          "value": "3a2810c20a0a0bb400268337d6e942ca"
        }
      }
    ]
  }
}
```

## CMDB Instance - POST /now/cmdb/instance/\{classname\}

Creates a single configuration item \(CI\) with the specified outbound and inbound relations within the specified Configuration Management Database \(CMDB\) table.

**Note:** If the CMDB class has a dependent identification rule defined, then the input payload must contain the sys\_id of an existing CI. For example, for **outbound\_relations**, the **target** parameter must contain the sys\_id of an existing CI, which then becomes the child. For **inbound\_relations**, it becomes the parent.

```

  "depends_on": {
    "outbound_relations":
      {
        "target": "b4fd7c8437201000deeabfc8bcbe5dc1",
        "type": "60bc4e22c0a8010e01f074cbe6bd73c3"
      }
    }
```

### URL format

Versioned URL: `/api/now/{api_version}/cmdb/instance/{className}`

Default URL: `/api/now/cmdb/instance/{className}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

className

</td><td id="entry-className-cmdb">

CMDB class name. This is the name of the table that contains the desired CI records, such as cmdb\_ci\_linux\_server or cmdb\_ci\_apache\_web\_server.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None||

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="entry-attributes-cmdb">

Data attributes to define in the CI record. The available attributes depend on the specified CMDB class. You can locate the available attributes in the associated CMDB table which typically begins with "cmdb\_ci", such as cmdb\_ci\_linux\_server or cmdb\_ci\_mfp\_printer.Data type: Object

</td></tr><tr><td>

inbound\_relations

</td><td id="entry-inbound_relations-cmdb">

List of objects that define the inbound relations to associate with the CI.Data type: Array

```
"inbound_relations": [
  {
    "target": "String",
    "type": "String"
  }
]
```

</td></tr><tr><td>

inbound\_relations.target

</td><td id="entry-inbound_relations_target-cmdb">

Required if **inbound\_relations** is specified. Sys\_id of the target inbound relation to associate with the specified CI. Located in the Configuration Item \[cmdb\_ci\] table. Data type: String

</td></tr><tr><td>

inbound\_relations.type

</td><td id="entry-inbound_relations_type-cmdb">

Required if **inbound\_relations** is specified. Sys\_id of the type of inbound relationship. Located in the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr><td>

outbound\_relations

</td><td>

List of objects that define the outbound relations to associate with the CI.Data type: Array

 ```
"outbound_relations": [
  {
    "target": "String",
    "type": "String"
  }
]
```

</td></tr><tr><td>

outbound\_relations.target

</td><td id="entry-request-outbound_relations_target-cmdb">

Required if **outbound\_relations** is specified. Sys\_id of the target outbound relation. Located in the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr><td>

outbound\_relations.type

</td><td id="entry-request-outbound_relations_type-cmdb">

Required if **outbound\_relations** is specified. Sys\_id of the type of outbound relationship. Located in the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr><td>

source

</td><td id="entry-source-cmdb">

Required. Entity that updated the information. This must be one of the choice values specified in the discovery\_source field in the Configuration Item \[cmdb\_ci\] table.Data type: String

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
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|405|Invalid method. The functionality is disabled.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_ags_gn4_3mb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td>

Data attributes currently in the CI record. The available attributes depend on the specified CMDB class. You can locate the available attributes in the associated CMDB table which typically begins with "cmdb\_ci", such as cmdb\_ci\_linux\_server or cmdb\_ci\_mfp\_printer.Data type: Object

</td></tr><tr id="row-result-error-cmdb"><td>

error

</td><td id="entry-result-error-cmdb">

Information on any errors encountered while processing the endpoint request. Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr id="row-result-error_detail-cmdb"><td>

error.detail

</td><td id="entry-result-error_detail-cmdb">

Additional information about the error.Data type: String

</td></tr><tr id="row-result-error_message-cmdb"><td>

error.message

</td><td id="entry-result-error_message-cmdb">

Message that identifies the error.Data type: String

</td></tr><tr id="row-result-inbound_relations-cmdb"><td>

inbound\_relations

</td><td id="entry-result-inbound_relations-cmdb">

List of objects that define the inbound relations associated with the CI.Data type: Array

```
"inbound_relations": [
  {
    "sys_id": "String",
    "target": {Object},
    "type": {Object}
  }
]
```

</td></tr><tr id="row-result-inbound_relations_sys_id-cmdb"><td>

inbound\_relations.sys\_id

</td><td id="entry-result-inbound_relations_sys_id-cmdb">

Sys\_id of the inbound CI relationship. Located in the CI Relationship \[cmdb\_rel\_ci\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_target-cmdb"><td>

inbound\_relations.target

</td><td id="entry-result-inbound_relations_target-cmdb">

Information that describes the target inbound relation.Data type: Object

```
"target": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-inbound_relations_target_display_value-cmdb"><td>

inbound\_relations.target.display\_value

</td><td id="entry-result-inbound_relations_target_display_value-cmdb">

Name of the inbound relation to display in a user interface.Data type: String

</td></tr><tr id="row-result-inbound_relations_target_link-cmdb"><td>

inbound\_relations.target.link

</td><td id="entry-result-inbound_relations_target_link-cmdb">

CMDB REST endpoint URL to use to retrieve the inbound relation from the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_target_value-cmdb"><td>

inbound\_relations.target.value

</td><td id="entry-result-inbound_relations_target_value-cmdb">

Sys\_id of the inbound CI. Located in the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_type-cmdb"><td>

inbound\_relations.type

</td><td id="entry-result-inbound_relations_type-cmdb">

Information about the type of inbound relationship. Data type: Object

```
"type": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-inbound_relations_type_display_value-cmdb"><td>

inbound\_relations.type.display\_value

</td><td id="entry-result-inbound_relations_type_display_value-cmdb">

Name of the inbound type to display in a user interface.Data type: String

</td></tr><tr id="row-result-inbound_relations_type_link-cmdb"><td>

inbound\_relations.type.link

</td><td id="entry-result-inbound_relations_type_link-cmdb">

Table REST endpoint URL to use to retrieve the inbound relation type from the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_type_value-cmdb"><td>

inbound\_relations.type.value

</td><td id="entry-result-inbound_relations_type_value-cmdb">

Sys\_id of the type of inbound relationship. Located in the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations-cmdb"><td>

outbound\_relations

</td><td id="entry-result-outbound_relations-cmdb">

List of objects that define the outbound relations associated with the CI.Data type: Array

```
"outbound_relations": [
  {
    "sys_id": "String",
    "target": {Object},
    "type": {Object}
  }
]
```

</td></tr><tr id="row-result-outbound_relations_sys_id-cmdb"><td>

outbound\_relations.sys\_id

</td><td id="entry-result-outbound_relations_sys_id-cmdb">

Sys\_id of the outbount CI relationship. Located in the CI Relationship \[cmdb\_rel\_ci\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_target-cmdb"><td>

outbound\_relations.target

</td><td id="entry-result-outbound_relations_target-cmdb">

Required. Information about the target outbound relation.Data type: Object

```
"target": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-outbound_relations_target_display_value-cmdb"><td>

outbound\_relations.target.display\_value

</td><td id="entry-result-outbound_relations_target_display_value-cmdb">

Name of the outbound relation to display in a user interface.Data type: String

</td></tr><tr id="row-result-outbound_relations_target_link-cmdb"><td>

outbound\_relations.target.link

</td><td id="entry-result-outbound_relations_target_link-cmdb">

CMDB REST endpoint URL to use to retrieve the outbound relation from the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_target_value-cmdb"><td>

outbound\_relations.target.value

</td><td id="entry-result-outbound_relations_target_value-cmdb">

Sys\_id of the outbound CI. Located in the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_type-cmdb"><td>

outbound\_relations.type

</td><td id="entry-result-outbound_relations_type-cmdb">

Information about the type of outbound relationship. Data type: Object

```
"type": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-outbound_relations_type_display_value-cmdb"><td>

outbound\_relations.type.display\_value

</td><td id="entry-result-outbound_relations_type_display_value-cmdb">

Name of the outbound type to display in a user interface.Data type: String

</td></tr><tr id="row-result-outbound_relations_type_link-cmdb"><td>

outbound\_relations.type.link

</td><td id="entry-result-outbound_relations_type_link-cmdb">

Table REST endpoint URL to use to retrieve the outbound relation from the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_type_value-cmdb"><td>

outbound\_relations.type.value

</td><td id="entry-result-outbound_relations_type_value-cmdb">

Sys\_id of the type of outbound relationship. Located in the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-status-cmdb"><td>

status

</td><td id="entry-result-status-cmdb">

Only appears if an error is encountered. Status of the endpoint processing.Possible value: failure

Data type: String

</td></tr></tbody>
</table>### cURL Request

The following code example shows how to call this endpoint.

```
curl "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci_linux_server" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json"\
--user "username":"password" \
--data {
  "outbound_relations": [
    {
      "type" : "1a9cb166f1571100a92eb60da2bce5c5",
      "target" : "3a307c930a0a0bb400353965d0b8861f"
    },
    {
      "type" : "607ad1b2c0a8010e01941856b365af90",
      "target" : "3a307c930a0a0bb400353965d0b8861f"
    }
  ],
  "attributes": {
    "name" : "lnux999",
    "firewall_status": "Intranet"
  },
  "source": "ServiceNow",
  "inbound_relations": [
    {
      "type" : "1a9cb166f1571100a92eb60da2bce5c5",
      "target" : "3a27d4370a0a0bb4006316812bf45439"
    }
  ]
}
```

```
{
    "result": {
        "outbound_relations": [
            {
                "sys_id": "403ff2641b425010593876a61a4bcb4b",
                "type": {
                    "display_value": "Depends on::Used by",
                    "link": "https://instance.servicenow.com/api/now/table/cmdb_rel_type/1a9cb166f1571100a92eb60da2bce5c5",
                    "value": "1a9cb166f1571100a92eb60da2bce5c5"
                },
                "target": {
                    "display_value": "PS ORA01",
                    "link": "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci/3a307c930a0a0bb400353965d0b8861f",
                    "value": "3a307c930a0a0bb400353965d0b8861f"
                }
            },
            {
                "sys_id": "443ff2641b425010593876a61a4bcb4c",
                "type": {
                    "display_value": "Exchanges data with::Exchanges data with",
                    "link": "https://instance.servicenow.com/api/now/table/cmdb_rel_type/607ad1b2c0a8010e01941856b365af90",
                    "value": "607ad1b2c0a8010e01941856b365af90"
                },
                "target": {
                    "display_value": "PS ORA01",
                    "link": "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci/3a307c930a0a0bb400353965d0b8861f",
                    "value": "3a307c930a0a0bb400353965d0b8861f"
                }
            }
        ],
        "attributes": {
            "firewall_status": "Intranet",
            "os_address_width": "",
            "attested_date": "",
            "operational_status": "1",
            "os_service_pack": "",
            "cpu_core_thread": "",
            "cpu_manufacturer": "",
            "sys_updated_on": "2020-07-13 20:27:28",
            "discovery_source": "ServiceNow",
            "first_discovered": "2020-07-13 20:27:28",
            "due_in": "",
            "used_for": "Production",
            "invoice_number": "",
            "gl_account": "",
            "sys_created_by": "dora.gray",
            "warranty_expiration": "",
            "ram": "",
            "cpu_name": "",
            "cpu_speed": "",
            "owned_by": "",
            "checked_out": "",
            "kernel_release": "",
            "sys_domain_path": "/",
            "classification": "Production",
            "disk_space": "",
            "object_id": "",
            "maintenance_schedule": "",
            "cost_center": "",
            "attested_by": "",
            "dns_domain": "",
            "assigned": "",
            "purchase_date": "",
            "life_cycle_stage": "",
            "short_description": "",
            "cd_speed": "",
            "floppy": "",
            "managed_by": "",
            "os_domain": "",
            "last_discovered": "2020-07-13 20:27:28",
            "can_print": "false",
            "sys_class_name": "cmdb_ci_linux_server",
            "manufacturer": "",
            "cpu_count": "",
            "vendor": "",
            "life_cycle_stage_status": "",
            "model_number": "",
            "assigned_to": "",
            "start_date": "",
            "os_version": "",
            "serial_number": "",
            "cd_rom": "false",
            "support_group": "",
            "unverified": "false",
            "correlation_id": "",
            "attributes": "",
            "asset": "",
            "form_factor": "",
            "cpu_core_count": "",
            "skip_sync": "false",
            "attestation_score": "",
            "sys_updated_by": "dora.gray",
            "sys_created_on": "2020-07-13 20:27:28",
            "sys_domain": {
                "display_value": "global",
                "link": "https://instance.servicenow.com/api/now/table/sys_user_group/global",
                "value": "global"
            },
            "cpu_type": "",
            "install_date": "",
            "asset_tag": "",
            "dr_backup": "",
            "hardware_substatus": "",
            "fqdn": "",
            "change_control": "",
            "internet_facing": "true",
            "delivery_date": "",
            "hardware_status": "installed",
            "install_status": "1",
            "supported_by": "",
            "name": "lnux299",
            "subcategory": "Computer",
            "default_gateway": "",
            "chassis_type": "",
            "virtual": "false",
            "assignment_group": "",
            "managed_by_group": "",
            "sys_id": "0c3ff2641b425010593876a61a4bcb39",
            "po_number": "",
            "checked_in": "",
            "sys_class_path": "/!!/!2/!(/!!/!0",
            "mac_address": "",
            "company": "",
            "justification": "",
            "department": "",
            "cost": "",
            "comments": "",
            "os": "",
            "sys_mod_count": "0",
            "monitor": "false",
            "model_id": "",
            "ip_address": "",
            "duplicate_of": "",
            "sys_tags": "",
            "cost_cc": "USD",
            "order_date": "",
            "schedule": "",
            "environment": "",
            "due": "",
            "attested": "false",
            "location": "",
            "category": "Hardware",
            "fault_count": "0",
            "host_name": "",
            "lease_id": ""
        },
        "inbound_relations": [
            {
                "sys_id": "c03ff2641b425010593876a61a4bcb49",
                "type": {
                    "display_value": "Depends on::Used by",
                    "link": "https://instance.servicenow.com/api/now/table/cmdb_rel_type/1a9cb166f1571100a92eb60da2bce5c5",
                    "value": "1a9cb166f1571100a92eb60da2bce5c5"
                },
                "target": {
                    "display_value": "PS Apache01",
                    "link": "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci/3a27d4370a0a0bb4006316812bf45439",
                    "value": "3a27d4370a0a0bb4006316812bf45439"
                }
            }
        ]
    }
}
```

### cURL Request

The following code example shows how to call this endpoint for a class that has a dependant identification rule defined. The **outbound\_relations.target** must be included in the payload and contain the sys\_id of an existing CI.

```
curl "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci_linux_server" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json"\
--user "username":"password" \
--data {
  "attributes": {
    "name": "test",
    "sys_class_name":"cmdb_ci_db_mssql_instance",
    "instance_name":"Iname"
  },
  "source": "ServiceNow",
  "depends_on": {
    "outbound_relations":
      {
        "target": "b4fd7c8437201000deeabfc8bcbe5dc1",
        "type": "60bc4e22c0a8010e01f074cbe6bd73c3"
      }
    }
  }
}
```

```
{
  "result": {
    "outbound_relations": [
      {
        "sys_id": "505cfa3a53662110af64ddeeff7b1217",
        "type": {
          "display_value": "Runs on::Runs",
          "link": http://instance.servicenow.com/api/now/table/cmdb_rel_type/60bc4e22c0a8010e01f074cbe6bd73c3,
          "value": "60bc4e22c0a8010e01f074cbe6bd73c3"
        },
        "target": {
          "display_value": "*ANNIE-IBM",
          "link": http://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci/b4fd7c8437201000deeabfc8bcbe5dc1,
          "value": "b4fd7c8437201000deeabfc8bcbe5dc1"
        }
      }
    ],
    "attributes": {
      "attested_date": "",
      "operational_status": "1",
      "running_process_command": "",
      "sys_updated_on": "2023-05-05 21:28:24",
      "type": "",
      "running_process_key_parameters": "",
      "rp_command_hash": "",
      "discovery_source": "ServiceNow",
      "first_discovered": "2023-05-05 21:28:24",
      "due_in": "",
      "service_pack": "",
      "used_for": "Production",
      "is_clustered": "false",
      "invoice_number": "",
      "gl_account": "",
      "sys_created_by": "admin",
      "warranty_expiration": "",
      "owned_by": "",
      "checked_out": "",
      "rp_key_parameters_hash": "",
      "sys_domain_path": "/",
      "business_unit": "",
      "version": "",
      "cpu_sockets": "",
      "maintenance_schedule": "",
      "cost_center": "",
      "attested_by": "",
      "dns_domain": "",
      "assigned": "",
      "purchase_date": "",
      "life_cycle_stage": "",
      "short_description": "",
      "managed_by": "",
      "port_dynamic": "false",
      "last_discovered": "2023-05-05 21:28:24",
      "can_print": "false",
      "sys_class_name": "cmdb_ci_db_mssql_instance",
      "manufacturer": "",
      "cl_port": "",
      "vendor": "",
      "life_cycle_stage_status": "",
      "model_number": "",
      "config_file": "",
      "assigned_to": "",
      "start_date": "",
      "instance_name": "Iname",
      "serial_number": "",
      "engine_edition": "",
      "support_group": "",
      "version_name": "",
      "unverified": "false",
      "correlation_id": "",
      "attributes": "",
      "asset": "",
      "config_directory": "",
      "tcp_port": "",
      "listener_name": "",
      "skip_sync": "false",
      "pid": "",
      "attestation_score": "",
      "sys_updated_by": "admin",
      "install_directory": "",
      "sys_created_on": "2023-05-05 21:28:24",
      "sys_domain": {
        "display_value": "global",
        "link": http://instance.servicenow.com/api/now/table/sys_user_group/global,
        "value": "global"
      },
      "install_date": "",
      "asset_tag": "",
      "fqdn": "",
      "change_control": "",
      "delivery_date": "",
      "install_status": "1",
      "supported_by": "",
      "name": "test",
      "subcategory": "Database",
      "assignment_group": "",
      "edition": "",
      "managed_by_group": "",
      "sys_id": "185cba3a53662110af64ddeeff7b12af",
      "po_number": "",
      "database": "",
      "checked_in": "",
      "sys_class_path": "/!!/!(/!2/!,",
      "mac_address": "",
      "company": "",
      "justification": "",
      "department": "",
      "cost": "",
      "comments": "",
      "attestation_status": "Not Yet Reviewed",
      "sys_mod_count": "0",
      "monitor": "false",
      "model_id": "",
      "ip_address": "",
      "duplicate_of": "",
      "sys_tags": "",
      "cost_cc": "USD",
      "order_date": "",
      "schedule": "",
      "environment": "",
      "due": "",
      "attested": "false",
      "location": "",
      "category": "Resource",
      "fault_count": "0",
      "lease_id": ""
    },
    "inbound_relations": []
  }
}
```

### cURL Request

The following code example shows what is returned when a sys\_id is not passed for a class that has a dependant identification rule defined. Same result occurs if the sys\_id is invalid.

```
curl "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci_linux_server" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json"\
--user "username":"password" \
--data "{
  "attributes": {
    "name": "test",
    "sys_class_name":"cmdb_ci_db_mssql_instance",
    "instance_name":"Iname"
  },
  "source": "ServiceNow",
  "depends_on": {
    "outbound_relations": {
        "type": "60bc4e22c0a8010e01f074cbe6bd73c3"
    }
  }
}
```

```
{
  "error": {
    "detail": "Exception while executing request: null Check logs for error trace or enable glide.rest.debug property to verify REST request processing",
    "message": "Exception while executing request: null"
  },
  "status": "failure"
}
```

## CMDB Instance - PUT /now/cmdb/instance/\{classname\}/\{sys\_id\}

Updates the specified configuration item \(CI\) record with the specified attribute name-value pairs. This endpoint does not create, update, or delete the associated relations.

**Note:** This endpoint does not conform to the HTML specifications. Standard PUT endpoints are destructive in that they remove any elements that are not included in the request. This endpoint does not remove non-specified elements.

### URL format

Versioned URL: `/api/now/{api_version}/cmdb/instance/{className}/{sys_id}`

Default URL: `/api/now/cmdb/instance/{className}/{sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

className

</td><td id="entry-className-cmdb">

CMDB class name. This is the name of the table that contains the desired CI records, such as cmdb\_ci\_linux\_server or cmdb\_ci\_apache\_web\_server.Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="entry-sys_id-cmdb">

Sys\_id of the CI record to update.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None||

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="entry-attributes-cmdb">

Data attributes to replace in the CI record. The available attributes depend on the specified CMDB class. You can locate the available attributes in the associated CMDB table which typically begins with "cmdb\_ci", such as cmdb\_ci\_linux\_server or cmdb\_ci\_mfp\_printer.For information about attestation, see [CIs attestation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/attesting-cis.md).

Data type: Object

</td></tr><tr><td>

source

</td><td id="entry-source-cmdb">

Required. Entity that updated the information. This must be one of the choice values specified in the discovery\_source field in the Configuration Item \[cmdb\_ci\] table.Data type: String

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
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|405|Invalid method. The functionality is disabled.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_ens_hq4_3mb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td>

Data attributes currently in the CI record. The available attributes depend on the specified CMDB class. You can locate the available attributes in the associated CMDB table which typically begins with "cmdb\_ci", such as cmdb\_ci\_linux\_server or cmdb\_ci\_mfp\_printer.Data type: Object

</td></tr><tr id="row-result-error-cmdb"><td>

error

</td><td id="entry-result-error-cmdb">

Information on any errors encountered while processing the endpoint request. Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr id="row-result-error_detail-cmdb"><td>

error.detail

</td><td id="entry-result-error_detail-cmdb">

Additional information about the error.Data type: String

</td></tr><tr id="row-result-error_message-cmdb"><td>

error.message

</td><td id="entry-result-error_message-cmdb">

Message that identifies the error.Data type: String

</td></tr><tr id="row-result-inbound_relations-cmdb"><td>

inbound\_relations

</td><td id="entry-result-inbound_relations-cmdb">

List of objects that define the inbound relations associated with the CI.Data type: Array

```
"inbound_relations": [
  {
    "sys_id": "String",
    "target": {Object},
    "type": {Object}
  }
]
```

</td></tr><tr id="row-result-inbound_relations_sys_id-cmdb"><td>

inbound\_relations.sys\_id

</td><td id="entry-result-inbound_relations_sys_id-cmdb">

Sys\_id of the inbound CI relationship. Located in the CI Relationship \[cmdb\_rel\_ci\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_target-cmdb"><td>

inbound\_relations.target

</td><td id="entry-result-inbound_relations_target-cmdb">

Information that describes the target inbound relation.Data type: Object

```
"target": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-inbound_relations_target_display_value-cmdb"><td>

inbound\_relations.target.display\_value

</td><td id="entry-result-inbound_relations_target_display_value-cmdb">

Name of the inbound relation to display in a user interface.Data type: String

</td></tr><tr id="row-result-inbound_relations_target_link-cmdb"><td>

inbound\_relations.target.link

</td><td id="entry-result-inbound_relations_target_link-cmdb">

CMDB REST endpoint URL to use to retrieve the inbound relation from the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_target_value-cmdb"><td>

inbound\_relations.target.value

</td><td id="entry-result-inbound_relations_target_value-cmdb">

Sys\_id of the inbound CI. Located in the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_type-cmdb"><td>

inbound\_relations.type

</td><td id="entry-result-inbound_relations_type-cmdb">

Information about the type of inbound relationship. Data type: Object

```
"type": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-inbound_relations_type_display_value-cmdb"><td>

inbound\_relations.type.display\_value

</td><td id="entry-result-inbound_relations_type_display_value-cmdb">

Name of the inbound type to display in a user interface.Data type: String

</td></tr><tr id="row-result-inbound_relations_type_link-cmdb"><td>

inbound\_relations.type.link

</td><td id="entry-result-inbound_relations_type_link-cmdb">

Table REST endpoint URL to use to retrieve the inbound relation type from the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_type_value-cmdb"><td>

inbound\_relations.type.value

</td><td id="entry-result-inbound_relations_type_value-cmdb">

Sys\_id of the type of inbound relationship. Located in the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations-cmdb"><td>

outbound\_relations

</td><td id="entry-result-outbound_relations-cmdb">

List of objects that define the outbound relations associated with the CI.Data type: Array

```
"outbound_relations": [
  {
    "sys_id": "String",
    "target": {Object},
    "type": {Object}
  }
]
```

</td></tr><tr id="row-result-outbound_relations_sys_id-cmdb"><td>

outbound\_relations.sys\_id

</td><td id="entry-result-outbound_relations_sys_id-cmdb">

Sys\_id of the outbount CI relationship. Located in the CI Relationship \[cmdb\_rel\_ci\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_target-cmdb"><td>

outbound\_relations.target

</td><td id="entry-result-outbound_relations_target-cmdb">

Required. Information about the target outbound relation.Data type: Object

```
"target": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-outbound_relations_target_display_value-cmdb"><td>

outbound\_relations.target.display\_value

</td><td id="entry-result-outbound_relations_target_display_value-cmdb">

Name of the outbound relation to display in a user interface.Data type: String

</td></tr><tr id="row-result-outbound_relations_target_link-cmdb"><td>

outbound\_relations.target.link

</td><td id="entry-result-outbound_relations_target_link-cmdb">

CMDB REST endpoint URL to use to retrieve the outbound relation from the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_target_value-cmdb"><td>

outbound\_relations.target.value

</td><td id="entry-result-outbound_relations_target_value-cmdb">

Sys\_id of the outbound CI. Located in the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_type-cmdb"><td>

outbound\_relations.type

</td><td id="entry-result-outbound_relations_type-cmdb">

Information about the type of outbound relationship. Data type: Object

```
"type": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-outbound_relations_type_display_value-cmdb"><td>

outbound\_relations.type.display\_value

</td><td id="entry-result-outbound_relations_type_display_value-cmdb">

Name of the outbound type to display in a user interface.Data type: String

</td></tr><tr id="row-result-outbound_relations_type_link-cmdb"><td>

outbound\_relations.type.link

</td><td id="entry-result-outbound_relations_type_link-cmdb">

Table REST endpoint URL to use to retrieve the outbound relation from the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_type_value-cmdb"><td>

outbound\_relations.type.value

</td><td id="entry-result-outbound_relations_type_value-cmdb">

Sys\_id of the type of outbound relationship. Located in the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-status-cmdb"><td>

status

</td><td id="entry-result-status-cmdb">

Only appears if an error is encountered. Status of the endpoint processing.Possible value: failure

Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci_linux_server/70bc4e11c0a8210d01f074cbe6bd73b4" \
--request PUT \
--header "Accept:application/json" \
--header "Content-Type:application/json"\
--user "username":"password" \
--data {
  "attributes": {
    "firewall_status": "Extranet",
    "discovery_source": "ServiceNows",
    "name": "Linux299",
    "used_for": "Pre-production",
    "container": "Box"
  },
  "source": "ServiceNow"
}

```

```
{
    "result": {
        "outbound_relations": [
            {
                "sys_id": "403ff2641b425010593876a61a4bcb4b",
                "type": {
                    "display_value": "Depends on::Used by",
                    "link": "https://instance.service-now.com/api/now/table/cmdb_rel_type/1a9cb166f1571100a92eb60da2bce5c5",
                    "value": "1a9cb166f1571100a92eb60da2bce5c5"
                },
                "target": {
                    "display_value": "PS ORA01",
                    "link": "https://instance.service-now.com/api/now/cmdb/instance/cmdb_ci/3a307c930a0a0bb400353965d0b8861f",
                    "value": "3a307c930a0a0bb400353965d0b8861f"
                }
            },
            {
                "sys_id": "443ff2641b425010593876a61a4bcb4c",
                "type": {
                    "display_value": "Exchanges data with::Exchanges data with",
                    "link": "https://instance.service-now.com/api/now/table/cmdb_rel_type/607ad1b2c0a8010e01941856b365af90",
                    "value": "607ad1b2c0a8010e01941856b365af90"
                },
                "target": {
                    "display_value": "PS ORA01",
                    "link": "https://instance.service-now.com/api/now/cmdb/instance/cmdb_ci/3a307c930a0a0bb400353965d0b8861f",
                    "value": "3a307c930a0a0bb400353965d0b8861f"
                }
            }
        ],
        "attributes": {
            "firewall_status": "Extranet",
            "os_address_width": "",
            "attested_date": "",
            "operational_status": "1",
            "os_service_pack": "",
            "cpu_core_thread": "",
            "cpu_manufacturer": "",
            "sys_updated_on": "2020-07-13 20:59:40",
            "discovery_source": "ServiceNow",
            "first_discovered": "2020-07-13 20:27:28",
            "due_in": "",
            "used_for": "Pre-production",
            "invoice_number": "",
            "gl_account": "",
            "sys_created_by": "dora.gray",
            "warranty_expiration": "",
            "ram": "",
            "cpu_name": "",
            "cpu_speed": "",
            "owned_by": "",
            "checked_out": "",
            "kernel_release": "",
            "sys_domain_path": "/",
            "classification": "Production",
            "disk_space": "",
            "object_id": "",
            "maintenance_schedule": "",
            "cost_center": "",
            "attested_by": "",
            "dns_domain": "",
            "assigned": "",
            "purchase_date": "",
            "life_cycle_stage": "",
            "short_description": "",
            "cd_speed": "",
            "floppy": "",
            "managed_by": "",
            "os_domain": "",
            "last_discovered": "2020-07-13 20:59:40",
            "can_print": "false",
            "sys_class_name": "cmdb_ci_linux_server",
            "manufacturer": "",
            "cpu_count": "",
            "vendor": "",
            "life_cycle_stage_status": "",
            "model_number": "",
            "assigned_to": "",
            "start_date": "",
            "os_version": "",
            "serial_number": "",
            "cd_rom": "false",
            "support_group": "",
            "unverified": "false",
            "correlation_id": "",
            "attributes": "",
            "asset": {
                "display_value": "Unknown",
                "link": "https://instance.service-now.com/api/now/table/alm_asset/21cfba641b425010593876a61a4bcb52",
                "value": "21cfba641b425010593876a61a4bcb52"
            },
            "form_factor": "",
            "cpu_core_count": "",
            "skip_sync": "false",
            "attestation_score": "",
            "sys_updated_by": "dora.gray",
            "sys_created_on": "2020-07-13 20:27:28",
            "sys_domain": {
                "display_value": "global",
                "link": "https://instance.service-now.com/api/now/table/sys_user_group/global",
                "value": "global"
            },
            "cpu_type": "",
            "install_date": "",
            "asset_tag": "",
            "dr_backup": "",
            "hardware_substatus": "",
            "fqdn": "",
            "change_control": "",
            "internet_facing": "true",
            "delivery_date": "",
            "hardware_status": "installed",
            "install_status": "1",
            "supported_by": "",
            "name": "Linux299",
            "subcategory": "Computer",
            "default_gateway": "",
            "chassis_type": "",
            "virtual": "false",
            "assignment_group": "",
            "managed_by_group": "",
            "sys_id": "0c3ff2641b425010593876a61a4bcb39",
            "po_number": "",
            "checked_in": "",
            "sys_class_path": "/!!/!2/!(/!!/!0",
            "mac_address": "",
            "company": "",
            "justification": "",
            "department": "",
            "cost": "",
            "comments": "",
            "os": "",
            "sys_mod_count": "3",
            "monitor": "false",
            "model_id": {
                "display_value": "Unknown",
                "link": "https://instance.service-now.com/api/now/table/cmdb_model/0ce0a2681b4e1010593876a61a4bcba6",
                "value": "0ce0a2681b4e1010593876a61a4bcba6"
            },
            "ip_address": "",
            "duplicate_of": "",
            "sys_tags": "",
            "cost_cc": "USD",
            "order_date": "",
            "schedule": "",
            "environment": "",
            "due": "",
            "attested": "false",
            "location": "",
            "category": "Hardware",
            "fault_count": "0",
            "host_name": "",
            "lease_id": ""
        },
        "inbound_relations": [
            {
                "sys_id": "c03ff2641b425010593876a61a4bcb49",
                "type": {
                    "display_value": "Depends on::Used by",
                    "link": "https://instance.service-now.com/api/now/table/cmdb_rel_type/1a9cb166f1571100a92eb60da2bce5c5",
                    "value": "1a9cb166f1571100a92eb60da2bce5c5"
                },
                "target": {
                    "display_value": "PS Apache01",
                    "link": "https://instance.service-now.com/api/now/cmdb/instance/cmdb_ci/3a27d4370a0a0bb4006316812bf45439",
                    "value": "3a27d4370a0a0bb4006316812bf45439"
                }
            }
        ]
    }
}
```

## CMDB Instance - POST /now/cmdb/instance/\{classname\}/\{sys\_id\}/relation

Adds an inbound and/or outbound relation to the specified configuration item \(CI\). The specified CI is the parent.

### URL format

Versioned URL: `/api/now/{api_version}/cmdb/instance/{className}/{sys_id}/relation`

Default URL: `/api/now/cmdb/instance/{className}/{sys_id}/relation`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

className

</td><td id="entry-className-cmdb">

CMDB class name. This is the name of the table that contains the desired CI records, such as cmdb\_ci\_linux\_server or cmdb\_ci\_apache\_web\_server.Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="entry-sys_id-cmdb">

Sys\_id of the CI record to update.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None||

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

inbound\_relations

</td><td id="entry-inbound_relations-cmdb">

List of objects that define the inbound relations to associate with the CI.Data type: Array

```
"inbound_relations": [
  {
    "target": "String",
    "type": "String"
  }
]
```

</td></tr><tr><td>

inbound\_relations.target

</td><td id="entry-inbound_relations_target-cmdb">

Required if **inbound\_relations** is specified. Sys\_id of the target inbound relation to associate with the specified CI. Located in the Configuration Item \[cmdb\_ci\] table. Data type: String

</td></tr><tr><td>

inbound\_relations.type

</td><td id="entry-inbound_relations_type-cmdb">

Required if **inbound\_relations** is specified. Sys\_id of the type of inbound relationship. Located in the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr><td>

outbound\_relations

</td><td id="entry-outbound_relations-cmdb">

List of objects that define the outbound relations to associate with the CI.Data type: Array

```
"outbound_relations": [
  {
    "target": "String",
    "type": "String"
  }
]
```

</td></tr><tr><td>

outbound\_relations.target

</td><td id="entry-request-outbound_relations_target-cmdb">

Required if **outbound\_relations** is specified. Sys\_id of the target outbound relation. Located in the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr><td>

outbound\_relations.type

</td><td id="entry-request-outbound_relations_type-cmdb">

Required if **outbound\_relations** is specified. Sys\_id of the type of outbound relationship. Located in the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr><td>

source

</td><td id="entry-source-cmdb">

Required. Entity that updated the information. This must be one of the choice values specified in the discovery\_source field in the Configuration Item \[cmdb\_ci\] table.Data type: String

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
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|405|Invalid method. The functionality is disabled.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_hj2_qn4_3mb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td>

Data attributes currently in the CI record. The available attributes depend on the specified CMDB class. You can locate the available attributes in the associated CMDB table which typically begins with "cmdb\_ci", such as cmdb\_ci\_linux\_server or cmdb\_ci\_mfp\_printer.Data type: Object

</td></tr><tr id="row-result-error-cmdb"><td>

error

</td><td id="entry-result-error-cmdb">

Information on any errors encountered while processing the endpoint request. Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr id="row-result-error_detail-cmdb"><td>

error.detail

</td><td id="entry-result-error_detail-cmdb">

Additional information about the error.Data type: String

</td></tr><tr id="row-result-error_message-cmdb"><td>

error.message

</td><td id="entry-result-error_message-cmdb">

Message that identifies the error.Data type: String

</td></tr><tr id="row-result-inbound_relations-cmdb"><td>

inbound\_relations

</td><td id="entry-result-inbound_relations-cmdb">

List of objects that define the inbound relations associated with the CI.Data type: Array

```
"inbound_relations": [
  {
    "sys_id": "String",
    "target": {Object},
    "type": {Object}
  }
]
```

</td></tr><tr id="row-result-inbound_relations_sys_id-cmdb"><td>

inbound\_relations.sys\_id

</td><td id="entry-result-inbound_relations_sys_id-cmdb">

Sys\_id of the inbound CI relationship. Located in the CI Relationship \[cmdb\_rel\_ci\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_target-cmdb"><td>

inbound\_relations.target

</td><td id="entry-result-inbound_relations_target-cmdb">

Information that describes the target inbound relation.Data type: Object

```
"target": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-inbound_relations_target_display_value-cmdb"><td>

inbound\_relations.target.display\_value

</td><td id="entry-result-inbound_relations_target_display_value-cmdb">

Name of the inbound relation to display in a user interface.Data type: String

</td></tr><tr id="row-result-inbound_relations_target_link-cmdb"><td>

inbound\_relations.target.link

</td><td id="entry-result-inbound_relations_target_link-cmdb">

CMDB REST endpoint URL to use to retrieve the inbound relation from the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_target_value-cmdb"><td>

inbound\_relations.target.value

</td><td id="entry-result-inbound_relations_target_value-cmdb">

Sys\_id of the inbound CI. Located in the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_type-cmdb"><td>

inbound\_relations.type

</td><td id="entry-result-inbound_relations_type-cmdb">

Information about the type of inbound relationship. Data type: Object

```
"type": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-inbound_relations_type_display_value-cmdb"><td>

inbound\_relations.type.display\_value

</td><td id="entry-result-inbound_relations_type_display_value-cmdb">

Name of the inbound type to display in a user interface.Data type: String

</td></tr><tr id="row-result-inbound_relations_type_link-cmdb"><td>

inbound\_relations.type.link

</td><td id="entry-result-inbound_relations_type_link-cmdb">

Table REST endpoint URL to use to retrieve the inbound relation type from the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_type_value-cmdb"><td>

inbound\_relations.type.value

</td><td id="entry-result-inbound_relations_type_value-cmdb">

Sys\_id of the type of inbound relationship. Located in the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations-cmdb"><td>

outbound\_relations

</td><td id="entry-result-outbound_relations-cmdb">

List of objects that define the outbound relations associated with the CI.Data type: Array

```
"outbound_relations": [
  {
    "sys_id": "String",
    "target": {Object},
    "type": {Object}
  }
]
```

</td></tr><tr id="row-result-outbound_relations_sys_id-cmdb"><td>

outbound\_relations.sys\_id

</td><td id="entry-result-outbound_relations_sys_id-cmdb">

Sys\_id of the outbount CI relationship. Located in the CI Relationship \[cmdb\_rel\_ci\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_target-cmdb"><td>

outbound\_relations.target

</td><td id="entry-result-outbound_relations_target-cmdb">

Required. Information about the target outbound relation.Data type: Object

```
"target": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-outbound_relations_target_display_value-cmdb"><td>

outbound\_relations.target.display\_value

</td><td id="entry-result-outbound_relations_target_display_value-cmdb">

Name of the outbound relation to display in a user interface.Data type: String

</td></tr><tr id="row-result-outbound_relations_target_link-cmdb"><td>

outbound\_relations.target.link

</td><td id="entry-result-outbound_relations_target_link-cmdb">

CMDB REST endpoint URL to use to retrieve the outbound relation from the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_target_value-cmdb"><td>

outbound\_relations.target.value

</td><td id="entry-result-outbound_relations_target_value-cmdb">

Sys\_id of the outbound CI. Located in the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_type-cmdb"><td>

outbound\_relations.type

</td><td id="entry-result-outbound_relations_type-cmdb">

Information about the type of outbound relationship. Data type: Object

```
"type": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-outbound_relations_type_display_value-cmdb"><td>

outbound\_relations.type.display\_value

</td><td id="entry-result-outbound_relations_type_display_value-cmdb">

Name of the outbound type to display in a user interface.Data type: String

</td></tr><tr id="row-result-outbound_relations_type_link-cmdb"><td>

outbound\_relations.type.link

</td><td id="entry-result-outbound_relations_type_link-cmdb">

Table REST endpoint URL to use to retrieve the outbound relation from the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_type_value-cmdb"><td>

outbound\_relations.type.value

</td><td id="entry-result-outbound_relations_type_value-cmdb">

Sys\_id of the type of outbound relationship. Located in the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-status-cmdb"><td>

status

</td><td id="entry-result-status-cmdb">

Only appears if an error is encountered. Status of the endpoint processing.Possible value: failure

Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci_linux_server/3a290cc60a0a0bb400000bdb386af1cf/relation" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json"\
--user "username":"password" \
--data {
  "outbound_relations": [
    {
      "type" : "1a9cb166f1571100a92eb60da2bce5c5",
      "target" : "3a307c930a0a0bb400353965d0b8861f"
    },
    {
      "type" : "607ad1b2c0a8010e01941856b365af90",
      "target" : "3a307c930a0a0bb400353965d0b8861f"
    }
  ],
  "source": "ServiceNow",
  "inbound_relations": [
    {
      "type" : "1a9cb166f1571100a92eb60da2bce5c5",
      "target" : "3a27d4370a0a0bb4006316812bf45439"
    }
  ]
}
```

```
{
    "result": {
        "outbound_relations": [
            {
                "sys_id": "403ff2641b425010593876a61a4bcb4b",
                "type": {
                    "display_value": "Depends on::Used by",
                    "link": "https://instance.servicenow.com/api/now/table/cmdb_rel_type/1a9cb166f1571100a92eb60da2bce5c5",
                    "value": "1a9cb166f1571100a92eb60da2bce5c5"
                },
                "target": {
                    "display_value": "PS ORA01",
                    "link": "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci/3a307c930a0a0bb400353965d0b8861f",
                    "value": "3a307c930a0a0bb400353965d0b8861f"
                }
            },
            {
                "sys_id": "443ff2641b425010593876a61a4bcb4c",
                "type": {
                    "display_value": "Exchanges data with::Exchanges data with",
                    "link": "https://instance.servicenow.com/api/now/table/cmdb_rel_type/607ad1b2c0a8010e01941856b365af90",
                    "value": "607ad1b2c0a8010e01941856b365af90"
                },
                "target": {
                    "display_value": "PS ORA01",
                    "link": "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci/3a307c930a0a0bb400353965d0b8861f",
                    "value": "3a307c930a0a0bb400353965d0b8861f"
                }
            }
        ],
        "attributes": {
            "firewall_status": "Active",
            "os_address_width": "",
            "attested_date": "",
            "operational_status": "1",
            "os_service_pack": "",
            "cpu_core_thread": "",
            "cpu_manufacturer": "",
            "sys_updated_on": "2020-07-13 21:24:05",
            "discovery_source": "ServiceNow",
            "first_discovered": "2020-07-13 20:27:28",
            "due_in": "",
            "used_for": "Production",
            "invoice_number": "",
            "gl_account": "",
            "sys_created_by": "dora.gray",
            "warranty_expiration": "",
            "ram": "",
            "cpu_name": "",
            "cpu_speed": "",
            "owned_by": "",
            "checked_out": "",
            "kernel_release": "",
            "sys_domain_path": "/",
            "classification": "Production",
            "disk_space": "",
            "object_id": "",
            "maintenance_schedule": "",
            "cost_center": "",
            "attested_by": "",
            "dns_domain": "",
            "assigned": "",
            "purchase_date": "",
            "life_cycle_stage": "",
            "short_description": "",
            "cd_speed": "",
            "floppy": "",
            "managed_by": "",
            "os_domain": "",
            "last_discovered": "2020-07-13 21:24:05",
            "can_print": "false",
            "sys_class_name": "cmdb_ci_linux_server",
            "manufacturer": "",
            "cpu_count": "",
            "vendor": "",
            "life_cycle_stage_status": "",
            "model_number": "",
            "assigned_to": "",
            "start_date": "",
            "os_version": "",
            "serial_number": "",
            "cd_rom": "false",
            "support_group": "",
            "unverified": "false",
            "correlation_id": "",
            "attributes": "",
            "asset": {
                "display_value": "Unknown",
                "link": "https://instance.servicenow.com/api/now/table/alm_asset/21cfba641b425010593876a61a4bcb52",
                "value": "21cfba641b425010593876a61a4bcb52"
            },
            "form_factor": "",
            "cpu_core_count": "",
            "skip_sync": "false",
            "attestation_score": "",
            "sys_updated_by": "dora.gray",
            "sys_created_on": "2020-07-13 20:27:28",
            "sys_domain": {
                "display_value": "global",
                "link": "https://instance.servicenow.com/api/now/table/sys_user_group/global",
                "value": "global"
            },
            "cpu_type": "",
            "install_date": "",
            "asset_tag": "",
            "dr_backup": "",
            "hardware_substatus": "",
            "fqdn": "",
            "change_control": "",
            "internet_facing": "true",
            "delivery_date": "",
            "hardware_status": "installed",
            "install_status": "1",
            "supported_by": "",
            "name": "Linux299",
            "subcategory": "Computer",
            "default_gateway": "",
            "chassis_type": "",
            "virtual": "false",
            "assignment_group": "",
            "managed_by_group": "",
            "sys_id": "0c3ff2641b425010593876a61a4bcb39",
            "po_number": "",
            "checked_in": "",
            "sys_class_path": "/!!/!2/!(/!!/!0",
            "mac_address": "",
            "company": "",
            "justification": "",
            "department": "",
            "cost": "",
            "comments": "",
            "os": "",
            "sys_mod_count": "4",
            "monitor": "false",
            "model_id": {
                "display_value": "Unknown",
                "link": "https://instance.servicenow.com/api/now/table/cmdb_model/0ce0a2681b4e1010593876a61a4bcba6",
                "value": "0ce0a2681b4e1010593876a61a4bcba6"
            },
            "ip_address": "",
            "duplicate_of": "",
            "sys_tags": "",
            "cost_cc": "USD",
            "order_date": "",
            "schedule": "",
            "environment": "",
            "due": "",
            "attested": "false",
            "location": "",
            "category": "Hardware",
            "fault_count": "0",
            "host_name": "",
            "lease_id": ""
        },
        "inbound_relations": [
            {
                "sys_id": "c03ff2641b425010593876a61a4bcb49",
                "type": {
                    "display_value": "Depends on::Used by",
                    "link": "https://instance.servicenow.com/api/now/table/cmdb_rel_type/1a9cb166f1571100a92eb60da2bce5c5",
                    "value": "1a9cb166f1571100a92eb60da2bce5c5"
                },
                "target": {
                    "display_value": "PS Apache01",
                    "link": "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci/3a27d4370a0a0bb4006316812bf45439",
                    "value": "3a27d4370a0a0bb4006316812bf45439"
                }
            }
        ]
    }
}
```

## CMDB Instance - PATCH /now/cmdb/instance/\{classname\}/\{sys\_id\}

Replaces the attributes in the specified configuration item \(CI\) record with the specified name-value pairs. This endpoint does not create, update, or delete the associated relations.

### URL format

Versioned URL: `/api/now/{api_version}/cmdb/instance/{className}/{sys_id}`

Default URL: `/api/now/cmdb/instance/{className}/{sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

className

</td><td id="entry-className-cmdb">

CMDB class name. This is the name of the table that contains the desired CI records, such as cmdb\_ci\_linux\_server or cmdb\_ci\_apache\_web\_server.Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="entry-sys_id-cmdb">

Sys\_id of the CI record to update.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None||

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td id="entry-attributes-cmdb">

Data attributes to replace in the CI record. The available attributes depend on the specified CMDB class. You can locate the available attributes in the associated CMDB table which typically begins with "cmdb\_ci", such as cmdb\_ci\_linux\_server or cmdb\_ci\_mfp\_printer.For information about attestation, see [CIs attestation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/attesting-cis.md).

Data type: Object

</td></tr><tr><td>

source

</td><td id="entry-source-cmdb">

Required. Entity that updated the information. This must be one of the choice values specified in the discovery\_source field in the Configuration Item \[cmdb\_ci\] table.Data type: String

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
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|405|Invalid method. The functionality is disabled.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_ojn_3n4_3mb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td>

Data attributes currently in the CI record. The available attributes depend on the specified CMDB class. You can locate the available attributes in the associated CMDB table which typically begins with "cmdb\_ci", such as cmdb\_ci\_linux\_server or cmdb\_ci\_mfp\_printer.Data type: Object

</td></tr><tr id="row-result-error-cmdb"><td>

error

</td><td id="entry-result-error-cmdb">

Information on any errors encountered while processing the endpoint request. Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr id="row-result-error_detail-cmdb"><td>

error.detail

</td><td id="entry-result-error_detail-cmdb">

Additional information about the error.Data type: String

</td></tr><tr id="row-result-error_message-cmdb"><td>

error.message

</td><td id="entry-result-error_message-cmdb">

Message that identifies the error.Data type: String

</td></tr><tr id="row-result-inbound_relations-cmdb"><td>

inbound\_relations

</td><td id="entry-result-inbound_relations-cmdb">

List of objects that define the inbound relations associated with the CI.Data type: Array

```
"inbound_relations": [
  {
    "sys_id": "String",
    "target": {Object},
    "type": {Object}
  }
]
```

</td></tr><tr id="row-result-inbound_relations_sys_id-cmdb"><td>

inbound\_relations.sys\_id

</td><td id="entry-result-inbound_relations_sys_id-cmdb">

Sys\_id of the inbound CI relationship. Located in the CI Relationship \[cmdb\_rel\_ci\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_target-cmdb"><td>

inbound\_relations.target

</td><td id="entry-result-inbound_relations_target-cmdb">

Information that describes the target inbound relation.Data type: Object

```
"target": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-inbound_relations_target_display_value-cmdb"><td>

inbound\_relations.target.display\_value

</td><td id="entry-result-inbound_relations_target_display_value-cmdb">

Name of the inbound relation to display in a user interface.Data type: String

</td></tr><tr id="row-result-inbound_relations_target_link-cmdb"><td>

inbound\_relations.target.link

</td><td id="entry-result-inbound_relations_target_link-cmdb">

CMDB REST endpoint URL to use to retrieve the inbound relation from the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_target_value-cmdb"><td>

inbound\_relations.target.value

</td><td id="entry-result-inbound_relations_target_value-cmdb">

Sys\_id of the inbound CI. Located in the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_type-cmdb"><td>

inbound\_relations.type

</td><td id="entry-result-inbound_relations_type-cmdb">

Information about the type of inbound relationship. Data type: Object

```
"type": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-inbound_relations_type_display_value-cmdb"><td>

inbound\_relations.type.display\_value

</td><td id="entry-result-inbound_relations_type_display_value-cmdb">

Name of the inbound type to display in a user interface.Data type: String

</td></tr><tr id="row-result-inbound_relations_type_link-cmdb"><td>

inbound\_relations.type.link

</td><td id="entry-result-inbound_relations_type_link-cmdb">

Table REST endpoint URL to use to retrieve the inbound relation type from the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-result-inbound_relations_type_value-cmdb"><td>

inbound\_relations.type.value

</td><td id="entry-result-inbound_relations_type_value-cmdb">

Sys\_id of the type of inbound relationship. Located in the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations-cmdb"><td>

outbound\_relations

</td><td id="entry-result-outbound_relations-cmdb">

List of objects that define the outbound relations associated with the CI.Data type: Array

```
"outbound_relations": [
  {
    "sys_id": "String",
    "target": {Object},
    "type": {Object}
  }
]
```

</td></tr><tr id="row-result-outbound_relations_sys_id-cmdb"><td>

outbound\_relations.sys\_id

</td><td id="entry-result-outbound_relations_sys_id-cmdb">

Sys\_id of the outbount CI relationship. Located in the CI Relationship \[cmdb\_rel\_ci\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_target-cmdb"><td>

outbound\_relations.target

</td><td id="entry-result-outbound_relations_target-cmdb">

Required. Information about the target outbound relation.Data type: Object

```
"target": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-outbound_relations_target_display_value-cmdb"><td>

outbound\_relations.target.display\_value

</td><td id="entry-result-outbound_relations_target_display_value-cmdb">

Name of the outbound relation to display in a user interface.Data type: String

</td></tr><tr id="row-result-outbound_relations_target_link-cmdb"><td>

outbound\_relations.target.link

</td><td id="entry-result-outbound_relations_target_link-cmdb">

CMDB REST endpoint URL to use to retrieve the outbound relation from the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_target_value-cmdb"><td>

outbound\_relations.target.value

</td><td id="entry-result-outbound_relations_target_value-cmdb">

Sys\_id of the outbound CI. Located in the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_type-cmdb"><td>

outbound\_relations.type

</td><td id="entry-result-outbound_relations_type-cmdb">

Information about the type of outbound relationship. Data type: Object

```
"type": {
  "display_value": "String",
  "link": "String",
  "value": "String"
}
```

</td></tr><tr id="row-result-outbound_relations_type_display_value-cmdb"><td>

outbound\_relations.type.display\_value

</td><td id="entry-result-outbound_relations_type_display_value-cmdb">

Name of the outbound type to display in a user interface.Data type: String

</td></tr><tr id="row-result-outbound_relations_type_link-cmdb"><td>

outbound\_relations.type.link

</td><td id="entry-result-outbound_relations_type_link-cmdb">

Table REST endpoint URL to use to retrieve the outbound relation from the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-result-outbound_relations_type_value-cmdb"><td>

outbound\_relations.type.value

</td><td id="entry-result-outbound_relations_type_value-cmdb">

Sys\_id of the type of outbound relationship. Located in the CI Relationship Type \[cmdb\_rel\_type\] table.Data type: String

</td></tr><tr id="row-status-cmdb"><td>

status

</td><td id="entry-result-status-cmdb">

Only appears if an error is encountered. Status of the endpoint processing.Possible value: failure

Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_class_sw/70bc4e11c0a8210d01f074cbe6bd73b4" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json"\
--user "username":"password"\
--data {
    "attributes": {
      "firewall_status": "Active",
      "name": "Linux299",
      "used_for": "Production"
    },
    "source": "ServiceNow"
}
```

```
{
  "result": {
    "outbound_relations": [
      {
        "sys_id": "403ff2641b425010593876a61a4bcb4b",
        "type": {
          "display_value": "Depends on::Used by",
          "link": "https://instance.servicenow.com/api/now/table/cmdb_rel_type/1a9cb166f1571100a92eb60da2bce5c5",
          "value": "1a9cb166f1571100a92eb60da2bce5c5"
        },
        "target": {
          "display_value": "PS ORA01",
          "link": "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci/3a307c930a0a0bb400353965d0b8861f",
          "value": "3a307c930a0a0bb400353965d0b8861f"
        }
      },
      {
        "sys_id": "443ff2641b425010593876a61a4bcb4c",
        "type": {
          "display_value": "Exchanges data with::Exchanges data with",
          "link": "https://instance.servicenow.com/api/now/table/cmdb_rel_type/607ad1b2c0a8010e01941856b365af90",
          "value": "607ad1b2c0a8010e01941856b365af90"
        },
        "target": {
          "display_value": "PS ORA01",
          "link": "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci/3a307c930a0a0bb400353965d0b8861f",
          "value": "3a307c930a0a0bb400353965d0b8861f"
        }
      }
    ],
    "attributes": {
      "firewall_status": "Active",
      "os_address_width": "",
      "attested_date": "",
      "operational_status": "1",
      "os_service_pack": "",
      "cpu_core_thread": "",
      "cpu_manufacturer": "",
      "sys_updated_on": "2020-07-13 21:24:05",
      "discovery_source": "ServiceNow",
      "first_discovered": "2020-07-13 20:27:28",
      "due_in": "",
      "used_for": "Production",
      "invoice_number": "",
      "gl_account": "",
      "sys_created_by": "dora.gray",
      "warranty_expiration": "",
      "ram": "",
      "cpu_name": "",
      "cpu_speed": "",
      "owned_by": "",
      "checked_out": "",
      "kernel_release": "",
      "sys_domain_path": "/",
      "classification": "Production",
      "disk_space": "",
      "object_id": "",
      "maintenance_schedule": "",
      "cost_center": "",
      "attested_by": "",
      "dns_domain": "",
      "assigned": "",
      "purchase_date": "",
      "life_cycle_stage": "",
      "short_description": "",
      "cd_speed": "",
      "floppy": "",
      "managed_by": "",
      "os_domain": "",
      "last_discovered": "2020-07-13 21:24:05",
      "can_print": "false",
      "sys_class_name": "cmdb_ci_linux_server",
      "manufacturer": "",
      "cpu_count": "",
      "vendor": "",
      "life_cycle_stage_status": "",
      "model_number": "",
      "assigned_to": "",
      "start_date": "",
      "os_version": "",
      "serial_number": "",
      "cd_rom": "false",
      "support_group": "",
      "unverified": "false",
      "correlation_id": "",
      "attributes": "",
      "asset": {
        "display_value": "Unknown",
        "link": "https://instance.servicenow.com/api/now/table/alm_asset/21cfba641b425010593876a61a4bcb52",
        "value": "21cfba641b425010593876a61a4bcb52"
      },
      "form_factor": "",
      "cpu_core_count": "",
      "skip_sync": "false",
      "attestation_score": "",
      "sys_updated_by": "dora.gray",
      "sys_created_on": "2020-07-13 20:27:28",
      "sys_domain": {
        "display_value": "global",
        "link": "https://instance.servicenow.com/api/now/table/sys_user_group/global",
        "value": "global"
      },
      "cpu_type": "",
      "install_date": "",
      "asset_tag": "",
      "dr_backup": "",
      "hardware_substatus": "",
      "fqdn": "",
      "change_control": "",
      "internet_facing": "true",
      "delivery_date": "",
      "hardware_status": "installed",
      "install_status": "1",
      "supported_by": "",
      "name": "Linux299",
      "subcategory": "Computer",
      "default_gateway": "",
      "chassis_type": "",
      "virtual": "false",
      "assignment_group": "",
      "managed_by_group": "",
      "sys_id": "0c3ff2641b425010593876a61a4bcb39",
      "po_number": "",
      "checked_in": "",
      "sys_class_path": "/!!/!2/!(/!!/!0",
      "mac_address": "",
      "company": "",
      "justification": "",
      "department": "",
      "cost": "",
      "comments": "",
      "os": "",
      "sys_mod_count": "4",
      "monitor": "false",
      "model_id": {
        "display_value": "Unknown",
        "link": "https://instance.servicenow.com/api/now/table/cmdb_model/0ce0a2681b4e1010593876a61a4bcba6",
        "value": "0ce0a2681b4e1010593876a61a4bcba6"
      },
      "ip_address": "",
      "duplicate_of": "",
      "sys_tags": "",
      "cost_cc": "USD",
      "order_date": "",
      "schedule": "",
      "environment": "",
      "due": "",
      "attested": "false",
      "location": "",
      "category": "Hardware",
      "fault_count": "0",
      "host_name": "",
      "lease_id": ""
    },
    "inbound_relations": [
      {
        "sys_id": "c03ff2641b425010593876a61a4bcb49",
         "type": {
           "display_value": "Depends on::Used by",
            "link": "https://instance.servicenow.com/api/now/table/cmdb_rel_type/1a9cb166f1571100a92eb60da2bce5c5",
            "value": "1a9cb166f1571100a92eb60da2bce5c5"
          },
          "target": {
            "display_value": "PS Apache01",
            "link": "https://instance.servicenow.com/api/now/cmdb/instance/cmdb_ci/3a27d4370a0a0bb4006316812bf45439",
            "value": "3a27d4370a0a0bb4006316812bf45439"
          }
        }
      ]
    }
}
```

