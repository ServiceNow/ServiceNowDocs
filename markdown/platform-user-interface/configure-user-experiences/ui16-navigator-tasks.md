---
title: Use the Core UI navigator
description: Everyone can collapse and expand the navigator, work with favorites, and view navigation history in Core UI.You can collapse or expand information in the application navigator to display only what you want to see.You can add, edit, or delete favorites for frequently accessed items in the application navigator.In Core UI, you can view your navigation history in the application navigator.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/configure-user-experiences/ui16-navigator-tasks.html
release: zurich
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Core UI application navigator, Core UI, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Use the Core UI navigator

Everyone can collapse and expand the navigator, work with favorites, and view navigation history in Core UI.

## Before you begin

Role required: admin

## About this task

Complete any of the following tasks to work with the navigator in Core UI.

**Parent Topic:**[Core UI application navigator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/c_UI16ApplicationNavigator.md)

## Collapse or expand information in the Core UI application navigator

You can collapse or expand information in the application navigator to display only what you want to see.

### Before you begin

Role required: none

### Procedure

1.  Perform one of the following actions.

<table id="choicetable_ah3_rs3_ks"><tbody><tr><td id="d119843e149">

**Collapse or expand an application or application section**

</td><td>

Click the application or application section label.

</td></tr><tr><td id="d119843e158">

**Collapse or expand all applications**

</td><td>

Double-click the all applications tab icon \(\[Omitted image "IconUI16AllApplications.png"\] Alt text: All applications tab icon\).

</td></tr><tr><td id="d119843e173">

**Collapse or expand the application navigator**

</td><td>

Click the arrow icon at the bottom of the application navigator. In the collapsed view, the application navigator displays favorites only. Click the filter icon or the arrow icon in the collapsed view to expand the application navigator.

</td></tr></tbody>
</table>    \[Omitted image "UI16CollapsedApplicationNavigator.png"\] Alt text: The collapsed view of the application navigator displays favorites only


## Add or edit favorites in Core UI

You can add, edit, or delete favorites for frequently accessed items in the application navigator.

### Before you begin

Role required: none

### About this task

Items you add as favorites appear in the favorites tab of the application navigator, represented by a star icon.

\[Omitted image "UI16Favorites.png"\] Alt text: Core UI favorites in the application navigator favorites tab

Favorites also appear in the collapsed view of the application navigator as icons.

### Procedure

1.  Add a favorite in one of the following ways.

<table id="choicetable_wqh_2yx_pt"><tbody><tr><td id="d119843e301">

**Add a module as a favorite**

</td><td>

In the application navigator, click the star icon by a module.

</td></tr><tr><td id="d119843e310">

**Add all the modules under an application as favorites**

</td><td>

In the application navigator, click the star icon by an application.

</td></tr><tr><td id="d119843e319">

**Add a list as a favorite using the list context menu**

</td><td>

1.  Open a list.
2.  Click the list context menu icon \(\[Omitted image "MenuIconUI14.png"\] Alt text: List context menu icon\) by the list title.
3.  Select **Create Favorite**.
4.  In the flyout, edit the name and icon as needed.


</td></tr><tr><td id="d119843e352">

**Add a list as a favorite by dragging and dropping**

</td><td>

1.  Open a list.
2.  Drag a breadcrumb to the **Favorites** tab of the application navigator.


</td></tr><tr><td id="d119843e373">

**Add a record as a favorite using the form context menu**

</td><td>

1.  Open a record.
2.  Click the form context menu icon \(\[Omitted image "MenuIconUI14.png"\] Alt text: Form context menu icon\) by the form title.
3.  Select **Create Favorite**.
4.  In the flyout, edit the name and icon as needed.


</td></tr><tr><td id="d119843e407">

**Add a record as a favorite by dragging and dropping**

</td><td>

1.  Open a record.
2.  Drag the record title to the **Favorites** tab of the application navigator.


</td></tr><tr><td id="d119843e428">

**Add a different type of link as a favorite**

</td><td>

Drag a supported link type to the **Favorites** tab of the application navigator. You can drag any of the following links:-   Breadcrumbs
-   Links in lists
-   Reports
 **Note:** You may not be able to create bookmarks with other types of links.

</td></tr><tr><td id="d119843e455">

**Add a knowledge base article as a favorite**

</td><td>

1.  Open a knowledge article.
2.  In the header at the top left, click the star icon.
3.  In the **Create Favorite** dialog box, edit the name and icon as needed.
4.  Click **Done**.


</td></tr></tbody>
</table>    You can add a different favorite for each view of a list or form.

    The favorite is added to the **Favorites** tab of the application navigator.

2.  To edit or delete a favorite, complete any of the following actions.

<table id="choicetable_zxc_mcg_qs"><tbody><tr><td id="d119843e503">

**Reorder favorites in the list**

</td><td>

1.  At the bottom of the application navigator, click **Edit Favorites**.
2.  Drag a favorite to a new location in the list.
3.  Click **Done** or **Edit Favorites**.


</td></tr><tr><td id="d119843e533">

**Customize the name or icon for a favorite**

</td><td>

1.  At the bottom of the application navigator, click **Edit Favorites**.
2.  Click a favorite.
3.  Customize the name and icon as needed.
4.  Click **Done** or **Edit Favorites**.


</td></tr><tr><td id="d119843e566">

**Delete a favorite**

</td><td>

1.  Point to the favorite.
2.  Click the remove favorite icon \(\[Omitted image "RemoveFavoriteIcon.png"\] Alt text: Remove Favorite icon\).


</td></tr></tbody>
</table>
## View your navigation history in Core UI

In Core UI, you can view your navigation history in the application navigator.

### Before you begin

Role required: none

### About this task

Items you have accessed recently appear in the history tab of the application navigator, which is represented by a clock icon. Items appear in chronological order from most to least recently accessed.

\[Omitted image "UI16YourHistory.png"\] Alt text:

History entries are stored in the Navigator History \[sys\_ui\_navigator\_history\] table. The system creates history entries for many types of content, including lists, records, and dashboards. Some content types are not tracked in the history, such as UI pages and other non-standard interfaces.

### Procedure

1.  In the application navigator, click the history tab, which is represented by a clock.

2.  Click an item to open it.


