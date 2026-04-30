---
title: AWA Agent Consult API
description: Handles agent consult work items.Ends a consult work item.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-01-21"
reading_time_minutes: 3
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# AWA Agent Consult API

Handles agent consult work items.

This API requires the Advanced Work Assignment plugin \(com.glide.awa\) and the awa\_integration\_user role.

For more information about AWA, see [Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-overview&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

Use the [AWA Offer Work API](awa-offer-work-api.md#) to initiate a consult transfer to an agent or a queue.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## AWA Agent Consult - PUT /now/awa/consult/end

Ends a consult work item.

When a document is consult transferred to an agent, the respective work item must be closed with the appropriate consult state, either `Transferred` or `Ended`.

A work item is a single piece of work handled by an AWA agent from start to finish. A work item is created based on a document, such as an interaction or task.

### URL format

Versioned URL: `/api/now/{api_version}/awa/consult/end`

Default URL: `/api/now/awa/consult/end`

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

document\_sys\_id

</td><td>

Sys\_id of the document associated with the consult work item.A document is any record in any table, such as an interaction, case, or incident.

Data type: String

</td></tr><tr><td>

hand\_over

</td><td>

Flag that indicates whether a consult transfer must be ended or transferred.Valid values:

-   true: Transfer the document to consult agent and set the consult work item’s consult state as `Transferred`.
-   false: Ends the consult transfer and set the consult work item’s consult state as`Ended`.

**Note:** If the consult work item’s consult state is `Requested`, the state changes to `Cancelled`.

Data type: Boolean

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

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td id="entry-400-status-code">

Bad Request. A bad request type or malformed request was detected.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

403

</td><td id="entry-403-status-code-awa">

Forbidden.Possible reasons:

-   The user doesn't have the awa\_integration\_user role.
-   The value of the glide.awa.enabled property isn't `true`. This property is listed in the System Property \[sys\_property\] table if the Advanced Work Assignment \(com.glide.awa\) plugin is installed. For more information, see [Components installed with Advanced Work Assignment](https://www.servicenow.com/docs/access?context=installed-with-awa&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

success

</td><td>

Flag that indicates whether the ending consult is successful.Valid values:

-   true: The ending consult is successful.
-   false: The ending consult is unsuccessful.

Data type: Boolean

</td></tr><tr><td>

message

</td><td>

Success or failure information for the ending consult.Possible values:

-   `Consult is successfully ended.` – Success.
-   `Cannot find the work item for document ID: <api_caller_sys_id>` – Make sure the active consult work item exists for the document.

Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.servicenow.com/api/now/awa/consult/end" \
--request PUT \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data '{
    "document_sys_id": "59616aba87bd5210be070d48dabb35e6",
    "hand_over": "true"
}' \
--user 'username':'password'
```

```
{
  "result": {
    "success": true,
    "message": "Consult is successfully ended."
  }
}
```

