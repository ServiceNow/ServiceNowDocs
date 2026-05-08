---
title: Edit Operational Sustainability Management dashboard elements
description: You can edit the contents of a dashboard or dashboard tab, including data visualizations and filters. Because dashboards are shared, any changes you make are applied globally.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 4
breadcrumb: [Monitoring assessment data using Operational Sustainability Management dashboards, Configure, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Edit Operational Sustainability Management dashboard elements

You can edit the contents of a dashboard or dashboard tab, including data visualizations and filters. Because dashboards are shared, any changes you make are applied globally.

## Before you begin

Role required: sn\_esg.data\_owner, sn\_esg.metrics\_manager

## About this task

You can edit the details of dashboards created in the in-line editor and in the technical editor in the Operational Sustainability Workspace. When you edit the content of dashboards created in the technical editor, you’re redirected to UI Builder.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace** &gt; **Analytics dashboard**.

2.  Select the Analytics dashboard icon ![](../images/dashboard-icon.png) and then select the dashboard you want to edit.

3.  Perform any of the following actions.

<table id="choicetable_gv3_q3r_g5"><thead><tr><th align="left" id="d23497e79">

Action

</th><th align="left" id="d23497e82">

Steps

</th></tr></thead><tbody><tr><td id="d23497e88">

**Add an element**

</td><td>

1.  Select **Edit** to put the dashboard into edit mode.
2.  Select **Add new element**. From the list, select the component you want to add. Select **Saved data visualization** or **Saved filter** to add one or more saved elements from the library to the dashboard.

You can also select **Add new element** on any selected dashboard element to see the list of elements.

3.  Select the element. The element is added to the dashboard where you can edit it.
4.  Drag to move the widget or resize it.


</td></tr><tr><td id="d23497e132">

**Save a data visualization to the Visualization Library**

</td><td>

1.  Select **Edit** to put the dashboard into edit mode.
2.  Select **Add new element**. From the list, select **Data visualization**.
3.  Create the visualization as described in [Data visualizations in Platform Analytics](https://www.servicenow.com/docs/access?context=analytics-center-data-visualizations&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).
4.  Select the More actions icon ![](../images/more-menu.png) and select **Add to library**.
5.  Give the visualization a name and a description.
6.  Select **Add to library**.
The data visualization is available in the Visualization library for use on other dashboards.

</td></tr><tr><td id="d23497e186">

**Delete an element from the dashboard**

</td><td>

1.  Select **Edit** to put the dashboard into edit mode
2.  Select the element that you want to delete.
3.  In the header, select the More actions icon ![](../images/more-menu.png) and select **Delete**.
 **Note:** There’s no confirmation message. The widget disappears from the dashboard.

</td></tr><tr><td id="d23497e221">

**Configure an element**

</td><td>

1.  Select **Edit** to put the dashboard into edit mode.
2.  Select the element that you want to edit.
3.  In the element's header, select the Configure icon ![](../images/configuration-icon.png) to open the Configuration panel.
4.  Configure the element and choose **Save**. For more information about configuring an element, see one of the following:
    -   [Edit a data visualization in an inline dashboard](https://www.servicenow.com/docs/access?context=editing-dv-in-line-db&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)
    -   [Edit a Platform Analytics filter on a dashboard](https://www.servicenow.com/docs/access?context=edit-filters-configurable-workspaces&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)
    -   [Heading component reference](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/now-components/now-heading/uib-config)
    -   [Image component reference](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/now-components/now-image/uib-setup)
    -   [Simple List component reference](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/shared-components/now-record-list-connected-snapshot/uib-setup)
 **Note:** If you change a visualization from the Visualization Library, you have the choice to save the change only to the dashboard or to the element in the library. When you change an element in the library, the change is reflected everywhere the element is used. When you change only in the dashboard, you create a copy of the visualization that exists only in that dashboard.

</td></tr><tr><td id="d23497e287">

**Move an element between tabs**

</td><td>

When you have multiple tabs, you can move elements from tab to another or to the pane above the tabs.1.  Select **Edit** to put the dashboard into edit mode.
2.  Select the More actions icon ![](../images/more-menu.png) and choose **Move to a different tab** or **Move above the tabs**.
3.  When you choose **Move to a different tab**, choose the tab and select **Move**.


</td></tr><tr><td id="d23497e327">

**Add filters to the dashboard**

</td><td>

Filters let users filter data for all report widgets on a dashboard that follow them. You can add filters to both the entire dashboard and to individual dashboard tabs.

 For more information, see [Filters in Platform Analytics](https://www.servicenow.com/docs/access?context=interactive-filters-workspace&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

</td></tr><tr><td id="d23497e346">

**Configure a data visualization to follow or not follow filters**

</td><td>

Data visualizations follow filters by default. A data visualization follows filters in the same tab as itself or above the tabs. Data visualizations either follow all such tabs that target their data sources, or none.1.  Select **Edit** to put the dashboard into edit mode.
2.  Select the dashboard element that you want to follow or not follow filters.
3.  In the header, select the Configure icon ![](../images/configuration-icon.png) to open the Configuration panel.
4.  In the Data update section, select or deselect **Follow filters**.
5.  To show a filter icon ![Filter icon.](../../../reuse/icons/product-icons/filter-outline-24.svg) on the data visualization when it follows an interactive filter, select the **Show filter icon**.


</td></tr><tr><td id="d23497e392">

**Enable chart interaction**

</td><td>

Choose what happens when a user selects a visualization or one of its segments. 1.  Select the **Edit** to put the dashboard into edit mode.
2.  Select **Allow chart interaction**.
3.  Select **Go to data view** to open the records view of the associated segment or visualization.
4.  Select **Apply as filter** to filter the visualizations on the dashboard on the selected element.

**Note:** This option is only available on pie, donut, semi-donut, horizontal bar, and vertical bar visualizations. It’s available in the Dashboard inline editor, but not in the Visualization Designer.

5.  Select **Go to URL** to open a specified web page.


</td></tr><tr><td id="d23497e438">

**View the description of a dashboard element**

</td><td>

Point to the element, then select the information icon ![](../images/details-icon.png). If the element doesn’t have a description, the info icon doesn’t appear.

</td></tr></tbody>
</table>    **Note:** If you’re unable to edit the dashboard, you don’t have permissions to edit the dashboard.


**Parent Topic:**[Monitoring assessment data using Operational Sustainability Management dashboards](monitor-data-using-esg-dashboards.md)

