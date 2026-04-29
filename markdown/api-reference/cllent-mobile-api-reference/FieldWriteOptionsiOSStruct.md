---
title: FieldWriteOptions class - iOS
description: The FieldWriteOptions class provides functions that set the options for updating or creating fields in a record on a ServiceNow instance.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# FieldWriteOptions class- iOS

The FieldWriteOptions class provides functions that set the options for updating or creating fields in a record on a ServiceNow instance.

<table id="table_vx2_klw_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

rawValue

</td><td>

Integer

</td><td>

Result of the bitwise operation of the `suppressAutoSysField` and the `treatInputValuesAsDisplayValues` properties.

</td></tr><tr><td>

suppressAutoSysField

</td><td>

Boolean

</td><td>

Flag that indicates whether to suppress the automatic generation of system fields.Possible values:

-   true: Suppress automatic generation of system fields.
-   false: Allow automatic generation of system fields.

Default: false

</td></tr><tr><td>

treatInputValuesAsDisplayValues

</td><td>

Boolean

</td><td>

Flag that indicates whether to set field values using their display value rather than the actual value.Possible values:

-   true: Use display value.
-   false: Use actual value.

Default: false

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

