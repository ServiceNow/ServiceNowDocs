---
title: NowServiceError class - Android
description: The NowServiceError sealed class that returns NowSDK errors.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowServiceError class- Android

The NowServiceError sealed class that returns NowSDK errors.

|Name|Type|Description|
|----|----|-----------|
|cause|[Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/)|Cause of the error.|
|message|String|Message that contains the error details to display to the user.|

|Type|Description|
|----|-----------|
|SDKNotConfigured|The NowSDK was not configured. Most likely the NowSDK.configure\(\) method was not called.|
|ServiceConfigurationInvalid|The NowSDK was configured with invalid setting. Verify that all settings in the configuration are correct.|
|ServiceDisabled|The associated service is disabled.|
|ServiceSettingsInvalid|Unable to process the service settings.|
|ServiceSettingsRetrievalFailed|Unable to retrieve the NowSDK service settings from the ServiceNow instance.|

**Parent Topic:**[Mobile SDK - Android](../../concept/MobileSDKAndroidAPI.md)

