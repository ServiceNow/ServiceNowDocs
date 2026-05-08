---
title: Continuous Integration and Continuous Delivery \(CICD\) Update Set API
description: The CICD Update Set API provides methods to create, retrieve, preview, commit, and back-out an update set.Retrieves an update set with a given sys\_id and allows you to remove the existing retrieved update set from the instance.Commits multiple update sets in a single request according to the order that they're provided.Previews an update set to check for any conflicts and retrieve progress information about the update set operation.Backs out an installation operation that was performed on an update set with a given sys\_id.Commits an update set with a given sys\_id.Creates a new update set and inserts the new record in the Update Sets \[sys\_update\_set\] table.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 22
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Continuous Integration and Continuous Delivery \(CICD\) Update Set API

The CICD Update Set API provides methods to create, retrieve, preview, commit, and back-out an update set.

This API is associated with the actions you can perform on [system update sets](https://www.servicenow.com/docs/bundle/xanadu-application-development/page/build/system-update-sets/concept/system-update-sets.html) and requires the sn\_cicd.sys\_ci\_automation role and Continuous Integration and Continuous Delivery \(CICD\) REST API \(com.glide.continuousdelivery\) plugin to access it.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## CICD Update Set - POST /api/sn\_cicd/update\_set/retrieve

Retrieves an update set with a given sys\_id and allows you to remove the existing retrieved update set from the instance.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/update_set/retrieve`

Default URL: `/api/sn_cicd/update_set/retrieve`

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

update\_set\_id

</td><td>

Required. Sys\_id of the update set on the source instance from where the update set was retrieved.Table: Update Sets \[sys\_update\_set\]

Data type: String

</td></tr><tr><td>

update\_source\_id

</td><td>

Sys\_id of the remote instance record.Table: Remote Instances \[sys\_update\_set\_source\]

Data type: String

</td></tr><tr><td>

update\_source\_instance\_id

</td><td>

Instance ID of the remote instance.Table: Remote Instances \[sys\_update\_set\_source\]

Data type: String

</td></tr><tr><td>

auto\_preview

</td><td>

Flag that indicates whether to automatically preview the update set after retrieval.Valid values:

-   true: Preview the update set upon retrieval.
-   false: Don't preview the update set upon retrieval.

Data type: Boolean

Default: false

</td></tr><tr><td>

cleanup\_retrieved

</td><td>

Flag that indicates whether to remove the existing retrieved update set from the instance.Valid values:

-   true: Remove the update set.
-   false: Don't remove the update set

Data type: Boolean

Default: false

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_tq1_qdy_qdc" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_lxy_pbx_qdc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="entry-error">

Error message with details about the error.Data type: String

</td></tr><tr><td>

links

</td><td id="entry-link">

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr><td>

links.progress

</td><td id="entry-links_progress">

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr><td>

links.progress.id

</td><td id="entry-progress_id">

Sys\_id containing progress details for the operation. You can use this value when calling the endpoint [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#).Data type: String

</td></tr><tr><td>

links.progress.url

</td><td id="entry-progress_url">

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr><td>

percent\_complete

</td><td id="entry-percent_complete">

Percentage of the request that is complete.Data type: Number

</td></tr><tr><td>

status

</td><td id="entry-status">

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr><td>

status\_detail

</td><td id="entry-status_detail">

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr><td>

status\_label

</td><td id="entry-status_label">

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr><td>

status\_message

</td><td id="entry-status_message">

Additional description of the action's current state, if available.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example retrieves a particular update set with a given sys\_id and instance ID.

```
curl 
"https://instance.servicenow.com/api/sn_cicd/update_set/retrieve?update_set_id=2ce715950d619e10f87785462179bd67&update_source_id=e66613a49d011210f877036c70ae59f7" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'

```

Response body. Shows details about the update set's current status and execution progress.

```
{
  "result": {
    "links": {
      "progress": {
        "id": "e2ea3eedc92dde10f877184664aecd90",
        "url": "https://instance.servicenow.com/api/sn_cicd/progress/e2ea3eedc92dde10f877184664aecd90"
      }
    },
    "status": "0",
    "status_label": "Pending",
    "status_message": "",
    "status_detail": "",
    "error": "",
    "percent_complete": 0
  }
}   

```

## CICD Update Set - POST /api/sn\_cicd/update\_set/commitMultiple

Commits multiple update sets in a single request according to the order that they're provided.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/update_set/commitMultiple`

Default URL: `/api/sn_cicd/update_set/commitMultiple`

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

remote\_update\_set\_ids

</td><td>

Required. List of sys\_ids associated with any update sets to commit. Sys\_ids are committed in the order given in the request.**Note:** You can use the [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#) endpoint to get the remote update set ID.

Data type: String

Table: Retrieved Update Sets \[sys\_remote\_update\_set\]

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

force\_commit

</td><td>

Flag that indicates whether to force commit the update set. This feature is useful when some remote update sets specified in the input are already committed in an earlier operation. This feature also ensures the commit order is obeyed in the order the update sets are provided.Valid values:

-   true: Force commits the update set.
-   false: Doesn't force commit the update set. If the commit isn't forced, the commit fails if the commit order isn't obeyed.

Data type: String

Default: false

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
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Type

</td><td>

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>### Status codes

|Name|Description|
|----|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|404|Not found. The requested item wasn’t found.|
|409|Conflict. The requested item isn’t unique.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table id="table_lxy_pbx_qdc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="entry-error">

Error message with details about the error.Data type: String

</td></tr><tr><td>

links

</td><td id="entry-link">

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr><td>

links.progress

</td><td id="entry-links_progress">

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr><td>

links.progress.id

</td><td id="entry-progress_id">

Sys\_id containing progress details for the operation. You can use this value when calling the endpoint [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#).Data type: String

</td></tr><tr><td>

links.progress.url

</td><td id="entry-progress_url">

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr><td>

percent\_complete

</td><td id="entry-percent_complete">

Percentage of the request that is complete.Data type: Number

</td></tr><tr><td>

status

</td><td id="entry-status">

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr><td>

status\_detail

</td><td id="entry-status_detail">

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr><td>

status\_label

</td><td id="entry-status_label">

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr><td>

status\_message

</td><td id="entry-status_message">

Additional description of the action's current state, if available.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to commit an update with a given sys\_id.

```
curl 
"https://instance.servicenow.com/api/sn_cicd/update_set/commitMultiple?remote_update_set_ids=0a9f45ab9d415e10f877036c70ae5968%2Cc2e89999c9e19e10f877184664aecd40" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{\"force_commit\":\"true\"}" \
--user 'username':'password'

```

Response body.

```
{
  "result": {
    "links": {
      "progress": {
        "id": "3d174aa1c969de10f877184664aecdc0",
        "url": "https://instance.servicenow.com/api/sn_cicd/progress/3d174aa1c969de10f877184664aecdc0"
      }
    },
    "status": "0",
    "status_label": "Pending",
    "status_message": "",
    "status_detail": "",
    "error": "",
    "percent_complete": 0
  }
}
```

## CICD Update Set - POST /api/sn\_cicd/update\_set/preview/\{remote\_update\_set\_id\}

Previews an update set to check for any conflicts and retrieve progress information about the update set operation.

**Note:** If the update set you want to preview doesn't exist on the instance, you must first use the [CICD Update Set - POST /api/sn\_cicd/update\_set/retrieve](cicd-update-set-api.md#) endpoint to retrieve the update set or manually in the UI.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/update_set/preview/{remote_update_set_id}`

Default URL: `/api/sn_cicd/update_set/preview/{remote_update_set_id}`

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

remote\_update\_set\_id

</td><td>

Sys\_id of the update set to preview.Table: Retrieved Update Sets \[sys\_remote\_update\_set\]

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_rbg_n2y_qdc" class="rest_api_request_headers"><thead><tr><th>

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
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Type

</td><td>

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_lxy_pbx_qdc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="entry-error">

Error message with details about the error.Data type: String

</td></tr><tr><td>

links

</td><td id="entry-link">

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr><td>

links.progress

</td><td id="entry-links_progress">

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr><td>

links.progress.id

</td><td id="entry-progress_id">

Sys\_id containing progress details for the operation. You can use this value when calling the endpoint [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#).Data type: String

</td></tr><tr><td>

links.progress.url

</td><td id="entry-progress_url">

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr><td>

percent\_complete

</td><td id="entry-percent_complete">

Percentage of the request that is complete.Data type: Number

</td></tr><tr><td>

status

</td><td id="entry-status">

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr><td>

status\_detail

</td><td id="entry-status_detail">

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr><td>

status\_label

</td><td id="entry-status_label">

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr><td>

status\_message

</td><td id="entry-status_message">

Additional description of the action's current state, if available.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to preview a remote update set using a given ID.

```
curl 
curl "https://instance.servicenow.com/api/sn_cicd/update_set/preview/8f4608d39d89da10f877036c70ae5998" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body.

```
{
  "result": {
    "links": {
      "progress": {
        "id": "54e9c665c969de10f877184664aecd72",
        "url": "https://instance.servicenow.com/api/sn_cicd/progress/54e9c665c969de10f877184664aecd72"
      }
    },
    "status": "0",
    "status_label": "Pending",
    "status_message": "",
    "status_detail": "",
    "error": "",
    "percent_complete": 0
  }
}
```

## CICD Update Set - POST /api/sn\_cicd/update\_set/back\_out

Backs out an installation operation that was performed on an update set with a given sys\_id.

For more information about how the back out operation affects an update set, see Back out an update set.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/update_set/back_out`

Default URL: `/api/sn_cicd/update_set/back_out`

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

rollback\_installs

</td><td>

Flag that indicates whether to rollback the batch installation performed during the update set commit.Possible values:

-   true: Rollback the installation.
-   false: Don't rollback the installation.

Data type: Boolean

Default: true

</td></tr><tr><td>

update\_set\_id

</td><td>

Required. Sys\_id of the update set. Table: Update Sets \[sys\_update\_set\]

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

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Type

</td><td id="d3003e172">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|404|Not found. The requested item wasn’t found.|
|405|Invalid method. The functionality is inactive.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="entry-error">

Error message with details about the error.Data type: String

</td></tr><tr><td>

links

</td><td id="entry-link">

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr><td>

links.progress

</td><td id="entry-links_progress">

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr><td>

links.progress.id

</td><td id="entry-progress_id">

Sys\_id containing progress details for the operation. You can use this value when calling the endpoint [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#).Data type: String

</td></tr><tr><td>

links.progress.url

</td><td id="entry-progress_url">

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr><td>

percent\_complete

</td><td id="entry-percent_complete">

Percentage of the request that is complete.Data type: Number

</td></tr><tr><td>

status

</td><td id="entry-status">

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr><td>

status\_detail

</td><td id="entry-status_detail">

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr><td>

status\_label

</td><td id="entry-status_label">

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr><td>

status\_message

</td><td id="entry-status_message">

Additional description of the action's current state, if available.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to roll back an installation operation on a specific update sys\_id.

```
curl 
"https://instance.servicenow.com/api/sn_cicd/update_set/back_out?update_set_id=73dd24e39dcd1e10f877036c70ae59ae&rollback_installs=false" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
```

Response:

```
{
  "result": {
    "links": {
      "progress": {
        "id": "036bf811c9619e10f877184664aecdcb",
        "url": "https://instance.servicenow.com/api/sn_cicd/progress/036bf811c9619e10f877184664aecdcb"
      }
    },
    "status": "0",
    "status_label": "Pending",
    "status_message": "",
    "status_detail": "",
    "error": "",
    "percent_complete": 0
  }
} 
```

## CICD Update Set - POST /api/sn\_cicd/update\_set/commit/\{remote\_update\_set\_id\}

Commits an update set with a given sys\_id.

When you have previewed an update set and have resolved any issues, you can commit the update set using this endpoint. Committing an update set applies all changes to the instance and creates a local copy of the update set that contains an update record for every change. For more information about committing an update set, see Commit an update set.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/update_set/commit/{remote_update_set_id}`

Default URL: `/api/sn_cicd/update_set/ commit/{remote_update_set_id}`

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

remote\_update\_set\_id

</td><td>

Sys\_id of the update set to commit.**Note:** You can use the [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#) endpoint to get the remote update set ID.

Table: Retrieved Update Sets \[sys\_remote\_update\_set\]

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

force\_commit

</td><td>

Flag that indicates whether to force commit the update set.Valid values:

-   true: Force commits the update set even if you haven't yet previewed it to check for conflicts.
-   false: Doesn't force commit the update set. You must preview the update set before proceeding with the commit.

Data type: String

Default: false

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
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Type

</td><td>

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Name|Description|
|----|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn’t found.|
|409|Conflict. The requested item isn’t unique.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="entry-error">

Error message with details about the error.Data type: String

</td></tr><tr><td>

links

</td><td id="entry-link">

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr><td>

links.progress

</td><td id="entry-links_progress">

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr><td>

links.progress.id

</td><td id="entry-progress_id">

Sys\_id containing progress details for the operation. You can use this value when calling the endpoint [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#).Data type: String

</td></tr><tr><td>

links.progress.url

</td><td id="entry-progress_url">

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr><td>

percent\_complete

</td><td id="entry-percent_complete">

Percentage of the request that is complete.Data type: Number

</td></tr><tr><td>

status

</td><td id="entry-status">

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr><td>

status\_detail

</td><td id="entry-status_detail">

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr><td>

status\_label

</td><td id="entry-status_label">

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr><td>

status\_message

</td><td id="entry-status_message">

Additional description of the action's current state, if available.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example commits the update set with the associated sys\_id.

```
curl 
"https://instance.servicenow.com/api/sn_cicd/update_set/commit/4ee89999c9e19e10f877184664aecd42" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body.

```
{
  "result": {
    "links": {
      "progress": {
        "id": "bf380a11c9e59e10f877184664aecd0e",
        "url": "https://instance.servicenow.com/api/sn_cicd/progress/bf380a11c9e59e10f877184664aecd0e"
      }
    },
    "status": "0",
    "status_label": "Pending",
    "status_message": "",
    "status_detail": "",
    "error": "",
    "percent_complete": 0
  }
}
```

## CICD Update Set - POST /api/sn\_cicd/update\_set/create

Creates a new update set and inserts the new record in the Update Sets \[sys\_update\_set\] table.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/update_set/create`

Default URL: `/api/sn_cicd/update_set/create`

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

description

</td><td>

Description of the update set.Data type: String

Default: null

</td></tr><tr><td>

scope

</td><td>

Required if the **sys\_id** parameter is not passed. The scope name of the application in which to create the new update set.Table: Applications \[sys\_scope\]

Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Required if the **scope** parameter is not passed. Sys\_id of the application in which to create the new update set.Table: Applications \[sys\_scope\]

Data type: String

</td></tr><tr><td>

update\_set\_name

</td><td>

Required. Name to give the update set.Data type: String

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

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Type

</td><td>

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

| | |
|---|---|
|201|The update set was created successfully.|
|400|Bad request. The update set name is null or empty, or both input sys\_id and scope are null or empty.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|409|Conflict. The requested item isn’t unique.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="entry-error">

Error message with details about the error.Data type: String

</td></tr><tr><td>

status

</td><td id="entry-status">

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr><td>

status\_detail

</td><td id="entry-status_detail">

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr><td>

status\_label

</td><td id="entry-status_label">

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr><td>

status\_message

</td><td id="entry-status_message">

Additional description of the action's current state, if available.Data type: String

</td></tr><tr><td>

update\_set\_id

</td><td>

Sys\_id of the created update set. Table: Update Sets \[sys\_update\_set\]

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example demonstrates how to create a new update set with the name `Testupdateset` and the scope set to `sn_test`.

```
curl 
"https://instance.servicenow.com/api/sn_cicd/update_set/create?update_set_name=Testupdateset&scope=sn_test" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body.

```
{
  "result": {
    "status": "2",
    "status_label": "",
    "status_message": "Successfully created update set: Test update set 1",
    "status_detail": "",
    "error": "",
    "update_set_id": "a9a485d1c9a19e10f877184664aecd11"
  }
}
```

