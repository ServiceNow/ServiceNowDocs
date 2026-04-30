---
title: Configuring Entity View Action Mapper
description: The Entity View Action Mapper \(EVAM\) enables you to map specific actions to entity views, enabling customized behavior and streamlined workflows. Learn how to configure EVAM so you can define, configure, and apply mappings to enhance user interactions with data in the platform.
locale: en-US
release: zurich
product: Entity View Action Mapper \(EVAM\)
classification: entity-view-action-mapper-evam
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [EVAM, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Configuring Entity View Action Mapper

The Entity View Action Mapper \(EVAM\) enables you to map specific actions to entity views, enabling customized behavior and streamlined workflows. Learn how to configure EVAM so you can define, configure, and apply mappings to enhance user interactions with data in the platform.

## Configuration overview

To get started with EVAM, you need the following plugins for UI Builder:

-   sn\_ui\_builder
-   sn\_ui\_builder\_icons
-   sn\_ui\_builder\_properties\_pane

EVAM also relies on:

-   Now Design System \(NDS\) components
-   @devsnc/sn-layout \(com.devsnc\_sn\_layout\): Layout

-   -   -   
-   **[Define a data source](../task/define-evam-datasource.md)**  
The data source is an entity that has associated data that you intend to display. For example, a community post or a user.
-   **[Define an EVAM view template](../task/define-evam-template.md)**  
You can configure multiple view templates per data source based on conditions to customize how data displays for users. The view template maps fields from the view configuration to component.
-   **[Define an EVAM configuration bundle](../task/define-view-configuration-bundle.md)**  
Create a view configuration to combine conditions, database fields, and declarative actions with an associated view template using the Entity View Action Mapper \(EVAM\).

**Parent Topic:**[Manage instance data sources](../../general/concept/manage-data-sources.md)

