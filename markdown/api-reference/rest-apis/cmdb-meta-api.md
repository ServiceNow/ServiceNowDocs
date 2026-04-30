---
title: CMDB Meta API
description: The CMDB Meta API provides endpoints to obtain meta data on a Configuration Management Database \(CMDB\) class.Returns the meta data for the specified CMDB class.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# CMDB Meta API

The CMDB Meta API provides endpoints to obtain meta data on a Configuration Management Database \(CMDB\) class.

This API requires that the user have the ITIL role.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## CMDB Meta - GET /now/cmdb/meta/\{classname\}

Returns the meta data for the specified CMDB class.

### URL format

Versioned URL: `/api/now/{api_version}/cmdb/meta/{className}`

Default URL: `/api/now/cmdb/meta/{className}`

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

</td><td>

CMDB class name. This is the name of the table that contains the desired CI records, such as cmdb\_ci\_linux\_server or cmdb\_ci\_apache\_web\_server.Data type: String

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
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td>

Available fields in the specified class table. Data type: Array

</td></tr><tr><td>

children

</td><td>

List of classes extended from the specified class.Data type: Array

</td></tr><tr><td>

icon

</td><td>

Class icon sys\_id.Data type: String

</td></tr><tr><td>

icon\_url

</td><td>

Class icon URL. Data type: String

</td></tr><tr><td>

identification\_rules

</td><td>

Attributes associated with the configuration item identification rules for the specified class. Data type: Object

</td></tr><tr><td>

is\_extendable

</td><td>

Flag that indicates whether the class can be extended to create other classes.Possible values:

-   true: Class can be extended.
-   false: Class cannot be extended.

 Data type: Boolean

</td></tr><tr><td>

label

</td><td>

Specified class display name.Data type: String

</td></tr><tr><td>

name

</td><td>

Table/class name.Data type: String

</td></tr><tr><td>

parent

</td><td>

Parent class.Data type: String

</td></tr><tr><td>

relationship\_rules

</td><td>

Relationships between the specifed class and other classes in the CMDB. Data type: Array

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.servicenow/api/now/cmdb/meta/cmdb_ci_computer" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'

```

```
{
  "result": {
    "icon_url": "images/app.ngbsm/computer.svg",
    "is_extendable": true,
    "parent": "cmdb_ci_hardware",
    "children": [
      "cmdb_ci_ucs_blade",
      "cmdb_ci_pc_hardware",
      "cmdb_ci_ucs_rack_unit",
      "cmdb_ci_mainframe_hardware",
      "cmdb_ci_server",
      "cmdb_ci_storage_switch"
    ],
    "name": "cmdb_ci_computer",
    "icon": "c6442dd69fb00200eb3919eb552e7012",
    "attributes": [
      {
        "is_inherited": "false",
        "is_mandatory": "false",
        "is_read_only": "false",
        "default_value": null,
        "label": "OS Address Width (bits)",
        "type": "integer",
        "element": "os_address_width",
        "max_length": "40",
        "is_display": "false"
      },
      {
        "is_inherited": "true",
        "is_mandatory": "false",
        "is_read_only": "true",
        "default_value": "false",
        "label": "Skip sync",
        "type": "boolean",
        "element": "skip_sync",
        "max_length": "40",
        "is_display": "false"
      },
      {
        "is_inherited": "true",
        "is_mandatory": "false",
        "is_read_only": "false",
        "default_value": null,
        "label": "DNS Domain",
        "type": "string",
        "element": "dns_domain",
        "max_length": "255",
        "is_display": "false"
      },
      {
        "is_inherited": "true",
        "is_mandatory": "false",
        "is_read_only": "false",
        "default_value": null,
        "label": "Purchased",
        "type": "glide_date",
        "element": "purchase_date",
        "max_length": "40",
        "is_display": "false"
      },
      {
        "is_inherited": "true",
        "is_mandatory": "false",
        "is_read_only": "false",
        "default_value": null,
        "label": "Lease contract",
        "type": "string",
        "element": "lease_id",
        "max_length": "40",
        "is_display": "false"
      }
    ],
    "relationship_rules": [
      {
        "parent": "cmdb_ci_computer",
        "relation_type": "cb5592603751200032ff8c00dfbe5d17",
        "child": "dscy_route_next_hop"
      },
      {
        "parent": "cmdb_ci_computer",
        "relation_type": "cb5592603751200032ff8c00dfbe5d17",
        "child": "dscy_router_interface"
      },
      {
        "parent": "cmdb_ci_computer",
        "relation_type": "cb5592603751200032ff8c00dfbe5d17",
        "child": "dscy_route_interface"
      },
      {
        "parent": "cmdb_ci_computer",
        "relation_type": "55c95bf6c0a8010e0118ec7056ebc54d",
        "child": "cmdb_ci_storage_pool"
      },
      {
        "parent": "cmdb_ci_computer",
        "relation_type": "55c95bf6c0a8010e0118ec7056ebc54d",
        "child": "cmdb_ci_disk_partition"
      },
      {
        "parent": "cmdb_ci_computer",
        "relation_type": "55c95bf6c0a8010e0118ec7056ebc54d",
        "child": "cmdb_ci_storage_volume"
      },
      {
        "parent": "cmdb_ci_computer",
        "relation_type": "55c95bf6c0a8010e0118ec7056ebc54d",
        "child": "cmdb_ci_storage_device"
      }
    ],
    "label": "Computer",
    "identification_rules": {
      "related_rules": [
        {
          "condition": "",
          "exact_count_match": false,
          "referenced_field": "installed_on",
          "active": true,
          "attributes": "name",
          "allow_fallback": false,
          "table": "cmdb_print_queue_instance",
          "order": 100,
          "allow_null_attribute": false
        }
      ],
      "applies_to": "cmdb_ci_hardware",
      "identifiers": [
        {
          "condition": "valid=true^absent=false^EQ",
          "exact_count_match": true,
          "referenced_field": "cmdb_ci",
          "active": true,
          "attributes": "serial_number,serial_number_type",
          "allow_fallback": false,
          "table": "cmdb_serial_number",
          "order": 100,
          "allow_null_attribute": false
        },
        {
          "condition": null,
          "exact_count_match": false,
          "referenced_field": null,
          "active": true,
          "attributes": "serial_number",
          "allow_fallback": false,
          "table": null,
          "order": 200,
          "allow_null_attribute": false
        },
        {
          "condition": null,
          "exact_count_match": false,
          "referenced_field": null,
          "active": true,
          "attributes": "name",
          "allow_fallback": false,
          "table": null,
          "order": 300,
          "allow_null_attribute": false
        },
        {
          "condition": "install_status!=100^EQ",
          "exact_count_match": true,
          "referenced_field": "cmdb_ci",
          "active": true,
          "attributes": "ip_address,mac_address",
          "allow_fallback": false,
          "table": "cmdb_ci_network_adapter",
          "order": 400,
          "allow_null_attribute": false
        }
      ],
      "name": "Hardware Rule",
      "description": "Identifier for hardware.",
      "active": true,
      "is_independent": true
    }
  }
}

```

