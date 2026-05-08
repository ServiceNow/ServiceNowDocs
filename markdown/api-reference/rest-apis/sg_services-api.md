---
title: SG Services API
description: The SG Services API provides endpoints to create and manage application services and the upstream relationships between them.Converts a manual or empty type application service to a calculated application service. During conversion, the application service record moves into the \[cmdb\_ci\_service\_calculated\] table with the newly assigned class.Deletes an application service.Finds the details of a given application service and its upstream relationships.Populates an application service with a service population method.Creates an application service, tags and constructs upstream relationships such as business applications, business service offerings, and other application services.Constructs upstream relations such as business applications, business service offerings, and other application services.Deletes an application service upstream relationship.Changes the application service lifecycle state to activate, deactivate, or retire.Updates an existing application service provided and creates tags for the given application service.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 32
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# SG Services API

The SG Services API provides endpoints to create and manage application services and the upstream relationships between them.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

This API can only be used when the CMDB Application API and CLI \(sn\_service\_graph\) plugin is activated. This API is used within the `sn_service_graph` namespace.

Using this API does not require details regarding source tables or relationship types.

To script critical operations which support automation across the enterprise, you can leverage APIs or run command line operations that the CMDB Application CLI and API store app provide instead of using the user interface. The CMDB Application CLI and API store app provides a robust framework which consolidates all the APIs that are related to application services and the command lines that let you access the interface to those APIs.

CMDB Application CLI and API commands enable the following tasks:

-   Registering and creating an application service and establishing upstream relationships
-   Getting details of a given application service and its upstream relationships
-   Connecting higher level constructs such as business applications and business service offerings
-   Populating an application service with a given population type
-   Changing the state of an application service

For the command line solution, see CMDB Application CLI and API available commands.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## SG Services – POST /sg\_services/app\_service/convert

Converts a manual or empty type application service to a calculated application service. During conversion, the application service record moves into the \[cmdb\_ci\_service\_calculated\] table with the newly assigned class.

The following properties for identifying a CI take precedence as follows:

1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.

### URL format

Versioned URL: `/api/sn_service_graph/{api_version}/sg_services/app_service/convert`

Default URL: `/api/sn_service_graph/sg_services/app_service/convert`

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

&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version. Data type: String

</td></tr><tr><td>

levels

</td><td>

Number of levels to include in the conversion.Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the application service. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\] table. Data type: String

</td></tr></tbody>
</table>### Headers

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
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or the user does not have the app\_service\_admin role.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_iyx_jnx_gqb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Indicates success or failure.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to convert an application service type.

```
curl "https://instance.service-now.com/api/sn_service_graph/sg_services/app_service/convert" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
 \"name\": \"Test Register\",
 \"environment\": \"Test\",
 \"version\": \"1.0\",
 \"levels\" : 8
}" \
--user 'username':'password'
```

Results indicating a successful conversion to a calculated application service.

```
{
  "result": {
  "status": "success"
  }
}
```

## SG Services – POST /sg\_services/app\_service/delete

Deletes an application service.

The following properties for identifying a CI take precedence as follows:

1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.

### URL format

Versioned URL: `/api/sn_service_graph/{api_version}/sg_services/app_service/delete`

Default URL: `/api/sn_service_graph/sg_services/app_service/delete`

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

<table id="table_e5t_gwt_gqb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version. Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the application service. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\] table. Data type: String

</td></tr></tbody>
</table>### Headers

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
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or the user does not have the app\_service\_admin role.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_pvd_l5t_gqb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Indicates success or failure.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to delete an application service.

```
curl "https://instance.service-now.com/api/sn_service_graph/sg_services/app_service/delete" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   \"name\": \"Test Register\",
   \"environment\": \"Test\",
   \"version\": \"1.0\"
}" \
--user 'username':'password'
```

Results indicating a successful removal of an application service.

```
{
  "result": {
  "status": "success"
  }
}
```

