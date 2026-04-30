---
title: Reference field attributes for input form screens in offline mode
description: Configure the fields that you want to use and the data you want to display in offline mode by using various input attributes.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure for input form screens, Offline mode, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Reference field attributes for input form screens in offline mode

Configure the fields that you want to use and the data you want to display in offline mode by using various input attributes.

**Note:**

-   You must create an input form screen before you create variables and attributes. For information about creating an input form screen, see [Configure an input form screen](../task/parameter-screen-config.md).
-   Offline mode is only available on the Mobile Agent app.

## Reference inputs

Use reference inputs for inputs that reference a field on a table. These inputs work like [reference fields](https://www.servicenow.com/docs/access?context=c_ReferenceField&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) in the forms on your instance. You can configure your reference input with conditions, reference qualifiers, and a search option to help your users find what they need quickly.

You can use these attributes with reference inputs.

**Note:** All attributes are case-sensitive.

|Attribute|Description|
|---------|-----------|
|SourceTable|The source table for your reference qualifier.|
|SourceFieldName|The field name of the referenced field in the source table.|
|TargetTable|The table you want to target for your reference qualifier.|

The following additional attributes are optional:

<table id="table_anh_jbw_b4b"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OfflineMobileViewId

</td><td>

Define the mobile card used to display reference field data in offline mode. The **OfflineMobileViewId** attribute takes precedence over the **MobileViewId** attribute.

</td></tr><tr><td>

EnableSearch

</td><td>

Option to determine whether the search bar displays. The value must be **true** or **false**.

</td></tr><tr><td>

OfflineConditions

</td><td>

Encoded query condition used to query the reference data. The **OfflineConditions** attribute takes precedence over the **Conditions** attribute.**Note:** This attribute can also be used when the **Conditions** attribute has a condition that cannot be supported in offline.

</td></tr><tr><td>

SearchType

</td><td>

Defines the query used for search. The value can be `starts_with` or `contains`. If this attribute is not configured, the instance uses `starts_with` by default on the display label column.

</td></tr><tr><td>

OfflineFetchScript

</td><td>

Use to specify a list of Sys IDs for reference records. Using this attribute, you can define what records to cache while in offline mode.

 Reference fields can return many thousands of records, but only 1,000 records are supported to cache for offline mode. Use this attribute to define the specific records \(1,000 or less\) that you want to cache for use while offline.

 If this attribute is not used, then the first 1,000 records returned are cached.

</td></tr><tr><td>

OfflineMaxNumRecords

</td><td>

Defines the number of records that you can cache in offline mode. The maximum number is 1000.You can set a different value for each reference input.

</td></tr></tbody>
</table>**Parent Topic:**[Configure reference inputs for input form screens in offline mode](../task/reference-fields-offline-mode.md)

