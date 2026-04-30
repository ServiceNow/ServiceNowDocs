---
title: Using extension point for incident management
description: Extension points enable you to extend the functionality of an application and integrate customizations without altering the application code. Extension points are stored in the Extension Point \[sys\_extension\_point\] table.
locale: en-US
release: yokohama
product: Field Service Integrations
classification: field-service-integrations
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Incident Management for Field Service, Integration with Incident Management, Integrating Field Service Management with other applications, Configuring Field Service Management, Field Service Management]
---

# Using extension point for incident management

Extension points enable you to extend the functionality of an application and integrate customizations without altering the application code. Extension points are stored in the Extension Point \[sys\_extension\_point\] table.

The Incident Management for Field Service plugin \(sn\_fsm\_inc\_mng\) adds theIncidentWorkOrderIntegration extension point, which creates a logic to enable the synchronization of following configurations:

-   Mapping work notes from the work order to the **Activity** section on the incident record.
-   Auto-closing the incident record when the related work order is closed complete.

The default extension points that are provided with an application cannot be modified or deactivated. If modification is necessary, if you have the system administrator role, you can do the following:

-   Create an implementation of an extension point.
-   Make the necessary changes in the implementation.
-   Update the order of the implementation to a lower number. The system executes the implementation with the lowest order number.

    **Note:** API names used in the implementation must remain the same so the extension point can identify the implementation. Otherwise, an error will result.


**Parent Topic:**[Setting up Incident Management for Field Service](../concept/setting-up-incident-fsm.md)

