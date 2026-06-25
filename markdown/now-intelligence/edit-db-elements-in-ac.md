---
title: Edit in-line Platform Analytics dashboard elements
description: You can edit the contents of a dashboard or dashboard tab, including data visualizations and filters. Because dashboards are shared, any changes you make are applied globally.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/edit-db-elements-in-ac.html
release: australia
topic_type: task
last_updated: "2026-04-22"
reading_time_minutes: 5
keywords: [Performance Analytics widgets, add Performance Analytics widgets, reports, add reports to dashboard]
breadcrumb: [Edit a dashboard, Working with in-line dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Edit in-line Platform Analytics dashboard elements

You can edit the contents of a dashboard or dashboard tab, including data visualizations and filters. Because dashboards are shared, any changes you make are applied globally.

## Before you begin

Role required: dashboard\_admin for all dashboards, or any role for dashboards that you own or ones that you have been given the right to edit. See [Platform Analytics dashboard roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/pa-dashboard-roles.md) for more information about viewing and editing rights on dashboards.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Open the dashboard that you want to edit.

3.  Select **Edit** to put the dashboard into edit mode.

4.  If you are in a different application scope than the dashboard, use the application picker to select the correct scope.

    \[Omitted image "app-scope-picker.png"\] Alt text: Application scope picker

5.  Focus on the element you want to edit.

    A menu appears in the element header. The selection of actions to take depends on your roles.

    \[Omitted image "db-element-menu-itil.png"\] Alt text: Menu in header of data visualization with Add to library, Duplicate, and Delete actions.

    \[Omitted image "db-element-menu-admin.png"\] Alt text: Menu in header of filter with actions available to admin.

6.  Perform any of the following actions on the element.

<table id="choicetable_gv3_q3r_g5"><thead><tr><th align="left" id="d90613e173">

Action

</th><th align="left" id="d90613e176">

Steps

</th></tr></thead><tbody><tr><td id="d90613e182">

**Configure an element**

</td><td>

Focus on the element and select **Configure**. The configuration panel opens.Configuration options depend on the element type. For data visualizations and filters, they also depend on the visualization or filter type, respectively. For more information, see [Creating data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/creating-data-visualizations.md) or [Filters in Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/interactive-filters-workspace.md).

**Note:** There are role and ownership requirements for editing a component that is shared from a library. If you aren’t allowed to edit an element, create a local version that is not linked to the library and edit that one. For more information, see [Edit a copy of a shared dashboard element](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/editing-local-copy-saved-dv.md).

</td></tr><tr><td id="d90613e219">

**Resize the element**

</td><td>

Focus on the element. To increase its height, press **Resize**. To decrease its height, press Shift-**Resize**. To change its width or overall size, select a corner of the element and drag it.

</td></tr><tr><td id="d90613e234">

**Add an element to the Library**

</td><td>

Role required for data visualization: itil, report\_user, viz\_creator, or higherRole required for filter: analytics\_filter\_admin or higher

1.  Focus on the element.
2.  Expand the **More actions** menu \(\[Omitted image "context-menu-db-element-ac.png"\] Alt text: More actions icon\) in the header and choose **Add to library**.

\[Omitted image "context-menu-add-dv-library.png"\] Alt text: Dashboard element More actions menu with Add to library option highlighted

3.  Give the visualization a name and a description.
4.  Select **Add to library**.
The data visualization is available in the Visualization library for use on other dashboards.

</td></tr><tr><td id="d90613e280">

**Delete an element from the dashboard**

</td><td>

1.  Focus on the element that you want to delete.
2.  In the header, select the More actions menu icon \(\[Omitted image "context-menu-db-element-ac.png"\] Alt text: More actions icon\) and choose **Delete**.

\[Omitted image "delete-db-element-ac-2.png"\] Alt text: Dashboard element More actions menu with Delete option highlighted

 **Note:** There’s no confirmation message. The widget disappears from the dashboard.

</td></tr><tr><td id="d90613e316">

**Move an element between or above tabs**

</td><td>

When you have multiple tabs, you can move elements from tab to another or to the pane above the tabs.1.  Focus on the element that you want to delete.
2.  In the header, select the More actions menu icon \(\[Omitted image "context-menu-db-element-ac.png"\] Alt text: More actions icon\) and select **Move above the tabs** or **Move to a different tab**.

\[Omitted image "db-element-menu-itil.png"\] Alt text: Menu in header of filter with Move above the tabs, Move to a different tab, Add to library, Duplicate, and Delete actions.

3.  When you choose **Move to a different tab**, choose the tab and select **Move**.


</td></tr><tr><td id="d90613e359">

**Configure a data visualization to follow or not follow filters**

</td><td>

Data visualizations follow filters by default. A data visualization follows filters in the same tab as itself or above the tabs. Data visualizations either follow all such tabs that target their data sources, or none.For configuration instructions, see [Configure a data visualization to follow filters or not](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/configure-dv-follow-filters-or-not.md).

</td></tr><tr><td id="d90613e377">

**Set drilldown options**

</td><td>

Choose what happens when you select a visualization or one of its segments. The procedure depends on the type of dashboard. The default drilldown from a dashboard opened in Platform Analytics experience or any other workspace/experience is to Core UI artifacts.-   For a dashboard created in the inline editor and viewed in Platform Analytics experience, choose a preconfigured Chart Interaction. For more information, see [Chart interactions in a data visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/dv-chart-interactions.md).
-   For a dashboard created in the inline editor and viewed in a workspace/experience other than the Platform Analytics experience, see [Configure custom redirection from a dashboard component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/config-custom-redirection-from-db.md). The inline dashboard first has to be enabled to be viewed in the workspace, and then has to be referenced from a page built from the Dashboards page template, as described in [Add a dashboard to a Dashboards page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/add-dashboard-to-workspace.md).
-   For a technical dashboard, see [Add a drilldown event to a data visualization on a technical dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/add-custom-drilldown-event.md).


</td></tr></tbody>
</table>
**Parent Topic:**[Edit Platform Analytics dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/edit-db-in-ac.md)

**Related topics**  


[Share a Platform Analytics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/share-db-in-ac.md)

