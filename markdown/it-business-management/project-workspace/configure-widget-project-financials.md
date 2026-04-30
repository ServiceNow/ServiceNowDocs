---
title: Configure a widget for project financial metrics
description: Configure a widget to view and track the financial metrics of a project on the Financials tab of the Project Workspace page.
locale: en-US
release: yokohama
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [View forecasts and manage financial plans for a project, Project workspace classic - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Configure a widget for project financial metrics

Configure a widget to view and track the financial metrics of a project on the **Financials** tab of the Project Workspace page.

**Important:**

Classic Project Workspace is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Use new Project Workspace with enhanced UI to help you efficiently manage your projects.

## Before you begin

Role required: pps\_admin

## Procedure

1.  Navigate to **All** &gt; **Project Administration** &gt; **Widgets**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_osc_b4b_xhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the widget.

</td></tr><tr><td>

Scripted

</td><td>

Option for indicating the value on the widget is from a code script.By default, this option is selected and is read-only.

</td></tr><tr><td>

Show Label

</td><td>

Option for displaying either the label or the color indicator.If you clear the check box, the **Color** field appears and you can set the color.

</td></tr><tr><td>

Active

</td><td>

Option for indicating the status of the widget.Only active widgets can be shown on the **Financials** tab of the Project Workspace.

</td></tr><tr><td>

Parent widget

</td><td>

Widget that is the parent of the current widget.The current widget displays in the Child widgets related list of the selected widget.

 You can add a maximum of three child widgets for a parent widget.

</td></tr><tr><td>

Formatter required

</td><td>

Option for specifying whether a currency formatter is required for the widget.

</td></tr><tr><td>

Script

</td><td>

Code script that returns a requested metric value that is displayed on the widget.

 In the script, use the context and filter objects. The context object contains all of the project financial fields, such as capex\_costs, opex\_costs, and budget\_cost.

 The following sample script returns the Estimate At Completion metric value of a project to appear on the widget.

 ```
var context = JSON.parse(context);
var filter = context.filters;

var now_GR = new GlideRecord('pm_project');
gr.addEncodedQuery(filter['pm_project']);
gr.query();
if(gr.next())
	gr.getValue('forecast_cost');
Collapse
```

</td></tr><tr><td>

Short description

</td><td>

Description of the widget.

</td></tr></tbody>
</table>
## What to do next

[Associate the widget to the Project table](associate-widget-to-project.md).

-   **[Associate a widget to the Project table](associate-widget-to-project.md)**  
After you configure a widget, associate it with the Project table to show the financial data of a project.

**Parent Topic:**[View forecasts and manage financial plans for a project in classic Project Workspace](view-plan-financials-in-project-workspace.md)

