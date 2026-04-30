---
title: Custom interactive filters
description: As an administrator, you can create scripted interactive filter widgets to provide advanced filtering options on dashboard reports.
locale: en-US
release: xanadu
product: Interactive Filters
classification: interactive-filters
topic_type: concept
last_updated: "2024-10-22"
reading_time_minutes: 2
breadcrumb: [Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Custom interactive filters

As an administrator, you can create scripted interactive filter widgets to provide advanced filtering options on dashboard reports.

With a custom interactive filter, you can control aspects of the filter interface and filtering logic. Create filters that fit your specific needs. Custom interactive filters include filters that perform multiple, common filtering operations with a single click.

Custom filters are scripted **System UI** **Widgets** that use the DashboardMessageHandler JavaScript class to define and publish report filters.

Role required: hp\_publisher\_admin and report\_admin. The hp\_publisher\_admin role exists only for managing interactive filters in Core UI. By default, it contains the role analytics\_filter\_admin for managing Core UI filters that are migrated to Platform Analytics experience.

**Note:** The exposed API for custom interactive filters is limited and does not provide parity with standard interactive filters. Before implementing any custom interactive filters, review the [Custom interactive filter limitations](../reference/custom-if-limitations.md).

Access control lists on the Table API may restrict the records shown when a dashboard is filtered. To alleviate this problem, add users or roles to the Table API access control list. For more information, see [Access control list rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

The code that publishes the filter must call the SNC.canvas.interactiveFilters.setDefaultValue\(\) method and it must call the dashboardMessageHandler.publishFilter\(\) method to publish the filter.

Define the appearance of the widget, such as available buttons, using Jelly.

You can add multiple custom interactive filters to the same dashboard. The filters must have unique IDs in the filter object and unique IDs for the [DashboardMessageHandler](../../../app-store/dev_portal/API_reference/DashboardMessageHandler/concept/c_DashboardMessageHandler.md#).

-   **[Custom interactive filter examples](../reference/r_CustomPublisherExample.md#)**  
As an administrator, you can create custom interactive filter widgets to provide advanced filtering options on dashboards.
-   **[Use the Debug filter](c_DebugPublisher.md)**  
The debug interactive filter helps you create custom filters. This filter displays a JSON array representation of all active filters on a dashboard.
-   **[Custom interactive filter limitations](../reference/custom-if-limitations.md)**  
Custom interactive filters are a fallback for use when standard interactive filters do not provide certain functionality.
-   **[DashboardMessageHandler](../../../app-store/dev_portal/API_reference/DashboardMessageHandler/concept/c_DashboardMessageHandler.md#)**  
Provides methods to define custom filtering logic for interactive filters.
-   **[Dynamic JavaScript filters](dynamic-js-filters.md#)**  
Create dynamic conditions in JavaScript that you can configure as part of a report visualization's criteria instead of specified values.

**Parent Topic:**[Interactive Filters](c_HomepagePublishers.md)

