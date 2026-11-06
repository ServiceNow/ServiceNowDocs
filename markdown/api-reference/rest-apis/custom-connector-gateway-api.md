---
title: Custom Connector Gateway API
description: The Custom Connector Gateway \(XCC\) API provides an asynchronous ingest endpoint.Adds or overwrites a document in the AI Search index.Maps an external user identity to a ServiceNow user and their group memberships, enabling document ACLs to be enforced at search time.Deletes every document in the index for this connector.Removes all user principal mappings for this connector.Deletes all documents for this connector that match an AI Search query.Deletes a single document from the index by its ID.Removes a single user principal mapping for this connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/rest-apis/custom-connector-gateway-api.html
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-09-28"
reading_time_minutes: 24
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Custom Connector Gateway API

The Custom Connector Gateway \(XCC\) API provides an asynchronous ingest endpoint.

The Custom Connector Gateway \(XCC\) API provides an asynchronous ingest endpoint for document and principal operations into ServiceNow AI Search.

**Max request body size:** 100 MB.

## About the Gateway Model

ServiceNow's built-in External Content Connectors use a pull model: ServiceNow reaches out to the data source. This breaks when your data is behind a firewall that ServiceNow can't reach, or when no prebuilt connector exists for your source.

The Custom Connector Gateway flips the model. You run a connector in your own environment and push data to ServiceNow. ServiceNow handles the indexing. This API is your ingest surface.

For more information, see [Custom Connector Gateway external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/custom-connector-gateway-external-content-connector.md).

## Authentication - Two Layers Required

Every call to this gateway requires an **XCC JWT**, which is distinct from the OAuth access token used with the Glide instance. Obtain it in two steps:

**Step 1 - OAuth access token** \(from the Glide instance\):

```
POST https://<instance>.service-now.com/oauth_token.do
Content-Type: application/x-www-form-urlencoded
grant_type=client_credentials&client_id=...&client_secret=...
```

Cache the returned `access_token` and refresh proactively before `expires_in` elapses.

**Step 2 - XCC JWT** \(from the Glide instance, using the OAuth token\):

```
GET  https://<instance>.service-now.com/api/sn_ext_conn/xcc_api/jwt/<schema_table>/fetch
POST https://<instance>.service-now.com/api/sn_ext_conn/xcc_api/jwt/<schema_table>/generate
Authorization: Bearer <oauth_access_token>
```

Use `/fetch` to retrieve a cached JWT; fall back to `/generate` to mint a fresh one. The `<schema_table>` scopes the token to a specific index schema. The XCC JWT expires - re-acquire on a cadence \(every 55 minutes is typical\).

Pass the XCC JWT as the `x-xcc-access-token` header on every call to this gateway. Note that the gateway is a **separate service** from the Glide instance and may run on a different hostname.

## End-to-End Crawl Flow

For each crawl run, follow this sequence:

1.  Auth - mint an OAuth access token, then mint an XCC JWT.
2.  Principal sync \(optional\) - connect to LDAP, resolve user and group identities, and sync via `ADDPRINCIPAL` so ServiceNow knows your users.
3.  Record `crawl_start_millis` - capture the epoch-millisecond timestamp before sending any documents.
4.  Discover and ingest - walk your source, encode each file as base64, build an `ADDDOCUMENT` payload with ACLs, and POST to this endpoint.
5.  Stale content cleanup - after all documents are sent, issue a `DELETEBYQUERY` to remove anything with `indexeddate < crawl_start_millis`. AI Search auto-populates `indexeddate` on every ingested document; you don't set it.

When a file is deleted from your source between crawls, it will not be re-ingested, and the cleanup query removes it from the index automatically.

## Requires

-   plugin: `sn_ext_conn` \(External Content Connectors\)
-   role: `ais__admin`
-   crawler role: `snc_internal` for the integration-user that the client-crawler will use.

## Namespace

**Base URI**: `/xcc-ingest` \(on the XCC Gateway host, not the Glide instance\)

**Parent Topic:**[REST API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/api-rest.md)

## Custom Connector Gateway API - POST /xcc-ingest \(ADDDOCUMENT\)

Adds or overwrites a document in the AI Search index.

### URL format

**Note:** Available versions are specified in the [REST API Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_CustomWebServices.md).

