---
title: Using extension point for planned work management
description: Extension points enable you to extend the functionality of an application and integrate customizations without altering the application code. Extension points are stored in the Extension Point \[sys\_extension\_point\] table.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Planned Work Management, Set up work orders and tasks, Configure, Field Service Management]
---

# Using extension point for planned work management

Extension points enable you to extend the functionality of an application and integrate customizations without altering the application code. Extension points are stored in the Extension Point \[sys\_extension\_point\] table.

The Planned Work Management plugin \(com.snc.fsm\_planned\_work\_management\) adds the global.PlannedMaintenanceExtensionPoint extension point, which creates a logic to create work orders for the planned work schedule using the enhanced capabilities of Planned work management. For more information on the other extension points for Planned Work Management, see [Extension points in Field Service Management](extension-points-field-service.md).

The default extension points that are provided with an application cannot be modified or deactivated. If modification is necessary, if you have the administrator role, you can do the following:

-   Create an implementation of an extension point.
-   Make any necessary changes in the implementation.
-   Update the order of the implementation to a lower number. The system executes the implementation with the lowest order number.

    **Note:** API names used in the implementation must remain the same so the extension point can identify the implementation. Otherwise, an error results.


**Related topics**  


[bundle-crapiref.extension-points]

