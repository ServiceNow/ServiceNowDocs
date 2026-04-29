---
title: Enable filters to apply to a local data instance
description: To enable a viewer to switch between which field values or breakdown elements they see in a data visualization, add filter components to the UI Builder page. For those filters to apply to a local data instance, configure that instance accordingly.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use a local data instance, Technical dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Enable filters to apply to a local data instance

To enable a viewer to switch between which field values or breakdown elements they see in a data visualization, add filter components to the UI Builder page. For those filters to apply to a local data instance, configure that instance accordingly.

## Before you begin

Role required: ui\_builder\_admin, admin

## About this task

To enable filters to apply to a local data source, you first have to create a client state parameter named `parFilters` and then add that state parameter to the local data instance.

## Procedure

1.  Open the UI Builder page with the local data instance and data visualizations you want to filter.

2.  In the Data and scripts drawer, select **Client state parameters**.

3.  Select **+ Add**.

4.  In the Edit client state parameters dialog, name the new parameter `parFilters`, assign it type JSON, and set the initial value of `{}`.

    ![parFilters client state parameter in the Edit client state parameters dialog.](../../par-for-workspace/image/parFilters-param.png)

5.  Close the Edit client state parameters dialog.

6.  In the Data and scripts drawer, under Data resources, select the desired local data instance.

7.  In the Edit &lt;name of local data instance&gt; dialog, scroll down to the **Filter configurations** field.

8.  Enter `@state.parFilters` into the **Filter configurations** field and close the data instance editor.

9.  In the configuration panel of a data visualization that uses this local data resource, turn on **Follow filters** in the Data update section.

10. Turn on **Show filter icon**.

11. Save the UI Builder page.


## What to do next

Add filter components to the UI Builder page and configure them for relevant values from the local data instance.

**Parent Topic:**[Use a local data instance with a data visualization](dv-local-data-instance.md)

**Related topics**  


[Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md)