## SG Services – POST /sg\_services/app\_service/find

Finds the details of a given application service and its upstream relationships.

Users with the app\_service\_user role can use this API, but results are restricted to application services in Operational status. The app\_service\_admin role provides unlimited viewing of application services.

The following properties for identifying a CI take precedence as follows:

1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.

### URL format

Versioned URL: `/api/sn_service_graph/{api_version}/sg_services/app_service/find`

Default URL: `/api/sn_service_graph/sg_services/app_service/find`

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

&lt;IRE fields&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version. Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the application service. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\] table. Data type: String

</td></tr></tbody>
</table>### Headers

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
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or the user does not have the app\_service\_admin role.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_iyx_jnx_gqb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version. Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the application service. Data type: String

</td></tr><tr><td>

operational\_status

</td><td>

Operational status of the application service. For example, active.Data type: String

</td></tr><tr><td>

relationships

</td><td>

List of objects defining the application service's upstream relationships.Data type: Array

 ```
"relationships": [
 {
    "name": "String",
    "number": "String",
    "sys_id": "String",
    "class_name": "String",
    "relationship": "String"
 }
]
```

</td></tr><tr><td>

relationships.class\_name

</td><td>

Name of the class that contains the application service.Data type: String

</td></tr><tr><td>

relationships.name

</td><td>

Name of the relationship.Data type: String

</td></tr><tr><td>

relationships.number

</td><td>

Unique number of the relationship.Data type: String

</td></tr><tr><td>

relationships.relationship

</td><td>

The relationship rule.Data type: String

</td></tr><tr><td>

relationships.sys\_id

</td><td>

Sys\_id of the relationship.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\] table. Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to find details of an application service.

```
curl "https://instance.service-now.com/api/sn_service_graph/sg_services/app_service/find" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   \"name\": \"Test App Service1\"
 }" \
--user 'username':'password'
```

The response body includes the application service and relationship information.

```
{
  "result": {
    "aliases": null,
    "asset": null,
    "asset_tag": null,
    "assigned": "",
    "assigned_to": null,
    "assignment_group": null,
    "attestation_score": null,
    "attested": "0",
    "attested_by": null,
    "attested_date": "",
    "attributes": null,
    "bucket": null,
    "business_contact": null,
    "business_need": null,
    "business_relation_manager": null,
    "business_unit": null,
    "busines_criticality": "4 - not critical",
    "can_print": "0",
    "category": null,
    "change_control": null,
    "checked_in": "",
    "checked_out": "",
    "checkout": null,
    "comments": null,
    "company": null,
    "compatibility_dependencies": null,
    "consumer_type": "internal",
    "correlation_id": null,
    "cost": null,
    "cost_cc": "USD",
    "cost_center": null,
    "delivery_date": "",
    "delivery_manager": null,
    "department": null,
    "discovery_source": "Manual Entry",
    "dns_domain": null,
    "due": "",
    "due_in": null,
    "duplicate_of": null,
    "end_date": "",
    "environment": null,
    "fault_count": "0",
    "first_discovered": "2021-07-19 20:09:48",
    "fqdn": null,
    "gl_account": null,
    "hide_from_dashboard": "0",
    "install_date": "",
    "install_status": "1",
    "invoice_number": null,
    "ip_address": null,
    "justification": null,
    "last_discovered": "2021-07-19 20:09:48",
    "last_review_date": "",
    "layer": null,
    "lease_id": null,
    "life_cycle_stage": null,
    "life_cycle_stage_status": null,
    "location": null,
    "mac_address": null,
    "maintenance_schedule": null,
    "managed_by": null,
    "managed_by_group": null,
    "manufacturer": null,
    "model_id": null,
    "model_number": null,
    "monitor": "0",
    "monitoring_requirements": null,
    "name": "Test App Service1",
    "number": "SNSVC0001014",
    "operational_status": "2",
    "order_date": "",
    "owned_by": null,
    "parent": null,
    "portfolio_status": "pipeline",
    "po_number": null,
    "prerequisites": null,
    "price_model": "per_unit",
    "price_unit": null,
    "published_ref": null,
    "purchase_date": "",
    "schedule": null,
    "serial_number": null,
    "service_classification": "Application Service",
    "service_level_requirement": null,
    "service_owner_delegate": null,
    "service_status": "requirements",
    "severity": null,
    "short_description": null,
    "skip_sync": "0",
    "sla": null,
    "spm_service_portfolio": null,
    "spm_taxonomy_node": null,
    "stakeholders": null,
    "start_date": "",
    "state": null,
    "subcategory": null,
    "supported_by": null,
    "support_group": null,
    "sys_class_name": "cmdb_ci_service_auto",
    "sys_class_path": "/!!/!7/!(",
    "sys_created_by": "admin",
    "sys_created_on": "2021-07-19 20:09:48",
    "sys_domain": "global",
    "sys_domain_path": "/",
    "sys_id": "a2f0618040697410f87713b656474255",
    "sys_mod_count": "0",
    "sys_updated_by": "admin",
    "sys_updated_on": "2021-07-19 20:09:48",
    "unit_description": null,
    "unverified": "0",
    "used_for": "Production",
    "user_group": null,
    "vendor": null,
    "version": null,
    "view_service": "61e1cb757f23220002d31ccebefa9120",
    "warranty_expiration": "",
    "relationships": [
      {
        "name": "Test Biz App1",
        "sys_id": "0250a94040697410f87713b656474250",
        "number": "APM0001001",
        "class_name": "cmdb_ci_business_app",
        "relationship": "Consumes::Consumed by"
      },
      {
        "name": "Tech Service Offering1",
        "sys_id": "98d0ed4040697410f87713b6564742ef",
        "number": "BSN0001005",
        "class_name": "service_offering",
        "relationship": "Contains::Contained by"
      }
    ]
  }
}
```