Versioned URL: `/xcc-ingest`

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
|None|This endpoint does not accept query parameters.|

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

operation

</td><td>

Operation type. Value for this topic: ADDDOCUMENT.Data type: String

Required.

</td></tr><tr><td>

connector

</td><td>

Connector identifier. Scopes this document to a specific connector configuration in ServiceNow. Must match the connector registered in the XCC schema.Data type: String

Required.

Example: `my_connector`

</td></tr><tr><td>

id

</td><td>

Stable, unique identifier for this document within the connector's scope. If a document with this ID already exists, it is replaced. Use a SHA-256 hash of the absolute file path to generate a deterministic ID: the same file always maps to the same ID across crawl runs.Data type: String

Required.

Example: `a3f2c1d0e5b4908172634f5e6a7b8c9d`

</td></tr><tr><td>

url

</td><td>

Source URL of the document in your system. ServiceNow displays this as the click-through link in search results. Use a URL that resolves to the document in your source system, even if it is behind a firewall.Data type: String

Required.

Example: `https://internal.company.com/docs/report.pdf`

</td></tr><tr><td>

file\_content

</td><td>

Base64-encoded binary content of the document. AI Search extracts text from the decoded bytes for full-text indexing. Base64 encoding increases payload size by approximately 33% - a 75 MB file becomes a ~100 MB payload, which is the gateway's maximum request size.Data type: String

Required.

Example: `SGVsbG8gV29ybGQ=`

</td></tr><tr><td>

fields

</td><td>

Document metadata as key-to-string-array pairs. All values must be arrays of strings even for single-valued fields. Common metadata keys used by the reference file-system connector.Data type: Object

Required.

Example: `{"file_name": ["report.pdf"], "file_path": ["/data/reports/report.pdf"], "file_size": ["245832"], "file_type": ["pdf"]}`

</td></tr><tr><td>

acls

</td><td>

Access control list for an `ADDDOCUMENT` request. Controls which ServiceNow users can see this document in search results.Exactly one of the following must be true:

-   `everyone: true` - all authenticated ServiceNow users can see the document
-   `none: true` - no one can see the document \(useful for staging\)
-   At least one entry in `user_allow` or `group_allow` with `everyone: false`

Map your source system's permissions to ACL fields. For POSIX filesystems.

Use the same user and group identifiers you registered via `ADDPRINCIPAL` - the `glide_user` value for users, and the group names from the `groups` array.

Data type: Object

Required.

</td></tr><tr><td>

acls.everyone

</td><td>

When `true`, all authenticated ServiceNow users can see this document. Set to `false` when using `user_allow` or `group_allow`.Data type: Boolean

Optional.

</td></tr><tr><td>

acls.none

</td><td>

When `true`, no user can see this document. Useful for temporarily suppressing content without deleting it.Data type: Boolean

Optional.

Example: `false`

</td></tr><tr><td>

acls.user\_allow

</td><td>

ServiceNow user identifiers \(typically email addresses\) who are allowed to see this document. Must correspond to `glide_user` values registered via `ADDPRINCIPAL`.Data type: Array

Optional.

Example: `["john.doe@company.com"]`

</td></tr><tr><td>

acls.group\_allow

</td><td>

ServiceNow group names whose members are allowed to see this document. Must correspond to group names registered via `ADDPRINCIPAL`.Data type: Array

Optional.

Example: `["Engineering"]`

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

x-xcc-access-token

</td><td>

XCC JWT obtained from the XCC API on the Glide instance. This is the schema-scoped token from `/api/sn_ext_conn/xcc_api/jwt/<schema_table>/fetch` or `.../generate`, &lt;b&gt;not&lt;/b&gt; the OAuth access token used to mint it. The gateway validates this JWT against the schema before processing the payload. Data type: String

Example: `eyJhbGciOiJSUzI1NiJ9...`.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None|This endpoint returns no custom response headers.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|202|Request accepted for asynchronous processing. The payload has been received by the gateway and will be forwarded to the AI Search index. There is no synchronous confirmation of indexing success - monitor the connector's status in ServiceNow if confirmation is needed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|
|503|Concurrency limit reached. The gateway is at capacity. Back off and retry with exponential delay.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Always `SUCCESS` for a 202 response.Data type: String

