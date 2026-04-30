---
title: Configure a workspace home page in Workspace Builder
description: Edit the home page for a workspace in App Engine Studio \(AES\). Adjust what users see when first accessing the workspace, which is a dashboard.
locale: en-US
release: yokohama
product: Workspace Builder
classification: workspace-builder
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Add a workspace, Add an application experience, Enhance your app, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Configure a workspace home page in Workspace Builder

Edit the home page for a workspace in App Engine Studio \(AES\). Adjust what users see when first accessing the workspace, which is a dashboard.

This video shows you how to perform the following procedure.

This video shows you how to configure a workspace home page in Workspace Builder.

## Before you begin

Role required: sn\_app\_eng\_studio.user or delegated\_developer. For more information, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## About this task

You can edit workspace home pages in Workspace Builder only for workspaces created in Tokyo and going forward. You can edit older workspaces in UI Builder.

**Note:** The home page is an essential part of the workspace, and thus can't be hidden or removed.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Next to the workspace you created, select the additional actions icon \(![Additional actions icon](../image/additional-actions-icon-purple.png)\) and then select **Edit**.

    You can also select the bar that lists the workspace in the Experience section of your app.

    ![Select to edit a workspace](../image/wb-edit-worspace-experience-purple.png "Edit a workspace")

    The home page for the workspace appears in Workspace Builder, where you can drag elements and components to design the page.

    If you created the workspace that contains a technical dashboard, Workspace Builder prompts you to **Open in UI Builder** when you try to edit the workspace.

4.  Add an element to the page.

    You must be in the **Navigation configuration** tab. If you're already in the **Navigation configuration** tab, you can't select it.

    1.  In the navigation panel, select **Home**.

        ![Workspace Builder home page](../image/workspace-builder-1-purple.png)

    2.  In the home page canvas, select **Add new element**.

    3.  From the list, select the element or component that you want to add.

        For example, to add a graphic of data from the specified table, select **Data visualization** and choose a **New data visualization** or a **Saved data visualization**.

        You can add the following elements to the home page in Workspace Builder.

<table id="table_zxl_qls_s5b"><thead><tr><th>

Element

</th><th>

Description

</th><th>

More information

</th></tr></thead><tbody><tr><td>

Data visualization

</td><td>

Graphic, visual representation of current instance data. You can create a new data visualization or repurpose an existing data visualization by choosing it in the Select visualization from library modal and selecting **Add to dashboard**.In addition to data visualizations, you can select the **Library** element to add an already-saved data visualization to the home page.

</td><td>

