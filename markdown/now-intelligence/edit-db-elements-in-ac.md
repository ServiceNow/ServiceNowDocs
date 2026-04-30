---
title: Edit Platform Analytics dashboard elements
description: You can edit the contents of a dashboard or dashboard tab, including data visualizations and filters. Because dashboards are shared, any changes you make are applied globally.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
keywords: [Performance Analytics widgets, add Performance Analytics widgets, reports, add reports to dashboard]
breadcrumb: [Edit a dashboard, Create, share, edit, and more, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Edit Platform Analytics dashboard elements

You can edit the contents of a dashboard or dashboard tab, including data visualizations and filters. Because dashboards are shared, any changes you make are applied globally.

## Before you begin

You can edit the details of dashboards created in the inline editor and in the technical editor in the configurable workspace. When you edit the content of dashboards created in the technical editor, you’re redirected to UI Builder.

Role required: dashboard\_admin for all dashboards, or any role for dashboards that you own or ones that you have been given the right to edit. See [Platform Analytics dashboard roles](../../par-for-workspace/concept/pa-dashboard-roles.md) for more information about viewing and editing rights on dashboards.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Select the **Dashboard** tab and select the dashboard you want to edit.

    If you are in a different application scope than the dashboard, use the application picker to select the correct scope.

    ![Application scope picker](../../par-for-workspace/image/app-scope-picker.png)

3.  Perform any of the following actions on the element.

<table id="choicetable_gv3_q3r_g5"><thead><tr><th align="left" id="d79299e134">

Action

</th><th align="left" id="d79299e137">

Steps

</th></tr></thead><tbody><tr><td id="d79299e143">

**Add an element**

</td><td>

1.  Select the **Edit** button \(![Edit button](../image/edit-button.png)\) to put the dashboard into edit mode.

**Note:** If you don’t see the **Edit** button, you don’t have rights to edit the dashboard.

2.  Select **Add new element**. From the list, select the component you want to add. Select **Saved data visualization** or **Saved filter** to add one or more saved elements from the library to the dashboard.

You can also select the **Add new element** button on any selected dashboard element to see the list of elements.

![Filter element with four Add new element icons highlighted](../image/add-new-element-handles.png)

3.  Select the element. The element is added to the dashboard where you can edit it.
4.  Drag to move the widget or resize it.


</td></tr><tr><td id="d79299e203">

**Save a data visualization to the Visualization Library**

</td><td>

Role required: admin or viz\_creator1.  Select the **Edit** button \(![Edit button](../image/edit-button.png)\) to put the dashboard into edit mode.

**Note:** If you don’t see the **Edit** button, you don’t have rights to edit the dashboard.

2.  Select **Add new element**. From the list, select **Data visualization**.
3.  Create the visualization as described in [Data visualizations in Platform Analytics](../../performance-analytics/concept/analytics-center-data-visualizations.md).
4.  Select the More actions menu icon \(![More actions icon](../image/context-menu-db-element-ac.png)\) in the header and choose **Add to library**.

![Dashboard element More actions menu with Add to library option highlighted](../image/context-menu-add-dv-library.png)

5.  Give the visualization a name and a description.
6.  Select **Add to library**.
The data visualization is available in the Visualization library for use on other dashboards.

</td></tr><tr><td id="d79299e287">

**Delete an element from the dashboard**

</td><td>

1.  Select the **Edit** button \(![Edit button](../image/edit-button.png)\) to put the dashboard into edit mode.

**Note:** If you don’t see the **Edit** button, you don’t have rights to edit the dashboard.

2.  Select the element that you want to delete.
3.  In the header, select the More actions menu icon \(![More actions icon](../image/context-menu-db-element-ac.png)\) and choose **Delete**.

![Dashboard element More actions menu with Delete option highlighted](../image/delete-db-element-ac-2.png)

 **Note:** There’s no confirmation message. The widget disappears from the dashboard.

</td></tr><tr><td id="d79299e339">

**Configure an element**

</td><td>

1.  Select the **Edit** button \(![Edit button](../image/edit-button.png)\) to put the dashboard into edit mode.

**Note:** If you don’t see the **Edit** button, you don’t have rights to edit the dashboard.

2.  Select the element that you want to edit.
3.  In the element's header, select the Settings icon \(![Settings icon](../image/icon-config-ac.png)\) to open the Configuration panel.
4.  Configure the element and choose **Save**. For more information about configuring an element, see one of the following:
    -   [Edit a data visualization in an inline dashboard](editing-dv-in-line-db.md)
    -   [Edit a Platform Analytics filter on a dashboard](../../par-for-workspace/task/edit-filters-configurable-workspaces.md)
    -   [Heading component reference](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/now-components/now-heading/uib-config)
    -   [Image component reference](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/now-components/now-image/uib-setup)
    -   [Simple List component reference](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/shared-components/now-record-list-connected-snapshot/uib-setup)
 **Note:** There are role and ownership requirements for editing a component in a library, such as the Visualization or Filter library. If you change a visualization from the Visualization Library and you have the viz\_creator or admin role, you have the choice to save the change only to the dashboard or to the element in the library. When you change an element in the library, the change is reflected everywhere the element is used. When you change only in the dashboard, you create a new copy of the visualization that exists only in that dashboard.

</td></tr><tr><td id="d79299e429">

**Move an element between tabs**

</td><td>

When you have multiple tabs, you can move elements from tab to another or to the pane above the tabs.1.  Select the **Edit** button \(![Edit button](../image/edit-button.png)\) to put the dashboard into edit mode.

**Note:** If you don’t see the **Edit** button, you don’t have rights to edit the dashboard.

2.  Select the More actions menu icon \(![More actions menu icon](../image/context-menu-db-element-ac.png)\) next to the element's name and choose **Move to a different tab** or **Move above the tabs**.
3.  When you choose **Move to a different tab**, choose the tab and select **Move**.


</td></tr><tr><td id="d79299e481">

**Add filters to the dashboard**

</td><td>

Role required: analytics\_filter\_admin.Filters let users filter data for all report widgets on a dashboard that follow them. You can add filters to both the entire dashboard and to individual dashboard tabs.

For more information, see [Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md).

</td></tr><tr><td id="d79299e502">

**Configure a data visualization to follow or not follow filters**

</td><td>

Data visualizations follow filters by default. A data visualization follows filters in the same tab as itself or above the tabs. Data visualizations either follow all such tabs that target their data sources, or none.1.  Select the **Edit** button \(![Edit button](../image/edit-button.png)\) to put the dashboard into edit mode.

**Note:** If you don’t see the **Edit** button, you don’t have rights to edit the dashboard.

2.  Select the dashboard element that you want to follow or not follow filters.
3.  In the header, select the Settings icon \(![Settings icon](../image/icon-config-ac.png)\) to open the Configuration panel.
4.  In the Data update section, select or deselect **Follow filters**.
5.  To show a filter icon \(![Filter icon](../image/InteractiveFilterFilteringIcon.png)\) on the data visualization when it follows an interactive filter, select the **Show filter icon**.
![Element configuration- Data update section](../image/db-config-data-update-ac.png)

</td></tr><tr><td id="d79299e565">

**Enable chart interaction**

</td><td>

Choose what happens when a user selects a visualization or one of its segments. 1.  Select the **Edit** button \(![Edit button](../image/edit-button.png)\) to put the dashboard into edit mode.

**Note:** If you don’t see the **Edit** button, you don’t have rights to edit the dashboard.

2.  Select **Allow chart interaction**.
3.  Select **Go to data view** to open the records view of the associated segment or visualization.
4.  Select **Apply as filter** to filter the visualizations on the dashboard on the selected element.

**Note:** This option is only available on pie, donut, semi-donut, horizontal bar, and vertical bar visualizations. It is available in the Dashboard inline editor, but not in the Visualization Designer.

5.  Select **Go to URL** to open a specified web page.


</td></tr><tr><td id="d79299e622">

**View the description of a dashboard element**

</td><td>

Point to the element, then select the information icon \(![Information icon](../../reporting/image/icon-info.png)\). If the element doesn’t have a description, the info icon doesn’t appear.

</td></tr><tr><td id="d79299e637">

**Set drilldown options**

</td><td>

Choose what happens when a user selects a visualization or one of its segments. The procedure depends on the type of dashboard. The default drilldown from a dashboard opened in Platform Analytics experience or any other workspace/experience is to Core UI artifacts.-   For a dashboard created in the inline editor and viewed in Platform Analytics experience, choose a preconfigured Chart Interaction. For more information, see [Chart interactions in a data visualization](../../par-for-workspace/concept/dv-chart-interactions.md).
-   For a dashboard created in the inline editor and viewed in a workspace/experience other than the Platform Analytics experience, see [Configure custom redirection from a dashboard component](../../performance-analytics/task/config-custom-redirection-from-db.md). The inline dashboard first has to be enabled to be viewed in the workspace, and then has to be referenced from a page built from the Dashboards page template, as described in [Add a dashboard to a Dashboards page](../../performance-analytics/task/add-dashboard-to-workspace.md).
-   For a technical dashboard, see [Add a drilldown event to a data visualization on a technical dashboard](add-custom-drilldown-event.md).


</td></tr></tbody>
</table>
**Parent Topic:**[Edit Platform Analytics dashboards](edit-db-in-ac.md)

**Related topics**  


[Share a Platform Analytics dashboard](share-db-in-ac.md)

