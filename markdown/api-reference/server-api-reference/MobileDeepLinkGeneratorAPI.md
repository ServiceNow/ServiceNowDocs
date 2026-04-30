---
title: MobileDeepLinkGenerator - Global
description: The MobileDeepLinkGenerator script include provides methods to embed a link to a mobile app list or form applet.Instantiates a MobileDeepLinkGenerator object for a specific mobile app.Create a link to a form applet.Create a link to a list applet.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# MobileDeepLinkGenerator- Global

The MobileDeepLinkGenerator script include provides methods to embed a link to a mobile app list or form applet.

Use this script include in a global server-side script to create a link to a list or form applet within these apps:

-   Now Mobile
-   Mobile Agent
-   Mobile Onboarding

**Note:**

The Mobile Onboarding application is being deprecated!

With the ServiceNow AI Platform Rome release in September 2021, we started phasing out support for the Mobile Onboarding application. Customers may no longer activate it, and we are not offering enhancements or non-critical bug fixes. Mobile onboarding features are available in the [Now Mobile app for HR Service Delivery](https://www.servicenow.com/docs/access?context=mobile-employee-experience-for-hr-service-delivery&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

For example, create a link from an email, push notification, or Virtual Agent conversation that opens a record or list of records in the app. The form or list only includes data that the user has access rights to view.

For an example of this API used in a push notification, see [Configure push notification message content](https://www.servicenow.com/docs/access?context=config-push-notification-message-content&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US). For additional information on deep links, see [Deep linking for mobile](https://www.servicenow.com/docs/access?context=deep-link-mobile&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## MobileDeepLinkGenerator - MobileDeepLinkGenerator\(String clientType\)

Instantiates a MobileDeepLinkGenerator object for a specific mobile app.

<table id="table_fzm_gjr_vhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

clientType

</td><td>

String

</td><td>

Name of the app to create a link to. Options include:

 -   agent: Creates a link to a list or screen in the Mobile Agent app.
-   request: Creates a link to a list or screen in the Now Mobile app.
-   onboarding: Creates a link to a list or screen in the Mobile Onboarding.

</td></tr></tbody>
</table>**Note:**

The Mobile Onboarding application is being deprecated!

With the ServiceNow AI Platform Rome release in September 2021, we started phasing out support for the Mobile Onboarding application. Customers may no longer activate it, and we are not offering enhancements or non-critical bug fixes. Mobile onboarding features are available in the [Now Mobile app for HR Service Delivery](https://www.servicenow.com/docs/access?context=mobile-employee-experience-for-hr-service-delivery&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

```
var glide = new global.MobileDeepLinkGenerator('onboarding');
```

## MobileDeepLinkGenerator - getFormScreenLink\(String formScreenId, String tableName, String recordSysId\)

Create a link to a form applet.

|Name|Type|Description|
|----|----|-----------|
|formScreenId|String|Sys ID of the applet record in the Applets \[sys\_sg\_screen\] table.|
|tableName|String|Name of the table containing the record in the **recordSysId** parameter.|
|recordSysId|String|Sys ID of the record to open in the applet.|

|Type|Description|
|----|-----------|
|String|Link to the record in the mobile app form applet.|

```
var deepLinkGenerator = new global.MobileDeepLinkGenerator("agent");
var link = deepLinkGenerator.getFormScreenLink("<sys_id>", current.getTableName(), current.getValue("sys_id"));
```

## MobileDeepLinkGenerator - getScreenLink\(String documentId, Object uiParams\)

Create a link to a list applet.

|Name|Type|Description|
|----|----|-----------|
|documentId|String|Sys ID of the applet record in the Applets \[sys\_sg\_screen\] table.|
|uiParams|Object|Optional. JSON object containing any URL parameters to include in the link. Determine which URL parameters to include by inspecting the URL you want to link to. In general, URL parameters filter records in the list. For example, `var param = {'<company-sys-id>': 'servicenow'}`, where `<company-sys-id>` is the Sys ID of a company UI parameter from the UI Parameters \[sys\_sg\_ui\_parameter\] table for a specific mobile screen.|

|Type|Description|
|----|-----------|
|String|Link to the mobile app list applet.|

```
var uiParams = {
    "b250294ab3c12300a0d56ad4c6a8dc8c": "servicenow", 
    "7250294ab3c12300a0d56ad4c6a8dc90": "santa clara"}

var deepLinkGenerator = new global.MobileDeepLinkGenerator("request");
var link = deepLinkGenerator.getScreenLink("a75df1920f2033001befa68ca8767e50", uiParams);
```