-   [Data visualizations in Platform Analytics](https://www.servicenow.com/docs/access?context=analytics-center-data-visualizations&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
-   [Create a single score data visualization in the Visualization Designer or on a dashboard](https://www.servicenow.com/docs/access?context=create-dv-sing-sc-ac&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
-   [Developer site data visualization component listing](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/shared-components/sn-par-visualization-base/overview)


</td></tr><tr><td>

Filter

</td><td>

Refine the visualizations on a dashboard based on specified criteria. The filters can apply to both tables and indicators.

</td><td>

-   [Filters in Platform Analytics](https://www.servicenow.com/docs/access?context=interactive-filters-workspace&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
-   [Developer site filter component listing](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/shared-components/sn-component-filter/overview)


</td></tr><tr><td>

Filter groups

</td><td>

Set of filters that you can apply simultaneously. Filter groups enable you to organize your filters and reduce the time it takes to apply them to visualizations.

</td><td>

[Create a filter group](https://www.servicenow.com/docs/access?context=create-filter-group&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)

</td></tr><tr><td>

Heading

</td><td>

Title or text for the top of the home page or section.

</td><td>

[Developer site heading component listing](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/now-heading/overview)

</td></tr><tr><td>

Image

</td><td>

Static or animated images or pictures for the workspace.

</td><td>

[Developer site image component listing](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/now-image/overview)

</td></tr><tr><td>

List - Simple

</td><td>

Table data that you can customize for the dashboard audience.

</td><td>

-   [Simple List widget](https://www.servicenow.com/docs/access?context=simple-list-widget&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) or [List - Simple Usage - Developer site](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/now-record-list-connected-snapshot/overview)
-   [Developer site List - simple component listing](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/now-record-list-connected-snapshot/overview)


</td></tr><tr><td>

Process Mining - Map

</td><td>

Visualization that shows how a process is being executed for a particular data set that is being analyzed.

</td><td>

[Configure a Process Mining map on a dashboard](https://www.servicenow.com/docs/access?context=configure-po-map&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)

</td></tr><tr><td>

Rich text

</td><td>

Content that renders in custom HTML. Rich text enables you to format text in a creative and attention-grabbing way.

</td><td>

[Developer site rich text component listing](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/now-rich-text/overview)

</td></tr></tbody>
</table>        The [Workspace Builder components for home pages](../reference/workspace-builder-components-ref.md) has details on home page elements. For more information, see [Exploring Platform Analytics dashboards](https://www.servicenow.com/docs/access?context=ac-elements&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

        If you want to include additional elements that aren't available in the **Add new element** menu, you must edit the workspace in UI Builder. For a complete list of elements you can add in UI Builder, see the components documentation on the [ServiceNow Developer Site](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?availability[]=Draft&availability[]=In+Progress&availability[]=Available&categories[]=Dev-Design+System&releases[]=utah&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades).

        The element appears on the dashboard, where you can make edits.

    4.  Drag the element to move or resize it.

    5.  In the canvas header, select **Save**.

5.  If needed, complete any additional changes to an element.

<table id="choicetable_r4f_dmd_wxb"><tbody><tr><td id="d230504e515">

**Edit an element**

</td><td>

1.  Select the element that you want to edit, such as a data visualization.

A header appears with the name of the element type.

![Data visualization element to be edited](../image/wb-data-viz-purple-new.png)

2.  Select the settings icon \(![Workspace element settings icon](../image/workspace-element-settings-icon-purple.png)\) in the element header to open the configuration panel within the canvas.

**Note:** You can also select the context menu icon \(![Context menu icon to display options](../image/context-menu-icon-purple.png)\) and select **Configure** to edit the element.

3.  Edit the configuration of the element in the configuration panel as needed.

For example, if you're editing a data visualization, you must specify the source table. For more information on editing components, see [Add and configure components](../../../administer/ui-builder/task/add-components.md#).

4.  In the canvas header, select **Save**.


</td></tr><tr><td id="d230504e579">

**Copy an element to reuse on the home page**

</td><td>

Select the context menu icon \(![Context menu icon to display options](../image/context-menu-icon-purple.png)\) and select **Duplicate** to copy the element. You can then make additional changes to the copied element.

</td></tr><tr><td id="d230504e597">

**Add an element to the library for reuse**

</td><td>

Select the context menu icon \(![Context menu icon to display options](../image/context-menu-icon-purple.png)\) and select **Add to library** to include the element in your library to reuse on other dashboards.

</td></tr><tr><td id="d230504e615">

**Delete an element from the workspace dashboard**

</td><td>

1.  Select the element that you want to delete.

A header appears with the name of the element type.

2.  In the header, select the context menu icon \(![Context menu icon to display options](../image/context-menu-icon-purple.png)\) and select **Delete**.

![Delete workspace element](../image/workspace-delete-element-purple.png)

**Note:** There's no confirmation message. The element disappears from the dashboard.

</td></tr></tbody>
</table>6.  If needed, complete any additional configuration changes to the dashboard.

<table id="choicetable_uqm_zfr_dvb"><tbody><tr><td id="d230504e664">

**Configure the dashboard layout**

</td><td>

Select and drag an entire element to move it around the dashboard layout.Resize an element by selecting and dragging the handlebars \(![Element handlebars to drag and resize](../image/wb-element-handlebars-purple.png)\) in the lower corners of the element.

</td></tr><tr><td id="d230504e682">

**Duplicate the dashboard**

</td><td>

To make a copy of the dashboard:-   Select the more options icon for the dashboard \(![More options icon](../image/wb-more-options-icon.png)\).
-   Select **Duplicate**.
-   Enter the **New name** and **Description** for the copied dashboard on the modal.
-   Select **Duplicate**.
Access the duplicated dashboard by exiting out of editing mode and selecting the new dashboard from the dashboard name drop-down menu.![Select the duplicated dashboard](../image/wb-switch-dashboards.png)

</td></tr><tr><td id="d230504e730">

**Add tabs to the workspace and edit them as needed**

</td><td>

1.  Add a tab to the home page by selecting **Add a tab**.

When you add your first tab to a home page dashboard, a new part of the layout appears below the title. Elements you add to the tab are visible no matter which tab the user is on.

A tab labeled **untitled** is added next to any existing tabs.

2.  Rename a tab by selecting the tab name, selecting the edit icon \(![Icon to edit the workspace tab name](../image/wb-edit-icon.png)\), typing the new name, and pressing **Enter**.
3.  Reorder a tab by selecting the tab and dragging it to the new position.
4.  Delete a tab by selecting its delete icon \(![Icon to delete a workspace tab](../image/trash-icon.png)\) then selecting **Delete**.

**Note:** No confirmation message appears. The tab disappears from the dashboard.

</td></tr><tr><td id="d230504e788">

**Preview a workspace and make in-line edits**

</td><td>

Make basic edits to a workspace when previewing it using the In-line editor.1.  In the Workspace Builder header, select **Preview**.
2.  In the preview that appears in a new browser tab, select **Edit**.
3.  Adjust the home page elements and widgets by resizing, reorganizing, or reconfiguring them.

For more information, see [Edit Platform Analytics dashboards](https://www.servicenow.com/docs/access?context=edit-db-in-ac&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

4.  Select **Add new element** to add items to your workspace home page.
5.  Select **Exit Editing Mode** to stop editing in the In-line editor.


</td></tr><tr><td id="d230504e840">

**Open a printer-friendly version of the dashboard**

</td><td>

Select the more options icon for the dashboard \(![More options icon](../image/wb-more-options-icon.png)\) and select **Printer friendly** to display the workspace home page in a format suitable for printing.

</td></tr><tr><td id="d230504e859">

**Add a bookmark to Analytics Center**

</td><td>

Select the more options icon for the dashboard \(![More options icon](../image/wb-more-options-icon.png)\) and select **Add to bookmarks** to include a bookmark for the workspace in the Analytics Center Bookmarks section.

</td></tr><tr><td id="d230504e882">

**Make additional or more advanced configurations to the home page**

</td><td>

In the configuration panel, select **Open in UI Builder**.

</td></tr><tr><td id="d230504e894">

**Delete the dashboard**

</td><td>

Select the more options icon for the dashboard \(![More options icon](../image/wb-more-options-icon.png)\) and select **Delete**. You must select **Delete** again to conform.**Note:** Workspaces should have at least one dashboard home page.

</td></tr></tbody>
</table>7.  Share the dashboard.

    1.  Select the more options icon for the dashboard \(![More options icon](../image/wb-more-options-icon.png)\) and select **Share**.

    2.  On the modal, fill in the fields.

<table id="table_dgn_vhr_wxb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Grant access to

</td><td>

Users and groups that can access the dashboard.

</td></tr><tr><td>

Allow recipients to add, edit, or delete sharing permissions associated with this dashboard

</td><td>

Option that enables the users and groups you share the dashboard with to add, edit, and delete the sharing rights for any user, group, or role.

</td></tr><tr><td>

Add as viewer / Add as editor

</td><td>

Option to specify read-only or write access for the dashboard.

</td></tr><tr><td>

Manage access

</td><td>

Roles that can access the dashboard. Search for and select a role in the search box. For each role with access, select the access level:-   **Can edit**
-   **Can view**
-   **Can share**


</td></tr><tr><td>

Copy link with filter

</td><td>

Button that copies the dashboard URL for the specified users and roles with the currently applied filters.

</td></tr><tr><td>

Copy link

</td><td>

Button that copies the dashboard URL for the specified users and roles without any filters.

</td></tr></tbody>
</table>    3.  Select **Confirm**.

8.  In the Workspace Builder header, select **Save**.


**Parent Topic:**[Add a workspace](add-workspace.md)

