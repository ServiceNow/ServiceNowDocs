---
title: Edit Operational Sustainability Management dashboards
description: You can edit dashboard and dashboard tab information in the in-line editor. If the dashboard has been shared, any changes you make are applied globally.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-09-23"
reading_time_minutes: 4
breadcrumb: [Monitoring assessment data using Operational Sustainability Management \(formerly ESG\) dashboards, Configure, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Edit Operational Sustainability Management dashboards

You can edit dashboard and dashboard tab information in the in-line editor. If the dashboard has been shared, any changes you make are applied globally.

## Before you begin

Role required: sn\_esg.data\_owner, sn\_esg.metrics\_manager

## About this task

You can edit the details of the dashboards you have created. When you edit the content of dashboards created in the technical editor, you’re redirected to UI Builder.

**Important:** By default, dashboards are subject to edit lock. Only one person at a time can have the same dashboard in edit mode. If you’re viewing a locked dashboard, you aren’t able to make edits even with edit permissions. You’ll see the locking user's initials next to the **Refresh** and **View dashboard details** icons. Hover on the initials to see the user's name, company, and roles.

The **More actions** menu includes the option to clear the edit lock. Use this option with caution.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace** &gt; **Analytics dashboard**.

2.  Select the Analytics dashboard icon and then select the dashboard you want to edit.

3.  Perform any of the following actions.

<table id="choicetable_gv3_q3r_g5"><thead><tr><th align="left" id="d20233e104">

Action

</th><th align="left" id="d20233e107">

Steps

</th></tr></thead><tbody><tr><td id="d20233e113">

**Edit dashboard details**

</td><td>

To edit the details of a dashboard created in the in-line editor:

1.  Select the View dashboard details icon ![](../images/details-icon.png).
2.  Select **Edit** to put the dashboard into edit mode.
3.  Edit the details of the dashboard and then select **Exit editing mode**.
 To edit the details of a technical dashboard:

1.  Select the View dashboard details icon ![](../images/details-icon.png).
2.  Select the arrow next to the **Edit in UI builder** button and then select **Edit dashboard details** to put the dashboard into edit mode.

**Note:** If you don’t see this option, you don’t have permission to edit the dashboard.

3.  Edit the details of the dashboard and then select **Exit editing mode**.
 For more information, see [Edit Operational Sustainability Management dashboard details](edit-esg-dashboard-details.md).

</td></tr><tr><td id="d20233e187">

**Configure the dashboard layout**

</td><td>

Select and drag an element's handlebars to resize it. Select and drag an entire element to move it around the dashboard layout. Elements include data visualizations, filters, and other dashboard content.

</td></tr><tr><td id="d20233e196">

**Add a tab to a dashboard**

</td><td>

Select **Add a tab**. A tab labeled `New Tab` is added next to any existing tabs. When you add your first tab to a dashboard, there’s a new part of the layout below the title and above the tabs. Add elements above the tabs that are visible no matter which tab has focus. Select the pencil icon ![](../images/pencil-icon.png) to rename the tab.

</td></tr><tr><td id="d20233e219">

**Reorder a dashboard tab**

</td><td>

You can reorder tabs by dragging and dropping them. You can also reorder dashboard tabs using keyboard actions:1.  Select **Edit** to put the dashboard into edit mode.
2.  Use the TAB key to move the focus to a dashboard tab.
3.  Use the LEFT and RIGHT arrow keys to select a tab to move.
4.  Use the SHIFT+LEFT arrow or SHIFT+RIGHT arrow command to move the selected tab left or right.
5.  Select **Save**.


</td></tr><tr><td id="d20233e253">

**Duplicate a dashboard tab**

</td><td>

You can duplicate a tab on the current dashboard.1.  Select **Edit** to put the dashboard into edit mode.
2.  Select the More actions icon ![](../images/more-menu.png) next to the tab's name and choose **Duplicate**.
A new tab with the same content as the duplicated tab opens with the name `New Tab`. Choose the pencil icon ![](../images/pencil-icon.png) to rename the tab.

</td></tr><tr><td id="d20233e291">

**Delete a dashboard tab**

</td><td>

1.  Select **Edit** to put the dashboard into edit mode.
2.  Select the More actions icon ![](../images/more-menu.png) next to the tab's name and choose **Delete**.
 **Note:** There’s no confirmation message. The tab disappears from the dashboard.

</td></tr><tr><td id="d20233e323">

**Rename a tab**

</td><td>

1.  Select the tab to make it active.
2.  Point to the tab name and select the pencil icon.
3.  Enter the new name.
 **Note:**

If you rename a tab on a dashboard that has been translated, the translations are replaced with the new English tab name. To translate the new name:

1.  Navigate to User Menu &gt; Preferences.
2.  On the Display tab, select the target language.
3.  On the translated dashboard, rename the tab with the translation of its new name.


</td></tr><tr><td id="d20233e362">

**Configure the refresh settings**

</td><td>

Role required: admin.1.  Select **Edit** to put the dashboard into edit mode.
2.  Select the Dashboard settings icon ![](../images/settings-icon.png) to open the Settings panel.
3.  Select **Show refresh information** to show the time of the last refresh under the dashboard's title.
4.  Select **Scheduled repetition** to configure the number of minutes that the dashboard is automatically refreshed.

The minimum refresh interval is 10 minutes.

</td></tr><tr><td id="d20233e401">

**Configure background colors**

</td><td>

1.  Select **Edit** to put the dashboard into edit mode.
2.  Select the Dashboard settings icon ![](../images/settings-icon.png) to open the Settings panel.
3.  Open the Background Color menu to show the pre-configured colors.
4.  Choose an existing color or select the Color Palette icon to open the palette.

Specify Hex or RGBA values, or choose from the color picker.

</td></tr><tr><td id="d20233e435">

**Configure Insights**

</td><td>

Choose whether and which analytics to show in the **Insights** section.When you select **Show insights panel**, an Insights button is added to the dashboard and the selected analytics options are shown. For more information, see [Proactive analytics insights on dashboards](https://www.servicenow.com/docs/access?context=proactive-analytics&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

</td></tr></tbody>
</table>    **Note:** If you aren’t able to edit, either you don’t have permission to edit the dashboard, or it is in edit lock.


**Parent Topic:**[Monitoring assessment data using Operational Sustainability Management \(formerly ESG\) dashboards](monitor-data-using-esg-dashboards.md)

