---
title: SNMobileAnalytics API
description: The SNMobileAnalytics API provides methods that you can call within a WebView using JavaScript. These methods enable you to push custom analytics data \(events, pages, and user properties\) to the User Experience Analytics for Service Portal dashboard.Adds a new web-triggered event with its associated properties to the current mobile session timeline.Adds a new screen UI action tag to the current mobile session time line.Sets the ID of the current active user for the current mobile session.Adds a new web-triggered page to the current mobile session time line.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# SNMobileAnalytics API

The SNMobileAnalytics API provides methods that you can call within a WebView using JavaScript. These methods enable you to push custom analytics data \(events, pages, and user properties\) to the User Experience Analytics for Service Portal dashboard.

To use these methods within your mobile application, you must first call the installJavascriptInterface\(\) method, which exposes these JavaScript methods to the associated WebView.

Refer to [NowAnalyticsService - installJavascriptInterface\(into webView: WKWebView\)](../../MobileSDKiOS/NowAnalyticsService/concept/NowAnalyticsServiceiOSProtocol.md#) for the iOS implementation.

Refer to [NowAnalyticsSDK - installJavascriptInterface\(webView: WebView\)](../../MobileSDKAndroid/NowAnalytics/concept/NowAnalyticsAndroidInterface.md#) for the Android implementation.

**Parent Topic:**[Mobile SDK API reference - iOS](../../MobileSDKiOS/concept/MobileSDKiOSAPI.md)

## SNMobileAnalytics - addEvent\(String eventName, Object properties\)

Adds a new web-triggered event with its associated properties to the current mobile session timeline.

<table id="table_mqk_vgf_mqb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

eventName

</td><td>

String

</td><td>

Name of the event to add.

</td></tr><tr><td>

properties

</td><td>

Object

</td><td>

Optional. List of custom property key-value pairs for the event. Supported value types:

-   Boolean
-   Date
-   Number
-   String

**Note:** The total size of the **eventName**, properties key and value should not exceed 300 bytes \(per event\).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
SNMobileAnalytics.addEvent('MyEvent', JSON.stringify({'Type': 'Show', 'Amount': 16}))
```

## SNMobileAnalytics - addScreenAction\(String actionName\)

Adds a new screen UI action tag to the current mobile session time line.

|Name|Type|Description|
|----|----|-----------|
|actionName|String|Name of the triggered web action.|

|Type|Description|
|----|-----------|
|None| |

```
SNMobileAnalytics.addScreenAction('Custom UI Action')
```

## SNMobileAnalytics - setUserId\(String userId\)

Sets the ID of the current active user for the current mobile session.

|Name|Type|Description|
|----|----|-----------|
|userID|String|ID to set for the current user.|

|Type|Description|
|----|-----------|
|None| |

```
SNMobileAnalytics.setUserId('user123') 
```

## SNMobileAnalytics - startScreen\(String screenName\)

Adds a new web-triggered page to the current mobile session time line.

|Name|Type|Description|
|----|----|-----------|
|screenName|String|Name of the screen to log the start time for, such as `WelcomeScreen`.|

|Type|Description|
|----|-----------|
|None| |

```
SNMobileAnalytics.startScreen('My Web Page')
```

