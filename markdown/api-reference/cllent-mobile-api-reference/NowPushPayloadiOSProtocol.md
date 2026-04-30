---
title: NowPushPayload protocol
description: NowPushPayload is a generic protocol you can use to define a push notification protocol within the NowSDK framework.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowPushPayload protocol

NowPushPayload is a generic protocol you can use to define a push notification protocol within the `NowSDK` framework.

<table id="table_g3x_ksb_qgc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

String

</td><td>

Message displayed to the user in the push notification, located in the **body** field of the push notification.

</td></tr><tr><td>

type

</td><td>

`NowPushType: String, Codable`

</td><td>

Type of push notification.Possible values:

-   launchVirtualAgent

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

