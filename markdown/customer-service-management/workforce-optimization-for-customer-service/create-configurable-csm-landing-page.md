---
title: Create a Manager Workspace landing page
description: Create a landing page based on your business requirement.Set a default landing page to surface the information that is most relevant for your business.
locale: en-US
release: xanadu
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configuring Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Create a Manager Workspace landing page

Create a landing page based on your business requirement.

## Before you begin

**Important:** Starting with the Tokyo release, Legacy Workforce Optimization is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Create reports and key performance indicators that are required to set up the landing page.

Role required: sn\_mgr\_workspace.admin

## About this task

The landing page displays a set of reports that are the initial view of your workspace. You can enhance the Workforce Optimization experience by customizing the landing page to monitor metrics and trends that matter most to you. Use the User Interface \(UI\) Builder to add data visualization components to display widgets and reports that you want to track and monitor. For more information, see Creating custom landing pages for workspaces.

Using UI Builder, you can:

-   Clone the existing CSM landing page.

    **Note:** The application scope can be set to CSM Workspace, CSM Manager Workspace or Workforce Optimization. The **Clone Page** action isn’t available in the Global scope.

-   Add or edit containers in the page.
-   Add or edit visualizations for each container.
-   Edit the layout of a page or container.

## Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Administration** &gt; **Landing Pages**.

2.  Select the **CSM Landing Page**.

3.  Select **Clone Page**.

    **Note:** The **Clone Page** action is available when the application scope is CSM workspace.

4.  Fill out the form.

    The settings in the **Layout** and **Available Child Slots** fields determine how the content renders on the page.

    |Field|Description|
    |-----|-----------|
    |Name|The name of your landing page.|
    |Component|The component defaults to sn-page and is read only.|
    |Order|The order for the landing page. If you have multiple landing pages, the order determines the landing page precedence. Pages with a lower-order value take precedence over pages with a higher-order value.|
    |Active|Determines whether the landing page is active. Enable for a landing page to be displayed.|
    |Optional Page Title|A title to display on the page.|
    |Available Child Slots|A predefined style of child slots.|
    |Layout|The layout of the columns on the page.|

5.  Select **Update** to save your landing page.

6.  Configure permissions for users to access the landing page.

    1.  Select the **UX Page Element Permissions** related list.

    2.  Select **New**.

    3.  Select the role or group for the landing page to be visible.

    4.  Select **Submit** to save your permissions.

    Any page element \(including sub elements\) can have a restriction to a given set of roles or groups. If there are no element permissions set on roles or groups, then all users see the element. If there are some element permissions set, then a user needs just one role or group assignment to see the element.

7.  Configure a container:

    1.  Select the **UX Page Elements** related list.

    2.  Select **New Container** or select an existing container.

    3.  Fill out the form.

    |Field|Description|
    |-----|-----------|
    |Name|The name of your container.|
    |Component|The component defaults to sn-page-container and is read-only.|
    |Parent element|The landing page that your container resides.|
    |Slot|The component placement within the parent element's slot configuration.|
    |Order|The order the page shows.|
    |Border|Enable if you want a border around your container.|
    |Optional Container Title|A title to display on the container.|
    |Type|Select a type of styling for your visualization.|
    |Available Child Slots|A predefined style of child slots.|
    |Layout|The layout of the columns on the page.|

8.  Configure a widget:

    1.  Select **New Visualization** or select an existing widget.

    2.  Fill out the form.

<table id="table_xwv_4y1_b3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of your widget.

</td></tr><tr><td>

Component

</td><td>

The component defaults to sn-page-widget-visualization and is read only.

</td></tr><tr><td>

Parent element

</td><td>

The container that your widget resides in.

</td></tr><tr><td>

Slot

</td><td>

The component placement within the parent element's slot configuration.

</td></tr><tr><td>

Order

</td><td>

The order the component shows.

</td></tr><tr><td>

Report

</td><td>

Select the report that you want to render:-   Single score
-   Trend by
-   List
 **Note:** Choose and populate either **Report** or **PA Widget**, but you can’t display both.

</td></tr><tr><td>

PA Widget

</td><td>

Select the PA widget that you want to render:-   Single score
-   Time series
 **Note:** Choose and populate either **Report** or **PA Widget**, but you can’t display both.

</td></tr><tr><td>

Optional Widget Label

</td><td>

A label to display on the widget.

</td></tr><tr><td>

Size Variant

</td><td>

Select the size of the widget. Choices include:-   Small
-   Medium
-   Large
-   Extra Large
 **Note:** Not all size variants apply to all widgets.

</td></tr><tr><td>

Border

</td><td>

Check if you want a border around your widget.

</td></tr><tr><td>

Refresh Interval

</td><td>

Determines the number of minutes before a widget refreshes with new data. The interval begins when a user navigates away from a landing page, and ends when the user comes back to the landing page.**Note:** There’s no auto-refresh, but a user can select the refresh button at any time.

</td></tr><tr><td>

Additional Details

</td><td>

Any additional information to note about the widget.

</td></tr><tr><td>

Visualization SysID \[Read Only\]

</td><td>

Designated ID for the widget.

</td></tr><tr><td>

Report Type \[Read Only\]

</td><td>

The type of report that renders.

</td></tr></tbody>
</table>9.  Select **Update** or **Submit** to save changes to the page element.

10. Select **Update** to save changes to the landing page.


**Parent Topic:**[Configuring Workforce Optimization for Customer Service](../concept/setup-configurable-wfo-cs.md)

## Set the default landing page

Set a default landing page to surface the information that is most relevant for your business.

### Before you begin

**Important:** Starting with the Tokyo release, Legacy Workforce Optimization is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: sn\_mgr\_workspace.admin

### Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Administration** &gt; **All Workspaces**.

2.  Select **Manager Workspace**.

3.  Drag and drop the PA indicators or containers.

4.  Set the refresh rate interval for the reports or indicators.

5.  In the Landing Pages related list, set the value of the **Order** field of the landing page that you want to set as the default to minimum.

    **Note:** The landing page with the minimum order value is considered to be the default landing page.

6.  Verify the default landing page assignment by navigating to **Workspace Experience** &gt; **Administration** &gt; **Landing Pages**

    Verify the landing page that you want to set default has the minimum **Order** value.


