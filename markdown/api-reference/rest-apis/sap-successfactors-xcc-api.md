---
title: SAP SuccessFactors XCC
description: The SAP SuccessFactors XCC API.Uploads the user-to-assignment-profile mapping data file that a SAP SuccessFactors Learning administrator exports, as an attachment on the connector configuration record identified by conn\_sys\_id.Uploads the trainings data file that a SAP SuccessFactors Learning administrator exports, as an attachment on the connector configuration record identified by conn\_sys\_id.Uploads the library-and-assignment-profile-mapping data file that a SAP SuccessFactors Learning administrator exports, as an attachment on the connector configuration record identified by conn\_sys\_id.Queues a user mapping crawl job that reads the connector's most recently uploaded user and library-and-assignment-profile-mapping data files. Updates the access-control relationships AI Search uses to enforce each search user's original document access restrictions.Queues a document crawl job that reads the connector's most recently uploaded trainings, library-and-assignment-profile-mapping, and user data files. Sends the discovered training content and metadata to AI Search for indexing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/rest-apis/sap-successfactors-xcc-api.html
release: brazil
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 12
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# SAP SuccessFactors XCC

The SAP SuccessFactors XCC API.

Automates data uploads and crawl triggers for the SAP SuccessFactors external content connector.

Lets a caller programmatically attach the trainings, library-and-assignment-profile-mapping, and user data CSV \(or zipped CSV\) files that a SAP SuccessFactors Learning administrator exports. Starts the document and user mapping crawls that index that data for AI Search, as an alternative to the connector's admin configuration UI.

This API works with CSV data files from the [Export SAP SuccessFactors Learning data for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/export-sap-successfactors-data-external-content-indexing.md) application.

Supports upload and crawl-start operations.

**Authentication** Supports both HTTP Basic authentication and OAuth 2.0; OAuth is recommended for production integrations.

OAuth 2.0 uses the Resource Owner Password Credentials grant. Register an OAuth client for external APIs in the instance's Application Registry, with a broadly scoped client scope restriction, then request a token:

```
curl -X POST "https://<instance-url>/oauth_token.do" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -d "grant_type=password&client_id=<client_id>&client_secret=<client_secret>&username=<username>&password=<password>"
```

Send the returned token on every request as `Authorization: Bearer <access_token>`.

-   Mapping to ServiceNow Data Model
-   Connector configuration: Uploaded file attachments map to the `sn_ext_conn_sap_sf_configuration` table.
-   Crawl jobs: Crawl-start operations create records in the `sn_ext_conn_connector_job` table.

**Behavioral notes** Both crawl-start operations require the trainings, library-and-assignment-profile-mapping, and user data files to already be attached to the connector configuration. Requests are rejected for if a crawl of the same type is already queued or in progress for that connector. Both return immediately after queuing the crawl job; the crawl itself, including indexing new content and permissions in AI Search, completes asynchronously. Uploads reject files larger than the maximum size allowed by the `com.glide.attachment.max_size` system property \(1 GB by default\).

Requires:

-   plugin: `com.sn_ext_conn_sap_sf` \(External Content Connectors SAP SuccessFactors\)
-   depends on: `com.sn_ext_conn_admin` \(External Content Connectors Admin\)
-   role: Not restricted to a specific role. Every operation requires authentication, and the platform's default Scripted REST access control denies requests from sessions holding the `snc_external` role.

Namespace information:

-   Namespace: `sn_ext_conn_sap_sf`
-   Base URI: `/api/sn_ext_conn_sap_sf/automate_successfactors_connector`

**Parent Topic:**[REST API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/api-rest.md)

## SAP SuccessFactors XCC - PUT /users

Uploads the user-to-assignment-profile mapping data file that a SAP SuccessFactors Learning administrator exports, as an attachment on the connector configuration record identified by conn\_sys\_id.

### URL format

**Note:** Available versions are specified in the [REST API Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_CustomWebServices.md).

Versioned URL: `/api/sn_ext_conn_sap_sf/automate_successfactors_connector/users`

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
</table>|Name|Description|Data type|
|----|-----------|---------|
|None|This endpoint does not accept query parameters.| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

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
|None|This endpoint returns no custom response headers.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|201|Users file uploaded and attached to the connector configuration.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|415| |
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

|Parameter|Description|Data type|
|---------|-----------|---------|
|result|Example: \{"success": true, "message": "principal\_full crawl started successfully", "crawl\_job\_id": "5a6b7c8d9e0f1a2b3c4d5e6f7a8b9c0d"\}.|object|

### cURL request

Example PUT request to `/api/sn_ext_conn_sap_sf/automate_successfactors_connector/users`.

```
curl "https://instance.servicenow.com/api/sn_ext_conn_sap_sf/automate_successfactors_connector/users" \
--request PUT \
--header "Accept:application/json" \
--user 'username':'password'
```

```
{
  "result": {
    "result": {
      "success": true,
      "message": "File uploaded successfully",
      "attachment_sys_id": "a2b3c4d5e6f7a8b9c0d1e2f3a4b5c6d7",
      "content_type": "text/csv",
      "size_bytes": 51340,
      "created_on": "2026-08-19 12:41:18"
    }
  }
}
```

## SAP SuccessFactors XCC - PUT /training

Uploads the trainings data file that a SAP SuccessFactors Learning administrator exports, as an attachment on the connector configuration record identified by conn\_sys\_id.

### URL format

**Note:** Available versions are specified in the [REST API Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_CustomWebServices.md).

Versioned URL: `/api/sn_ext_conn_sap_sf/automate_successfactors_connector/training`

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
</table>|Name|Description|Data type|
|----|-----------|---------|
|None|This endpoint does not accept query parameters.| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

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
|None|This endpoint returns no custom response headers.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|201|Trainings file uploaded and attached to the connector configuration.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|415| |
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

