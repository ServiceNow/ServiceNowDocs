---
title: Using scripted extension points in server-side scripts
description: Use the scripted extension points in the server-side script includes that store JavaScript functions and object classes. By using extension points, you can integrate customizations without actually altering the core components in the application code.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using extension points, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Using scripted extension points in server-side scripts

Use the scripted extension points in the server-side script includes that store JavaScript functions and object classes. By using extension points, you can integrate customizations without actually altering the core components in the application code.

You create the scripted extension points and add them to the script includes in the base application code. When customizing a base application, you implement the scripted extension points by creating the custom script includes and registering them against the scripted extension points.

**Note:** For an example of a scripted extension point and to learn more about this process, see [Using extension points to extend application functionality](extension-points.md).

-   **[Creating and adding a scripted extension point](impl-scripted-ext-pts-base-code.md)**  
When developing an application, create scripted extension points and add them to the script includes in the application code. Use a scripted extension point to designate the specific location where data or objects can be sent to a registered custom script include and where returned results are processed.

**Parent Topic:**[Using extension points to extend application functionality](extension-points.md)

