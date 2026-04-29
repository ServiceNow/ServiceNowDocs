---
title: Transform data
description: The NowData framework provides the ability to easily transform data into records.
locale: en-US
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Interact with table data in a ServiceNow instance, Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Transform data

The NowData framework provides the ability to easily transform data into records.

Using the [NowRecord](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowRecord/concept/NowRecordiOSAPI.md#) convenience structure, which contains the properties `sysId` and `fields`, you can easily transform data into a record. Whenever you obtain a `Data` wrapping `Result` or `Publisher`, you can easily transform it into a `NowRecord` wrapping `Result` or `Publisher` using the convertToRecord\(\) and convertToRecords\(\) methods. For additional information, see [NowTableService class - iOS](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowTableService/concept/NowTableServiceiOSAPI.md#).

**Note:** While NowRecord makes it very easy to quickly obtain data, depending on your use case, the Codable methods might be preferable as a strongly typed Codable structure provides more flexibility than a collection of "any" fields.

