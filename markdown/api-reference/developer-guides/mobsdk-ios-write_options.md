---
title: Configure field write options
description: Within the Mobile SDK, when writing data to a ServiceNow instance through a REST endpoint, you can define field write options.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Interact with table data in a ServiceNow instance, Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Configure field write options

Within the Mobile SDK, when writing data to a ServiceNow instance through a REST endpoint, you can define field write options.

You configure field write options using the [FieldWriteOptions class - iOS](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/FieldWriteOptions/concept/FieldWriteOptionsiOSStruct.md#) structure. This structure enables you to configure:

-   Whether to suppress automatic generation of system fields.
-   Whether to set field values using their [display value](https://www.servicenow.com/docs/access?context=c_DisplayValues&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)[display value](https://www.servicenow.com/docs/access?context=c_DisplayValues&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) rather than their actual value.

