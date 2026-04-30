---
title: Push Installation API
description: The Push Installation API provides endpoints to register and unregister the tokens that enable mobile devices to receive push notifications from an application.Adds or updates tokens that enable devices to receive push notifications from the specified application.Deactivates the tokens that enable mobile devices to receive push notifications from the specified application.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Push Installation API

The Push Installation API provides endpoints to register and unregister the tokens that enable mobile devices to receive push notifications from an application.

A push notification is a text message that appears on a user's mobile device to alert them about something important or to ask them to perform an action.

When creating custom mobile applications, in order to set up Push notifications, you must register the device with the manufacturer’s service. The service must know the address of a user's device so it can properly send notifications to that device using push tokens. The device also needs to be able to receive the notifications and act on them. For instructions on how to register a device and get a push token, refer to the device’s operating systems developer documentation. For example, for Apple devices, refer to [https://developer.apple.com/documentation/usernotifications/registering\_your\_app\_with\_apns](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Push Installation - POST /now/push/\{pushApplicationName\}/installation

Adds or updates tokens that enable devices to receive push notifications from the specified application.

### URL format

Versioned URL: `/api/now/{api_version}/push/{pushApplicationName}/installation`

Default URL: `/api/now/push/{pushApplicationName}/installation`

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

pushApplicationName

</td><td>

Name of the application for which to register the push notifications. This parameter must be the same as the value in the Name column for the associated application.Data type: String

Table: Push Application \[sys\_push\_application\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

platform

</td><td>

Platform on which to register the push notification. Data type: String

Table: In the Name field of the Push Platform \[sys\_push\_platform\] table.

</td></tr><tr><td>

token

</td><td>

Token supplied by the device manufacturer, such as Apple, when the mobile application registers to receive push notifications. Data type: String

Stored in: Push Notification Installation \[sys\_push\_notif\_app\_install\]

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
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
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|None||

### Sample cURL request

```
curl -X POST \
  https://instance.servicenow.com/api/now/push/ServiceNowPushApp/installation \
--header "Content-Type: application/json" \
--user "username":"password" \
--data '{"platform":"Apple","token":"544836d77ac2e551bbf78204630509a7d494fc87f52e85da52e5b5d42910e2cf"}' \
```

```
None
```

## Push Installation - POST /now/push/\{pushApplicationName\}/removeInstallation

Deactivates the tokens that enable mobile devices to receive push notifications from the specified application.

### URL format

Versioned URL: `/api/now/{api_version}/push/{pushApplicationName}/removeInstallation`

Default URL: `/api/now/push/{pushApplicationName}/removeInstallation`

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

pushApplicationName

</td><td>

Name of the application for which to unregister the push notifications.Data type: String

Table: In the Name field for the associated application in the Push Application \[sys\_push\_application\] table.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

platform

</td><td>

Platform on which to register the push notification. Data type: String

Table: In the Name field of the Push Platform \[sys\_push\_platform\] table.

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
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
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|None||

### Sample cURL request

```
curl -X POST \
  https://instance.servicenow.com/api/now/push/ServiceNowPushApp/removeInstallation \
--header "Content-Type: application/json" \
--user "username":"password" \
--data '{"platform":"Apple"}' \
```

```
None
```