|Parameter|Description|Data type|
|---------|-----------|---------|
|result|Example: \{"success": true, "message": "principal\_full crawl started successfully", "crawl\_job\_id": "5a6b7c8d9e0f1a2b3c4d5e6f7a8b9c0d"\}.|object|

### cURL request

Example PUT request to `/api/sn_ext_conn_sap_sf/automate_successfactors_connector/training`.

```
curl "https://instance.servicenow.com/api/sn_ext_conn_sap_sf/automate_successfactors_connector/training" \
--request PUT \
--header "Accept:application/json" \
--user 'username':'password'
```

```
{
  "result": {
    "result": {
      "success": true,
      "message": "File uploaded successfully",
      "attachment_sys_id": "a2b3c4d5e6f7a8b9c0d1e2f3a4b5c6d7",
      "content_type": "text/csv",
      "size_bytes": 51340,
      "created_on": "2026-08-19 12:41:18"
    }
  }
}
```

## SAP SuccessFactors XCC - PUT /ap\_lib\_mapping

Uploads the library-and-assignment-profile-mapping data file that a SAP SuccessFactors Learning administrator exports, as an attachment on the connector configuration record identified by `conn_sys_id`.

### URL format

**Note:** Available versions are specified in the [REST API Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_CustomWebServices.md).

Versioned URL: `/api/sn_ext_conn_sap_sf/automate_successfactors_connector/ap_lib_mapping`

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
</table>|Name|Description|Data type|
|----|-----------|---------|
|None|This endpoint does not accept query parameters.| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

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
|None|This endpoint returns no custom response headers.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|201|Library-and-assignment-profile-mapping file uploaded and attached to the connector configuration.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|415| |
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

|Parameter|Description|Data type|
|---------|-----------|---------|
|result|Example: \{"success": true, "message": "principal\_full crawl started successfully", "crawl\_job\_id": "5a6b7c8d9e0f1a2b3c4d5e6f7a8b9c0d"\}.|object|

### cURL request

Example PUT request to `/api/sn_ext_conn_sap_sf/automate_successfactors_connector/ap_lib_mapping`.

```
curl "https://instance.servicenow.com/api/sn_ext_conn_sap_sf/automate_successfactors_connector/ap_lib_mapping" \
--request PUT \
--header "Accept:application/json" \
--user 'username':'password'
```

```
{
  "result": {
    "result": {
      "success": true,
      "message": "File uploaded successfully",
      "attachment_sys_id": "a2b3c4d5e6f7a8b9c0d1e2f3a4b5c6d7",
      "content_type": "text/csv",
      "size_bytes": 51340,
      "created_on": "2026-08-19 12:41:18"
    }
  }
}
```

## SAP SuccessFactors XCC - POST /start\_user\_mapping\_crawl

Queues a user mapping crawl job that reads the connector's most recently uploaded user and library-and-assignment-profile-mapping data files. Updates the access-control relationships AI Search uses to enforce each search user's original document access restrictions.

### URL format

Versioned URL: `/api/sn_ext_conn_sap_sf/automate_successfactors_connector/start_user_mapping_crawl`

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
</table>|Name|Description|Data type|
|----|-----------|---------|
|None|This endpoint does not accept query parameters.| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

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
|None|This endpoint returns no custom response headers.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|409| |
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

|Parameter|Description|Data type|
|---------|-----------|---------|
|result|Example: \{"success": true, "message": "principal\_full crawl started successfully", "crawl\_job\_id": "5a6b7c8d9e0f1a2b3c4d5e6f7a8b9c0d"\}.|object|

### cURL request

Example POST request to `/api/sn_ext_conn_sap_sf/automate_successfactors_connector/start_user_mapping_crawl`.

```
curl "https://instance.servicenow.com/api/sn_ext_conn_sap_sf/automate_successfactors_connector/start_user_mapping_crawl" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
```

```
{
  "result": {
    "result": {
      "success": true,
      "message": "principal_full crawl started successfully",
      "crawl_job_id": "5a6b7c8d9e0f1a2b3c4d5e6f7a8b9c0d"
    }
  }
}
```

## SAP SuccessFactors XCC - POST /start\_document\_crawl

Queues a document crawl job that reads the connector's most recently uploaded trainings, library-and-assignment-profile-mapping, and user data files. Sends the discovered training content and metadata to AI Search for indexing.

### URL format

**Note:** Available versions are specified in the [REST API Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_CustomWebServices.md).

Versioned URL: `/api/sn_ext_conn_sap_sf/automate_successfactors_connector/start_document_crawl`

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
</table>|Name|Description|Data type|
|----|-----------|---------|
|None|This endpoint does not accept query parameters.| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

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
|None|This endpoint returns no custom response headers.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|403|Forbidden. The user doesn't have access rights to the specified record.|
|404|Not found. The requested item wasn't found.|
|409| |
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

|Parameter|Description|Data type|
|---------|-----------|---------|
|result|Example: \{"success": true, "message": "principal\_full crawl started successfully", "crawl\_job\_id": "5a6b7c8d9e0f1a2b3c4d5e6f7a8b9c0d"\}.|object|

### cURL request

Example POST request to `/api/sn_ext_conn_sap_sf/automate_successfactors_connector/start_document_crawl`.

```
curl "https://instance.servicenow.com/api/sn_ext_conn_sap_sf/automate_successfactors_connector/start_document_crawl" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
```

```
{
  "result": {
    "result": {
      "success": true,
      "message": "principal_full crawl started successfully",
      "crawl_job_id": "5a6b7c8d9e0f1a2b3c4d5e6f7a8b9c0d"
    }
  }
}
```

