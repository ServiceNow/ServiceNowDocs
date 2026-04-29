---
title: Custom interactive filter limitations
description: Custom interactive filters are a fallback for use when standard interactive filters do not provide certain functionality.
locale: en-US
release: australia
product: Interactive Filters
classification: interactive-filters
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Custom interactive filters, Interactive Filters, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Custom interactive filter limitations

Custom interactive filters are a fallback for use when standard interactive filters do not provide certain functionality.

**Note:** The exposed [DashboardMessageHandler](../../../app-store/dev_portal/API_reference/DashboardMessageHandler/concept/c_DashboardMessageHandler.md#) API for custom interactive filters is limited and does not provide parity with standard interactive filters. The API does not support these features.

## Unsupported custom interactive filter features

-   **Setting default filter values**

    Creators of custom interactive filters are not able to select default filter values.

-   **Retaining filter value on refreshing the widget**

    When you click a widget's refresh icon \(![](../image/icon-refresh2.png)\) to refresh its content, or when you select **Refresh** from the context menu \(![](../image/context-menu.png)\), the custom interactive filter value does not persist.

-   **Resetting custom filter values / All filter values**

    When you select **Reset Filters** from the context menu \(![](../image/context-menu.png)\), the custom interactive filter does not change and is still applied.

-   **Setting filter values on page load or tab switch**

    Custom interactive filter values do not persist when the user switches tabs, or opens a new dashboard and returns to the first dashboard or dashboard tab.

-   **Adding multiple instances of the same custom interactive filter on a tab**

    If there is more than one instance of the same custom interactive filter on a tab, unexpected behavior can result.

    **Note:** Custom interactive filter values do not persist across tabs. To filter values on multiple tabs on the same dashboard, you must add the custom interactive filter to each tab.

-   **Unsubscribing reports on removal of custom interactive filter**

    Reports following a custom interactive filter on a dashboard continue to follow that filter even when the filter is deleted from the dashboard.

-   **Filtering widgets in Export to PDF**

    When you create custom content to be placed as widgets on dashboards and home pages, you must perform extra tests before you export the content to PDF. In the exported PDF, report widgets that are filtered using custom interactive filters may appear as blank squares or the widget content does not respect the filter.

-   **Custom interactive filters cannot be used in a breakdown dashboard**

    On breakdown dashboards, the breakdown itself is used to filter all Performance Analytics widget data. For more information, see [Using breakdowns on dashboards](../../performance-analytics/concept/c_SpecialDashboards.md).


**Parent Topic:**[Custom interactive filters](../concept/c_CustomPublishers.md)