## SG Services – POST /sg\_services/app\_service/populate

Populates an application service with a service population method.

The following properties for identifying a CI take precedence as follows:

1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.

### URL format

Versioned URL: `/api/sn_service_graph/{api_version}/sg_services/app_service/populate`

Default URL: `/api/sn_service_graph/sg_services/app_service/populate`

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

&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version. Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the application service. Data type: String

</td></tr><tr><td>

population\_method

</td><td>

Required. Identifies the population method and its accompanying property to identify the content for population.Only one accompanying object is valid per type.

 Data type: Object

</td></tr><tr><td>

population\_method.group\_id

</td><td>

Group ID of the CMDB group configured with the cmdb\_group population type.Data type: "String"

 ```
"population_method": {
  "group_id": "String",
  "type": "cmdb_group"
}
```

 Associated population type: cmdb\_group

</td></tr><tr><td>

population\_method.levels

</td><td>

Number of levels to use in building the service. If the level value is not provided, the system checks the sys\_property for the value. If svc.manual.convert.levels.default\_value is not populated, a default value of 3 is used.Data type: Number

 ```
"population_method": {
  "levels": Number,
  "type": "dynamic_service"
}
```

 Associated population type: dynamic\_service

 Default: 3 if no level value is set for the sys\_property

</td></tr><tr><td>

population\_method.service\_candidate

</td><td>

Unique identifier of the service candidate.

 Data type: String

 ```
"population_method": {
  "service_candidate": "String",
  "type": "tag_based_service_family"
}
```

 Associated population type: tag\_based\_service\_family

</td></tr><tr><td>

population\_method.service\_relations

</td><td>

List of objects containing hierarchy data for the CIs within the application service. All CIs form pairs with a parent and child CI. The top-level CI, referred to as the entry point of an application service, does not have a parent CI.Data type: Array

 ```
"population_method": {

  "service_relations":[
     {
      "child": "String",
      "parent": "String"
     }
  ],

  "type": "service_hierarchy"   
}
```

 Associated population type: service\_hierarchy

