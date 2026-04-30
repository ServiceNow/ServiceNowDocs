---
title: AWA Inbox Actions API
description: The AWA Inbox Actions API provides endpoints to accept or reject a work item on behalf of an agent. This API also retrieves reject reasons for rejected work items.Gets the work item reject reasons for a specified service channel.Accepts a work item in Pending Accept state on behalf of an agent.Rejects a work item in Pending Accept state on behalf of an agent. On success, Assigned to field is empty and the value of the Rejected field is true for the specified work item.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# AWA Inbox Actions API

The AWA Inbox Actions API provides endpoints to accept or reject a work item on behalf of an agent. This API also retrieves reject reasons for rejected work items.

This API requires the Advanced Work Assignment \(com.glide.awa\) plugin and awa\_integration\_user role. For more information, refer to [Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-overview&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## AWA Inbox Actions – GET /awa/inbox/actions/reject\_reasons/\{channel\_id\}

Gets the work item reject reasons for a specified service channel.

### URL format

Versioned URL: `/api/now/awa/inbox/actions/reject_reasons/{channel_id}`

Default URL: `/api/now/{api_version}/awa/inbox/actions/reject_reasons/{channel_id}`

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

channel\_id

</td><td>

Sys\_id of a service channel.Data type: String

Table: Service Channels \[awa\_service\_channel\]

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
-   The value of the glide.awa.enabled property isn't `true`. This property is listed in the System Property \[sys\_property\] table if the Advanced Work Assignment \(com.glide.awa\) plugin is installed. For more information, see [Components installed with Advanced Work Assignment](https://www.servicenow.com/docs/access?context=installed-with-awa&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

</td></tr><tr><td>

404

</td><td>

Record not found. The channel ID provided is not valid.

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

display\_value

</td><td>

Display value of the Reason field in the Reject Reasons \[awa\_reject\_reason\] table.Data type: String

</td></tr><tr><td>

order

</td><td>

Order in which the reject reasons are listed in the agent inbox.Data type: Number

</td></tr><tr><td>

value

</td><td>

Value of the reject reason field stored in the database.Data type: String

</td></tr><tr><td>

Sys\_id

</td><td>

Sys\_id of a rejection reason for this service channel.Data type: String

Table: Reject Reasons \[awa\_reject\_reason\]

</td></tr></tbody>
</table>The following example shows how to retrieve reject reasons for the Chat service channel.

```
curl "https://instance.service-now.com/api/now/awa/inbox/actions/reject_reasons/27f675e3739713004a905ee515f6a7c3" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body displaying rejected tasks with reasons for rejection.

```
{
  "result": [
    {
      "order": 2,
      "value": "Not my expertise",
      "display_value": "Not my expertise",
      "sys_id": "31e3fa29b38023002e7b6e5f26a8dc17"
    },
    {
      "order": 1,
      "value": "Busy",
      "display_value": "Busy",
      "sys_id": "4e93fa29b38023002e7b6e5f26a8dc20"
    }
  ]
}
```

## AWA Inbox Actions – POST /awa/inbox/actions/accept

Accepts a work item in **Pending Accept** state on behalf of an agent.

### URL format

Versioned URL: `/api/now/{api_version}/awa/inbox/actions/accept`

Default URL: `/api/now/awa/inbox/actions/accept`

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

agent\_id

</td><td>

Sys\_id of the agent listed.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

work\_item\_id

</td><td>

Sys\_id of the work item. The work item must meet the following criteria:

-   Work item must be assigned to the specified agent.
-   Work item must be in **Pending Accept** state.

Data type: String

Table: AWA Work Item \[awa\_work\_item\]

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

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_qsk_1hj_mtb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Invalid request. Possible reasons:

-   Missing agent ID.
-   Missing work item ID.
-   Work item is assigned to a different agent.
-   Work item isn't in pending accept state.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

403

</td><td id="entry-403-status-code-awa">

Forbidden.Possible reasons:

-   The user doesn't have the awa\_integration\_user role.
-   The value of the glide.awa.enabled property isn't `true`. This property is listed in the System Property \[sys\_property\] table if the Advanced Work Assignment \(com.glide.awa\) plugin is installed. For more information, see [Components installed with Advanced Work Assignment](https://www.servicenow.com/docs/access?context=installed-with-awa&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

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

documentTable

</td><td>

Name of the table listing the document assigned to this work item.Data type: String

</td></tr><tr><td>

documentSysId

</td><td>

Sys\_id of the document record assigned to the task.Data type: String

Table: In the table identified in the **documentTable** field.

</td></tr><tr id="ordr-row-error"><td>

error

</td><td>

Details describing an error encountered during the request process.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Details of the error encountered during the request process. Possible values:

-   `Missing agent ID`: The **agent\_id** wasn't provided in the request body.
-   `Missing work item ID`: The **work\_item\_id** wasn't provided in the request body.
-   `Work item is assigned to a different agent`: The specified work item is not assigned to the specified agent.
-   `Wrong work item ID`: The work item provided in the request body is inaccurate or doesn't exist.
-   `Work item is not in pending accept state`: The work item provided in the request body is in a state other than **Pending Accept**.

Data type: String

</td></tr><tr><td>

error.message

</td><td>

Message for the error encountered during the request process. The description is provided in the **error.detail** property.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of an unsuccessful request. This property is only included in the response if there is an error.Valid value: `failure`

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to change the state of a selected agent's work item from **Pending Accept** to **Accepted**.

```
curl "https://instance.service-now.com/api/now/awa/inbox/actions/accept" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
 \"agent_id\":\"46c9e158a9fe198101d44d0d22cb640d\",
 \"work_item_id\":\"fd69abfc878b01101ae365b83cbb35fe\"
}" \
--user 'username':'password'
```

The response body lists the sys\_id and table of the document related to the work item.

```
{
  "result": {
    "documentSysId": "57af7aec73d423002728660c4cf6a71c",
    "documentTable": "incident"
  }
}
```

## AWA Inbox Actions – POST /awa/inbox/actions/reject

Rejects a work item in **Pending Accept** state on behalf of an agent. On success, **Assigned to** field is empty and the value of the **Rejected** field is true for the specified work item.

### URL format

Versioned URL: `/api/now/{api_version}/awa/inbox/actions/reject`

Default URL: `/api/now/awa/inbox/actions/reject`

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

agent\_id

</td><td>

Sys\_id of the agent listed.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

reject\_reason\_id

</td><td>

Sys\_id of a rejection reason for this service channel.Data type: String

Table: Reject Reasons \[awa\_reject\_reason\]

</td></tr><tr><td>

work\_item\_id

</td><td>

Sys\_id of the work item. The work item must meet the following criteria:

-   Work item must be assigned to the specified agent.
-   Work item must be in **Pending Accept** state.

Data type: String

Table: AWA Work Item \[awa\_work\_item\]

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

</td><td>

Invalid request. Possible reasons:

-   Missing agent ID.
-   Missing work item ID.
-   Missing reject reason ID.
-   Work item is assigned to a different agent.
-   Work item isn't in pending accept state.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

403

</td><td id="entry-403-status-code-awa">

Forbidden.Possible reasons:

-   The user doesn't have the awa\_integration\_user role.
-   The value of the glide.awa.enabled property isn't `true`. This property is listed in the System Property \[sys\_property\] table if the Advanced Work Assignment \(com.glide.awa\) plugin is installed. For more information, see [Components installed with Advanced Work Assignment](https://www.servicenow.com/docs/access?context=installed-with-awa&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

</td></tr><tr><td>

404

</td><td>

Not found. The requested item wasn't found.Possible reasons:

-   Wrong agent ID – There is no record for the specified user.
-   Wrong reject reason ID – There is no record for the specified reject reason.
-   Wrong work item ID – There is no record for the specified work item.

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

agent\_id

</td><td>

Sys\_id of the agent listed.Data type: String

Table: User \[sys\_user\]

</td></tr><tr id="ordr-row-error"><td>

error

</td><td>

Details describing an error encountered during the request process.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Details of the error encountered during the request process. Possible values:

-   `Missing agent ID` – The **agent\_id** wasn't provided in the request body.
-   `Missing reject reason item ID` – The **reject\_reason\_id** wasn't provided in the request body.
-   `Missing work item ID`: The **work\_item\_id** wasn't provided in the request body.
-   `There is no record for awa_reject_reason : <reason_sys_id>` – The **reject\_reason\_id** provided in the request body doesn't have a matching record in the Reject Reasons \[awa\_reject\_reason\] table.
-   `There is no record for awa_work_item : <work_item_sys_id>` – The **work\_item\_id** provided in the request body doesn't have a matching record in the AWA Work Item \[awa\_work\_item\] table.
-   `There is no record for sys_user : <agent_sys_id>` – The **agent\_id** provided in the request body doesn't have a matching record in the User \[sys\_user\] table.
-   `Work item is not in pending accept state`: The work item provided in the request body is in a state other than **Pending Accept**.

Data type: String

</td></tr><tr><td>

error.message

</td><td>

Message for the error encountered during the request process. The description is provided in the **error.detail** property.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of an unsuccessful request. This property is only included in the response if there is an error.Valid value: `failure`

Data type: String

</td></tr><tr><td>

reject\_reason\_id

</td><td>

Sys\_id of a rejection reason for this service channel.Data type: String

Table: Reject Reasons \[awa\_reject\_reason\]

</td></tr><tr><td>

work\_item\_id

</td><td>

Sys\_id of the work item. Data type: String

</td></tr></tbody>
</table>The following example shows how to reject an assigned work item with the "not my expertise" reason.

```
curl "https://instance.service-now.com/api/now/awa/inbox/actions/reject" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    \"agent_id\":\"46c9e158a9fe198101d44d0d22cb640d\",
    \"work_item_id\":\"3ed5df4d87cf01101ae365b83cbb35af\",
    \"reject_reason_id\":\"31e3fa29b38023002e7b6e5f26a8dc17\"
}" \
--user 'username':'password'
```

Successful output displays the same work item, reject reason, and user ID provided in the request body. The specified work item in the AWA Work Item \[awa\_work\_item\] table has an empty **Assigned to** field and the value of the **Rejected** field is true.

```
{
  "result": {
    "work_item_id": "3ed5df4d87cf01101ae365b83cbb35af",
    "reject_reason_id": "31e3fa29b38023002e7b6e5f26a8dc17",
    "agent_id": "46c9e158a9fe198101d44d0d22cb640d"
  }
}
```

