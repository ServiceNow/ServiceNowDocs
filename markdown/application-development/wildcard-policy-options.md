---
title: Wildcard Policies options
description: When using a segment policy to enable broad access permissions by category, wildcard options for each category further specify which kinds of access are permitted.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/wildcard-policy-options.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Reference, Application Runtime Policy \(ARP\), Developing your application, Building applications]
---

# Wildcard Policies options

When using a segment policy to enable broad access permissions by category, wildcard options for each category further specify which kinds of access are permitted.

Segment policies can be configured with the following wildcard options.

## Network wildcards

-   **Client Cross-origin Request**

    Enables client-side requests to an external host, such as a fetch or XHR call made from a UI page script.

-   **Client Cross-origin Scripts**

    Enables client-side requests to load an external script resource.

-   **Inbound Cross Scope Request**

    Enables access to API resources in different application scopes.

-   **Inbound Global Request**

    Enables runtime access to ServiceNow global APIs.

-   **Server Outbound Request**

    Enables outbound call to an external host, such as a call made from a script include.


## Scripting wildcards

-   **Script Includes**

    Enables unrestricted calls to script includes defined in other application scopes. For more information about script includes, see [Script includes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/c_ScriptIncludes.md).

-   **Scriptable**

    Enables unrestricted access to ServiceNow provided server-side JavaScript APIs, such as GlideRecord.


## ARL \(application resource limits\) wildcards

-   **Scheduled Job Limit**

    Sets the number of scheduled jobs the application can create to the maximum allowed value \(100%\).

-   **Event Handler Limit**

    Sets the number of event handlers the application can trigger to the maximum allowed value.

-   **API Transaction Limit**

    Sets the number of API transactions the application can make to the maximum allowed value.

-   **Interactive Transaction Limit**

    Sets the number of transactions triggered by UI elements to the maximum allowed value.


**Parent Topic:**[Application Runtime Policy reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/application-runtime-policy-reference.md)

