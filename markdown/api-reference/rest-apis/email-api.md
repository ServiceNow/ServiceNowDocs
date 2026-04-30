---
title: Email API
description: The Email API provides endpoints that enable you to receive and send email messages using REST.Returns the email details for the specified email record.Creates an email record using the passed information.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 7
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Email API

The Email API provides endpoints that enable you to receive and send email messages using REST.

Users must have the email\_api\_send role to send email.

**Note:** You might get errors if you do not have read/write access to the Email \[sys\_email\] table.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Email - GET /now/email/\{id\}

Returns the email details for the specified email record.

### URL format

Versioned URL: `/api/now/{api_version}/email/{id}`

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

id

</td><td>

Sys\_id of the email for which to return details.Data type: String

Table: Email \[sys\_email\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_fields

</td><td>

Comma-separated list of fields to return in the response.Data type: String

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
|403|Indicates the record is not found or the requesting user does not have access to the record. Verify the user has the proper role and access permissions.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

bcc

</td><td>

List of the email addresses of the blind copied recipients of the email message. Maps to the blind\_copied field.Data type: Array

</td></tr><tr><td>

cc

</td><td>

List of the email addresses of the copied recipients for the email message. Maps to the copied field.Data type: Array

</td></tr><tr><td>

headers

</td><td>

Name-value pairs of the headers associated with the message and their values.Data type: Object

</td></tr><tr><td>

html

</td><td>

HTML-enabled body of the email message. Maps to the body field.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the email record.Data type: String

</td></tr><tr><td>

importance

</td><td>

Importance of the email message. Maps to the importance field.Data type: String

</td></tr><tr><td>

state

</td><td>

Processing state of the email message. Indicates whether the system scheduled jobs have processed the email message. Possible include:

-   error
-   ignored
-   processed
-   ready

Data type: String

</td></tr><tr><td>

subject

</td><td>

Subject of the email message. Maps to the subject field.Data type: String

</td></tr><tr><td>

text

</td><td>

Text-only body of the email message. Maps to the body\_text field.Data type: String

</td></tr><tr><td>

to

</td><td>

List of the email addresses of the direct recipients of the email message. Maps to the recipients field.Data type: Array

</td></tr><tr><td>

type

</td><td>

Current state of the email message as incoming or outgoing mail. Possible values:

-   received
-   received-ignored
-   send-failed
-   send-ignored
-   send-ready
-   sent

Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "http://instance.servicenow.com/api/now/email/06e095427f0022007f005212bdfa91b3" \
--request GET \
--header "Accept:application/json" \
--user "user-name":"password"

```

```
{
  "result" : {
    "headers" : {
      "X-ServiceNow-SysEmail-Version" : "2",
      "X-ServiceNow-Source" : "Notification-24e34b54c61122aa0108c1b7a33697cf"
    },
    "cc" : [
      ""
    ],
    "type" : "send-ready",
    "html" : "<html><head></head><body><div><p><font size=\"5\" color=\"#808080\" face=\"helvetica\"><strong>Incident has been closed.</strong></font></p></div>\n\t\t<div><p><font size=\"4\" color=\"#808080\" face=\"helvetica\"><strong>Summary details</strong></font></p><p><font size=\"3\" color=\"#808080\" face=\"helvetica\">Closed by: System Administrator</font></p><p><font size=\"3\" color=\"#808080\" face=\"helvetica\">Closed notes: Fixed</font></p></div>\n\t\t<div><p><font size=\"3\" color=\"#808080\" face=\"helvetica\">You can view all the details of the incident by following the link below:</font></p><font face=\"helvetica\"><a href=\"incident.do?sys_id=e8e875b0c0a80164009dc852b4d677d5&amp;sysparm_stack=incident_list.do?sysparm_query=active=true\" style=\"background-color: #278efc;border: 1px solid #0368d4;color: #ffffff;font-size: 16px;font-family: Helvetica, Arial, sans-serif;text-decoration: none; border-radius: 3px;-webkit-border-radius: 3px;-moz-border-radius: 3px;display: inline-block;padding: 5px;\">Take me to the Incident</a></font><br /><br /><p><font size=\"3\" color=\"#808080\" face=\"helvetica\">Thank you.</font></p></div><div>&nbsp;</div><div style=\"display:inline\">Ref:MSG0000006</div></body></html>",
    "bcc" : [
      ""
    ],
    "subject" : "Your incident INC0000005 has been closed",
    "to" : [
      "alejandro.mascall@example.com"
    ],
    "state" : "ready",
    "id" : "06e095427f0022007f005212bdfa91b3",
    "importance" : "",
    "text" : ""
  }
}
```

## Email - POST /now/email

Creates an email record using the passed information.

### URL format

Versioned URL: `/api/now/{api_version}/email`

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

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

bcc

</td><td>

List of the email addresses of the blind copied recipients of the email message. Maps to the blind\_copied field.**Note:** You can only specify up to 100 addresses in this field.

 Data type: Array

</td></tr><tr><td>

cc

</td><td>

List of the email addresses of the copied recipients for the email message. Maps to the copied field.**Note:** You can only specify up to 100 addresses in this field.

 Data type: Array

</td></tr><tr><td>

headers

</td><td>

Name-value pairs of the headers associated with the message and their values.Data type: Object

</td></tr><tr><td>

html

</td><td>

HTML-enabled body of the email message. Maps to the body field.Data type: String

</td></tr><tr><td>

importance

</td><td>

Importance of the email message. Maps to the importance field.Data type: String

</td></tr><tr><td>

subject

</td><td>

Subject of the email message. Maps to the subject field.Data type: String

</td></tr><tr><td>

table\_name

</td><td>

Name of the table to save the email. Use this parameter to associate an email message to a particular related record elsewhere in the system.**Note:** This parameter also requires specifying the **table\_record\_id** parameter.

 Data type: String

</td></tr><tr><td>

table\_record\_id

</td><td>

Target-related record to which the email applies. Use this parameter to associate an email message to a particular related record elsewhere in the system.**Note:** This parameter also requires specifying the **table\_name** parameter.

 Data type: String

</td></tr><tr><td>

text

</td><td>

Text-only body of the email message. Maps to the body\_text field.Data type: String

</td></tr><tr><td>

to

</td><td>

Required. List of the email addresses of the direct recipients for the email message. Maps to the recipients field.**Note:** You can only specify up to 100 addresses in this field.

 Data type: Array

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
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|403|Requesting user does not have access to the record. Verify that the user has the proper role and access permissions.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

href

</td><td>

Link to the email record as an Email API GET request.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the Email record.Data type: String

</td></tr><tr><td>

links

</td><td>

List of links to the Email record.Data type: Array

</td></tr><tr><td>

rel

</td><td>

Type of link listed in the **href** parameter.Possible values:

-   self: The Email API GET request for the Email record.
-   status: The Email API GET request for the Email record showing only the id, type, state, and error fields.

 Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "http://instance.servicenow.com/api/now/email" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--user 'username':'password'\
--data "{
  \"to\": [
    \"User1 <user1@example.com>\",
    \"User2 <user2@example.com>\"
  ],
  \"cc\": [
    \"User3 <user3@example.com>\",
    \"User4 <user4@example.com>\"
  ],
  \"bcc\": [
    \"User5 <user5@example.com>\",
    \"User6 <user6@example.com>\"
  ],
  \"subject\": \"Hello There\",
  \"text\": \"Test Message\",
  \"html\": \"<b>Test Message</b>\",
  \"table_name\": \"incident\",
  \"table_record_id\": \"136b2140bd0312004d7d1371f1abbdb6\",
  \"headers\": {
    \"X-Custom\": \"header\"
  }
}"
```

```
{
 "result": {
   "id": "b963219a44b02200964f63773cd6adfc",
   "links": [
     {
       "rel": "self",
       "href": "/now/v1/email/b963219a44b02200964f63773cd6adfc"
     },
     {
       "rel": "status",
       "href": "/now/v1/email/b963219a44b02200964f63773cd6adfc?sysparm_fields=id,type,state,error"
     }
   ]
 }
}
```

