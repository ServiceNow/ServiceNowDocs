---
title: FieldWriteOptions structure - Android
description: The FieldWriteOptions class provides functions that set the options for updating or creating fields in a record on a ServiceNow instance.Sets the options for writing or creating fields in a record on your ServiceNow instance.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# FieldWriteOptions structure - Android

The FieldWriteOptions class provides functions that set the options for updating or creating fields in a record on a ServiceNow instance.

|Name|Type|Description|
|----|----|-----------|
|queryItems|[Map](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/)&lt;String, String&gt;|Collection of request query items that represent the write options.|

**Parent Topic:**[Mobile SDK API reference - Android](../../concept/MobileSDKAndroidAPI.md)

## FieldWriteOptions - FieldWriteOptions\(vararg options: FieldWriteOptions.Options\)

Sets the options for writing or creating fields in a record on your ServiceNow instance.

<table id="table_xth_4vs_4pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

vararg options

</td><td>

FieldWriteOptions.Options

</td><td>

Options to set when creating or writing to fields.Valid values:

-   TREAT\_INPUT\_VALUES\_AS\_DISPLAY\_VALUES: Specified field values should be saved as the display values. If this value isn't set to `true`, the passed values are assumed to be the actual field values.
-   SUPPRESS\_AUTO\_SYS\_FIELD: Suppress auto-generation of system fields.

</td></tr></tbody>
</table>The following code example shows how to call this function.

```
// Update assigned_to field using actual value (syd_id of user)
val response = runCatching {
    getNowTableService()?.updateRecord("sys_id_of_record", "sn_customerservice_case", mapOf("assigned_to" to "<sys_id_of_user>"))?.execute()
}

// Update assigned_to field using display value
val fieldWriteOptions = FieldWriteOptions(FieldWriteOptions.Options.TREAT_INPUT_VALUES_AS_DISPLAY_VALUES)
val response = runCatching {
    getNowTableService()?.updateRecord("sys_id_of_user", "sn_customerservice_case", mapOf("assigned_to" to "John Doe"))?.execute()
}
```

