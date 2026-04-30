---
title: Create a widget that displays a ServiceNow UI page
description: You can create a ServiceNow UI page that displays a web page. You can then add that UI page to a widget that can be added to dashboards.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [UI page, Dashboards]
breadcrumb: [Widgets, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a widget that displays a ServiceNow UI page

You can create a ServiceNow UI page that displays a web page. You can then add that UI page to a widget that can be added to dashboards.

## Before you begin

Role required: admin

## About this task

A UI page is a ServiceNow page that is not a list or a form. Not every UI page will fit in a widget. Some UI pages, such as external site widgets or gadgets, don’t display properly when placed in a dashboard.

To learn how to make a UI page without using a framework page template, see the [Making a UI page without using the framework page template](https://community.servicenow.com/community?id=community_blog&sys_id=e26e22eddbd0dbc01dcaf3231f96196e) blog posting by a developer in the ServiceNow Community.

**Note:** This functionality requires a knowledge of JavaScript.

## Procedure

1.  Create or find a ServiceNow UI page that you want to display as a widget.

    Note the name of this UI page, to use in Step 4. The UI page name is the value of the name field in the form where you define the content of the UI page.

2.  Navigate to **System UI** &gt; **Widgets** and click **New**.

    **Widgets** records are widget category records, not records for individual widgets. When adding a widget to the dashboard, first select the category and then the widget. The JavaScript you specify in step 4 includes the list of widgets to include in that category.

3.  Fill in the following fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|The name of this widget category. Select this category when adding its widgets to a dashboard.|
    |**Renderer Type**|Select **JavaScript**.|
    |**Active**|Clear this field to make the widget unavailable to add to dashboards.|
    |**Roles**|Select which roles can see this category when adding widgets to dashboards. If you select no roles, all roles can see the category.|

4.  Add the following JavaScript in the **Script** field, making replacements as specified.

    The return statement contains the widgets listed in this widget category.

    **Note:** The code snippet in this step works in non-scoped applications. Use the code snippet in step 5 for scoped applications.

<table id="simpletable_nph_gcf_cw"><tbody><tr><td>

widget\_name

</td><td>

The name of the widget that the user selects in the widget picker when adding the widget to a dashboard. This string also appears on the widget header. This value is the Name that you configure in step 3.

</td></tr><tr><td>

UI\_page\_name

</td><td>

The name of the UI page from step 1 to show in the widget.

</td></tr></tbody>
</table>    ```
    function sections() {
        return {
            'widget_name': { 'uiPageName' : 'UI_page_name'},
            'widget_name2': {'uiPageName': 'UI_page_name_2'}
        };
    }
    
    function render() {
        var uiPageName = renderer.getPreferences().get("uiPageName");
        return renderer.getRenderedPage(uiPageName);
    }
    
    function getEditLink() {
        var uiPageName = renderer.getPreference('uiPageName');
        return 'sys_ui_page.do?sysparm_query=' + encodeURIComponent('name=' + uiPageName);
    }
    ```

5.  Use this code example for scoped applications:

    ```
    function sections() {
        return {
        'Widget': {
        'type': 'widgetname'
        }
        };
    }
    
    function render() {
        var scope = gs.getCurrentScopeName();
        scope = (scope == "rhino.global" ? "" : scope + "_");
        var page = renderer.getPreference('type');
        return renderer.getRenderedPage(scope + page);
    }
    
    function getEditLink() {
        var scope = gs.getCurrentScopeName();
        scope = (scope == "rhino.global" ? "" : scope + "_");
        var page = renderer.getPreference('type');
        return "sys_ui_page.do?sysparm_query=name=" + scope + page;
    }
    ```

6.  Click **Submit**.


## What to do next

[Edit a responsive dashboard](t_EditADashboard.md)

**Parent Topic:**[Widgets](../concept/widgets.md)

