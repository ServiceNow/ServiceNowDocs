---
title: Using client extension points in client-side UI scripting
description: Use client extension points in client-side UI scripting to modify forms, so that you do not have to directly modify the form. By using client extension points, you can integrate customizations without actually altering the core components in the application code.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/client-extension-points.html
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using extension points to extend application functionality, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Using client extension points in client-side UI scripting

Use client extension points in client-side UI scripting to modify forms, so that you do not have to directly modify the form. By using client extension points, you can integrate customizations without actually altering the core components in the application code.

You create client extension points and add them to the UI scripts in the base application code. When customizing a base application, implement the client extension points by creating the custom UI scripts and registering them against the client extension points.

**Note:** You create and register the client extension points in a manner that is similar to how you implement the scripted and UI extension points. For a detailed example of a scripted extension point, and to learn more about this process, see [Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md) and [Using UI extension points in server-side UI macros](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/ui-extension-points.md).

-   **[Creating and adding a client extension point](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/impl-client-ext-pts-base-code.md)**  
Create client extension points and add them to the client-side UI scripts in the base application code.

**Parent Topic:**[Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md)

