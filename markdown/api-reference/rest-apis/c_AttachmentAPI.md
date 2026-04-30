---
title: Attachment API
description: The Attachment API provides endpoints that allow you to upload and query file attachments.This method deletes the attachment with a specific sys\_id value.Returns the metadata for multiple attachments.Returns the binary file attachment with a specific sys\_id value.Returns the metadata for the attachment file with a specific sys\_id value.Uploads a specified binary file as an attachment to a specified record.Uploads a multipart file attachment.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 18
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Attachment API

The Attachment API provides endpoints that allow you to upload and query file attachments.

You can upload or retrieve a single file with each request.

The Attachment API respects any system limitations on uploaded files, such as maximum file size and allowed attachment types. You can control these settings using the properties **com.glide.attachment.max\_size**, 1024MB by default, and **glide.attachment.extensions**.

**Note:** The Attachment API accepts all Content-Type values \(\*/\*\). Specify the file content type when uploading an attachment. The content type is stored with file metadata allowing other tools to correctly identify and parse the file.

The following video provides more information on the Attachment API:

Web Services Part 5 \| How to Make REST Attachment API Requests

## Attachment API role requirements

To create attachments, the user record used to authenticate the HTTP request with ServiceNow must have any roles required to create Attachment \[sys\_attachment\] records. It must also have any roles required to read and write records on the target table, such as the itil role to add attachments to incident records.

By default there is no single role allowing a user to add attachments. You can create a role to explicitly allow adding attachments, then assign this role to the user account being used to make the request.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Attachment - DELETE /now/attachment/\{sys\_id\}

This method deletes the attachment with a specific sys\_id value.

### URL format

Versioned URL: `/api/now/v1/attachment/{sys_id}`

Default URL: `/api/now/attachment/{sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_id

</td><td>

Sys\_id value of the attachment to delete.Data type: String

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
|204|Indicates the request ran successfully.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|None||

### cURL request

```
curl "https://instance.servicenow.com/api/now/attachment/615ea769c0a80166001cf5f2367302f5" \
--request DELETE \
--user 'username':'password'

