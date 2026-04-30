---
title: Cloud Services Catalog API
description: The Cloud Services Catalog API provides methods related to Day-1 \(provisioning\) and Day-2 \(modification\) operations available in the Cloud Services Catalog, such as creating cloud service stacks and calling resource operation requests. You can also retrieve information about catalog requests, stacks getting status, and other information.Returns a list of resource catalog items based on a given configuration item \(CI\) class.Returns a list of resource catalog items based on a given resource block.Returns a list of catalog items based on the given blueprint of a Provision or Lifecycle catalog type.Returns a list of catalog items based on Provision-type blueprints \(also known as stacks\).Returns the status and details of a given catalog RITM \(request item\).Submits a resource operation request to perform day 2 operations on provisioned resources.Submits a cloud services request. This method accepts provisioned requests for both day 2 operations and stacks or resource operation catalog items.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 28
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Cloud Services Catalog API

The Cloud Services Catalog API provides methods related to Day-1 \(provisioning\) and Day-2 \(modification\) operations available in the Cloud Services Catalog, such as creating cloud service stacks and calling resource operation requests. You can also retrieve information about catalog requests, stacks getting status, and other information.

This API is included in the `now` namespace and requires the sn\_cmp.cloud\_service\_user role. The Cloud Services Catalog \(CSC\) application is available as a separate subscription and requires either the ITOM Enterprise bundle or ITOM Cloud Accelerate product Entitlement.

The Cloud Services Catalog API features actions you perform during Day 2 operations. In the context of this API, resource catalog items refer to catalog items related to Day 2 operations.

