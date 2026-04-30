---
title: Edit Platform Analytics dashboards
description: You can edit dashboard and dashboard tab information in the inline editor. If the dashboard has been shared, any changes you make are applied globally.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
keywords: [Edit inline editor dashboards, inline editor dashboard options, reports, add reports to dashboard]
breadcrumb: [Dashboards in Platform Analytics, Platform Analytics experience, Platform Analytics]
---

# Edit Platform Analytics dashboards

You can edit dashboard and dashboard tab information in the inline editor. If the dashboard has been shared, any changes you make are applied globally.

## Before you begin

You can edit the details of the dashboards you've created. When you edit the content of dashboards created in the technical editor, you’re redirected to UI Builder.

Role required: dashboard\_admin for all dashboards, or any role for dashboards that you own or ones that you have been given the right to edit. See [Platform Analytics dashboard roles](../../par-for-workspace/concept/pa-dashboard-roles.md) for more information about viewing and editing rights on dashboards.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Select the dashboard that you want to edit.

    If you are in a different application scope than the dashboard, use the application picker to select the correct scope.

    ![Application scope picker](../../par-for-workspace/image/app-scope-picker.png)

3.  Perform any of the following actions.

<table id="choicetable_gv3_q3r_g5"><thead><tr><th align="left" id="d132550e122">

Action

</th><th align="left" id="d132550e125">

Steps

</th></tr></thead><tbody><tr><td id="d132550e131">

**Edit dashboard details**

</td><td>

To edit the details of a dashboard created in the inline editor:

1.  Select the information button \(![Dashboard details icon](../../reporting/image/icon-info-ac-2.png)\).
2.  Select the **Edit** button \(![Edit button](../image/edit-button.png)\) to put the dashboard into edit mode.

**Note:** If you don’t see the **Edit** button, you don’t have the right to edit the dashboard.

3.  Edit the details of the dashboard and then select **Exit editing mode**.
 To edit the details of a technical dashboard:

1.  Select the information button ![info icon](../../performance-analytics/image/InfoIcon.png).
2.  Select the arrow next to the **Edit in UI builder** button and then select **Edit dashboard details** to put the dashboard into edit mode.

**Note:** If you don’t see this option, you don’t have the right to edit the dashboard.

![Edit in UI builder menu expanded to show Edit dashboard details option](../../par-for-workspace/image/edit-tech-db-details.png)

3.  Edit the details of the dashboard and then select **Exit editing mode**.
 For more information, see [Configure Platform Analytics dashboard details](config-db-in-ac.md).

</td></tr><tr><td id="d132550e221">

**Configure the dashboard layout**

</td><td>

Select and drag an element's handlebars to resize it. Select and drag an entire element to move it around the dashboard layout. Elements include data visualizations, filters, and other dashboard content.

</td></tr><tr><td id="d132550e230">

**Add a tab to a dashboard**

</td><td>

Select **Add a tab**. A tab labeled `Untitled` is added next to any existing tabs. When you add your first tab to a dashboard, there’s a new part of the layout below the title and above the tabs. Add elements above the tabs that are visible no matter which tab has focus. Select the pencil icon \(![pencil icon](../image/icon-pencil-ac.png)\) to rename the tab.

</td></tr><tr><td id="d132550e254">

**Reorder a dashboard tab**

</td><td>

You can reorder tabs by dragging and dropping them. You can also reorder dashboard tabs using keyboard actions:1.  Select the **Edit** button \(![Edit button](../image/edit-button.png)\) to put the dashboard into edit mode.

**Note:** If you don’t see the **Edit** button, you don’t have the right to edit the dashboard.

2.  Use the TAB key to move the focus to a dashboard tab.
3.  Use the LEFT and RIGHT arrow keys to select a tab to move.
4.  Use the SHIFT+LEFT arrow or SHIFT+RIGHT arrow command to move the selected tab left or right.
5.  Select **Save**.


