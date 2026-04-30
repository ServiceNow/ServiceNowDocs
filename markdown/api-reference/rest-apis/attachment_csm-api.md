---
title: CSM Attachment API
description: The CSM Attachment API provides endpoints that allow both internal and external users to upload, download, and remove attachments associated with a table and to retrieve attachment metadata.Deletes the specified attachment.Returns the metadata for multiple attachments.Returns the file attachment for the specified attachment sys\_id.Returns the metadata for the attachment file with the specific attachment sys\_id.Uploads a specified binary file as an attachment to a specified record.Uploads a multipart file attachment.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 24
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# CSM Attachment API

The CSM Attachment API provides endpoints that allow both internal and external users to upload, download, and remove attachments associated with a table and to retrieve attachment metadata.

Only attachments associated with tables specified in the **glide.rest.attachment\_csm\_api.allowed\_tables** system property are valid in any of the associated endpoint calls. Any logged in user, both snc\_internal and snc\_external, can access this API. Guests and public users do not have access rights.

This API respects any system limitations on uploaded files, such as maximum file size and allowed attachment types. You can control these settings using the **com.glide.attachment.max\_size** and **glide.attachment.extensions** properties.

By default, this API has a rate limit of 500 per hour for unauthenticated and snc\_external users. For more information about rate limiting, see [Inbound REST API rate limiting](inbound-REST-API-rate-limiting.md).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## CSM Attachment - DELETE /now/attachment\_csm/\{sys\_id\}

Deletes the specified attachment.

### URL format

Versioned URL: `/api/now/{api_version}/attachment_csm/{sys_id}`

Default URL: `/api/now/v1/attachment_csm/{sys_id}`

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

sys\_id

</td><td>

Sys\_id of the attachment to delete. This attachment must belong to one of the tables listed within the **glide.rest.attachment\_csm\_api.allowed\_tables** property in the System Properties \[sys\_properties\] table.Data type: String

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
|None| |

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|204|Successful. Indicates the request completed successfully.|
|400|Bad Request. Indicates that the attachment from this table might not be accessible. Verify that the associated table is included in the **glide.rest.attachment\_csm\_api.allowed\_tables** system property.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|None||

### Sample cURL request

```
curl "https://instance.servicenow.com/api/now/v1/attachment_csm/615ea769c0a80166001cf5f2367302f5" \
--request DELETE \
--user 'username':'password'
```

```
None
```

## CSM Attachment - GET /now/attachment\_csm

Returns the metadata for multiple attachments.

**Note:** You can reference all sysparm query parameters using either their full name or their shortened name \(without the **sysparm\_** prefix\). For example, for **sysparm\_limit** you can also use **limit**.

### URL format

Versioned URL: `/api/now/{api_version}/attachment_csm`

Default URL: `/api/now/v1/attachment_csm`

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

sysparm\_limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. This limit is applied before ACL evaluation. If no records return, including records you have access to, rearrange the record order so records you have access to return first.

**Note:** Unusually large **sysparm\_limit** values can impact system performance.

Data type: Number

Default: 10000

</td></tr><tr id="row_sysparm_offset"><td>

sysparm\_offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

Default: 0

</td></tr><tr><td>

sysparm\_query

</td><td>

Required. Encoded query to use to search for attachments.This parameter must at least contain `sysparm_query=table_name=<table>` where **&lt;table&gt;** can only be those tables specified in the **glide.rest.attachment\_csm\_api.allowed\_tables** property located in the System Properties \[sys\_properties\] table.

For example: `sysparm_query=file_name=kb_knowledge`.

Syntax: `sysparm_query=<col_name><operator><value>`.

-   &lt;col\_name&gt;: Name of the table column to filter against.
-   &lt;operator&gt;: Supports the following values:

    -   =: Exactly matches &lt;value&gt;.
    -   !=: Does not match &lt;value&gt;.
    -   ^: Logically AND multiple query statements.
    -   ^OR: Logically OR multiple query statements.
    -   LIKE: &lt;col\_name&gt; contains the specified string. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   STARTSWITH: &lt;col\_name&gt; starts with the specified string. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   ENDSWITH: &lt;col\_name&gt; ends with the specified string. Only works for &lt;col\_name&gt; fields whose data type is string.
