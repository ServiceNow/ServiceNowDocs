---
title: Add Platform Analytics pages to a configurable workspace
description: Add an Analytics Center and its related pages to your own workspace through page templates.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Creating Platform Analytics pages, Platform Analytics]
---

# Add Platform Analytics pages to a configurable workspace

Add an Analytics Center and its related pages to your own workspace through page templates.

## Before you begin

Role required: ui\_builder\_admin

## About this task

In workspaces, the Analytics Center provides a central page with tabs for all the other pages related to Platform Analytics. You do not have to add an Analytics Center, but this procedure uses that page as example. The same procedure applies to adding the other Platform Analytics pages from templates. Details about those pages are provided at the end of this topic.

## Procedure

1.  Open your configurable workspace in the UI Builder.

2.  Scroll to the desired template.

    This procedure shows how to set up the Analytics Center template, but the instructions apply to any template, such as Dashboards.

3.  On the Select a Page Template dialog, expand **View legacy templates**.

4.  Hold your cursor over the Analytics Center template and select **Use template**.

    ![The Analytics Center template selected.](../../par-for-workspace/image/analytics-center-template.png)

5.  Specify a name and a path for the page.

6.  In the URL parameters page, press **Looks good**.

7.  Under Page parameters, add the following optional parameters:

    -   tab
    -   filter
    These parameters ensure that on page refresh, the last open tab of the Analytics Center opens. Also, the last selected filter \(such as **Bookmarked**\) is enabled.


## Result

You now have a page with a fully configured Analytics Center, including all components. However, none of the links to other pages work until those pages are added and configured.

## What to do next

Create pages using the following templates. Follow the same process you used to create the Analytics Center page, including using the original page instead of copying the content. Give the pages the following paths and parameters:

**Note:**

-   KPI Details, Simple List, and Dashboard overview are legacy page templates, like Analytics Center. You must specify the parameters manually for these pages. Newer page templates give you the parameters in the course of page creation.
-   Platform Analytics is modular. You can create only some of the pages and get their standalone functions. For example, if you only want dashboard support or KPI Details, create the pages with that functionality and don't create an Analytics Center.

<table id="table_c3v_3q3_k1c"><thead><tr><th>

Template name

</th><th>

Function

</th><th>

Required parameters

</th><th>

Optional parameters

</th><th>

Path

</th></tr></thead><tbody><tr><td>

KPI Details

</td><td>

Displays the details of a single indicator

</td><td>

uuid

</td><td>

scoreDate, breakdowns, domain, aggregate

</td><td>

ac\_kpi\_details

</td></tr><tr><td>

Simple List

</td><td>

Displays a list of table records

</td><td>

table

</td><td>

listTitle, query, disableInlineEditing, listView

</td><td>

simplelist

</td></tr><tr><td>

Standard record

</td><td>

Displays the details of a table record

</td><td>

table, sysId

</td><td>

query, extraParams, views, selectedTabIndex

</td><td>

record

</td></tr><tr><td>

Dashboard overview

</td><td>

Displays all dashboard tiles

</td><td>

none

</td><td>

none

</td><td>

all-dashboards

</td></tr><tr><td>

Dashboards \(see [Add a dashboard to a Dashboards page](add-dashboard-to-workspace.md)\)

</td><td>

Used to create, edit, and show dashboards along with data visualizations inside those dashboards. This page template is the minimum requirement for dashboard support.

</td><td>

none

</td><td>

edit, sysId, tabSysId, filter, element

</td><td>

dashboards

</td></tr><tr><td>

Visualization designer

</td><td>

Used to create and edit data visualizations independently of dashboards, without using the Dashboards editor.

</td><td>

sysid

</td><td>

none

</td><td>

visualization-designer

</td></tr></tbody>
</table>**Important:** You must use these paths, which are the same paths of the pages in the Platform Analytics experience. The preconfigured event handlers on the pages use these paths. If you do not give your pages these paths, the event handlers will not work.

**Parent Topic:**[Creating Platform Analytics pages in your own workspace](../concept/adding-analytics-center-to-ws.md)

**Related topics**  


[Create a Platform Analytics workspace from App Engine Studio](../concept/create-analytics-ws-aes.md)

[Add a dashboard to a Dashboards page](add-dashboard-to-workspace.md)

[Configure custom redirection from a dashboard component](config-custom-redirection-from-db.md)

[Add a dashboard to a Dashboards page](add-dashboard-to-workspace.md)

