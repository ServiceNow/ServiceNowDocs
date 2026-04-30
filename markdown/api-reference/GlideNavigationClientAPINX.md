---
title: GlideNavigation \(Next Experience\) - Client
description: The GlideNavigation API enables refreshing the navigator and main frame in the Next Experience UI Framework.Refreshes the navigator contents.
locale: en-US
release: zurich
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Client Next Experience API reference, API reference, API implementation and reference]
---

# GlideNavigation \(Next Experience\) - Client

The GlideNavigation API enables refreshing the navigator and main frame in the Next Experience UI Framework.

Methods for this API are called within the nowapi namespace using the g\_navigation system variable.

**Parent Topic:**[Client Next Experience API reference](../../../../../build/applications/concept/api-client-next.md)

## GlideNavigation \[Next Experience\] - refreshNavigator\(\)

Refreshes the navigator contents.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to trigger a menu transaction similar to Core UI.

```
// onChange() client script settings:
// Table: Incident
// UI Type: All
// Type: onChange
// Field Name: Short description
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
   if (isLoading || newValue === '') {
      return;
   }

   nowapi.g_navigation.refreshNavigator();
}
```

