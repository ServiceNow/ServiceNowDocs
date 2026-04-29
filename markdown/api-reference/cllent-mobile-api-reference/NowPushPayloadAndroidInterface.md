---
title: NowPushPayload interface - Android
description: The NowPushPayload interface defines the push notification payload that the NowSDK implements.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowPushPayload interface- Android

The NowPushPayload interface defines the push notification payload that the NowSDK implements.

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

instanceId

</td><td>

ServiceNow instance identifier as provided by the push notification system.Data type: String

</td></tr><tr><td>

instanceName

</td><td>

ServiceNow instance name.Data type: String

</td></tr><tr><td>

message

</td><td>

Body of the push notification.Data type: String

</td></tr><tr><td>

notificationId

</td><td>

Unique identifier for this push notification.Data type: Integer

</td></tr><tr><td>

threadId

</td><td>

ID to use to group notifications. User the same ID in different payloads to indicate a group.Data type: String

</td></tr><tr><td>

title

</td><td>

Title of the push notification.Data type: String

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK - Android](../../concept/MobileSDKAndroidAPI.md)

