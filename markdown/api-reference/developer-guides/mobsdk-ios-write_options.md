---
title: Configure field write options
description: Within the Mobile SDK, when writing data to a ServiceNow instance through a REST endpoint, you can define field write options.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/mobsdk-ios-write\_options.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Interact with table data in a ServiceNow instance, Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Configure field write options

Within the Mobile SDK, when writing data to a ServiceNow instance through a REST endpoint, you can define field write options.

You configure field write options using the [FieldWriteOptions class - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/FieldWriteOptionsiOSStruct.md) structure. This structure enables you to configure:

-   Whether to suppress automatic generation of system fields.
-   Whether to set field values using their [display value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/c_DisplayValues.md)[display value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/c_DisplayValues.md) rather than their actual value.

