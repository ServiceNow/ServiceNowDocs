---
title: Using UI extension points in server-side UI macros
description: Use UI extension points in the server-side UI macros, such as HTML extensions, to add custom content to a UI page without having to directly modify the page. By using UI extension points, you can integrate customizations without actually altering the core components in the application code.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using extension points to extend application functionality, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Using UI extension points in server-side UI macros

Use UI extension points in the server-side UI macros, such as HTML extensions, to add custom content to a UI page without having to directly modify the page. By using UI extension points, you can integrate customizations without actually altering the core components in the application code.

You create the UI extension points and add them to the UI macros in the base application code. When customizing a base application, implement the UI extension points by creating the custom UI macros and registering them against the UI extension points.

**Note:** You create and register the UI extension points in a manner that is similar to how you implement the scripted extension points. For a detailed example of a scripted extension point, and to learn more about this process, see [Using extension points to extend application functionality](extension-points.md).

-   **[Creating and adding a UI extension point](impl-ui-ext-pts-base-code.md#)**  
When developing an application, create UI extension points and add them to the server-side UI macros, such as HTML extensions, or the UI pages in the base application code.
-   **[Registering custom UI macros against the UI extension points](implementing-ui-ext-pts-custom-code.md#)**  
Register custom UI macros against a selected UI extension point in the application code.

**Parent Topic:**[Using extension points to extend application functionality](extension-points.md)