&lt;value&gt;: Value to match against.


All parameters are case-sensitive. Queries can contain more than one entry, such as `sysparm_query=<col_name><operator><value>[<operator><col_name><operator><value>]`.

For example:

`(sysparm_query=caller_id=javascript:gs.getUserID()^active=true)`

Encoded queries also supports order by functionality. To sort responses based on certain fields, use the `ORDERBY` and `ORDERBYDESC` clauses in **sysparm\_query**.

Syntax:

-   `ORDERBY<col_name>`
-   `ORDERBYDESC<col_name>`

For example: `sysparm_query=active=true^ORDERBYnumber^ORDERBYDESCcategory`

This query filters all active records and orders the results in ascending order by number, and then in descending order by category.

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
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_osc_2tj_llb"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Metadata of the requested attachment.Data type: Object

```
"result": {
  "average_image_color": "String",
  "compressed": "String", 
  "content_type": "String",
  "created_by_name": "String",
  "download_link": "String",
  "file_name": "String",
  "image_height": "String",
  "image_width": "String",
  "size_bytes": "String",
  "size_compressed": "String",
  "sys_created_by": "String",
  "sys_created_on": "String",
  "sys_id": "String",
  "sys_mod_count": "String",
  "sys_tags": "String",
  "sys_updated_by": "String",
  "sys_updated_on": "String",
  "table_name": "String",
  "table_sys_id": "String",
  "updated_by_name": "String"
}
```

</td></tr><tr><td>

result.average\_image\_color

</td><td>

If the attachment is an image, the sum of all colors.Data type: String

Unit: RGB or number of pixels.

</td></tr><tr><td>

result.compressed

</td><td>

Flag that indicates whether the attachment file has been compressed.Possible values:

-   true: File has been compressed.
-   false: File has not been compressed.

Data type: String

</td></tr><tr><td>

result.content\_type

</td><td>

Content-type of the associated attachment file, such as image or jpeg or application/x-shockwave-flash.Data type: String

</td></tr><tr><td>

result.created\_by\_name

</td><td>

Full name of entity that originally created the attachment file.Data type: String

</td></tr><tr><td>

result.download\_link

</td><td>

Download URL of the attachment on the ServiceNow instance.Data type: String

</td></tr><tr><td>

result.file\_name

</td><td>

File name of the attachment.Data type: String

</td></tr><tr><td>

result.image\_height

</td><td>

If an image file, the height of the image.Data type: String

Unit: Pixels

</td></tr><tr><td>

result.image\_width

</td><td>

If an image file, the width of the image.Data type: String

Unit: Pixels

</td></tr><tr><td>

result.size\_bytes

</td><td>

Size of the attachment.Data type: String

Unit: Bytes

</td></tr><tr><td>

result.size\_compressed

</td><td>

Size of the compressed attachment file. If the file is not compressed, empty.Data type: String

Unit: Bytes

</td></tr><tr><td>

result.sys\_created\_by

</td><td>

Entity that originally created the attachment file.Data type: String

</td></tr><tr><td>

result.sys\_created\_on

</td><td>

Date and time that the attachment file was initially saved to the instance.Data type: String

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the attachment file.Data type: String

</td></tr><tr><td>

result.sys\_mod\_count

</td><td>

Number of times the attachment file has been modified \(uploaded to the instance\).Data type: String

</td></tr><tr><td>

result.sys\_tags

</td><td>

Any system tags associated with the attachment file.Data type: String

</td></tr><tr><td>

result.sys\_updated\_by

</td><td>

Entity that last updated the attachment file.Data type: String

</td></tr><tr><td>

result.sys\_updated\_on

</td><td>

Date and time that the attachment file was last updated.Data type: String

</td></tr><tr><td>

result.table\_name

</td><td>

Name of the table to which the attachment is associated.Data type: String

</td></tr><tr><td>

result.table\_sys\_id

</td><td>

Sys\_id of the table associated with the attachment.Data type: String

</td></tr><tr><td>

result.updated\_by\_name

</td><td>

