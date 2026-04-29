---
title: Associate a widget to the Project table
description: After you configure a widget, associate it with the Project table to show the financial data of a project.
locale: en-US
release: australia
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure a widget for project financial metrics, View forecasts and manage financial plans for a project, Project workspace classic - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Associate a widget to the Project table

After you configure a widget, associate it with the Project table to show the financial data of a project.

**Important:**

Classic Project Workspace is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Use new Project Workspace with enhanced UI to help you efficiently manage your projects.

## Before you begin

You should [configure a widget](configure-widget-project-financials.md) before you can associate it with the Project \[pm\_project\] table.

Role required: pps\_admin

## Procedure

1.  Navigate to **All** &gt; **Project Administration** &gt; **Widgets**.

2.  Open a widget to associate with the Project table.

3.  In the Widget associations related list, click **New**.

4.  On the form, fill in the fields.

<table id="table_oc2_3zk_xbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Association ID

</td><td>

Record to associate to the widget.To access the relevant records, you must select the Tables \[sys\_db\_objects\] table in the **Table name** list and the Project \[pm\_project\] table in the **Document** list.

</td></tr><tr><td>

Association table

</td><td>

Table to associate to the widget.You must select Table \[sys\_db\_objects\] from the list.

</td></tr><tr><td>

Widget

</td><td>

Unique name of the widget.

</td></tr><tr><td>

Order

</td><td>

Position of the widget in relation to other widgets in the **Financials** tab of the Project Workspace. Widgets appear in numeric order with the smallest number listed first.

</td></tr><tr><td>

Display on card

</td><td>

Option to display the widget in the **Financials** tab.

</td></tr><tr><td>

Include by default

</td><td>

Option to show the widget by default in the **Financials** tab.

</td></tr></tbody>
</table>
**Parent Topic:**[Configure a widget for project financial metrics](configure-widget-project-financials.md)

