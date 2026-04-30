---
title: NowAPIEndpoint protocol - iOS
description: The NowAPIEndpoint protocol provides an interface for accessing any publicly exposed ServiceNow REST APIs.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowAPIEndpoint protocol - iOS

The NowAPIEndpoint protocol provides an interface for accessing any publicly exposed ServiceNow REST APIs.

<table id="table_vx2_klw_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

httpMethod

</td><td>

String

</td><td>

HTTP method that the associate endpoint implements, such as get, delete, post, put, and patch.

</td></tr><tr><td>

relativePath

</td><td>

String

</td><td>

Path of the associated endpoint relative to the `/api` path. For example: `/api/now/account`

</td></tr><tr><td>

requiresAuthentication

</td><td>

Boolean

</td><td>

Flag that indicates whether the endpoint requires authentication.Default: true

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK API reference - iOS](../../concept/MobileSDKiOSAPI.md)

