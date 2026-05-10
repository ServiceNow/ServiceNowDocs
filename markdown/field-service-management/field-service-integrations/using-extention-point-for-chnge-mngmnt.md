---
title: Using an extension point to synchronize work orders with change requests
description: Extension points enable you to extend the functionality of an application and integrate customizations without altering the application code. Extension points are stored in the Extension Point \[sys\_extension\_point\] table.
locale: en-US
release: australia
product: Field Service Integrations
classification: field-service-integrations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up Change Management, Integration with Change Management, Integrating Field Service Management with other applications, Configure, Field Service Management]
---

# Using an extension point to synchronize work orders with change requests

Extension points enable you to extend the functionality of an application and integrate customizations without altering the application code. Extension points are stored in the Extension Point \[sys\_extension\_point\] table.

The Change Management for Field Service plugin \(sn\_fsm\_chg\_mng\) adds the ChangeWorkOrderIntegration extension point, which creates a logic to enable the synchronization of following configurations:

-   Mapping work notes from the work order to the **Activity** section on the change request.
-   Auto-closing the change request when the related work order is closed complete.

The default extension points that are provided with an application cannot be modified or deactivated. If modification is necessary, if you have the system administrator role, you can do the following:

-   Create an implementation of an extension point.
-   Make any necessary changes in the implementation.
-   Update the order of the implementation to a lower number. The system executes the implementation with the lowest order number.

    **Note:** API names used in the implementation must remain the same so the extension point can identify the implementation. Otherwise, an error will result.


**Related topics**  


[Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md)

