---
title: Widget New Record form
description: Use these form fields to create a new widget for your project administration.
locale: en-US
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Form field information for Strategic Planning, Reference, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Widget New Record form

Use these form fields to create a new widget for your project administration.

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
</table>**Parent Topic:**[Form field information for Strategic Planning](../../alignment-planner-workspace/reference/form-field-information-for-strategic-planning.md)

