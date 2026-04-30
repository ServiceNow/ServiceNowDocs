---
title: cabrillo - Client
description: Cabrillo JS is a client side JavaScript API for accessing capabilities inside ServiceNow native mobile applications.Boolean value indicating if Cabrillo JS is executing a ServiceNow native mobile application.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Client mobile API reference, API reference, API implementation and reference]
---

# cabrillo - Client

Cabrillo JS is a client side JavaScript API for accessing capabilities inside ServiceNow native mobile applications.

Use Cabrillo JS to build a custom mobile experience in ServiceNow native mobile applications. Cabrillo JS provides APIs to use native device capabilities, native mobile UI, and other ServiceNow mobile functionality.

Cabrillo JS is available in AngularJS as an injectable parameter. For example, you can inject Cabrillo JS in a Service Portal widget client script.

```
function(cabrillo) {
    var c = this;

    // Used to determine if Cabrillo is executing in ServiceNow's native mobile apps.
    c.isNative = cabrillo.isNative();
}
```

Cabrillo JS APIs are only supported when executing in ServiceNow native mobile applications. Use the cabrillo.isNative\(\) API to determine if the script is executing in a native context.

**Note:** Cabrillo JS APIs are unavailable in GlideForm client scripts.

**Parent Topic:**[Client mobile API reference](../../../../../build/applications/concept/api-client-mobile.md)

## cabrillo - isNative\(\)

Boolean value indicating if Cabrillo JS is executing a ServiceNow native mobile application.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns true if Cabrillo JS is running in a native context; otherwise, false.|

```
var isNative = cabrillo.isNative();
```

