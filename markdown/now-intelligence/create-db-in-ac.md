---
title: Create a dashboard with the in-line editor
description: In the Platform Analytics experience, you can create shareable dashboards with data visualizations, filters, and other elements. You can create elements and add existing elements from the inline editor.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create, share, edit, and more, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Create a dashboard with the in-line editor

In the Platform Analytics experience, you can create shareable dashboards with data visualizations, filters, and other elements. You can create elements and add existing elements from the inline editor.

## Before you begin

Save your work regularly.

Role required: Any user with an internal role can create dashboards with the inline editor.

**Note:** Data visualizations based on table data are automatically shared with users that you share a dashboard with.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Select **Create new dashboard**.

3.  Select the **inline editor** tile and give the dashboard a name and a description.

    If you want to use scripting, data binding, and other advanced capabilities, select the **Technical editor** tile to continue in UI Builder. This editor is available only to users who can access UI Builder \(ui\_builder\_admin role\). If you do not have this role, go to step 6. For more information about the technical editor, see [Technical dashboards](../../performance-analytics/concept/technical-dashboards.md).

4.  Select **Create new dashboard**.

    ![Create new inline dashboard modal](../image/create-new-inline-ed-db-modal.png)

5.  Choose **inline editor**.

    The Technical editor option opens a page in UI Builder that is treated as a dashboard, with a list of available components. Creating dashboards in UI Builder is recommended for developers. For more information, see [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)and [Create a technical dashboard in UI Builder](create-tech-db-in-ac.md).

6.  Give the dashboard a meaningful name and description.

7.  Select **Add new element** to add content to the dashboard.

    See [Exploring Platform Analytics dashboards](../reference/ac-elements.md) for information about what you can add to a dashboard.

    When you add a data visualization, select **New data visualization** to create a visualization from scratch or **Saved data visualization** to choose one from the library. When you add a filter, select **New filter** to create the filter without preconfigured data or **Saved filter** to reuse an existing filter.

    ![Add data visualization dialogue box with options to add a New data visualization or a Saved data visualization](../../par-for-workspace/image/add-dv-modal.png)

8.  Select the information icon \(![information icon](../../reporting/image/icon-info.png)\) to open the Details panel and provide a name and description for your dashboard.

9.  Arrange the data on the canvas to make it useful.

    You can click and drag from the corners of the elements to resize them on the canvas.

10. Select **Add a tab** to create room for more information on additional tabs.

11. Select **Save** early and often.

    The dashboard inline editor doesn’t automatically save your dashboard when you’re creating it. Be sure to save your work regularly.


## What to do next

-   [Edit Platform Analytics dashboard elements](edit-db-elements-in-ac.md)
-   [Configure Platform Analytics dashboard details](config-db-in-ac.md)

**Parent Topic:**[Creating dashboards and other common dashboard tasks](../concept/common-dashboard-tasks.md)

**Related topics**  


[Edit Platform Analytics dashboards](edit-db-in-ac.md)

[Share a Platform Analytics dashboard](share-db-in-ac.md)

[Duplicate a Platform Analytics dashboard](../../reporting/task/duplicate-db.md#)

[Print a Platform Analytics dashboard](printer-friendly-db-ac.md)

[Export a Platform Analytics dashboard](export-pae-dashboard-ppt.md)

[Schedule the export of dashboards and data visualizations](../../par-for-workspace/task/schedule-export-dboards-data-viz.md)

[Bookmark a Platform Analytics dashboard](bookmark-dashboard-ac.md)

[Delete a Platform Analytics dashboard](delete-db-in-ac.md)

