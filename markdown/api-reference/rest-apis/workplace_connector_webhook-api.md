---
title: Workplace Connector Webhook API
description: The Workplace Connector Webhook API is a generic interface that enables data from different kinds of workplace hardware or sensors \(such as badging systems or occupancy sensors\) to be stored in Workplace Service Delivery tables.Creates a record in the Connector Events \[sn\_wsd\_wc\_connector\_events\] table and then stores the hardware/sensor-based event data passed in the endpoint's payload into the Payload field of that record.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Workplace Connector Webhook API

The Workplace Connector Webhook API is a generic interface that enables data from different kinds of workplace hardware or sensors \(such as badging systems or occupancy sensors\) to be stored in Workplace Service Delivery tables.

This API runs in the `sn_wsd_wc` namespace. To access this API the Workplace Connectors \(com.sn\_wsd\_wc\) plugin must be activated.

Before calling this API, you must configure records in the Connector Configuration \[sn\_wsd\_wc\_connector\_config\] and Provider Configuration \[sn\_wsd\_wc\_provider\_config\] tables. For information on how to configure these records, see Configure Workplace Connectors.

In addition, you must set up an extension point that defines the data conversion/mapping from the hardware/sensor-based event payload to the target ServiceNow table, such as the Employee Attendance Data \[sn\_wsd\_wc\_employee\_attendance\_data\] table.

For additional information on workplace connector webhooks, see Workplace Connectors.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Workplace Connector Webhook - POST /workplace\_connector\_webhook/event

Creates a record in the Connector Events \[sn\_wsd\_wc\_connector\_events\] table and then stores the hardware/sensor-based event data passed in the endpoint's payload into the Payload field of that record.

After the endpoint stores the payload, it sets the State field within the Connector Events record to `new`, indicating the payload hasn’t been processed.

A scheduled job locates the new badging records in the Connector Events table and transforms and writes them to the Employee Attendance Data \[sn\_wsd\_wc\_employee\_attendance\_data\] table. The State field is then set to `processed`.

The mapping of the data between the payload data in the Connector Events record and the Employee Attendance Data record is defined in an extension point. This extension point is identified in the Extension Point Definition field in the associated Connector Configuration \[sn\_wsd\_wc\_connector\_config\] table. For this endpoint, this is the BadgingDataHandler extension point.

**Note:** Records in the Connector Events table in the `processed` state are purged after two days from the creation date. Records in the `error` state are purged after seven days from the date of creation. Records in the `new`state are never purged.

### URL format

Versioned URL: `/api/sn_wsd_wc/{api_version}/workplace_connector_webhook/event`

Default URL: `/api/sn_wsd_wc/workplace_connector_webhook/event`

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

ni.nolog.id

</td><td>

Required. Sys\_id of the provider configuration record associated with the hardware that generated the event information.Data type: String

Table: Provider Configuration \[sn\_wsd\_wc\_provider\_config\]

</td></tr><tr><td>

token\_name

</td><td>

Name of the security token, such as a user name or other value that identifies the security token. Used for authenticating the request.Data type: String

Table: Provider configuration \[sn\_wsd\_wc\_provider\_config\]

</td></tr><tr><td>

token\_value

</td><td>

Value associated with the security token, such as a password. Used for authenticating the request.Data type: String

Table: Provider configuration \[sn\_wsd\_wc\_provider\_config\]

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;payload&gt;

</td><td>

Name-value pairs of the hardware/sensor-based event data. The names must correspond to the names identified in the BadgingDataHandler extension point.

For example:

```
{
  "Time zone": "(UTC-08:00) Pacific Time (US & Canada)",
  "Event": "Access granted",
  "Door": "L_SJC005_B1.101_ELEVATOR 2 INT",
  "Side": "Reader - In",
  "Cardholder": "ninat.salem",
  "First name": "Nina T",
  "Last name": "Salem",
  "Credential": " ninat.salem's credential",
  "Employee ID (Cardholder)": "10097",
  "Event timestamp": "11/07/2022 00:56:57"
}
```

You can pass multiple event's data within a single endpoint call. Pass each event's data in a separate object. Each event's data is stored in a separate Employee Attendance Data record.

**Note:** Ensure that any provided timestamp adheres to ISO 8601 formatting to avoid any issues with date parsing.

Data type: JSON object

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
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Description of any error that occurred during the processing of the data.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
"status": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Information that provides details about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the endpoint processing.Possible values:

-   failure: Endpoint failed. Refer to the **error** object for additional details.
-   success: Endpoint completed successfully. Record was added.

Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint to add multiple card reader events to the Connector Events table. Before processing the request, the request is authenticated.

```
curl http://instance.servicenow.com/api/sn_wsd_wc/v1/workplace_connector_webhook/event?token_name=token&ni.nolog.id=8e666cb0a3053110bc6e146546fcdad1&token_value=babugosha  \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data --data "{
  \"Time zone\": \"(UTC+02:00) Jerusalem\",
  \"Event\": \"Access granted\",
  \"Door\": \"L_TLV001_A3.07_KITCHEN AREA INT\",
  \"Side\": \"Reader - In\",
  \"Cardholder\": \" ninat.alem\",
  \"First name\": \" Nina T\",
  \"Last name\": \" Salem\",
  \"Credential\": \" ninat.salem's credential\",
  \"Employee ID (Cardholder)\": 10097,
  \"Event timestamp\": \"11/07/2022 10:57:24\"
}
{
  \"Time zone\": \"(UTC+02:00) Jerusalem\",
  \"Event\": \"Access granted\",
  \"Door\": \"L_TLV003_A4.07_FRONT ENT\",
  \"Side\": \"Reader - In\",
  \"Cardholder\": \" joe.blue\",
  \"First name\": \" Joe\",
  \"Last name\": \" Blue\",
  \"Credential\": \" joe.blue's credential\",
  \"Employee ID (Cardholder)\": 24098,
  \"Event timestamp\": \"11/07/2022 10:59:33\"
}"
```

Response:

```
// Successful response
{
  "staus": "success"
}

// Error response
{
  "error": {
    "message": "Events request is invalid. Events query parms incomplete, some fields are missing",
    "detail": "Missing fields: token_name, token_value"
  }
  "status": "failure"
}
```