</td></tr><tr><td>

message

</td><td>

Human-readable confirmation message.Data type: String

Example: `Successfully delivered ingest request.`

</td></tr></tbody>
</table>### cURL request

Example POST request to `/xcc-ingest`.

```
curl "https://instance.servicenow.com/xcc-ingest" \
--request POST \
--header "Accept:application/json" \
--header "x-xcc-access-token: <token>" \
--header "Content-Type:application/json" \
--data '{
  "operation": "ADDDOCUMENT",
  "connector": "my_connector",
  "id": "a3f2c1d0e5b4908172634f5e6a7b8c9d",
  "url": "https://internal.company.com/docs/report.pdf",
  "file_content": "SGVsbG8gV29ybGQ=",
  "fields": {
    "file_name": [
      "report.pdf"
    ],
    "file_path": [
      "/data/reports/report.pdf"
    ],
    "file_size": [
      "245832"
    ],
    "file_type": [
      "pdf"
    ]
  },
  "acls": {},
  "acls.everyone": false,
  "acls.none": false,
  "acls.user_allow": [
    "john.doe@company.com"
  ],
  "acls.group_allow": [
    "Engineering"
  ]
}'
```

```
{
  "result": {
    "status": "SUCCESS",
    "message": "Successfully delivered ingest request."
  }
}
```

## Custom Connector Gateway API - POST /xcc-ingest \(ADDPRINCIPAL\)

Maps an external user identity to a ServiceNow user and their group memberships, enabling document ACLs to be enforced at search time.

### URL format

**Note:** Available versions are specified in the [REST API Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_CustomWebServices.md).

Versioned URL: `/xcc-ingest`

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
|None|This endpoint does not accept query parameters.|

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

operation

</td><td>

Operation type. Value for this topic: ADDPRINCIPAL.Data type: String

Required.

</td></tr><tr><td>

connector

</td><td>

Connector identifier.Data type: String

Required.

Example: `my_connector`

</td></tr><tr><td>

user

</td><td>

External user identifier in the source system. For the file-system connector, this is the POSIX username \(e.g., `jdoe`\). Must match the owner values used in `acls.user_allow` when ingesting documents.Data type: String

Required.

</td></tr><tr><td>

glide\_user

</td><td>

The ServiceNow user identifier that maps to this external user. Typically the user's email address in ServiceNow \(the `mail` attribute from LDAP\). ServiceNow uses this mapping to evaluate `user_allow` ACLs at search time.Data type: String

Required.

Example: `john.doe@company.com`

</td></tr><tr><td>

groups

</td><td>

Complete list of groups this user belongs to, expressed as ServiceNow group names. Replaces the user's entire group membership - does not append. Send all groups every time. ServiceNow uses this list to evaluate `group_allow` ACLs at search time.Data type: Array

Optional.

Example: `["Engineering", "All-Employees"]`

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

x-xcc-access-token

</td><td>

XCC JWT obtained from the XCC API on the Glide instance. This is the schema-scoped token from `/api/sn_ext_conn/xcc_api/jwt/<schema_table>/fetch` or `.../generate`, &lt;b&gt;not&lt;/b&gt; the OAuth access token used to mint it. The gateway validates this JWT against the schema before processing the payload.Data type: String

Example: `eyJhbGciOiJSUzI1NiJ9...`.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None|This endpoint returns no custom response headers.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|202|Request accepted for asynchronous processing. The payload has been received by the gateway and will be forwarded to the AI Search index. There is no synchronous confirmation of indexing success - monitor the connector's status in ServiceNow if confirmation is needed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|
|503|Concurrency limit reached. The gateway is at capacity. Back off and retry with exponential delay.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Always `SUCCESS` for a 202 response.Data type: String

</td></tr><tr><td>

message

</td><td>

Human-readable confirmation message.Data type: String

Example: `Successfully delivered ingest request.`

</td></tr></tbody>
</table>### cURL request

Example POST request to `/xcc-ingest`.

```
curl "https://instance.servicenow.com/xcc-ingest" \
--request POST \
--header "Accept:application/json" \
--header "x-xcc-access-token: <token>" \
--header "Content-Type:application/json" \
--data '{
  "operation": "ADDPRINCIPAL",
  "connector": "my_connector",
  "user": "jdoe",
  "glide_user": "john.doe@company.com",
  "groups": [
    "Engineering",
    "All-Employees"
  ]
}'
```