Full name of entity that last updated the attachment file.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.service-now.com/api/now/v1/attachment_csm?sysparm_limit=1" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": [
    {
      "table_sys_id": "5054b6f8c0a800060056addcf551ecf8",
      "size_bytes": "462",
      "download_link": "https://instance.service-now.com/api/now/v1/attachment_csm/615ea769c0a80166001cf5f2367302f5/file",
      "sys_updated_on": "2009-05-21 04:12:21",
      "sys_id": "615ea769c0a80166001cf5f2367302f5",
      "image_height": "",
      "sys_created_on": "2009-05-21 04:12:21",
      "file_name": "blocks.swf",
      "sys_created_by": "glide.maint",
      "compressed": "true",
      "average_image_color": "",
      "sys_updated_by": "glide.maint",
      "sys_tags": "",
      "table_name": "content_block_programmatic",
      "image_width": "",
      "sys_mod_count": "0",
      "content_type": "application/x-shockwave-flash",
      "size_compressed": "485",
      "created_by_name": "John Smith",
      "updated_by_name": "John Smith"
    }
  ]
}
```

## CSM Attachment - GET /now/attachment\_csm/\{sys\_id\}/file

Returns the file attachment for the specified attachment sys\_id.

### URL format

Versioned URL: `/api/now/{api_version}/attachment_csm/{sys_id}/file`

Default URL: `/api/now/v1/attachment_csm/{sys_id}/file`

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

sys\_id

</td><td>

Sys\_id of the attachment. This attachment must belong to one of the tables listed within the **glide.rest.attachment\_csm\_api.allowed\_tables** property in the System Properties \[sys\_properties\] table.Data type: String

Table: Attachments \[sys\_attachment\]

</td></tr></tbody>
</table>|Name|Description|
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

</td><td>

Data format of the response body. For example, use `image/jpeg` or `image/png` to accept JPEG or PNG image files exclusively. To allow all image types, specify `image/*`; to allow any file type, specify `*/*`.Default: \*/\*

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|X-Attachment-Metadata|Metadata about the returned file, such as size, name, and file type.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. Indicates that the attachment from this table might not be accessible. Verify that the associated table is included in the **glide.rest.attachment\_csm\_api.allowed\_tables** system property.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

|Name|Description|
|----|-----------|
| |Contents of the attachment.|

### Sample cURL request

```
curl "https://instance.servicenow.com/api/now/v1/attachment_csm/<attachment_sys_id>/file" \
--request GET \
--header "Accept:*/*" \
--user 'username':'password'
```

```
Recipient list Internal users Sheet1
sys_id	email
 Recipient list Internal users.xlsx
