---
title: External Content Ingestion API
description: The External Content Ingestion API provides endpoints that enable ingestion of content from sources outside of your ServiceNow instance into the ServiceNow AI Search application's index.Deletes all external documents that match the specified query from the AI Search index.Deletes the external document with a specified unique identifier from the AI Search index.Sends a list of external documents to the AI Search ingestion batcher for indexing. After indexing completes, content from the ingested documents becomes searchable.Stores binary content as a content object in AI Search.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 19
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# External Content Ingestion API

The External Content Ingestion API provides endpoints that enable ingestion of content from sources outside of your ServiceNow® instance into the ServiceNow® AI Search application's index.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## External Content Ingestion API – DELETE /ais/external\_content/deleteByQuery/\{schema\_table\_name\}

Deletes all external documents that match the specified query from the AI Search index.

### URL format

Versioned URL: `/api/now/{api_version}/ais/external_content/deleteByQuery/{schema_table_name}?query={query}`

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

schema\_table\_name

</td><td>

The name of the external content schema table that defines the schema for the indexed documents to delete. For example, `u_ext_content`.

 Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

query

</td><td>

A valid URL-escaped query for the schema table specified by **schema\_table\_name**. For example, `title=Introduction` to query for documents whose title is `Introduction`.

 Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

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
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Object describing the error encountered during processing of the request.

 Data type: Object

 ```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Details of the error encountered during processing of the request.

 Data type: String

</td></tr><tr><td>

error.message

</td><td>

Message for the error encountered during processing of the request.

 Data type: String

</td></tr><tr><td>

result

</td><td>

Result from a successfully processed request.

 Data type: String

</td></tr><tr><td>

status

</td><td>

Status of an unsuccessful request.

 Valid values:

-   **failure**

 Data type: String

</td></tr></tbody>
</table>### cURL request

Delete documents with title field values `Introduction` and `Report for 31 October 2020` from the u\_ext\_content schema table.

```
curl "https://instance.service-now.com/api/now/v2/ais/external_content/deleteByQuery/u_ext_content?query=title%3DIntroduction%20OR%20title%3DReport%20for%2031%20October%202020" \
--request DELETE \
--user "username":"password" \
--header "Accept: application/json"
```

```
{
  "result": "Delete By Query Successfully Executed"
}
```

## External Content Ingestion API – DELETE /ais/external\_content/deleteDocument/\{schema\_table\_name\}/\{document\_id\}

Deletes the external document with a specified unique identifier from the AI Search index.

### URL format

Versioned URL: `/api/now/{api_version}/ais/external_content/deleteDocument/{schema_table_name}/{document_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

document\_id

</td><td>

The unique identifier for the external document to delete. For example, `ADMIN-2027858531-16`.

 Data type: string

</td></tr><tr><td>

schema\_table\_name

</td><td>

The name of the external content schema table that defines the schema for the indexed document to delete. For example, `u_ext_content`.

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
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Object describing the error encountered during processing of the request.

 Data type: Object

 ```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Details of the error encountered during processing of the request.

 Data type: String

</td></tr><tr><td>

error.message

</td><td>

Message for the error encountered during processing of the request.

 Data type: String

</td></tr><tr><td>

result

</td><td>

Result from a successfully processed request.

 Data type: String

</td></tr><tr><td>

status

</td><td>

Status of an unsuccessful request.

 Valid values:

-   **failure**

 Data type: String

</td></tr></tbody>
</table>### cURL request

Delete the document with identifier `ADMIN-2587918521-27` from the u\_ext\_content schema table.

```
curl 'https://instance.service-now.com/api/now/v2/ais/external_content/deleteDocument/u_ext_content/ADMIN-2587918521-27' \
--request DELETE \
--user 'username':'password' \
--header 'Accept: application/json'
```

```
{
  "result":"Document removed"
}
```

## External Content Ingestion API – POST /ais/external\_content/ingestDocument/\{schema\_table\_name\}

Sends a list of external documents to the AI Search ingestion batcher for indexing. After indexing completes, content from the ingested documents becomes searchable.

You can use this endpoint to feed external documents with text content and metadata.

If you need to associate searchable binary content and metadata with an external document, follow these steps:

1.  Store the binary content in AI Search using the [POST /ais/external\_content/storeContent](external-content-ingestion-api.md#) endpoint. Record the value of the **result** response body parameter.
2.  Send the external document to AI Search using this endpoint. Set the document's **content\_pointer** request body parameter to match the recorded **result** response body parameter value.

During ingestion, AI Search parses the binary content and adds its searchable content to the indexed record that represents the external document. Parsing removes the stored content object.

### URL format

Versioned URL: `/api/now/{api_version}/ais/external_content/ingestDocument/{schema_table_name}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

schema\_table\_name

</td><td>

The name of the external content schema table that defines the schema for external documents in the request. For example, `u_ext_content`.

 Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[array\]

</td><td>

Required. Unnamed array of objects in which each object represents an external document to ingest for indexing.

 Data type: Array

 ```
[
  {
    "content_pointer": "String",
    "document_id": "String",
    "principals": {Object},
    "properties": {Object}
  }
]
```

</td></tr><tr><td>

\[array\].content\_pointer

</td><td>

Identifier for an instance of binary content stored using the [POST /ais/external\_content/storeContent](external-content-ingestion-api.md#) endpoint. During ingestion, AI Search parses the binary content and adds its searchable content to the indexed record that represents the external document. Parsing removes the stored content object.

**Note:** This identifier should match the **result** response body element returned by the storeContent endpoint.

 Data type: String

</td></tr><tr><td>

\[array\].document\_id

</td><td>

Required. Unique identifier for the external document in the external content schema table specified by the **schema\_table\_name** path parameter.

 **Note:** When you ingest a document, it overwrites any existing document in the same external content schema table that has the same **document\_id**. If two or more documents in the same ingestion request have the same **document\_id**, the request fails.

 Data type: String

</td></tr><tr><td>

\[array\].principals

</td><td>

Object containing key-value pairs that describe the external document's access permissions for externally defined security principals \(users and groups\).

**Note:**

If you omit this parameter for a document, the request succeeds, but AI Search rejects the document with the ingestion feedback message `The principal of the document is missing`.

If this parameter object does not include any key-value pairs that grant access to a document, the request succeeds, but AI Search rejects the document with the ingestion feedback message `The principal of the document is invalid`.

 Data type: Object

 ```
"principals": {
  "everyone": Boolean,
  "groups.deny": [Array],
  "groups.read": [Array],
  "none": Boolean,
  "users.deny": [Array],
  "users.read": [Array]
}
```

 Versions supported: Available starting in v2 of the API.

</td></tr><tr><td>

\[array\].principals.everyone

</td><td>

Flag that indicates whether access to the external document is allowed for all users. When this parameter is set to **true**, all ServiceNow AI Platform users can view the indexed record created from the document.

**Note:** If you set both this parameter and **\[array\].principals.none** to **true** for a document, the request succeeds, but AI Search rejects the document with ingestion feedback message `The principal of the document is invalid`. You can only set one of these two parameters to **true** in a request.

 Valid values:

-   **true**: Allow access to the document for all users. AI Search ignores all **\[array\].principals.groups.\*** and **\[array\].principals.users.\*** parameter settings for the document.
-   **false**: Do not allow all users to access the external document. Users can only access the document if **\[array\].principals.none** is set to false and if allowed by the interaction of their user mappings and the **\[array\].principals.groups.\*** and **\[array\].principals.users.\*** parameters.

 Data type: Boolean

 Default: **true**

 Versions supported: Available starting in v2 of the API.

</td></tr><tr><td>

\[array\].principals.groups.deny

</td><td>

Array of strings where each string is the name of an externally defined group that is denied access to the external document. ServiceNow AI Platform users mapped to any of these external groups cannot view the indexed search result record created from the document.

 If either **\[array\].principals.everyone** or **\[array\].principals.none** is set to **true**, this parameter has no effect.

 This parameter takes precedence over **\[array\].principals.groups.read**. If the same user is mapped to external groups with both read and deny access permissions for a document, AI Search denies that user access to the indexed record.

 By default, **\[array\].principals.users.read** takes precedence over this parameter. To reverse this precedence order for an indexed source, see [Change the precedence of user read and group deny permissions for an external content indexed source.](https://www.servicenow.com/docs/access?context=defining-access-perms-ext-docs-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

 Data type: Array

 Values can be in any format, depending on the names of the externally defined groups specified. Examples include:

 ```
"groups.deny": [
  "hr-admin",
  "legal"
]
```

 Versions supported: Available starting in v2 of the API.

</td></tr><tr><td>

\[array\].principals.groups.read

</td><td>

Array of strings where each string is the name of an externally defined group that is allowed to access the external document. ServiceNow AI Platform users mapped to any of these external groups can view the indexed search result record created from the document.

 If either **\[array\].principals.everyone** or **\[array\].principals.none** is set to **true**, this parameter has no effect.

 **\[array\].principals.groups.deny** takes precedence over this parameter. If the same user is mapped to external groups with both read and deny access permissions for a document, AI Search denies that user access to the indexed record.

 Data type: Array

 Values can be in any format, depending on the names of the externally defined groups specified. Examples include:

 ```
"groups.read": [
  "devops",
  "it",
  "report-admins"
]
```

 Versions supported: Available starting in v2 of the API.

</td></tr><tr><td>

\[array\].principals.none

</td><td>

Boolean option indicating whether access to the external document is denied for all users. When this parameter is set to **true**, only ServiceNow AI Platform users with the ais\_high\_security\_admin elevated privilege role can view the indexed record created from the document.

**Note:** If you set both this parameter and **\[array\].principals.everyone** to **true** for a document, AI Search rejects the document during ingestion with error message `The principal of the document is invalid`. You can only set one of these two parameters to **true** in a request.

 Valid values:

-   **true**: Deny access to the document for all users except those with the ais\_high\_security\_admin elevated privilege role. AI Search ignores all **\[array\].principals.groups.\*** and **\[array\].principals.users.\*** parameter settings for the document.
-   **false**: Do not deny access to the document for all users. Users can access the document if **\[array\].principals.everyone** is set to **true**, or if allowed by the interaction of their user mappings and the **\[array\].principals.groups.read** and **\[array\].principals.users.read** parameters.

 Data type: Boolean

 Default: **false**

 Versions supported: Available starting in v2 of the API.

</td></tr><tr><td>

\[array\].principals.users.deny

</td><td>

Array of strings where each string is the name of an externally defined user that is denied access to the external document. ServiceNow AI Platform users mapped to any of these external users cannot view the indexed search result record created from the document.

 If either **\[array\].principals.everyone** or **\[array\].principals.none** is set to **true**, this parameter has no effect.

 This parameter takes precedence over **\[array\].principals.users.read**. If the same user is mapped to external users with both read and deny access permissions for a document, AI Search denies that user access to the indexed record.

 Data type: Array

 Values can be in any format, depending on the names of the externally defined users specified. Examples include:

 ```
"users.deny": [
  "ad\bow-ruggeri",
  "abel-tuter@sharepoint"
]
```

 Versions supported: Available starting in v2 of the API.

</td></tr><tr><td>

\[array\].principals.users.read

</td><td>

Array of strings where each string is the name of an externally defined user that is allowed to access the external document. ServiceNow AI Platform users mapped to any of these external users can view the indexed search result record created from the document.

 If either **\[array\].principals.everyone** or **\[array\].principals.none** is set to **true**, this parameter has no effect.

 **\[array\].principals.users.deny** takes precedence over this parameter. If the same user is mapped to external users with both read and deny access permissions for a document, AI Search denies that user access to the indexed record.

 By default, this parameter takes precedence over **\[array\].principals.groups.deny**. To reverse this precedence order for an indexed source, see [Change the precedence of user read and group deny permissions for an external content indexed source.](https://www.servicenow.com/docs/access?context=defining-access-perms-ext-docs-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

 Data type: Array

 Values can be in any format, depending on the names of the externally defined users specified. Examples include:

 ```
"users.read": [
  "ad\abel-tuter",
  "beth-anglin@sharepoint"
]
```

 Versions supported: Available starting in v2 of the API.

</td></tr><tr><td>

\[array\].properties

</td><td>

Object containing name-value pairs where each pair represents a field name and value to ingest for the document. All field names and values must be specified as strings.

 After ingestion, these document field values are accessible through the indexed source defined for the external content schema table specified by the **schema\_table\_name** path parameter. Users can search for these field values in search sources derived from this indexed source.

 Data type: Object

 Field names can only contain lowercase letters and underscores. Values can include any characters. Value length is limited by the **max\_length** attribute defined for the field in the external content schema table. Examples of field name-value pairs include:

 ```
"properties": {
  "creation_date": "2020-11-03 12:27:43",
  "file_size": "10285",
  "title": "Introduction",
  "url": "file:///myhost/reports/Introduction.pdf"
}
```

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|202|Partial Success. The request was processed. Some documents have ingestion feedback warning or error messages.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Object describing the error encountered during processing of the request.

 Data type: Object

 ```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Details of the error encountered during processing of the request.

 Data type: String

</td></tr><tr><td>

error.message

</td><td>

Message for the error encountered during processing of the request.

 Data type: String

</td></tr><tr><td>

result

</td><td>

JSON-formatted string representing the result object for the ingestion request.

 Data type: String

 ```
"result": "{\"duration_in_ms\": Number, \"feedback\": [Array] }"
```

</td></tr><tr><td>

result.duration\_in\_ms

</td><td>

Time spent ingesting the external documents.

 Data type: Number

 Unit: Milliseconds

</td></tr><tr><td>

result.feedback

</td><td>

Array of objects in which each object represents feedback for a document ingested from the request body.

 Data type: Array

 ```
"feedback": [
  {
    "document_id": "String",
    "messages": [Array]
  }
]
```

</td></tr><tr><td>

result.feedback.document\_id

</td><td>

Unique identifier for the external document as specified in the request body.

 Data type: String

</td></tr><tr><td>

result.feedback.messages

</td><td>

Array of unnamed objects in which each object represents an ingestion feedback message logged during indexing of the external document.

 Data type: Array

 ```
"messages": [
  {
    "code": "String",
    "component": "String",
    "level": "String",
    "message": "String"
  }
]
```

</td></tr><tr><td>

result.feedback.messages.code

</td><td>

Code for an exception thrown by the indexing workflow component that logged the ingestion feedback message.

 Data type: String

</td></tr><tr><td>

result.feedback.messages.component

</td><td>

Identifier for the indexing workflow component that logged the ingestion feedback message.

 Data type: String

</td></tr><tr><td>

result.feedback.messages.level

</td><td>

Logging level for the ingestion feedback message.

 Valid values:

-   **ERROR**
-   **INFO**
-   **MINOR\_ERROR**
-   **WARN**

 Data type: String

</td></tr><tr><td>

result.feedback.messages.message

</td><td>

Text logged for the ingestion feedback message.

 Data type: String

</td></tr><tr><td>

status

</td><td>

Status of an unsuccessful request.

 Valid values:

-   **failure**

 Data type: String

</td></tr></tbody>
</table>### Precedence order for principal permissions

The precedence order for **\[array\].principals** permissions depends on the value of the **user\_read\_takes\_precedence\_over\_group\_deny** attribute for the indexed source used to ingest an external document.

<table id="table_vlm_d2t_vpb"><thead><tr><th>

Attribute value

</th><th>

Precedence order for principal permissions

</th></tr></thead><tbody><tr><td>

true

</td><td>

From highest precedence to lowest:

1.  **\[array\].principals.everyone**, **\[array\].principals.none**
2.  **\[array\].principals.users.deny**
3.  **\[array\].principals.users.read**
4.  **\[array\].principals.groups.deny**
5.  **\[array\].principals.groups.read**

**Note:** This is the default attribute value for external content indexed sources.

</td></tr><tr><td>

false

</td><td>

From highest precedence to lowest:

1.  **\[array\].principals.everyone**, **\[array\].principals.none**
2.  **\[array\].principals.users.deny**, **\[array\].principals.groups.deny**
3.  **\[array\].principals.users.read**, **\[array\].principals.groups.read**

**Note:** For instructions on setting this attribute value, see [Change the precedence of user read and group deny permissions for an external content indexed source](https://www.servicenow.com/docs/access?context=defining-access-perms-ext-docs-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>### cURL request

Feed two external documents \(with content pointers to binary content objects previously stored using the [POST /ais/external\_content/storeContent](external-content-ingestion-api.md#) endpoint\) for indexing into the u\_ext\_content schema table.

```
curl 'https://instance.servicenow.com/api/now/v2/ais/external_content/ingestDocument/u_ext_content' \
  --request POST \
  --user 'username':'password' \
  --header 'Accept: application/json' \
  --header 'Content-Type: application/json' \
  --data '[
  {
    "document_id": "ADMIN-2027858531-16",
    "content_pointer": "749b52a1-baa8-4556-a4f3-00404c95e6a8",
    "properties": {
      "title": "Introduction",
      "url": "file:///myhost/reports/Introduction.pdf",
      "file_name": "Introduction.pdf",
      "file_size": "10285",
      "creation_date": "2020-11-01 12:27:43"
    },
    "principals": {
      "everyone": false,
      "groups.read": [
        "report-users",
        "report-admins"
      ],
      "users.deny": [
        "ad\abel-tuter"
      ]
    }
  },
  {
    "document_id": "ADMIN-2587918521-27",
    "content_pointer": "bd605435-268b-464f-a7c3-0c5ea894a5c2",
    "properties": {
      "title": "Report for 31 August 2020",
      "url": "file:///myhost/reports/Report-2020-08-31.pdf",
      "file_size": "27597",
      "creation_date": "2020-09-01 12:48:13"
    },
    "principals": {
      "everyone": false,
      "groups.read": [
        "report-users",
        "report-admins"
      ],
      "users.read": [
        "ad\beth-anglin"
      ]
    }
  }
]'
```

```
{
  "result":"{\"duration_in_ms\":3822,\"feedback\":[{\"messages\":[{\"level\":\"INFO\",\"message\":\"CREATED\",\"component\":\"init\"},{\"level\":\"INFO\",\"message\":\"OK\",\"component\":\"index-886de18e750030108b23bcd69cdc2dd3-indexer.index-886de18e750030108b23bcd69cdc2dd3-content-dispatcher\"},{\"level\":\"INFO\",\"message\":\"COMPLETED\",\"component\":\"sink.sink\"}],\"document_id\":\"ADMIN-2027858531-16\"},{\"messages\":[{\"level\":\"INFO\",\"message\":\"CREATED\",\"component\":\"init\"},{\"level\":\"WARN\",\"message\":\"field \\u0027text\\u0027 tokens exceed index.maxTokens\",\"code\":\"INDEX_ENGINE-32\",\"component\":\"ingestGlideDocument.standardAnalyzer\"},{\"level\":\"INFO\",\"message\":\"OK\",\"component\":\"index-886de18e750030108b23bcd69cdc2dd3-indexer.index-886de18e750030108b23bcd69cdc2dd3-content-dispatcher\"},{\"level\":\"INFO\",\"message\":\"COMPLETED\",\"component\":\"sink.sink\"}],\"document_id\":\"ADMIN-2587918521-27\"}]}"
}
```

## External Content Ingestion API – POST ais/external\_content/storeContent

Stores binary content as a content object in AI Search.

You can associate stored binary content with an external document by following these steps:

1.  Store the binary content using this endpoint. Record the value of the **result** response body parameter.
2.  Send the external document to AI Search using the [POST /ais/external\_content/ingestDocument/\{schema\_table\_name\}](external-content-ingestion-api.md#) endpoint. Set the document's **content\_pointer** request body parameter to match the recorded **result** response body parameter value.

During ingestion, AI Search parses the binary content and adds its searchable content to the indexed record that represents the external document. Parsing removes the stored content object.

### URL format

Versioned URL: `/api/now/{api_version}/ais/external_content/storeContent`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Parameter

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

|Element|Description|
|-------|-----------|
|\[binary data\]|Required. Binary content to store as a content object in AI Search.|

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Content-Type

</td><td>

Data format of the request body.

 Valid values:

-   **application/msword**
-   **application/octet-stream**
-   **application/pdf**
-   **application/vnd.ms-excel**
-   **application/vnd.ms-powerpoint**
-   **application/vnd.ms-powerpoint.presentation.macroenabled.12**
-   **application/vnd.openxmlformats-officedocument.presentationml.presentation**
-   **application/vnd.openxmlformats-officedocument.presentationml.template**
-   **application/vnd.openxmlformats-officedocument.spreadsheetml.sheet**
-   **application/vnd.openxmlformats-officedocument.wordprocessingml.document**
-   **application/vnd.openxmlformats-officedocument.wordprocessingml.template**
-   **text/html**
-   **text/plain**

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
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Object describing the error encountered during processing of the request.

 Data type: Object

 ```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Details of the error encountered during processing of the request.

 Data type: String

</td></tr><tr><td>

error.message

</td><td>

Message for the error encountered during processing of the request.

 Data type: String

</td></tr><tr><td>

result

</td><td>

Identifier for the binary content object stored by successful request.

 Data type: String

 ```
"result" : "91841766-2a5f-4c64-a20a-27ca485eca21"
```

 **Note:** To attach the stored content to an ingested external document, specify this identifier as the **content\_pointer** request body element for a request to the ingestDocument endpoint.

</td></tr><tr><td>

status

</td><td>

Status of an unsuccessful request.

 Valid values:

-   **failure**

 Data type: String

</td></tr></tbody>
</table>### cURL request

Store binary content for a PDF file as a content object.

```
curl 'https://instance.servicenow.com/api/now/v2/ais/external_content/storeContent' \
--request POST \
--user 'username':'password' \
--header 'Content-Type: application/pdf' \
--data-binary '@Report-2020-08-31.pdf'
```

The response body includes the unique identifier for the new content object.

```
{
  "result" : "fb439a4f-62ad-4dab-9654-5088d99a6ff9"
}
```