</td></tr><tr><td id="d132550e299">

**Duplicate a dashboard tab**

</td><td>

You can duplicate a tab on the current dashboard.1.  Select the **Edit** button \(![Edit button](../image/edit-button.png)\) to put the dashboard into edit mode.

**Note:** If you don’t see the **Edit** button, you don’t have the right to edit the dashboard.

2.  Select the More actions menu icon \(![More actions icon](../image/context-menu-db-element-ac.png)\) next to the tab's name and choose **Duplicate**.
A new tab with the same content as the duplicated tab opens with the name Untitled. Choose the pencil icon to rename the tab.

</td></tr><tr><td id="d132550e341">

**Delete a dashboard tab**

</td><td>

1.  Select the **Edit** button \(![Edit button](../image/edit-button.png)\) to put the dashboard into edit mode.

**Note:** If you don’t see the **Edit** button, you don’t have the right to edit the dashboard.

2.  Select the More actions menu icon \(![More actions icon](../image/context-menu-db-element-ac.png)\) next to the tab's name and choose **Delete**.
 **Note:** There’s no confirmation message. The tab disappears from the dashboard.

</td></tr><tr><td id="d132550e385">

**Rename a tab**

</td><td>

1.  Select the tab to make it active.
2.  Point to the tab name and select the pencil icon \(![pencil icon](../image/icon-pencil-ac.png)\).
3.  Type the new name then press Enter.
 **Note:** If you rename a tab on a dashboard that has been translated, the translations are replaced with the new English tab name. To translate the new name:

1.  Navigate to **User Menu** &gt; **Preferences**.
2.  On the **Display** tab, select the target language.
3.  On the translated dashboard, rename the tab with the translation of its new name.


</td></tr><tr><td id="d132550e438">

**Configure the refresh settings**

</td><td>

Role required: admin.1.  Select the **Edit** button \(![Edit button](../image/edit-button.png)\) to put the dashboard into edit mode.

**Note:** If you don’t see the **Edit** button, you don’t have the right to edit the dashboard.

2.  Select the Dashboard Settings button \(![Edit columns icon](../image/icon-cogwheel-ac.png)\) to open the Settings panel.
3.  Select **Show refresh information** to show the time of the last refresh under the dashboard's title.
4.  Select **Scheduled repetition** to configure the number of minutes that the dashboard is automatically refreshed.

The minimum refresh interval is 10 minutes.

</td></tr><tr><td id="d132550e487">

**Configure background colors**

</td><td>

1.  Open the Background Color menu to show the preconfigured colors.
2.  Choose an existing color or select the Color Palette icon \(![palette icon](../image/icon-color-palette.png)\) to open the palette.

Specify Hex or RGBA values, or choose from the color picker.

</td></tr><tr><td id="d132550e513">

**Configure Insights**

</td><td>

Choose whether and which analytics to show in the **Insights** section.When you select **Show insights panel**, an Insights button is added to the dashboard and the selected analytics options are shown. For more information, see [Proactive analytics insights on dashboards](../../par-for-workspace/concept/proactive-analytics.md).

</td></tr></tbody>
</table>
-   **[Edit Platform Analytics dashboard elements](edit-db-elements-in-ac.md)**  
You can edit the contents of a dashboard or dashboard tab, including data visualizations and filters. Because dashboards are shared, any changes you make are applied globally.
-   **[Add images to Platform Analytics dashboard cards](add-images-db-cards-ac.md)**  
Distinguish the cards in the dashboard overview with uploaded images.

**Parent Topic:**[Dashboards in Platform Analytics](../../performance-analytics/concept/analytics-center-dashboards.md)

**Related topics**  


[Share a Platform Analytics dashboard](share-db-in-ac.md)

[Configure Platform Analytics dashboard details](config-db-in-ac.md)

[Configure Platform Analytics dashboard settings](configure-ac-db-settings.md#)

