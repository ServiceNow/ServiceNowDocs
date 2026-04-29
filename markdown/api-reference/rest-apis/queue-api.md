---
title: AWA Routing API
description: The AWA Routing API provides endpoints to route a document to a queue.If an active work item exists, routes a document to a queue. If an active work item does not exist for the specified document, creates a work item and set its fields accordingly.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# AWA Routing API

The AWA Routing API provides endpoints to route a document to a queue.

This API requires the Advanced Work Assignment plugin \(com.glide.awa\) and the awa\_integration\_user role.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## AWA Routing - POST /now/awa/queues/\{queue\_sys\_id\}/work\_item

If an active work item exists, routes a document to a queue. If an active work item does not exist for the specified document, creates a work item and set its fields accordingly.

### URL format

Versioned URL: `/api/now/{api_version}/awa/queues/{queue_sys_id}/work_item`

Default URL: `/api/now/awa/queues/{queue_sys_id}/work_item`

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

queue\_sys\_id

</td><td>

Sys\_id of the queue record.Data type: String

Table: Queue \[awa\_queue\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

document\_sys\_id

</td><td>

Sys\_id of the document to route to the queue.Data type: String

</td></tr><tr><td>

document\_table

</td><td>

Name of the table associated with the document, such as incident.Data type: String

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
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

display\_name

</td><td>

Name of the document to route by this work item, such as case record.Data type: String

</td></tr><tr><td>

document\_sys\_id

</td><td>

Sys\_id of the document to route to the queue.Data type: String

</td></tr><tr><td>

document\_table

</td><td>

Name of the table associated with the document.Data type: String

</td></tr><tr><td>

queue\_sys\_id

</td><td>

Sys\_id of the queue on which to route a document.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the work item assigned to the queue.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl -X POST \
  https://instance.servicenow.com/api/now/awa/queues/339eed3f3b892300a2bac9bb34efc4c3/work_item \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-u 'username':'password'
-d '{
  "document_sys_id": "9c573169c611228700193229fff72400",
  "document_table": "incident"
}'
```

```
{
  "result": {
    "sys_id": "cd57f90ddbb26300db2051735e9619f0",
    "document_table": "incident",
    "document_sys_id": "9c573169c611228700193229fff72400",
    "queue_sys_id": "339eed3f3b892300a2bac9bb34efc4c3",
    "display_name": "Incident: INC0000001"
  }
}
```