To use this API, ensure that you have completed the Cloud Services Catalog guided setup process or have a working configuration where provisioning and catalog operations are working in the UI. For more information about these steps, see [Cloud Services Catalog](https://www.servicenow.com/docs/access?context=csc-home&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Cloud Services Catalog - GET /now/cmp\_catalog\_api/itemsbyciclass

Returns a list of resource catalog items based on a given configuration item \(CI\) class.

### URL format

Default URL: `/api/now/cmp_catalog_api/itemsbyciclass`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ci\_class

</td><td>

Required. Name of the CI class to get the resource catalog items from \(for example, "cmdb\_ci\_vm\_instance"\). Located in the Reference CI Type field in the Configuration Item \[cmdb\_ci\] table.Data type: String

</td></tr><tr><td>

display\_variables

</td><td>

Flag that indicates whether to list catalog item variables associated with each catalog item.Valid values:

-   true: Displays list catalog item variables.
-   false: Doesn't display list catalog item variables.

Data type: Boolean

Default: False

</td></tr><tr><td>

operation\_name

</td><td>

Optional. Name of the operation. Located in the Name column of the resource interface in the OperationSignature \[sn\_cmp\_rb\_op\_signature\] table.**Note:** This parameter can query part or whole of the operation. For example, if you want to list all interfaces starting with "Servicenow", you can set the variable as `operation_name = Servicenow`.

Default: All catalog items of all operation types are returned.

Data type: String

</td></tr><tr><td>

resource\_interface

</td><td>

Optional. Resource interface that the resource catalog item is hosted on. Located in the Name column of the ResourceInterfaces \[sn\_cmp\_rb\_resourceinterface\] table.Data type: String

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
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|405|Invalid method. The functionality is disabled.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td>

Active state of the resource operation catalog item. Possible values:

-   true: The resource operation catalog item is active.
-   false: The resource operation catalog item is inactive.

Data type: String

</td></tr><tr><td>

created\_on

</td><td>

Time stamp from when the resource operation catalog item was created. Format: yyyy-MM-dd HH:mm:ss.

Data type: String

</td></tr><tr><td>

display\_name

</td><td>

Name of the resource interface. Located in the ResourceInterfaces \[sn\_cmp\_rb\_resourceinterface\] table.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the resource operation catalog item.Data type: String

Table: Resource Operation Catalog Item \[sn\_cmp\_rsrc\_opr\_cat\_item\]

</td></tr><tr><td>

name

</td><td>

Name of the resource operation catalog item. Located in the Resource Operation Catalog Item \[sn\_cmp\_rsrc\_opr\_cat\_item\] table.Data type: String

</td></tr><tr><td>

short\_description

</td><td>

Brief description of the resource operation catalog item.Data type: String

Table: Resource Operation Catalog Item \[sn\_cmp\_rsrc\_opr\_cat\_item\]

</td></tr><tr><td>

updated\_on

</td><td>

Time stamp from when the resource operation catalog item was last updated. Required format: yyyy-MM-dd HH:mm:ss.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example requests and returns the status of the request item.

```
curl "https://instance.servicenow.com/api/now/cmp_catalog_api/itemsbyciclass?ci_class=cmdb_ci_vm_instance&resource_interface=Virtual%20Machine%20Store%20Extension%20Interface&operation_name=Execute%20Job%20Template" \
--request GET \ 
--header 'Accept: application/json' \ 
--user 'username':'password'
```

Response:

```
[
  {
    "display_name": "Virtual Server-Virtual Machine Store Extension Interface-Execute Job Template",
    "id": "01b2341a56789012345d6ddeeff7b89fc",
    "created_on": "2019-04-28 12:58:26",
    "updated_on": "2019-04-28 12:58:26",
    "name": "Virtual Server-Virtual Machine Store Extension Interface-Execute Job Template",
    "short_description": "Catalog item to invoke operation",
    "active": true
  }
]
```

## Cloud Services Catalog - GET /now/cmp\_catalog\_api/itemsbyrb

Returns a list of resource catalog items based on a given resource block.

### URL format

Default URL: `/api/now/cmp_catalog_api/itemsbyrb`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

display\_variables

</td><td>

Flag that indicates whether to list catalog item variables associated with each catalog item.Valid values:

-   true: Displays list catalog item variables.
-   false: Doesn't display list catalog item variables.

Data type: Boolean

Default: False

</td></tr><tr><td>

operation\_name

</td><td>

Optional. Name of the operation. Located in the Name column of the resource interface in the OperationSignature \[sn\_cmp\_rb\_op\_signature\] table.**Note:** This parameter can query part or whole of the operation. For example, if you want to list all interfaces starting with "Servicenow", you can set the variable as `operation_name = Servicenow`.

Default: All catalog items of all operation types are returned.

Data type: String

</td></tr><tr><td>

resource\_block

</td><td>

Required. Name of the resource block to get its related resource operation catalog items from \(for example, Virtual Server\).Default: All catalog items of all operation types are returned.

Data type: String

Table: Resource Block \[sn\_cmp\_rb\_resourceblock\]

</td></tr><tr><td>

resource\_interface

</td><td>

Optional. Resource interface that the resource catalog item is hosted on. Located in the Name column of the ResourceInterfaces \[sn\_cmp\_rb\_resourceinterface\] table.Data type: String

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
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|405|Invalid method. The functionality is disabled.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_dbv_lt3_1bc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td>

Active state of the resource operation catalog item. Possible values:

-   true: The resource operation catalog item is active.
-   false: The resource operation catalog item is inactive.

Data type: String

</td></tr><tr><td>

display\_name

</td><td>

Name of the resource interface. Located in the ResourceInterfaces \[sn\_cmp\_rb\_resourceinterface\] table.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the resource operation catalog item.Data type: String

Table: Resource Operation Catalog Item \[sn\_cmp\_rsrc\_opr\_cat\_item\]

</td></tr><tr><td>

name

</td><td>

Name of the resource operation catalog item. Located in the Resource Operation Catalog Item \[sn\_cmp\_rsrc\_opr\_cat\_item\] table.Data type: String

</td></tr><tr><td>

short\_description

</td><td>

Brief description of the resource operation catalog item.Data type: String

Table: Resource Operation Catalog Item \[sn\_cmp\_rsrc\_opr\_cat\_item\]

</td></tr><tr><td>

variables

</td><td>

List of extra details about the resource catalog item. The variables returned in this API vary based on the query parameters that were passed.Data type: Array of Objects

```
"variables": [
  {
    "parameter1": "String",
    "parameter2": "String"
  }
]
```

</td></tr></tbody>
</table>This example list of resource catalog items based on a Virtual Server resource block:

```
curl "https://instance.servicenow.com/api/now/cmp_catalog_api/itemsbyrb?resource_interface=Virtual%20Machine%20Store%20Extension%20Interface&operation_name=Execute%20Job%20Template&resource_block=Virtual%20Server" \
--request GET \ 
--header 'Accept: application/json' \ 
--user 'username':'password'
```

Response:

```
[
  {
    "display_name": "Virtual Server-Virtual Machine Store Extension Interface-Execute Job Template",
    "id": "01b2341a56789012345d6ddeeff7b89fc",
    "created_on": "2019-04-28 12:58:26",
    "updated_on": "2019-04-28 12:58:26",
    "name": "Virtual Server-Virtual Machine Store Extension Interface-Execute Job Template",
    "short_description": "Catalog item to invoke operation",
    "active": true
  }
]
```

## Cloud Services Catalog - GET /now/cmp\_catalog\_api/services

Returns a list of catalog items based on the given blueprint of a Provision or Lifecycle catalog type.

### URL format

Default URL: `/api/now/cmp_catalog_api/services`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

catalog\_type

</td><td>

Optional. Type of catalog item. Accepted values \(case-sensitive\):-   `Provision` - Returns all Blueprint type catalog items.
-   `LifeCycle` - Returns all Day 2 Operation type catalog items.

If the input is empty \(default\), all services of both catalog types are returned.

Data type: String

</td></tr><tr><td>

display\_variables

</td><td>

Flag that indicates whether to list catalog item variables associated with each catalog item.Valid values:

-   true: Displays list catalog item variables.
-   false: Doesn't display list catalog item variables.

Data type: Boolean

Default: False

</td></tr><tr><td>

blueprint\_name

</td><td>

Optional. Name of the blueprint in which to fetch the related catalog items. Located in the Category Item \[sn\_cmp\_bp\_cat\_item\] table. **Note:** This parameter can query part or whole of the blueprint name. For example, if you want to list all blueprints starting with "Servicenow", you can set the variable as `blueprint_name = Servicenow`.

Default: all services of all blueprints are returned.

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
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|405|Invalid method. The functionality is disabled.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_mqx_4y3_1bc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td>

Flag that indicates whether the catalog is active. Possible values:

-   true: Catalog is active.
-   false: Catalog isn't active.

Data type: String

</td></tr><tr><td>

blueprint

</td><td>

Sys\_id of the blueprint.Data type: String

Table: Blueprint \[sn\_cmp\_bp\_blueprint\]

</td></tr><tr><td>

blueprint\_category

</td><td>

Sys\_id of the blueprint category.Data type: String

Table: Cloud Service Category \[sn\_capi\_service\_category\]

</td></tr><tr><td>

blueprint\_category\_name

</td><td>

Name of the blueprint category. Possible values:

-   Access
-   Analytics
-   Application Services
-   Blockchain
-   Business Productivity
-   Compute
-   Config Management
-   Containers
-   Database
-   Developer Tools
-   Event
-   Hybrid Cloud
-   IOT
-   IPAM
-   Loud Balancer
-   Machine Learning
-   Management Tools
-   Marketplace
-   Mobile
-   Network
-   Productivity
-   Security
-   Shell Access
-   Storage
-   Tools
-   Unknown
-   Virtual Reality

Data type: String

Table:Cloud Service Category \[sn\_capi\_service\_category\]

</td></tr><tr><td>

blueprint\_name

</td><td>

Name of the blueprint. Located in the Blueprint \[sn\_cmp\_bp\_blueprint\] table.Data type: String

</td></tr><tr><td>

blueprint\_type

</td><td>

Type of blueprint. Possible value: `Custom Blueprint`

Data type: String

</td></tr><tr><td>

catalog\_name

</td><td>

Name of the catalog.Data type: String

Table: Cloud Catalog Item \[sn\_cmp\_bp\_cat\_item\]

</td></tr><tr><td>

catalog\_type

</td><td>

Type of catalog. Possible values:

-   `1`: Catalog is of type provision.
-   `2`: Catalog is of type lifecycle.

Data type: String

</td></tr><tr><td>

catalog\_type

</td><td>

Type of catalog. Possible values:

-   `1`: Catalog is of type provision.
-   `2`: Catalog is of type lifecycle.

Data type: String

</td></tr><tr><td>

createdOn

</td><td>

Time stamp from when the catalog item was created. Data type: String

</td></tr><tr><td>

createdBy

</td><td>

User that created the catalog item.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the blueprint.Data type: String

Table: Cloud Catalog Item \[sn\_cmp\_bp\_cat\_item\]

</td></tr><tr><td>

last\_updated\_on

</td><td>

Time stamp from when the catalog item was last updated. Data type: String

</td></tr><tr><td>

last\_updated\_by

</td><td>

User that last updated the catalog item, such as an admin or the system. Data type: String

</td></tr><tr><td>

operation

</td><td>

Sys\_id of the operation.Data type: String

Table: OperationSignature \[sn\_cmp\_rb\_op\_signature\]

</td></tr><tr><td>

operation\_name

</td><td>

Name of the operation. Possible values:

-   Deprovision: Deletes resources with a terminated state and updates resource CMDB tables accordingly.
-   ModifyLease: Modifies the lease operation scheduled on provisioned resources.
-   ModifySchedule: Modifies the schedule for provisioned resources.
-   Start: Starts the resources that are in an off state.
-   Stop: Stops the resources that are in an on state.

Data type: String

</td></tr><tr><td>

variables

</td><td>

Details about the list catalog item. The variables returned in this API vary based on the query parameters that are passed in the request.Data type: Array of Objects

```
"variables": [
  {
    "parameter1": "String",
    "parameter2": "String"
  }
]
```

</td></tr></tbody>
</table>This example returns all the catalog items of a Lifecycle type blueprint named "classiclb".

```
curl "https://instance.servicenow.comapi/now/cmp_catalog_api/services?display_variables=true&catalog_type=LifeCycle&blueprint_name=classiclb" \
--request GET \ 
--header 'Accept: application/json' \ 
--user 'username':'password'
```

Response:

```
[
  {
    "catalog_name": "Deprovision",
    "blueprint": "d90d9d80476c46104bf15222516d43b9",
    "blueprint_name": "classiclb",
    "blueprint_category": "57c0dbd9934b22004a9032bfa67ffb79",
    "active": true,
    "category": "86d85478678232005ca552e457415a79",
    "blueprint_category_name": "Compute",
    "shortDescription": "Are you sure you want to perform this operation?",
    "id": "01b2341a56789012345d6ddeeff7b89fc",
    "variables": [
      {
        "id": "a12d34c5678c91234bf45678912d34e4",
        "name": "StackID",
        "question_text": "StackID",
        "default_value": "Not specified"
      }
    ],
    "last_updated_on": "2024-02-19 07:46:03",
    "last_updated_by": "system",
    "catalog_type": "2",
    "created_on": "2024-02-19 07:46:02",
    "created_by": "user@password.com",
    "operation": "a70d51c0476c46104bf15222516d4375",
    "blueprint_type": "Custom Blueprint",
    "operation_name": "Deprovision"
  },
  {
    "catalog_name": "ModifySchedule",
    "blueprint": "d90d9d80476c46104bf15222516d43b9",
    "blueprint_name": "classiclb",
    "blueprint_category": "57c0dbd9934b22004a9032bfa67ffb79",
    "active": true,
    "category": "86d85478678232005ca552e457415a79",
    "blueprint_category_name": "Compute",
    "shortDescription": null,
    "id": "361d55c0476c46104bf15222516d4351",
    "variables": [
      {
        "id": "031d55c0476c46104bf15222516d43af",
        "name": "ScheduleProfile",
        "question_text": "ScheduleProfile",
        "default_value": "Not specified"
      },
      {
        "id": "0b1d55c0476c46104bf15222516d43c9",
        "name": "ScheduleTimeZone",
        "question_text": "ScheduleTimeZone",
        "default_value": "Not specified"
      }
    ],
    "last_updated_on": "2024-02-19 07:45:53",
    "last_updated_by": "system",
    "catalog_type": "2",
    "created_on": "2024-02-19 07:45:52",
    "created_by": "user@password.com",
    "operation": "130d51c0476c46104bf15222516d436c",
    "blueprint_type": "Custom Blueprint",
    "operation_name": "ModifySchedule"
  },
  {
    "catalog_name": "Stop",
    "blueprint": "d90d9d80476c46104bf15222516d43b9",
    "blueprint_name": "classiclb",
    "blueprint_category": "57c0dbd9934b22004a9032bfa67ffb79",
    "active": true,
    "category": "86d85478678232005ca552e457415a79",
    "blueprint_category_name": "Compute",
    "shortDescription": "Are you sure you want to perform this operation?",
    "id": "542dd5c0476c46104bf15222516d43b0",
    "variables": [
      {
        "id": "a02d19c0476c46104bf15222516d4301",
        "name": "StackID",
        "question_text": "StackID",
        "default_value": "Not specified"
      }
    ],
    "last_updated_on": "2024-02-19 07:46:00",
    "last_updated_by": "system",
    "catalog_type": "2",
    "created_on": "2024-02-19 07:45:58",
    "created_by": "user@password.com",
    "operation": "930d51c0476c46104bf15222516d436f",
    "blueprint_type": "Custom Blueprint",
    "operation_name": "Stop"
  },
  {
    "catalog_name": "Cleanup",
    "blueprint": "d90d9d80476c46104bf15222516d43b9",
    "blueprint_name": "classiclb",
    "blueprint_category": "57c0dbd9934b22004a9032bfa67ffb79",
    "active": true,
    "category": "86d85478678232005ca552e457415a79",
    "blueprint_category_name": "Compute",
    "shortDescription": "Are you sure you want to perform this operation?",
    "id": "712d59c0476c46104bf15222516d435c",
    "variables": [
      {
        "id": "da2d59c0476c46104bf15222516d43dc",
        "name": "resourceId",
        "question_text": "ResourceId",
        "default_value": "Not specified"
      },
      {
        "id": "da2d59c0476c46104bf15222516d43e2",
        "name": "operationName",
        "question_text": "OperationName",
        "default_value": "Not specified"
      }
    ],
    "last_updated_on": "2024-02-19 07:46:06",
    "last_updated_by": "system",
    "catalog_type": "2",
    "created_on": "2024-02-19 07:46:04",
    "created_by": "user@password.com",
    "operation": "ab0d51c0476c46104bf15222516d437b",
    "blueprint_type": "Custom Blueprint",
    "operation_name": "Cleanup"
  },
  {
    "catalog_name": "ModifyLease",
    "blueprint": "d90d9d80476c46104bf15222516d43b9",
    "blueprint_name": "classiclb",
    "blueprint_category": "57c0dbd9934b22004a9032bfa67ffb79",
    "active": true,
    "category": "86d85478678232005ca552e457415a79",
    "blueprint_category_name": "Compute",
    "shortDescription": null,
    "id": "bb1dd5c0476c46104bf15222516d4301",
    "variables": [
      {
        "id": "142dd5c0476c46104bf15222516d4382",
        "name": "resourceId",
        "question_text": "ResourceId",
        "default_value": "Not specified"
      },
      {
        "id": "d82dd5c0476c46104bf15222516d4394",
        "name": "operationName",
        "question_text": "OperationName",
        "default_value": "Not specified"
      }
    ],
    "last_updated_on": "2024-02-19 07:45:58",
    "last_updated_by": "system",
    "catalog_type": "2",
    "created_on": "2024-02-19 07:45:56",
    "created_by": "user@password.com",
    "operation": "2b0d51c0476c46104bf15222516d4378",
    "blueprint_type": "Custom Blueprint",
    "operation_name": "ModifyLease"
  },
  {
    "catalog_name": "Start",
    "blueprint": "d90d9d80476c46104bf15222516d43b9",
    "blueprint_name": "classiclb",
    "blueprint_category": "57c0dbd9934b22004a9032bfa67ffb79",
    "active": true,
    "category": "86d85478678232005ca552e457415a79",
    "blueprint_category_name": "Compute",
    "shortDescription": "Are you sure you want to perform this operation?",
    "id": "d71d95c0476c46104bf15222516d4312",
    "variables": [
      {
        "id": "731d95c0476c46104bf15222516d43ae",
        "name": "resourceId",
        "question_text": "ResourceId",
        "default_value": "Not specified"
      },
      {
        "id": "731d95c0476c46104bf15222516d43b4",
        "name": "operationName",
        "question_text": "OperationName",
        "default_value": "Not specified"
      }
    ],
    "last_updated_on": "2024-02-19 07:45:55",
    "last_updated_by": "system",
    "catalog_type": "2",
    "created_on": "2024-02-19 07:45:54",
    "created_by": "user@password.com",
    "operation": "270d51c0476c46104bf15222516d4372",
    "blueprint_type": "Custom Blueprint",
    "operation_name": "Start"
  }
]
```

## Cloud Services Catalog - GET /now/cmp\_catalog\_api/stacks

Returns a list of catalog items based on Provision-type blueprints \(also known as stacks\).

### URL format

Default URL: `/api/now/cmp_catalog_api/stacks`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

blueprint\_name

</td><td>

Optional. Name of the blueprint in which to fetch the related catalog items. Located in the Category Item \[sn\_cmp\_bp\_cat\_item\] table. **Note:** This parameter can query part or whole of the blueprint name. For example, if you want to list all blueprints starting with "Servicenow", you can set the variable as `blueprint_name = Servicenow`.

Default: all services of all blueprints are returned.

Data type: String

</td></tr><tr><td>

display\_variables

</td><td>

Flag that indicates whether to list catalog item variables associated with each catalog item.Valid values:

-   true: Displays list catalog item variables.
-   false: Doesn't display list catalog item variables.

Data type: Boolean

Default: False

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
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|405|Invalid method. The functionality is disabled.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td>

Flag that indicates whether the catalog is active. Possible values:

-   true: Catalog is active.
-   false: Catalog isn't active.

Data type: String

</td></tr><tr><td>

blueprint

</td><td>

Sys\_id of the blueprint.Data type: String

Table: Blueprint \[sn\_cmp\_bp\_blueprint\]

</td></tr><tr><td>

blueprint\_category

</td><td>

Sys\_id of the blueprint category.Data type: String

Table: Cloud Service Category \[sn\_capi\_service\_category\]

</td></tr><tr><td>

blueprint\_category\_name

</td><td>

Name of the blueprint category. Possible values:

-   Access
-   Analytics
-   Application Services
-   Blockchain
-   Business Productivity
-   Compute
-   Config Management
-   Containers
-   Database
-   Developer Tools
-   Event
-   Hybrid Cloud
-   IOT
-   IPAM
-   Loud Balancer
-   Machine Learning
-   Management Tools
-   Marketplace
-   Mobile
-   Network
-   Productivity
-   Security
-   Shell Access
-   Storage
-   Tools
-   Unknown
-   Virtual Reality

Data type: String

Table:Cloud Service Category \[sn\_capi\_service\_category\]

</td></tr><tr><td>

blueprint\_name

</td><td>

Name of the blueprint. Located in the Blueprint \[sn\_cmp\_bp\_blueprint\] table.Data type: String

</td></tr><tr><td>

blueprint\_type

</td><td>

Type of blueprint. Possible value: `Custom Blueprint`

Data type: String

</td></tr><tr><td>

catalog\_name

</td><td>

Name of the catalog.Data type: String

Table: Cloud Catalog Item \[sn\_cmp\_bp\_cat\_item\]

</td></tr><tr><td>

catalog\_type

</td><td>

Type of catalog. Possible values:

-   `1`: Catalog is of type provision.
-   `2`: Catalog is of type lifecycle.

Data type: String

</td></tr><tr><td>

catalog\_type\_name

</td><td>

Name of the catalog type.Possible values:

-   Provision Operation \(Day 1\): Catalog type is named provision.
-   LifeCycle Operation \(Day 2\): Catalog type is named lifecycle.

Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the blueprint.Data type: String

Table: Cloud Catalog Item \[sn\_cmp\_bp\_cat\_item\]

</td></tr><tr><td>

lifecycleOperations

</td><td>

Object containing the life cycle operation's name and sys\_id.Date type: Array of Objects

```
"lifecycleOperations": [
      {
        "id": "String",
        "name": "String"
      }
```

</td></tr><tr><td>

lifecycleOperations.id

</td><td>

Sys\_id of the life cycle operation.Data type: String

Table: OperationSignature \[sn\_cmp\_rb\_op\_signature\]

</td></tr><tr><td>

lifeCycleOperations.name

</td><td>

Type of life cycle operations. Possible values:

-   Cleanup: Cleans up resources with a terminated state.
-   Deprovision: Deletes resources in a terminated state and updates resource CMDB tables accordingly.
-   ModifyLease: Modifies the lease operation scheduled on provisioned resources.
-   ModifySchedule: Performs business hours scheduling on stacks at the time of provisioning or on existing stacks.
-   Start: Starts the resources that are in an off state.
-   Stop: Stops the resources that are in an on state.

Date type: Object

</td></tr><tr><td>

operation

</td><td>

Sys\_id of the operation.Data type: String

Table: OperationSignature \[sn\_cmp\_rb\_op\_signature\]

</td></tr><tr><td>

operation\_name

</td><td>

Name of the operation. Possible values:

-   Deprovision: Deletes resources with a terminated state and updates resource CMDB tables accordingly.
-   ModifyLease: Modifies the lease operation scheduled on provisioned resources.
-   ModifySchedule: Modifies the schedule for provisioned resources.
-   Start: Starts the resources that are in an off state.
-   Stop: Stops the resources that are in an on state.

Data type: String

</td></tr><tr><td>

shortDescription

</td><td>

Brief description of the catalog.Data type: String

</td></tr><tr><td>

template\_name

</td><td>

Name of the template.Data type: String

Table: Cloud Catalog Item \[sn\_cmp\_bp\_cat\_item\]

</td></tr><tr><td>

template\_type

</td><td>

Sys\_id of the template type.Data type: String

Table: Cloud Catalog Item \[sn\_cmp\_bp\_cat\_item\]

</td></tr><tr><td>

template\_cloud\_product\_name

</td><td>

Name of the product.Data type: String

Table: Cloud Catalog Item \[sn\_cmp\_bp\_cat\_item\]

</td></tr><tr><td>

variables

</td><td>

Details about the list catalog item. The variables returned in this API vary based on the query parameters that are passed in the request.Data type: Array of Objects

```
"variables": [
  {
    "parameter1": "String",
    "parameter2": "String"
  }
]
```

</td></tr></tbody>
</table>The following example returns all catalog items in the instance with the provision catalog type.

```
curl "https://instance.servicenow.com/api/now/cmp_catalog_api/stacks" \
--request GET \ 
--header 'Accept: application/json' \ 
--user 'username':'password'
```

Return:

```
[
  {
    "catalog_type": "1",
    "catalog_type_name": "Provision Operation (Day 1)",
    "catalog_name": "classiclb",
    "blueprint": "d90d9d80476c46104bf15222516d43b9",
    "blueprint_name": "classiclb",
    "blueprint_category": "57c0dbd9934b22004a9032bfa67ffb79",
    "blueprint_category_name": "Compute",
    "active": true,
    "category": "8641fe260b212200eff7ef9bb4673a3d",
    "shortDescription": null,
    "id": "07cc9580476c46104bf15222516d43c3",
    "last_updated_on": "2024-02-19 07:46:13",
    "last_updated_by": "user@servicenow.com",
    "blueprint_type": "Cloud Template",
    "template_type": "932f81e49f00320048111f80a57fcf6e",
    "template_name": "CloudFormation Template",
    "template_cloud_product": "52cfc4749f00320048111f80a57fcf9a",
    "template_cloud_product_name": "AWS CloudFormation",
    "lifecycleOperations": [
      {
        "id": "1d2d19c0476c46104bf15222516d4392",
        "name": "Deprovision"
      },
      {
        "id": "361d55c0476c46104bf15222516d4351",
        "name": "ModifySchedule"
      },
      {
        "id": "542dd5c0476c46104bf15222516d43b0",
        "name": "Stop"
      },
      {
        "id": "712d59c0476c46104bf15222516d435c",
        "name": "Cleanup"
      },
      {
        "id": "bb1dd5c0476c46104bf15222516d4301",
        "name": "ModifyLease"
      },
      {
        "id": "d71d95c0476c46104bf15222516d4312",
        "name": "Start"
      }
    ],
    "created_on": "2024-02-19 07:44:44",
    "created_by": "user@servicenow.com",
    "operation": "130d51c0476c46104bf15222516d4368",
    "operation_name": "Provision"
  }
]
```

## Cloud Services Catalog - GET /now/cmp\_catalog\_api/status

Returns the status and details of a given catalog RITM \(request item\).

Use this method to identify and trace the request's origin and monitor its flow. The response includes the following:

1.  RITM number for the submitted request
2.  The stage the request is in
3.  The users who opened and is assigned the request
4.  The group assigned to the request
5.  When the request was opened
6.  The state the request is in
7.  Submission data

### URL format

Default URL: `/api/now/cmp_catalog_api/status`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

req\_item

</td><td>

Unique request item number in the Requested Item \[sc\_req\_item\] table. For example, `RITM0000001`.Data type: String

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
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|405|Invalid method. The functionality is disabled.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

assignmentGroup

</td><td>

Group assigned to the request.Data type: String

</td></tr><tr><td>

assignedTo

</td><td>

User email assigned to the request.Data type: String

</td></tr><tr><td>

catItem

</td><td>

Sys\_id of the catalog item request.Data type: String

Table: Cloud Catalog Item \[sn\_cmp\_bp\_cat\_item\]

</td></tr><tr><td>

error

</td><td>

Message with details about a returned error. Possible error messages:

-   Record Not Found: The request item doesn't exist.
-   User Not Authenticated: The user's credentials aren't authorized to make this request.

Data type: String

</td></tr><tr><td>

number

</td><td>

Unique Request Item Number \(RITM\) given to the new request item.Data type: String

Table: Request Item \[sc\_req\_item\]

</td></tr><tr><td>

openedAt

</td><td>

Time stamp from when the request item was opened. Format: yyyy-MM-dd HH:mm:ss.

Date type: String

</td></tr><tr><td>

openedBy

</td><td>

Sys\_id of the user who opened the request.Data type: String

</td></tr><tr><td>

stage

</td><td>

Current processing stage of the request item. Possible values:

-   Deploying Stack
-   Deployment Cancelled
-   Deployment Failed
-   Deployment Successful
-   Resource Limit Exceeded
-   Retrying Stack Deployment
-   Task Created for User
-   Waiting for Provision Approval

Data type: String

</td></tr><tr><td>

state

</td><td>

Current completion state of the request item.Possible values:

-   Closed Complete
-   Closed Incomplete
-   Closed Skipped
-   Open
-   Pending
-   Work in Progress

Data type: String

</td></tr><tr><td>

submissionData

</td><td>

Information about the request submission, like cloud account, location, application, and cost center data. Submission data varies depending on the request item number passed in the request.Data type: Object

```
"submissionData": "{\"key1\":\"value\", \"key2\":\"value\"}"
}
```

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the request item record.Data type: String

Table: Request Item \[sc\_req\_item\]

</td></tr></tbody>
</table>### cURL request

The following example returns status information for the request item number, RITM0010076.

```
curl "https://instance.servicenow.com/api/now/cmp_catalog_api/statusreq_item=RITM0010076" \
--request GET \ 
--header 'Accept: application/json' \ 
--user 'username':'password'
```

Response:

```
{ 
  "catItem": "39737024c390719005091d75e0013115", 
  "stage": "Task Created for User", 
  "sys_id": "ee1197db476cc2904bf15222516d439f", 
  "assignedTo": null, 
  "assignmentGroup": null, 
  "number": "RITM0010072", 
  "openedAt": "2024-02-29 18:32:55", 
  "openedBy": "6816f79cc0a8016401c5a33be04be441", 
  "state": "Open", 
  "submissionData": "{\"CloudAccount\":\"AzureCA\",\"CSC_Azure_Functions_newResourceGroup\":\"test-rg-dnd\",\"CSC_Azure_Functions_runTimeVersion\":\"~18\",\"CSC_Azure_Functions_runTimeEngine\":\"node\",\"CSC_Azure_Functions_os\":\"Windows\",\"CSC_Azure_Functions_functionAppName\":\"sa02291029-fa\",\"LeaseEndDate\":\"2024-05-29 17:29:57\",\"ScheduleProfile\":\"-- No Schedule --\",\"UserGroup\":\"cfcbad03d711110050f5edcb9e61038f\",\"CSC_Azure_Functions_applicationName\":\"function-app\",\"ScheduleTimeZone\":\"America/Los_Angeles\",\"BusinessService\":\"\",\"environment\":\"Production\",\"CostCenter\":\"\",\"UseExistingWorkspace\":false,\"CSC_Azure_Functions_existingResourceGroup\":\"cpg-dnd\",\"CSC_Azure_Functions_isNewResourceGroup\":\"false\",\"CSC_Azure_Functions_storageAccountName\":\"sa02291029fasa\",\"Application\":\"\",\"StackName\":\"sa02291029\",\"Location\":\"Azure Datacenter - eastus\",\"Workspace\":\"\"}" 
}
```

## Cloud Services Catalog - POST /now/cmp\_catalog\_api/submitoprequest

Submits a resource operation request to perform day 2 operations on provisioned resources.

### URL format

Default URL: `/api/now/cmp_catalog_api/submitoprequest`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table id="table_urr_lqw_cbc" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cat\_id

</td><td>

Required. sys\_id of the cloud catalog item to invoke. Available in the Cloud Catalog Item \[sn\_cmp\_bp\_cat\_item\] table.Data type: String

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CloudAccount

</td><td>

Required. Name of the cloud account in which to submit the request. Account names are available in the Cloud Account \[cmdb\_ci\_cmp\_cloud\_account\] table.Data type: String

</td></tr><tr><td>

Location

</td><td>

Required. Datacenter location in which to provision the resource. For example, `us-west-1` or `asia-south-2`. This value should match the datacenter location of the cloud account's platform provider. Available in the Associated Datacenter \[sn\_cmp\_ca\_assc\_datacenter\] table. Data type: String

</td></tr><tr><td>

StackName

</td><td>

Required. Name of the stack. The stack name is dynamic and is reflected in resource management.Data type: String

</td></tr><tr><td>

resourceId

</td><td>

Required. Sys\_id of the resource where Day 2 operations will be performed.Data type: String

Table: Stack Items \[sn\_cmp\_stack\_item\]

</td></tr><tr><td>

resource\_block

</td><td>

Required. Name of the resource block to get its related resource operation catalog items from \(for example, Virtual Server\).Default: All catalog items of all operation types are returned.

Data type: String

Table: Resource Block \[sn\_cmp\_rb\_resourceblock\]

</td></tr><tr><td>

operation\_name

</td><td>

Optional. Name of the operation. Located in the Name column of the resource interface in the OperationSignature \[sn\_cmp\_rb\_op\_signature\] table. The operation name you enter depends on the value passed in the **resourceBlock** parameter.**Note:** This parameter can query part or whole of the operation. For example, if you want to list all interfaces starting with "Servicenow", you can set the variable as `operation_name = Servicenow`.

Default: All catalog items of all operation types are returned.Data type: String

</td></tr><tr><td>

resourceInterface

</td><td>

Required. Name of the resource block to get its related resource operation catalog items from \(for example, Virtual Server\). The resource interface you enter depends on the value passed in the **resourceBlock** and **operation\_name** parameters.Default: All catalog items of all operation types are returned.

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
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|405|Invalid method. The functionality is disabled.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_m3n_ndj_1bc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

assignmentGroup

</td><td>

Group assigned to the request.Data type: String

</td></tr><tr><td>

assignedTo

</td><td>

User email assigned to the request.Data type: String

</td></tr><tr><td>

catItem

</td><td>

Sys\_id of the catalog item request.Data type: String

Table: Cloud Catalog Item \[sn\_cmp\_bp\_cat\_item\]

</td></tr><tr><td>

number

</td><td>

Unique Request Item Number \(RITM\) given to the new request item.Data type: String

Table: Request Item \[sc\_req\_item\]

</td></tr><tr><td>

openedAt

</td><td>

Time stamp from when the request item was opened. Format: yyyy-MM-dd HH:mm:ss.

Date type: String

</td></tr><tr><td>

openedBy

</td><td>

Sys\_id of the user who opened the request.Data type: String

</td></tr><tr><td>

stage

</td><td>

Current processing stage of the request item. Possible values:

-   Deploying Stack
-   Deployment Cancelled
-   Deployment Failed
-   Deployment Successful
-   Resource Limit Exceeded
-   Retrying Stack Deployment
-   Task Created for User
-   Waiting for Provision Approval

Data type: String

</td></tr><tr><td>

state

</td><td>

Current completion state of the request item.Possible values:

-   Closed Complete
-   Closed Incomplete
-   Closed Skipped
-   Open
-   Pending
-   Work in Progress

Data type: String

</td></tr><tr><td>

submissionData

</td><td>

Information about the request submission, like cloud account, location, application, and cost center data. Submission data varies depending on the request item number passed in the request.Data type: Object

```
"submissionData": "{\"key1\":\"value\", \"key2\":\"value\"}"
}
```

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the request item record.Data type: String

Table: Request Item \[sc\_req\_item\]

</td></tr></tbody>
</table>The following example creates a Day 2 operation request item.

```
curl "https://instance.servicenow.com/api/now/cmp_catalog_api/submitoprequest?cat_id=e44dcd238731e5101126cbb4dabb3506" /
--request POST\ 
--header 'Accept: application/json' \ 
--user 'username':'password'

//Request body:
{"StackName":"sa02292143","CloudAccount":"AWS","Location":"AWS Datacenter - us-east-1","resourceId":"df8c61e3eb2cc210d298fbbdbad0cd74","operationName":"Deprovision","resourceInterface":"S3 Interface","resourceBlock":"S3"}
```

Response body:

```
{ 
  "number": "RITM0010078", 
  "catItem": "e44dcd238731e5101126cbb4dabb3506", 
  "stage": "request_approved", 
  "sys_id": "9bf5cab3c3594610bc89b33605013190", 
  "assignedTo": null, 
  "assignmentGroup": null, 
  "openedAt": "2024-04-08 09:08:47", 
  "openedBy": "6816f79cc0a8016401c5a33be04be441", 
  "state": "Open", 
  "submissionData": "{\"StackName\":\"sa02292143\",\"CloudAccount\":\"AWS\",\"Location\":\"AWS Datacenter - us-east-1\",\"resourceId\":\"df8c61e3eb2cc210d298fbbdbad0cd74\",\"operationName\":\"Deprovision\",\"resourceInterface\":\"S3 Interface\",\"resourceBlock\":\"S3\"}" 
} 
 
Sample Request Body for CSC S3 Bucket Catalog Order: 
 
{"StackName":"sa02292143","CloudAccount":"AWS","Location":"AWS Datacenter - us-east-1","resourceId":"df8c61e3eb2cc210d298fbbdbad0cd74","operationName":"Deprovision","resourceInterface":"S3 Interface","resourceBlock":"S3"}
```

## Cloud Services Catalog - POST /now/cmp\_catalog\_api/submitrequest

Submits a cloud services request. This method accepts provisioned requests for both day 2 operations and stacks or resource operation catalog items.

### URL format

Default URL: `/api/now/cmp_catalog_api/submitrequest`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cat\_id

</td><td>

Required. sys\_id of the cloud catalog item to invoke. Available in the Cloud Catalog Item \[sn\_cmp\_bp\_cat\_item\] table.Data type: String

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CloudAccount

</td><td>

Required. Name of the cloud account in which to submit the request. Account names are available in the Cloud Account \[cmdb\_ci\_cmp\_cloud\_account\] table.Data type: String

</td></tr><tr><td>

Location

</td><td>

Required. Datacenter location in which to provision the resource. For example, `us-west-1` or `asia-south-2`. This value should match the datacenter location of the cloud account's platform provider. Available in the Associated Datacenter \[sn\_cmp\_ca\_assc\_datacenter\] table. Data type: String

</td></tr><tr><td>

StackName

</td><td>

Required. Name of the stack. The stack name is dynamic and is reflected in resource management.Data type: String

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

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|405|Invalid method. The functionality is disabled.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_m3n_ndj_1bc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

assignmentGroup

</td><td>

Group assigned to the request.Data type: String

</td></tr><tr><td>

assignedTo

</td><td>

User email assigned to the request.Data type: String

</td></tr><tr><td>

catItem

</td><td>

Sys\_id of the catalog item request.Data type: String

Table: Cloud Catalog Item \[sn\_cmp\_bp\_cat\_item\]

</td></tr><tr><td>

number

</td><td>

Unique Request Item Number \(RITM\) given to the new request item.Data type: String

Table: Request Item \[sc\_req\_item\]

</td></tr><tr><td>

openedAt

</td><td>

Time stamp from when the request item was opened. Format: yyyy-MM-dd HH:mm:ss.

Date type: String

</td></tr><tr><td>

openedBy

</td><td>

Sys\_id of the user who opened the request.Data type: String

</td></tr><tr><td>

stage

</td><td>

Current processing stage of the request item. Possible values:

-   Deploying Stack
-   Deployment Cancelled
-   Deployment Failed
-   Deployment Successful
-   Resource Limit Exceeded
-   Retrying Stack Deployment
-   Task Created for User
-   Waiting for Provision Approval

Data type: String

</td></tr><tr><td>

state

</td><td>

Current completion state of the request item.Possible values:

-   Closed Complete
-   Closed Incomplete
-   Closed Skipped
-   Open
-   Pending
-   Work in Progress

Data type: String

</td></tr><tr><td>

submissionData

</td><td>

Information about the request submission, like cloud account, location, application, and cost center data. Submission data varies depending on the request item number passed in the request.Data type: Object

```
"submissionData": "{\"key1\":\"value\", \"key2\":\"value\"}"
}
```

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the request item record.Data type: String

Table: Request Item \[sc\_req\_item\]

</td></tr></tbody>
</table>The following example submits a cloud resource request in the instance's AWS Cloud Account.

```
curl "https://instance.servicenow.com/api/now/cmp_catalog_api/submitrequest?cat_id=022e3deec3122910a769f44ed40131b9" /
--request POST \ 
--header 'Accept: application/json' \ 
--user 'username':'password'

//Request body:
{"CloudAccount":"AWS","Location":"us-east-1","StackName":"ss"}
```

Response:

```
{ 
  "number": "RITM0010001", 
  "catItem": "022e3deec3122910a769f44ed40131b9", 
  "stage": "check_permissions", 
  "sys_id": "86d34233c3594610bc89b336050131dd", 
  "assignedTo": null, 
  "assignmentGroup": null, 
  "openedAt": "2024-04-08 08:59:25", 
  "openedBy": "6816f79cc0a8016401c5a33be04be441", 
  "state": "Open", 
  "submissionData": "{\"CloudAccount\":\"AWS\",\"Location\":\"us-east-1\",\"StackName\":\"ss\"}" 
}
```

