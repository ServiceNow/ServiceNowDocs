---
title: FetchConfiguration structure - iOS
description: The FetchConfiguration structure provides the ability to define the configuration for fetching records from your ServiceNow instance.Defines the criteria for what records, and associated fields within those records, to return when fetching data from a ServiceNow instance through a REST endpoint.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Mobile SDK API reference - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# FetchConfiguration structure - iOS

The FetchConfiguration structure provides the ability to define the configuration for fetching records from your ServiceNow instance.

<table id="table_vx2_klw_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

filter

</td><td>

[Filter](../../Filter/concept/FilteriOSStructure.md#)

</td><td>

Optional. Query to apply to the return results. For example, to return only active records with a short description that contains the word "broken", pass the following query: `active=true^short_descriptionLIKEbroken`Default: nil - No filter applied, all records returned \(any system or table limits are honored.\)

</td></tr><tr><td>

limit

</td><td>

Integer

</td><td>

Optional. Number of records to return per page/response.Default: nil - All records returned \(any system or table limits are honored.\)

</td></tr><tr><td>

readConfiguration

</td><td>

[FieldReadConfiguration](../../FieldReadConfiguration/concept/FieldReadConfigurationiOSStruct.md#)

</td><td>

Optional. Configuration of the fields returned in the response.Default: nil - All fields are returned.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK API reference - iOS](../../concept/MobileSDKiOSAPI.md)

## FetchConfiguration - init\(filter: Filter? = nil, limit: Int? = nil, readConfiguration: FieldReadConfiguration? = nil\)

Defines the criteria for what records, and associated fields within those records, to return when fetching data from a ServiceNow instance through a REST endpoint.

<table id="table_pgj_tg2_vpb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

filter

</td><td>

[Filter](../../Filter/concept/FilteriOSStructure.md#)

</td><td>

Optional. Query to apply to the return results. For example, to return only active records with a short description that contains the word "broken", pass the following query: `active=true^short_descriptionLIKEbroken`Default: nil - No filter applied, all records returned \(any system or table limits are honored.\)

</td></tr><tr><td>

limit

</td><td>

Integer

</td><td>

Optional. Number of records to return per page/response.Default: nil - All records returned \(any system or table limits are honored.\)

</td></tr><tr><td>

readConfiguration

</td><td>

[FieldReadConfiguration](../../FieldReadConfiguration/concept/FieldReadConfigurationiOSStruct.md#)

</td><td>

Optional. Configuration of the fields returned in the response.Default: nil - All fields are returned.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

Shows how to configure the data to fetch from the Table API.

```
/// The configuration for what to fetch from the Table API.
lazy var fetchConfiguration: FetchConfiguration = {
  let includeFields = [
    // Case details
    "number",
    "short_description",
    "priority",
    "state",
    "opened_at",
    
    // Account details
    "account.name",
    "account.number",
    "contact.name",
    "contact.email",
    "contact_type",

    // Assignment
    "assignment_group.name",
    "assigned_to.name"
  ]
  let readConfiguration = FieldReadConfiguration(includeFields: includeFields, options: .actualValues)
  let filter = Filter(criteria: [], sortBy: [.desc("number")], queryCategory: nil)
  return FetchConfiguration(filter: filter, limit: 10, readConfiguration: readConfiguration)
}()
```