```
{
  "result": {
    "status": "SUCCESS",
    "message": "Successfully delivered ingest request."
  }
}
```

## Custom Connector Gateway API - POST /xcc-ingest \(DELETEALLDOCUMENTS\)

Deletes every document in the index for this connector.

### URL format

**Note:** Available versions are specified in the [REST API Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_CustomWebServices.md).

Versioned URL: `/xcc-ingest`

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
|None|This endpoint does not accept query parameters.|

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

operation

</td><td>

Operation type. Value for this topic: DELETEALLDOCUMENTS.Data type: String

Required.

</td></tr><tr><td>

connector

</td><td>

Connector identifier. All documents indexed under this connector will be removed.Data type: String

Required.

Example: `my_connector`

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

x-xcc-access-token

</td><td>

XCC JWT obtained from the XCC API on the Glide instance. This is the schema-scoped token from `/api/sn_ext_conn/xcc_api/jwt/<schema_table>/fetch` or `.../generate`, &lt;b&gt;not&lt;/b&gt; the OAuth access token used to mint it. The gateway validates this JWT against the schema before processing the payload.Data type: String

Example: `eyJhbGciOiJSUzI1NiJ9...`

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None|This endpoint returns no custom response headers.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|202|Request accepted for asynchronous processing. The payload has been received by the gateway and will be forwarded to the AI Search index. There is no synchronous confirmation of indexing success - monitor the connector's status in ServiceNow if confirmation is needed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|
|503|Concurrency limit reached. The gateway is at capacity. Back off and retry with exponential delay.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Always `SUCCESS` for a 202 response.Data type: String

</td></tr><tr><td>

message

</td><td>

Human-readable confirmation message.Data type: String

Example: `Successfully delivered ingest request.`

</td></tr></tbody>
</table>### cURL request

Example POST request to `/xcc-ingest`.

```
curl "https://instance.servicenow.com/xcc-ingest" \
--request POST \
--header "Accept:application/json" \
--header "x-xcc-access-token: eyJhbGciOiJSUzI1NiJ9..." \
--header "Content-Type:application/json" \
--data '{
  "operation": "DELETEALLDOCUMENTS",
  "connector": "my_connector"
}'
```

```
{
  "result": {
    "status": "SUCCESS",
    "message": "Successfully delivered ingest request."
  }
}
```

## Custom Connector Gateway API - POST /xcc-ingest \(DELETEALLPRINCIPALS\)

Removes all user principal mappings for this connector.

### URL format

**Note:** Available versions are specified in the [REST API Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_CustomWebServices.md).

Versioned URL: `/xcc-ingest`

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
|None|This endpoint does not accept query parameters.|

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

operation

</td><td>

Operation type. Value for this topic: DELETEALLPRINCIPALS.Data type: String

Required.

</td></tr><tr><td>

connector

</td><td>

Connector identifier. All principal mappings for this connector will be removed.Data type: String

Required.

Example: `my_connector`

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

x-xcc-access-token

</td><td>

XCC JWT obtained from the XCC API on the Glide instance. This is the schema-scoped token from `/api/sn_ext_conn/xcc_api/jwt/<schema_table>/fetch` or `.../generate`, &lt;b&gt;not&lt;/b&gt; the OAuth access token used to mint it. The gateway validates this JWT against the schema before processing the payload.Data type: String

Example: `eyJhbGciOiJSUzI1NiJ9...`

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None|This endpoint returns no custom response headers.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|202|Request accepted for asynchronous processing. The payload has been received by the gateway and will be forwarded to the AI Search index. There is no synchronous confirmation of indexing success - monitor the connector's status in ServiceNow if confirmation is needed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|
|503|Concurrency limit reached. The gateway is at capacity. Back off and retry with exponential delay.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Always `SUCCESS` for a 202 response.Data type: String

</td></tr><tr><td>

message

</td><td>

Human-readable confirmation message.Data type: String

Example: `Successfully delivered ingest request.`

</td></tr></tbody>
</table>### cURL request

Example POST request to `/xcc-ingest`.

