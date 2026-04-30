---
title: FieldReadConfiguration structure - iOS
description: The FieldReadConfiguration structure enables you to configure which fields to fetch from a ServiceNow instance table and in which format.Configures the fields within a record in a ServiceNow table to pass back in the return results of a REST endpoint call.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# FieldReadConfiguration structure- iOS

The FieldReadConfiguration structure enables you to configure which fields to fetch from a ServiceNow instance table and in which format.

<table id="table_vx2_klw_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

includeFields

</td><td>

Array

</td><td id="mobile_sdk_ios-includeFields-entry">

List of fields to pass back in the return results.

</td></tr><tr><td>

options

</td><td>

Array

</td><td id="mobile_sdk_ios-options-entry">

List of the types of fields to return.Possible values:

-   actualValues: Returns the values actually stored in each of the fields, including the sys\_ids for referenced records. Use this setting if dates need to be decoded in Codable models using Date.
-   description: Returns the description of the parameter.
-   displayValues: Returns the [display values](https://www.servicenow.com/docs/access?context=c_DisplayValues&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US), if available, for the selected fields. For example, user names typically contain a reference link \(sys\_id\) to the user record. If you request the display value, the person's name is returned instead of the sys\_id that is stored in the associated field.

**Note:** Display values returned by a ServiceNow instance are formatted and internationalized based on the user profile configuration of the authenticated user. This may differ from the device language and locale settings on the device.

-   excludeReferenceLink: Does not return any data that is defined as reference links within the table.
-   rawValue: Returns the raw value of the parameter.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

## FieldReadConfiguration - init\(includeFields: \[FieldName\] = \[\], options: Options = \[\]\)

Configures the fields within a record in a ServiceNow table to pass back in the return results of a REST endpoint call.

<table id="table_b5w_5sp_kqb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

includeFields

</td><td>

Array

</td><td id="mobile_sdk_ios-includeFields-entry">

List of fields to pass back in the return results.

</td></tr><tr><td>

options

</td><td>

Array

</td><td id="mobile_sdk_ios-options-entry">

List of the types of fields to return.Possible values:

-   actualValues: Returns the values actually stored in each of the fields, including the sys\_ids for referenced records. Use this setting if dates need to be decoded in Codable models using Date.
-   description: Returns the description of the parameter.
-   displayValues: Returns the [display values](https://www.servicenow.com/docs/access?context=c_DisplayValues&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US), if available, for the selected fields. For example, user names typically contain a reference link \(sys\_id\) to the user record. If you request the display value, the person's name is returned instead of the sys\_id that is stored in the associated field.

**Note:** Display values returned by a ServiceNow instance are formatted and internationalized based on the user profile configuration of the authenticated user. This may differ from the device language and locale settings on the device.

-   excludeReferenceLink: Does not return any data that is defined as reference links within the table.
-   rawValue: Returns the raw value of the parameter.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

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
  let filter = Filter(criteria: [], sortBy: [.desc("opened_at")], queryCategory: nil)
  return FetchConfiguration(filter: filter, limit: 10, readConfiguration: readConfiguration)
}()
```

