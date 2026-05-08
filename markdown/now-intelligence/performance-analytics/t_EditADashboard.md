---
title: Edit a responsive dashboard
description: You can edit the contents of a dashboard, including Performance Analytics widgets, reports, and tabs. Because dashboards are shared, any modifications you make are applied globally.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Performance Analytics widgets, add Performance Analytics widgets, reports, add reports to dashboard, add a report to dashboard, add CMDB widgets to dashboards, CMDB widgets, risk assessment heatmaps, add risk assessment heatmaps to dashboards, Top Searches widgets, text search widgets, add Top Searches, delete a widget personal dashboard, edit a dashboard, add an interactive filter to a dashboard, remove a widget from a dashboard]
breadcrumb: [Create and use dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Edit a responsive dashboard

You can edit the contents of a dashboard, including Performance Analytics widgets, reports, and tabs. Because dashboards are shared, any modifications you make are applied globally.

## Before you begin

**Note:** This topic refers to Dashboards in the Core UI. If your instance is migrated to Platform Analytics experience, see [Edit Platform Analytics dashboards](edit-db-in-ac.md).

Owners of Core UI responsive dashboards have the option to migrate these dashboards to Platform Analytics experience. For more information, see [Migrate dashboards that you own](../../par-for-workspace/task/data-migration-migrate-dbs-you-own.md).

If Platform Analytics experience is enabled, the dashboard picker shows both Core UI and Platform Analytics experience dashboards.

Core UI dashboard backgrounds are not themeable with custom colors.

Role required: The dashboard\_admin role is required to create or edit Core UI Responsive Dashboards, which may still be necessary in Service Portal, for example. See [Dashboard permissions](../concept/c_DashboardRoles.md) for more information about viewing and editing rights on dashboards.

**Note:** Responsive dashboards do not support the Sticky Notes widget.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards** or **All** &gt; **Performance Analytics** &gt; **Dashboards**.

2.  From the dashboard picker, select the dashboard that you want to edit.

3.  Perform any of the following actions.

<table id="choicetable_gv3_q3r_g5"><thead><tr><th align="left" id="d230674e213">

Action

</th><th align="left" id="d230674e216">

Steps

</th></tr></thead><tbody><tr><td id="d230674e222">

**Add a widget**

</td><td>

1.  Click the plus sign \(![Plus sign button](../image/AddWidgetButton.png)\) to put the dashboard in edit mode.
2.  From the list, select the type of widget that you want to add, for example, Performance Analytics, Report, or Content Block.
3.  Select the widget. A preview of the widget appears.
4.  Click **Add**. The widget appears at the top of the dashboard.
5.  Drag to move the widget or resize it.
 **Note:** Data visualization titles are not automatically translated on localized ServiceNow instances.

</td></tr><tr><td id="d230674e264">

**Delete a widget from the dashboard**

</td><td>

1.  Click the plus sign \(![Plus sign button](../image/icon-add-user-db.png)\) to put the dashboard in edit mode.
2.  Point to the top of the widget, then click the X icon \(![X icon](../image/RemoveWidgetButton.png)\) that appears.
 **Note:** There is no confirmation message. The widget disappears from the dashboard.

</td></tr><tr><td id="d230674e298">

**Configure widget layouts**

</td><td>

To change widget appearance and layouts, and show and hide widget headers, see [Configure the layout of a responsive dashboard](configure-widget-layouts.md).

</td></tr><tr><td id="d230674e314">

**Edit a widget**

</td><td>

1.  Click the plus sign \(![Plus sign button](../image/icon-add-user-db.png)\) to put the dashboard in edit mode.
2.  Point to the widget's header and select the pencil icon \(![Pencil icon](../image/EditWidgetButton.png)\). This icon is available only if your roles give you access to the widget's source. Edit rights to a dashboard do not necessarily give you edit rights to the widgets on that dashboard.

![Widget header with edit options shown by pointing at it](../image/widget-edit-mode-header.png)

 The widget opens in the tool where it was created. For example, when you edit a report widget, the source report opens in the Report Designer.

</td></tr><tr><td id="d230674e354">

**Apply a quick layout to a dashboard**

</td><td>

Click the configuration icon \(![Configuration icon](../image/ConfigurationPaneButton.png)\) to open the Configuration pane, then click a layout to snap the widgets against. Modify the layout as desired.

</td></tr><tr><td id="d230674e369">

**Add a tab to a dashboard**

</td><td>

Click the configuration icon \(![Configuration icon](../image/ConfigurationPaneButton.png)\) to open the Configuration pane, then click **Create Tab**. The panel created with the dashboard becomes the dashboard's first tab. The default names of the tabs are the name of the dashboard followed by New Tab and New Tab 2. To change the default names, see Rename a tab in this table.**Note:** You cannot link an existing tab into a dashboard.

</td></tr><tr><td id="d230674e390">

**Reorder a dashboard tab**

</td><td>

1.  Click the plus sign \(![Plus sign button](../image/AddWidgetButton.png)\) to put the dashboard in edit mode.
2.  Select the dashboard tab and drag it to the desired position.
 Alternatively,

1.  Click the context menu \(![Context menu icon](../../../common/image/Form_MenuIcon.png)\) and select **Dashboard Properties**.
2.  On the **Dashboard Tabs** related list, enter numbers in the **Order** column to specify the tab order. Tabs display from left to right with lower numbers appearing first.


</td></tr><tr><td id="d230674e441">

**Delete a dashboard tab**

</td><td>

Click the tab to make it active. Point to the tab name and click the trash icon that appears.**Note:** The dashboard tab no longer appears on any dashboards where it appeared. Dashboards may have tabs that appear in multiple dashboards.

</td></tr><tr><td id="d230674e453">

**Rename a tab**

</td><td>

1.  Click the tab to make it active.
2.  Point to the tab name and click the pencil icon that appears.
3.  Type the new name then press Enter.
 **Note:** If you rename a tab on a dashboard that has been translated, the translations are replaced with the new English tab name. To translate the new name:

1.  Navigate to **User Menu** &gt; **Preferences**.
2.  On the **Display** tab, select the target language.
3.  On the translated dashboard, rename the tab with the translation of its new name.


</td></tr><tr><td id="d230674e500">

**Enable filtering of data for report widgets**

</td><td>

Interactive filters let users filter data for all report widgets on a dashboard that follow them.1.  Click the plus sign \(![Plus sign button](../image/AddWidgetButton.png)\) to put the dashboard in edit mode.
2.  From the list, select **Interactive Filters**.
3.  Navigate to the filter you want to add.
4.  Click **Add**.
For more information, see [Interactive Filters](../concept/c_HomepagePublishers.md).

</td></tr><tr><td id="d230674e545">

**Configure a report widget to follow interactive filters**

</td><td>

1.  Point to the report widget, then click the gear icon \(![Gear icon](../image/Pa_dashboard_cog.png)\).
2.  In the Edit Widget window, select the **Follow interactive filter** check box.
3.  To show a filter icon \(![Filter icon](../image/InteractiveFilterFilteringIcon.png)\) on the report when it is following an interactive filter, select the **Show when following** check box.
 **Note:** Performance Analytics widgets cannot follow interactive filters.

</td></tr><tr><td id="d230674e587">

**Enable filtering of data for Performance Analytics widgets**

</td><td>

1.  Click the plus sign \(![Plus sign button](../image/AddWidgetButton.png)\) to put the dashboard in edit mode.
2.  Add a breakdown to a dashboard so that users can filter data for all Performance Analytics widgets on that dashboard. Only users with the pa\_admin or pa\_power user roles can work with breakdowns.
 See [Add breakdown sources to a dashboard](t_ExistingBreakdownDashboard.md).

</td></tr><tr><td id="d230674e621">

**View the description of a widget**

</td><td>

Point to the widget, then click the question mark \(![Question mark icon](../image/QuestionMarkButtonWidgets.png)\). If the widget does not have a description, the question mark icon does not appear.

</td></tr></tbody>
</table>
-   **[Configure the layout of a responsive dashboard](configure-widget-layouts.md)**  
You can change the appearance of widgets; change widget layouts; change the colors of the widget title, header, and background; and show or hide widget headers.

**Parent Topic:**[Create and use dashboards](../concept/create-and-edit-dashboards.md)

**Related topics**  


[Share a responsive dashboard](t_ControlAccessToADashboard.md)

