---
title: AI Search External User Mapping API
description: The AI Search External User Mapping API provides endpoints that enable ingestion of user mapping information from external sources into the ServiceNow AI Search application's index.Imports a list of external user mappings into an AI Search user mapping table. Each mapping specifies externally defined user and group aliases for a ServiceNow AI Platform user. AI Search uses these aliases to determine which external document search results the user can view.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# AI Search External User Mapping API

The AI Search External User Mapping API provides endpoints that enable ingestion of user mapping information from external sources into the ServiceNow® AI Search application's index.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## AI Search External User Mapping - POST /ais/external\_content/user\_mapping/import\_multiple/\{target\_table\}

Imports a list of external user mappings into an AI Search user mapping table. Each mapping specifies externally defined user and group aliases for a ServiceNow AI Platform user. AI Search uses these aliases to determine which external document search results the user can view.

To learn how AI Search external content security utilizes external user mappings, see [External content security for AI Search](https://www.servicenow.com/docs/access?context=external-content-security-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

User and group names in external user mappings should match those specified in security access permissions for external documents ingested via the External Content Ingestion API's POST /ais/external\_content/ingestDocument/\{schema\_table\_name\} endpoint. For more information on ingesting external documents with security access permissions for externally defined users and groups, see [External Content Ingestion API](external-content-ingestion-api.md#).

To view import histories for external user mapping records imported through this endpoint, navigate to **AI Search** &gt; **External Content** &gt; **User mapping import history**. From a history record, you can view the Import Set \[sys\_import\_set\] and Multi Import Set \[sys\_multi\_import\_set\] records for an import task. Use information from these records to verify that your external user mappings were imported correctly.

### URL format

Versioned URL: `/api/now/{api_version}/ais/external_content/user_mapping/import_multiple/{target_table}`

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

target\_table

</td><td>

The name of the AI Search user mapping table that you want the imported mappings to appear in. For example, `x_snc_sharepoint_user_table`.

**Note:** You must create the target AI Search user mapping table via the **AI Search** &gt; **External Content** &gt; **Create User Mapping** module before using this endpoint. If you specify a user mapping table that does not exist, the request fails.

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

\{object\}

</td><td>

Required. Unnamed object.

 Data type: Object

 ```
{
  "records": [Array]
}
```

</td></tr><tr><td>

\{object\}.records

</td><td>

Required. Array of objects in which each object represents a user mapping to import into the specified target table.

 Data type: Array

 ```
"records": [
  {
    "external_group": [Array],
    "external_user": [Array],
    "mapping_value": "String"
  }
]
```

</td></tr><tr><td>

\{object\}.records.external\_group

</td><td>

Array of strings where each string is the name of an externally defined group to set as an alias for the ServiceNow AI Platform user specified by the **\{object\}.records.mapping\_value** parameter.

 Data type: Array

 Values can be in any format, depending on the names of the externally defined groups selected for the user mapping. Examples include:

 ```
"external_group": [
  "itil",
  "hr-admin",
  "report-dev"
]
```

</td></tr><tr><td>

\{object\}.records.external\_user

</td><td>

Array of strings where each string is the name of an externally defined user to set as an alias for the ServiceNow AI Platform user specified by the **\{object\}.records.mapping\_value** parameter.

 Data type: Array

 Values can be in any format, depending on the names of the externally defined user accounts selected for the user mapping. Examples include:

 ```
"external_user": [
  "beth-anglin",
  "ad\beth.anglin",
  "beth-anglin@sharepoint"
]
```

</td></tr><tr><td>

\{object\}.records.mapping\_value

</td><td>

**Email** field value that uniquely identifies an existing record. All externally defined user and group aliases in the request are mapped to the ServiceNow AI Platform user with this email address.

**Note:** The API treats this parameter as the unique identifier for the user mapping record. If you import another user mapping with the same **mapping\_value** as an existing user mapping record, the new record overwrites the existing record.

 Data type: String

 Table: User \[sys\_user\]

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
|201|Successful. The request was successfully processed.|
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

import\_set\_id

</td><td>

Sys\_id for the new record created in the Import Set \[sys\_import\_set\] table by a successful request.

 Data type: String

</td></tr><tr><td>

multi\_import\_set\_id

</td><td>

Sys\_id for the new record created in the Multi Import Set \[sys\_multi\_import\_set\] table by a successful request.

 Data type: String

</td></tr><tr><td>

result

</td><td>

Result for an unsuccessful request. Includes a message describing the reason for the request failure.

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

Import externally defined user and group aliases for ServiceNow AI Platform users Beth Anglin and Abel Tuter into an AI Search user mapping table named x\_snc\_sharepoint\_user\_table.

```
curl -X POST 'https://instance.servicenow.com/api/now/v1/ais/external_content/user_mapping/import_multiple/x_snc_sharepoint_user_table' \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -u 'username':'password' \
  -d '{
    "records": [
      {
        "mapping_value": "beth.anglin@example.com",
        "external_user": [
          "ad\beth-anglin",
          "beth.anglin@sharepoint"
        ],
        "external_group": [
          "itil",
          "itil-admin",
          "itil-dev"
        ]
      },
      {
        "mapping_value": "abel.tuter@example.com",
        "external_user": [
          "ad\abel-tuter",
          "abel.tuter@sharepoint"
        ],
        "external_group": [
          "hr",
          "hr-admin",
          "hr-dev"
        ]
      }
    ]
  }'
```

The response shows the sys\_ids for the generated Import Set and Multi Import Set records.

```
{
  "import_set_id": "6e9ddb629d987010f877878bd9f0e9dd",
  "multi_import_set_id": "269ddb629d987010f877878bd9f0e9de"
}
```

### cURL request

Import invalid request containing an empty mapping record.

```
curl 'https://instance.servicenow.com/api/now/v1/ais/external_content/user_mapping/import_multiple/u_ext_content_user_mapping' \
  --request POST \
  --user 'username':'password' \
  --header 'Accept: application/json' \
  --header 'Content-Type: application/json' \
  --data '{
    "records": [
      {
        "mapping_value": "beth.anglin@example.com",
        "external_user": [
          "ad\beth-anglin",
          "beth.anglin@sharepoint"
        ],
        "external_group": [
          "reports",
          "reports-admin",
          "reports-dev"
        ]
      },
      {}
    ]
  }'

```

The request fails with status 400 and the response indicates the nature of the failure.

```
{
  "result": "Error in processing the message"
}
```