</td></tr><tr><td>

population\_method.service\_relations.child

</td><td>

Name of a child CI related to the CI.Data type: String

</td></tr><tr><td>

population\_method.service\_relations.parent

</td><td>

Name of a parent CI related to the CI.Data type: String

</td></tr><tr><td>

population\_method.tags

</td><td>

List of objects containing tags to associate with the CI. This information is located in the Key Values \[cmdb\_key\_value\] table.Data type: Array

 ```
"population_method": {

  "tags": [
     {
      "tag": "String",
      "value": "String"
     }
  ],

  "type": "tag_list"  
}
```

 Associated population type: tag\_list

</td></tr><tr><td>

population\_method.tags.tag

</td><td>

Tag name.Data type: String

</td></tr><tr><td>

population\_method.tags.value

</td><td>

Tag value.Data type: String

</td></tr><tr><td>

population\_method.type

</td><td>

Required. Population type to add to the application service.Data type: Object

 Valid values:

-   cmdb\_group
-   service\_hierarchy
-   dynamic\_service
-   tag\_list
-   tag\_based\_service\_family

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\] table. Data type: String

</td></tr></tbody>
</table>### Headers

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
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or the user does not have the app\_service\_admin role.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_iyx_jnx_gqb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Indicates success or failure.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to populate an application service with a dynamic\_service type.

```
curl "https://instance.service-now.com/api/sn_service_graph/sg_services/app_service/populate" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"name\": \"Test Register\",
  \"environment\": \"Test\",
  \"version\": \"1.0\",

 \"population_method\": {
   \"type\": \"dynamic_service\",
   \"levels\" : 8
  }
}" \
--user 'username':'password'
```

Results indicating a successful population of an application service.

```
{
  "result": {
  "status": "success"
  }
}
```

## SG Services – POST /sg\_services/app\_service/register

Creates an application service, tags and constructs upstream relationships such as business applications, business service offerings, and other application services.

The following properties for identifying a CI take precedence as follows:

1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.

### URL format

Versioned URL: `/api/sn_service_graph/{api_version}/sg_services/app_service/register`

Default URL: `/api/sn_service_graph/sg_services/app_service/register`

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

&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version. Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the application service. Data type: String

</td></tr><tr><td>

relationships

</td><td>

Upstream relationships categorized by type.Data type: Object

 ```
"relationships": {
 "business_app": [Array],
 "business_service_offering": [Array],
 "parent_app_service": [Array],
 "technical_service_offering": [Array]
}
```

 Maximum number of relationships is 25.

</td></tr><tr><td>

relationships.business\_app

</td><td>

List of objects representing Business Application relationship types. These values can be defined using one of the following items as key-value pairs.

-   &lt;IRE field name&gt;
-   number
-   sys\_id

 Data type: Array

</td></tr><tr><td>

relationships.business\_service\_offering

</td><td>

List of objects representing Business Service Offering relationship types. These values can be defined using the following items as key-value pairs.

-   &lt;IRE field name&gt;
-   number
-   sys\_id

 Data type: Array

</td></tr><tr><td>

relationships.parent\_app\_service

</td><td>

List of objects representing Application Service relationship types. These values can be defined using the following items as key-value pairs.

-   &lt;IRE field name&gt;
-   number
-   sys\_id

 Data type: Array

</td></tr><tr><td>

relationships.technical\_service\_offering

</td><td>

List of objects representing technology management offering \(formerly technical service offering\)relationship types. These values can be defined using the following items as key-value pairs.

-   &lt;IRE field name&gt;
-   number
-   sys\_id

 Data type: Array

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\] table. Data type: String

</td></tr><tr><td>

tags

</td><td>

List of objects containing tag definitions as key-value pairs.```
"tags": [
 {
  "key": "String",
  "value": "String"
 }]
```

 Data type: Array

