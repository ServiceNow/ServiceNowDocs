---
title: FieldReadConfiguration class - Android
description: The FieldReadConfiguration class provides the ability to define what fields to return or not return in a response record.Defines the fields to include in the return response from the associated ServiceNow table.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# FieldReadConfiguration class - Android

The FieldReadConfiguration class provides the ability to define what fields to return or not return in a response record.

|Name|Type|Description|
|----|----|-----------|
|includeFields|[Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/)​&lt;String&gt;|Fields to return in the response.|
|queryItems|[Map](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-map/)&lt;String, String&gt;|Read-only. Collection of query items representing the read configuration.|
|queryParams|QueryParams|Iterable structure that contains name-value pairs of request query parameters. Use these parameters to build a request.|

**Parent Topic:**[Mobile SDK API reference - Android](../../concept/MobileSDKAndroidAPI.md)

## FieldReadConfiguration - FieldReadConfiguration\(includeFields: Collection&lt;String&gt; = listOf\(\), vararg options: FieldReadConfiguration.Options\)

Defines the fields to include in the return response from the associated ServiceNow table.

<table id="table_mlz_4ps_4pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

includeFields

</td><td>

Collection&lt;String&gt;

</td><td>

List of comma-separated fields to return in the response. If the list is empty, all fields are returned.

</td></tr><tr><td>

vararg options

</td><td>

FieldReadConfiguration.Options

</td><td>

Optional. Array of zero or more options that define the type of field information to return.Possible values:

-   ACTUAL\_VALUES: Include the field's actual value in the response.
-   DISPLAY\_VALUES: Include the field's display value in the response.
-   EXCLUDE\_REFERENCE\_LINK: Exclude the Table API links for the reference fields.

</td></tr></tbody>
</table>The following code example shows how to call this function.

```
val readConfiguration = FieldReadConfiguration(
  includeFields = listOf("sys_id", "sys_created_on", "short_description"),
  options = arrayOf(FieldReadConfiguration.Options.DISPLAY_VALUES)
)
val fetchConfiguration = FetchConfiguration(
  filter = Filter("active=true"),
  readConfiguration = readConfiguration
)
val response = nowTableService.records("incident", fetchConfiguration).execute()
handleResponse(response)
```