```

```
""
```

## Attachment - GET /now/attachment

Returns the metadata for multiple attachments.

### URL format

Versioned URL: `api/now/v1/attachment`

Default URL: `api/now/attachment`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_limit

</td><td>

Limit to be applied on pagination. **Note:** Unusually large `sysparm_limit` values can impact system performance.

Data type: String

Default: 1000

</td></tr><tr id="row_sysparm_offset"><td>

sysparm\_offset

</td><td>

Number of records to exclude from the query. Use this parameter to get more records than specified in **sysparm\_limit** parameter. For example, if **sysparm\_limit** is set to 500, but there are additional records you want to query, you can specify a **sysparm\_offset** parameter value of 500 to get the second set of records.Data type: String

Default: 0

</td></tr><tr><td>

sysparm\_query

</td><td>

Encoded query. Queries for the Attachment API are relative to the Attachments \[sys\_attachment\] table.For example: **\(sysparm\_query=file\_name=attachment.doc\)**

The encoded query provides support for order by. To sort responses based on certain fields, use the ORDERBY and ORDERBYDESC clauses in sysparm\_query. For example, `sysparm_query=ORDERBYfile_name^ORDERBYDESCtable_Name` orders the results in ascending order by name first, then in descending order by table name.

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
|Content-Type|Content type of the response. For metadata requests, this is the content type of the metadata, not the content type of the attachment files.|
|Link|Links to download the attachments.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|Returned information depends on the selected attachments.||

### cURL request

```
curl "https://instance.servicenow.com/api/now/attachment?sysparm_limit=1" \
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
      "download_link": "https://instance.service-now.com/api/now/attachment/615ea769c0a80166001cf5f2367302f5/file",
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
      "size_compressed": "485"
    }
  ]
}
```

## Attachment - GET /now/attachment/\{sys\_id\}/file

Returns the binary file attachment with a specific sys\_id value.

### URL format

Versioned URL: `/api/now/v1/attachment/{sys_id}/file`

Default URL: `/api/now/attachment/{sys_id}/file`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

|Name|Description|
|----|-----------|
|sys\_id|Sys\_id of the attachment record from which to return binary data.|

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
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|Binary file attachment||

### cURL request

```
curl "https://instance.servicenow.com/api/now/attachment/615ea769c0a80166001cf5f2367302f5/file" \
--request GET \
--header "Accept:*/*" \
--user "username":"password"
```

```
Binary response not shown.
```

## Attachment - GET /now/attachment/\{sys\_id\}

Returns the metadata for the attachment file with a specific sys\_id value.

### URL format

Versioned URL: `/api/now/v1/attachment/{sys_id}`

Default URL: `/api/now/attachment/{sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

|Name|Description|
|----|-----------|
|sys\_id|Sys\_id of the attachment record for which to retrieve the metadata.|

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
|Content-Type|The content type of the response. For metadata requests, this is the content type of the metadata, not the content type of the attachment files.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Indicates the specified attachment does not exist, or the current user cannot access it.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|Metadata specific to the specified attachment.||

### cURL request

```
curl "https://instance.servicenow.com/api/now/attachment/615ea769c0a80166001cf5f2367302f5" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": {
    "table_sys_id": "5054b6f8c0a800060056addcf551ecf8",
    "size_bytes": "462",
    "download_link": "https://instance.service-now.com/api/now/attachment/615ea769c0a80166001cf5f2367302f5/file",
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
    "size_compressed": "485"
  }
}
```

## Attachment - POST /now/attachment/file

Uploads a specified binary file as an attachment to a specified record.

**Note:** The file to attach must be specified after the last parameter in the passed-in request parameter list.

### URL format

Versioned URL: `/api/now/v1/attachment/file`

Default URL: `/api/now/attachment/file`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

creation\_time

</td><td>

Creation date and time of the attachment. Use this parameter to capture attachment creation times when the Now Mobile app is offline and the attachment is uploaded to a record at a later time.

Data type: String

Default: The current date and time.

</td></tr><tr><td>

encryption\_context

</td><td>

Sys\_id of an encryption context record. Specify this parameter to allow only users with the specified encryption context to access the attachment. For additional information on encryption context records, see [Field Encryption](https://www.servicenow.com/docs/access?context=field-encryption&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).Data type: String

 Default: File is encrypted using encryption context accessible to the user, otherwise the attached file is not encrypted with any encryption context.

</td></tr><tr><td>

file\_name

</td><td>

Required. Name to give the attachment. Data type: String

</td></tr><tr><td>

table\_name

</td><td>

Required. Name of the table to attach the file to.Data type: String

</td></tr><tr><td>

table\_sys\_id

</td><td>

Required. Sys\_id of the record in the table specified in **table\_name** that you want to attach the file to. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|&lt;String&gt;|Path to the binary file to attach to the specified record.|

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

</td><td>

Content type of the file to attach, such as image/jpeg or \*/\*. This header is mandatory to post file attachments.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|Location|URL of the new attachment.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|201|Indicates the query ran successfully.|
|400|Indicates that one or more mandatory parameters were missing from the request.|
|404|Indicates the record specified by the **table\_name** and **table\_sys\_id** parameters does not exist or is not accessible to the current user.|
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
</table>### cURL request

```
curl "https://instance.servicenow.com/api/now/attachment/file?table_name=incident&table_sys_id=d71f7935c0a8016700802b64c67c11c6&file_name=Issue_screenshot" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type: image/jpeg" \
--user "username":"password" \
--data-binary "@ location of the file on file system"
```

```
{
  "result": {
    "table_sys_id": "d71f7935c0a8016700802b64c67c11c6",
    "size_bytes": "36597",
    "download_link": "https://instance.servicenow.com/api/now/attachment/6ea10fe64f411200adf9f8e18110c739/file",
    "sys_updated_on": "2016-01-22 15:14:07",
    "sys_id": "6ea10fe64f411200adf9f8e18110c739",
    "image_height": "",
    "sys_created_on": "2016-01-22 15:14:07",
    "file_name": "Issue_screenshot",
    "sys_created_by": "admin",
    "compressed": "true",
    "average_image_color": "",
    "sys_updated_by": "admin",
    "sys_tags": "",
    "table_name": "incident",
    "image_width": "",
    "sys_mod_count": "0",
    "content_type": "image/jpeg",
    "size_compressed": "25130"
  }
}
```

## Attachment - POST /now/attachment/upload

Uploads a multipart file attachment.

The multipart POST method does not accept any parameters. You must specify the table name and record sys\_id values within the form body. See the cURL example for a sample of a multipart/form-data request.

**Important:** When using multipart POST, ensure that the file content is contained in the final part of the message only. Earlier parts should contain only metadata such as table name and record sys\_id.

### URL format

Versioned URL: `/api/now/v1/attachment/upload`

Default URL: `/api/now/attachment/upload`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

</td></tr><tr><td>

Content-Type

</td><td>

Content type of the request. Set this value to multipart/form-data when using the multipart POST method.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|Location|URL of the new attachment.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|201|Indicates the query ran successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

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
</table>### POST multipart mandatory values

When sending a multipart POST request to upload a file attachment, include attachment data in the message body, not in the URL parameters. You must specify these values in the message body:

<table id="table_p1v_nnj_js"><thead><tr><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Type

</td><td>

Content-Type of the file, included in the message body for multipart uploads.**Note:** The Content-Type must be defined within the file portion of the POST message, not within the form data. See the sample POST multipart message for an example of a multipart message.

 Data type: String

</td></tr><tr><td>

table\_name

</td><td>

Name of the table to which you want to attach the file.Data type: String

</td></tr><tr><td>

table\_sys\_id

</td><td>

Sys\_id of the record on the specified table to which you want to attach the file.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/now/attachment/upload" \
--request POST \
--header "Accept:application/json"\
--user "username":"password"\
--header "Content-Type:multipart/form-data"\
 -F 'table_name=incident' \
 -F 'table_sys_id=d71f7935c0a8016700802b64c67c11c6'\
 -F 'uploadFile=@ location of the file on file system'
\
```

```
{
  "result": {
    "table_sys_id": "d71f7935c0a8016700802b64c67c11c6",
    "size_bytes": "36597",
    "download_link": "https://instance.service-now.com/api/now/attachment/994adbc64f511200adf9f8e18110c796/file",
    "sys_updated_on": "2016-02-02 14:00:21",
    "sys_id": "994adbc64f511200adf9f8e18110c796",
    "image_height": "",
    "sys_created_on": "2016-02-02 14:00:21",
    "file_name": "banner-CS0001345_v1_1.jpeg",
    "sys_created_by": "admin",
    "compressed": "true",
    "average_image_color": "",
    "sys_updated_by": "admin",
    "sys_tags": "",
    "table_name": "incident",
    "image_width": "",
    "sys_mod_count": "0",
    "content_type": "image/jpeg",
    "size_compressed": "25130"
  }
}
```