```

## CSM Attachment - GET /now/attachment\_csm/\{sys\_id\}

Returns the metadata for the attachment file with the specific attachment sys\_id.

### URL format

Versioned URL: `/api/now/{api_version}/attachment_csm/{sys_id}`

Default URL: `/api/now/v1/attachment_csm/{sys_id}`

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

sys\_id

</td><td>

Sys\_id of the attachment record for which to return metadata. This attachment must belong to one of the tables listed within the **glide.rest.attachment\_csm\_api.allowed\_tables** property in the System Properties \[sys\_properties\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
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
|400|Bad Request. Indicates that the attachment from this table might not be accessible. Verify that the associated table is included in the **glide.rest.attachment\_csm\_api.allowed\_tables** system property.|
|401|Unauthorized. The user credentials are incorrect.|
|404|Not Found. Indicates the specified attachment does not exist, or the current user does not have the rights to access it.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_ezp_y1k_llb"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Metadata of the requested attachment.Data type: Object

```
"result": {
  "average_image_color": "String",
  "compressed": "String", 
  "content_type": "String",
  "created_by_name": "String",
  "download_link": "String",
  "file_name": "String",
  "image_height": "String",
  "image_width": "String",
  "size_bytes": "String",
  "size_compressed": "String",
  "sys_created_by": "String",
  "sys_created_on": "String",
  "sys_id": "String",
  "sys_mod_count": "String",
  "sys_tags": "String",
  "sys_updated_by": "String",
  "sys_updated_on": "String",
  "table_name": "String",
  "table_sys_id": "String",
  "updated_by_name": "String"
}
```

</td></tr><tr><td>

result.average\_image\_color

</td><td>

If the attachment is an image, the sum of all colors.Data type: String

Unit: RGB or number of pixels.

</td></tr><tr><td>

result.compressed

</td><td>

Flag that indicates whether the attachment file has been compressed.Possible values:

-   true: File has been compressed.
-   false: File has not been compressed.

Data type: String

</td></tr><tr><td>

result.content\_type

</td><td>

Content-type of the associated attachment file, such as image or jpeg or application/x-shockwave-flash.Data type: String

</td></tr><tr><td>

result.created\_by\_name

</td><td>

Full name of entity that originally created the attachment file.Data type: String

</td></tr><tr><td>

result.download\_link

</td><td>

Download URL of the attachment on the ServiceNow instance.Data type: String

</td></tr><tr><td>

result.file\_name

</td><td>

File name of the attachment.Data type: String

</td></tr><tr><td>

result.image\_height

</td><td>

If an image file, the height of the image.Data type: String

Unit: Pixels

</td></tr><tr><td>

result.image\_width

</td><td>

If an image file, the width of the image.Data type: String

Unit: Pixels

</td></tr><tr><td>

result.size\_bytes

</td><td>

Size of the attachment.Data type: String

Unit: Bytes

</td></tr><tr><td>

result.size\_compressed

</td><td>

Size of the compressed attachment file. If the file is not compressed, empty.Data type: String

Unit: Bytes

</td></tr><tr><td>

result.sys\_created\_by

</td><td>

Entity that originally created the attachment file.Data type: String

</td></tr><tr><td>

result.sys\_created\_on

</td><td>

Date and time that the attachment file was initially saved to the instance.Data type: String

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the attachment file.Data type: String

</td></tr><tr><td>

result.sys\_mod\_count

</td><td>

Number of times the attachment file has been modified \(uploaded to the instance\).Data type: String

</td></tr><tr><td>

result.sys\_tags

</td><td>

Any system tags associated with the attachment file.Data type: String

</td></tr><tr><td>

result.sys\_updated\_by

</td><td>

Entity that last updated the attachment file.Data type: String

</td></tr><tr><td>

result.sys\_updated\_on

</td><td>

Date and time that the attachment file was last updated.Data type: String

</td></tr><tr><td>

result.table\_name

</td><td>

Name of the table to which the attachment is associated.Data type: String

</td></tr><tr><td>

result.table\_sys\_id

</td><td>

Sys\_id of the table associated with the attachment.Data type: String

</td></tr><tr><td>

result.updated\_by\_name

</td><td>

Full name of entity that last updated the attachment file.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.servicenow.com/api/now/v1/attachment_csm/615ea769c0a80166001cf5f2367302f5" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": {
    "table_sys_id": "5054b6f8c0a800060056addcf551ecf8",
    "size_bytes": "462",
    "download_link": "https://instance.service-now.com/api/now/v1/attachment_csm/615ea769c0a80166001cf5f2367302f5/file",
    "sys_updated_on": "2019-05-21 04:12:21",
    "sys_id": "615ea769c0a80166001cf5f2367302f5",
    "image_height": "",
    "sys_created_on": "2019-05-21 04:12:21",
    "file_name": "blocks.swf",
    "sys_created_by": "glide.maint",
    "compressed": "true",
    "average_image_color": "",
    "sys_updated_by": "glide.maint",
    "sys_tags": "",
    "table_name": "content_block_programmatic",
    "image_width": "",
    "sys_mod_count": "0",
    "content_type": "application/x-shockwave-flash",
    "size_compressed": "485",
    "created_by_name": "John Smith",
    "updated_by_name": "John Smith"
  }
}
```

## CSM Attachment - POST /now/attachment\_csm/file

Uploads a specified binary file as an attachment to a specified record.

The endpoint also returns the metadata for the saved attachment.

### URL format

Versioned URL: `/api/now/{api_version}/attachment_csm/file`

Default URL: `/api/now/v1/attachment_csm/file`

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

encryption\_context

</td><td>

