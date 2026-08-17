---
title: NowServiceError class - Android
description: The NowServiceError sealed class that returns NowSDK errors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/cllent-mobile-api-reference/NowServiceErrorAndroidAPI.html
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowServiceError class- Android

The NowServiceError sealed class that returns NowSDK errors.

|Name|Type|Description|
|----|----|-----------|
|cause|[Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/)|Cause of the error.|
|message|String|Message that contains the error details to display to the user.|

<table id="table_hr4_4tb_qgc"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SDKNotConfigured

</td><td>

The NowSDK was not configured. [`NowSDK.configure()`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowSDKAndroidAPI.md) was not called before creating the service.

</td></tr><tr><td>

ServiceConfigurationInvalid

</td><td>

The NowSDK was configured with invalid setting, such as a malformed instance URL.

</td></tr><tr><td>

ServiceDisabled

</td><td>

The associated service is turned off.If returned by [NowVoiceSDK - makeVoiceService\(instanceURL: URL\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceSDKAndroidAPI.md), voice is turned off on the instance. To use NowVoice, `sdk.voice.enabled` must be `true`.

</td></tr><tr><td>

ServiceSettingsInvalid

</td><td>

Unable to process the service settings.If returned by [NowVoiceSDK - makeVoiceService\(instanceURL: URL\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceSDKAndroidAPI.md), the `sdk.voice.enabled` key is missing from the instance settings.

</td></tr><tr><td>

ServiceSettingsNotFound

</td><td>

The instance doesn't have `sdk.voice` settings configured.

</td></tr><tr><td>

ServiceSettingsRetrievalFailed

</td><td>

A network or authentication error occurred. Unable to retrieve the NowSDK service settings from the ServiceNow instance.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/MobileSDKAndroidAPI.md)