```
curl "https://instance.servicenow.com/xcc-ingest" \
--request POST \
--header "Accept:application/json" \
--header "x-xcc-access-token: eyJhbGciOiJSUzI1NiJ9..." \
--header "Content-Type:application/json" \
--data '{
  "operation": "DELETEALLPRINCIPALS",
  "connector": "my_connector"
}'
```

```
{
  "result": {
    "status": "SUCCESS",
    "message": "Successfully delivered ingest request."
  }
}
```

## Custom Connector Gateway API - POST /xcc-ingest \(DELETEBYQUERY\)

Deletes all documents for this connector that match an AI Search query.

### URL format

**Note:** Available versions are specified in the [REST API Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_CustomWebServices.md).

Versioned URL: `/xcc-ingest`

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
|None|This endpoint does not accept query parameters.|

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

operation

</td><td>

Operation type. Value for this topic: DELETEBYQUERY.Data type: String

Required.

</td></tr><tr><td>

connector

</td><td>

Connector identifier. Limits the query to documents owned by this connector.Data type: String

Required.

Example: `my_connector`

</td></tr><tr><td>

query

</td><td>

AI Search query language string. Supported forms.`RANGE` query - Delete documents indexed before a timestamp \(stale cleanup\)

```
indexeddate:RANGE(*, 1742208000000, lower=exclusive, upper=exclusive)
```

`RANGE` query - Delete documents indexed after a timestamp \(roll back a bad crawl\)

```
indexeddate:RANGE(1742208000000, *, lower=exclusive, upper=exclusive)
```

`OR` query - Delete a specific list of documents by ID.

```
OR(.id:abc123, .id:def456, .id:ghi789)
```

Field match - Delete all documents where a field equals a value.

```
file_type:pdf
```

The `indexeddate` field value is epoch milliseconds. Record `crawl_start_millis` before the first `ADDDOCUMENT` of the crawl, then use it in the RANGE query at the end of the crawl to remove stale documents.

Data type: String

Required.

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

x-xcc-access-token

</td><td>

XCC JWT obtained from the XCC API on the Glide instance. This is the schema-scoped token from `/api/sn_ext_conn/xcc_api/jwt/<schema_table>/fetch` or `.../generate`, &lt;b&gt;not&lt;/b&gt; the OAuth access token used to mint it. The gateway validates this JWT against the schema before processing the payload.Data type: String

Example: `eyJhbGciOiJSUzI1NiJ9...`

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None|This endpoint returns no custom response headers.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|202|Request accepted for asynchronous processing. The payload has been received by the gateway and will be forwarded to the AI Search index. There is no synchronous confirmation of indexing success - monitor the connector's status in ServiceNow if confirmation is needed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|
|503|Concurrency limit reached. The gateway is at capacity. Back off and retry with exponential delay.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Always `SUCCESS` for a 202 response.Data type: String

</td></tr><tr><td>

message

</td><td>

Human-readable confirmation message.Data type: String

Example: `Successfully delivered ingest request.`

</td></tr></tbody>
</table>### cURL request

Example POST request to `/xcc-ingest`.

```
curl "https://instance.servicenow.com/xcc-ingest" \
--request POST \
--header "Accept:application/json" \
--header "x-xcc-access-token: eyJhbGciOiJSUzI1NiJ9..." \
--header "Content-Type:application/json" \
--data '{
  "operation": "DELETEBYQUERY",
  "connector": "my_connector",
  "query": "indexeddate:RANGE(*, 1742208000000, lower=exclusive, upper=exclusive)"
}'
```

```
{
  "result": {
    "status": "SUCCESS",
    "message": "Successfully delivered ingest request."
  }
}
```

## Custom Connector Gateway API - POST /xcc-ingest \(DELETEDOCUMENT\)

Deletes a single document from the index by its ID.

### URL format

**Note:** Available versions are specified in the [REST API Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_CustomWebServices.md).

Versioned URL: `/xcc-ingest`

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
|None|This endpoint does not accept query parameters.|

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

operation

</td><td>

Operation type. Value for this topic: DELETEDOCUMENT.Data type: String

Required.

</td></tr><tr><td>

connector

</td><td>

Connector identifier. Scopes the deletion to documents owned by this connector.Data type: String

Required.

Example: `my_connector`

</td></tr><tr><td>