</td></tr><tr><td>

tags.key

</td><td>

Tag category name.Data type: String

</td></tr><tr><td>

tags.value

</td><td>

Tag value.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|cHeader|Description|
|-------|-----------|
|none| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or the user does not have the app\_service\_admin role.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

cHeader

</th><th>

Description

</th></tr></thead><tbody><tr><td>

app\_service

</td><td>

Application service details.Data type: Object

 ```
"app_service": {
  "name": "String",
  "number": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

app\_service.name

</td><td>

Name of the application service.Data type: String

</td></tr><tr><td>

app\_service.number

</td><td>

Unique number that identifies the application service. Data type: String

</td></tr><tr><td>

app\_service.sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\] table. Data type: String

</td></tr><tr><td>

message

</td><td>

Message describing the status.Possible values:

-   Service already exists
-   Service registered successfully

 Data type: String

</td></tr><tr><td>

status

</td><td>

Status indicating whether the service has been registered.Possible values:

-   Insert: The application service was successfully created.
-   No action: The application service already exists. No action taken.

 Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to register an application service.

```
curl "instance.service-now.com/api/sn_service_graph/sg_services/app_service/register" \--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"name\": \"Test Register\",
  \"environment\": \"Test\",
  \"version\": \"1.0\",
  \"number\": \" SNSVC0001014\",
  \"relationships\": {
    \"business_application\": [
      {
        \"sys_id\": \"0250a94040697410f87713b656474250\"
      },
      {
        \"number\": \"APM0001002\"
      },
      {
        \"name\": \"Test Biz App1\"
      }
    ],
    \"business_service_offering\": [
      {
        \"sys_id\": \"ed32e98040697410f87713b656474259\"
      }
    ],
    \"technical_service_offering\": [
      {
        \"sys_id\": \"80e12d8040697410f87713b65647421c\"
      },
      {
        \"number\": \"BSN0001005\"
      },
      {
        \"name\": \"Tech Service Offering2\"
      }
    ],
    \"parent_app_service\": [
      {
        \"sys_id\": \"a2f0618040697410f87713b656474255\"
      }
    ]
  },
  \"tags\": [
    {
      \"key\": \"key1\",
      \"value\": \"value1\"
    },
    {
      \"key\": \"key2\",
      \"value\": \"value2\"
    }
  ]
}" \
--user 'username':'password'
```

The response body includes ID and status information.

```
{
  "result": {
    "app_service": {
      "sys_id": "5780cb604061f410f87713b656474271",
      "name": "Test Register",
      "number": " SNSVC0001014"
    },
    "message": "Service registered successfully",
    "status": "INSERT"
  }
}
```

## SG Services – POST /sg\_services/app\_service/relationship/create

Constructs upstream relations such as business applications, business service offerings, and other application services.

This API creates a relationship, taking input with a single parent and a corresponding child object.

The following properties for identifying a CI take precedence as follows:

1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.

### URL format

Versioned URL: `/api/sn_service_graph/{api_version}/sg_services/app_service/relationship/create`

Default URL: `/api/sn_service_graph/sg_services/app_service/relationship/create`

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

child

</td><td>

Information identifying the child application service with which to create a relationship.A dynamic CI group can be added as a child but cannot be parent.

Data type: Object

```
"child": {
  "<service_app_identifier>": "String"
}
```

Table: Service Instance \[cmdb\_ci\_service\_auto\]

</td></tr><tr><td>

child.&lt;service\_app\_identifier&gt;

</td><td>

Details identifying the child application service with which to create a relationship.Only one option is required. Each option is listed by processing precedence:

-   sys\_id: Sys\_id of the child application service.
-   number: Unique number that identifies the child application service.
-   &lt;IRE field name&gt;: IRE fields identifying the application service. For example, name or version.

Data type: String

</td></tr><tr><td>

parent

</td><td>

Details identifying the parent application service with which to create a relationship.Data type: Object

```
"parent": {
  "<service_app_identifier>": "String",
  "class_name": "String"
}
```

</td></tr><tr><td>

parent.&lt;service\_app\_identifier&gt;

</td><td>

Information identifying the application service.Only one option is required. Each option is listed by processing precedence:

-   sys\_id: Sys\_id the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\].
-   number: Unique number that identifies the application service.
-   &lt;IRE field name&gt;: One or more IRE fields identifying the application service. For example, name or version.

Data type: String

</td></tr><tr><td>

parent.class\_name

</td><td>

Name of the class that contains the application service.The parent class name should be from one of the following tables:

-   cmdb\_ci\_business\_app
-   cmdb\_ci\_service\_auto
-   cmdb\_ci\_service\_by\_tags
-   cmdb\_ci\_service\_calculated
-   cmdb\_ci\_service\_discovered
-   service\_offering

Default: cmdb\_ci\_service\_auto

Data type: String

</td></tr></tbody>
</table>### Headers

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
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or the user does not have the app\_service\_admin role.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_iyx_jnx_gqb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Indicates success or failure.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how create a relationship from an application service.

```
curl "https://instance.service-now.com/api/sn_service_graph/sg_services/app_service/relationship/create" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"child\": {
   \"name\": \"wdfsdf\",
   \"environment\": \"Test\",
   \"version\": \"1.0\"
   },
  \"parent\": {
   \"sys_id\": \"abcdefg\",
   \"name\": \"business App1\",
   \"class_name\": \"service_offering\"
  }
}" \
--user 'username':'password'
```

Results indicating a successful creation of an application service relationship.

```
{
  "result": {
  "status": "success"
  }
}
```

## SG Services – POST /sg\_services/app\_service/relationship/delete

Deletes an application service upstream relationship.

The following properties for identifying a CI take precedence as follows:

1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.

### URL format

Versioned URL: `/api/sn_service_graph/{api_version}/sg_services/app_service/relationship/delete`

Default URL: `/api/sn_service_graph/sg_services/app_service/relationship/delete`

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

child

</td><td>

Information describing the child relationship to be deleted from the service application.Data type: Object

 ```
