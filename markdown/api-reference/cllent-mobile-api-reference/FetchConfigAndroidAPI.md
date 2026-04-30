---
title: FetchConfiguration class - Android
description: The FetchConfiguration class provides the ability to define the configuration for fetching records from the associatedServiceNow table.Enables you to define the records and fields to return from the associated ServiceNow table.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# FetchConfiguration class- Android

The FetchConfiguration class provides the ability to define the configuration for fetching records from the associatedServiceNow table.

This class only contains a single function \(constructor\), [FetchConfiguration\(\)](FetchConfigAndroidAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|filter|[Filter](../../Filter/concept/FilterAndroidAPI.md#)|Query to use to filter the return results.|
|limit|Integer|Number of records per page/response to return.|
|queryParams|QueryParams|Iterable structure that contains name-value pairs of request query parameters.|
|readConfiguration|[FieldReadConfiguration](../../FieldReadConfiguration/concept/FieldReadConfigAndroidAPI.md#)|Configuration for the fields to return in the response.|

**Parent Topic:**[Mobile SDK - Android](../../concept/MobileSDKAndroidAPI.md)

## FetchConfiguration - FetchConfiguration\(filter: Filter? = null, limit: Int? = null, readConfiguration: FieldReadConfiguration? = null\)

Enables you to define the records and fields to return from the associated ServiceNow table.

<table id="table_bjv_mls_4pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

filter

</td><td>

[Filter](../../Filter/concept/FilterAndroidAPI.md#)

</td><td>

Optional. Query to use to filter the records that are returned from the table. For example: `active=true^short_descriptionLIKEbroken`Default: null - Return all records.

</td></tr><tr><td>

limit

</td><td>

Integer

</td><td>

Optional. Number of records to return per page/response.Default: null - Return the maximum allowed by the ServiceNow REST API.

</td></tr><tr><td>

readConfiguration

</td><td>

[FieldReadConfiguration](../../FieldReadConfiguration/concept/FieldReadConfigAndroidAPI.md#)

</td><td>

Optional. Configuration of the fields returned in the response.Default: null - Return all fields.

</td></tr></tbody>
</table>The following code example shows how to call this function.

```
nowTableService.records("incident", FetchConfiguration( 
  filter = Filter("active=true"), 
  limit = 10, 
  readConfiguration = FieldReadConfiguration( 
    includeFields = listOf("sys_id", "short_description") 
  ) 
))
```