id

</td><td>

Identifier of the document to delete. Must exactly match the `id` used when the document was originally ingested.Data type: String

Required.

Example: `a3f2c1d0e5b4908172634f5e6a7b8c9d`

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

x-xcc-access-token

</td><td>

XCC JWT obtained from the XCC API on the Glide instance. This is the schema-scoped token from `/api/sn_ext_conn/xcc_api/jwt/<schema_table>/fetch` or `.../generate`, &lt;b&gt;not&lt;/b&gt; the OAuth access token used to mint it. The gateway validates this JWT against the schema before processing the payload.Data type: String

Example: `eyJhbGciOiJSUzI1NiJ9...`

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None|This endpoint returns no custom response headers.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|202|Request accepted for asynchronous processing. The payload has been received by the gateway and will be forwarded to the AI Search index. There is no synchronous confirmation of indexing success - monitor the connector's status in ServiceNow if confirmation is needed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|
|503|Concurrency limit reached. The gateway is at capacity. Back off and retry with exponential delay.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Always `SUCCESS` for a 202 response.Data type: String

</td></tr><tr><td>

message

</td><td>

Human-readable confirmation message.Data type: String

Example: `Successfully delivered ingest request.`

</td></tr></tbody>
</table>### cURL request

Example POST request to `/xcc-ingest`.

```
curl "https://instance.servicenow.com/xcc-ingest" \
--request POST \
--header "Accept:application/json" \
--header "x-xcc-access-token: eyJhbGciOiJSUzI1NiJ9..." \
--header "Content-Type:application/json" \
--data '{
  "operation": "DELETEDOCUMENT",
  "connector": "my_connector",
  "id": "a3f2c1d0e5b4908172634f5e6a7b8c9d"
}'
```

```
{
  "result": {
    "status": "SUCCESS",
    "message": "Successfully delivered ingest request."
  }
}
```

## Custom Connector Gateway API - POST /xcc-ingest \(DELETEPRINCIPAL\)

Removes a single user principal mapping for this connector.

### URL format

**Note:** Available versions are specified in the [REST API Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_CustomWebServices.md).

Versioned URL: `/xcc-ingest`

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
|None|This endpoint does not accept query parameters.|

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

operation

</td><td>

Operation type. Value for this topic: DELETEPRINCIPAL.Data type: String

Required.

</td></tr><tr><td>

connector

</td><td>

Connector identifier. Scopes the principal removal to this connector.Data type: String

Required.

Example: `my_connector`

</td></tr><tr><td>

user

</td><td>

External user identifier to remove. Must match the `user` value used when the principal was originally registered.Data type: String

Required.

Example: `jdoe`

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

x-xcc-access-token

</td><td>

XCC JWT obtained from the XCC API on the Glide instance. This is the schema-scoped token from `/api/sn_ext_conn/xcc_api/jwt/<schema_table>/fetch` or `.../generate`, &lt;b&gt;not&lt;/b&gt; the OAuth access token used to mint it. The gateway validates this JWT against the schema before processing the payload.Data type: String

Example: `eyJhbGciOiJSUzI1NiJ9...`

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None|This endpoint returns no custom response headers.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|202|Request accepted for asynchronous processing. The payload has been received by the gateway and will be forwarded to the AI Search index. There is no synchronous confirmation of indexing success - monitor the connector's status in ServiceNow if confirmation is needed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|
|503|Concurrency limit reached. The gateway is at capacity. Back off and retry with exponential delay.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Always `SUCCESS` for a 202 response.Data type: String

</td></tr><tr><td>

message

</td><td>

Human-readable confirmation message.Data type: String

Example: `Successfully delivered ingest request.`

</td></tr></tbody>
</table>### cURL request

Example POST request to `/xcc-ingest`.

```
curl "https://instance.servicenow.com/xcc-ingest" \
--request POST \
--header "Accept:application/json" \
--header "x-xcc-access-token: eyJhbGciOiJSUzI1NiJ9..." \
--header "Content-Type:application/json" \
--data '{
  "operation": "DELETEPRINCIPAL",
  "connector": "my_connector",
  "user": "jdoe"
}'
```

```
{
  "result": {
    "status": "SUCCESS",
    "message": "Successfully delivered ingest request."
  }
}
```

