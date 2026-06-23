---
title: Create a dashboard with the in-line editor
description: In the Platform Analytics experience, you can create shareable dashboards with data visualizations, filters, and other elements. You can create elements and add existing elements from the inline editor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/now-intelligence/create-db-in-ac.html
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Dashboards in Platform Analytics, Platform Analytics experience, Platform Analytics]
---

# Create a dashboard with the in-line editor

In the Platform Analytics experience, you can create shareable dashboards with data visualizations, filters, and other elements. You can create elements and add existing elements from the inline editor.

## Before you begin

Save your work regularly.

Role required: Any user with an internal role can create dashboards with the inline editor.

**Note:** Data visualizations based on table data are automatically shared with users that you share a dashboard with.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Dashboards**.

2.  Select **Create new dashboard**.

3.  Select the **inline editor** tile and give the dashboard a name and a description.

    If you want to use scripting, data binding, and other advanced capabilities, select the **Technical editor** tile to continue in UI Builder. This editor is available only to users who can access UI Builder \(ui\_builder\_admin role\). If you do not have this role, go to step 6. For more information about the technical editor, see [Technical dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/now-intelligence/technical-dashboards.md).

4.  Select **Create new dashboard**.

    \[Omitted image "create-new-inline-ed-db-modal.png"\] Alt text: Create new inline dashboard modal

5.  Choose **inline editor**.

    The Technical editor option opens a page in UI Builder that is treated as a dashboard, with a list of available components. Creating dashboards in UI Builder is recommended for developers. For more information, see [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/application-development/ui-builder/ui-builder-overview.md)and [Create a technical dashboard in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/now-intelligence/create-tech-db-in-ac.md).

6.  Give the dashboard a meaningful name and description.

7.  Select **Add new element** to add content to the dashboard.

    See [Platform Analytics dashboard overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/now-intelligence/ac-elements.md) for information about what you can add to a dashboard.

    When you add a data visualization, select **New data visualization** to create a visualization from scratch or **Saved data visualization** to choose one from the library. When you add a filter, select **New filter** to create the filter without preconfigured data or **Saved filter** to reuse an existing filter.

    \[Omitted image "add-dv-modal.png"\] Alt text: Add data visualization dialogue box with options to add a New data visualization or a Saved data visualization

8.  Select the information icon \(\[Omitted image "icon-info.png"\] Alt text: information icon\) to open the Details panel and provide a name and description for your dashboard.

9.  Arrange the data on the canvas to make it useful.

    You can click and drag from the corners of the elements to resize them on the canvas.

10. Select **Add a tab** to create room for more information on additional tabs.

11. Select **Save** early and often.

    The dashboard inline editor doesn’t automatically save your dashboard when you’re creating it. Be sure to save your work regularly.


## What to do next

-   [Configure Platform Analytics dashboard details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/now-intelligence/config-db-in-ac.md)
-   [Edit Platform Analytics dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/now-intelligence/edit-db-in-ac.md)

