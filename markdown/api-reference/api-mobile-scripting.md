---
title: Mobile Scripting API reference
description: Mobile Scripts are JavaScript APIs that you write in the sn\_mobile\_scripting scoped namespace to evaluate conditions and read or update records for mobile app components.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/api-mobile-scripting.html
release: brazil
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [API reference, API implementation and reference]
---

# Mobile Scripting API reference

Mobile Scripts are JavaScript APIs that you write in the sn\_mobile\_scripting scoped namespace to evaluate conditions and read or update records for mobile app components.

Mobile scripting supports a smaller set of classes and methods than server-side scripting, because the same script must be able to run against the local database on a device. Depending on the use case and execution context, a mobile script runs on the device or on the instance.

Whether a script that uses this API is evaluated on the instance or on the device depends on how the component that runs the script is configured. The same script is used in both cases, without modification.

## Supported components

Mobile scripts are currently supported for the following components:

-   **Button conditions**: Determine whether a button is shown or enabled for the current record and user.
-   **Write-back actions \(WBA\)**: Set field values on a record when the action runs.

## Available classes

-   [MobileGlideDate - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideDateScopedAPI.md): Work with date values.
-   [MobileGlideDateTime - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideDateTimeScopedAPI.md): Work with date and time values.
-   [MobileGlideElement - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideElementScopedAPI.md): Read and set values on a single field.
-   [MobileGlideRecord - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideRecordScopedAPI.md): Query, read, and update records.
-   [MobileGlideSystem - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideSystemScopedAPI.md) \(mgs\): Utility methods for the current user, session, and date-time values.
-   [MobileGlideTime - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideTimeScopedAPI.md): Work with time values.
-   [MobileGlideUser - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileGlideUserScopedAPI.md): Access the current user's profile, roles, and groups.
-   [MobileScripts - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/MobileScriptsScopedAPI.md): Load and invoke custom mobile scripts.

## Instantiating a class

```
var gr = new sn_mobile_scripting.MobileGlideRecord('incident');
```

MobileGlideSystem is available as the mgs object and doesn't require instantiation.

## API access requirements

The Mobile Scripting classes are provided within the sn\_mobile\_scripting namespace and require the Mobile Scripting plugin \(com.glide.sg.mobile\_scripting\).

To create or modify the scripts that call this API, you need the mobile\_admin role.

