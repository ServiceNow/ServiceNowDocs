---
title: Configure field write options
description: Within the Mobile SDK, when writing data to a ServiceNow instance through a REST endpoint, you can define field write options.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/mobsdk-and-write\_options.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Interact with table data in a ServiceNow instance, Mobile SDK Developer Guide - Android, Developer guides, API implementation and reference]
---

# Configure field write options

Within the Mobile SDK, when writing data to a ServiceNow instance through a REST endpoint, you can define field write options.

You configure field write options using the [FieldWriteOptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/FieldWriteOptionsAndroidAPI.md) API. This interface enables you to configure:

-   Whether to suppress automatic generation of system fields.
-   Whether to set field values using their display valuedisplay value rather than their actual value.

