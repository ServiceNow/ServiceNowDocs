---
title: Next Experience client-side scripting global variables
description: Next Experience global variables are used in client scripts to determine whether Next Experience is applied to a page.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Next Experience client-side scripting global variables

Next Experience global variables are used in client scripts to determine whether Next Experience is applied to a page.

-   **NOW.isUsingPolaris**

    Returns **true** if Next Experience is applied to the current page.

-   **NOW.isPolarisWrapper**

    Returns **true** if the page is running in the Next Experience Unified Navigation. This global variable exists only in the Unified Navigation.

    For more information about the Unified Navigation, see [Using the Next Experience Unified Navigation](../../../get-started/servicenow-overview/concept/using-the-next-experience-global-header.md).


Client script:

```
// Reload the current page in the unified navigator if not currently in the unified nav
if (NOW.isUsingPolaris && (!top.NOW || top.NOW.isPolarisWrapper !== "true")) {
    var currentPath = window.location.pathname + window.location.search;
    top.window.location.href = "/now/nav/ui/classic/params/target/" + encodeURIComponent(currentPath)
}

```

**Parent Topic:**[Configuring the Next Experience UI](../concept/next-experience-ui-admin.md)

**Related topics**  


[PolarisUI API - Scoped](https://www.servicenow.com/docs/access?context=PolarisUIScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

