---
title: Data Classification API
description: The Data Classification API provides endpoints to group data by type.Returns a list of all data classifications available in the current domain.Assigns pre-defined or user-defined data classifications to existing dictionary entries.Removes all data classifications for the specified dictionary entries.Retrieves all data classifications for the specified dictionary entries.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Data Classification API

The Data Classification API provides endpoints to group data by type.

With the Data Classification API, you can:

-   Assign data classifications to existing dictionary entries.
-   Look up the data classifications for specific dictionary entries.
-   Remove all data classifications associated with specific dictionary entries.
-   Retrieve a list of all data classifications available in the current domain.

This API requires the Data Classification \[com.glide.data\_classification\] plugin.

For more information, see [Data Classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-classification/data-classification.md).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Data Classification - GET /data\_classification/getAllDataClasses

Returns a list of all data classifications available in the current domain.

Requires the admin, data\_classification\_admin, or data\_classification\_auditor role.

### URL format

Default URL: `/api/now/data_classification/getAllDataClasses`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
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

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Result of the request. Returns the sys\_id and name for each available data classification. If there are no data classifications, it returns an empty array.Data classifications can be organized into parent-child relationships. If there are parent data classifications, they are identified in the result.

Data type: Array of Objects

```
"result": [
  {
    "name": "String",
    "parent": {Object},
    "sys_id": "String"
  }
]
```

</td></tr><tr><td>

result.name

</td><td>

Name of the data classification.Data type: String

</td></tr><tr><td>

result.parent

</td><td>

Entry for a parent data classification.Data type: Object

```
"parent": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.parent.name

</td><td>

Name of the parent data classification.Data type: String

</td></tr><tr><td>

result.parent.sys\_id

</td><td>

Sys\_id of the parent data classification record.Data type: String

Table: Data Classification \[data\_classification\]

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the data classification record.Data type: String

Table: Data Classification \[data\_classification\]

</td></tr></tbody>
</table>### cURL request

Retrieves a list of all the available data classifications.

```
curl "https://instance.servicenow.com/api/now/data_classification/getAllDataClasses" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

```
{
  "result": [
    {
      "parent": {
        "sys_id": "a9670fc773fc1010ae8dd21efaf6a735",
        "name": "Confidential"
      },
      "sys_id": "348107b951d71010f877f3f178e7dd0d",
      "name": "Personally identifiable information"
    },
    {
      "sys_id": "a9670fc773fc1010ae8dd21efaf6a735",
      "name": "Confidential"
    },
    {
      "sys_id": "59b7070b73fc1010ae8dd21efaf6a764",
      "name": "Restricted"
    },
    {
      "sys_id": "11d60fc773fc1010ae8dd21efaf6a744",
      "name": "Internal"
    },
    {
      "sys_id": "f5b4cf4773fc1010ae8dd21efaf6a766",
      "name": "Public"
    }
  ]
}

```

## Data Classification - POST /data\_classification/classify

Assigns pre-defined or user-defined data classifications to existing dictionary entries.

Requires the admin or data\_classification\_admin role.

### URL format

Default URL: `/api/now/data_classification/classify`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dictionary\_entries

</td><td>

Required. Sys\_ids of the records you want to classify. Entered as a comma-separated list enclosed in a string.

Table: Dictionary \[sys\_dictionary\] table

Data type: String

</td></tr><tr><td>

data\_classes

</td><td>

Required. Sys\_ids of the data classifications you want to assign. Entered as a comma-separated list enclosed in a string.

Table: Data Classification \[data\_classification\]

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

</td></tr><tr><td>

Content-Type

</td><td>

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
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Message describing the result of the operation. Data type: String

</td></tr></tbody>
</table>### cURL request

Assigns a data classification to a dictionary entry.

```
curl "https://instance.servicenow.com/api/now/data_classification/classify" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    \"dictionary_entries\": \"445de0a6dba30300efc57416bf9619b0\",
    \"data_classes\": \"40edb1f51bbcec50b92a10a61a4bcb8a\"
}" \
--user 'username':'password'

```

```
{
  "result": "Successfully stored the data classification configurations"
}

```

## Data Classification - POST /data\_classification/clear

Removes all data classifications for the specified dictionary entries.

Requires the admin or data\_classification\_admin role.

### URL format

Default URL: `/api/now/data_classification/clear`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dictionary\_entries

</td><td>

Required. Sys\_ids of the records you want to remove classifications from. Entered as a comma-separated list enclosed in a string.

Table: Dictionary \[sys\_dictionary\]

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

</td></tr><tr><td>

Content-Type

</td><td>

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
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Message describing the result of the operation. Data type: String

</td></tr></tbody>
</table>### cURL request

Clears the data classifications for a dictionary entry.

```
curl "https://instance.servicenow.com/api/now/data_classification/clear" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    \"dictionary_entries\": \"445de0a6dba30300efc57416bf9619b0\"
}" \
--user 'username':'password'

```

```
{
  "result": "Classifications removed for the specified dictionary entries"
}

```

## Data Classification - POST /data\_classification/getClassification

Retrieves all data classifications for the specified dictionary entries.

Requires the admin, data\_classification\_admin, or data\_classification\_auditor role.

### URL format

Default URL: `/api/now/data_classification/getClassification`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dictionary\_entries

</td><td>

Required. Sys\_ids of the records you want to retrieve classifications for. Entered as a comma-separated list enclosed in a string.

Table: Dictionary \[sys\_dictionary\]

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

</td></tr><tr><td>

Content-Type

</td><td>

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
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Result of the request. Returns a JSON object containing each dictionary entry's sys\_id with an array of its associated data classifications. If there are no associated data classifications, it returns a message describing the result of the operation.Data classifications can be organized into parent-child relationships. If there are parent data classifications, they are identified in the result.

Data type: Object

```
"result": {
  <sys_dictionary_sys_id>: [
    {
      "name": "String",
      "parent": {Object},
      "sys_id": "String"
    }
  ]
}
```

</td></tr><tr><td>

result.name

</td><td>

Name of the data classification.Data type: String

</td></tr><tr><td>

result.parent

</td><td>

Entry for a parent data classification.Data type: Object

```
"parent": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

result.parent.name

</td><td>

Name of the parent data classification.Data type: String

</td></tr><tr><td>

result.parent.sys\_id

</td><td>

Sys\_id of the parent data classification record.Data type: String

Table: Data Classification \[data\_classification\]

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the data classification record.Data type: String

Table: Data Classification \[data\_classification\]

</td></tr></tbody>
</table>### cURL request

Get the data classifications associated with a specific dictionary entry.

```
curl "https://instance.servicenow.com/api/now/data_classification/getClassification" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    \"dictionary_entries\": \"445de0a6dba30300efc57416bf9619b0\"
}" \
--user 'username':'password'

```

```
{
  "result": {
    "445de0a6dba30300efc57416bf9619b0": [
      {
        "parent": {
          "sys_id": "a9670fc773fc1010ae8dd21efaf6a735",
          "name": "Confidential"
        },
        "sys_id": "348107b951d71010f877f3f178e7dd0d",
        "name": "Personally identifiable information"
      }
    ]
  }
}

```