"child": {
  "<IRE field name>": "String",
  "number": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

child.&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the child application service. For example, name or version.Data type: String

</td></tr><tr><td>

child.number

</td><td>

Unique number that identifies the child application service.Data type: String

</td></tr><tr><td>

child.sys\_id

</td><td>

Sys\_id of the child application service listed in the Service Instance \[cmdb\_ci\_service\_auto\].Data type: String

</td></tr><tr><td>

parent

</td><td>

Details identifying the parent application service from which to remove a relationship.Data type: Object

 ```
"parent": {
  "<IRE field name>": "String",
  "number": "String",
  "sys_id": "String",
  "class_name": "String"
}
```

</td></tr><tr><td>

parent.&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version. Data type: String

</td></tr><tr><td>

parent.number

</td><td>

Unique number that identifies the application service. Data type: String

</td></tr><tr><td>

parent.sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\] table. Data type: String

</td></tr><tr><td>

parent.class\_name

</td><td>

Name of the class that contains the application service.The parent class name should be from one of the following tables:

-   cmdb\_ci\_service\_auto
-   cmdb\_ci\_service\_discovered
-   cmdb\_ci\_service\_by\_tags
-   cmdb\_ci\_service\_calculated
-   service\_offering
-   cmdb\_ci\_business\_app

 Default: cmdb\_ci\_service\_auto

 Data type: String

</td></tr></tbody>
</table>### Headers

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
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or the user does not have the app\_service\_admin role.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Indicates success or failure.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to remove a relationship from an application service.

