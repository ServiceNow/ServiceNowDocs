---
title: Edit Platform Analytics dashboards
description: You can edit dashboard and dashboard tab information in the inline editor. If the dashboard has been shared, any changes you make are applied globally.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/edit-db-in-ac.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [Edit inline editor dashboards, inline editor dashboard options, reports, add reports to dashboard]
breadcrumb: [Working with in-line dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Edit Platform Analytics dashboards

You can edit dashboard and dashboard tab information in the inline editor. If the dashboard has been shared, any changes you make are applied globally.

## Before you begin

You can edit the details of dashboards created in the inline editor and in the technical editor in the Platform Analytics experience. When you edit elements in dashboards created in the technical editor, you’re redirected to UI Builder.

Role required: dashboard\_admin for all dashboards, or any role for dashboards that you own or ones that you have been given the right to edit. See [Platform Analytics dashboard roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/pa-dashboard-roles.md) for more information about viewing and editing rights on dashboards.

## About this task

**Important:** By default, dashboards are subject to edit lock. Only one person at a time can have the same dashboard in edit mode. If you are viewing a locked dashboard, you will not have an **Edit** button even with edit rights. You will see the locking user's initials next to the **Refresh** and **View dashboard details** icons. Hover on the initials to see the user's name, company, and roles.

\[Omitted image "db-locking-user-initials.png"\] Alt text: Locked dashboard showing locking user's initials.

The **More actions** menu includes the option to clear the edit lock. Use this option with caution.

\[Omitted image "db-clear-edit-lock.png"\] Alt text: Clear edit lock option in More actions menu.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Select the dashboard that you want to edit.

    If you are in a different application scope than the dashboard, use the application picker to select the correct scope.

    \[Omitted image "app-scope-picker.png"\] Alt text: Application scope picker

3.  Perform any of the following actions.

<table id="choicetable_gv3_q3r_g5"><thead><tr><th align="left" id="d166553e161">

Action

</th><th align="left" id="d166553e164">

Steps

</th></tr></thead><tbody><tr><td id="d166553e170">

**Edit dashboard details**

</td><td>

To edit the details of a dashboard created in the inline editor:

1.  Select the information button \(\[Omitted image "icon-info-ac-2.png"\] Alt text: Dashboard details icon\).
2.  Select the **Edit** button \(\[Omitted image "edit-button.png"\] Alt text: Edit button\) to put the dashboard into edit mode.

**Note:** If you don’t see the **Edit** button, either you don’t have the right to edit the dashboard or it is in edit lock.

3.  Edit the details of the dashboard and then select **Exit editing mode**.
 To edit the details of a technical dashboard:

1.  Select the information button \[Omitted image "InfoIcon.png"\] Alt text: info icon.
2.  Select the arrow next to the **Edit in UI builder** button and then select **Edit dashboard details** to put the dashboard into edit mode.

**Note:** If you don’t see this option, you don’t have the right to edit the dashboard.

\[Omitted image "edit-tech-db-details.png"\] Alt text: Edit in UI builder menu expanded to show Edit dashboard details option

3.  Edit the details of the dashboard and then select **Exit editing mode**.
 For more information, see [Configure Platform Analytics dashboard details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/config-db-in-ac.md).

</td></tr><tr><td id="d166553e260">

**Configure the dashboard layout**

</td><td>

Select and drag an element's handlebars to resize it. Select and drag an entire element to move it around the dashboard layout. Elements include data visualizations, filters, and other dashboard content.

</td></tr><tr><td id="d166553e269">

**Add a tab to a dashboard**

</td><td>

Select **Add a tab**. A tab labeled `Untitled` is added next to any existing tabs. When you add your first tab to a dashboard, there’s a new part of the layout below the title and above the tabs. Add elements above the tabs that are visible no matter which tab has focus. Select the pencil icon \(\[Omitted image "icon-pencil-ac.png"\] Alt text: pencil icon\) to rename the tab.

</td></tr><tr><td id="d166553e293">

**Reorder a dashboard tab**

</td><td>

You can reorder tabs by dragging and dropping them. You can also reorder dashboard tabs using keyboard actions:1.  Select the **Edit** button \(\[Omitted image "edit-button.png"\] Alt text: Edit button\) to put the dashboard into edit mode.

**Note:** If you don’t see the **Edit** button, you don’t have the right to edit the dashboard.

2.  Use the TAB key to move the focus to a dashboard tab.
3.  Use the LEFT and RIGHT arrow keys to select a tab to move.
4.  Use the SHIFT+LEFT arrow or SHIFT+RIGHT arrow command to move the selected tab left or right.
5.  Select **Save**.


</td></tr><tr><td id="d166553e338">

**Duplicate a dashboard tab**

</td><td>

You can duplicate a tab on the current dashboard.1.  Select the **Edit** button \(\[Omitted image "edit-button.png"\] Alt text: Edit button\) to put the dashboard into edit mode.

**Note:** If you don’t see the **Edit** button, you don’t have the right to edit the dashboard.

2.  Select the More actions menu icon \(\[Omitted image "context-menu-db-element-ac.png"\] Alt text: More actions icon\) next to the tab's name and choose **Duplicate**.
A new tab with the same content as the duplicated tab opens with the name Untitled. Choose the pencil icon to rename the tab.

</td></tr><tr><td id="d166553e380">

**Delete a dashboard tab**

</td><td>

1.  Select the **Edit** button \(\[Omitted image "edit-button.png"\] Alt text: Edit button\) to put the dashboard into edit mode.

**Note:** If you don’t see the **Edit** button, you don’t have the right to edit the dashboard.

2.  Select the More actions menu icon \(\[Omitted image "context-menu-db-element-ac.png"\] Alt text: More actions icon\) next to the tab's name and choose **Delete**.
 **Note:** There’s no confirmation message. The tab disappears from the dashboard.

</td></tr><tr><td id="d166553e424">

**Rename a tab**

</td><td>

1.  Select the tab to make it active.
2.  Point to the tab name and select the pencil icon \(\[Omitted image "icon-pencil-ac.png"\] Alt text: pencil icon\).
3.  Type the new name then press Enter.
 **Note:** If you rename a tab on a dashboard that has been translated, the translations are replaced with the new English tab name. To translate the new name:

1.  Navigate to **User Menu** &gt; **Preferences**.
2.  On the **Display** tab, select the target language.
3.  On the translated dashboard, rename the tab with the translation of its new name.


</td></tr><tr><td id="d166553e477">

**Configure the refresh settings**

</td><td>

Role required: admin.1.  Select the **Edit** button \(\[Omitted image "edit-button.png"\] Alt text: Edit button\) to put the dashboard into edit mode.

**Note:** If you don’t see the **Edit** button, you don’t have the right to edit the dashboard.

2.  Select the Dashboard Settings button \(\[Omitted image "icon-cogwheel-ac.png"\] Alt text: Edit columns icon\) to open the Settings panel.
3.  Select **Show refresh information** to show the time of the last refresh under the dashboard's title.
4.  Select **Scheduled repetition** to configure the number of minutes that the dashboard is automatically refreshed.

The minimum refresh interval is 10 minutes.

</td></tr><tr><td id="d166553e526">

**Configure background colors**

</td><td>

1.  Open the Background Color menu to show the preconfigured colors.
2.  Choose an existing color or select the Color Palette icon \(\[Omitted image "icon-color-palette.png"\] Alt text: palette icon\) to open the palette.

Specify Hex or RGBA values, or choose from the color picker.

</td></tr><tr><td id="d166553e552">

**Configure Insights**

</td><td>

Choose whether and which analytics to show in the **Insights** section.When you select **Show insights panel**, an Insights button is added to the dashboard and the selected analytics options are shown. For more information, see [Proactive analytics insights on dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/proactive-analytics/proactive-analytics.md).

</td></tr></tbody>
</table>
-   **[Add visual elements to an in-line dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/add-elements-to-a-dashboard.md)**  
Populate your dashboard with a selection of widgets, including data visualizations and filters.
-   **[Edit in-line Platform Analytics dashboard elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/edit-db-elements-in-ac.md)**  
You can edit the contents of a dashboard or dashboard tab, including data visualizations and filters. Because dashboards are shared, any changes you make are applied globally.
-   **[Group dashboard elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/group-db-elements.md)**  
Improve your layout control and dashboard customization capabilities, by organizing related elements into single visual and logical units. Configure backgrounds and borders according to group.
-   **[Edit a copy of a shared dashboard element](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/editing-local-copy-saved-dv.md)**  
To configure a shared element that you added to a dashboard from a library, make a local copy that is not linked to a library. You only have to do this if you do not have permission to edit the version in the library.
-   **[Add images to Platform Analytics dashboard cards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/add-images-db-cards-ac.md)**  
Distinguish the cards in the dashboard overview with uploaded images.

**Parent Topic:**[Common dashboard tasks in the in-line editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/common-dashboard-tasks.md)

**Related topics**  


[Create a dashboard with the in-line editor]()

[Share a Platform Analytics dashboard]()

[Duplicate a Platform Analytics dashboard]()

[Print a Platform Analytics dashboard]()

[Export a Platform Analytics dashboard]()

[Schedule the export of dashboards and data visualizations]()

[Bookmark a Platform Analytics dashboard]()

[Delete a Platform Analytics dashboard]()

