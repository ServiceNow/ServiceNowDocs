---
title: CCCIF Media Resource API
description: The Custom Chat Chatbot Interoperability Framework \(CCCIF\) Media Resource API provides endpoints that enable a primary bot to upload attachments to the associated ServiceNow instance.Uploads a private attachment to the called ServiceNow instance which stores the attachment in the Attachments \[sys\_attachment\] table.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# CCCIF Media Resource API

The Custom Chat Chatbot Interoperability Framework \(CCCIF\) Media Resource API provides endpoints that enable a primary bot to upload attachments to the associated ServiceNow instance.

Call this API in your primary bot to upload private attachments from a user that is having a conversation through Virtual Agent \(VA\). You must then send the mediaUrl parameter that is returned by this API to the VA API.

If the attachment is public, you can just send the attachment URL in the request body of your [Virtual Agent Bot Integration](bot-api.md#) call.

To access this API, the Conversational Custom Chat Integration \(com.glide.cs.custom.adapter\) plugin must be activated. In addition, the attachment system properties must be configured.

For additional information on the capabilities of the Virtual Agent API, see [Virtual Agent API](https://www.servicenow.com/docs/access?context=virtual-agent-api-landing-page&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## CCCIF - POST /cccif/media/upload

Uploads a private attachment to the called ServiceNow instance which stores the attachment in the Attachments \[sys\_attachment\] table.

Call this method in your primary bot to upload private attachments from a user that is having a conversation through Virtual Agent \(VA\). You must then send the mediaUrl parameter that is returned by this method to the VA API using the [Virtual Agent Bot Integration API](bot-api.md#).

### URL format

Versioned URL: `/api/now/{api_version}/cccif/media/upload`

Default URL: `/api/now/cccif/media/upload`

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

file

</td><td>

Required. Path of the file to upload.Data type: String, such as @File path &lt;file\_path&gt;

</td></tr><tr><td>

provider\_application\_id

</td><td>

Sys\_id of the sys\_cs\_provider\_application interacting with the VA bot.Default: Sys\_id of the VA Bot to Bot Provider Application

</td></tr><tr><td>

user\_id

</td><td>

Required. Unique user identifier of the user interacting with the VA bot. This can be any string that is unique for each user.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Supported types: **multipart/form-data**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|201|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attachmentId

</td><td>

Sys\_id of the attachment that was stored.Data type: String

</td></tr><tr><td>

error

</td><td>

Description of any error detected while processing the request.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Details about the error that was encountered.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Message describing the error that was thrown.Data type: String

</td></tr><tr><td>

mediaUrl

</td><td>

Attachment URL to send to the primary bot to access the attachment. The primary bot must send this URL in the **message.attachment.url** parameter of the request body of the POST /sn\_va\_as\_service/bot/integration endpoint.Data type: String

</td></tr><tr><td>

name

</td><td>

File name of the attachment.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the attachment in the Attachment table.Possible values:

-   available
-   conditionally available
-   not available
-   pending

Data type: String

</td></tr></tbody>
</table>### cURL request

This example shows how to upload a .png file attachment.

```
curl --location --request POST 'https://instance.servicenow.com/api/now/v1/cccif/media/upload' \
--header 'Authorization: Basic xxxxxxxxxxxxx' \
--header 'Content-Type:multipart/form-data' \
--form 'user_id="lincoln"' \
--form 'file=@"/Users/Desktop/Screenshot 2021-10-25 at 5.08.14 PM.png"'

```

Response:

```
Response :{
  "result": {
    "mediaUrl": "https://instance.servicenow.com/api/now/v1/cs/media/vGfewkfAv0VBo2RxmlTM448L789Pp6rqLFLUNYQxZsUUFrsgMA8aW9W0zWx1a5fG",
    "name": "Screenshot 2021-10-25 at 5.08.14 PM.png",
    "state": "pending",
    "attachmentId": "299c648887b73c1022b6a6cd0ebb3534"
  }
```

