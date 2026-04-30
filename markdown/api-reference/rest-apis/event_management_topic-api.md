---
title: Event Management Topic Open API
description: The Event Management Topic Open API provides an endpoint that enables you to send a topic through your message broker and store it on a ServiceNow instance.Creates a new record in the Topic \[sn\_api\_notif\_mgmt\_topic\] table and saves the passed topic information to that record.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Event Management Topic Open API

The Event Management Topic Open API provides an endpoint that enables you to send a topic through your message broker and store it on a ServiceNow instance.

Using this API you can store topics created through your message broker in the ServiceNow Topic \[topic\] table.

This API runs in the `sn-api-notif-mgmt` namespace and requires the sn\_api\_notif\_mgmt.event\_mgmt\_integration role.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Event Management Topic Open - POST /sn\_api\_notif\_mgmt/topic

Creates a new record in the Topic \[sn\_api\_notif\_mgmt\_topic\] table and saves the passed topic information to that record.

Use this endpoint to synchronize topics created in your message-bus middleware with those in your ServiceNow instance.

When topics are created using this endpoint, the user\_created field in the associated topic record is set to `false` and the type field is set to `egress`.

### URL format

Versioned URL: `/api/sn_api_notif_mgmt/{api_version}/topic`

Default URL: `/api/sn_api_notif_mgmt/topic`

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

contentQuery

</td><td>

Filter to apply to the payload of the event. This query is a deeper event filter that is used to find information such as event severity or ticket type. You can pass this parameter as a nested query.For example, for the following trouble ticket event payload, this query applies to the attributes that are in the *"event"* object of the payload:

```
{
  "eventId":"dc2003c2c3bb3550054e20bdc0013136",
  "@type":"Troubleticket",
  "eventType":"TroubleTicketCreateEvent",
  "event":{
    "troubleTicket":{
      "short_description":"Test payload",
      "severity":3,
      "ticketType":"incident"
    }
  }
}
```

This parameter supports the following conditions:

-   AND: such as`variable1=value1&variable2=value2&variable3=value3`
-   OR: such as `variable1=value1,value2,value3`
-   Hierarchical variables: such as `variable1.variable2.variable3=value1`

For example: `"contentQuery": "troubleTicket.ticketType=incident&troubleTicket.severity=1",`

This field is mapped to the content\_query field in the associated topic record.

For additional information, refer to the [TMF688 Event Management API User Guide](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/).

Data type: String

</td></tr><tr><td>

externalId

</td><td>

Unique external identifier for the topic, such as a GUID. This field is mapped to the topic\_id field in the associated Topic record.Data type: String

</td></tr><tr><td>

headerQuery

</td><td>

Filter to apply to the event header properties. This query defines the type of events to listen to for the associated topic. You can pass this parameter as a nested query.This parameter supports the following conditions:

-   AND: such as`variable1=value1&variable2=value2&variable3=value3`
-   OR: such as `variable1=value1,value2,value3`
-   Hierarchical variables: such as `variable1.variable2.variable3=value1`

For example: `"headerQuery": "eventType=TroubleTicketStatusChangeEvent,TroubleTicketAttributeChangeEvent"`

This field is mapped to the header\_query field in the associated topic record.

For additional information, refer to the [TMF688 Event Management API User Guide](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/).

Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the topic.This field is mapped to the topic\_name field in the associated topic record.

Data type: String

</td></tr><tr><td>

namespace

</td><td>

Namespace for the topic. Empty if there is no associated namespace.This field is mapped to the namespace field in the associated topic record.

Data type: String

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

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

201

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

`Topic external id passed already exists. Please pass the unique topic external id`: Indicates that passed external ID already exists in the Topic table.`Please pass the unique combination of topic name, header query, content query and namespace`: Indicates that the combination of topic name, namespace, header query, and content query already exists.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contentQuery

</td><td>

Value of the content\_query field in the created topic record.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Value of the topic\_id field in the created topic record.Data type: String

</td></tr><tr><td>

headerQuery

</td><td>

Value of the header\_query field in the created Topic record. This field is used by the topic picker framework to determine what event messages should be sent to a topic.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the created topic record.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the topic.Data type: String

</td></tr><tr><td>

namespace

</td><td>

Value of the namespace field in the created topic record.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "http://instance.servicenow.com/api/sn_api_notif_mgmt/topic" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
--data
{
  "name": "HighPriorityTroubleTicket",
  "headerQuery": "eventType=TroubleTicketStatusChangeEvent,TroubleTicketAttributeChangeEvent",
  "contentQuery": "troubleTicket.ticketType=incident&troubleTicket.severity=1",
  "externalId": "ext001",
  "namespace": "telecomEvents"
}
```

Response:

```

{
  "externalId": "ext001",
  "name": "HighPriorityTroubleTicket",
  "headerQuery": "eventType=TroubleTicketStatusChangeEvent,TroubleTicketAttributeChangeEvent",
  "contentQuery": "troubleTicket.ticketType=incident&troubleTicket.severity=1",
  "namespace": "telecomEvents",
  "id": "7ee9850443c3f550461f99612bb8f223"
}
```

