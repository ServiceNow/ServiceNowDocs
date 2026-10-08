---
title: Create a dashboard with the in-line editor
description: In the Platform Analytics experience, you can create shareable dashboards with data visualizations, filters, and other elements. You can create elements and add existing elements from the inline editor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/create-db-in-ac.html
release: brazil
topic_type: task
last_updated: "2026-09-25"
reading_time_minutes: 4
breadcrumb: [Working with in-line dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Create a dashboard with the in-line editor

In the Platform Analytics experience, you can create shareable dashboards with data visualizations, filters, and other elements. You can create elements and add existing elements from the inline editor.

## Before you begin

The dashboard inline editor doesn’t automatically save your dashboard when you’re creating it. Be sure to save your work regularly.

Role required: Any user with an internal role can create dashboards with the inline editor.

**Note:** Data visualizations based on table data are automatically shared with users that you share a dashboard with.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Select **Create dashboard**.

3.  Select the **In-line editor** tile and give the dashboard a name and a description.

    If you want to use scripting, data binding, and other advanced capabilities, select the **Technical editor** tile to continue in UI Builder. This editor is available only to users who can access UI Builder \(ui\_builder\_admin role\). If you don't have this role, go to step 6. For more information about the technical editor, see [Technical dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/technical-dashboards.md).

    \[Omitted image "create-new-inline-ed-db-modal.png"\] Alt text: Create inline dashboard modal

4.  Select **Create dashboard**.

    On migrated instances, you have the choice to create the dashboard in Next Experience or in Core UI if you require legacy features. See [Create or configure a responsive dashboard in Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/t_CreateADashboard.md).

    \[Omitted image "create-core-ui-db-from-library.png"\] Alt text: Create Core UI dashboard on migrated instance

5.  In the Dashboard Designer, select **Add new element** to add content to the dashboard.

    See [Dashboard elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/dashboard-elements.md) for information about what you can add to a dashboard.

    When you add a data visualization, select **New visualization** to create a visualization from scratch or **Saved visualization** to choose one or more from the library. When you add a filter, select **New filter** to create the filter without preconfigured data or **Saved filter** to reuse an existing filter. For more information, see [Filters in Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/interactive-filters-workspace.md).

    \[Omitted image "add-dv-modal.png"\] Alt text: Add data visualization dialogue box with options to add a New visualization or a Saved visualization

6.  Select the information icon \[Omitted image "icon-info.png"\] Alt text: information icon to open the Details panel and edit the name and description of your dashboard.

    You can also edit the dashboard's certification, visibility, and category. For more information, see [Configure Platform Analytics dashboard details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/config-db-in-ac.md).

7.  Arrange the elements on the canvas so that it tells the story you want to tell with your data.

    You can also click and drag from the corners of the elements to resize them on the canvas.

8.  Select **Add a tab** to create room for more information on additional tabs.

9.  Select **Save**


## What to do next

-   [Edit in-line Platform Analytics dashboard elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/edit-db-elements-in-ac.md)
-   [Configure Platform Analytics dashboard details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/config-db-in-ac.md)

**Parent Topic:**[Common dashboard tasks in the in-line editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/common-dashboard-tasks.md)

**Related topics**  


[Create Core UI dashboards on upgraded instances]()

[Edit Platform Analytics dashboards]()

[Share a Platform Analytics dashboard]()

[Duplicate a Platform Analytics dashboard]()

[Print a Platform Analytics dashboard]()

[Export a Platform Analytics dashboard]()

[Schedule the export of dashboards and data visualizations]()

[Bookmark a Platform Analytics dashboard]()

[Delete a Platform Analytics dashboard]()

