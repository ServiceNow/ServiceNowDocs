---
title: Create a filter on a technical dashboard in UI Builder
description: To filter data visualizations and simple lists in a technical dashboard, add a filter component in UI Builder and configure event handlers.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-10-02"
reading_time_minutes: 2
breadcrumb: [Filters, Platform Analytics]
---

# Create a filter on a technical dashboard in UI Builder

To filter data visualizations and simple lists in a technical dashboard, add a filter component in UI Builder and configure event handlers.

## Before you begin

Role required: ui\_builder\_admin, admin

## Procedure

1.  Locate the dashboard in the dashboard library and open it for editing, as described in [Edit Platform Analytics dashboards](../../dashboards/task/edit-db-in-ac.md).

    If the dashboard is a technical dashboard, you see an **Edit in UI Builder** button. If it is in the inline editor, you see an **Edit** button. In the latter case, go to [Create or add a filter on an inline dashboard](select-workspace-filter-type.md).

2.  If you are in a different application scope than the dashboard, use the application picker to select the correct scope.

    ![Application scope picker](../image/app-scope-picker.png)

3.  Select **Edit in UI Builder**.

4.  Add layout elements and a filter component as described in [Add and configure components](https://www.servicenow.com/docs/access?context=add-components&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

5.  Configure the filter as described in the [Filter component reference](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/now-components/sn-component-filter/overview) on the Developer Site.

    This reference includes a description of each configuration field and general usage information that applies to UI Builder pages in general.

    **Important:** Be certain to configure the event handlers and page scripts to link the filter to the relevant data visualizations or lists.


**Parent Topic:**[Filters in Platform Analytics](../concept/interactive-filters-workspace.md)

**Related topics**  


[Create or add a filter on an inline dashboard](select-workspace-filter-type.md)

[Create a filter in the Filter Designer](add-filter-library.md)

[Make a data visualization act as a filter](make-dv-act-as-filter.md)

[Configure a Single/Multiple select or cascading filter](create-select-filter-workspace.md)

[Configure a True/False filter](create-boolean-filter-workspace.md)

[Configure a Date filter in the inline editor](create-date-filter-workspace.md)

[Create a domain filter](create-domain-filter.md#)

[Edit a Platform Analytics filter on a dashboard](edit-filters-configurable-workspaces.md)

[Troubleshoot breakdown filters](troubleshoot-breakdown-filters.md)