Sys\_id of an encryption context record. Specify this parameter to allow only users with the specified encryption context to access the attachment. For additional information on encryption context records, see [Field Encryption](https://www.servicenow.com/docs/access?context=field-encryption&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).Data type: String

Default: Attached file is not encrypted with any encryption context.

</td></tr><tr><td>

file\_name

</td><td>

Required. Name to give the attachment.**Note:** The file to attach must be specified after the last parameter in the passed-in query parameter list.

Data type: String

</td></tr><tr><td>

table\_name

</td><td>

Required. Name of the table to which you want to attach the file. This table must be listed within the **glide.rest.attachment\_csm\_api.allowed\_tables** system property in the System Properties \[sys\_properties\] table.Data type: String

</td></tr><tr><td>

table\_sys\_id

</td><td>

Required. Sys\_id of the record on the specified table to which you want to attach the file. Data type: String

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;String&gt;

</td><td>

Path to the binary file to attach to the specified record.Data type: String

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

Required. Data format of the file to post. For example, use `image/jpeg` or `image/png` to post JPEG or PNG image files exclusively. To allow all image types, specify `image/*`; to allow any file type, specify `*/*`.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. Indicates that the attachment from this table might not be accessible. Verify that the associated table is included in the **glide.rest.attachment\_csm\_api.allowed\_tables** system property.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. Indicates the record specified by the **table\_name** and **table\_sys\_id** parameters does not exist or is not accessible by the current user.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_kbr_qck_llb"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Metadata of the requested attachment.Data type: Object

```
"result": {
  "average_image_color": "String",
  "compressed": "String", 
  "content_type": "String",
  "created_by_name": "String",
  "download_link": "String",
  "file_name": "String",
  "image_height": "String",
  "image_width": "String",
  "size_bytes": "String",
  "size_compressed": "String",
  "sys_created_by": "String",
  "sys_created_on": "String",
  "sys_id": "String",
  "sys_mod_count": "String",
  "sys_tags": "String",
  "sys_updated_by": "String",
  "sys_updated_on": "String",
  "table_name": "String",
  "table_sys_id": "String",
  "updated_by_name": "String"
}
```

</td></tr><tr><td>

result.average\_image\_color

</td><td>

If the attachment is an image, the sum of all colors.Data type: String

Unit: RGB or number of pixels.

</td></tr><tr><td>

result.compressed

</td><td>

Flag that indicates whether the attachment file has been compressed.Possible values:

-   true: File has been compressed.
-   false: File has not been compressed.

Data type: String

</td></tr><tr><td>

result.content\_type

</td><td>

Content-type of the associated attachment file, such as image or jpeg or application/x-shockwave-flash.Data type: String

</td></tr><tr><td>

result.created\_by\_name

</td><td>

Full name of entity that originally created the attachment file.Data type: String

</td></tr><tr><td>

result.download\_link

</td><td>

Download URL of the attachment on the ServiceNow instance.Data type: String

</td></tr><tr><td>

result.file\_name

</td><td>

File name of the attachment.Data type: String

</td></tr><tr><td>

result.image\_height

</td><td>

If an image file, the height of the image.Data type: String

Unit: Pixels

</td></tr><tr><td>

result.image\_width

</td><td>

If an image file, the width of the image.Data type: String

Unit: Pixels

</td></tr><tr><td>

result.size\_bytes

</td><td>

Size of the attachment.Data type: String

Unit: Bytes

</td></tr><tr><td>

result.size\_compressed

</td><td>

Size of the compressed attachment file. If the file is not compressed, empty.Data type: String

Unit: Bytes

</td></tr><tr><td>

result.sys\_created\_by

</td><td>

Entity that originally created the attachment file.Data type: String

</td></tr><tr><td>

result.sys\_created\_on

</td><td>

Date and time that the attachment file was initially saved to the instance.Data type: String

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the attachment file.Data type: String

</td></tr><tr><td>

result.sys\_mod\_count

</td><td>

Number of times the attachment file has been modified \(uploaded to the instance\).Data type: String

</td></tr><tr><td>

result.sys\_tags

</td><td>

Any system tags associated with the attachment file.Data type: String

</td></tr><tr><td>

result.sys\_updated\_by

</td><td>

Entity that last updated the attachment file.Data type: String

</td></tr><tr><td>

result.sys\_updated\_on

</td><td>

Date and time that the attachment file was last updated.Data type: String

</td></tr><tr><td>

result.table\_name

</td><td>

Name of the table to which the attachment is associated.Data type: String

</td></tr><tr><td>

result.table\_sys\_id

</td><td>

Sys\_id of the table associated with the attachment.Data type: String

</td></tr><tr><td>

result.updated\_by\_name

</td><td>

Full name of entity that last updated the attachment file.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

Shows how to upload the .jpg file `Issue_screenshot.jpg` in the `/images` directory.

```
curl "https://instance.servicenow.com/api/now/v1/attachment_csm/file?table_name=incident&table_sys_id=d71f7935c0a8016700802b64c67c11c6&file_name=Issue_screenshot" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type: image/jpeg" \
--user "username":"password" \
--data-binary "@/images/Issue_screenshot.jpg"
```

```
{
  "result": {
    "table_sys_id": "d71f7935c0a8016700802b64c67c11c6",
    "size_bytes": "36597",
    "download_link": "https://instance.service-now.com/api/now/v1/attachment_csm/6ea10fe64f411200adf9f8e18110c739/file",
    "sys_updated_on": "2019-01-22 15:14:07",
    "sys_id": "6ea10fe64f411200adf9f8e18110c739",
    "image_height": "",
    "sys_created_on": "2019-01-22 15:14:07",
    "file_name": "Issue_screenshot",
    "sys_created_by": "username",
    "compressed": "true",
    "average_image_color": "",
    "sys_updated_by": "username",
    "sys_tags": "",
    "table_name": "incident",
    "image_width": "",
    "sys_mod_count": "0",
    "content_type": "image/jpeg",
    "size_compressed": "25130",
    "created_by_name": "John Smith",
    "updated_by_name": "John Smith"
  }
}
```

## CSM Attachment - POST /now/attachment\_csm/upload

Uploads a multipart file attachment.

The multipart POST method does not accept any parameters. You must specify the table name and record sys\_id values within the form body. See the cURL example below for a sample of a multipart/form-data request.

**Note:** When using multipart POST, ensure the file content is contained in the final part of the message only. Earlier parts should contain only metadata such as table name and record sys\_id.

When sending a multipart/form-data POST request to upload a file attachment, include attachment data in the form body, not in the URL parameters or request body.

<table id="table_p1v_nnj_js"><thead><tr><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Type

</td><td>

Content-Type of the file, included in the message body for multipart uploads.**Note:** You must define the Content-Type within the file portion of the POST message, not within the form data.

 Data type: String

</td></tr><tr><td>

table\_name

</td><td>

Name of the table to which you want to attach the file. This table must be specified in the **glide.rest.attachment\_csm\_api.allowed\_tables** property in the System Properties \[sys\_properties\] table.Data type: String

</td></tr><tr><td>

table\_sys\_id

</td><td>

Sys\_id of the record on the specified table to which you want to attach the file.Data type: String

</td></tr></tbody>
</table>### URL format

Versioned URL: `/api/now/{api_version}/attachment_csm/upload`

Default URL: `/api/now/v1/attachment_csm/upload`

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

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Content-Type|Data format of the request body. Set this value to `multipart/form-data` when using the multipart POST method.|

|Header|Description|
|------|-----------|
|Location|URL of the new attachment in the ServiceNow platform instance.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|201|Successful. Indicates the request completed successfully.|
|400|Bad Request. Indicates that the attachment from this table might not be accessible. Verify that the associated table is included in the **glide.rest.attachment\_csm\_api.allowed\_tables** system property.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item was not found.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table id="table_bbj_pfk_llb"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Metadata of the requested attachment.Data type: Object

```
"result": {
  "average_image_color": "String",
  "compressed": "String", 
  "content_type": "String",
  "created_by_name": "String",
  "download_link": "String",
  "file_name": "String",
  "image_height": "String",
  "image_width": "String",
  "size_bytes": "String",
  "size_compressed": "String",
  "sys_created_by": "String",
  "sys_created_on": "String",
  "sys_id": "String",
  "sys_mod_count": "String",
  "sys_tags": "String",
  "sys_updated_by": "String",
  "sys_updated_on": "String",
  "table_name": "String",
  "table_sys_id": "String",
  "updated_by_name": "String"
}
```

</td></tr><tr><td>

result.average\_image\_color

</td><td>

If the attachment is an image, the sum of all colors.Data type: String

Unit: RGB or number of pixels.

</td></tr><tr><td>

result.compressed

</td><td>

Flag that indicates whether the attachment file has been compressed.Possible values:

-   true: File has been compressed.
-   false: File has not been compressed.

Data type: String

</td></tr><tr><td>

result.content\_type

</td><td>

Content-type of the associated attachment file, such as image or jpeg or application/x-shockwave-flash.Data type: String

</td></tr><tr><td>

result.created\_by\_name

</td><td>

Full name of entity that originally created the attachment file.Data type: String

</td></tr><tr><td>

result.download\_link

</td><td>

Download URL of the attachment on the ServiceNow instance.Data type: String

</td></tr><tr><td>

result.file\_name

</td><td>

File name of the attachment.Data type: String

</td></tr><tr><td>

result.image\_height

</td><td>

If an image file, the height of the image.Data type: String

Unit: Pixels

</td></tr><tr><td>

result.image\_width

</td><td>

If an image file, the width of the image.Data type: String

Unit: Pixels

</td></tr><tr><td>

result.size\_bytes

</td><td>

Size of the attachment.Data type: String

Unit: Bytes

</td></tr><tr><td>

result.size\_compressed

</td><td>

Size of the compressed attachment file. If the file is not compressed, empty.Data type: String

Unit: Bytes

</td></tr><tr><td>

result.sys\_created\_by

</td><td>

Entity that originally created the attachment file.Data type: String

</td></tr><tr><td>

result.sys\_created\_on

</td><td>

Date and time that the attachment file was initially saved to the instance.Data type: String

</td></tr><tr><td>

result.sys\_id

</td><td>

Sys\_id of the attachment file.Data type: String

</td></tr><tr><td>

result.sys\_mod\_count

</td><td>

Number of times the attachment file has been modified \(uploaded to the instance\).Data type: String

</td></tr><tr><td>

result.sys\_tags

</td><td>

Any system tags associated with the attachment file.Data type: String

</td></tr><tr><td>

result.sys\_updated\_by

</td><td>

Entity that last updated the attachment file.Data type: String

</td></tr><tr><td>

result.sys\_updated\_on

</td><td>

Date and time that the attachment file was last updated.Data type: String

</td></tr><tr><td>

result.table\_name

</td><td>

Name of the table to which the attachment is associated.Data type: String

</td></tr><tr><td>

result.table\_sys\_id

</td><td>

Sys\_id of the table associated with the attachment.Data type: String

</td></tr><tr><td>

result.updated\_by\_name

</td><td>

Full name of entity that last updated the attachment file.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.service-now.com/api/now/v1/attachment_csm/upload" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:multipart/form-data" \
--user "username":"password" \
 -F "table_name=incident" \
 -F "table_sys_id=d71f7935c0a8016700802b64c67c11c6" \
 -F "uploadFile=@/image/banner-CS0001345_v1_1.jpeg"

```

```
{
  "result": {
    "table_sys_id": "d71f7935c0a8016700802b64c67c11c6",
    "size_bytes": "36597",
    "download_link": "https://instance.service-now.com/api/now/v1/attachment_csm/994adbc64f511200adf9f8e18110c796/file",
    "sys_updated_on": "2019-02-02 14:00:21",
    "sys_id": "994adbc64f511200adf9f8e18110c796",
    "image_height": "",
    "sys_created_on": "2019-02-02 14:00:21",
    "file_name": "banner-CS0001345_v1_1.jpeg",
    "sys_created_by": "username",
    "compressed": "true",
    "average_image_color": "",
    "sys_updated_by": "username",
    "sys_tags": "",
    "table_name": "incident",
    "image_width": "",
    "sys_mod_count": "0",
    "content_type": "image/jpeg",
    "size_compressed": "25130",
    "created_by_name": "John Smith",
    "updated_by_name": "John Smith"
  }
}
```