```
curl "https://instance.service-now.com/api/sn_service_graph/sg_services/app_service/relationship/delete" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"child\": {
  \"name\": \"Test Register\",
  \"environment\": \"Test\",
  \"version\": \"1.0\"

  },
  \"parent\": {
   \"sys_id\": \"abcdefg\",
   \"name\": \"business App1\",
   \"class_name\": \"service_offering\"
     }
 }" \
--user 'username':'password'
```

Results indicating a successful removal of an application service relationship.

```
{
  "result": {
  "status": "success"
  }
}
```

## SG Services – POST /sg\_services/app\_service/state

Changes the application service lifecycle state to activate, deactivate, or retire.

The following properties for identifying a CI take precedence as follows:

1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.

### URL format

Versioned URL: `/api/sn_service_graph/{api_version}/sg_services/app_service/state`

Default URL: `/api/sn_service_graph/sg_services/app_service/state`

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

<table id="table_h3q_lsx_gqb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version. Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the application service. Data type: String

</td></tr><tr><td>

state

</td><td>

Required. Lifecycle state of the application service. Valid values:

-   ACTIVATE – Life cycle is operational and in use.
    -   life\_cycle\_stage=Operational
    -   life\_cycle\_stage\_status=In Use
    -   operational\_status=Operational
-   DEACTIVATE – Life cycle is not operational and is in the design stage.
    -   life\_cycle\_stage=Design
    -   life\_cycle\_stage\_status=Build
    -   operational\_status=Non-Operational
-   RETIRE – End of life.
    -   life\_cycle\_stage=End Of Life
    -   life\_cycle\_stage\_status=Retired
    -   operational\_status=Retired

Data type: String

Stored in: Service Instance \[cmdb\_ci\_service\_auto\]

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\] table. Data type: String

</td></tr></tbody>
</table>### Headers

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
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or the user does not have the app\_service\_admin role.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_iyx_jnx_gqb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Indicates success or failure.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to change an application service lifecycle state to activate.

```
curl "https://instance.service-now.com/api/sn_service_graph/sg_services/app_service/state" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  {
  \"name\": \"Test Register\",
  \"environment\": \"Test\",
  \"version\": \"1.0\",
  \"state\": \"activate\"
  }
}" \
--user 'username':'password'
```

Results indicating a successful operation.

```
{
  "result": {
  "status": "success"
  }
}
```

## SG Services – POST /sg\_services/app\_service/update

Updates an existing application service provided and creates tags for the given application service.

The following properties for identifying a CI take precedence as follows:

1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.

### URL format

Versioned URL: `/api/sn_service_graph/{api_version}/sg_services/app_service/update`

Default URL: `/api/sn_service_graph/sg_services/app_service/update`

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
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;fields or tags to update&gt;

</td><td>

Use key-value pairs to identify each field or tag to be updated.Only basic information can be updated, no upstream relationships can be updated.

 Data type: String

</td></tr><tr><td>

&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version. You can send the sys\_id, number or IRE to identify an application service; however, none of these fields can be updated when used as an identifier. To update the IRE fields, input should include the sys\_id or number as an identifier.

 Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the application service. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\] table. Data type: String

</td></tr></tbody>
</table>### Headers

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
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or the user does not have the app\_service\_admin role.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_iyx_jnx_gqb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version. Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the application service. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\] table. Data type: String

</td></tr><tr><td>

&lt;updated fields&gt;

</td><td>

If the update is successful, each modified field sent in the payload is listed in the response body.

</td></tr></tbody>
</table>### cURL request

The following example shows how to update an application service, using name as an IRE field.

```
curl "https://instance.service-now.com/api/sn_service_graph/sg_services/app_service/update" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  {
   \"name\": \"Test Register\",
   \"environment\": \"Test\",
   \"version\": \"1.0\"
  }
}" \
--user 'username':'password'
```

Response includes application service identification information and updated fields.

```
{
  "result": {
  "sys_id": "123456",
  "number": "SVCKji0w9e",
  "name": "Test Register",
  "environment": "Test",
  "version": "1.0"
  }
}
```

