---
title: NowServiceConfiguration structure - iOS
description: The NowServiceConfiguration structure defines configuration information for a feature service.Configures the calling feature service with the specified configuration information.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowServiceConfiguration structure - iOS

The NowServiceConfiguration structure defines configuration information for a feature service.

|Name|Type|Description|
|----|----|-----------|
|appBundleId|String|Bundle ID of the application integrating with the NowSDK.|
|instanceUrl|String|URL of the ServiceNow instance that the feature service will access. For example: `https://instance.servicenow.com`.|

**Parent Topic:**[Mobile SDK API reference - iOS](../../concept/MobileSDKiOSAPI.md)

## NowServiceConfiguration - init\(instanceUrl: URL, appBundleId: String\)

Configures the calling feature service with the specified configuration information.

|Name|Type|Description|
|----|----|-----------|
|instanceUrl|String|URL of the ServiceNow instance that the feature service will access. For example: `https://instance.servicenow.com`.|
|appBundleId|String|Bundle ID of the application integrating with the NowSDK.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
guard 
  let instanceUrl = URL(string: "https://instance.service-now.com") else {
    return
  }

NowServiceConfiguration(instanceUrl: instanceUrl, appBundleId: "com.servicenow.appBundle")
```

